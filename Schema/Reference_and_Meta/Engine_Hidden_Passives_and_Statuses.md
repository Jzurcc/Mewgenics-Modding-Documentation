---
title: "Hidden Passives Schema"
description: "Passives that exist but are hidden from the UI."
---

# Hidden Passives Schema

## Overview
> [!NOTE]
> This schema tracks passive effects that the engine applies secretly behind the scenes without telling the player (e.g. base stat hooks).

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
HiddenStats {
    hidden true
    stats { bonus_hp 1 }
}
```

---

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

> This document lists passives and statuses that are proven to exist or work in the engine but are completely absent from the `.gon` schema extraction. They may be hardcoded, deprecated, or exist only as internal engine state strings.

## Part 1: Completely Hidden (228)

These identifiers are proven to exist or work in the engine but are completely absent from `.gon` schema extraction. They may be hardcoded in the engine binary, deprecated, or exist only as internal state strings.

<details>
<summary><b>View All Hidden Identifiers</b></summary>

| :--- |
| Identifier |
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

</details>