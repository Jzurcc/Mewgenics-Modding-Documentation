# Mewgenics Mod Developer Documentation: Engine: Passive IDs

> **Note on Math Equations:** Some keys labeled as `Number` actually support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Engine: Passive IDs

This document lists every confirmed Passive ID found across all game data files. These IDs are used as **dynamic keys** in any Passive Container block (e.g. `passives`, `bonus_passives`, `AddPassivesToMinions`). The value is either `true` (to simply grant the passive) or a Block overriding the passive's default configuration.

> **Note:** With 910+ unique passive IDs, this is one of the largest systems in the game. Many passives are the names of other blocks (e.g. `AddStatusToBasicAttack`) — granting the passive gives the character that reactive behaviour permanently.

### All Confirmed `{Passives}` Values

<details>
<summary><b>Expand</b></summary>

| ID | Type | Notes |
| :--- | :--- | :--- |
| `AIControlNextTurn` | Block | Applies or references the 'AIControlNextTurn' effect/state. |
| `AOEBonus` | Number | Applies or references the 'AOEBonus' effect/state. |
| `AbilityAfterEnemyCastSpell_Stackable` | Enum | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. |
| `AbilityChargeRefundChance` | Block | Applies the 'AbilityChargeRefundChance' effect. |
| `AbilityDamageMultiplier` | Number |  |
| `AbilityDisableIfLivingCrow` | Number | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. |
| `AbilityEnableIfConsumedCharacterHasTag` | Enum | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. |
| `AbilityEnabledAtHealthThreshold` | Number | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. |
| `AbilityEnabledIfHasStatus` | Enum | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. |
| `AbilityEnabledIfMovementTrapped` | Number | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. |
| `AbilityEnabledIfNoAggroTarget` | Number | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. |
| `AbilityEnabledIfNotHasStatus` | Enum | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. |
| `AbilityEnabledIfSpecificItemEquipped` | Enum | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. |
| `AbilityEnabledOncePerRound` | Number | Applies or references the 'AbilityEnabledOncePerRound' effect/state. |
| `AbilityEnabledPercentEachTurn` | Number | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. |
| `AbilityHealthThreshold` | Block | AI Trigger: Executes an ability when health drops below a specific threshold. |
| `AbilityInheritsWeaponEffects` | Number | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. |
| `AbilityOnBattleStart` | Enum | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AbilityOnBattleStart_UseAI` | Enum | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. |
| `AbilityOnRoundEnd` | Block | AI Trigger: Executes an ability at the end of the combat round. |
| `AbilityOnRoundEndOnce` | Block | Applies or references the 'AbilityOnRoundEndOnce' effect/state. |
| `AbilityReaction` | Enum | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). |
| `AbilityWhenBuddyDies` | Enum | Applies or references the 'AbilityWhenBuddyDies' effect/state. |
| `AbilityWhenTaggedCharacterMovesNear` | Block | AI Trigger: Executes an ability when a character with a specific tag moves adjacent. |
| `AbsorbManaAura` | Number | Applies the 'AbsorbManaAura' effect. |
| `AbsorbManaFromOtherSpells` | Number | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. |
| `AddAdvantageToEvent` | Block | Applies or references the 'AddAdvantageToEvent' effect/state. |
| `AddAllyNeighborsToAbilityRange` | Number | Applies the 'AddAllyNeighborsToAbilityRange' effect. |
| `AddAllyNeighborsToAttackRange` | Number | Applies the 'AddAllyNeighborsToAttackRange' effect. |
| `AddBonusMeleeRange` | Number | Applies the 'AddBonusMeleeRange' effect. |
| `AddBonusRange` | Number | Applies or references the 'AddBonusRange' effect/state. |
| `AddChaScalingSpellDamage` | Number | Applies the 'AddChaScalingSpellDamage' effect. |
| `AddConstitution` | Number |  |
| `AddCorpseHealth` | Number | Applies the 'AddCorpseHealth' effect. |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. |
| `AddDamageToBasicAttack` | Number | Applies the 'AddDamageToBasicAttack' effect. |
| `AddDamageToElementDamage` | Block | Applies or references the 'AddDamageToElementDamage' effect/state. |
| `AddElementsToBasicAttack` | Enum |  |
| `AddElementsToSpells` | Enum | Applies or references the 'AddElementsToSpells' effect/state. |
| `AddEndOfCombatRegen` | Number | Applies or references the 'AddEndOfCombatRegen' effect/state. |
| `AddHiddenTag` | Enum | Applies or references the 'AddHiddenTag' effect/state. |
| `AddInitiative` | Number | Applies or references the 'AddInitiative' effect/state. |
| `AddKnockbackDamage` | Number | Applies or references the 'AddKnockbackDamage' effect/state. |
| `AddKnockbackToEverything` | Number | Applies the 'AddKnockbackToEverything' effect. |
| `AddLevelUpRerolls` | Number | Applies or references the 'AddLevelUpRerolls' effect/state. |
| `AddLevelUpStatMultiplier` | Number | Applies the 'AddLevelUpStatMultiplier' effect. |
| `AddLootMultiplier` | Number |  |
| `AddManaRegen` | Number | Applies or references the 'AddManaRegen' effect/state. |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. |
| `AddMeleeKnockback` | Number | Applies or references the 'AddMeleeKnockback' effect/state. |
| `AddMovement` | Number | Applies or references the 'AddMovement' effect/state. |
| `AddPassiveToSpawnedRocks` | Block | Applies the 'AddPassiveToSpawnedRocks' effect. |
| `AddPassivesToCharmed` | Block | Applies the 'AddPassivesToCharmed' effect. |
| `AddPassivesToMinions` | Block | Applies the 'AddPassivesToMinions' effect. |
| `AddPassivesToSummonAbilityMinions` | Block | Applies the 'AddPassivesToSummonAbilityMinions' effect. |
| `AddRangedCritChance` | Number | Applies the 'AddRangedCritChance' effect. |
| `AddSelfStatusToBasicAttack` | Block | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. |
| `AddSelfStatusToWeapons` | Block | Applies the 'AddSelfStatusToWeapons' effect. |
| `AddSpeed` | Number | Applies the 'AddSpeed' effect. |
| `AddSpellDamage` | Number | Applies the 'AddSpellDamage' effect. |
| `AddStartingMana` | Number | Applies the 'AddStartingMana' effect. |
| `AddStatusToAllDamage` | Block | Modifier: Injects a status effect into a specific action. |
| `AddStatusToAllDamageAbilities` | Block | Applies the 'AddStatusToAllDamageAbilities' effect. |
| `AddStatusToBackstabs` | Block | Modifier: Injects a status effect into a specific action. |
| `AddStatusToBasicAttack` | Block | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `AddStatusToBasicAttackWithCooldown` | Block | Applies the 'AddStatusToBasicAttackWithCooldown' effect. |
| `AddStatusToBasicMeleeAttack` | Block |  |
| `AddStatusToElementAbilities` | Block | Applies the 'AddStatusToElementAbilities' effect. |
| `AddStatusToElementDamage` | Block | Applies the 'AddStatusToElementDamage' effect. |
| `AddStatusToExplosions` | Block | Applies the 'AddStatusToExplosions' effect. |
| `AddStatusToFirstBasicAttack` | Block | Applies the 'AddStatusToFirstBasicAttack' effect. |
| `AddStatusToFirstSpellEachTurn` | Block |  |
| `AddStatusToKnockbackDamage` | Block | Modifier: Injects a status effect into a specific action. |
| `AddStatusToMeleeDamage` | Block | Applies the 'AddStatusToMeleeDamage' effect. |
| `AddStatusToReceivedDamage` | Block | Modifier: Applies a status effect whenever the character takes damage. |
| `AddStatusToReceivedDamage_ExcludeStatuses` | Block | Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect. |
| `AddStatusToSpells` | Block | Modifier: Injects a status effect into a specific action. |
| `AddStatusToTrampleDamage` | Block | Applies the 'AddStatusToTrampleDamage' effect. |
| `AddStatusToWeapons` | Block | Applies the 'AddStatusToWeapons' effect. |
| `AddStatusesIfPersistentWeatherElement` | Block | Applies the 'AddStatusesIfPersistentWeatherElement' effect. |
| `AddStatusesToReceivedElementalDamage` | Block | Applies the 'AddStatusesToReceivedElementalDamage' effect. |
| `AddTag` | Enum | Applies or references the 'AddTag' effect/state. |
| `AddTemporaryEffectsToBasicAttack` | Block | Applies the 'AddTemporaryEffectsToBasicAttack' effect. |
| `AddTemporaryEffectsToEquipment` | Block | Applies the 'AddTemporaryEffectsToEquipment' effect. |
| `AddUnfilledMaxHealth` | Number | Applies the 'AddUnfilledMaxHealth' effect. |
| `AddWeaponScaling` | Number | Applies the 'AddWeaponScaling' effect. |
| `AdvancedTint` | Array | Applies or references the 'AdvancedTint' effect/state. |
| `AdventureTokenPassivePool` | Block | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. |
| `AfterImage` | Enum | Spawns a visual decoy or shade at the caster's previous location. |
| `AggroTargetIsBuddy` | Number | Applies or references the 'AggroTargetIsBuddy' effect/state. |
| `AggroTargetIsCurrentTurn` | Number | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. |
| `AggroTargetIsGovernedByHitEffect` | Block | AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity. |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. |
| `AggroTargetIsLowestMaxHealthCat` | Number | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. |
| `AlienBeastDangerZones` | Array | Applies or references the 'AlienBeastDangerZones' effect/state. |
| `AlienBeastEyeStalks` | Number | Applies or references the 'AlienBeastEyeStalks' effect/state. |
| `AllDamageCrits` | Number | Applies the 'AllDamageCrits' effect. |
| `AllDamageImmune_IncludingSpeculative` | Number | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. |
| `AllSpellsCostActPoints` | Number | Applies or references the 'AllSpellsCostActPoints' effect/state. |
| `AllSpellsCostCharge` | Number | Applies or references the 'AllSpellsCostCharge' effect/state. |
| `AllStatsAura` | Block | Passive: Projects an aura that modifies all primary stats of nearby characters. |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. |
| `AllStatsUpPerDisorder` | Number | Applies or references the 'AllStatsUpPerDisorder' effect/state. |
| `AllUnitsExplodeOnDeath` | Number | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. |
| `AlliesAvoidTraps` | Number | Applies the 'AlliesAvoidTraps' effect. |
| `AlliesScrambleSpellAfterCast` | Number | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. |
| `AllowPassTurn` | Number | Applies the 'AllowPassTurn' effect. |
| `AlluringDoodieEater` | Block | Applies or references the 'AlluringDoodieEater' effect/state. |
| `AllyBonusAbilityAura` | Enum | Applies the 'AllyBonusAbilityAura' effect. |
| `AllyChainKnockback` | Number | Applies the 'AllyChainKnockback' effect. |
| `AllyDamageReaction` | Enum | Applies the 'AllyDamageReaction' effect. |
| `AllyDamageReduction` | Number | Applies the 'AllyDamageReduction' effect. |
| `AllyDodgeChanceAura` | Block | Applies or references the 'AllyDodgeChanceAura' effect/state. |
| `AllyHealthRegenAura` | Block | Applies the 'AllyHealthRegenAura' effect. |
| `AllyManaRegenAura` | Block | Applies the 'AllyManaRegenAura' effect. |
| `AllyMoveAbilityAura` | Enum | Applies the 'AllyMoveAbilityAura' effect. |
| `AllyMultiplyKnockbackDamage` | Number | Applies the 'AllyMultiplyKnockbackDamage' effect. |
| `AllyMultiplyKnockbackDistance` | Number | Applies the 'AllyMultiplyKnockbackDistance' effect. |
| `AllyUncappedHPAura` | Number | Applies the 'AllyUncappedHPAura' effect. |
| `AlphaAllStatsUp` | Number | Applies or references the 'AlphaAllStatsUp' effect/state. |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. |
| `AlphaDodgeChance` | Number | Applies or references the 'AlphaDodgeChance' effect/state. |
| `AlphaStatusOnTurnBegin` | Block | Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. |
| `AlphaTurns` | Number | Applies the 'AlphaTurns' effect. |
| `AlternateCraftingPools` | Block | Applies the 'AlternateCraftingPools' effect. |
| `AlwaysChosenForLevelUp` | Number | Applies or references the 'AlwaysChosenForLevelUp' effect/state. |
| `AlwaysHitDifferentTargets` | Number | Applies or references the 'AlwaysHitDifferentTargets' effect/state. |
| `Ammo` | Number | Applies or references the 'Ammo' effect/state. |
| `AmplifyKnockback` | Number | Applies the 'AmplifyKnockback' effect. |
| `AmplifyNegativeStatus` | Number | Applies the 'AmplifyNegativeStatus' effect. |
| `AmplifyPositiveStatus` | Number | Applies the 'AmplifyPositiveStatus' effect. |
| `AmplifyStatus` | Enum | Applies the 'AmplifyStatus' effect. |
| `Angel` | Number | Applies or references the 'Angel' effect/state. |
| `ApplyPassivesToSpawnerWhileAlive` | Block | Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. |
| `ApplyStatusesToRandomEnemiesEachTurn` | Block | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. |
| `ArmorBreakOnHit` | Block | Applies or references the 'ArmorBreakOnHit' effect/state. |
| `ArmorDodgeChance` | Number | Applies or references the 'ArmorDodgeChance' effect/state. |
| `ArmorPickup` | Block | Pickup Logic: Defines what happens when an armor item is collected. |
| `Autism` | Block | Applies the 'Autism' effect. |
| `AutoCritLowDamage` | Number | Applies the 'AutoCritLowDamage' effect. |
| `AutoEquipConsumables` | Number | Applies or references the 'AutoEquipConsumables' effect/state. |
| `AutocastEachRound` | Block | Forces the character to automatically cast a specific ability at the start of each combat round. |
| `AutocastEachTurn` | Enum | Applies the 'AutocastEachTurn' effect. |
| `AutocastEachTurnBegin` | Enum | Applies the 'AutocastEachTurnBegin' effect. |
| `AvoidDamagingCharmedEnemies` | Number | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. |
| `AwardCoinsOnDeath` | Number | Applies or references the 'AwardCoinsOnDeath' effect/state. |
| `BackflipWhenTargeted` | Block |  |
| `BackstabAllDirections` | Number | Applies or references the 'BackstabAllDirections' effect/state. |
| `BackstabCritChance` | Number | Applies the 'BackstabCritChance' effect. |
| `BackstabFront` | Number |  |
| `BackstabImmunity` | Number | Applies or references the 'BackstabImmunity' effect/state. |
| `BackstabWeakness` | Number | Applies the 'BackstabWeakness' effect. |
| `BaitAura` | Block | Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots). |
| `BalanceStats` | Number | Applies or references the 'BalanceStats' effect/state. |
| `BaseStatMultiply` | Enum | Applies or references the 'BaseStatMultiply' effect/state. |
| `BasicAIDangerZone` | Number | Applies or references the 'BasicAIDangerZone' effect/state. |
| `BasicAttackAOEBonus` | Number | Applies the 'BasicAttackAOEBonus' effect. |
| `BasicAttackCantMiss` | Number |  |
| `BasicAttackCritChance` | Number | Applies the 'BasicAttackCritChance' effect. |
| `BasicAttackDamageMultiplier` | Number | Applies the 'BasicAttackDamageMultiplier' effect. |
| `BasicAttackStatusCarefulness` | Number | Applies the 'BasicAttackStatusCarefulness' effect. |
| `BasicAttackStatusSwap` | Array | Applies the 'BasicAttackStatusSwap' effect. |
| `BattlefieldUniqueRandomPassive` | Block | Map Rule: Grants a unique random passive modifier to the battlefield. |
| `Bird` | Enum | Applies or references the 'Bird' effect/state. |
| `BirdRewards` | Block | Loot logic: Rewards dropped by bird-type enemies. |
| `BlackHolePassive` | Number | Applies or references the 'BlackHolePassive' effect/state. |
| `BlacklistPickupType` | Enum |  |
| `BlastResistance` | Number | Applies the 'BlastResistance' effect. |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. |
| `Blind` | Number |  |
| `BloatEyePassive2` | Enum | Applies or references the 'BloatEyePassive2' effect/state. |
| `BlockAllDamage` | Number | Applies or references the 'BlockAllDamage' effect/state. |
| `BlockDamageUnderThreshold` | Number | Applies or references the 'BlockDamageUnderThreshold' effect/state. |
| `BlockNegativeStatus` | Number | Applies or references the 'BlockNegativeStatus' effect/state. |
| `BombBehavior` | Number | Applies or references the 'BombBehavior' effect/state. |
| `BoneArmorPassive` | Number | Applies or references the 'BoneArmorPassive' effect/state. |
| `BonusAbility` | Enum | Applies the 'BonusAbility' effect. |
| `BonusAbility_DelayedApplication` | Enum | Applies or references the 'BonusAbility_DelayedApplication' effect/state. |
| `BonusFoodEachBattle` | Number | Applies the 'BonusFoodEachBattle' effect. |
| `BonusHealthRegenBasedOnDex` | Number | Applies the 'BonusHealthRegenBasedOnDex' effect. |
| `BonusHealthRegenPerDisorder` | Number |  |
| `BonusRangeBasedOnDex` | Number | Applies the 'BonusRangeBasedOnDex' effect. |
| `BonusTurnPattern` | Array | Applies or references the 'BonusTurnPattern' effect/state. |
| `BoobyTrapItems` | Block | Applies the 'BoobyTrapItems' effect. |
| `BoostAllyStatsOnDeath` | Number | Applies the 'BoostAllyStatsOnDeath' effect. |
| `BoostDamageAura` | Number | Applies the 'BoostDamageAura' effect. |
| `BoostDamageGlobalAura` | Number | Applies the 'BoostDamageGlobalAura' effect. |
| `BoostHeals` | Number | Applies or references the 'BoostHeals' effect/state. |
| `BoostRangeAura` | Number | Applies the 'BoostRangeAura' effect. |
| `BoostRangeGlobalAura` | Number | Applies the 'BoostRangeGlobalAura' effect. |
| `BoostReceivedHealing` | Number | Applies or references the 'BoostReceivedHealing' effect/state. |
| `BoostWeaponDamage` | Number | Applies the 'BoostWeaponDamage' effect. |
| `BossRewards` | Block | Loot logic: Rewards dropped upon defeating a boss. |
| `BouncyProjectiles` | Block | Applies the 'BouncyProjectiles' effect. |
| `Brace` | Number | Applies or references the 'Brace' effect/state. |
| `BraceForEachNeighboringEnemy` | Number | Applies the 'BraceForEachNeighboringEnemy' effect. |
| `BreakAtAux` | Number | Applies or references the 'BreakAtAux' effect/state. |
| `BreakOnElement` | Enum | Applies or references the 'BreakOnElement' effect/state. |
| `BreakWhenNoShield` | Number | Applies or references the 'BreakWhenNoShield' effect/state. |
| `Brittle` | Number | Applies or references the 'Brittle' effect/state. |
| `BrittleDuringElement` | Enum | Applies or references the 'BrittleDuringElement' effect/state. |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. |
| `Buddy` | Enum | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. |
| `BuffImmunity` | Number | Applies or references the 'BuffImmunity' effect/state. |
| `BungaCheers` | Block | Animation/AI State: Bunga cheering animation logic. |
| `BungaEntrance` | Block | Animation/AI State: Bunga entering the arena. |
| `Burn` | Number | Applies or references the 'Burn' effect/state. |
| `CCImmunity` | Number | Applies the 'CCImmunity' effect. |
| `CanLevelUpWhenDead` | Number | Applies or references the 'CanLevelUpWhenDead' effect/state. |
| `CanMutateTo` | Array | Applies or references the 'CanMutateTo' effect/state. |
| `CanRemoveCursedItems` | Number |  |
| `CanShield` | Number | Applies or references the 'CanShield' effect/state. |
| `CantCatchDiseases` | Number | Applies or references the 'CantCatchDiseases' effect/state. |
| `CantDodge` | Number | Applies the 'CantDodge' effect. |
| `CantSpreadDiseases` | Number | Applies or references the 'CantSpreadDiseases' effect/state. |
| `CapBasicAttackDamage` | Number | Applies or references the 'CapBasicAttackDamage' effect/state. |
| `CapDamageFromAllies` | Number | Applies the 'CapDamageFromAllies' effect. |
| `CapMovementAbilityRange` | Number | Applies or references the 'CapMovementAbilityRange' effect/state. |
| `CapReceivedDamage` | Number | Applies or references the 'CapReceivedDamage' effect/state. |
| `CapTechSpent` | Number | Applies the 'CapTechSpent' effect. |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. |
| `CatAPultAnimation` | Block | Applies the 'CatAPultAnimation' effect. |
| `CatPartsSizeScale` | Block | Applies or references the 'CatPartsSizeScale' effect/state. |
| `CatPartsTransform` | Block | Visual: Transforms specific body parts of the character. |
| `CatchBoomerang` | Number | Applies or references the 'CatchBoomerang' effect/state. |
| `CatchProjectiles` | Block | Applies or references the 'CatchProjectiles' effect/state. |
| `CaveFamilyEnrage` | Block | AI Trigger: Enrage logic triggered when a cave family member is killed. |
| `CaveWomanBirthControl` | Number | Applies or references the 'CaveWomanBirthControl' effect/state. |
| `CerberubsAggroTargetBehavior` | Block | AI Logic: Custom aggro targeting rules for Cerberubs. |
| `ChainKnockback` | Number | Applies the 'ChainKnockback' effect. |
| `ChanceToAmbush` | Number | Applies or references the 'ChanceToAmbush' effect/state. |
| `ChanceToBackflip` | Block | Applies or references the 'ChanceToBackflip' effect/state. |
| `ChanceToBlock` | Number | Applies or references the 'ChanceToBlock' effect/state. |
| `ChanceToBlockAndCounter` | Block | Applies or references the 'ChanceToBlockAndCounter' effect/state. |
| `ChanceToDisableActionsIfNotCharmed` | Number | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. |
| `ChanceToForceEvent` | Block | Applies or references the 'ChanceToForceEvent' effect/state. |
| `ChanceToFormChangeOnAbilityDamage` | Block | Reaction: Probability to change forms when taking ability damage. |
| `ChanceToRevive` | Number | Applies or references the 'ChanceToRevive' effect/state. |
| `ChanceToSpitOnDamage` | Block | Reaction: Probability to use a spit counter-attack when damaged. |
| `ChangeTauntPriority` | Number | Applies the 'ChangeTauntPriority' effect. |
| `ChangeTileOnDeath` | Enum | Applies or references the 'ChangeTileOnDeath' effect/state. |
| `ChangeTileOnPop` | Enum | Applies or references the 'ChangeTileOnPop' effect/state. |
| `ChaosBossFormChangeGuide` | Block | Boss Logic: Maps the form transition phases for the Chaos Boss. |
| `ChaosBossPieces` | Block | Boss Logic: Defines the separate destructible pieces of the Chaos Boss. |
| `ChaosHeadDropIn` | Block | Boss Logic: Drop-in attack/animation for the Chaos Head. |
| `CharacterLightSource` | Block | Visual: Attaches a dynamic lighting source to the character. |
| `Charge` | Number | Applies or references the 'Charge' effect/state. |
| `ChargeSpiritBombAura` | Enum | Applies or references the 'ChargeSpiritBombAura' effect/state. |
| `CharismaIsMaxStat` | Number | Applies or references the 'CharismaIsMaxStat' effect/state. |
| `CharismaUp` | Number | Applies the 'CharismaUp' effect. |
| `CharmAllFlies` | Number | Applies the 'CharmAllFlies' effect. |
| `CharmImmunity` | Number | Applies or references the 'CharmImmunity' effect/state. |
| `CherubimReaction` | Block | Reaction: Custom reaction triggers for Cherubim enemies. |
| `ClassManaCostReduction` | Block | Applies or references the 'ClassManaCostReduction' effect/state. |
| `CobraReflex` | Enum | Applies the 'CobraReflex' effect. |
| `CoinPickup` | Number | Applies or references the 'CoinPickup' effect/state. |
| `CoinsAddDamage` | Number | Applies the 'CoinsAddDamage' effect. |
| `CollectPickupsOnBattleEnd` | Number | Applies the 'CollectPickupsOnBattleEnd' effect. |
| `Conductor` | Number | Applies the 'Conductor' effect. |
| `ConductorManaRegen` | Number | Applies the 'ConductorManaRegen' effect. |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. |
| `ConfusionEffectOnTaggedAbilities` | Enum | Applies the 'ConfusionEffectOnTaggedAbilities' effect. |
| `ConjureBonusAbility` | Enum |  |
| `ConjureCastSpellsForAllies` | Number | Applies the 'ConjureCastSpellsForAllies' effect. |
| `ConsumableEffectsMultiplierBonus` | Number | Applies the 'ConsumableEffectsMultiplierBonus' effect. |
| `ConsumablesInfiniteRange` | Number | Applies the 'ConsumablesInfiniteRange' effect. |
| `ConsumablesMeleeRange` | Number | Applies the 'ConsumablesMeleeRange' effect. |
| `ConvertDamageToScaledStatus` | Block | Applies or references the 'ConvertDamageToScaledStatus' effect/state. |
| `CopyBasicAttackEffects` | Number | Applies or references the 'CopyBasicAttackEffects' effect/state. |
| `CopyCatPassive_Initializer` | Number | Applies or references the 'CopyCatPassive_Initializer' effect/state. |
| `CopyPassiveSlot` | Number | Applies or references the 'CopyPassiveSlot' effect/state. |
| `CountAsCorpse` | Number | Applies or references the 'CountAsCorpse' effect/state. |
| `CounterAttack` | Enum | Reaction: Executes a counter-attack ability when hit. |
| `CounterAttackAfterEnemyCastSpell` | Enum | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. |
| `CounterNextAttacks` | Number | Applies or references the 'CounterNextAttacks' effect/state. |
| `CreateGlobalModifiers` | Block | Encounter Rule: Generates map-wide modifiers. |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. |
| `CritsApplyStatus` | Block | Applies the 'CritsApplyStatus' effect. |
| `CrowAttackLink` | Number | Applies or references the 'CrowAttackLink' effect/state. |
| `CyborgTurns` | Block |  |
| `DamageEnemiesOnHeal` | Number | Combat Trigger: Deals damage to enemies on heal. |
| `DamageEnemiesOnKill` | Number | Combat Trigger: Deals damage to enemies on kill. |
| `DamageFromBehindOnly` | Number | Applies or references the 'DamageFromBehindOnly' effect/state. |
| `DamageIfDidntUseSpecificAbility` | Block | Combat Trigger: Deals damage to if didnt use specific ability. |
| `DamageNeighborTilesWhenCastSpell` | Block | Combat Trigger: Deals damage to neighbor tiles when cast spell. |
| `DamageNeighborsAfterMove` | Block |  |
| `DamageNeighborsOnEndMove` | Block | Combat Trigger: Deals damage to neighbors on end move. |
| `DamageReductionAura` | Block | Combat Trigger: Deals damage to reduction aura. |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. |
| `DeadAltAbility` | Enum | Applies or references the 'DeadAltAbility' effect/state. |
| `DeathChill` | Number | Applies the 'DeathChill' effect. |
| `DeathRattle` | Enum | Event Trigger: Executes logic or abilities exactly when the character dies. |
| `DeathRattleRevive` | Block | Event Trigger: Revives the character immediately upon death. |
| `DebuffImmunity` | Number | Applies or references the 'DebuffImmunity' effect/state. |
| `DejaVu` | Number | Applies the 'DejaVu' effect. |
| `DelayedAutoRevive` | Block | Applies or references the 'DelayedAutoRevive' effect/state. |
| `DemonicGlyphFrames` | Number | Applies or references the 'DemonicGlyphFrames' effect/state. |
| `DemonicGlyphStealer` | Number | Applies or references the 'DemonicGlyphStealer' effect/state. |
| `DepressionAura` | Block |  |
| `Diabetes` | Block | Applies the 'Diabetes' effect. |
| `DiceBehavior` | Block | AI Logic: Custom behavior for Dice enemies. |
| `DicerArt` | Array | Applies or references the 'DicerArt' effect/state. |
| `DieWhenOnlyGolemsLeft` | Number | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. |
| `DieWhenSpawnerDies` | Number | Applies or references the 'DieWhenSpawnerDies' effect/state. |
| `DiesToElement` | Block | Vulnerability: Character dies instantly if hit by this element. |
| `DiesToPiercingAndSpikes` | Block | Vulnerability: Character dies instantly if hit by piercing attacks or spikes. |
| `DigestDeadBodies` | Enum | Applies or references the 'DigestDeadBodies' effect/state. |
| `DirtyClaws` | Number | Applies the 'DirtyClaws' effect. |
| `DisableAbilities` | Enum | Applies or references the 'DisableAbilities' effect/state. |
| `DisableAbilitiesWithTag` | Enum |  |
| `DisablePassiveSlot` | Number | Applies or references the 'DisablePassiveSlot' effect/state. |
| `DisableSpells` | Number | Applies or references the 'DisableSpells' effect/state. |
| `Disguised` | Number | Applies or references the 'Disguised' effect/state. |
| `DisguisedTrapper` | Enum | Applies or references the 'DisguisedTrapper' effect/state. |
| `DisplayBuddyCatOnSpawn` | Number | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. |
| `DisplayDangerAOE` | Enum | Applies or references the 'DisplayDangerAOE' effect/state. |
| `DissuadeInstakills` | Number | Applies or references the 'DissuadeInstakills' effect/state. |
| `Divide4OnDeath` | Enum | Applies or references the 'Divide4OnDeath' effect/state. |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. |
| `DivineShieldPickup` | Number | Applies or references the 'DivineShieldPickup' effect/state. |
| `DodgeChance` | Number |  |
| `DodgeChanceWithBlindSpot` | Number | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. |
| `DodgeWhenTargeted` | Block | Reaction: Executes a dodge maneuver when targeted. |
| `Doomed` | Number | Applies the 'Doomed' effect. |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number |  |
| `DoubleCastTaggedSpells` | Enum | Applies or references the 'DoubleCastTaggedSpells' effect/state. |
| `DoubleCastWeapons` | Number | Applies the 'DoubleCastWeapons' effect. |
| `DoubleReceivedNegativeStatus` | Number | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. |
| `DoubleReceivedPositiveStatus` | Number | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. |
| `DownRankAIIfWeaponUsable` | Enum | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. |
| `DrinkWater` | Number |  |
| `DropAsFamiliarOnArmorBreak` | Enum | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. |
| `DropAsFamiliarOnTookDamage` | Enum | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. |
| `DropSoulJarOnDeath` | Enum | Applies or references the 'DropSoulJarOnDeath' effect/state. |
| `DukeOfFlies` | Number | Applies the 'DukeOfFlies' effect. |
| `DurabilityTransform` | Block | Applies or references the 'DurabilityTransform' effect/state. |
| `DustCloudBehavior` | Number | Applies or references the 'DustCloudBehavior' effect/state. |
| `Dybbuk1HPTracker` | Number | Applies or references the 'Dybbuk1HPTracker' effect/state. |
| `DybbukPossessionFallback` | Block | Logic: Fallback state when a Dybbuk possession fails. |
| `Dyslexia` | Array | Applies the 'Dyslexia' effect. |
| `EMP` | Block | Applies the 'EMP' effect. |
| `EachSpellFreeAtFullMana` | Number | Applies the 'EachSpellFreeAtFullMana' effect. |
| `ElectricArcs` | Number | Applies or references the 'ElectricArcs' effect/state. |
| `ElementImmune` | Enum | Applies or references the 'ElementImmune' effect/state. |
| `ElementWeakness` | Enum | Applies or references the 'ElementWeakness' effect/state. |
| `ElementalAttunement` | Block | Applies the 'ElementalAttunement' effect. |
| `ElementalManaCostReduction` | Block | Applies the 'ElementalManaCostReduction' effect. |
| `EliteFlatTint` | Array |  |
| `EliteParticle` | Enum |  |
| `EliteTint` | Array |  |
| `Empath` | Number | Applies the 'Empath' effect. |
| `EnemiesGetPickupsKnockedOut` | Number | Applies the 'EnemiesGetPickupsKnockedOut' effect. |
| `EnergyStorm` | Number | Applies the 'EnergyStorm' effect. |
| `EnrageOnDamage` | Number | Applies or references the 'EnrageOnDamage' effect/state. |
| `EquipRandomTemporaryItemFromPool` | Enum |  |
| `EquipTemporaryItem` | Enum | Applies the 'EquipTemporaryItem' effect. |
| `EquipmentPassiveMultiplierBonus` | Number | Applies the 'EquipmentPassiveMultiplierBonus' effect. |
| `EquipmentSetBonusBonus` | Number | Applies the 'EquipmentSetBonusBonus' effect. |
| `EraseSpawnCoins` | Number | Applies or references the 'EraseSpawnCoins' effect/state. |
| `EscapeSequence` | Block | Applies the 'EscapeSequence' effect. |
| `Eternal` | Block | Applies the 'Eternal' effect. |
| `EventBounterHunterPassive` | Number | Applies or references the 'EventBounterHunterPassive' effect/state. |
| `ExcludeFromEvents` | Enum | Applies or references the 'ExcludeFromEvents' effect/state. |
| `ExhaustionRoundChange` | Number | Applies the 'ExhaustionRoundChange' effect. |
| `ExpireOnSpawnerTurnEnd` | Number | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. |
| `ExplodeOverkilledEnemies` | Number | Applies the 'ExplodeOverkilledEnemies' effect. |
| `ExplosionImmunity` | Number | Applies or references the 'ExplosionImmunity' effect/state. |
| `ExtraBasicAttacks` | Number | Applies the 'ExtraBasicAttacks' effect. |
| `ExtraBasicAttacks_Status` | Number | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `ExtraDispersedTurns` | Number | Applies or references the 'ExtraDispersedTurns' effect/state. |
| `ExtraInjuryOnDeath` | Number | Applies the 'ExtraInjuryOnDeath' effect. |
| `ExtraMovePoints` | Number | Applies the 'ExtraMovePoints' effect. |
| `ExtraStatusWhenDealingDamage` | Block | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. |
| `ExtraTrinketUses` | Number | Applies or references the 'ExtraTrinketUses' effect/state. |
| `ExtraTurnsPerTaggedUnit` | Enum | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. |
| `ExtraWeaponAttacks` | Number | Applies the 'ExtraWeaponAttacks' effect. |
| `FaceArmorPassiveMultiplierBonus` | Number | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. |
| `FaceAwayLastDamage` | Block | Reaction: Forces the character to face away from the last damage source. |
| `FaceLastDamage` | Number | Reaction: Forces the character to face towards the last damage source. |
| `FaceShield` | Number | Applies or references the 'FaceShield' effect/state. |
| `FadeInsteadOfDie` | Number | Applies or references the 'FadeInsteadOfDie' effect/state. |
| `FamiliarBonusAbility` | Enum | Applies the 'FamiliarBonusAbility' effect. |
| `FamiliarSecondaryDamageImmunity` | Number | Applies the 'FamiliarSecondaryDamageImmunity' effect. |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. |
| `FinalBossBeamQueue` | Block | Boss Logic: Attack queue for the final boss beam. |
| `FinalBossBecomeTheChild` | Block | Boss Logic: Phase transition for the final boss. |
| `FinalBossHitCountdownBoris` | Block | Boss Logic: Countdown trigger for Boris. |
| `FinalBossHitCountdownExplosive` | Block | Boss Logic: Countdown trigger for explosives. |
| `FinalBossHitCountdownHoly` | Block | Boss Logic: Countdown trigger for holy attacks. |
| `FinalBossPupils` | Block | Boss Logic: Pupil state management. |
| `FinalBossShield` | Enum | Applies or references the 'FinalBossShield' effect/state. |
| `FinalBossShieldHealth` | Block | Boss Logic: Shield health management. |
| `FinalBossSyncAnimations` | Block | Boss Logic: Synchronizes multi-part boss animations. |
| `FindExtraItemFromPoolOnBattleEnd` | Enum | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. |
| `FistOfFateUniqueEnemyTracker` | Number | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. |
| `Flammable` | Number | Applies or references the 'Flammable' effect/state. |
| `FlatHealWhenDealDamage` | Number |  |
| `FlingObjectsOnTop` | Number | Applies or references the 'FlingObjectsOnTop' effect/state. |
| `FlowerPowerAuraBrace` | Number | Applies the 'FlowerPowerAuraBrace' effect. |
| `FlowerPowerAuraStrength` | Number | Applies the 'FlowerPowerAuraStrength' effect. |
| `FlowersOnEndTurn` | Number | Applies or references the 'FlowersOnEndTurn' effect/state. |
| `FlushmasterCelebration` | Enum | Applies or references the 'FlushmasterCelebration' effect/state. |
| `FlyDamageIncrease` | Number | Applies the 'FlyDamageIncrease' effect. |
| `Flying` | Number | Applies or references the 'Flying' effect/state. |
| `FollowUp` | Enum | Applies the 'FollowUp' effect. |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. |
| `ForceDodgeEverything` | Number | Applies or references the 'ForceDodgeEverything' effect/state. |
| `ForceSpecificInjury` | Equation | Applies the 'ForceSpecificInjury' effect. |
| `ForceUseAbility` | Enum | Applies the 'ForceUseAbility' effect. |
| `FormChange` | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FormChangeDuringWeatherElement` | Block | Logic: Changes form automatically during specific weather conditions. |
| `FormChangeHealthThreshold` | Block | Logic: Changes form when health crosses a threshold. |
| `FormChangeOffMap` | Block | Logic: Changes form when pushed off the map. |
| `FormChangeOnElementInfluence` | Block | Logic: Changes form when affected by an element. |
| `FormChangeWhenBuddyDies` | Enum | Applies or references the 'FormChangeWhenBuddyDies' effect/state. |
| `FormChangeWhileHasStatus` | Block | Logic: Changes form automatically while possessing a specific status. |
| `FormChangeWhilePrimingAbility` | Block | Logic: Changes form while preparing/priming a specific ability. |
| `FormChanger` | Block | AI Role: Designates the character as one that frequently shifts forms. |
| `Fragile` | Number | Applies or references the 'Fragile' effect/state. |
| `FragileDuringElement` | Enum | Applies or references the 'FragileDuringElement' effect/state. |
| `FrankBolts` | Number | Applies or references the 'FrankBolts' effect/state. |
| `FreeFirstCast` | Number | Applies or references the 'FreeFirstCast' effect/state. |
| `FreeFirstCastAndAfterSpendMana` | Number | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. |
| `FreeFirstCastEachMatch` | Number | Applies or references the 'FreeFirstCastEachMatch' effect/state. |
| `FreePathfindElement` | Enum | Applies the 'FreePathfindElement' effect. |
| `FreeSpellsAtFullMana` | Number | Applies the 'FreeSpellsAtFullMana' effect. |
| `FreezePiercing` | Number | Applies the 'FreezePiercing' effect. |
| `FrontstabBasicAttackCritChance` | Number | Applies the 'FrontstabBasicAttackCritChance' effect. |
| `FrontstabCritChance` | Number | Applies the 'FrontstabCritChance' effect. |
| `FullBlockEverything` | Number | Applies or references the 'FullBlockEverything' effect/state. |
| `FullBlockEverythingTo0Damage` | Number | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. |
| `FullHeal` | Number | Applies the 'FullHeal' effect. |
| `FullHealthAllStatsUp` | Number | Applies the 'FullHealthAllStatsUp' effect. |
| `FullHealthCritChance` | Number | Applies the 'FullHealthCritChance' effect. |
| `FullHealthManaRegen` | Number | Applies the 'FullHealthManaRegen' effect. |
| `FullPower` | Number | Applies the 'FullPower' effect. |
| `FurnitureStats` | Block | Applies the 'FurnitureStats' effect. |
| `GainExtraShield` | Number | Applies the 'GainExtraShield' effect. |
| `GainManaWhenAnythingDies` | Number |  |
| `GasCanBehavior` | Number | Applies or references the 'GasCanBehavior' effect/state. |
| `GasCloudBehavior2` | Number | Applies or references the 'GasCloudBehavior2' effect/state. |
| `GeminiTwin` | Number | Applies or references the 'GeminiTwin' effect/state. |
| `GlobalFamiliarDamageBoost` | Number |  |
| `GlobalFamiliarMoveBoost` | Number |  |
| `GlobalFlowerTrapperAura` | Block |  |
| `GlobalManaBurnAura` | Number |  |
| `GlobalManaDrainAura` | Number | Applies or references the 'GlobalManaDrainAura' effect/state. |
| `GlobalMeleeRevengeDamage` | Block | Applies or references the 'GlobalMeleeRevengeDamage' effect/state. |
| `GoopImmunity` | Number | Applies or references the 'GoopImmunity' effect/state. |
| `GoopWalk` | Number | Applies or references the 'GoopWalk' effect/state. |
| `GrassTileHealing` | Number | Applies the 'GrassTileHealing' effect. |
| `GravityWell` | Block | Applies the 'GravityWell' effect. |
| `GroundFlopper` | Enum | Applies or references the 'GroundFlopper' effect/state. |
| `GuillotinaDeathHead` | Number | Applies or references the 'GuillotinaDeathHead' effect/state. |
| `HPAltStates` | Block | Visual: Alternative sprite states based on current health. |
| `HPGainBlock` | Number | Applies or references the 'HPGainBlock' effect/state. |
| `HarpoonTrapPassive` | Enum | Applies or references the 'HarpoonTrapPassive' effect/state. |
| `HeadArmorPassiveMultiplierBonus` | Number | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. |
| `HealAtStart` | Number | Applies the 'HealAtStart' effect. |
| `HealDamagesEnemies` | Number | Applies the 'HealDamagesEnemies' effect. |
| `HealNeighborsEachTurn` | Block | Passive: Restores health to adjacent allies at the start of the turn. |
| `HealingAura` | Number | Applies the 'HealingAura' effect. |
| `HealsAlsoRegenMana` | Number | Applies the 'HealsAlsoRegenMana' effect. |
| `HealsCanRevive` | Number | Applies the 'HealsCanRevive' effect. |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. |
| `HealthMultiplier` | Enum |  |
| `HealthPickup` | Block | Pickup Logic: Defines what happens when a health item is collected. |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. |
| `HiddenDoomed` | Number | Applies or references the 'HiddenDoomed' effect/state. |
| `HideEquipment` | Enum | Applies or references the 'HideEquipment' effect/state. |
| `HideSomeHudStuff` | Number | Applies or references the 'HideSomeHudStuff' effect/state. |
| `HitlerExecute` | Block | Boss Logic: Specific execution or ultimate attack state. |
| `HolyDamageMultiplierBonus` | Number | Applies the 'HolyDamageMultiplierBonus' effect. |
| `HolyShieldTransferToSpawner` | Number | Applies the 'HolyShieldTransferToSpawner' effect. |
| `HolyShieldTransferToTaggedMinions` | Enum | Applies the 'HolyShieldTransferToTaggedMinions' effect. |
| `HouseFoodRequirementMultiplier` | Number |  |
| `Hypomania` | Number | Applies the 'Hypomania' effect. |
| `IceBlockBehavior` | Number | Applies or references the 'IceBlockBehavior' effect/state. |
| `IgnoreTiles` | Number |  |
| `IllusionTint` | Number | Applies or references the 'IllusionTint' effect/state. |
| `ImmediateAbilityReaction` | Enum | Reaction: Executes an ability instantly, interrupting the current sequence. |
| `Immobile` | Number |  |
| `ImmobilePassive` | Number | Applies or references the 'ImmobilePassive' effect/state. |
| `ImmortalLeeches` | Number | Applies the 'ImmortalLeeches' effect. |
| `IncreaseExplosionDamage` | Number | Applies the 'IncreaseExplosionDamage' effect. |
| `IncreaseExplosionSize` | Number | Applies or references the 'IncreaseExplosionSize' effect/state. |
| `IncreaseHealingSpellRange` | Number | Applies the 'IncreaseHealingSpellRange' effect. |
| `IncreaseItemUsesOnEquip` | Number | Applies the 'IncreaseItemUsesOnEquip' effect. |
| `IncreaseSpellRange` | Number | Applies or references the 'IncreaseSpellRange' effect/state. |
| `InfiniteRebirth` | Block | Applies the 'InfiniteRebirth' effect. |
| `InheritSpawnerStats` | Number | Applies or references the 'InheritSpawnerStats' effect/state. |
| `InjuryImmunity` | Number | Applies or references the 'InjuryImmunity' effect/state. |
| `InnateElement` | Enum | Applies the 'InnateElement' effect. |
| `InsertIntoBackgroundPlaceholder` | Number | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeDisabler` | Number | Applies or references the 'InterchangeDisabler' effect/state. |
| `InvertBrainFaction` | Number | Applies the 'InvertBrainFaction' effect. |
| `ItemAuxTransform` | Block | Applies or references the 'ItemAuxTransform' effect/state. |
| `JesterLevelUpRerolls` | Number | Applies or references the 'JesterLevelUpRerolls' effect/state. |
| `JohnnyNeedsWashing` | Block | Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state. |
| `JohnnyWasher` | Enum | Applies or references the 'JohnnyWasher' effect/state. |
| `KaijuKnockbackImmune` | Number | Applies or references the 'KaijuKnockbackImmune' effect/state. |
| `KaijuWinCon` | Enum | Applies or references the 'KaijuWinCon' effect/state. |
| `KillsHeal` | Number | Applies the 'KillsHeal' effect. |
| `KillsToMeat` | Enum | Applies or references the 'KillsToMeat' effect/state. |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. |
| `KnockbackImmunity` | Number | Applies the 'KnockbackImmunity' effect. |
| `LateBloomer` | Block | Applies the 'LateBloomer' effect. |
| `LeaveBehindOnceEachMove` | Enum | Applies or references the 'LeaveBehindOnceEachMove' effect/state. |
| `LegacySpawnSavedCatIfExists` | Enum | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. |
| `LevelUpClassOverride` | Enum | Applies the 'LevelUpClassOverride' effect. |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. |
| `LightningAspectCharge` | Number | Applies the 'LightningAspectCharge' effect. |
| `LightningRod` | Block | Applies the 'LightningRod' effect. |
| `LimitDamage` | Number | Applies or references the 'LimitDamage' effect/state. |
| `LimitHeal` | Number | Applies or references the 'LimitHeal' effect/state. |
| `LimitSelfKnockbackDamage` | Number | Applies the 'LimitSelfKnockbackDamage' effect. |
| `LimitedTileTrail` | Enum | Applies the 'LimitedTileTrail' effect. |
| `LineOfSightTrueSightAura` | Number | Applies the 'LineOfSightTrueSightAura' effect. |
| `LobbedHook` | Number | Applies the 'LobbedHook' effect. |
| `LockOrientationFaceTile` | Array | Applies or references the 'LockOrientationFaceTile' effect/state. |
| `LoopingSoundWhileAlive` | Enum | Applies or references the 'LoopingSoundWhileAlive' effect/state. |
| `LowHealthAllyDodgeChanceAura` | Block | Applies the 'LowHealthAllyDodgeChanceAura' effect. |
| `LuckUp` | Number |  |
| `Madness` | Number | Applies the Madness debuff/status effect. |
| `MagicDamageImmune` | Number | Applies or references the 'MagicDamageImmune' effect/state. |
| `MakeBasicAttackPassThroughThings` | Number | Applies the 'MakeBasicAttackPassThroughThings' effect. |
| `MakeBasicAttackPull` | Number |  |
| `MakeSpellsRequireCharge` | Number | Applies the 'MakeSpellsRequireCharge' effect. |
| `MamaCatAnimations` | Number | Applies or references the 'MamaCatAnimations' effect/state. |
| `ManaCostReduction` | Number | Applies or references the 'ManaCostReduction' effect/state. |
| `ManaCostReductionTagged` | Block | Applies the 'ManaCostReductionTagged' effect. |
| `ManaPickup` | Block | Pickup Logic: Defines what happens when a mana item is collected. |
| `ManaRegenMultiplierIfManaEmpty` | Number | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. |
| `ManglerMonsterPassive` | Enum | Applies or references the 'ManglerMonsterPassive' effect/state. |
| `MaxAccuracy` | Number | Applies the 'MaxAccuracy' effect. |
| `MaxStartingMana` | Number | Applies the 'MaxStartingMana' effect. |
| `MegaDinoDropController` | Block | Boss Logic: Manages loot drops for the Mega Dino. |
| `MegaMinions` | Number | Applies the 'MegaMinions' effect. |
| `MeleeRevengeDamage` | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. |
| `Metal` | Number | Applies or references the 'Metal' effect/state. |
| `MetalDetector` | Number | Applies the 'MetalDetector' effect. |
| `MimicSpawnerAttacks` | Number | Applies or references the 'MimicSpawnerAttacks' effect/state. |
| `MiniVolcanoReaction` | Enum | Applies or references the 'MiniVolcanoReaction' effect/state. |
| `MinimumKnockbackFromAllDamage` | Number | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. |
| `MinimumKnockbackFromPhysicalAttacks` | Number | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. |
| `MinimumTech` | Number | Applies the 'MinimumTech' effect. |
| `MissChance` | Number | Applies the 'MissChance' effect. |
| `ModelingClayPassive` | Number | Applies or references the 'ModelingClayPassive' effect/state. |
| `ModifyAbility` | Block | Applies or references the 'ModifyAbility' effect/state. |
| `ModularPickup` | Block | Pickup Logic: Defines what happens when a modular item is collected. |
| `MonkCatReactionAbilities` | Block | Reaction: Specific counter-attack or dodge abilities used by the Monk class. |
| `MoonHeadCrackedVisual` | Enum | Applies or references the 'MoonHeadCrackedVisual' effect/state. |
| `MoonHeadFinisherEnabler` | Number | Applies or references the 'MoonHeadFinisherEnabler' effect/state. |
| `MotherGrowController` | Block | Boss Logic: Manages the growth phases of the Mother boss. |
| `MotherTumorPassive` | Block | Boss Logic: Passive effects applied to the Mother's tumors. |
| `MotherTumorSpawnInCapture` | Block | Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning. |
| `Mount` | Block | Character Form: Behavior and stats for the 'Mount' state. |
| `MoveAfterAnyAttemptedAttack` | Block | AI Movement: Forces a move action immediately after attacking, even if it missed. |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | Enum | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. |
| `MoveAwayFromDamageSource` | Enum |  |
| `MoveAwayWhenEnemyAdjacent` | Block | AI Movement: Moves away if an enemy enters an adjacent tile. |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. |
| `MoveRandomly` | Number | Applies the 'MoveRandomly' effect. |
| `MoveSpeedMultiplier` | Enum | Applies or references the 'MoveSpeedMultiplier' effect/state. |
| `MoveTowardsDamageSource` | Block | AI Movement: Closes distance on the last source of damage. |
| `MoveTowardsKillers` | Enum | AI Movement: Seeks out entities that have recently killed an ally. |
| `MoveWhenDamaged` | Enum | AI Movement: Forces a reposition when taking damage. |
| `MovementReaction` | Block | Reaction: Triggers an effect or ability when forced to move. |
| `MultiSpawnOnDeath` | Block | Event Trigger: Spawns multiple entities upon death. |
| `MulticatHeads` | Number | Applies or references the 'MulticatHeads' effect/state. |
| `MulticlassLevelUp` | Enum | Applies the 'MulticlassLevelUp' effect. |
| `MultiplyCoinsOnBattleStart` | Number | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. |
| `MultiplyReceivedHealing` | Number | Applies or references the 'MultiplyReceivedHealing' effect/state. |
| `MutateAfterXTurns` | Number | Applies or references the 'MutateAfterXTurns' effect/state. |
| `MutateViaAbility` | Enum | Applies or references the 'MutateViaAbility' effect/state. |
| `MuteDemonicGlyphDisplay` | Number | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. |
| `NeckArmorPassiveMultiplierBonus` | Number | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. |
| `NoHealthOnlyShield` | Number | Applies or references the 'NoHealthOnlyShield' effect/state. |
| `NoManaRegen` | Number | Applies the 'NoManaRegen' effect. |
| `NoReflection` | Number | Applies the 'NoReflection' effect. |
| `NonStackingDivineShield` | Number |  |
| `NonStackingShield` | Number |  |
| `NubbyTossPriority` | Number | Applies the 'NubbyTossPriority' effect. |
| `NukeQuestFinalBossModifications` | Block | Special encounter trigger for the Nuke Quest ending. |
| `NumbingLeeches` | Number | Applies the 'NumbingLeeches' effect. |
| `ObjectDetector` | Block | Applies or references the 'ObjectDetector' effect/state. |
| `OrthogonalAIDangerZone` | Number | Applies or references the 'OrthogonalAIDangerZone' effect/state. |
| `OverManaReducesManaCosts` | Number |  |
| `OverhealGainsBothShield` | Number | Applies the 'OverhealGainsBothShield' effect. |
| `OverrideBasicAttack` | Enum | Applies or references the 'OverrideBasicAttack' effect/state. |
| `OverrideMaxHealth` | Number | Applies or references the 'OverrideMaxHealth' effect/state. |
| `OverrideMaxMana` | Number | Applies the 'OverrideMaxMana' effect. |
| `OverridePalette` | Number | Applies the 'OverridePalette' effect. |
| `PackHunting` | Number | Applies or references the 'PackHunting' effect/state. |
| `Paranoia` | Enum | Applies the 'Paranoia' effect. |
| `ParasitesArentCursed` | Number | Applies the 'ParasitesArentCursed' effect. |
| `PassiveAfterXKills` | Block | Applies or references the 'PassiveAfterXKills' effect/state. |
| `PassiveAtFullHealth` | Block | Applies the 'PassiveAtFullHealth' effect. |
| `PassiveAtHealthThreshold` | Block | Applies or references the 'PassiveAtHealthThreshold' effect/state. |
| `PassiveAtInjuryThreshold` | Block | Applies the 'PassiveAtInjuryThreshold' effect. |
| `PassiveAtStatThreshold` | Block | Applies the 'PassiveAtStatThreshold' effect. |
| `PassiveGroup` | Block | Passive: A collection of passives grouped together for easier management. |
| `PassiveIfAllArmorEmpty` | Block | Applies the 'PassiveIfAllArmorEmpty' effect. |
| `PassiveIfEmptyFace` | Block | Applies the 'PassiveIfEmptyFace' effect. |
| `PassiveIfEmptyHead` | Block | Applies the 'PassiveIfEmptyHead' effect. |
| `PassiveIfEmptyNeck` | Block | Applies the 'PassiveIfEmptyNeck' effect. |
| `PassiveIfStrAuxEquals` | Block | Applies or references the 'PassiveIfStrAuxEquals' effect/state. |
| `PassiveIfWeaponIsUsable` | Block | Applies or references the 'PassiveIfWeaponIsUsable' effect/state. |
| `PassiveLevelScaledStatus` | Block | Applies the 'PassiveLevelScaledStatus' effect. |
| `PassiveLevelUpAtCombatEnd` | Number | Applies the 'PassiveLevelUpAtCombatEnd' effect. |
| `PassiveUntilCastSpell` | Block | Applies the 'PassiveUntilCastSpell' effect. |
| `PassiveUntilGetKill` | Block | Applies the 'PassiveUntilGetKill' effect. |
| `PassiveWhenAffectedByElement` | Block |  |
| `PassiveWhenAtFullMana` | Block | State Trigger: Grants nested passives when at full mana. |
| `PassiveWhenDead` | Block | State Trigger: Grants passives when this condition is met. |
| `PassiveWhenOnTile` | Block | State Trigger: Grants passives when this condition is met. |
| `PassiveWhenTheAlpha` | Block | State Trigger: Grants nested passives when the alpha. |
| `PassiveWhileHasDurability` | Block | Applies or references the 'PassiveWhileHasDurability' effect/state. |
| `PassiveWhileHasStatus` | Block | Passive: Activates only while the character has the specified status. |
| `PassiveWhileInMonkMeleeStance` | Block | Applies the 'PassiveWhileInMonkMeleeStance' effect. |
| `PassiveWhileInMonkRangedStance` | Block | Applies the 'PassiveWhileInMonkRangedStance' effect. |
| `PassiveWhileNotHasStatus` | Block | Passive: Activates only while the character does NOT have the specified status. |
| `PassiveWhileNotTakingTurn` | Block | Grants nested passives that are only active while it is NOT the character's turn. |
| `PassiveWhilePreviewingMonkRangedStance` | Block | Applies the 'PassiveWhilePreviewingMonkRangedStance' effect. |
| `PassiveWhileShielded` | Block | Applies or references the 'PassiveWhileShielded' effect/state. |
| `PassiveWhileWearingMetal` | Block | Applies the 'PassiveWhileWearingMetal' effect. |
| `PermanentImmobile` | Number | Applies the 'PermanentImmobile' effect. |
| `PermanentItems` | Number | Applies the 'PermanentItems' effect. |
| `PermanentKitten` | Number | Applies the 'PermanentKitten' effect. |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. |
| `Phasing` | Number | Applies or references the 'Phasing' effect/state. |
| `PhysicalAttacksMiss` | Number | Applies or references the 'PhysicalAttacksMiss' effect/state. |
| `Plant` | Number | Applies or references the 'Plant' effect/state. |
| `Poison` | Number | Applies or references the 'Poison' effect/state. |
| `PoisonMultiplier` | Number | Applies the 'PoisonMultiplier' effect. |
| `PoisonThorns` | Number | Applies or references the 'PoisonThorns' effect/state. |
| `PoopWhenHit` | Enum |  |
| `PreventSpecificInjury` | Equation | Applies or references the 'PreventSpecificInjury' effect/state. |
| `PrioritizeAggroTarget` | Number | Applies or references the 'PrioritizeAggroTarget' effect/state. |
| `PrioritizeFarAwayTargets` | Number | Applies or references the 'PrioritizeFarAwayTargets' effect/state. |
| `PrioritizeHitDifferentTargets` | Number | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. |
| `PrioritizePlayerCats` | Number | Applies or references the 'PrioritizePlayerCats' effect/state. |
| `PrioritizeWeakestEnemy` | Number | Applies or references the 'PrioritizeWeakestEnemy' effect/state. |
| `ProtectTargetedAllies` | Block | AI Logic: Navigates to intercept attacks directed at allies. |
| `Quiver` | Number | Applies the 'Quiver' effect. |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. |
| `RandomPassivePool` | Block | Logic: Grants a random passive from the specified pool upon spawning. |
| `RandomSeededStatModifier` | Array | Applies or references the 'RandomSeededStatModifier' effect/state. |
| `RandomStatUp` | Number |  |
| `RandomizeAIWeightsEachTurn` | Array | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. |
| `RangedTrueShot` | Number | Applies or references the 'RangedTrueShot' effect/state. |
| `RealTimePressure_OneUnit` | Number | Applies the 'RealTimePressure_OneUnit' effect. |
| `ReceivedStatusReplacement` | Array | Applies the 'ReceivedStatusReplacement' effect. |
| `ReclaimItemOnBreak` | Number | Applies or references the 'ReclaimItemOnBreak' effect/state. |
| `ReduceManaCost` | Number | Applies or references the 'ReduceManaCost' effect/state. |
| `ReduceSpellCostsPerDisorder` | Number | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. |
| `ReduceSpellCostsPerParasite` | Number | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. |
| `ReflectProjectiles` | Number | Passive: Reflects incoming projectiles back at the attacker. |
| `RefreshEquipmentAbilityOnElement` | Block | Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state. |
| `RefreshMoveOnWeaponConnect` | Number | Applies the 'RefreshMoveOnWeaponConnect' effect. |
| `ReloadOnAllyCatDies` | Number | Applies or references the 'ReloadOnAllyCatDies' effect/state. |
| `ReloadOnAllyDies` | Number | Applies or references the 'ReloadOnAllyDies' effect/state. |
| `ReloadOnAnyDamage` | Number | Applies or references the 'ReloadOnAnyDamage' effect/state. |
| `ReloadOnBackstab` | Number | Applies or references the 'ReloadOnBackstab' effect/state. |
| `ReloadOnElementalDamageReceived` | Enum | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. |
| `ReloadOnGainCoins` | Number | Applies or references the 'ReloadOnGainCoins' effect/state. |
| `ReloadOnGainDivineShield` | Number | Applies or references the 'ReloadOnGainDivineShield' effect/state. |
| `ReloadOnKill` | Number | Applies or references the 'ReloadOnKill' effect/state. |
| `ReloadOnKillEnemy` | Number | Applies or references the 'ReloadOnKillEnemy' effect/state. |
| `ReloadOnKillTagged` | Enum | Applies or references the 'ReloadOnKillTagged' effect/state. |
| `ReloadOnSpendMana` | Number | Applies or references the 'ReloadOnSpendMana' effect/state. |
| `ReloadOnTotalDamageReceived` | Number | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. |
| `ReloadOnUseAbilityWithManaCost` | Number | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. |
| `RemoveExtraDispersedTurn` | Number |  |
| `RemoveLineOfSightRestrictions` | Number | Applies the 'RemoveLineOfSightRestrictions' effect. |
| `RemoveOncePerFightRestriction` | Number | Applies the 'RemoveOncePerFightRestriction' effect. |
| `ReplaceBasicAttack` | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `ReplaceBasicAttackWhenCastable` | Enum | Applies the 'ReplaceBasicAttackWhenCastable' effect. |
| `ReplaceBasicAttackWhenDead` | Enum | Applies the 'ReplaceBasicAttackWhenDead' effect. |
| `ReplaceBasicAttack_Mutation` | Enum |  |
| `ReplaceBasicMove` | Enum | Applies or references the 'ReplaceBasicMove' effect/state. |
| `ReplaceBasicMove_Mutation` | Enum |  |
| `ReplaceBlankTilesOnBattleStart` | Enum | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. |
| `ReplaceBrain` | Block | Applies the 'ReplaceBrain' effect. |
| `ReplaceSpawnedObjects` | Array | Applies the 'ReplaceSpawnedObjects' effect. |
| `ReplaceSpellsWhenDead` | Enum | Applies the 'ReplaceSpellsWhenDead' effect. |
| `RerollItemsOnBattleEnd` | Number | Applies or references the 'RerollItemsOnBattleEnd' effect/state. |
| `ReturnBoundItemOnBattleEnd` | Number | Applies or references the 'ReturnBoundItemOnBattleEnd' effect/state. |
| `RevengeDamage` | Block |  |
| `ReviveNextRound` | Block | Queues the character to be resurrected at the start of the next combat round. |
| `ReviveOnWin` | Number | Applies the 'ReviveOnWin' effect. |
| `Robot` | Number | Character Form: Behavior and stats for the 'Robot' state. |
| `RobotsInheritArmor` | Number | Applies the 'RobotsInheritArmor' effect. |
| `RockDetector` | Number | Applies the 'RockDetector' effect. |
| `RockyArmorPassive` | Number | Applies or references the 'RockyArmorPassive' effect/state. |
| `RockyArmorSalvage` | Enum |  |
| `RunInXTurns` | Number | Applies or references the 'RunInXTurns' effect/state. |
| `RunWhenKittensDead` | Number | Applies or references the 'RunWhenKittensDead' effect/state. |
| `RunWhenLastPlayerCatIsCharmed` | Block | AI Logic: Flee logic when the player team is entirely crowd-controlled. |
| `SafeDoomed` | Number | Applies or references the 'SafeDoomed' effect/state. |
| `SafeExplosions` | Number | Applies the 'SafeExplosions' effect. |
| `ScaldingOrbMoonBossOneShot` | Block | Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. |
| `ScaledStatusAlliesOnSpendMana` | Block | Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. |
| `ScaledStatusOnBleedDamage` | Block | Applies the 'ScaledStatusOnBleedDamage' effect. |
| `ScaledStatusOnHolyShieldBlock` | Block | Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. |
| `ScaledStatusOnLoseShield` | Block | Applies the 'ScaledStatusOnLoseShield' effect. |
| `ScaledStatusOnOverHealed` | Block | Applies the 'ScaledStatusOnOverHealed' effect. |
| `ScaledStatusOnOverMana` | Block | Applies the 'ScaledStatusOnOverMana' effect. |
| `ScaledStatusOnSpendMana` | Block | Applies the 'ScaledStatusOnSpendMana' effect. |
| `ScalingAttackAnimation` | Block | Visual: Animation scales based on damage output. |
| `SchizoIllusionAIModifier` | Number | Applies or references the 'SchizoIllusionAIModifier' effect/state. |
| `SchrodingerDisorder` | Number | Applies the 'SchrodingerDisorder' effect. |
| `Scleroderma` | Number | Applies the 'Scleroderma' effect. |
| `SecurityBotProtect` | Block | AI Logic: Guarding behavior for Security Bot units. |
| `SelfDamageWhenDealDamage` | Block | Applies the 'SelfDamageWhenDealDamage' effect. |
| `SelfStatusCarefulness` | Number | Applies or references the 'SelfStatusCarefulness' effect/state. |
| `SetBrittleImmune` | Enum | Applies or references the 'SetBrittleImmune' effect/state. |
| `SetDefaultFace` | Enum | Applies the 'SetDefaultFace' effect. |
| `SetDefaultFacePassive` | Enum | Applies or references the 'SetDefaultFacePassive' effect/state. |
| `SetFaction` | Enum | Applies or references the 'SetFaction' effect/state. |
| `SetFragileImmune` | Enum | Applies or references the 'SetFragileImmune' effect/state. |
| `SetSpellCosts` | Number | Applies the 'SetSpellCosts' effect. |
| `ShareHealthRegen` | Number | Applies the 'ShareHealthRegen' effect. |
| `SharePickups` | Number | Applies the 'SharePickups' effect. |
| `SharePickupsWithSpawner` | Number | Applies or references the 'SharePickupsWithSpawner' effect/state. |
| `SharkySmellsBlood` | Number | Applies or references the 'SharkySmellsBlood' effect/state. |
| `Shield` | Number | Applies or references the 'Shield' effect/state. |
| `ShoulderCheck` | Number | Applies the 'ShoulderCheck' effect. |
| `ShovingMatch` | Enum | Applies the 'ShovingMatch' effect. |
| `ShowHiddenThings` | Number |  |
| `SizeScale` | Enum |  |
| `SkipFirstRounds` | Block | AI Logic: Passes turn for the first X rounds of combat. |
| `SlotMachineRollPool` | Block | Logic: Defines the possible outcomes for slot machine enemies. |
| `Slow` | Number |  |
| `SmallEnemiesIgnoreYou` | Number | Applies the 'SmallEnemiesIgnoreYou' effect. |
| `SmallRockBehavior` | Number | AI Logic: Movement/interaction profile for small rocks. |
| `SmiteEnemiesWhoKill` | Block | Applies the 'SmiteEnemiesWhoKill' effect. |
| `SpawnCatCloneOnCorpsePopped` | Number | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. |
| `SpawnCatCopyOnBattleStart` | Block | Applies the 'SpawnCatCopyOnBattleStart' effect. |
| `SpawnCatCopyWhenDowned` | Block |  |
| `SpawnCreepOnHit` | Number | Applies or references the 'SpawnCreepOnHit' effect/state. |
| `SpawnCreepOnHitKnockback` | Number | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. |
| `SpawnEachTurn` | Block | Applies or references the 'SpawnEachTurn' effect/state. |
| `SpawnExtraThingsOnBattleStart` | Block | Applies or references the 'SpawnExtraThingsOnBattleStart' effect/state. |
| `SpawnItemLinkedFamiliar` | Block | Applies or references the 'SpawnItemLinkedFamiliar' effect/state. |
| `SpawnMeatOnMove` | Enum | Applies the 'SpawnMeatOnMove' effect. |
| `SpawnNearEnemies` | Number | Applies or references the 'SpawnNearEnemies' effect/state. |
| `SpawnObjectOnPopCorpse` | Enum | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. |
| `SpawnOnBattleStart` | Enum | Applies or references the 'SpawnOnBattleStart' effect/state. |
| `SpawnOnBattleStartRandomEmptyTile` | Block | Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. |
| `SpawnOnDeath` | Block | Event Trigger: Spawns a specific entity when killed. |
| `SpawnOnDowned` | Enum |  |
| `SpawnRandomPickupsOnTaggedUnitKilled` | Block | Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. |
| `SpawnThingOnDamage` | Block | Applies or references the 'SpawnThingOnDamage' effect/state. |
| `SpawnThingOnDeath` | Enum | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `SpawnerCatDataReference` | Number | Applies or references the 'SpawnerCatDataReference' effect/state. |
| `SpecialFriends` | Block | Applies the 'SpecialFriends' effect. |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. |
| `SpewerAltGraphics` | Block | Visual: Alternative graphics for Spewer enemies. |
| `SplittableMove` | Number | Applies the 'SplittableMove' effect. |
| `SpreadExtraDebuffs` | Number | Applies the 'SpreadExtraDebuffs' effect. |
| `SpreadPainBonus` | Number | Applies the 'SpreadPainBonus' effect. |
| `SpreadPainBonusCrit` | Number | Applies the 'SpreadPainBonusCrit' effect. |
| `SpreadWater` | Number | Applies or references the 'SpreadWater' effect/state. |
| `SproutsGrantMovement` | Number | Applies or references the 'SproutsGrantMovement' effect/state. |
| `StackingDodgeChanceOnTookDamage` | Block | Applies the 'StackingDodgeChanceOnTookDamage' effect. |
| `StackingFlowerTrail` | Block | Applies or references the 'StackingFlowerTrail' effect/state. |
| `StacyMutant_Brace` | Block | Character Form: Behavior and stats for the 'StacyMutant_Brace' state. |
| `StacyMutant_Counter` | Block | Character Form: Behavior and stats for the 'StacyMutant_Counter' state. |
| `StacyMutant_Damage` | Block | Character Form: Behavior and stats for the 'StacyMutant_Damage' state. |
| `StacyMutant_DoubleHead` | Block | Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state. |
| `StacyMutant_Fire` | Block | Character Form: Behavior and stats for the 'StacyMutant_Fire' state. |
| `StacyMutant_Health` | Block | Character Form: Behavior and stats for the 'StacyMutant_Health' state. |
| `StacyMutant_Holy` | Block | Character Form: Behavior and stats for the 'StacyMutant_Holy' state. |
| `StacyMutant_Ice` | Block | Character Form: Behavior and stats for the 'StacyMutant_Ice' state. |
| `StacyMutant_Lightning` | Block | Character Form: Behavior and stats for the 'StacyMutant_Lightning' state. |
| `StacyMutant_Mirror` | Block | Character Form: Behavior and stats for the 'StacyMutant_Mirror' state. |
| `StacyMutant_Speed` | Block | Character Form: Behavior and stats for the 'StacyMutant_Speed' state. |
| `StacyMutant_Thorns` | Block | Character Form: Behavior and stats for the 'StacyMutant_Thorns' state. |
| `StartDead` | Number | Applies or references the 'StartDead' effect/state. |
| `StartOffMap` | Number | Applies or references the 'StartOffMap' effect/state. |
| `StatDependentPassive` | Block | Applies or references the 'StatDependentPassive' effect/state. |
| `StatMinimum` | Number | Applies the 'StatMinimum' effect. |
| `StatsAtLowHealth` | Block | Applies the 'StatsAtLowHealth' effect. |
| `StatusAdjacentOnTheirTurnBegin` | Block | Event Trigger: Applies nested statuses to adjacent on their turn begin. |
| `StatusAdjacentOnTheirTurnEnd` | Block | Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state. |
| `StatusAfterCastSpell` | Block | Applies or references the 'StatusAfterCastSpell' effect/state. |
| `StatusAfterXTurns` | Block | Event Trigger: Applies a status effect after X turns have passed. |
| `StatusAllCharactersOnSpawn` | Block | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. |
| `StatusAlliesEachTurn` | Block | Applies or references the 'StatusAlliesEachTurn' effect/state. |
| `StatusAlliesOnBattleStart` | Block | Applies or references the 'StatusAlliesOnBattleStart' effect/state. |
| `StatusAlliesOnDeath` | Block | Event Trigger: Applies nested statuses to allies on death. |
| `StatusAlliesOnGainCoins` | Block | Event Trigger: Applies nested statuses to allies on gain coins. |
| `StatusAlliesOnKill` | Block | Event Trigger: Applies nested statuses to allies on kill. |
| `StatusAlliesOnSpendMana` | Block | Event Trigger: Applies nested statuses to allies on spend mana. |
| `StatusAlliesScaledByCursedOnDeath` | Block | Event Trigger: Applies nested statuses to allies scaled by cursed on death. |
| `StatusAllyWhenAllySpendsMana` | Block | Event Trigger: Applies nested statuses to ally when ally spends mana. |
| `StatusAnyCatAllyWhoKills` | Block | Event Trigger: Applies nested statuses to any cat ally who kills. |
| `StatusCarefulness` | Number | Applies or references the 'StatusCarefulness' effect/state. |
| `StatusCollector` | Block | Passive: Gains benefits based on the number of statuses applied to them. |
| `StatusDamagers` | Block | Event Trigger: Applies nested statuses to damagers. |
| `StatusEachRoundBegin` | Block |  |
| `StatusEachRoundEnd` | Block |  |
| `StatusEachTurnBegin` | Block | Event Trigger: Applies nested statuses to each turn begin. |
| `StatusEachTurnBeginIfHasStatus` | Block | Event Trigger: Applies a status at the start of the turn if a prerequisite status is met. |
| `StatusEachTurnEnd` | Block | Applies or references the 'StatusEachTurnEnd' effect/state. |
| `StatusEachTurnEndForEachTurn` | Block | Event Trigger: Applies nested statuses to each turn end for each turn. |
| `StatusEachTurnEndIfEnabledAtStartOfTurn` | Block | Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start. |
| `StatusEachTurnEndPerEnemyKill` | Block | Event Trigger: Applies nested statuses to each turn end per enemy kill. |
| `StatusEnemiesOnDeath` | Block | Event Trigger: Applies nested statuses to enemies on death. |
| `StatusEveryXSpellCasts` | Block | Applies or references the 'StatusEveryXSpellCasts' effect/state. |
| `StatusEveryXSpellCastsEachTurn` | Block |  |
| `StatusEveryXTurnBegins` | Block | Event Trigger: Applies nested statuses to every x turn begins. |
| `StatusIfBattleAlreadyBegan` | Block | Event Trigger: Applies nested statuses to if battle already began. |
| `StatusIfDidntMove` | Block |  |
| `StatusIfUnusedActPoints` | Block | Applies or references the 'StatusIfUnusedActPoints' effect/state. |
| `StatusIfUnusedMovePoints` | Block | Event Trigger: Applies nested statuses to if unused move points. |
| `StatusImmunity` | Enum | Applies or references the 'StatusImmunity' effect/state. |
| `StatusKilledCharacters` | Block | Event Trigger: Applies nested statuses to killed characters. |
| `StatusKillers` | Block | Instantly kills the target if they possess the specified status effects. |
| `StatusOnAllyCatDeath` | Block | Event Trigger: Applies nested statuses when ally cat death. |
| `StatusOnAnyDeath` | Block | Event Trigger: Applies nested statuses when any death. |
| `StatusOnBackstab` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnBattleEnd` | Block | Applies the nested status effects when the encounter finishes. |
| `StatusOnBattleEndIfKillThresholdMet` | Block | Event Trigger: Applies nested statuses when battle end if kill threshold met. |
| `StatusOnBattleStart` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnBreak` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnBreakItem` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnCastSpell` | Block | Event Trigger: Applies nested statuses when cast spell. |
| `StatusOnCollectPickup` | Block | Event Trigger: Applies nested statuses when collect pickup. |
| `StatusOnCrit` | Block | Event Trigger: Applies nested statuses when crit. |
| `StatusOnDealtDamage` | Block | Event Trigger: Applies nested statuses when dealt damage. |
| `StatusOnDealtDamageThreshold` | Block | Event Trigger: Applies nested statuses when dealt damage threshold. |
| `StatusOnDie` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnDodge` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnEatFood` | Block | Event Trigger: Applies nested statuses when eat food. |
| `StatusOnEatPill` | Block |  |
| `StatusOnEndMove` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnEnemyCastSpell` | Block |  |
| `StatusOnEnemyConfused` | Block | Event Trigger: Applies statuses when an enemy becomes confused. |
| `StatusOnEnemyDeath` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnFallAsleep` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnFullMana` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnGainCoins` | Block | Event Trigger: Applies nested statuses when gain coins. |
| `StatusOnGainShield` | Block | Event Trigger: Applies nested statuses when gain shield. |
| `StatusOnHeal` | Block | Event Trigger: Applies nested statuses when heal. |
| `StatusOnHealed` | Block | Event Trigger: Applies nested statuses when healed. |
| `StatusOnKill` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnKillEnemy` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnLoseShield` | Block | Event Trigger: Applies nested statuses when lose shield. |
| `StatusOnOverHealed` | Block | Event Trigger: Applies nested statuses when over healed. |
| `StatusOnOverMana` | Block | Event Trigger: Applies nested statuses when over mana. |
| `StatusOnPickupCoins` | Block | Event Trigger: Applies nested statuses when pickup coins. |
| `StatusOnPopCorpse` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnSetPieceBreak` | Block |  |
| `StatusOnSpawnIn` | Block | Event Trigger: Applies statuses immediately when spawned. |
| `StatusOnStanceSwitch` | Block | Event Trigger: Applies nested statuses when stance switch. |
| `StatusOnTakeHealthDamage` | Block | Event Trigger: Applies nested statuses when take health damage. |
| `StatusOnTakeHealthOrShieldDamage` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnTookDamage` | Block | Event Trigger: Applies nested statuses when took damage. |
| `StatusOnTookDamageFromAbility` | Block | Event Trigger: Applies statuses when taking damage from an ability. |
| `StatusOnTookDamageFromEnemyAbility` | Block | Event Trigger: Applies nested statuses when took damage from enemy ability. |
| `StatusOnTriggerTrap` | Block | Event Trigger: Applies nested statuses when trigger trap. |
| `StatusOnTurnEndIfCastNSpells` | Block | Event Trigger: Applies nested statuses when turn end if cast n spells. |
| `StatusOnTurnEndIfDidntCastAbilityTypes` | Block | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnTurnEndIfManaExact` | Block | Event Trigger: Applies nested statuses when turn end if mana exact. |
| `StatusOnTurnEndIfManaOrHealthExact` | Block | Event Trigger: Applies nested statuses when turn end if mana or health exact. |
| `StatusOnUseAbilityWithTag` | Block | Event Trigger: Applies nested statuses when use ability with tag. |
| `StatusOnUseBasicAttack` | Block | Event Trigger: Applies nested statuses when use basic attack. |
| `StatusOnUseElementAbility` | Block | Event Trigger: Applies nested statuses when use element ability. |
| `StatusOverlappingCharactersAndDie` | Block | Event Trigger: Applies statuses to overlapping entities, then destroys self. |
| `StatusPerInjury` | Block | Event Trigger: Applies nested statuses to per injury. |
| `StatusRandomEnemiesOnBattleStart` | Block | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. |
| `StatusReplacement` | Array | Event Trigger: Applies nested statuses to replacement. |
| `StatusThingsKnockedBack` | Block | Event Trigger: Applies nested statuses to things knocked back. |
| `StatusWhenAllySpendsMana` | Block | Event Trigger: Applies nested statuses to when ally spends mana. |
| `StatusWhenStatusCompletelyRemoved` | Block | Event Trigger: Applies statuses when a tracked status effect is fully cleansed. |
| `Stealth` | Number | Applies the 'Stealth' effect. |
| `StevenBolts` | Number | Applies or references the 'StevenBolts' effect/state. |
| `StrengthForEachNeighboringEnemy` | Number | Applies the 'StrengthForEachNeighboringEnemy' effect. |
| `StrengthInNumbersAura` | Number | Applies the 'StrengthInNumbersAura' effect. |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. |
| `StrictLimitDamage` | Number | Applies the 'StrictLimitDamage' effect. |
| `StripKnockback` | Number | Applies or references the 'StripKnockback' effect/state. |
| `StripStatuses` | Number | Applies or references the 'StripStatuses' effect/state. |
| `Study` | Number | Applies the 'Study' effect. |
| `StunImmunity` | Number | Passive: Prevents Stun from being applied. |
| `SupportDieInsteadOfRun` | Block | AI Logic: Forces a support unit to die rather than flee. |
| `SupportFormChangeInsteadOfRun` | Enum | AI Logic: Forces a support unit to transform rather than flee. |
| `SurviveAt1HP` | Number | Applies or references the 'SurviveAt1HP' effect/state. |
| `SwapHighestAndLowestStat` | Number |  |
| `SwimmingFormChange` | Block | Logic: Automates form change when entering/exiting water. |
| `SyncFormsWithBuddy` | Block | Logic: Forces this character's form to match their familiar/buddy. |
| `T3HitlerSpawningPhase` | Block | Boss Logic: Minion spawn phase for the T3 Hitler boss. |
| `TVBotDisableAttack` | Number | Applies or references the 'TVBotDisableAttack' effect/state. |
| `TVBotDisableMove` | Number | Applies or references the 'TVBotDisableMove' effect/state. |
| `TVBotDisableSpells` | Number | Applies or references the 'TVBotDisableSpells' effect/state. |
| `TVBotScreen` | Block | Visual: TV Bot screen state. |
| `TagGreed` | Enum | Applies or references the 'TagGreed' effect/state. |
| `TaggedPickupEffectReplacement` | Block | Applies the 'TaggedPickupEffectReplacement' effect. |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. |
| `TakeWeaponFromSpawner` | Number | Applies or references the 'TakeWeaponFromSpawner' effect/state. |
| `Tall` | Number | Applies or references the 'Tall' effect/state. |
| `TallTumorManaBurn` | Enum | Applies or references the 'TallTumorManaBurn' effect/state. |
| `TauntAlways` | Number | Applies the 'TauntAlways' effect. |
| `TauntAtFullHealth` | Number | Applies the 'TauntAtFullHealth' effect. |
| `Tech` | Number | Applies the 'Tech' effect. |
| `TempInitiativeChange` | Number | Applies the 'TempInitiativeChange' effect. |
| `Terminator2Chase` | Enum | Applies or references the 'Terminator2Chase' effect/state. |
| `Terminator2Run` | Block | AI Movement: Specific run logic for Terminator2. |
| `TerminatorChase` | Block | AI Movement: Specific chase logic for Terminator. |
| `TerminatorSkin` | Block | Visual: Skin definition for Terminator. |
| `TheHunger` | Block | Applies the 'TheHunger' effect. |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. |
| `TileDamageMultiplier` | Number | Applies the 'TileDamageMultiplier' effect. |
| `TileElementDamageImmunity` | Enum | Applies or references the 'TileElementDamageImmunity' effect/state. |
| `TileTrail` | Enum |  |
| `TileTrail_Ahead` | Enum | Applies or references the 'TileTrail_Ahead' effect/state. |
| `TinkererBasicAttackSwitching` | Block | Logic: Allows Tinkerer to swap basic attacks. |
| `TintItem` | Block | Applies or references the 'TintItem' effect/state. |
| `TireBehavior` | Number | Applies or references the 'TireBehavior' effect/state. |
| `TormentorHeal` | Number | Applies or references the 'TormentorHeal' effect/state. |
| `TossTargetIsAggroTarget` | Number | Applies or references the 'TossTargetIsAggroTarget' effect/state. |
| `TossTargetIsBuddy` | Number | Applies or references the 'TossTargetIsBuddy' effect/state. |
| `TossTargetIsNotInWater` | Number | Applies or references the 'TossTargetIsNotInWater' effect/state. |
| `TourettesMeows` | Block | Applies the 'TourettesMeows' effect. |
| `TowerDefense` | Block | Applies the 'TowerDefense' effect. |
| `TowerDefenseReflex` | Enum | Applies the 'TowerDefenseReflex' effect. |
| `TrackAmountKilledByPlayer` | Enum | Applies or references the 'TrackAmountKilledByPlayer' effect/state. |
| `Trample` | Number | Applies or references the 'Trample' effect/state. |
| `TransformInXTurns` | Block | Logic: Forces a form change after X turns. |
| `TransformItemOnElementInfluence` | Block | Applies or references the 'TransformItemOnElementInfluence' effect/state. |
| `TransformOnDeath` | Enum | Applies or references the 'TransformOnDeath' effect/state. |
| `TransformOnDeathImmediately` | Enum | Logic: Bypasses death sequence to instantly assume a new form. |
| `TransformOnElementInfluence` | Block | Logic: Changes form when affected by elements. |
| `TransformOnElementInfluencex` | Block | Logic: Variant element influence transformation. |
| `TransformOnStatusThreshold` | Block | Logic: Changes form when a status effect reaches a certain stack count. |
| `TransformWhenBuddyDies` | Enum | Applies or references the 'TransformWhenBuddyDies' effect/state. |
| `TrapEffectsMultiplier` | Number | Applies the 'TrapEffectsMultiplier' effect. |
| `Trapper` | Block | Character Form: Behavior and stats for the 'Trapper' state. |
| `TriggerBleedOnBleed` | Number |  |
| `TrinketActiveEffectsMultiplierBonus` | Number | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. |
| `TrinketPassiveMultiplierBonus` | Number | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. |
| `Triskaidekaphobia` | Number | Applies the 'Triskaidekaphobia' effect. |
| `TrueShot` | Number | Applies or references the 'TrueShot' effect/state. |
| `TunnelVision` | Block | Applies or references the 'TunnelVision' effect/state. |
| `TutorialBossRiggedFight` | Number | Applies or references the 'TutorialBossRiggedFight' effect/state. |
| `TwisterFling` | Block | Logic: Fling behavior for tornado attacks. |
| `UncappedHP` | Number | Applies the 'UncappedHP' effect. |
| `UncappedHPBonusStr` | Number | Applies the 'UncappedHPBonusStr' effect. |
| `UncappedMana` | Number | Applies the 'UncappedMana' effect. |
| `Uncontrollable` | Number | Applies or references the 'Uncontrollable' effect/state. |
| `Undead` | Number | Applies or references the 'Undead' effect/state. |
| `UnlimitedDeathRattleRevive` | Block | Logic: Endless resurrection on death. |
| `UnlockOrientation` | Number | Applies or references the 'UnlockOrientation' effect/state. |
| `UpTireBehavior` | Number | Applies or references the 'UpTireBehavior' effect/state. |
| `UpgradeLevelUpClassActives` | Enum | Applies the 'UpgradeLevelUpClassActives' effect. |
| `UpgradeLevelUpClassPassives` | Enum | Applies the 'UpgradeLevelUpClassPassives' effect. |
| `UpgradeSpawnedPickups` | Number | Applies the 'UpgradeSpawnedPickups' effect. |
| `UpgradeTaggedSpawnsToChampions` | Enum |  |
| `UseAbility` | Enum | Logic: Forces execution of an ability. |
| `UseAbilityWhenOutOfStatus` | Block | Logic: Casts a specific ability the moment a status effect expires. |
| `UseAbilityWhenShieldDepleted` | Enum | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. |
| `Vegan` | Number |  |
| `Vengeful` | Number | Applies the 'Vengeful' effect. |
| `Wall` | Number | Applies or references the 'Wall' effect/state. |
| `WaterWalk` | Number | Applies or references the 'WaterWalk' effect/state. |
| `Weakness` | Number | Applies the 'Weakness' effect. |
| `WeaponActiveEffectsMultiplierBonus` | Number |  |
| `WeaponCountsAsBasicAttack` | Number | Applies the 'WeaponCountsAsBasicAttack' effect. |
| `WeaponDamageMultiplierBonus` | Number | Applies the 'WeaponDamageMultiplierBonus' effect. |
| `WeaponPassiveMultiplierBonus` | Number |  |
| `WeaponsDontLoseDurability` | Number | Applies or references the 'WeaponsDontLoseDurability' effect/state. |
| `WeremanTransformationReceiver` | Enum | Applies or references the 'WeremanTransformationReceiver' effect/state. |
| `WhitelistPickupType` | Enum | Applies or references the 'WhitelistPickupType' effect/state. |
| `WideBackstab` | Number | Applies or references the 'WideBackstab' effect/state. |
| `WispDodge` | Number | Applies or references the 'WispDodge' effect/state. |
| `WobblyCat` | Number | Applies the 'WobblyCat' effect. |
| `XIsConsumedCharacterMaxHP` | Number | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. |
| `XIsCountDeaths` | Number | Applies or references the 'XIsCountDeaths' effect/state. |
| `XIsCountStatusStacks` | Enum | Applies or references the 'XIsCountStatusStacks' effect/state. |
| `XIsFormulaLockedUntilComplete` | Equation | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. |
| `XIsFreeArmorSlots` | Number | Applies or references the 'XIsFreeArmorSlots' effect/state. |
| `XIsIncreaseEachTurn` | Number | Applies or references the 'XIsIncreaseEachTurn' effect/state. |
| `XIsLivingAlliesWithTag` | Enum | Applies or references the 'XIsLivingAlliesWithTag' effect/state. |
| `XIsLivingCharactersWithTag` | Enum | Applies or references the 'XIsLivingCharactersWithTag' effect/state. |
| `XIsMultipliedPercentHealth` | Array | Applies or references the 'XIsMultipliedPercentHealth' effect/state. |
| `XIsOtherHealsThisTurn` | Number | Applies or references the 'XIsOtherHealsThisTurn' effect/state. |
| `XIsRampAndReset` | Number | Applies or references the 'XIsRampAndReset' effect/state. |
| `XIsRecycleCostReduction` | Number | Applies or references the 'XIsRecycleCostReduction' effect/state. |
| `XIsSpellStormRampAndReset` | Number | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. |
| `XIsTimesDamageTaken` | Number | Applies or references the 'XIsTimesDamageTaken' effect/state. |
| `YOffset` | Enum | Applies or references the 'YOffset' effect/state. |
| `ZeroKnockbackDamage` | Number | Applies or references the 'ZeroKnockbackDamage' effect/state. |

</details>

### Known Explicit Parameters

These are hardcoded configuration keys found within these blocks (not dynamic IDs).

<details>
<summary><b>Expand</b></summary>

| Parameter | Type | Notes |
| :--- | :--- | :--- |
| `element` | Enum |  |
| `mode` | Enum |  |
| `passives` | Block |  |
| `stacks` | Number | Number of stacks or intensity to apply. |
| `status` | Enum | ID of the status effect to apply or check. |
| `tag_filter` | Enum |  |
| `threshold` | Block |  |

</details>

