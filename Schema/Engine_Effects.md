# Mewgenics Mod Developer Documentation: Engine: Effects & Conditionals

> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Engine: Effects & Conditionals

This document is the authoritative reference for the `effects {}` engine schema. All of the contexts below can appear as keys inside an `effects {}` block. Many of these are conditional wrappers that evaluate a condition before executing their nested effect block.

> **Note:** Because many of these contexts accept arbitrary nested effects, any entry marked `[effect_block]` recursively refers back to this same document.

### All Confirmed `[effect_block]` Values

<details>
<summary><b>Expand</b></summary>

| ID | Type | Notes |
| :--- | :--- | :--- |
| `AIFavorLowHealth` | Number | Applies or references the 'AIFavorLowHealth' effect/state. |
| `AcidRain` | Number |  |
| `AddExtraTurnsBeforeRun` | Number |  |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. |
| `AddPostProcessEffect` | Block |  |
| `AddSpiritBombCharges` | Number | Applies or references the 'AddSpiritBombCharges' effect/state. |
| `AddTilesetObjects` | Block |  |
| `AddWeaponAux` | Equation | Applies or references the 'AddWeaponAux' effect/state. |
| `Adrenaline` | Number | Applies or references the 'Adrenaline' effect/state. |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. |
| `AlliesTakeExtraTurn` | Number | Applies or references the 'AlliesTakeExtraTurn' effect/state. |
| `AllyInfested` | Block |  |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. |
| `AlternateIdleAnimation` | Enum | Applies or references the 'AlternateIdleAnimation' effect/state. |
| `Ammo` | Number | Applies or references the 'Ammo' effect/state. |
| `ApplyMultipleTimes` | Block | A loop block that executes its nested logic multiple times. |
| `ApplyPassives` | Block | Grants the nested passive abilities dynamically. |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. |
| `ApplyStatusIfCrit` | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. |
| `ApplyStatusesNextTurnBegin` | Block | Delays the application of the nested status effects until the start of the target's next turn. |
| `ApplyToConsumed` | Block | Redirects the nested effects to apply to the entity that just consumed this object. |
| `ApplyToOthersWithSharedTagAndFaction` | Block | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. |
| `ApplyToRandomClosestAlly` | Block | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `ApplyToSourceOnKill` | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. |
| `ApplyToTile` | Block | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. |
| `ArcLightning` | Block | Executes a chain-lightning logic block that bounces between targets. |
| `Attraction` | Number | Applies or references the 'Attraction' effect/state. |
| `AutoReanimate` | Number |  |
| `BackflipWhenTargeted` | Number | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BlackHoleSuck` | Number | Applies or references the 'BlackHoleSuck' effect/state. |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. |
| `Blind` | Array | Applies or references the 'Blind' effect/state. |
| `Bloodzerked` | Number | Applies or references the 'Bloodzerked' effect/state. |
| `BodyGuard` | Block | Protects an ally by intercepting attacks directed at them. |
| `BombRatTurtle` | Number | Applies or references the 'BombRatTurtle' effect/state. |
| `BonusCritChance` | Number | Applies the 'BonusCritChance' effect. |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. |
| `BonusDamageBasedOnDistance` | Number | Applies or references the 'BonusDamageBasedOnDistance' effect/state. |
| `BonusDamageBasedOnMana` | Number | Applies or references the 'BonusDamageBasedOnMana' effect/state. |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `BounceObject` | Enum | Spawns a physics object that visually bounces off the target. |
| `BounceRock` | Enum | Applies or references the 'BounceRock' effect/state. |
| `Bound` | Number | Applies or references the 'Bound' effect/state. |
| `Brace` | Number | Applies or references the 'Brace' effect/state. |
| `BramblesOnHit` | Number | Applies or references the 'BramblesOnHit' effect/state. |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. |
| `BurgleCoin` | Array | Applies or references the 'BurgleCoin' effect/state. |
| `Burn` | Number | Applies or references the 'Burn' effect/state. |
| `ButterflySwarm` | Number |  |
| `BypassRockKnockback` | Number | Applies or references the 'BypassRockKnockback' effect/state. |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `CancelPrimedAbilities` | Number | Applies or references the 'CancelPrimedAbilities' effect/state. |
| `CanceledQueuedInput` | Number | Applies or references the 'CanceledQueuedInput' effect/state. |
| `CapDamage` | Number | Applies or references the 'CapDamage' effect/state. |
| `CaptureFamiliar` | Number | Applies the 'CaptureFamiliar' effect. |
| `CatPartsSizeScaleStatus` | Block | Visually scales specific body parts of a character. |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. |
| `ChampionUpgradeNextMinion` | Number | Applies or references the 'ChampionUpgradeNextMinion' effect/state. |
| `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. |
| `ChanceToBreakFree` | Block | Provides a probability to escape a grapple or restraining effect. |
| `ChangeCatClass` | Enum | Applies or references the 'ChangeCatClass' effect/state. |
| `ChangeFaction` | Enum | Applies or references the 'ChangeFaction' effect/state. |
| `ChangeTile` | Enum | Transforms the terrain tile under the target. |
| `ChangeTilesUnder` | Enum | Applies or references the 'ChangeTilesUnder' effect/state. |
| `ChaosBossFlipMidTeleport` | Number | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. |
| `ChaosBossFormChange` | Number | Applies or references the 'ChaosBossFormChange' effect/state. |
| `CharacterTypeGainsStatusAtBattleStart` | Block |  |
| `Charge` | Number | Applies or references the 'Charge' effect/state. |
| `ChargeFists` | Number | Applies or references the 'ChargeFists' effect/state. |
| `CharismaUp` | Number | Applies or references the 'CharismaUp' effect/state. |
| `Charmed` | Array | Applies or references the 'Charmed' effect/state. |
| `CharmedFacingForceAttack` | Number | Applies or references the 'CharmedFacingForceAttack' effect/state. |
| `CharmedForceAttack` | Number | Applies or references the 'CharmedForceAttack' effect/state. |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. |
| `ClearDefaultDebris` | Number |  |
| `ClearFinalBossBattlefield` | Number | Applies or references the 'ClearFinalBossBattlefield' effect/state. |
| `ClearNegativeEffects` | Number | Applies the 'ClearNegativeEffects' effect. |
| `ClearStarving` | Number | Applies or references the 'ClearStarving' effect/state. |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. |
| `CloneWeaponTemp` | Number | Applies or references the 'CloneWeaponTemp' effect/state. |
| `CockroachSwarm` | Number |  |
| `CoinTossBounce` | Equation | Applies or references the 'CoinTossBounce' effect/state. |
| `CollectsPickups` | Number | Applies or references the 'CollectsPickups' effect/state. |
| `CollectsPickupsWithAltEffects` | Block | Triggers alternative nested effects when collecting items or pickups. |
| `CollideWithConsumed` | Equation | Applies or references the 'CollideWithConsumed' effect/state. |
| `CollideWithThrowTarget` | Number | Applies or references the 'CollideWithThrowTarget' effect/state. |
| `CompleteItemQuest` | Enum | Applies or references the 'CompleteItemQuest' effect/state. |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. |
| `ConjureBonusAbility` | Enum | Adds a temporary bonus ability to the character's hand/deck. |
| `ConjureRandomAbilityFromCat` | Number | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. |
| `ConjureSingleUseBonusAbility` | Enum | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. |
| `ConstitutionUp` | Array | Applies or references the 'ConstitutionUp' effect/state. |
| `Consumed` | Block | State block triggered when this object or entity is eaten/consumed by another character. |
| `ContextualHeal` | Number | Applies or references the 'ContextualHeal' effect/state. |
| `CopySpells` | Number | Duplicates existing spells currently in the character's hand. |
| `CorpseVaporizer` | Number | Applies or references the 'CorpseVaporizer' effect/state. |
| `Counterspell` | Number | Applies or references the 'Counterspell' effect/state. |
| `CrackMoonHead` | Number | Applies or references the 'CrackMoonHead' effect/state. |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. |
| `CreateGlobalModifiers` | Block | Generates global map or encounter rules/modifiers. |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. |
| `CurrentWeaponAddElectricElement` | Number | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. |
| `DamageBasedOnMissingHealth` | Number | Applies or references the 'DamageBasedOnMissingHealth' effect/state. |
| `DamageDistanceAOEFalloff` | Number | Applies or references the 'DamageDistanceAOEFalloff' effect/state. |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `DamageTrinket` | Number | Applies or references the 'DamageTrinket' effect/state. |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. |
| `DamageWeapon` | Number | Applies or references the 'DamageWeapon' effect/state. |
| `DeathwormUnderground` | Enum | Applies or references the 'DeathwormUnderground' effect/state. |
| `DecoySwapper` | Number | Applies or references the 'DecoySwapper' effect/state. |
| `DeferVaporize` | Number | Applies or references the 'DeferVaporize' effect/state. |
| `DelayCastAbility` | Enum | Queues an ability to be cast automatically after a certain delay or trigger. |
| `DelayedFury` | Number | Applies or references the 'DelayedFury' effect/state. |
| `DelayedWindCone` | Block | Creates a delayed Area of Effect cone. |
| `DeleteInanimateObjectsChance` | Number |  |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. |
| `DeleteTraps` | Number | Applies or references the 'DeleteTraps' effect/state. |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DestroyNeckArmor` | Number | Applies or references the 'DestroyNeckArmor' effect/state. |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. |
| `DestroyWeapon` | Number | Applies or references the 'DestroyWeapon' effect/state. |
| `DestroyWeaponThrow` | Number | Applies or references the 'DestroyWeaponThrow' effect/state. |
| `DexterityUp` | Number | Applies or references the 'DexterityUp' effect/state. |
| `Die` | Number | Applies or references the 'Die' effect/state. |
| `DieViaAbilityInternally` | Number | Applies or references the 'DieViaAbilityInternally' effect/state. |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. |
| `DiminishingHealthRegen` | Number | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DinoLegAnimation` | Enum | Applies or references the 'DinoLegAnimation' effect/state. |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. |
| `Disguised` | Number | Applies or references the 'Disguised' effect/state. |
| `Displace` | Number | Applies or references the 'Displace' effect/state. |
| `DisplaceToAbilityTarget` | Number | Applies or references the 'DisplaceToAbilityTarget' effect/state. |
| `DisplaceToOriginalPosition` | Number | Applies or references the 'DisplaceToOriginalPosition' effect/state. |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. |
| `DissolveRandomArmorPiece` | Number | Applies or references the 'DissolveRandomArmorPiece' effect/state. |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. |
| `DoDistortionRing` | Block | Creates a visual distortion ring effect on the screen. |
| `DoScreenShake` | Block | Triggers a camera screen shake effect. |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. |
| `DontHealEnemies` | Number | Applies or references the 'DontHealEnemies' effect/state. |
| `Doomed` | Number | Applies or references the 'Doomed' effect/state. |
| `DoubleCast` | Number | Applies or references the 'DoubleCast' effect/state. |
| `DoubleCastSpell` | Number | Applies or references the 'DoubleCastSpell' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. |
| `DoubleLoot` | Number | Applies or references the 'DoubleLoot' effect/state. |
| `DoubleStatus` | Enum | Applies or references the 'DoubleStatus' effect/state. |
| `DrainAllyCatsForFleshGolem` | Number | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. |
| `DrinkWater` | Number | Applies or references the 'DrinkWater' effect/state. |
| `Drowsy` | Number | Applies or references the 'Drowsy' effect/state. |
| `DuplicateRandomEquippedItem` | Number | Applies or references the 'DuplicateRandomEquippedItem' effect/state. |
| `DustOnHit` | Block | Spawns a specific particle or cloud object upon impact. |
| `DybbukPossessed` | Block | Defines the abilities and behaviors available when possessing another entity. |
| `EliteUpgradeNextMinion` | Number | Applies or references the 'EliteUpgradeNextMinion' effect/state. |
| `Else` | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `EmptyMind` | Number | Applies or references the 'EmptyMind' effect/state. |
| `EnableWeather` | Enum | Applies or references the 'EnableWeather' effect/state. |
| `EndTurn` | Number | Applies or references the 'EndTurn' effect/state. |
| `Enlarge` | Number | Applies or references the 'Enlarge' effect/state. |
| `EnterMount` | Enum | Applies or references the 'EnterMount' effect/state. |
| `EquipPermanentItem` | Enum | Applies or references the 'EquipPermanentItem' effect/state. |
| `EventBounty` | Number | Applies or references the 'EventBounty' effect/state. |
| `EvolveAbilityFromPool` | Enum | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `ExistUntilIdleUpkeep` | Number | Applies or references the 'ExistUntilIdleUpkeep' effect/state. |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. |
| `ExplodeCharacter_DeathBloom` | Number | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. |
| `ExplodeCharacter_DeathBloom2` | Number | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. |
| `ExplodeCharacter_NoDie` | Number | Applies or references the 'ExplodeCharacter_NoDie' effect/state. |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. |
| `ExplodeCharacter_PartyBoss` | Number | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. |
| `ExplodeCharacter_RockCrusher` | Number | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. |
| `ExplosionIfHitSomething` | Number | Applies or references the 'ExplosionIfHitSomething' effect/state. |
| `ExtraBasicAttacks_Status` | Number | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `FaceAway` | Number | Applies or references the 'FaceAway' effect/state. |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. |
| `FactionConversion` | Number | Applies the 'FactionConversion' effect. |
| `FactionDisguiseSource` | Number | Applies or references the 'FactionDisguiseSource' effect/state. |
| `FactionUprising` | Enum |  |
| `FastKnockback` | Number | Applies or references the 'FastKnockback' effect/state. |
| `Fear` | Number | Applies or references the 'Fear' effect/state. |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. |
| `FinalBossQueueBeam` | Number | Applies or references the 'FinalBossQueueBeam' effect/state. |
| `FindExtraItemFromPoolOnBattleEnd` | Enum |  |
| `FindItem` | Enum | Applies or references the 'FindItem' effect/state. |
| `FindItemFromPool` | Enum | Generates an item drop from the specified loot pool. |
| `FireArmor` | Number | Applies or references the 'FireArmor' effect/state. |
| `FireArmor2` | Number | Applies or references the 'FireArmor2' effect/state. |
| `FireStorm` | Number |  |
| `FireflySwarm` | Number |  |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. |
| `FlatLeechIfDamaged` | Number | Applies or references the 'FlatLeechIfDamaged' effect/state. |
| `FloatingRockTrap` | Number | Applies or references the 'FloatingRockTrap' effect/state. |
| `FlowersOnHit` | Number | Applies or references the 'FlowersOnHit' effect/state. |
| `FlySwarm` | Number |  |
| `Fog` | Number |  |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. |
| `ForceCollectsPickups` | Number | Applies or references the 'ForceCollectsPickups' effect/state. |
| `ForceDisplace` | Number | Applies or references the 'ForceDisplace' effect/state. |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. |
| `ForceImmediateMoveAndAttack` | Block | Forces the character to immediately move to a target and use a specified ability. |
| `ForceMoveAndAttack` | Number | Applies or references the 'ForceMoveAndAttack' effect/state. |
| `ForceMoveAway` | Number | Applies or references the 'ForceMoveAway' effect/state. |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. |
| `ForceMoveTowardsEnemies` | Number | Applies or references the 'ForceMoveTowardsEnemies' effect/state. |
| `ForceMoveTowardsTaggedObject` | Block | Forces the character to move towards the nearest object with a specific tag. |
| `ForceTransferWeapon` | Number | Applies or references the 'ForceTransferWeapon' effect/state. |
| `ForceUseAbility` | Enum | Applies or references the 'ForceUseAbility' effect/state. |
| `ForceUseAbility_NonStack` | Enum | Applies or references the 'ForceUseAbility_NonStack' effect/state. |
| `FormChange` | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FreeSpell` | Number | Applies or references the 'FreeSpell' effect/state. |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. |
| `GainCoinsRange` | Block | Grants the player a randomized amount of coins within a min/max range. |
| `GainDisorder` | Enum | Applies or references the 'GainDisorder' effect/state. |
| `GainDisorderFromPool` | Enum | Applies or references the 'GainDisorderFromPool' effect/state. |
| `GainDisorderFromPool_PostCast` | Enum | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |
| `GenericBuff` | Number | Applies or references the 'GenericBuff' effect/state. |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. |
| `GiveBoundItemToTarget` | Number | Applies or references the 'GiveBoundItemToTarget' effect/state. |
| `GlobalHealthRegenAura` | Number |  |
| `GlobalSpawnCharacter` | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `GlobalSpawnOnRoundEnd` | Block |  |
| `Grappled` | Number | Applies or references the 'Grappled' effect/state. |
| `HealPercentMaxHP` | Number | Applies or references the 'HealPercentMaxHP' effect/state. |
| `HealRandomInjury` | Number | Applies or references the 'HealRandomInjury' effect/state. |
| `HealTo` | Number | Applies or references the 'HealTo' effect/state. |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. |
| `HeatWave` | Number |  |
| `HeavyHits` | Number | Applies or references the 'HeavyHits' effect/state. |
| `Hex` | Number | Applies or references the 'Hex' effect/state. |
| `HitExplosion` | Number | Applies or references the 'HitExplosion' effect/state. |
| `IceArmor` | Number | Applies or references the 'IceArmor' effect/state. |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. |
| `IgnoreDebuffs` | Number | Applies or references the 'IgnoreDebuffs' effect/state. |
| `IgnoreSelf` | Number | Applies or references the 'IgnoreSelf' effect/state. |
| `ImmediateUseAbility` | Enum | Applies or references the 'ImmediateUseAbility' effect/state. |
| `ImmediateUseAbility_Instant` | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. |
| `ImmediateUseDirectionalAbility` | Enum | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. |
| `Imprison` | Enum | Applies or references the 'Imprison' effect/state. |
| `IncAuxCounterCycle` | Block | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. |
| `IncreaseCumulativeBlastDamage` | Number | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. |
| `IncreaseItemAuxOnKill` | Number | Applies or references the 'IncreaseItemAuxOnKill' effect/state. |
| `Infested` | Number | Applies or references the 'Infested' effect/state. |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. |
| `InstantMaxHealthUp` | Number | Applies or references the 'InstantMaxHealthUp' effect/state. |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeMoveActPoints` | Number | Applies or references the 'InterchangeMoveActPoints' effect/state. |
| `Invulnerable` | Number | Applies or references the 'Invulnerable' effect/state. |
| `JohnnyCriesForWashers` | Number | Applies or references the 'JohnnyCriesForWashers' effect/state. |
| `JudgementDay` | Number |  |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. |
| `KnockOutClone` | Enum | Applies or references the 'KnockOutClone' effect/state. |
| `KnockOutCoin` | Number | Forces the target to drop coins. |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. |
| `KnockbackDamageImmuneUntilSettled` | Number | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. |
| `KnockbackDirectionIsFacingDirection` | Enum | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. |
| `LateStatusApplication` | Block | Applies a status effect after all primary damage and effects have fully resolved. |
| `LaunchOffScreen` | Equation | Applies or references the 'LaunchOffScreen' effect/state. |
| `LaunchOffScreenInstakill` | Number | Applies or references the 'LaunchOffScreenInstakill' effect/state. |
| `LeaveBehindRockOnKnockback` | Number | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. |
| `Leech` | Number | Applies or references the 'Leech' effect/state. |
| `Leeches` | Number | Applies or references the 'Leeches' effect/state. |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. |
| `LowGravityKnockbackBoost` | Number |  |
| `LowGravityRangeBoost` | Number |  |
| `LowerAmbientLight` | Number |  |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | Applies the Madness debuff/status effect. |
| `MadnessChanceOnTurnBegin` | Number | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. |
| `MagicWeakness` | Number | Applies or references the 'MagicWeakness' effect/state. |
| `MakeWeaponUnbreakable` | Number | Applies or references the 'MakeWeaponUnbreakable' effect/state. |
| `ManaGain` | Equation | Applies or references the 'ManaGain' effect/state. |
| `ManaLeeches` | Number | Applies or references the 'ManaLeeches' effect/state. |
| `ManaSteal` | Number | Applies or references the 'ManaSteal' effect/state. |
| `ManaStealToHealth` | Number | Applies or references the 'ManaStealToHealth' effect/state. |
| `ManglerAttack` | Number | Applies or references the 'ManglerAttack' effect/state. |
| `ManglerShuffle` | Boolean | Applies or references the 'ManglerShuffle' effect/state. |
| `Marked` | Number | Applies or references the 'Marked' effect/state. |
| `MassAttackThis` | Number | Applies or references the 'MassAttackThis' effect/state. |
| `Math` | Block | Triggers the Tinkerer's Math ability sequence. |
| `MaxHPUp` | Number | Applies or references the 'MaxHPUp' effect/state. |
| `Meaty` | Number | Applies or references the 'Meaty' effect/state. |
| `MergeDamageInstance` | Block | Combines damage numbers or visual hit effects. |
| `MeteorShower` | Number |  |
| `Meteornado` | Number |  |
| `Metronome` | Number | Executes a random musical or metronome ability. |
| `MimicMetronome` | Number | Applies or references the 'MimicMetronome' effect/state. |
| `MonkStanceSwitch` | Number | Applies or references the 'MonkStanceSwitch' effect/state. |
| `MotherTumorDebugForcePass` | Number | Applies or references the 'MotherTumorDebugForcePass' effect/state. |
| `MoveQuivered` | Number | Applies or references the 'MoveQuivered' effect/state. |
| `MovementUp` | Number | Applies or references the 'MovementUp' effect/state. |
| `Muted` | Number | Applies or references the 'Muted' effect/state. |
| `NextAbilityHeals` | Number | Applies or references the 'NextAbilityHeals' effect/state. |
| `NextActionLuckUp` | Number | Applies or references the 'NextActionLuckUp' effect/state. |
| `NextAttackBonusRange` | Number | Applies or references the 'NextAttackBonusRange' effect/state. |
| `NextAttackSpecialCrit` | Number | Modifies the character's next attack to have special critical properties. |
| `NextBasicAttackCritsThisTurn` | Block | Guarantees the next basic attack executed this turn will be a critical hit. |
| `NextBattleStatusStacks` | Block | Carries over the specified status effects into the next encounter/battle. |
| `NextDamageReduceAndHealAllies` | Number | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. |
| `NextTurnDoubleRangedDamage` | Number | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. |
| `NonStackingDivineShield` | Number | Applies or references the 'NonStackingDivineShield' effect/state. |
| `ObjectOnHit` | Enum | Spawns a specific physics/item object upon impact. |
| `ObjectOnHitCharacter` | Enum | Spawns a specific character or entity upon impact. |
| `ObjectOnHitEmpty` | Enum | Applies or references the 'ObjectOnHitEmpty' effect/state. |
| `ObjectOnHitFullyEmpty` | Enum | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. |
| `Ostracized` | Number | Applies or references the 'Ostracized' effect/state. |
| `OverHealToShield` | Number | Applies or references the 'OverHealToShield' effect/state. |
| `OverHealToStatuses` | Block | Converts excessive healing beyond maximum health into specific status effects. |
| `OverrideChainKnockback` | Number | Applies or references the 'OverrideChainKnockback' effect/state. |
| `OverrideChainKnockbackDamage` | Equation | Applies or references the 'OverrideChainKnockbackDamage' effect/state. |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. |
| `OverrideKnockbackDamage` | Number | Applies or references the 'OverrideKnockbackDamage' effect/state. |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. |
| `PartialPurge` | Number | Applies or references the 'PartialPurge' effect/state. |
| `PermanentCharisma` | Number | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentCharm` | Number | Applies the 'PermanentCharm' effect. |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Number | Applies or references the 'PermanentDexterity' effect/state. |
| `PermanentImmobile` | Number | Applies or references the 'PermanentImmobile' effect/state. |
| `PermanentIntelligence` | Number | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Number | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentSpeed` | Number | Applies or references the 'PermanentSpeed' effect/state. |
| `PermanentStrength` | Number | Applies or references the 'PermanentStrength' effect/state. |
| `PermanentUpgradeRandomActive` | Number | Applies or references the 'PermanentUpgradeRandomActive' effect/state. |
| `PermanentUpgradeRandomActiveOrPassive` | Number | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. |
| `PersistentElement` | Enum |  |
| `Petrify` | Array | Applies or references the 'Petrify' effect/state. |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. |
| `Poison` | Number | Applies or references the 'Poison' effect/state. |
| `PoisonLace` | Equation | Applies or references the 'PoisonLace' effect/state. |
| `PoolMetronome` | Block | Executes a random ability drawn from a specific pool. |
| `PopAndSpawn` | Enum | Destroys the target and replaces it with a new spawned entity. |
| `Possessed` | Number | Applies or references the 'Possessed' effect/state. |
| `ProbeCharmed` | Number | Applies or references the 'ProbeCharmed' effect/state. |
| `PullSourceToKnockbackImmuneTarget` | Number | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. |
| `PullSourceToTarget` | Number | Applies or references the 'PullSourceToTarget' effect/state. |
| `Purge` | Number | Applies or references the 'Purge' effect/state. |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. |
| `QuakeAreaChance` | Block | Provides a probability to trigger an earthquake Area of Effect. |
| `QueueUseAbility` | Enum | Applies or references the 'QueueUseAbility' effect/state. |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. |
| `RNGCannonRandomDamage` | Number | Applies or references the 'RNGCannonRandomDamage' effect/state. |
| `Rain` | Number |  |
| `RandomBonusDamage` | Number | Applies or references the 'RandomBonusDamage' effect/state. |
| `RandomDistanceDisplace` | Number | Displaces the target by a randomized distance. |
| `RandomInjury` | Number | Applies or references the 'RandomInjury' effect/state. |
| `RandomKnockback` | Block | Applies a randomized amount of knockback force. |
| `RandomKnockbackDirection` | Number | Applies or references the 'RandomKnockbackDirection' effect/state. |
| `RandomLightning` | Number |  |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. |
| `RandomPermanentStat` | Number | Applies or references the 'RandomPermanentStat' effect/state. |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. |
| `RandomStatusFromPool` | Block | Selects and applies a random status effect from the provided nested block. |
| `RandomWeatherEachFight` | Array |  |
| `RangeUp` | Number | Applies or references the 'RangeUp' effect/state. |
| `Reanimate` | Number | Applies or references the 'Reanimate' effect/state. |
| `RebukeDamage` | Number | Applies or references the 'RebukeDamage' effect/state. |
| `ReduceManaCost` | Number | Applies or references the 'ReduceManaCost' effect/state. |
| `ReduceManaCostExcludeBrainstorm` | Number | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. |
| `Reflect` | Number | Applies or references the 'Reflect' effect/state. |
| `ReformMoonHead` | Number | Applies or references the 'ReformMoonHead' effect/state. |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. |
| `RefreshItemAbilities` | Number | Applies or references the 'RefreshItemAbilities' effect/state. |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. |
| `RefreshMovePointsIfHit` | Number | Applies or references the 'RefreshMovePointsIfHit' effect/state. |
| `RefreshNonManaItemAbilities` | Number | Applies or references the 'RefreshNonManaItemAbilities' effect/state. |
| `RefreshOncePerFightAbilities` | Number | Applies or references the 'RefreshOncePerFightAbilities' effect/state. |
| `RefreshWeaponAbility` | Number | Applies or references the 'RefreshWeaponAbility' effect/state. |
| `Regurge` | Number | Applies or references the 'Regurge' effect/state. |
| `RemoveActPoints` | Number | Applies or references the 'RemoveActPoints' effect/state. |
| `RemoveItem` | Enum | Applies or references the 'RemoveItem' effect/state. |
| `RemoveKnockback` | Number | Applies or references the 'RemoveKnockback' effect/state. |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. |
| `RemoveStatus` | Enum | Applies or references the 'RemoveStatus' effect/state. |
| `RemoveStatusStacks` | Block | Removes a specific number of stacks of a status effect. |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. |
| `RepairAll` | Number | Applies or references the 'RepairAll' effect/state. |
| `RepairAllCondition` | Number | Applies or references the 'RepairAllCondition' effect/state. |
| `RepairArmorCondition` | Number | Applies or references the 'RepairArmorCondition' effect/state. |
| `RepairOnKill` | Number | Applies or references the 'RepairOnKill' effect/state. |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Number | Applies or references the 'RepairWeapon' effect/state. |
| `RepairWeaponCondition` | Number | Applies or references the 'RepairWeaponCondition' effect/state. |
| `RerollEnemy` | Number | Applies or references the 'RerollEnemy' effect/state. |
| `ResetArmorShield` | Number | Applies or references the 'ResetArmorShield' effect/state. |
| `ReturnDinoLegs` | Number | Applies or references the 'ReturnDinoLegs' effect/state. |
| `Revive` | Number | Applies or references the 'Revive' effect/state. |
| `ReviveNextRound` | Number | Queues the character to be resurrected at the start of the next combat round. |
| `Rot` | Number | Applies or references the 'Rot' effect/state. |
| `SafeDie` | Number | Applies or references the 'SafeDie' effect/state. |
| `SafeDoomed` | Number | Applies the 'SafeDoomed' effect. |
| `Sandstorm` | Number |  |
| `ScatterCoins` | Block | Throws coins out into the level randomly. |
| `ScatterHeldCoin` | Array | Applies or references the 'ScatterHeldCoin' effect/state. |
| `ScatterRandomPickups` | Number | Applies or references the 'ScatterRandomPickups' effect/state. |
| `ScrambleEverything` | Number | Applies or references the 'ScrambleEverything' effect/state. |
| `ScrambleLastUsedSpell` | Block | Randomizes or scrambles the properties of the last spell cast. |
| `Scrambled` | Number | Applies or references the 'Scrambled' effect/state. |
| `SelfStun` | Array | Applies or references the 'SelfStun' effect/state. |
| `SendRock` | Number | Applies or references the 'SendRock' effect/state. |
| `SetAnimationAlts` | Block | Overrides specific animation states with alternative animations. |
| `SetCrazyEyeBackgroundWeights` | Block | Adjusts visual rendering weights for the 'Crazy Eye' background effect. |
| `SetDefaultFace` | Enum | Applies or references the 'SetDefaultFace' effect/state. |
| `SetDistanceDisplace` | Number | Applies or references the 'SetDistanceDisplace' effect/state. |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. |
| `SetItemAux` | Block | Applies or references the 'SetItemAux' effect/state. |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. |
| `ShadowCrit` | Number | Applies or references the 'ShadowCrit' effect/state. |
| `Shatter` | Number | Applies or references the 'Shatter' effect/state. |
| `Shield` | Equation | Applies or references the 'Shield' effect/state. |
| `ShootHereCommand` | Number | Applies or references the 'ShootHereCommand' effect/state. |
| `ShootHereReceiver` | Number | Applies or references the 'ShootHereReceiver' effect/state. |
| `ShortCircuit` | Number | Applies or references the 'ShortCircuit' effect/state. |
| `ShowFakeDamage` | Block | Displays a visual damage number without actually modifying health. |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. |
| `SignalFinalBossShieldBroke` | Number | Applies or references the 'SignalFinalBossShieldBroke' effect/state. |
| `SizeScale` | Enum | Applies or references the 'SizeScale' effect/state. |
| `Sleep` | Number | Applies or references the 'Sleep' effect/state. |
| `Slow` | Number | Applies or references the 'Slow' effect/state. |
| `SmallHitExplosion` | Number | Applies or references the 'SmallHitExplosion' effect/state. |
| `SmartMetronome` | Number | Executes a 'smart' random ability that aims to be beneficial based on context. |
| `SmellBlood` | Number | Applies or references the 'SmellBlood' effect/state. |
| `Snow` | Number |  |
| `SolarFlare` | Block |  |
| `SoulLink` | Number | Applies or references the 'SoulLink' effect/state. |
| `SoundEventOnHit` | Enum | Applies or references the 'SoundEventOnHit' effect/state. |
| `SourceSwapsBackEndOfTurn` | Enum | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. |
| `SpawnBearTrap` | Number | Applies or references the 'SpawnBearTrap' effect/state. |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. |
| `SpawnCoinAnywhere` | Array | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `SpawnCreep` | Number | Applies or references the 'SpawnCreep' effect/state. |
| `SpawnCustomTrap` | Enum | Applies or references the 'SpawnCustomTrap' effect/state. |
| `SpawnExtraThingsOnBattleStart` | Block |  |
| `SpawnFlames` | Array | Applies or references the 'SpawnFlames' effect/state. |
| `SpawnNeutralWebTrapOnMiss` | Number | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. |
| `SpawnRock` | Number | Applies or references the 'SpawnRock' effect/state. |
| `SpawnThingIfHitKills` | Enum | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| `SpawnTilePuddleOnBattleStart` | Block |  |
| `SpawnVolcanoOnBattleStart` | Block |  |
| `SpawnWebTrap` | Number | Applies or references the 'SpawnWebTrap' effect/state. |
| `SpecialBossMultipartInstakill` | Enum | Applies or references the 'SpecialBossMultipartInstakill' effect/state. |
| `SpecialGodRays` | Block |  |
| `SpecificInjury` | Equation | Applies or references the 'SpecificInjury' effect/state. |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. |
| `SpellShield` | Number | Applies or references the 'SpellShield' effect/state. |
| `SpiderInfested` | Number | Applies or references the 'SpiderInfested' effect/state. |
| `SpitConsumed` | Number | Applies or references the 'SpitConsumed' effect/state. |
| `SplashDamage` | Number | Applies or references the 'SplashDamage' effect/state. |
| `SpreadDisease` | Block | Provides a chance to transmit a disease status to adjacent targets. |
| `StackingSandstorm` | Number | Applies or references the 'StackingSandstorm' effect/state. |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. |
| `StatBounty` | Number | Applies or references the 'StatBounty' effect/state. |
| `StatusAllCharactersOnSpawn` | Block |  |
| `StatusCharactersOnRoundEnd` | Block |  |
| `StatusCharactersOnRoundStart` | Block |  |
| `StatusGroup` | Block | Groups multiple status effects together for batch application. |
| `StealDemonicGlyph` | Number | Applies or references the 'StealDemonicGlyph' effect/state. |
| `StealEquipment` | Enum | Applies or references the 'StealEquipment' effect/state. |
| `StealTurn` | Number | Applies or references the 'StealTurn' effect/state. |
| `Stealth` | Number | Applies or references the 'Stealth' effect/state. |
| `StealthCritChance` | Number | Applies or references the 'StealthCritChance' effect/state. |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Array | Applies or references the 'Stun' effect/state. |
| `SwallowSmallCharacter` | Number | Applies or references the 'SwallowSmallCharacter' effect/state. |
| `SwapHighestAndLowestStat` | Number | Applies or references the 'SwapHighestAndLowestStat' effect/state. |
| `SwapWeapon` | Block | Replaces the character's currently equipped weapon with one from a specified pool. |
| `SwitchMusic` | Block | Changes the background music track or layer during combat. |
| `Switcheroo` | Number | Applies or references the 'Switcheroo' effect/state. |
| `T2CopyCat` | Number | Applies or references the 'T2CopyCat' effect/state. |
| `T3HitlerTriggerInitialSpawns` | Number | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. |
| `TagMetronome` | Enum | Applies or references the 'TagMetronome' effect/state. |
| `TakeBonusTurnWithAIControl` | Block | Grants the character an immediate extra turn, but forces the AI to control them during it. |
| `TakeBonusTurnWithStatus` | Block | Grants the character an immediate extra turn while afflicted with specific statuses. |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. |
| `TakeExtraTurnEndOfRound` | Number | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. |
| `Tangled` | Number | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `TargetedMetronome` | Number | Applies or references the 'TargetedMetronome' effect/state. |
| `Tarred` | Number | Applies or references the 'Tarred' effect/state. |
| `Taunting` | Number | Applies or references the 'Taunting' effect/state. |
| `TeamBonusAbility` | Enum | Applies or references the 'TeamBonusAbility' effect/state. |
| `TeamCastAbility` | Enum | Requires or involves multiple characters to execute the ability. |
| `Tech` | Number | Applies or references the 'Tech' effect/state. |
| `TeleportBackAtTurnEnd` | Enum | Applies or references the 'TeleportBackAtTurnEnd' effect/state. |
| `TempBackstab` | Number | Applies or references the 'TempBackstab' effect/state. |
| `TempBackstabBleed` | Number | Applies or references the 'TempBackstabBleed' effect/state. |
| `TempBackstabPiercing` | Number | Applies or references the 'TempBackstabPiercing' effect/state. |
| `TempBackstabPoison` | Number | Applies or references the 'TempBackstabPoison' effect/state. |
| `TempBasicAttackBonusAOE` | Number | Applies or references the 'TempBasicAttackBonusAOE' effect/state. |
| `TempBonusKnockback` | Number | Applies or references the 'TempBonusKnockback' effect/state. |
| `TempBonusKnockbackDamage` | Number | Applies or references the 'TempBonusKnockbackDamage' effect/state. |
| `TempCounterAttack` | Number | Applies or references the 'TempCounterAttack' effect/state. |
| `TempCritChanceUp` | Number | Applies or references the 'TempCritChanceUp' effect/state. |
| `TempDamageUp` | Number | Applies or references the 'TempDamageUp' effect/state. |
| `TempDexterityUp` | Equation | Applies or references the 'TempDexterityUp' effect/state. |
| `TempInitiativeChange` | Number | Applies or references the 'TempInitiativeChange' effect/state. |
| `TempInjuryImmunity` | Number | Applies or references the 'TempInjuryImmunity' effect/state. |
| `TempLuckUp` | Number | Applies or references the 'TempLuckUp' effect/state. |
| `TempManaCostReduction` | Number | Applies or references the 'TempManaCostReduction' effect/state. |
| `TempMovement` | Number | Applies or references the 'TempMovement' effect/state. |
| `TempPassiveUntilSettled` | Block | Passive: Active only until the physics engine stops moving the character. |
| `TempPassiveWhileHasStatus` | Block | Grants nested passives only while the character possesses the specified status. |
| `TempPenetrate` | Number | Applies or references the 'TempPenetrate' effect/state. |
| `TempPreEmptiveCounterAttack` | Number | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. |
| `TempRangeUp` | Number | Applies or references the 'TempRangeUp' effect/state. |
| `TempSpeedUp` | Number | Applies or references the 'TempSpeedUp' effect/state. |
| `TempSpellDamageUp` | Number | Applies or references the 'TempSpellDamageUp' effect/state. |
| `TempStrengthUp` | Equation | Applies or references the 'TempStrengthUp' effect/state. |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. |
| `ThornsDamageImmuneUntilSettled` | Number | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. |
| `TickDownStatus` | Enum | Applies or references the 'TickDownStatus' effect/state. |
| `TileDamageImmuneUntilSettled` | Number | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. |
| `TilesMovedToCritChance` | Number | Applies or references the 'TilesMovedToCritChance' effect/state. |
| `TilesMovedToMana` | Number | Applies or references the 'TilesMovedToMana' effect/state. |
| `TilesMovedToNeighborHeal` | Enum | Applies or references the 'TilesMovedToNeighborHeal' effect/state. |
| `TilesMovedToStrength` | Number | Applies or references the 'TilesMovedToStrength' effect/state. |
| `TimeDelayStatusApplication` | Block | Delays the nested effects by a specified amount of real-time seconds. |
| `TowerDefenseStatus` | Number | Applies or references the 'TowerDefenseStatus' effect/state. |
| `TowerDefenseStatus2` | Number | Applies or references the 'TowerDefenseStatus2' effect/state. |
| `TradeLife` | Number | Applies or references the 'TradeLife' effect/state. |
| `TrailBlazer` | Number | Applies or references the 'TrailBlazer' effect/state. |
| `Trample` | Number | Applies or references the 'Trample' effect/state. |
| `TransformAbility` | Enum | Applies or references the 'TransformAbility' effect/state. |
| `TransformBasicAttack` | Enum | Applies or references the 'TransformBasicAttack' effect/state. |
| `TransformBasicMove` | Enum | Applies or references the 'TransformBasicMove' effect/state. |
| `TransformEquipment` | Block | Upgrades or transforms a specific equipped item into another. |
| `TransformNow` | Enum | Applies or references the 'TransformNow' effect/state. |
| `TransformWeapon` | Block | Transforms the equipped weapon into another specific weapon state. |
| `Trapper_Status` | Number | Applies or references the 'Trapper_Status' effect/state. |
| `TriggerDOTStatuses` | Number | Applies or references the 'TriggerDOTStatuses' effect/state. |
| `TriggerGameEnding` | Number | Applies or references the 'TriggerGameEnding' effect/state. |
| `TriggerMotherConsume` | Number | Applies or references the 'TriggerMotherConsume' effect/state. |
| `TriggerMotherGrow` | Number | Applies or references the 'TriggerMotherGrow' effect/state. |
| `TriggerWerewolfTransform` | Array | Applies or references the 'TriggerWerewolfTransform' effect/state. |
| `TurnAround` | Number | Applies or references the 'TurnAround' effect/state. |
| `TurnControlDelay` | Enum | Applies or references the 'TurnControlDelay' effect/state. |
| `TurnRight` | Number | Applies or references the 'TurnRight' effect/state. |
| `TwisterDisplaceWithDamage` | Block | A whirlwind effect that randomly displaces targets and deals damage. |
| `UndoDamage` | Number | Applies or references the 'UndoDamage' effect/state. |
| `UpgradeRandomAbility` | Number | Applies or references the 'UpgradeRandomAbility' effect/state. |
| `UseAbility` | Enum | Forces the character or target to instantly use a specified ability. |
| `UseMoveAbilityWithAI` | Block | Forces the character to execute a movement ability using specific AI weights. |
| `UseRandomSpell_Madness` | Number | Applies the 'UseRandomSpell_Madness' effect. |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. |
| `VaporizeCorpseFlipAdvantage` | Array | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. |
| `VaporizeDice` | Number | Applies or references the 'VaporizeDice' effect/state. |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. |
| `VaporizeTarget` | Number | Applies or references the 'VaporizeTarget' effect/state. |
| `VisualCountDownThenApplyStatus` | Block | Displays a visual countdown above the target before applying the nested effects. |
| `VisualFX` | Enum | Applies or references the 'VisualFX' effect/state. |
| `VisualFXTile` | Enum | Applies or references the 'VisualFXTile' effect/state. |
| `VisualFlySwarm` | Number |  |
| `WaggleClone` | Block | Spawns visual clones or alternative hitbox variants of the projectile. |
| `Weakness` | Number | Applies or references the 'Weakness' effect/state. |
| `WeaponAuxMultiplier` | Enum | Applies or references the 'WeaponAuxMultiplier' effect/state. |
| `Webbed` | Number | Applies or references the 'Webbed' effect/state. |
| `Windy` | Number |  |
| `XIsTargetHealth` | Block | Math variable assignment: Evaluates X as the target's current health. |

</details>

### Known Explicit Parameters

These are hardcoded configuration keys found within these blocks (not dynamic IDs).

<details>
<summary><b>Expand</b></summary>

| Parameter | Type | Notes |
| :--- | :--- | :--- |
| `Conditional_AbilityTargetIsSelf` | Block | Conditional constraint. Nested properties only trigger if this is true. |
| `Conditional_ActiveWeather_Any` | Block | Conditional trigger: Executes nested logic if the current map weather matches any in the list. |
| `Conditional_AffectedByElement` | Block | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. |
| `Conditional_Ally` | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `Conditional_Backstab` | Block | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. |
| `Conditional_BadRoll` | Block | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. |
| `Conditional_Boss` | Block | Conditional trigger: Executes nested logic if the target is a Boss. |
| `Conditional_BossOrBig` | Block | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. |
| `Conditional_Buddy` | Block | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. |
| `Conditional_CanBeHealed` | Block | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. |
| `Conditional_Corpse` | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| `Conditional_DebuffRoll` | Block | Conditional trigger: Executes nested logic based on a randomized debuff probability. |
| `Conditional_DestructibleCorpse` | Block | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. |
| `Conditional_Enemy` | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `Conditional_Familiar` | Block | Conditional trigger: Executes nested logic if the target is a familiar. |
| `Conditional_FinishedSpawning` | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. |
| `Conditional_FirstApplicationThisTurn` | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. |
| `Conditional_FormulaIsPositive` | Block | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Conditional_HasCleansableDebuffs` | Block | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. |
| `Conditional_HasKnockback` | Block | Conditional: Executes logic if the triggering attack deals knockback. |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Conditional_HasTag` | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `Conditional_InForm` | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. |
| `Conditional_IsSelf` | Block | Conditional trigger: Executes nested logic if the target is the caster themselves. |
| `Conditional_IsTrample` | Block | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. |
| `Conditional_LastHit` | Block | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. |
| `Conditional_LivingPlayerCat` | Block | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. |
| `Conditional_NotAlly` | Block | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. |
| `Conditional_NotBig` | Block | Conditional trigger: Executes nested logic if the target is NOT classified as large. |
| `Conditional_NotBoss` | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| `Conditional_NotBossOrBig` | Block | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. |
| `Conditional_NotShielded` | Block | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. |
| `Conditional_Object` | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. |
| `Conditional_OncePerBattle` | Block | Conditional trigger: Executes nested logic only once per encounter/battle. |
| `Conditional_PartyMember` | Block | Conditional block: Executes nested logic only if the target is/has PartyMember. |
| `Conditional_PlayerCat` | Block | Conditional trigger: Executes nested logic if the target is a player-controlled cat. |
| `Conditional_RandomChance` | Block | Conditional trigger: Executes nested logic based on a flat percentage random roll. |
| `Conditional_Shielded` | Block | Conditional trigger: Executes nested logic if the target currently has a Shield status. |
| `Conditional_SourceAbilityHasTag` | Block | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. |
| `Conditional_SourceHasStatus` | Block | Conditional trigger: Executes nested logic if the caster currently has the specified status. |
| `Conditional_Speculative` | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. |
| `do_not_pop_corpse` | Boolean |  |
| `drop_body_ability` | Enum |  |
| `drop_on_death` | Boolean |  |
| `drop_on_self_death` | Boolean |  |
| `element` | Enum | The specific element type to check for. |
| `extra_statuses` | Block | Additional generic status applications. |
| `force_contact` | Boolean | If true, enforces physical overlap. |
| `form` | Enum | The specific form ID to check for. |
| `formula` | Equation | The math expression to evaluate. |
| `instant` | Boolean |  |
| `key` | Enum | A unique string identifier to track this specific application. |
| `kill_on_consume` | Boolean |  |
| `mount_mode` | Enum | If true, treats the consumption as riding/mounting instead of eating. |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| `status` | Enum | The specific status ID to check for. |
| `struggle_ability` | Enum | Ability triggered by the consumed entity while inside the consumer. |
| `tag` | Enum | The specific string tag to check for. |
| `threshold_expr` | Equation |  |
| `threshold_flat` | Number | A flat numerical health value threshold. |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). |
| `use_placeholder` | Boolean |  |
| `weather` | Array | An array of weather states to check against. |
| `wet` | Boolean |  |

</details>

### Context Index

The following Conditional and targeting blocks all behave as `[effect_block]` containers. Each has its own unique parameters listed below its entry.

---

#### `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `weather` | Array | An array of weather states to check against. |

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_Ally`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `element` | Enum | The specific element type to check for. |
| [`Conditional_Speculative`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_Corpse`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `odds` | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_HasStatus`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_InForm`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_Enemy`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `odds` | Number | The probability (0.0 to 1.0) of applying the debuff. |

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_FinishedSpawning`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_NotBoss`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_PartyMember`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `key` | Enum | A unique string identifier to track this specific application. |

</details>

---

#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `formula` | Equation | The math expression to evaluate. |

</details>

---

#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| [`Conditional_Corpse`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `status` | Enum | The specific status ID to check for. |

</details>

---

#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `tag` | Enum | The specific string tag to check for. |
| [`Conditional_Boss`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_InForm`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_NotBoss`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `threshold_expr` | Equation |  |
| `threshold_flat` | Number | A flat numerical health value threshold. |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). |
| [`Conditional_OncePerBattle`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `form` | Enum | The specific form ID to check for. |

</details>

---

#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `threshold_flat` | Number |  |

</details>

---

#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_Enemy`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_HasTag`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `key` | Enum |  |

</details>

---

#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_IsSelf`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `odds` | Number |  |

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |

</details>

---

#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `tag` | Enum | Specific entity tag required. |

</details>

---

#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `status` | Enum | ID of the status effect to apply or check. |

</details>

---

#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `tag` | Enum | The specific entity tag required or applied. |
| [`Conditional_Ally`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_HealthThreshold`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `Consumed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| `do_not_pop_corpse` | Boolean |  |
| `drop_body_ability` | Enum |  |
| `drop_on_death` | Boolean |  |
| `drop_on_self_death` | Boolean |  |
| `extra_statuses` | Block | Additional generic status applications. |
| `force_contact` | Boolean | If true, enforces physical overlap. |
| `instant` | Boolean |  |
| `kill_on_consume` | Boolean |  |
| `mount_mode` | Enum | If true, treats the consumption as riding/mounting instead of eating. |
| `struggle_ability` | Enum | Ability triggered by the consumed entity while inside the consumer. |
| `use_placeholder` | Boolean |  |
| `wet` | Boolean |  |

</details>

---

#### `Else`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_Displaceable`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HasKnockback`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HasStatus`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HasTag`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Object`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Speculative`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

---

#### `effects`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Notes |
| :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Any valid effect from the global effects schema. |
| [`Conditional_AbilityTargetIsSelf`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_ActiveWeather_Any`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_AffectedByElement`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Ally`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Backstab`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_BadRoll`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Boss`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_BossOrBig`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Buddy`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_CanBeHealed`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Corpse`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_DebuffRoll`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_DestructibleCorpse`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Displaceable`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Enemy`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Familiar`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_FirstApplicationThisTurn`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_FormulaIsPositive`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HasCleansableDebuffs`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HasStatus`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HasTag`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_InForm`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_IsSelf`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_IsTrample`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_LastHit`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_LivingPlayerCat`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_NotAlly`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_NotBig`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_NotBoss`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_NotBossOrBig`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_NotShielded`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Object`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_OncePerBattle`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_RandomChance`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Shielded`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_SourceAbilityHasTag`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_SourceHasStatus`](./Engine_Effects.md#context-index) | Block | Nested conditional. |
| [`Conditional_Speculative`](./Engine_Effects.md#context-index) | Block | Nested conditional. |

</details>

