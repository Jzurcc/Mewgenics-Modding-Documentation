---
title: "Hidden Passives Schema"
description: "Passives that exist but are hidden from the UI."
---

# Hidden Passives Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

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

### Object: `View All Hidden Identifiers`


<details>
<summary><b>Expand</b></summary>

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