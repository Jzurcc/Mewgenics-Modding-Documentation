# Passive Identifiers Audit Report

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

> Analysis of `Passive Identifiers.txt` against the generated Schema.

**Total Identifiers Checked:** 1867
**Found natively in `passive_pool` enum:** 53

## 1. Exists as Property Key but NOT in `passive_pool` (1586)

These identifiers are missing from the `passive_pool` enum, but they DO exist as property keys or contexts in the listed schema sections. This might indicate they are hardcoded structures rather than enum values.

| :--- | :--- |
| Identifier | Found In Sections |
| `AIControlNextTurn` | Items & Equipment, Miscellaneous |
| `AIFavorLowHealth` | Abilities & Spells, Miscellaneous |
| `AOEBonus` | Items & Equipment, Miscellaneous |
| `AOEPuddle` | Miscellaneous, Passives & Statuses |
| `AbilityAfterEnemyCastSpell_Stackable` | Characters & Bosses, Miscellaneous |
| `AbilityChargeRefundChance` | Miscellaneous, Passives & Statuses |
| `AbilityDamageMultiplier` | Miscellaneous |
| `AbilityDisableIfLivingCrow` | Abilities & Spells, Miscellaneous |
| `AbilityEnableIfConsumedCharacterHasTag` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledAtHealthThreshold` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledIfHasStatus` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledIfMovementTrapped` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledIfNoAggroTarget` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledIfNotHasStatus` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledIfSpecificItemEquipped` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledOncePerRound` | Abilities & Spells, Miscellaneous |
| `AbilityEnabledPercentEachTurn` | Abilities & Spells, Miscellaneous |
| `AbilityHealthThreshold` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `AbilityInheritsWeaponEffects` | Abilities & Spells, Miscellaneous |
| `AbilityOnBattleStart` | Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AbilityOnBattleStart_Immediate` | Events & Encounters, Miscellaneous |
| `AbilityOnBattleStart_UseAI` | Characters & Bosses, Miscellaneous |
| `AbilityOnRoundEnd` | Characters & Bosses, Miscellaneous |
| `AbilityOnRoundEndOnce` | Items & Equipment, Miscellaneous |
| `AbilityReaction` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AbilityWhenBuddyDies` | Characters & Bosses, Miscellaneous |
| `AbilityWhenTaggedCharacterMovesNear` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `AbsorbManaAura` | Miscellaneous, Passives & Statuses |
| `AbsorbManaFromOtherSpells` | Abilities & Spells, Miscellaneous |
| `AcidRain` | Miscellaneous |
| `AddAdvantageToEvent` | Items & Equipment, Miscellaneous |
| `AddAllyNeighborsToAbilityRange` | Miscellaneous, Passives & Statuses |
| `AddAllyNeighborsToAttackRange` | Miscellaneous, Passives & Statuses |
| `AddBonusMeleeRange` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddBonusRange` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddChaScalingSpellDamage` | Miscellaneous, Passives & Statuses |
| `AddConstitution` | Miscellaneous |
| `AddCorpseHealth` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddCritMultiplier` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddDamage` | Characters & Bosses, Miscellaneous |
| `AddDamageToBasicAttack` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddDamageToElementDamage` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddElement` | Miscellaneous, Passives & Statuses |
| `AddElementsToBasicAttack` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddElementsToSpells` | Abilities & Spells, Miscellaneous |
| `AddEndOfCombatRegen` | Items & Equipment, Miscellaneous |
| `AddExtraTurnsBeforeRun` | Miscellaneous |
| `AddFilledMaxHealth` | Miscellaneous, Passives & Statuses |
| `AddHiddenTag` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddInitiative` | Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddKnockbackDamage` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddKnockbackToEverything` | Miscellaneous, Passives & Statuses |
| `AddLeechesStatus` | Abilities & Spells, Miscellaneous |
| `AddLevelUpRerolls` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddLevelUpStatMultiplier` | Miscellaneous, Passives & Statuses |
| `AddLootMultiplier` | Cat Mutations, Miscellaneous |
| `AddManaRegen` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddMaxHealth` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddMeleeKnockback` | Characters & Bosses, Miscellaneous |
| `AddMovement` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `AddPassiveToSpawnedRocks` | Miscellaneous, Passives & Statuses |
| `AddPassivesToCharmed` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddPassivesToMinions` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddPassivesToSummonAbilityMinions` | Miscellaneous, Passives & Statuses |
| `AddPostProcessEffect` | Miscellaneous |
| `AddRandomEliteBuff` | Miscellaneous |
| `AddRangedCritChance` | Miscellaneous, Passives & Statuses |
| `AddSelfStatusToBasicAttack` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddSelfStatusToWeapons` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddSpeed` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `AddSpellDamage` | Miscellaneous, Passives & Statuses |
| `AddSpiritBombCharges` | Abilities & Spells, Miscellaneous |
| `AddStartingMana` | Cat Classes, Events & Encounters, Miscellaneous, Passives & Statuses |
| `AddStatusToAllDamage` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddStatusToAllDamageAbilities` | Miscellaneous, Passives & Statuses |
| `AddStatusToBackstabs` | Items & Equipment, Miscellaneous |
| `AddStatusToBasicAttack` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddStatusToBasicAttackWithCooldown` | Miscellaneous, Passives & Statuses |
| `AddStatusToBasicMeleeAttack` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `AddStatusToElementAbilities` | Miscellaneous, Passives & Statuses |
| `AddStatusToElementDamage` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddStatusToExplosions` | Miscellaneous, Passives & Statuses |
| `AddStatusToFirstBasicAttack` | Miscellaneous, Passives & Statuses |
| `AddStatusToFirstSpellEachTurn` | Miscellaneous |
| `AddStatusToKnockbackDamage` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddStatusToMeleeDamage` | Miscellaneous, Passives & Statuses |
| `AddStatusToReceivedDamage` | Characters & Bosses, Miscellaneous |
| `AddStatusToReceivedDamage_ExcludeStatuses` | Miscellaneous, Passives & Statuses |
| `AddStatusToSpells` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddStatusToTrampleDamage` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `AddStatusToWeapons` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddStatusesIfPersistentWeatherElement` | Miscellaneous, Passives & Statuses |
| `AddStatusesToReceivedElementalDamage` | Miscellaneous, Passives & Statuses |
| `AddTag` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddTemporaryEffectsToBasicAttack` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AddTemporaryEffectsToEquipment` | Miscellaneous, Passives & Statuses |
| `AddTilesetObjects` | Miscellaneous |
| `AddUnfilledMaxHealth` | Miscellaneous, Passives & Statuses |
| `AddWeaponAux` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `AddWeaponScaling` | Miscellaneous, Passives & Statuses |
| `Adrenaline` | Abilities & Spells, Miscellaneous |
| `AdvancedTint` | Characters & Bosses, Miscellaneous |
| `AdventureTokenPassivePool` | Characters & Bosses, Miscellaneous |
| `AggroTargetIsBuddy` | Characters & Bosses, Miscellaneous |
| `AggroTargetIsCurrentTurn` | Characters & Bosses, Miscellaneous |
| `AggroTargetIsGovernedByHitEffect` | Characters & Bosses, Miscellaneous |
| `AggroTargetIsLastEnemyThatDealtDamage` | Characters & Bosses, Miscellaneous |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Characters & Bosses, Miscellaneous |
| `AggroTargetIsLowestMaxHealthCat` | Characters & Bosses, Miscellaneous |
| `AlienBeastDangerZones` | Characters & Bosses, Miscellaneous |
| `AlienBeastEyeStalks` | Characters & Bosses, Miscellaneous |
| `AllDamageCrits` | Miscellaneous, Passives & Statuses |
| `AllDamageImmune_IncludingSpeculative` | Characters & Bosses, Miscellaneous |
| `AllSpellsCostActPoints` | Characters & Bosses, Miscellaneous |
| `AllSpellsCostCharge` | Items & Equipment, Miscellaneous |
| `AllStatsAura` | Characters & Bosses, Miscellaneous |
| `AllStatsUp` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AllStatsUpPerDisorder` | Items & Equipment, Miscellaneous |
| `AllUnitsExplodeOnDeath` | Items & Equipment, Miscellaneous |
| `AlliesAvoidTraps` | Miscellaneous, Passives & Statuses |
| `AlliesScrambleSpellAfterCast` | Items & Equipment, Miscellaneous |
| `AlliesTakeExtraTurn` | Abilities & Spells, Miscellaneous |
| `AllowPassTurn` | Miscellaneous, Passives & Statuses |
| `AlluringDoodieEater` | Items & Equipment, Miscellaneous |
| `AllyBonusAbilityAura` | Miscellaneous, Passives & Statuses |
| `AllyChainKnockback` | Miscellaneous, Passives & Statuses |
| `AllyDamageReaction` | Miscellaneous, Passives & Statuses |
| `AllyDamageReduction` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AllyDodgeChanceAura` | Items & Equipment, Miscellaneous |
| `AllyHealthRegenAura` | Miscellaneous, Passives & Statuses |
| `AllyInfested` | Miscellaneous |
| `AllyManaRegenAura` | Miscellaneous, Passives & Statuses |
| `AllyMoveAbilityAura` | Miscellaneous, Passives & Statuses |
| `AllyMultiplyKnockbackDamage` | Miscellaneous, Passives & Statuses |
| `AllyMultiplyKnockbackDistance` | Miscellaneous, Passives & Statuses |
| `AllyUncappedHPAura` | Miscellaneous, Passives & Statuses |
| `AlphaAllStatsUp` | Items & Equipment, Miscellaneous |
| `AlphaCat` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AlphaDodgeChance` | Abilities & Spells, Miscellaneous |
| `AlphaStatusOnTurnBegin` | Abilities & Spells, Miscellaneous |
| `AlphaTurns` | Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AlternateCraftingPools` | Miscellaneous, Passives & Statuses |
| `AlternateIdleAnimation` | Abilities & Spells, Miscellaneous |
| `AlwaysChosenForLevelUp` | Items & Equipment, Miscellaneous |
| `AlwaysHitDifferentTargets` | Characters & Bosses, Miscellaneous |
| `Ammo` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `AmplifyKnockback` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AmplifyNegativeStatus` | Miscellaneous, Passives & Statuses |
| `AmplifyPositiveStatus` | Miscellaneous, Passives & Statuses |
| `AmplifyStatus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `Angel` | Characters & Bosses, Miscellaneous |
| `ApplyMultipleTimes` | Abilities & Spells, Miscellaneous |
| `ApplyPassives` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `ApplyPassivesToSpawnerWhileAlive` | Abilities & Spells, Miscellaneous |
| `ApplyShieldToApplierBasedOnMaxHealth` | Abilities & Spells, Miscellaneous |
| `ApplyStatusIfCrit` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `ApplyStatusesNextTurnBegin` | Abilities & Spells, Miscellaneous |
| `ApplyStatusesToRandomEnemiesEachTurn` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ApplyToConsumed` | Abilities & Spells, Miscellaneous |
| `ApplyToOthersWithSharedTagAndFaction` | Abilities & Spells, Miscellaneous |
| `ApplyToRandomClosestAlly` | Abilities & Spells, Miscellaneous |
| `ApplyToRandomPartyMemberIfPossible` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `ApplyToSource` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ApplyToSourceOnKill` | Abilities & Spells, Miscellaneous |
| `ApplyToTile` | Abilities & Spells, Miscellaneous |
| `ArcLightning` | Abilities & Spells, Miscellaneous |
| `ArmorBreakOnHit` | Items & Equipment, Miscellaneous |
| `ArmorDodgeChance` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ArmorPickup` | Characters & Bosses, Miscellaneous |
| `Attraction` | Abilities & Spells, Miscellaneous |
| `AutoCritLowDamage` | Miscellaneous, Passives & Statuses |
| `AutoEquipConsumables` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `AutoReanimate` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `AutocastEachRound` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `AutocastEachTurn` | Miscellaneous, Passives & Statuses |
| `AutocastEachTurnBegin` | Miscellaneous, Passives & Statuses |
| `AvoidDamagingCharmedEnemies` | Characters & Bosses, Miscellaneous |
| `AwardCoinsOnDeath` | Characters & Bosses, Miscellaneous |
| `BackflipWhenTargeted` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous |
| `BackstabAllDirections` | Characters & Bosses, Miscellaneous |
| `BackstabCritChance` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `BackstabFront` | Cat Mutations, Miscellaneous |
| `BackstabImmunity` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `BackstabWeakness` | Miscellaneous, Passives & Statuses |
| `BaitAura` | Characters & Bosses, Miscellaneous |
| `BalanceStats` | Items & Equipment, Miscellaneous |
| `BaseStatMultiply` | Characters & Bosses, Miscellaneous |
| `BasicAIDangerZone` | Characters & Bosses, Miscellaneous |
| `BasicAttackAOEBonus` | Miscellaneous, Passives & Statuses |
| `BasicAttackCantMiss` | Cat Mutations, Items & Equipment, Miscellaneous |
| `BasicAttackCritChance` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `BasicAttackDamageMultiplier` | Miscellaneous, Passives & Statuses |
| `BasicAttackStatusCarefulness` | Miscellaneous, Passives & Statuses |
| `BasicAttackStatusSwap` | Miscellaneous, Passives & Statuses |
| `BattlefieldUniqueRandomPassive` | Characters & Bosses, Miscellaneous |
| `BearTrapTrail` | Abilities & Spells, Miscellaneous |
| `BigSplashDamage` | Miscellaneous, Passives & Statuses |
| `BirdRewards` | Characters & Bosses, Miscellaneous |
| `BlackHolePassive` | Characters & Bosses, Miscellaneous |
| `BlackHoleSuck` | Characters & Bosses, Miscellaneous |
| `BlacklistPickupType` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `Bleed` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BleedThorns` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BlessingOfPeace` | Items & Equipment, Miscellaneous |
| `Blind` | Abilities & Spells, Cat Mutations, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BloatEyePassive2` | Characters & Bosses, Miscellaneous |
| `BlockAllDamage` | Characters & Bosses, Miscellaneous |
| `BlockDamageUnderThreshold` | Items & Equipment, Miscellaneous |
| `BlockNegativeStatus` | Items & Equipment, Miscellaneous |
| `BloodRain` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `Bloodzerked` | Abilities & Spells, Miscellaneous |
| `BodyGuard` | Abilities & Spells, Miscellaneous |
| `BombBehavior` | Characters & Bosses, Miscellaneous |
| `BombRatTurtle` | Abilities & Spells, Miscellaneous |
| `BoneArmorPassive` | Items & Equipment, Miscellaneous |
| `BonusAbility` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BonusAbility_DelayedApplication` | Abilities & Spells, Miscellaneous |
| `BonusCritChance` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `BonusDamage` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `BonusDamageBasedOnDistance` | Abilities & Spells, Miscellaneous |
| `BonusDamageBasedOnMana` | Abilities & Spells, Miscellaneous |
| `BonusFoodEachBattle` | Miscellaneous, Passives & Statuses |
| `BonusHealthRegenBasedOnDex` | Miscellaneous, Passives & Statuses |
| `BonusHealthRegenPerDisorder` | Miscellaneous |
| `BonusKnockbackDamage` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `BonusRangeBasedOnDex` | Miscellaneous, Passives & Statuses |
| `BonusTurnPattern` | Characters & Bosses, Miscellaneous |
| `BoobyTrapItems` | Miscellaneous, Passives & Statuses |
| `BoostAllyStatsOnDeath` | Miscellaneous, Passives & Statuses |
| `BoostDamageAura` | Miscellaneous, Passives & Statuses |
| `BoostDamageGlobalAura` | Miscellaneous, Passives & Statuses |
| `BoostHeals` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `BoostRangeAura` | Miscellaneous, Passives & Statuses |
| `BoostRangeGlobalAura` | Miscellaneous, Passives & Statuses |
| `BoostReceivedHealing` | Items & Equipment, Miscellaneous |
| `BoostWeaponDamage` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BossRewards` | Characters & Bosses, Miscellaneous |
| `BounceObject` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BounceRock` | Abilities & Spells, Miscellaneous |
| `BouncyProjectiles` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `Bound` | Abilities & Spells, Miscellaneous |
| `Bounty` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `Brace` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BraceForEachNeighboringEnemy` | Miscellaneous, Passives & Statuses |
| `BramblesOnHit` | Abilities & Spells, Miscellaneous |
| `BreakAtAux` | Items & Equipment, Miscellaneous |
| `BreakIntoRocks` | Abilities & Spells, Miscellaneous |
| `BreakOnElement` | Items & Equipment, Miscellaneous |
| `BreakWhenNoShield` | Items & Equipment, Miscellaneous |
| `Brittle` | Items & Equipment, Miscellaneous |
| `BrittleCharismaUp` | Items & Equipment, Miscellaneous |
| `BrittleConstitutionUp` | Items & Equipment, Miscellaneous |
| `BrittleDexterityUp` | Items & Equipment, Miscellaneous |
| `BrittleDuringElement` | Items & Equipment, Miscellaneous |
| `BrittleIntelligenceUp` | Items & Equipment, Miscellaneous |
| `BrittleLuckUp` | Items & Equipment, Miscellaneous |
| `BrittleSpeedUp` | Items & Equipment, Miscellaneous |
| `BrittleStrengthUp` | Items & Equipment, Miscellaneous |
| `Bruise` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Buddy` | Characters & Bosses, Miscellaneous |
| `BuffImmunity` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `BungaCheers` | Characters & Bosses, Miscellaneous |
| `BungaEntrance` | Characters & Bosses, Miscellaneous |
| `BurgleCoin` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `Burn` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ButterflySwarm` | Miscellaneous |
| `BypassRockKnockback` | Abilities & Spells, Miscellaneous |
| `CCImmunity` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `CanApplyToInanimate` | Abilities & Spells, Miscellaneous |
| `CanLevelUpWhenDead` | Items & Equipment, Miscellaneous |
| `CanMutateTo` | Characters & Bosses, Miscellaneous |
| `CanRemoveCursedItems` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `CanShield` | Characters & Bosses, Miscellaneous |
| `CancelPrimedAbilities` | Abilities & Spells, Miscellaneous |
| `CanceledQueuedInput` | Abilities & Spells, Miscellaneous |
| `CantCatchDiseases` | Items & Equipment, Miscellaneous |
| `CantDodge` | Miscellaneous, Passives & Statuses |
| `CantSpreadDiseases` | Items & Equipment, Miscellaneous |
| `CapBasicAttackDamage` | Items & Equipment, Miscellaneous |
| `CapDamage` | Abilities & Spells, Miscellaneous |
| `CapDamageFromAllies` | Miscellaneous, Passives & Statuses |
| `CapMovementAbilityRange` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `CapReceivedDamage` | Characters & Bosses, Miscellaneous |
| `CapTechSpent` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `CaptureFamiliar` | Abilities & Spells, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `CastAgain` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `CastAgainWithStatus` | Items & Equipment, Miscellaneous |
| `CatAPultAnimation` | Miscellaneous, Passives & Statuses |
| `CatPartsSizeScale` | Items & Equipment, Miscellaneous |
| `CatPartsSizeScaleStatus` | Abilities & Spells, Miscellaneous |
| `CatPartsTransform` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `CatchBoomerang` | Abilities & Spells, Miscellaneous |
| `CaveFamilyEnrage` | Characters & Bosses, Miscellaneous |
| `CaveWomanBirthControl` | Abilities & Spells, Miscellaneous |
| `CerberubsAggroTargetBehavior` | Characters & Bosses, Miscellaneous |
| `ChampionUpgradeNextMinion` | Abilities & Spells, Miscellaneous |
| `ChanceToAmbush` | Items & Equipment, Miscellaneous |
| `ChanceToBackflip` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ChanceToBlock` | Items & Equipment, Miscellaneous |
| `ChanceToBlockAndCounter` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ChanceToBreak` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `ChanceToBreakFree` | Abilities & Spells, Miscellaneous |
| `ChanceToDisableActionsIfNotCharmed` | Characters & Bosses, Miscellaneous |
| `ChanceToForceEvent` | Items & Equipment, Miscellaneous |
| `ChanceToFormChangeOnAbilityDamage` | Characters & Bosses, Miscellaneous |
| `ChanceToRevive` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ChanceToSpitOnDamage` | Characters & Bosses, Miscellaneous |
| `ChangeCatClass` | Abilities & Spells, Miscellaneous |
| `ChangeFaction` | Abilities & Spells, Miscellaneous |
| `ChangeTauntPriority` | Miscellaneous, Passives & Statuses |
| `ChangeTile` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ChangeTileOnDeath` | Characters & Bosses, Miscellaneous |
| `ChangeTileOnPop` | Characters & Bosses, Miscellaneous |
| `ChangeTileUnderCharacterAtStart` | Events & Encounters, Miscellaneous |
| `ChangeTilesUnder` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous |
| `ChaosBossFlipMidTeleport` | Abilities & Spells, Miscellaneous |
| `ChaosBossFormChange` | Abilities & Spells, Miscellaneous |
| `ChaosBossFormChangeGuide` | Characters & Bosses, Miscellaneous |
| `ChaosBossPieces` | Characters & Bosses, Miscellaneous |
| `ChaosHeadDropIn` | Characters & Bosses, Miscellaneous |
| `CharacterLightSource` | Characters & Bosses, Miscellaneous |
| `CharacterTypeGainsStatusAtBattleStart` | Events & Encounters, Miscellaneous |
| `Charge` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ChargeFists` | Abilities & Spells, Miscellaneous |
| `ChargeSpiritBombAura` | Abilities & Spells, Miscellaneous |
| `CharismaIsMaxStat` | Items & Equipment, Miscellaneous |
| `CharismaUp` | Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `CharmAllFlies` | Miscellaneous, Passives & Statuses |
| `CharmImmunity` | Items & Equipment, Miscellaneous |
| `Charmed` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `CharmedFacingForceAttack` | Abilities & Spells, Miscellaneous |
| `CharmedForceAttack` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `CherubimReaction` | Characters & Bosses, Miscellaneous |
| `ClassManaCostReduction` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Cleanse` | Abilities & Spells, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `ClearDefaultDebris` | Miscellaneous |
| `ClearFinalBossBattlefield` | Abilities & Spells, Miscellaneous |
| `ClearNegativeEffects` | Miscellaneous, Passives & Statuses |
| `ClearStarving` | Abilities & Spells, Miscellaneous |
| `Cleave` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `CloneWeaponTemp` | Abilities & Spells, Miscellaneous |
| `CobraReflex` | Miscellaneous, Passives & Statuses |
| `CockroachSwarm` | Miscellaneous |
| `CoinPickup` | Characters & Bosses, Miscellaneous |
| `CoinTossBounce` | Abilities & Spells, Miscellaneous |
| `CoinsAddDamage` | Miscellaneous, Passives & Statuses |
| `CollectPickupsOnBattleEnd` | Miscellaneous, Passives & Statuses |
| `CollectsPickups` | Abilities & Spells, Miscellaneous |
| `CollectsPickupsWithAltEffects` | Abilities & Spells, Miscellaneous |
| `CollideWithConsumed` | Abilities & Spells, Miscellaneous |
| `CollideWithThrowTarget` | Abilities & Spells, Miscellaneous |
| `CompleteItemQuest` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `Conditional_AbilityTargetIsSelf` | Abilities & Spells, Miscellaneous |
| `Conditional_ActiveWeather_Any` | Abilities & Spells, Miscellaneous |
| `Conditional_Adjacent` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_AffectedByElement` | Abilities & Spells, Miscellaneous |
| `Conditional_Ally` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_Backstab` | Abilities & Spells, Miscellaneous |
| `Conditional_BadRoll` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_Boss` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_BossOrBig` | Abilities & Spells, Miscellaneous |
| `Conditional_Buddy` | Abilities & Spells, Miscellaneous |
| `Conditional_CanBeHealed` | Abilities & Spells, Miscellaneous |
| `Conditional_Corpse` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_DebuffRoll` | Abilities & Spells, Miscellaneous |
| `Conditional_DestructibleCorpse` | Abilities & Spells, Miscellaneous |
| `Conditional_Displaceable` | Abilities & Spells, Miscellaneous |
| `Conditional_DoesDamage` | Miscellaneous, Passives & Statuses |
| `Conditional_Enemy` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_Familiar` | Abilities & Spells, Miscellaneous |
| `Conditional_FinishedSpawning` | Abilities & Spells, Miscellaneous |
| `Conditional_FirstApplicationThisTurn` | Abilities & Spells, Cat Mutations, Miscellaneous, Passives & Statuses |
| `Conditional_Flying` | Miscellaneous |
| `Conditional_FormulaIsPositive` | Abilities & Spells, Miscellaneous |
| `Conditional_GoodRoll` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_HasCleansableDebuffs` | Abilities & Spells, Miscellaneous |
| `Conditional_HasKnockback` | Characters & Bosses, Miscellaneous |
| `Conditional_HasStatus` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_HasTag` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_HealthThreshold` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `Conditional_InForm` | Abilities & Spells, Miscellaneous |
| `Conditional_IsPhysicalAttack` | Characters & Bosses, Miscellaneous |
| `Conditional_IsSelf` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `Conditional_IsTrample` | Abilities & Spells, Miscellaneous |
| `Conditional_LastHit` | Abilities & Spells, Miscellaneous |
| `Conditional_LivingPlayerCat` | Abilities & Spells, Miscellaneous |
| `Conditional_ManaThreshold` | Items & Equipment, Miscellaneous |
| `Conditional_NotAlly` | Abilities & Spells, Miscellaneous |
| `Conditional_NotBig` | Abilities & Spells, Miscellaneous |
| `Conditional_NotBoss` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `Conditional_NotBossOrBig` | Abilities & Spells, Miscellaneous |
| `Conditional_NotShielded` | Abilities & Spells, Miscellaneous |
| `Conditional_Object` | Abilities & Spells, Miscellaneous |
| `Conditional_OncePerBattle` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `Conditional_PartyMember` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_PlayerCat` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `Conditional_RandomChance` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous |
| `Conditional_Shielded` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Conditional_SourceAbilityHasTag` | Abilities & Spells, Miscellaneous |
| `Conditional_SourceHasStatus` | Abilities & Spells, Miscellaneous |
| `Conditional_SourceHasTag` | Miscellaneous, Passives & Statuses |
| `Conditional_Speculative` | Abilities & Spells, Miscellaneous |
| `Conditional_Tiny` | Miscellaneous |
| `ConductorManaRegen` | Miscellaneous, Passives & Statuses |
| `Confusion` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ConfusionEffectOnTaggedAbilities` | Miscellaneous, Passives & Statuses |
| `ConjureBonusAbility` | Abilities & Spells, Cat Mutations, Characters & Bosses, Miscellaneous |
| `ConjureCastSpellsForAllies` | Miscellaneous, Passives & Statuses |
| `ConjureRandomAbilityFromCat` | Abilities & Spells, Miscellaneous |
| `ConjureSingleUseBonusAbility` | Abilities & Spells, Miscellaneous |
| `ConstitutionUp` | Abilities & Spells, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ConsumableEffectsMultiplierBonus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ConsumablesInfiniteRange` | Miscellaneous, Passives & Statuses |
| `ConsumablesMeleeRange` | Miscellaneous, Passives & Statuses |
| `Consumed` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `ContextualHeal` | Abilities & Spells, Miscellaneous |
| `ConvertDamageToScaledStatus` | Items & Equipment, Miscellaneous |
| `CopyBasicAttackEffects` | Abilities & Spells, Miscellaneous |
| `CopyCatPassive_Initializer` | Abilities & Spells, Miscellaneous |
| `CopyPassiveSlot` | Items & Equipment, Miscellaneous |
| `CopySpells` | Abilities & Spells, Miscellaneous |
| `CorpseVaporizer` | Abilities & Spells, Miscellaneous |
| `CountAsCorpse` | Characters & Bosses, Miscellaneous |
| `CounterAttack` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `CounterAttackAfterEnemyCastSpell` | Characters & Bosses, Miscellaneous |
| `CounterNextAttacks` | Items & Equipment, Miscellaneous |
| `Counterspell` | Abilities & Spells, Miscellaneous |
| `CrackMoonHead` | Abilities & Spells, Miscellaneous |
| `Craft` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `CreateGlobalModifiers` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous |
| `CritChanceUp` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `CritsApplyStatus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `CrowAttackLink` | Characters & Bosses, Miscellaneous |
| `CureDisease` | Miscellaneous, Passives & Statuses |
| `CurrentWeaponAddElectricElement` | Abilities & Spells, Miscellaneous |
| `CurrentWeaponAddPoison` | Abilities & Spells, Miscellaneous |
| `CurrentWeaponDamageUp` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `CyborgTurns` | Miscellaneous |
| `DamageBasedOnMissingHealth` | Abilities & Spells, Miscellaneous |
| `DamageDistanceAOEFalloff` | Abilities & Spells, Miscellaneous |
| `DamageEnemiesOnHeal` | Miscellaneous, Passives & Statuses |
| `DamageEnemiesOnKill` | Miscellaneous, Passives & Statuses |
| `DamageFromBehindOnly` | Characters & Bosses, Miscellaneous |
| `DamageIfDidntUseSpecificAbility` | Miscellaneous, Passives & Statuses |
| `DamageNeighborTilesWhenCastSpell` | Miscellaneous, Passives & Statuses |
| `DamageNeighborsAfterMove` | Miscellaneous, Passives & Statuses |
| `DamageNeighborsOnEndMove` | Miscellaneous, Passives & Statuses |
| `DamageOrHealConditionally` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DamageReductionAura` | Miscellaneous, Passives & Statuses |
| `DamageTrinket` | Abilities & Spells, Miscellaneous |
| `DamageUp` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DamageWeapon` | Abilities & Spells, Miscellaneous |
| `DashFury` | Abilities & Spells, Miscellaneous |
| `DeadAltAbility` | Abilities & Spells, Miscellaneous |
| `DeathRattle` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DeathRattleRevive` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `DeathwormUnderground` | Abilities & Spells, Miscellaneous |
| `DebuffImmunity` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DecoySwapper` | Abilities & Spells, Miscellaneous |
| `DeferVaporize` | Abilities & Spells, Miscellaneous |
| `DelayCastAbility` | Abilities & Spells, Miscellaneous |
| `DelayedAutoRevive` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `DelayedFury` | Abilities & Spells, Miscellaneous |
| `DelayedPain` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `DelayedWind` | Miscellaneous, Passives & Statuses |
| `DelayedWindCone` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `DelayedWindTrail` | Abilities & Spells, Miscellaneous |
| `DeleteInanimateObjectsChance` | Miscellaneous |
| `DeleteObject` | Abilities & Spells, Miscellaneous |
| `DeleteTraps` | Abilities & Spells, Miscellaneous |
| `DemonicGlyphFrames` | Characters & Bosses, Miscellaneous |
| `DemonicGlyphStealer` | Characters & Bosses, Miscellaneous |
| `DemonicGlyph_Bite` | Characters & Bosses, Miscellaneous |
| `DemonicGlyph_Bounce` | Characters & Bosses, Miscellaneous |
| `DemonicGlyph_Fire` | Characters & Bosses, Miscellaneous |
| `DemonicGlyph_Movement` | Characters & Bosses, Miscellaneous |
| `DemonicGlyph_Summon` | Characters & Bosses, Miscellaneous |
| `DepressionAura` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DestroyEquipmentAndAttachParasite` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `DestroyNeckArmor` | Abilities & Spells, Miscellaneous |
| `DestroyTrinket` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `DestroyWeapon` | Abilities & Spells, Miscellaneous |
| `DestroyWeaponThrow` | Abilities & Spells, Miscellaneous |
| `DexterityUp` | Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DiceBehavior` | Characters & Bosses, Miscellaneous |
| `DicerArt` | Characters & Bosses, Miscellaneous |
| `Die` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `DieViaAbilityInternally` | Abilities & Spells, Miscellaneous |
| `DieViolently` | Abilities & Spells, Miscellaneous |
| `DieWhenOnlyGolemsLeft` | Characters & Bosses, Miscellaneous |
| `DieWhenSpawnerDies` | Characters & Bosses, Miscellaneous |
| `DiesToElement` | Characters & Bosses, Miscellaneous |
| `DiesToPiercingAndSpikes` | Characters & Bosses, Miscellaneous |
| `DigestDeadBodies` | Characters & Bosses, Miscellaneous |
| `DiminishingHealthRegen` | Abilities & Spells, Cat Mutations, Miscellaneous, Passives & Statuses |
| `DinoLegAnimation` | Abilities & Spells, Miscellaneous |
| `DisableAbilities` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `DisableAbilitiesWithTag` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `DisablePassiveSlot` | Items & Equipment, Miscellaneous |
| `DisableSpells` | Characters & Bosses, Miscellaneous |
| `DisableTrample` | Abilities & Spells, Miscellaneous |
| `DisableWeapon` | Abilities & Spells, Miscellaneous |
| `Disguised` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `DisguisedTrapper` | Characters & Bosses, Miscellaneous |
| `Displace` | Abilities & Spells, Miscellaneous |
| `DisplaceToAbilityTarget` | Abilities & Spells, Miscellaneous |
| `DisplaceToOriginalPosition` | Abilities & Spells, Miscellaneous |
| `DisplaceTowardsSource` | Abilities & Spells, Miscellaneous |
| `DisplayBuddyCatOnSpawn` | Characters & Bosses, Miscellaneous |
| `DisplayDangerAOE` | Characters & Bosses, Miscellaneous |
| `DissolveRandomArmorPiece` | Abilities & Spells, Miscellaneous |
| `DissuadeInstakills` | Characters & Bosses, Miscellaneous |
| `DistanceBonusDamage` | Miscellaneous, Passives & Statuses |
| `Divide4OnDeath` | Characters & Bosses, Miscellaneous |
| `DivineShield` | Abilities & Spells, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DivineShieldPickup` | Characters & Bosses, Miscellaneous |
| `DoDamage` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `DoDistortionRing` | Abilities & Spells, Miscellaneous |
| `DoScreenShake` | Abilities & Spells, Miscellaneous |
| `DodgeChance` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `DodgeChanceWithBlindSpot` | Characters & Bosses, Miscellaneous |
| `DodgeChance_Status` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous |
| `DodgeWhenTargeted` | Characters & Bosses, Miscellaneous |
| `DontHealEnemies` | Abilities & Spells, Miscellaneous |
| `Doomed` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `DoubleCast` | Abilities & Spells, Miscellaneous |
| `DoubleCastSpell` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `DoubleCastSpellIfManaCostUnderThreshold` | Items & Equipment, Miscellaneous |
| `DoubleCastSpellThisTurn` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `DoubleCastSpellsEachTurn_Status` | Abilities & Spells, Miscellaneous |
| `DoubleCastTaggedSpells` | Items & Equipment, Miscellaneous |
| `DoubleCastWeapons` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `DoubleLoot` | Abilities & Spells, Miscellaneous |
| `DoubleReceivedNegativeStatus` | Items & Equipment, Miscellaneous |
| `DoubleReceivedPositiveStatus` | Items & Equipment, Miscellaneous |
| `DoubleStatus` | Abilities & Spells, Miscellaneous |
| `DrainAllyCatsForFleshGolem` | Abilities & Spells, Miscellaneous |
| `DrinkWater` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous |
| `DropAsFamiliarOnArmorBreak` | Items & Equipment, Miscellaneous |
| `DropAsFamiliarOnTookDamage` | Items & Equipment, Miscellaneous |
| `DropSoulJarOnDeath` | Items & Equipment, Miscellaneous |
| `Drowsy` | Abilities & Spells, Miscellaneous |
| `DuplicateRandomEquippedItem` | Abilities & Spells, Miscellaneous |
| `DurabilityTransform` | Items & Equipment, Miscellaneous |
| `DustCloudBehavior` | Characters & Bosses, Miscellaneous |
| `DustOnHit` | Abilities & Spells, Miscellaneous |
| `Dybbuk1HPTracker` | Characters & Bosses, Miscellaneous |
| `DybbukPossessed` | Abilities & Spells, Miscellaneous |
| `EachSpellFreeAtFullMana` | Miscellaneous, Passives & Statuses |
| `ElectricArcs` | Characters & Bosses, Miscellaneous |
| `ElementImmune` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ElementWeakness` | Characters & Bosses, Miscellaneous |
| `ElementalManaCostReduction` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `EliteFlatTint` | Miscellaneous |
| `EliteParticle` | Miscellaneous |
| `EliteTint` | Miscellaneous |
| `EliteUpgradeNextMinion` | Abilities & Spells, Miscellaneous |
| `Else` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `EmptyMana` | Miscellaneous, Passives & Statuses |
| `EmptyMind` | Abilities & Spells, Miscellaneous |
| `EnableWeather` | Abilities & Spells, Miscellaneous |
| `EndTurn` | Abilities & Spells, Miscellaneous |
| `EnemiesGetPickupsKnockedOut` | Miscellaneous, Passives & Statuses |
| `Enlarge` | Abilities & Spells, Miscellaneous |
| `EnrageOnDamage` | Characters & Bosses, Miscellaneous |
| `EnterMount` | Abilities & Spells, Miscellaneous |
| `EquipPermanentItem` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `EquipRandomTemporaryItemFromPool` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `EquipTemporaryItem` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `EquipmentPassiveMultiplierBonus` | Miscellaneous, Passives & Statuses |
| `EquipmentSetBonusBonus` | Miscellaneous, Passives & Statuses |
| `EraseSpawnCoins` | Characters & Bosses, Miscellaneous |
| `EventBounterHunterPassive` | Characters & Bosses, Miscellaneous |
| `EventBounty` | Abilities & Spells, Miscellaneous |
| `EvolveAbilityFromPool` | Abilities & Spells, Miscellaneous |
| `ExcludeFromEvents` | Items & Equipment, Miscellaneous |
| `ExhaustionRoundChange` | Miscellaneous, Passives & Statuses |
| `ExistUntilIdleUpkeep` | Abilities & Spells, Miscellaneous |
| `ExpireOnSpawnerTurnEnd` | Characters & Bosses, Miscellaneous |
| `ExplodeCharacter` | Abilities & Spells, Miscellaneous |
| `ExplodeCharacter_DeathBloom` | Abilities & Spells, Miscellaneous |
| `ExplodeCharacter_DeathBloom2` | Abilities & Spells, Miscellaneous |
| `ExplodeCharacter_NoDie` | Abilities & Spells, Miscellaneous |
| `ExplodeCharacter_Party` | Abilities & Spells, Miscellaneous |
| `ExplodeCharacter_PartyBoss` | Abilities & Spells, Miscellaneous |
| `ExplodeCharacter_RockCrusher` | Abilities & Spells, Miscellaneous |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Abilities & Spells, Miscellaneous |
| `ExplodeOverkilledEnemies` | Miscellaneous, Passives & Statuses |
| `ExplosionIfHitSomething` | Abilities & Spells, Miscellaneous |
| `ExplosionImmunity` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ExtraBasicAttacks` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ExtraBasicAttacks_Status` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous |
| `ExtraBasicMoves_Status` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ExtraDispersedTurns` | Characters & Bosses, Miscellaneous |
| `ExtraInjuryOnDeath` | Miscellaneous, Passives & Statuses |
| `ExtraMovePoints` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ExtraStatusWhenDealingDamage` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ExtraTrinketUses` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ExtraTurnsPerTaggedUnit` | Characters & Bosses, Miscellaneous |
| `ExtraWeaponAttacks` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `FaceArmorPassiveMultiplierBonus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `FaceAway` | Abilities & Spells, Cat Mutations, Miscellaneous, Passives & Statuses |
| `FaceAwayLastDamage` | Characters & Bosses, Miscellaneous |
| `FaceCamera` | Abilities & Spells, Miscellaneous |
| `FaceLastDamage` | Characters & Bosses, Miscellaneous |
| `FaceShield` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `FactionConversion` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `FactionDisguiseSource` | Abilities & Spells, Miscellaneous |
| `FactionUprising` | Miscellaneous |
| `FadeInsteadOfDie` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `FamiliarBonusAbility` | Miscellaneous, Passives & Statuses |
| `FamiliarSecondaryDamageImmunity` | Miscellaneous, Passives & Statuses |
| `FastKnockback` | Abilities & Spells, Miscellaneous |
| `Fear` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `FillMana` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `FinalBossBeamQueue` | Characters & Bosses, Miscellaneous |
| `FinalBossBecomeTheChild` | Characters & Bosses, Miscellaneous |
| `FinalBossHitCountdownBoris` | Characters & Bosses, Miscellaneous |
| `FinalBossHitCountdownExplosive` | Characters & Bosses, Miscellaneous |
| `FinalBossHitCountdownHoly` | Characters & Bosses, Miscellaneous |
| `FinalBossPupils` | Characters & Bosses, Miscellaneous |
| `FinalBossQueueBeam` | Abilities & Spells, Miscellaneous |
| `FinalBossShield` | Characters & Bosses, Miscellaneous |
| `FinalBossShieldHealth` | Characters & Bosses, Miscellaneous |
| `FinalBossSyncAnimations` | Characters & Bosses, Miscellaneous |
| `FindExtraItemFromPoolOnBattleEnd` | Items & Equipment, Miscellaneous |
| `FindItem` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `FindItemFromPool` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `FireArmor2` | Abilities & Spells, Miscellaneous |
| `FireStorm` | Miscellaneous |
| `FireflySwarm` | Miscellaneous |
| `Flammable` | Items & Equipment, Miscellaneous |
| `FlatAIBonus` | Abilities & Spells, Miscellaneous |
| `FlatHealWhenDealDamage` | Cat Mutations, Miscellaneous |
| `FlatLeech` | Abilities & Spells, Cat Mutations, Miscellaneous, Passives & Statuses |
| `FlatLeechIfDamaged` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `FlingObjectsOnTop` | Characters & Bosses, Miscellaneous |
| `FlippedFacingForceAttack` | Miscellaneous, Passives & Statuses |
| `FloatingRockTrap` | Abilities & Spells, Miscellaneous |
| `FlowerPowerAuraBrace` | Miscellaneous, Passives & Statuses |
| `FlowerPowerAuraStrength` | Miscellaneous, Passives & Statuses |
| `FlowersOnEndTurn` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `FlowersOnHit` | Abilities & Spells, Miscellaneous |
| `FlushmasterCelebration` | Characters & Bosses, Miscellaneous |
| `FlyDamageIncrease` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `FlySwarm` | Miscellaneous |
| `Fog` | Miscellaneous |
| `ForceAttack` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `ForceCollectsPickups` | Abilities & Spells, Miscellaneous |
| `ForceDisplace` | Abilities & Spells, Miscellaneous |
| `ForceDodgeEverything` | Characters & Bosses, Miscellaneous |
| `ForceImmediateMove` | Abilities & Spells, Miscellaneous |
| `ForceImmediateMoveAndAttack` | Abilities & Spells, Miscellaneous |
| `ForceMoveAndAttack` | Abilities & Spells, Miscellaneous |
| `ForceMoveAway` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ForceMoveNonAlliesInRangeTowardsTile` | Abilities & Spells, Miscellaneous |
| `ForceMoveTowards` | Abilities & Spells, Miscellaneous |
| `ForceMoveTowardsEnemies` | Abilities & Spells, Miscellaneous |
| `ForceMoveTowardsTaggedObject` | Abilities & Spells, Miscellaneous |
| `ForceSpecificInjury` | Miscellaneous, Passives & Statuses |
| `ForceTransferWeapon` | Abilities & Spells, Miscellaneous |
| `ForceUseAbility` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ForceUseAbilityOnTarget` | Items & Equipment, Miscellaneous |
| `ForceUseAbility_NonStack` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `FormChange` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `FormChangeDuringWeatherElement` | Characters & Bosses, Miscellaneous |
| `FormChangeHealthThreshold` | Characters & Bosses, Miscellaneous |
| `FormChangeOffMap` | Characters & Bosses, Miscellaneous |
| `FormChangeOnElementInfluence` | Characters & Bosses, Miscellaneous |
| `FormChangeWhenBuddyDies` | Characters & Bosses, Miscellaneous |
| `FormChangeWhileHasStatus` | Characters & Bosses, Miscellaneous |
| `FormChangeWhilePrimingAbility` | Characters & Bosses, Miscellaneous |
| `FormChanger` | Characters & Bosses, Miscellaneous |
| `Fragile` | Items & Equipment, Miscellaneous |
| `FragileDuringElement` | Items & Equipment, Miscellaneous |
| `FrankBolts` | Items & Equipment, Miscellaneous |
| `FreeFirstCast` | Abilities & Spells, Miscellaneous |
| `FreeFirstCastAndAfterSpendMana` | Abilities & Spells, Miscellaneous |
| `FreeFirstCastEachMatch` | Abilities & Spells, Miscellaneous |
| `FreePathfindElement` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `FreeSpell` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `FreeSpellsAtFullMana` | Miscellaneous, Passives & Statuses |
| `Freeze` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `FreezePiercing` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `FrontstabBasicAttackCritChance` | Miscellaneous, Passives & Statuses |
| `FrontstabCritChance` | Miscellaneous, Passives & Statuses |
| `FullBlockEverything` | Characters & Bosses, Miscellaneous |
| `FullBlockEverythingTo0Damage` | Characters & Bosses, Miscellaneous |
| `FullHeal` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `FullHealthAllStatsUp` | Miscellaneous, Passives & Statuses |
| `FullHealthCritChance` | Miscellaneous, Passives & Statuses |
| `FullHealthManaRegen` | Miscellaneous, Passives & Statuses |
| `FurnitureStats` | Miscellaneous, Passives & Statuses |
| `Fury` | Abilities & Spells, Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `GainCoins` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `GainCoinsRange` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `GainDisorder` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `GainDisorderFromPool` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `GainDisorderFromPool_PostCast` | Abilities & Spells, Miscellaneous |
| `GainExtraShield` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `GainManaWhenAnythingDies` | Cat Mutations, Miscellaneous |
| `GasCanBehavior` | Characters & Bosses, Miscellaneous |
| `GasCloudBehavior2` | Characters & Bosses, Miscellaneous |
| `GeminiTwin` | Characters & Bosses, Miscellaneous |
| `GenericBuff` | Abilities & Spells, Miscellaneous |
| `GenericDebuff` | Abilities & Spells, Miscellaneous |
| `GetAggroTarget` | Abilities & Spells, Miscellaneous |
| `GiveBoundItemToTarget` | Abilities & Spells, Miscellaneous |
| `GlobalEnemyAutoRevive` | Items & Equipment, Miscellaneous |
| `GlobalFamiliarDamageBoost` | Miscellaneous |
| `GlobalFamiliarMoveBoost` | Miscellaneous |
| `GlobalFlowerTrapperAura` | Miscellaneous |
| `GlobalHealthRegenAura` | Miscellaneous |
| `GlobalManaBurnAura` | Miscellaneous |
| `GlobalManaDrainAura` | Characters & Bosses, Miscellaneous |
| `GlobalMeleeRevengeDamage` | Items & Equipment, Miscellaneous |
| `GlobalSpawnCharacter` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `GlobalSpawnOnRoundEnd` | Miscellaneous |
| `GoopImmunity` | Characters & Bosses, Miscellaneous |
| `GoopWalk` | Characters & Bosses, Miscellaneous |
| `Grappled` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `Grappling` | Characters & Bosses, Miscellaneous |
| `GrassTileHealing` | Miscellaneous, Passives & Statuses |
| `GroundFlopper` | Characters & Bosses, Miscellaneous |
| `GuillotinaDeathHead` | Characters & Bosses, Miscellaneous |
| `HPAltStates` | Characters & Bosses, Miscellaneous |
| `HPGainBlock` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `HarpoonTrapPassive` | Characters & Bosses, Miscellaneous |
| `HeadArmorPassiveMultiplierBonus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `HealAlliesEachTurn` | Miscellaneous, Passives & Statuses |
| `HealAndOverhealToShield` | Miscellaneous, Passives & Statuses |
| `HealAtStart` | Miscellaneous, Passives & Statuses |
| `HealDamagesEnemies` | Miscellaneous, Passives & Statuses |
| `HealNeighborsEachTurn` | Characters & Bosses, Miscellaneous |
| `HealPercentMaxHP` | Abilities & Spells, Miscellaneous |
| `HealRandomInjury` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `HealTo` | Abilities & Spells, Miscellaneous |
| `HealsAlsoRegenMana` | Miscellaneous, Passives & Statuses |
| `HealsCanRevive` | Miscellaneous, Passives & Statuses |
| `HealthGain` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `HealthMultiplier` | Miscellaneous |
| `HealthPickup` | Characters & Bosses, Miscellaneous |
| `HealthRegenUp` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `HeatWave` | Miscellaneous |
| `HeavyHits` | Abilities & Spells, Miscellaneous |
| `Hex` | Abilities & Spells, Miscellaneous |
| `HiddenDoomed` | Characters & Bosses, Miscellaneous |
| `HideEquipment` | Abilities & Spells, Miscellaneous |
| `HideSomeHudStuff` | Items & Equipment, Miscellaneous |
| `HitExplosion` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `HitlerExecute` | Characters & Bosses, Miscellaneous |
| `HolyDamageBlessing` | Miscellaneous, Passives & Statuses |
| `HolyDamageMultiplierBonus` | Miscellaneous, Passives & Statuses |
| `HolyShieldTransferToSpawner` | Miscellaneous, Passives & Statuses |
| `HolyShieldTransferToTaggedMinions` | Miscellaneous, Passives & Statuses |
| `HouseFoodRequirementMultiplier` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `IceBlockBehavior` | Characters & Bosses, Miscellaneous |
| `IgnoreDamage` | Abilities & Spells, Miscellaneous |
| `IgnoreDebuffs` | Abilities & Spells, Miscellaneous |
| `IgnoreSelf` | Abilities & Spells, Miscellaneous |
| `IgnoreTiles` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `IllusionTint` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `ImmediateAbilityReaction` | Characters & Bosses, Miscellaneous |
| `ImmediateUseAbility` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous |
| `ImmediateUseAbility_Instant` | Items & Equipment, Miscellaneous |
| `ImmediateUseDirectionalAbility` | Abilities & Spells, Miscellaneous |
| `Immobile` | Abilities & Spells, Cat Mutations, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ImmobilePassive` | Characters & Bosses, Miscellaneous |
| `Imprison` | Abilities & Spells, Miscellaneous |
| `IncAuxCounterClamped` | Abilities & Spells, Miscellaneous |
| `IncAuxCounterCycle` | Abilities & Spells, Miscellaneous |
| `IncreaseCumulativeBlastDamage` | Abilities & Spells, Miscellaneous |
| `IncreaseExplosionDamage` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `IncreaseExplosionSize` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `IncreaseHealingSpellRange` | Miscellaneous, Passives & Statuses |
| `IncreaseItemAuxOnKill` | Abilities & Spells, Miscellaneous |
| `IncreaseItemUsesOnEquip` | Miscellaneous, Passives & Statuses |
| `IncreaseSpellRange` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `InheritSpawnerStats` | Characters & Bosses, Miscellaneous |
| `InjuryImmunity` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `InnateElement` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `InsertIntoBackgroundPlaceholder` | Characters & Bosses, Miscellaneous |
| `Instakill` | Abilities & Spells, Cat Mutations, Miscellaneous |
| `InstantMaxHealthUp` | Abilities & Spells, Miscellaneous |
| `IntelligenceUp` | Abilities & Spells, Cat Mutations, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `InterchangeDisabler` | Abilities & Spells, Miscellaneous |
| `InterchangeMoveActPoints` | Abilities & Spells, Miscellaneous |
| `InvertBrainFaction` | Miscellaneous, Passives & Statuses |
| `Invulnerable` | Abilities & Spells, Miscellaneous |
| `ItemAuxTransform` | Items & Equipment, Miscellaneous |
| `JesterLevelUpRerolls` | Items & Equipment, Miscellaneous |
| `JohnnyCriesForWashers` | Abilities & Spells, Miscellaneous |
| `JohnnyNeedsWashing` | Characters & Bosses, Miscellaneous |
| `JohnnyWasher` | Characters & Bosses, Miscellaneous |
| `JoinSpawnerFaction` | Miscellaneous, Passives & Statuses |
| `JudgementDay` | Miscellaneous |
| `JumpAttackLeaveBehind` | Abilities & Spells, Miscellaneous |
| `JustInCaseTrample` | Abilities & Spells, Miscellaneous |
| `KaijuKnockbackImmune` | Characters & Bosses, Miscellaneous |
| `KaijuWinCon` | Characters & Bosses, Miscellaneous |
| `KillEnemyOfTypeAtBattleStart` | Events & Encounters, Miscellaneous |
| `KillsToMeat` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `KineticSpikes` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `KnockOutClone` | Abilities & Spells, Miscellaneous |
| `KnockOutCoin` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `KnockUpAndAway` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous |
| `Knockback` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `KnockbackDamageImmuneUntilSettled` | Abilities & Spells, Miscellaneous |
| `KnockbackDirectionIsFacingDirection` | Abilities & Spells, Miscellaneous |
| `KnockbackIfCrit` | Items & Equipment, Miscellaneous |
| `KnockbackImmunity` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `LateStatusApplication` | Abilities & Spells, Miscellaneous |
| `LaunchOffScreen` | Abilities & Spells, Miscellaneous |
| `LaunchOffScreenInstakill` | Abilities & Spells, Miscellaneous |
| `LeaveBehind` | Abilities & Spells, Miscellaneous |
| `LeaveBehindOnceEachMove` | Items & Equipment, Miscellaneous |
| `LeaveBehindRockOnKnockback` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `Leech` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `LeechPercent` | Miscellaneous, Passives & Statuses |
| `Leeches` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `LegacySpawnSavedCatIfExists` | Characters & Bosses, Miscellaneous |
| `LevelUpClassOverride` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `Lifesteal` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `LightningAspectCharge` | Miscellaneous, Passives & Statuses |
| `LimitDamage` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `LimitHeal` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `LimitSelfKnockbackDamage` | Miscellaneous, Passives & Statuses |
| `LimitedTileTrail` | Miscellaneous, Passives & Statuses |
| `LineOfSightTrueSightAura` | Miscellaneous, Passives & Statuses |
| `LobbedHook` | Miscellaneous, Passives & Statuses |
| `LockOrientationFaceTile` | Characters & Bosses, Miscellaneous |
| `LoopingSoundWhileAlive` | Characters & Bosses, Miscellaneous |
| `LowGravityKnockbackBoost` | Miscellaneous |
| `LowGravityRangeBoost` | Miscellaneous |
| `LowHealthAllyDodgeChanceAura` | Miscellaneous, Passives & Statuses |
| `LowerAmbientLight` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `LuckUp` | Abilities & Spells, Cat Mutations, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Madness` | Abilities & Spells, Characters & Bosses, Events & Encounters, Miscellaneous, Passives & Statuses |
| `MadnessChanceOnTurnBegin` | Abilities & Spells, Miscellaneous |
| `MagicDamageImmune` | Characters & Bosses, Miscellaneous |
| `MagicWeakness` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `MakeBasicAttackPassThroughThings` | Miscellaneous, Passives & Statuses |
| `MakeBasicAttackPull` | Cat Mutations, Items & Equipment, Miscellaneous |
| `MakeSpellsRequireCharge` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `MakeWeaponUnbreakable` | Abilities & Spells, Miscellaneous |
| `MamaCatAnimations` | Characters & Bosses, Miscellaneous |
| `ManaCostReduction` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ManaCostReductionTagged` | Miscellaneous, Passives & Statuses |
| `ManaGain` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ManaGainRange` | Items & Equipment, Miscellaneous |
| `ManaLeeches` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ManaPickup` | Characters & Bosses, Miscellaneous |
| `ManaRegenMultiplierIfManaEmpty` | Miscellaneous, Passives & Statuses |
| `ManaSteal` | Abilities & Spells, Miscellaneous |
| `ManaStealToHealth` | Abilities & Spells, Miscellaneous |
| `ManglerAttack` | Abilities & Spells, Miscellaneous |
| `ManglerMonsterPassive` | Characters & Bosses, Miscellaneous |
| `ManglerShuffle` | Abilities & Spells, Miscellaneous |
| `Marked` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `MassAttackThis` | Abilities & Spells, Miscellaneous |
| `Math` | Abilities & Spells, Miscellaneous |
| `MaxAccuracy` | Miscellaneous, Passives & Statuses |
| `MaxHPUp` | Abilities & Spells, Miscellaneous |
| `MaxStartingMana` | Miscellaneous, Passives & Statuses |
| `Meaty` | Abilities & Spells, Miscellaneous |
| `MegaDinoDropController` | Characters & Bosses, Miscellaneous |
| `MeleeRevengeDamage` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `MergeDamageInstance` | Abilities & Spells, Miscellaneous |
| `Metal` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `MeteorShower` | Miscellaneous |
| `Meteornado` | Miscellaneous |
| `Metronome` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `MimicMetronome` | Abilities & Spells, Miscellaneous |
| `MimicSpawnerAttacks` | Characters & Bosses, Miscellaneous |
| `MiniVolcanoReaction` | Characters & Bosses, Miscellaneous |
| `MinimumKnockbackFromAllDamage` | Characters & Bosses, Miscellaneous |
| `MinimumKnockbackFromPhysicalAttacks` | Characters & Bosses, Miscellaneous |
| `MinimumTech` | Miscellaneous, Passives & Statuses |
| `MissChance` | Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ModelingClayPassive` | Items & Equipment, Miscellaneous |
| `ModifyAbility` | Items & Equipment, Miscellaneous |
| `ModularPickup` | Characters & Bosses, Miscellaneous |
| `MonkCatReactionAbilities` | Characters & Bosses, Miscellaneous |
| `MonkStanceSwitch` | Abilities & Spells, Miscellaneous |
| `MonkStances` | Cat Classes, Miscellaneous |
| `MoonHeadCrackedVisual` | Characters & Bosses, Miscellaneous |
| `MoonHeadFinisherEnabler` | Abilities & Spells, Miscellaneous |
| `MotherGrowController` | Characters & Bosses, Miscellaneous |
| `MotherTumorDebugForcePass` | Abilities & Spells, Miscellaneous |
| `MotherTumorPassive` | Characters & Bosses, Miscellaneous |
| `MotherTumorSpawnInCapture` | Characters & Bosses, Miscellaneous |
| `Mount` | Characters & Bosses, Miscellaneous |
| `MoveAfterAnyAttemptedAttack` | Characters & Bosses, Miscellaneous |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `MoveAwayFromDamageSource` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `MoveAwayWhenEnemyAdjacent` | Characters & Bosses, Miscellaneous |
| `MoveQuivered` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `MoveRandomly` | Miscellaneous, Passives & Statuses |
| `MoveSpeedMultiplier` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `MoveTowardsDamageSource` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `MoveTowardsKillers` | Characters & Bosses, Miscellaneous |
| `MoveWhenDamaged` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `MovementReaction` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `MovementUp` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `MultiSpawnOnDeath` | Characters & Bosses, Miscellaneous |
| `MulticatHeads` | Characters & Bosses, Miscellaneous |
| `MulticlassLevelUp` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `MultiplyCoinsOnBattleStart` | Items & Equipment, Miscellaneous |
| `MultiplyReceivedHealing` | Items & Equipment, Miscellaneous |
| `MutateAfterXTurns` | Characters & Bosses, Miscellaneous |
| `MutateViaAbility` | Characters & Bosses, Miscellaneous |
| `MuteDemonicGlyphDisplay` | Characters & Bosses, Miscellaneous |
| `Muted` | Abilities & Spells, Miscellaneous |
| `NeckArmorPassiveMultiplierBonus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `NextAbilityHeals` | Abilities & Spells, Miscellaneous |
| `NextActionLuckUp` | Abilities & Spells, Miscellaneous |
| `NextAttackBonusRange` | Abilities & Spells, Miscellaneous |
| `NextAttackSpecialCrit` | Abilities & Spells, Miscellaneous |
| `NextBasicAttackCritsThisTurn` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `NextBattleStatus` | Miscellaneous, Passives & Statuses |
| `NextBattleStatusStacks` | Abilities & Spells, Miscellaneous |
| `NextDamageReduceAndHealAllies` | Abilities & Spells, Miscellaneous |
| `NextPlayerCatTakesExtraTurn` | Items & Equipment, Miscellaneous |
| `NextTurnDoubleRangedDamage` | Abilities & Spells, Miscellaneous |
| `NoCorpses` | Items & Equipment, Miscellaneous |
| `NoHealthOnlyShield` | Characters & Bosses, Miscellaneous |
| `NoHealthRegen` | Events & Encounters, Miscellaneous |
| `NoManaRegen` | Events & Encounters, Miscellaneous, Passives & Statuses |
| `NoReflection` | Miscellaneous, Passives & Statuses |
| `NonLethal` | Miscellaneous, Passives & Statuses |
| `NonStackingDivineShield` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `NonStackingShield` | Miscellaneous |
| `NubbyTossPriority` | Miscellaneous, Passives & Statuses |
| `NukeQuestFinalBossModifications` | Abilities & Spells, Miscellaneous |
| `ObjectDetector` | Items & Equipment, Miscellaneous |
| `ObjectOnHit` | Abilities & Spells, Miscellaneous |
| `ObjectOnHitCharacter` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ObjectOnHitEmpty` | Abilities & Spells, Miscellaneous |
| `ObjectOnHitFullyEmpty` | Abilities & Spells, Miscellaneous |
| `OneUseSpellDamageUp` | Miscellaneous, Passives & Statuses |
| `OrthogonalAIDangerZone` | Characters & Bosses, Miscellaneous |
| `Ostracized` | Abilities & Spells, Miscellaneous |
| `OverHealToShield` | Abilities & Spells, Miscellaneous |
| `OverHealToStatuses` | Abilities & Spells, Miscellaneous |
| `OverManaReducesManaCosts` | Miscellaneous |
| `OverhealGainsBothShield` | Miscellaneous, Passives & Statuses |
| `OverrideBasicAttack` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `OverrideChainKnockback` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `OverrideChainKnockbackDamage` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `OverrideDamage` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `OverrideKnockbackDamage` | Abilities & Spells, Miscellaneous |
| `OverrideMaxHealth` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `OverrideMaxMana` | Miscellaneous, Passives & Statuses |
| `OverridePalette` | Miscellaneous, Passives & Statuses |
| `PackHunting` | Characters & Bosses, Miscellaneous |
| `ParasitesArentCursed` | Miscellaneous, Passives & Statuses |
| `PartialCleanse` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PartialPurge` | Abilities & Spells, Miscellaneous |
| `PassiveAfterXKills` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `PassiveAtFullHealth` | Miscellaneous, Passives & Statuses |
| `PassiveAtHealthThreshold` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `PassiveAtInjuryThreshold` | Miscellaneous, Passives & Statuses |
| `PassiveAtStatThreshold` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `PassiveGroup` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `PassiveIfAllArmorEmpty` | Miscellaneous, Passives & Statuses |
| `PassiveIfEmptyFace` | Miscellaneous, Passives & Statuses |
| `PassiveIfEmptyHead` | Miscellaneous, Passives & Statuses |
| `PassiveIfEmptyNeck` | Miscellaneous, Passives & Statuses |
| `PassiveIfStrAuxEquals` | Items & Equipment, Miscellaneous |
| `PassiveIfWeaponIsUsable` | Items & Equipment, Miscellaneous |
| `PassiveLevelScaledStatus` | Miscellaneous, Passives & Statuses |
| `PassiveLevelUpAtCombatEnd` | Miscellaneous, Passives & Statuses |
| `PassiveUntilCastSpell` | Miscellaneous, Passives & Statuses |
| `PassiveUntilGetKill` | Miscellaneous, Passives & Statuses |
| `PassiveWhenAffectedByElement` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PassiveWhenAtFullMana` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `PassiveWhenDead` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `PassiveWhenOnTile` | Items & Equipment, Miscellaneous |
| `PassiveWhenTheAlpha` | Miscellaneous, Passives & Statuses |
| `PassiveWhileHasDurability` | Items & Equipment, Miscellaneous |
| `PassiveWhileHasStatus` | Cat Mutations, Characters & Bosses, Miscellaneous |
| `PassiveWhileInMonkMeleeStance` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `PassiveWhileInMonkRangedStance` | Miscellaneous, Passives & Statuses |
| `PassiveWhileNotHasStatus` | Characters & Bosses, Miscellaneous |
| `PassiveWhileNotTakingTurn` | Abilities & Spells, Miscellaneous |
| `PassiveWhilePreviewingMonkRangedStance` | Miscellaneous, Passives & Statuses |
| `PassiveWhileShielded` | Items & Equipment, Miscellaneous |
| `PercentHeal` | Miscellaneous, Passives & Statuses |
| `PermanentCharisma` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `PermanentCharm` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `PermanentConfusion` | Events & Encounters, Miscellaneous |
| `PermanentConstitution` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PermanentDexterity` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PermanentImmobile` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `PermanentIntelligence` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PermanentItems` | Miscellaneous, Passives & Statuses |
| `PermanentKitten` | Miscellaneous, Passives & Statuses |
| `PermanentLuck` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `PermanentMadness` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PermanentSpeed` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PermanentStrength` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PermanentUpgradeRandomActive` | Abilities & Spells, Miscellaneous |
| `PermanentUpgradeRandomActiveOrPassive` | Abilities & Spells, Miscellaneous |
| `PersistentElement` | Miscellaneous |
| `Petrify` | Abilities & Spells, Cat Mutations, Miscellaneous, Passives & Statuses |
| `Phasing` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `PhysicalAttacksMiss` | Items & Equipment, Miscellaneous |
| `Piercing` | Miscellaneous, Passives & Statuses |
| `Plant` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `PlayBackground` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `Poison` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PoisonLace` | Abilities & Spells, Miscellaneous |
| `PoisonMultiplier` | Miscellaneous, Passives & Statuses |
| `PoisonThorns` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PoolMetronome` | Abilities & Spells, Miscellaneous |
| `PoopWhenHit` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `PopAndSpawn` | Abilities & Spells, Miscellaneous |
| `Possessed` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `PreEmptiveCounterNextAttacks` | Items & Equipment, Miscellaneous |
| `PreventDeathTransforms` | Abilities & Spells, Miscellaneous |
| `PreventSpecificInjury` | Items & Equipment, Miscellaneous |
| `PrioritizeAggroTarget` | Characters & Bosses, Miscellaneous |
| `PrioritizeFarAwayTargets` | Characters & Bosses, Miscellaneous |
| `PrioritizeHitDifferentTargets` | Characters & Bosses, Miscellaneous |
| `PrioritizePlayerCats` | Characters & Bosses, Miscellaneous |
| `PrioritizeWeakestEnemy` | Characters & Bosses, Miscellaneous |
| `ProbeCharmed` | Abilities & Spells, Events & Encounters, Miscellaneous |
| `ProtectTargetedAllies` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `PullSourceToKnockbackImmuneTarget` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `PullSourceToTarget` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `Purge` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `PurgeAll` | Abilities & Spells, Miscellaneous |
| `QuakeAreaChance` | Abilities & Spells, Miscellaneous |
| `QueueUseAbility` | Abilities & Spells, Miscellaneous |
| `Quivered` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RNGCannonRandomDamage` | Abilities & Spells, Miscellaneous |
| `RandomBonusDamage` | Abilities & Spells, Miscellaneous |
| `RandomDistanceDisplace` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `RandomInjury` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `RandomKnockback` | Abilities & Spells, Miscellaneous |
| `RandomKnockbackDirection` | Abilities & Spells, Miscellaneous |
| `RandomLightning` | Miscellaneous |
| `RandomMagicMissile` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RandomMutation` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RandomPassivePool` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `RandomPermanentStat` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RandomPermanentStatsDistinct` | Miscellaneous |
| `RandomSeededStatModifier` | Items & Equipment, Miscellaneous |
| `RandomStatDown` | Abilities & Spells, Cat Mutations, Miscellaneous |
| `RandomStatUp` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Miscellaneous, Passives & Statuses |
| `RandomStatusFromPool` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RandomTaggedMutation` | Abilities & Spells, Miscellaneous |
| `RandomWeatherEachFight` | Miscellaneous |
| `RandomizeAIWeightsEachTurn` | Characters & Bosses, Miscellaneous |
| `RangeUp` | Abilities & Spells, Cat Mutations, Miscellaneous, Passives & Statuses |
| `RangedTrueShot` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `RealTimePressure` | Items & Equipment, Miscellaneous |
| `RealTimePressure_OneUnit` | Miscellaneous, Passives & Statuses |
| `Reanimate` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `RebukeDamage` | Abilities & Spells, Miscellaneous |
| `ReceivedStatusReplacement` | Miscellaneous, Passives & Statuses |
| `ReclaimItemOnBreak` | Items & Equipment, Miscellaneous |
| `ReduceManaCost` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ReduceManaCostExcludeBrainstorm` | Abilities & Spells, Miscellaneous |
| `ReduceSpellCostsPerDisorder` | Items & Equipment, Miscellaneous |
| `ReduceSpellCostsPerParasite` | Items & Equipment, Miscellaneous |
| `Reflect` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `ReflectProjectiles` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous |
| `ReformMoonHead` | Abilities & Spells, Miscellaneous |
| `RefreshActPoints` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RefreshEquipmentAbilityOnElement` | Items & Equipment, Miscellaneous |
| `RefreshItemAbilities` | Abilities & Spells, Miscellaneous |
| `RefreshMoveOnWeaponConnect` | Miscellaneous, Passives & Statuses |
| `RefreshMovePoints` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `RefreshMovePointsIfHit` | Abilities & Spells, Miscellaneous |
| `RefreshNonManaItemAbilities` | Abilities & Spells, Miscellaneous |
| `RefreshOncePerFightAbilities` | Abilities & Spells, Miscellaneous |
| `RefreshWeaponAbility` | Abilities & Spells, Miscellaneous |
| `Regurge` | Abilities & Spells, Miscellaneous |
| `ReloadOnAllyCatDies` | Abilities & Spells, Miscellaneous |
| `ReloadOnAllyDies` | Abilities & Spells, Miscellaneous |
| `ReloadOnAnyDamage` | Abilities & Spells, Miscellaneous |
| `ReloadOnBackstab` | Abilities & Spells, Miscellaneous |
| `ReloadOnElementalDamageReceived` | Abilities & Spells, Miscellaneous |
| `ReloadOnGainCoins` | Abilities & Spells, Miscellaneous |
| `ReloadOnGainDivineShield` | Abilities & Spells, Miscellaneous |
| `ReloadOnKill` | Abilities & Spells, Miscellaneous |
| `ReloadOnKillEnemy` | Abilities & Spells, Miscellaneous |
| `ReloadOnKillTagged` | Abilities & Spells, Miscellaneous |
| `ReloadOnSpendMana` | Abilities & Spells, Miscellaneous |
| `ReloadOnTotalDamageReceived` | Abilities & Spells, Miscellaneous |
| `ReloadOnUseAbilityWithManaCost` | Abilities & Spells, Miscellaneous |
| `RemoteFlatLeech` | Characters & Bosses, Miscellaneous |
| `RemoteLeech` | Characters & Bosses, Miscellaneous |
| `RemoveActPoints` | Abilities & Spells, Miscellaneous |
| `RemoveAmbientLightEffects` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `RemoveExtraDispersedTurn` | Miscellaneous |
| `RemoveGlobalModifiers` | Characters & Bosses, Miscellaneous |
| `RemoveItem` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `RemoveKnockback` | Characters & Bosses, Miscellaneous |
| `RemoveLineOfSightRestrictions` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `RemoveMovePoints` | Abilities & Spells, Miscellaneous |
| `RemoveOncePerFightRestriction` | Miscellaneous, Passives & Statuses |
| `RemoveStatus` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `RemoveStatusStacks` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous |
| `RemoveTurnsThisRound` | Abilities & Spells, Miscellaneous |
| `RepairAll` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `RepairAllCondition` | Abilities & Spells, Miscellaneous |
| `RepairArmorCondition` | Abilities & Spells, Miscellaneous |
| `RepairOnKill` | Abilities & Spells, Miscellaneous |
| `RepairTrinket` | Items & Equipment, Miscellaneous |
| `RepairWeapon` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RepairWeaponCondition` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `ReplaceBasicAttack` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ReplaceBasicAttackWhenCastable` | Miscellaneous, Passives & Statuses |
| `ReplaceBasicAttackWhenDead` | Miscellaneous, Passives & Statuses |
| `ReplaceBasicAttack_Mutation` | Cat Mutations, Miscellaneous |
| `ReplaceBasicMove` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ReplaceBasicMove_Mutation` | Cat Mutations, Miscellaneous |
| `ReplaceBlankTilesOnBattleStart` | Items & Equipment, Miscellaneous |
| `ReplaceBrain` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `ReplaceSpawnedObjects` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ReplaceSpell` | Abilities & Spells, Miscellaneous |
| `ReplaceSpellsWhenDead` | Miscellaneous, Passives & Statuses |
| `RepressedMemoriesMetronome` | Miscellaneous, Passives & Statuses |
| `RerollEnemy` | Abilities & Spells, Miscellaneous |
| `RerollItemsOnBattleEnd` | Items & Equipment, Miscellaneous |
| `ResetArmorShield` | Abilities & Spells, Miscellaneous |
| `ReturnBoundItemOnBattleEnd` | Characters & Bosses, Miscellaneous |
| `ReturnDinoLegs` | Abilities & Spells, Miscellaneous |
| `RevengeDamage` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Revive` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ReviveNextRound` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `ReviveOnWin` | Miscellaneous, Passives & Statuses |
| `Robot` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `RobotsInheritArmor` | Miscellaneous, Passives & Statuses |
| `RockDetector` | Miscellaneous, Passives & Statuses |
| `RockyArmorPassive` | Items & Equipment, Miscellaneous |
| `RockyArmorSalvage` | Miscellaneous |
| `Rot` | Abilities & Spells, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `RunInXTurns` | Characters & Bosses, Miscellaneous |
| `RunWhenKittensDead` | Characters & Bosses, Miscellaneous |
| `RunWhenLastPlayerCatIsCharmed` | Characters & Bosses, Miscellaneous |
| `SafeDie` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `SafeDoomed` | Abilities & Spells, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `SafeExplosionIfHitSomething` | Miscellaneous, Passives & Statuses |
| `SafeExplosions` | Miscellaneous, Passives & Statuses |
| `Sandstorm` | Miscellaneous |
| `ScaldingOrbMoonBossOneShot` | Items & Equipment, Miscellaneous |
| `ScaledStatusAlliesOnSpendMana` | Items & Equipment, Miscellaneous |
| `ScaledStatusOnBleedDamage` | Miscellaneous, Passives & Statuses |
| `ScaledStatusOnHolyShieldBlock` | Items & Equipment, Miscellaneous |
| `ScaledStatusOnLoseShield` | Miscellaneous, Passives & Statuses |
| `ScaledStatusOnOverHealed` | Miscellaneous, Passives & Statuses |
| `ScaledStatusOnOverMana` | Miscellaneous, Passives & Statuses |
| `ScaledStatusOnSpendMana` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `ScalingAttackAnimation` | Characters & Bosses, Miscellaneous |
| `ScatterCoins` | Abilities & Spells, Cat Mutations, Miscellaneous |
| `ScatterHeldCoin` | Abilities & Spells, Miscellaneous |
| `ScatterRandomPickups` | Abilities & Spells, Miscellaneous |
| `SchizoIllusionAIModifier` | Abilities & Spells, Miscellaneous |
| `ScrambleEverything` | Abilities & Spells, Miscellaneous |
| `ScrambleLastUsedSpell` | Abilities & Spells, Miscellaneous |
| `Scrambled` | Abilities & Spells, Miscellaneous |
| `SecurityBotProtect` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `SelfDamageWhenDealDamage` | Miscellaneous, Passives & Statuses |
| `SelfStatusCarefulness` | Characters & Bosses, Miscellaneous |
| `SelfStun` | Abilities & Spells, Miscellaneous |
| `SendRock` | Abilities & Spells, Miscellaneous |
| `SerratedClaws` | Items & Equipment, Miscellaneous |
| `SetAnimationAlts` | Abilities & Spells, Miscellaneous |
| `SetBrittleImmune` | Items & Equipment, Miscellaneous |
| `SetCrazyEyeBackgroundWeights` | Abilities & Spells, Miscellaneous |
| `SetDefaultFace` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `SetDefaultFacePassive` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `SetDistanceDisplace` | Abilities & Spells, Miscellaneous |
| `SetFaction` | Items & Equipment, Miscellaneous |
| `SetFragileImmune` | Items & Equipment, Miscellaneous |
| `SetHealth` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous |
| `SetItemAux` | Items & Equipment, Miscellaneous |
| `SetKnockback` | Abilities & Spells, Miscellaneous |
| `SetShield` | Abilities & Spells, Miscellaneous |
| `SetSpellCosts` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ShadowCrit` | Abilities & Spells, Miscellaneous |
| `ShareHealthRegen` | Miscellaneous, Passives & Statuses |
| `SharePickups` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `SharePickupsWithSpawner` | Characters & Bosses, Miscellaneous |
| `SharkySmellsBlood` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `Shatter` | Abilities & Spells, Miscellaneous |
| `Shield` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `ShootHereCommand` | Abilities & Spells, Miscellaneous |
| `ShootHereReceiver` | Abilities & Spells, Miscellaneous |
| `ShortCircuit` | Abilities & Spells, Miscellaneous |
| `ShowFakeDamage` | Abilities & Spells, Miscellaneous |
| `ShowHiddenThings` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `ShowText` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `SignalFinalBossShieldBroke` | Abilities & Spells, Miscellaneous |
| `SizeScale` | Abilities & Spells, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `SizeScalePercent` | Miscellaneous, Passives & Statuses |
| `SkipFirstRounds` | Characters & Bosses, Miscellaneous |
| `Sleep` | Abilities & Spells, Events & Encounters, Miscellaneous, Passives & Statuses |
| `SlotMachineRollPool` | Characters & Bosses, Miscellaneous |
| `Slow` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SmallEnemiesIgnoreYou` | Miscellaneous, Passives & Statuses |
| `SmallHitExplosion` | Abilities & Spells, Miscellaneous |
| `SmallRockBehavior` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `SmartMetronome` | Abilities & Spells, Miscellaneous |
| `SmellBlood` | Abilities & Spells, Miscellaneous |
| `SmiteEnemiesWhoKill` | Miscellaneous, Passives & Statuses |
| `Snow` | Miscellaneous |
| `SolarFlare` | Miscellaneous |
| `SoulLink` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SoundEventOnHit` | Abilities & Spells, Miscellaneous |
| `SourceSwapsBackEndOfTurn` | Abilities & Spells, Miscellaneous |
| `SpawnBearTrap` | Abilities & Spells, Miscellaneous |
| `SpawnBearTrapIfHitKills` | Abilities & Spells, Miscellaneous |
| `SpawnBearTrapOnMiss` | Miscellaneous, Passives & Statuses |
| `SpawnCatCloneOnCorpsePopped` | Items & Equipment, Miscellaneous |
| `SpawnCatCopyOnBattleStart` | Miscellaneous, Passives & Statuses |
| `SpawnCatCopyWhenDowned` | Miscellaneous |
| `SpawnCoinAnywhere` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpawnCreep` | Abilities & Spells, Miscellaneous |
| `SpawnCreepOnHit` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `SpawnCreepOnHitKnockback` | Characters & Bosses, Miscellaneous |
| `SpawnCustomTrap` | Abilities & Spells, Miscellaneous |
| `SpawnEachTurn` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpawnExtraThingsOnBattleStart` | Cat Mutations, Items & Equipment, Miscellaneous |
| `SpawnFlames` | Abilities & Spells, Miscellaneous |
| `SpawnItemLinkedFamiliar` | Items & Equipment, Miscellaneous |
| `SpawnMeatOnMove` | Miscellaneous, Passives & Statuses |
| `SpawnNearEnemies` | Items & Equipment, Miscellaneous |
| `SpawnNeutralWebTrapOnMiss` | Abilities & Spells, Miscellaneous |
| `SpawnObjectOnPopCorpse` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpawnOnBattleStart` | Cat Classes, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpawnOnBattleStartRandomEmptyTile` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpawnOnDeath` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `SpawnOnDowned` | Cat Mutations, Items & Equipment, Miscellaneous |
| `SpawnRandomPickupsOnTaggedUnitKilled` | Items & Equipment, Miscellaneous |
| `SpawnRock` | Abilities & Spells, Miscellaneous |
| `SpawnScaledRotFly` | Miscellaneous, Passives & Statuses |
| `SpawnThingIfHitKills` | Abilities & Spells, Miscellaneous |
| `SpawnThingOnDamage` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpawnThingOnDeath` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpawnTilePuddleOnBattleStart` | Miscellaneous |
| `SpawnVolcanoOnBattleStart` | Miscellaneous |
| `SpawnWebTrap` | Abilities & Spells, Miscellaneous |
| `SpawnerCatDataReference` | Characters & Bosses, Miscellaneous |
| `SpecialBossMultipartInstakill` | Abilities & Spells, Miscellaneous |
| `SpecialGodRays` | Miscellaneous |
| `SpecificInjury` | Abilities & Spells, Miscellaneous |
| `SpeculativeMoveSelfCorpseOffMap` | Abilities & Spells, Miscellaneous |
| `SpeedUp` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpeedUp_WithoutInitiative` | Characters & Bosses, Miscellaneous |
| `SpellDamageUp` | Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `SpellShield` | Abilities & Spells, Miscellaneous |
| `SpewerAltGraphics` | Characters & Bosses, Miscellaneous |
| `SpiderInfested` | Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous |
| `SpitConsumed` | Abilities & Spells, Miscellaneous |
| `SplashDamage` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `SplittableMove` | Miscellaneous, Passives & Statuses |
| `SpreadDisease` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `SpreadExtraDebuffs` | Miscellaneous, Passives & Statuses |
| `SpreadPainBonus` | Miscellaneous, Passives & Statuses |
| `SpreadPainBonusCrit` | Miscellaneous, Passives & Statuses |
| `SpreadWater` | Characters & Bosses, Miscellaneous |
| `SproutsGrantMovement` | Characters & Bosses, Miscellaneous |
| `StackingDodgeChanceOnTookDamage` | Miscellaneous, Passives & Statuses |
| `StackingFlowerTrail` | Items & Equipment, Miscellaneous |
| `StackingSandstorm` | Abilities & Spells, Miscellaneous |
| `StanceSwitchToMelee` | Abilities & Spells, Miscellaneous |
| `StanceSwitchToRanged` | Abilities & Spells, Miscellaneous |
| `StartDead` | Characters & Bosses, Miscellaneous |
| `StartOffMap` | Characters & Bosses, Miscellaneous |
| `StatBounty` | Abilities & Spells, Miscellaneous |
| `StatDependentPassive` | Items & Equipment, Miscellaneous |
| `StatMinimum` | Miscellaneous, Passives & Statuses |
| `StatsAtLowHealth` | Miscellaneous, Passives & Statuses |
| `StatusAdjacentOnTheirTurnBegin` | Miscellaneous, Passives & Statuses |
| `StatusAdjacentOnTheirTurnEnd` | Items & Equipment, Miscellaneous |
| `StatusAfterCastSpell` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusAfterXStacks` | Items & Equipment, Miscellaneous |
| `StatusAfterXTurns` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `StatusAllCharactersOnSpawn` | Items & Equipment, Miscellaneous |
| `StatusAlliesEachTurn` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusAlliesOnBattleStart` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusAlliesOnDeath` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusAlliesOnGainCoins` | Miscellaneous, Passives & Statuses |
| `StatusAlliesOnKill` | Miscellaneous, Passives & Statuses |
| `StatusAlliesOnSpendMana` | Miscellaneous, Passives & Statuses |
| `StatusAlliesScaledByCursedOnDeath` | Miscellaneous, Passives & Statuses |
| `StatusAllyWhenAllySpendsMana` | Miscellaneous, Passives & Statuses |
| `StatusAnyCatAllyWhoKills` | Miscellaneous, Passives & Statuses |
| `StatusCarefulness` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `StatusCharactersOnRoundEnd` | Miscellaneous |
| `StatusCharactersOnRoundStart` | Miscellaneous |
| `StatusCollector` | Characters & Bosses, Miscellaneous |
| `StatusDamagers` | Miscellaneous, Passives & Statuses |
| `StatusEachRoundBegin` | Miscellaneous |
| `StatusEachRoundEnd` | Cat Mutations, Items & Equipment, Miscellaneous |
| `StatusEachTurnBegin` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusEachTurnBeginIfHasStatus` | Characters & Bosses, Miscellaneous |
| `StatusEachTurnEnd` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusEachTurnEndForEachTurn` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusEachTurnEndIfEnabledAtStartOfTurn` | Characters & Bosses, Miscellaneous |
| `StatusEachTurnEndPerEnemyKill` | Miscellaneous, Passives & Statuses |
| `StatusEnemiesOnDeath` | Miscellaneous, Passives & Statuses |
| `StatusEveryXSpellCasts` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusEveryXSpellCastsEachTurn` | Cat Mutations, Miscellaneous |
| `StatusEveryXTurnBegins` | Miscellaneous, Passives & Statuses |
| `StatusGroup` | Abilities & Spells, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `StatusIfBattleAlreadyBegan` | Miscellaneous, Passives & Statuses |
| `StatusIfDidntMove` | Cat Mutations, Miscellaneous |
| `StatusIfUnusedActPoints` | Items & Equipment, Miscellaneous |
| `StatusIfUnusedMovePoints` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusImmunity` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusKilledCharacters` | Cat Mutations, Miscellaneous, Passives & Statuses |
| `StatusKillers` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `StatusOnAllyCatDeath` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnAnyDeath` | Miscellaneous, Passives & Statuses |
| `StatusOnBackstab` | Items & Equipment, Miscellaneous |
| `StatusOnBattleEnd` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnBattleEndIfKillThresholdMet` | Miscellaneous, Passives & Statuses |
| `StatusOnBattleStart` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnBreak` | Items & Equipment, Miscellaneous |
| `StatusOnBreakItem` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnCastSpell` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnCollectPickup` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnCrit` | Miscellaneous, Passives & Statuses |
| `StatusOnDealtDamage` | Miscellaneous, Passives & Statuses |
| `StatusOnDealtDamageThreshold` | Miscellaneous, Passives & Statuses |
| `StatusOnDie` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous |
| `StatusOnDodge` | Items & Equipment, Miscellaneous |
| `StatusOnEatFood` | Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnEatPill` | Miscellaneous, Passives & Statuses |
| `StatusOnEndMove` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnEnemyCastSpell` | Miscellaneous |
| `StatusOnEnemyConfused` | Characters & Bosses, Miscellaneous |
| `StatusOnEnemyDeath` | Items & Equipment, Miscellaneous |
| `StatusOnFallAsleep` | Items & Equipment, Miscellaneous |
| `StatusOnFullMana` | Items & Equipment, Miscellaneous |
| `StatusOnGainCoins` | Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnGainShield` | Miscellaneous, Passives & Statuses |
| `StatusOnHeal` | Miscellaneous, Passives & Statuses |
| `StatusOnHealed` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnKill` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnKillEnemy` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnLoseShield` | Miscellaneous, Passives & Statuses |
| `StatusOnOverHealed` | Miscellaneous, Passives & Statuses |
| `StatusOnOverMana` | Miscellaneous, Passives & Statuses |
| `StatusOnPickupCoins` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnPopCorpse` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnSetPieceBreak` | Miscellaneous |
| `StatusOnSpawnIn` | Characters & Bosses, Miscellaneous |
| `StatusOnStanceSwitch` | Miscellaneous, Passives & Statuses |
| `StatusOnTakeHealthDamage` | Miscellaneous, Passives & Statuses |
| `StatusOnTakeHealthOrShieldDamage` | Items & Equipment, Miscellaneous |
| `StatusOnTookDamage` | Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnTookDamageFromAbility` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `StatusOnTookDamageFromEnemyAbility` | Miscellaneous, Passives & Statuses |
| `StatusOnTriggerTrap` | Miscellaneous, Passives & Statuses |
| `StatusOnTurnEndIfCastNSpells` | Miscellaneous, Passives & Statuses |
| `StatusOnTurnEndIfDidntCastAbilityTypes` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnTurnEndIfManaExact` | Miscellaneous, Passives & Statuses |
| `StatusOnUseAbilityWithTag` | Miscellaneous, Passives & Statuses |
| `StatusOnUseBasicAttack` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusOnUseElementAbility` | Miscellaneous, Passives & Statuses |
| `StatusOverlappingCharactersAndDie` | Characters & Bosses, Miscellaneous |
| `StatusPerInjury` | Miscellaneous, Passives & Statuses |
| `StatusRandomEnemiesOnBattleStart` | Events & Encounters, Items & Equipment, Miscellaneous |
| `StatusReplacement` | Miscellaneous, Passives & Statuses |
| `StatusThingsKnockedBack` | Miscellaneous, Passives & Statuses |
| `StatusWhenAllySpendsMana` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `StatusWhenStatusCompletelyRemoved` | Characters & Bosses, Miscellaneous |
| `StealDemonicGlyph` | Abilities & Spells, Miscellaneous |
| `StealEquipment` | Abilities & Spells, Miscellaneous |
| `StealTurn` | Abilities & Spells, Miscellaneous |
| `Stealth` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StealthCritChance` | Abilities & Spells, Miscellaneous |
| `StealthUntilBasicAttack` | Items & Equipment, Miscellaneous |
| `StevenBolts` | Items & Equipment, Miscellaneous |
| `StrengthForEachNeighboringEnemy` | Miscellaneous, Passives & Statuses |
| `StrengthInNumbersAura` | Miscellaneous, Passives & Statuses |
| `StrengthUp` | Abilities & Spells, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StrictLimitDamage` | Miscellaneous, Passives & Statuses |
| `StripKnockback` | Items & Equipment, Miscellaneous |
| `StripStatuses` | Characters & Bosses, Miscellaneous |
| `Stun` | Abilities & Spells, Cat Mutations, Characters & Bosses, Events & Encounters, Items & Equipment, Miscellaneous, Passives & Statuses |
| `StunImmunity` | Characters & Bosses, Miscellaneous |
| `SupportDieInsteadOfRun` | Characters & Bosses, Miscellaneous |
| `SupportFormChangeInsteadOfRun` | Characters & Bosses, Miscellaneous |
| `SurviveAt1HP` | Characters & Bosses, Miscellaneous |
| `SwallowSmallCharacter` | Abilities & Spells, Miscellaneous |
| `SwapHighestAndLowestStat` | Abilities & Spells, Cat Mutations, Miscellaneous |
| `SwapWeapon` | Abilities & Spells, Miscellaneous |
| `SwimmingFormChange` | Characters & Bosses, Miscellaneous |
| `SwitchMusic` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `Switcheroo` | Abilities & Spells, Miscellaneous |
| `SyncFormsWithBuddy` | Characters & Bosses, Miscellaneous |
| `T2CopyCat` | Abilities & Spells, Miscellaneous |
| `T3HitlerSpawningPhase` | Characters & Bosses, Miscellaneous |
| `T3HitlerTriggerInitialSpawns` | Abilities & Spells, Miscellaneous |
| `TVBotDisableAttack` | Characters & Bosses, Miscellaneous |
| `TVBotDisableMove` | Characters & Bosses, Miscellaneous |
| `TVBotDisableSpells` | Characters & Bosses, Miscellaneous |
| `TVBotScreen` | Characters & Bosses, Miscellaneous |
| `TagGreed` | Characters & Bosses, Miscellaneous |
| `TagMetronome` | Abilities & Spells, Miscellaneous |
| `TaggedPickupEffectReplacement` | Miscellaneous, Passives & Statuses |
| `TakeBonusTurnWithAIControl` | Abilities & Spells, Miscellaneous |
| `TakeBonusTurnWithStatus` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TakeExtraDamage` | Miscellaneous, Passives & Statuses |
| `TakeExtraTurn` | Abilities & Spells, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `TakeExtraTurnEndOfRound` | Abilities & Spells, Miscellaneous |
| `TakeWeaponFromSpawner` | Characters & Bosses, Miscellaneous |
| `Tall` | Characters & Bosses, Miscellaneous |
| `TallTumorManaBurn` | Characters & Bosses, Miscellaneous |
| `Tangled` | Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous |
| `TargetedMetronome` | Abilities & Spells, Miscellaneous |
| `Tarred` | Abilities & Spells, Events & Encounters, Miscellaneous, Passives & Statuses |
| `TauntAlways` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `TauntAtFullHealth` | Miscellaneous, Passives & Statuses |
| `Taunting` | Abilities & Spells, Miscellaneous |
| `TeamBonusAbility` | Abilities & Spells, Miscellaneous |
| `TeamCastAbility` | Abilities & Spells, Miscellaneous |
| `Tech` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TeleportBackAtTurnEnd` | Abilities & Spells, Miscellaneous |
| `TempBackstab` | Abilities & Spells, Miscellaneous |
| `TempBackstabBleed` | Abilities & Spells, Miscellaneous |
| `TempBackstabPiercing` | Abilities & Spells, Miscellaneous |
| `TempBackstabPoison` | Abilities & Spells, Miscellaneous |
| `TempBasicAttackBonusAOE` | Abilities & Spells, Miscellaneous |
| `TempBonusKnockback` | Abilities & Spells, Miscellaneous |
| `TempBonusKnockbackDamage` | Abilities & Spells, Miscellaneous |
| `TempCounterAttack` | Abilities & Spells, Miscellaneous |
| `TempCritChanceUp` | Abilities & Spells, Miscellaneous |
| `TempDamageUp` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TempDexterityUp` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TempInitiativeChange` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TempInjuryImmunity` | Abilities & Spells, Miscellaneous |
| `TempLuckUp` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TempManaCostReduction` | Abilities & Spells, Miscellaneous |
| `TempMeleeRangeUp` | Items & Equipment, Miscellaneous |
| `TempMovement` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TempNoManaRegen` | Abilities & Spells, Miscellaneous |
| `TempPassiveUntilSettled` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `TempPassiveWhileHasStatus` | Abilities & Spells, Miscellaneous |
| `TempPenetrate` | Abilities & Spells, Miscellaneous |
| `TempPreEmptiveCounterAttack` | Abilities & Spells, Miscellaneous |
| `TempRangeUp` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `TempSpeedUp` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TempSpellDamageUp` | Abilities & Spells, Miscellaneous, Passives & Statuses |
| `TempStrengthUp` | Abilities & Spells, Events & Encounters, Miscellaneous, Passives & Statuses |
| `TempTrampleUntilSettled` | Abilities & Spells, Miscellaneous |
| `Temporary` | Abilities & Spells, Items & Equipment, Miscellaneous, Passives & Statuses |
| `Terminator2Chase` | Characters & Bosses, Miscellaneous |
| `Terminator2Run` | Characters & Bosses, Miscellaneous |
| `TerminatorChase` | Characters & Bosses, Miscellaneous |
| `TerminatorSkin` | Characters & Bosses, Miscellaneous |
| `ThornsDamageImmuneUntilSettled` | Abilities & Spells, Miscellaneous |
| `TickDownStatus` | Abilities & Spells, Miscellaneous |
| `TileDamageImmuneUntilSettled` | Abilities & Spells, Miscellaneous |
| `TileDamageMultiplier` | Miscellaneous, Passives & Statuses |
| `TileElementDamageImmunity` | Characters & Bosses, Miscellaneous |
| `TileTrail` | Abilities & Spells, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `TileTrail_Ahead` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `TilesMovedToCritChance` | Abilities & Spells, Miscellaneous |
| `TilesMovedToMana` | Abilities & Spells, Miscellaneous |
| `TilesMovedToNeighborHeal` | Abilities & Spells, Miscellaneous |
| `TilesMovedToStrength` | Abilities & Spells, Miscellaneous |
| `TimeDelayStatusApplication` | Abilities & Spells, Miscellaneous |
| `TinkererBasicAttackSwitching` | Cat Classes, Characters & Bosses, Miscellaneous |
| `TintItem` | Items & Equipment, Miscellaneous |
| `TireBehavior` | Characters & Bosses, Miscellaneous |
| `TogglableRoundEndExtraTurn` | Miscellaneous, Passives & Statuses |
| `TormentorHeal` | Characters & Bosses, Miscellaneous |
| `TossTargetIsAggroTarget` | Abilities & Spells, Miscellaneous |
| `TossTargetIsBuddy` | Abilities & Spells, Miscellaneous |
| `TossTargetIsNotInWater` | Abilities & Spells, Miscellaneous |
| `TourettesMeows` | Miscellaneous, Passives & Statuses |
| `TowerDefenseReflex` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `TowerDefenseStatus` | Abilities & Spells, Miscellaneous |
| `TowerDefenseStatus2` | Abilities & Spells, Miscellaneous |
| `TrackAmountKilledByPlayer` | Characters & Bosses, Miscellaneous |
| `TradeLife` | Abilities & Spells, Miscellaneous |
| `TrailBlazer` | Abilities & Spells, Miscellaneous |
| `Trample` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `TransformAbility` | Abilities & Spells, Miscellaneous |
| `TransformBasicAttack` | Abilities & Spells, Miscellaneous |
| `TransformBasicMove` | Abilities & Spells, Miscellaneous |
| `TransformEquipment` | Abilities & Spells, Miscellaneous |
| `TransformInXTurns` | Characters & Bosses, Miscellaneous |
| `TransformItemOnElementInfluence` | Items & Equipment, Miscellaneous |
| `TransformNow` | Abilities & Spells, Miscellaneous |
| `TransformOnDeath` | Characters & Bosses, Miscellaneous |
| `TransformOnDeathImmediately` | Characters & Bosses, Miscellaneous |
| `TransformOnElementInfluence` | Characters & Bosses, Miscellaneous |
| `TransformOnElementInfluencex` | Characters & Bosses, Miscellaneous |
| `TransformOnStatusThreshold` | Characters & Bosses, Miscellaneous |
| `TransformWeapon` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `TransformWhenBuddyDies` | Characters & Bosses, Miscellaneous |
| `TrapEffectsMultiplier` | Miscellaneous, Passives & Statuses |
| `Trapper` | Characters & Bosses, Miscellaneous |
| `Trapper_Status` | Abilities & Spells, Miscellaneous |
| `TriggerBleedOnBleed` | Miscellaneous |
| `TriggerDOTStatuses` | Abilities & Spells, Miscellaneous |
| `TriggerGameEnding` | Abilities & Spells, Miscellaneous |
| `TriggerMotherConsume` | Abilities & Spells, Miscellaneous |
| `TriggerMotherGrow` | Abilities & Spells, Miscellaneous |
| `TriggerWerewolfTransform` | Abilities & Spells, Miscellaneous |
| `TrinketActiveEffectsMultiplierBonus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `TrinketPassiveMultiplierBonus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `TrueShot` | Items & Equipment, Miscellaneous |
| `TunnelVision` | Items & Equipment, Miscellaneous |
| `TurnAround` | Abilities & Spells, Miscellaneous |
| `TurnControlDelay` | Abilities & Spells, Miscellaneous |
| `TurnRight` | Abilities & Spells, Miscellaneous |
| `TutorialBossRiggedFight` | Characters & Bosses, Miscellaneous |
| `TwisterDisplaceWithDamage` | Abilities & Spells, Miscellaneous |
| `TwisterFling` | Characters & Bosses, Miscellaneous |
| `UncappedHP` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `UncappedHPBonusStr` | Miscellaneous, Passives & Statuses |
| `UncappedMana` | Miscellaneous, Passives & Statuses |
| `Uncontrollable` | Items & Equipment, Miscellaneous |
| `Undead` | Characters & Bosses, Items & Equipment, Miscellaneous |
| `UndoDamage` | Abilities & Spells, Miscellaneous |
| `UnlimitedDeathRattleRevive` | Characters & Bosses, Miscellaneous |
| `UnlockOrientation` | Characters & Bosses, Miscellaneous |
| `UpTireBehavior` | Characters & Bosses, Miscellaneous |
| `UpgradeLevelUpClassActives` | Miscellaneous, Passives & Statuses |
| `UpgradeLevelUpClassPassives` | Miscellaneous, Passives & Statuses |
| `UpgradeRandomAbility` | Abilities & Spells, Miscellaneous |
| `UpgradeSpawnedPickups` | Miscellaneous, Passives & Statuses |
| `UpgradeTaggedSpawnsToChampions` | Miscellaneous |
| `UseAbility` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous |
| `UseAbilityWhenOutOfStatus` | Characters & Bosses, Miscellaneous |
| `UseAbilityWhenShieldDepleted` | Characters & Bosses, Miscellaneous |
| `UseAbility_Madness` | Miscellaneous, Passives & Statuses |
| `UseAbility_NonStack` | Characters & Bosses, Miscellaneous |
| `UseMoveAbilityWithAI` | Abilities & Spells, Miscellaneous |
| `UseRandomSpell_Madness` | Miscellaneous, Passives & Statuses |
| `Vaporize` | Abilities & Spells, Characters & Bosses, Miscellaneous |
| `VaporizeCorpse` | Abilities & Spells, Miscellaneous |
| `VaporizeCorpseFlipAdvantage` | Abilities & Spells, Miscellaneous |
| `VaporizeDice` | Abilities & Spells, Miscellaneous |
| `VaporizeInanimate` | Abilities & Spells, Cat Mutations, Miscellaneous |
| `VaporizeTarget` | Abilities & Spells, Miscellaneous |
| `VisualCountDownThenApplyStatus` | Abilities & Spells, Miscellaneous |
| `VisualFX` | Abilities & Spells, Items & Equipment, Miscellaneous |
| `VisualFXTile` | Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous, Passives & Statuses |
| `VisualFlySwarm` | Miscellaneous |
| `WaggleClone` | Abilities & Spells, Miscellaneous |
| `Wall` | Characters & Bosses, Miscellaneous |
| `WaterWalk` | Cat Mutations, Characters & Bosses, Miscellaneous, Passives & Statuses |
| `Weakness` | Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous, Passives & Statuses |
| `WeaponActiveEffectsMultiplierBonus` | Miscellaneous, Passives & Statuses |
| `WeaponAuxMultiplier` | Abilities & Spells, Miscellaneous |
| `WeaponCountsAsBasicAttack` | Miscellaneous, Passives & Statuses |
| `WeaponDamageMultiplierBonus` | Items & Equipment, Miscellaneous, Passives & Statuses |
| `WeaponPassiveMultiplierBonus` | Miscellaneous, Passives & Statuses |
| `WeaponsDontLoseDurability` | Characters & Bosses, Miscellaneous, Passives & Statuses |
| `Webbed` | Abilities & Spells, Cat Mutations, Events & Encounters, Miscellaneous |
| `WeremanTransformationReceiver` | Characters & Bosses, Miscellaneous |
| `Wet` | Items & Equipment, Miscellaneous |
| `WhitelistPickupType` | Characters & Bosses, Miscellaneous |
| `WideBackstab` | Characters & Bosses, Miscellaneous |
| `Windy` | Miscellaneous |
| `WispDodge` | Characters & Bosses, Miscellaneous |
| `XIsConsumedCharacterMaxHP` | Abilities & Spells, Miscellaneous |
| `XIsCountDeaths` | Abilities & Spells, Miscellaneous |
| `XIsCountStatusStacks` | Abilities & Spells, Miscellaneous |
| `XIsFreeArmorSlots` | Abilities & Spells, Miscellaneous |
| `XIsIncreaseEachTurn` | Abilities & Spells, Miscellaneous |
| `XIsLivingAlliesWithTag` | Abilities & Spells, Miscellaneous |
| `XIsLivingCharactersWithTag` | Abilities & Spells, Miscellaneous |
| `XIsMultipliedPercentHealth` | Abilities & Spells, Miscellaneous |
| `XIsOtherHealsThisTurn` | Abilities & Spells, Miscellaneous |
| `XIsRampAndReset` | Abilities & Spells, Miscellaneous |
| `XIsRecycleCostReduction` | Abilities & Spells, Miscellaneous |
| `XIsSpellStormRampAndReset` | Abilities & Spells, Miscellaneous |
| `XIsTargetHealth` | Abilities & Spells, Miscellaneous |
| `XIsTimesDamageTaken` | Abilities & Spells, Miscellaneous |
| `YOffset` | Abilities & Spells, Cat Mutations, Characters & Bosses, Miscellaneous |
| `ZeroKnockbackDamage` | Characters & Bosses, Miscellaneous |
| `Zombie` | Miscellaneous |

## 2. Completely Missing (228)

These identifiers were not found in `passive_pool` OR anywhere as a property key in the entire Master Schema. They may be totally undocumented, deprecated, or solely referenced by the engine in a way the schema generator cannot currently extract.

| :--- |
| Missing Identifier |
| `AbilityCritChance` |
| `AbilityDodgeChance` |
| `AbilityOnEnemyCastSpell` |
| `AddBackstabBonus` |
| `AddCharisma` |
| `AddDamageToAllDamage` |
| `AddDamageToElementAbilities` |
| `AddDexterity` |
| `AddElementOnConnect` |
| `AddFlatBackstabBonus` |
| `AddIntScalingToBasicAttack` |
| `AddIntelligence` |
| `AddLuck` |
| `AddMaxMana` |
| `AddMeleeDamage` |
| `AddPassivesToAllCharacters` |
| `AddRangedDamage` |
| `AddStatusToMagicSpells` |
| `AddStatusToReceivedAbilityDamage` |
| `AddStrength` |
| `AggroTargetIsLastAttackedBy` |
| `AllDamageImmune` |
| `AllyDamageResist` |
| `AmplifyReceivedNegativeStatus` |
| `AmplifyReceivedPositiveStatus` |
| `ApplyStatuses` |
| `ApplyStatusesNextTurnEnd` |
| `ArmorBreakOnDeath` |
| `ArmorDamageReduction` |
| `AsteroidKnockbackBounce` |
| `AuraBase` |
| `BackstabSide` |
| `BackstabsBleed` |
| `BackstabsPierce` |
| `BackstabsPoison` |
| `BasicAttackChanceForMultiEffect` |
| `BasicAttackMultiplicity` |
| `BetterBurn` |
| `BloatEyePassive` |
| `Blur` |
| `BoneArmorDoesntBreak` |
| `BonusDamageToPermanentStr` |
| `BounceCoin` |
| `BounceHotRock` |
| `BrainFactionOverride` |
| `BrittleAllStatsUp` |
| `BrittleStatusBase` |
| `BumblefootButtFart` |
| `CantDodgeBackstabs` |
| `CapturedFamiliarIcon` |
| `ChanceGroup` |
| `ChanceToBlockProjectiles` |
| `CoinGreed` |
| `CoinSteal` |
| `CombatTutorialDriverEventListener` |
| `ConditionalPassive` |
| `Conditional_Big` |
| `Conditional_BuffRoll` |
| `Conditional_Cat` |
| `Conditional_Frontstab` |
| `Conditional_HasSetBonus` |
| `Conditional_IsPhysical` |
| `Conditional_ManaMatters` |
| `Conditional_NotEnemy` |
| `Consuming` |
| `CopiedSpells` |
| `CopyCatPassive` |
| `CorpseCounter` |
| `CustomRunAwayCondition` |
| `DamageAmpAura` |
| `DamageIfDidntAct` |
| `DamageReduction` |
| `DamageReflection` |
| `DeadAltAbility_Internal` |
| `DebugBrainTakeover` |
| `DebugWTF` |
| `DelayedStatusApplication` |
| `DelayedTrigger` |
| `DemonicGlyph` |
| `DestroyFaceArmor` |
| `DestroyHeadArmor` |
| `DexDownAura` |
| `DirectKnockbackCausesBleed` |
| `Dodge` |
| `DodgeAttacksEachTurn` |
| `DoubleCastSpellPassive` |
| `DropAsFamiliarBase` |
| `DybbukManualExitTag` |
| `Enrage` |
| `Exhaustion` |
| `ExpireOnRoundEnd` |
| `ExtraTurnAILimiter` |
| `FactionDisguise` |
| `FatsoBackstabReaction` |
| `FinalBossHitCountdown` |
| `FlatBackstabDamage` |
| `FlowersOnBeginTurn` |
| `ForceCollectsPickupsWithAltEffects` |
| `FormChangerMatchMonkStances` |
| `GasCloudBehavior` |
| `GlobalAuraBase` |
| `GlobalBrutalManaDrainAura` |
| `GlobalManaRegenAura` |
| `GlobalParticle` |
| `GrassOnEndTurn` |
| `HalfBasicAttackDamage` |
| `HealAtEnd` |
| `HeavierHits` |
| `HitEffect` |
| `IgnoreBuffs` |
| `ImbueAttackPassive` |
| `ImbueAttackStatus` |
| `ImbueBleed` |
| `ImbueKnockOutCoin` |
| `ImbueManaLeech` |
| `ImbuePoison` |
| `ImbueRandomStatDown` |
| `ImbueWeakness` |
| `InfiniteSliding` |
| `InstantMaxManaUp` |
| `JumpKnockback` |
| `KillsToManaThisTurn` |
| `KillsToMeatAndHealthThisTurn` |
| `KnockOutPickups` |
| `KnockUpTowardsAndCollide` |
| `KnockbackDamageImmune` |
| `LoseShieldNextTurn` |
| `ManaLeech` |
| `ManaRegenMultiplierIfNoCastSpells` |
| `MathRefund` |
| `MeleeRangeUp` |
| `MoveAutomatically` |
| `MultiplyKnockbackDamage` |
| `MultiplyKnockbackDistance` |
| `NextAbilityIncreaseRange` |
| `NextDamageCrits` |
| `NextDamageReduceAndPushback` |
| `NextDamageReduceThisTurn` |
| `NextMoveRangeIncrease` |
| `NextMoveTramples` |
| `NextSpellHealEqualToMana` |
| `Night` |
| `NoStartingMana` |
| `OldStealth` |
| `ParticleBurst` |
| `PassiveAtManaThreshold` |
| `PassiveAtZeroMovement` |
| `PassiveBrace` |
| `PassiveIfAllArmorFull` |
| `PassiveIfEmptyTrinket` |
| `PassiveIfEmptyWeapon` |
| `PassiveIfFirstWithStackKey` |
| `PassiveIfHasFace` |
| `PassiveIfHasHead` |
| `PassiveIfHasNeck` |
| `PassiveIfHasTrinket` |
| `PassiveIfHasWeapon` |
| `PassiveWhileCharmed` |
| `PassiveWhilePreviewingMonkMeleeStance` |
| `PetrifyCharmed` |
| `Phylactery` |
| `Pickup` |
| `PlayerCatBonusAbilityAura` |
| `PoopOnTurnEnd` |
| `PositionalWeakPoint_Base` |
| `PositionalWeakPoint_CriticalHits` |
| `RandomMutationOnBattleStart` |
| `RandomNegativeStatus` |
| `Reduce` |
| `RefreshTurns` |
| `ReloadAssociatedAbility` |
| `ReloadOnKillUnitWithStatus` |
| `RemoveStatusByStackKey` |
| `RepairTrinketCondition` |
| `ReplaceBasicMoveWhenDead` |
| `ReplaceNextBasicMove` |
| `RockSeekEnemies` |
| `RunWhenCatsTrappedOnceEach` |
| `RunWhenHasCoins` |
| `RunWhenMaxPhylacteryHeal` |
| `RunWhenOutOfMana` |
| `RunWhenWonFight` |
| `SelfManaGain` |
| `SetAuxCounter` |
| `SetProgressionFlag` |
| `SkipNextTurn` |
| `SoftKnockbackImmune` |
| `SpawnCoin` |
| `SpawnCreepInFront` |
| `SpawnDamageTrap` |
| `SpawnNeutralWebTrap` |
| `SpawnOnceWhenSettled` |
| `SpawnSnareTrap` |
| `SpdDownAura` |
| `SpecialFriendsLockAbility` |
| `StanceSwitchToMeleeOnConnect` |
| `StanceSwitchToRangedOnConnect` |
| `StationaryRegen` |
| `StatusEveryXTurnEnds` |
| `StatusFamiliarsOnKill` |
| `StatusIfDidntAct` |
| `StatusOnDealtDamageWithAbility` |
| `StatusOnTookDamageWhileNotDoingAbility` |
| `StatusOnTurnEndIfDidntCastSpells` |
| `StatusOnUseAbilityWithManaCost` |
| `StatusTombstone` |
| `StealthBuffs` |
| `StrDownAura` |
| `SwapBackAtTurnEnd` |
| `SwitchBrainFaction` |
| `T2CopyCatInternal` |
| `TargetEnemyOnEndTurn` |
| `Taunted` |
| `TempCharmed` |
| `TempMadness` |
| `TilesMovedToHealth` |
| `TransformAfterXTurns` |
| `TransformedAbility` |
| `TriggerProgressionUnlock` |
| `TurnLeft` |
| `TutorialRigCantLose` |
| `TutorialRigFirstRandomStat` |
| `TwoThirdsBasicAttackDamage` |
| `UniqueAdventureTokenPassiveSwitch` |
| `UpdateConditionalPassivesNow` |
| `UseRandomSpell` |
| `VeinyBonus` |
| `XIsArmorSetCount` |