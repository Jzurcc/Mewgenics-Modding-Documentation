# Mewgenics Mod Developer Documentation: Engine: Status IDs

> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Engine: Status IDs

This document lists every confirmed Status ID found across all game data files. These IDs are used as **dynamic keys** in any Status Container block (e.g. `AddStatusToBasicAttack`, `StatusOnKill`, `MeleeRevengeDamage`). The value paired with each key is typically the stack count or duration.

> **Note:** This list reflects confirmed base-game usage. Many additional statuses likely exist or can be synthesized by the engine.

### All Confirmed `[status_id]` Values

<details>
<summary><b>Expand</b></summary>

| ID | Type | Notes |
| :--- | :--- | :--- |
| `AbilityOnBattleStart` | Enum | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AbilityOnBattleStart_Immediate` | Enum | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| `AddInitiative` | Number | Applies or references the 'AddInitiative' effect/state. |
| `AddRandomEliteBuff` | Number |  |
| `AddStartingMana` | Number | Applies or references the 'AddStartingMana' effect/state. |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. |
| `AlphaTurns` | Number | Applies or references the 'AlphaTurns' effect/state. |
| `ApplyStatusIfCrit` | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `AutoReanimate` | Number | Applies the 'AutoReanimate' effect. |
| `BackflipWhenTargeted` | Number | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BigSplashDamage` | Number | Applies the 'BigSplashDamage' effect. |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. |
| `BlessingOfPeace` | Number | Applies or references the 'BlessingOfPeace' effect/state. |
| `Blind` | Number |  |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `BounceObject` | Enum | Spawns a physics object that visually bounces off the target. |
| `Bounty` | Number | Applies the 'Bounty' effect. |
| `Brace` | Number | Applies or references the 'Brace' effect/state. |
| `BrittleCharismaUp` | Number | Applies or references the 'BrittleCharismaUp' effect/state. |
| `BrittleConstitutionUp` | Number | Applies or references the 'BrittleConstitutionUp' effect/state. |
| `BrittleDexterityUp` | Number | Applies or references the 'BrittleDexterityUp' effect/state. |
| `BrittleIntelligenceUp` | Number | Applies or references the 'BrittleIntelligenceUp' effect/state. |
| `BrittleLuckUp` | Number | Applies or references the 'BrittleLuckUp' effect/state. |
| `BrittleSpeedUp` | Number | Applies or references the 'BrittleSpeedUp' effect/state. |
| `BrittleStrengthUp` | Number | Applies or references the 'BrittleStrengthUp' effect/state. |
| `Bruise` | Number | Applies the 'Bruise' effect. |
| `BurgleCoin` | Number | Applies the 'BurgleCoin' effect. |
| `Burn` | Number | Applies or references the 'Burn' effect/state. |
| `ChanceToBreak` | Number | Applies the 'ChanceToBreak' effect. |
| `ChangeTile` | Enum |  |
| `ChangeTileUnderCharacterAtStart` | Enum | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. |
| `ChangeTilesUnder` | Enum | Applies or references the 'ChangeTilesUnder' effect/state. |
| `Charge` | Number | Applies or references the 'Charge' effect/state. |
| `CharismaUp` | Number | Applies or references the 'CharismaUp' effect/state. |
| `Charmed` | Number | Applies the 'Charmed' effect. |
| `Cleanse` | Number | Applies the 'Cleanse' effect. |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Confusion` | Number | Applies the 'Confusion' effect. |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. |
| `Consumed` | Block | State triggered when the entity is eaten/consumed. |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. |
| `CreateGlobalModifiers` | Block | Generates global map or encounter rules/modifiers. |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. |
| `CureDisease` | Block | Applies the 'CureDisease' effect. |
| `CurrentWeaponDamageUp` | Number | Applies the 'CurrentWeaponDamageUp' effect. |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. |
| `DelayedPain` | Number | Applies or references the 'DelayedPain' effect/state. |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. |
| `DexterityUp` | Number | Applies or references the 'DexterityUp' effect/state. |
| `DiminishingHealthRegen` | Number | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DistanceBonusDamage` | Block | Applies the 'DistanceBonusDamage' effect. |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. |
| `DoubleCastSpellThisTurn` | Number | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |
| `DrinkWater` | Number | Applies or references the 'DrinkWater' effect/state. |
| `Drowsy` | Number |  |
| `Else` | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `EmptyMana` | Number | Applies the 'EmptyMana' effect. |
| `EquipPermanentItem` | Enum | Applies the 'EquipPermanentItem' effect. |
| `EquipTemporaryItem` | Enum | Applies the 'EquipTemporaryItem' effect. |
| `ExtraBasicAttacks_Status` | Number | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `FaceAway` | Number | Applies the 'FaceAway' effect. |
| `Fear` | Number | Applies or references the 'Fear' effect/state. |
| `Fights` | Number | Applies or references the 'Fights' effect/state. |
| `FillMana` | Array | Applies the 'FillMana' effect. |
| `FindItem` | Enum | Applies or references the 'FindItem' effect/state. |
| `FindItemFromPool` | Enum | Generates an item drop from the specified loot pool. |
| `FlatLeech` | Number |  |
| `FlippedFacingForceAttack` | Number | Applies the 'FlippedFacingForceAttack' effect. |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. |
| `ForceUseAbility` | Enum | Applies or references the 'ForceUseAbility' effect/state. |
| `ForceUseAbilityOnTarget` | Block | Applies or references the 'ForceUseAbilityOnTarget' effect/state. |
| `FormChange` | Block | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `Freeze` | Number | Applies the 'Freeze' effect. |
| `FullHeal` | Number | Applies the 'FullHeal' effect. |
| `GainCoins` | Number | Applies or references the 'GainCoins' effect/state. |
| `GainCoinsRange` | Block | Grants the player a randomized amount of coins within a min/max range. |
| `GainDisorder` | Enum | Applies or references the 'GainDisorder' effect/state. |
| `GainDisorderFromPool` | Block | Logic: Applies a negative mutation/disorder from a specific pool. |
| `HealAndOverhealToShield` | Number | Applies the 'HealAndOverhealToShield' effect. |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. |
| `Hex` | Number | Applies or references the 'Hex' effect/state. |
| `ImmediateUseAbility` | Enum | Applies or references the 'ImmediateUseAbility' effect/state. |
| `Immobile` | Number | Applies the 'Immobile' effect. |
| `IncAuxCounterClamped` | Block | Increments a generic auxiliary counter on the character, capped by a maximum value. |
| `Infested` | Number | Applies or references the 'Infested' effect/state. |
| `Instakill` | Array |  |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. |
| `KnockOutCoin` | Array | Forces the target to drop coins. |
| `KnockUpAndAway` | Block |  |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. |
| `KnockbackIfCrit` | Block | Applies or references the 'KnockbackIfCrit' effect/state. |
| `LeaveBehindRockOnKnockback` | Number | Applies the 'LeaveBehindRockOnKnockback' effect. |
| `Leech` | Number | Applies the 'Leech' effect. |
| `LeechPercent` | Number | Applies the 'LeechPercent' effect. |
| `Leeches` | Number |  |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | Applies or references the 'MagicWeakness' effect/state. |
| `ManaGain` | Equation | Applies or references the 'ManaGain' effect/state. |
| `ManaGainRange` | Block | Applies or references the 'ManaGainRange' effect/state. |
| `ManaLeeches` | Number | Applies or references the 'ManaLeeches' effect/state. |
| `Marked` | Number | Applies or references the 'Marked' effect/state. |
| `MissChance` | Number | Applies or references the 'MissChance' effect/state. |
| `MoveQuivered` | Number | Applies or references the 'MoveQuivered' effect/state. |
| `MovementUp` | Number | Applies the 'MovementUp' effect. |
| `NextBattleStatus` | Block | Applies the 'NextBattleStatus' effect. |
| `NoHealthRegen` | Number | Applies or references the 'NoHealthRegen' effect/state. |
| `NoManaRegen` | Number | Applies or references the 'NoManaRegen' effect/state. |
| `NonLethal` | Number | Applies the 'NonLethal' effect. |
| `NonStackingDivineShield` | Number | Applies the 'NonStackingDivineShield' effect. |
| `ObjectOnHitCharacter` | Enum | Spawns a specific character or entity upon impact. |
| `OneUseSpellDamageUp` | Number | Applies the 'OneUseSpellDamageUp' effect. |
| `Ostracized` | Number | Applies or references the 'Ostracized' effect/state. |
| `OverrideChainKnockback` | Number | Applies or references the 'OverrideChainKnockback' effect/state. |
| `OverrideChainKnockbackDamage` | Number | Applies the 'OverrideChainKnockbackDamage' effect. |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. |
| `PercentHeal` | Number | Applies the 'PercentHeal' effect. |
| `PermanentCharisma` | Number | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentConfusion` | Number | Applies or references the 'PermanentConfusion' effect/state. |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Number | Applies the 'PermanentDexterity' effect. |
| `PermanentIntelligence` | Number | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Number | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentMadness` | Number | Applies the 'PermanentMadness' effect. |
| `PermanentSpeed` | Number | Applies the 'PermanentSpeed' effect. |
| `PermanentStrength` | Number | Applies or references the 'PermanentStrength' effect/state. |
| `Petrify` | Number | Applies the 'Petrify' effect. |
| `Piercing` | Number | Applies the 'Piercing' effect. |
| `Poison` | Number | Applies or references the 'Poison' effect/state. |
| `PoisonLace` | Number | Applies or references the 'PoisonLace' effect/state. |
| `Possessed` | Number | Applies or references the 'Possessed' effect/state. |
| `PreEmptiveCounterNextAttacks` | Number | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. |
| `ProbeCharmed` | Number | Applies or references the 'ProbeCharmed' effect/state. |
| `PullSourceToKnockbackImmuneTarget` | Number | Applies the 'PullSourceToKnockbackImmuneTarget' effect. |
| `PullSourceToTarget` | Number | Applies or references the 'PullSourceToTarget' effect/state. |
| `Purge` | Number | Applies the 'Purge' effect. |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. |
| `RandomInjury` | Number | Applies the 'RandomInjury' effect. |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. |
| `RandomPermanentStat` | Number | Applies or references the 'RandomPermanentStat' effect/state. |
| `RandomPermanentStatsDistinct` | Block |  |
| `RandomStatDown` | Number |  |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. |
| `RandomStatusFromPool` | Block | Selects and applies a random status effect from the provided nested block. |
| `RandomTaggedMutation` | Enum | Applies or references the 'RandomTaggedMutation' effect/state. |
| `RangeUp` | Number | Applies the 'RangeUp' effect. |
| `Reanimate` | Number | Applies the 'Reanimate' effect. |
| `ReduceManaCost` | Number | Applies the 'ReduceManaCost' effect. |
| `Reflect` | Number | Applies or references the 'Reflect' effect/state. |
| `RefreshActPoints` | Number | Applies the 'RefreshActPoints' effect. |
| `RefreshMovePoints` | Number | Applies the 'RefreshMovePoints' effect. |
| `RemoteFlatLeech` | Number | Applies or references the 'RemoteFlatLeech' effect/state. |
| `RemoteLeech` | Number | Applies or references the 'RemoteLeech' effect/state. |
| `RemoveAmbientLightEffects` | Number | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `RemoveGlobalModifiers` | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. |
| `RemoveStatus` | Enum | Applies or references the 'RemoveStatus' effect/state. |
| `RemoveStatusStacks` | Block | Logic: Removes stacks of a specific status effect. |
| `RepairAll` | Number | Applies or references the 'RepairAll' effect/state. |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Number | Applies or references the 'RepairWeapon' effect/state. |
| `RepairWeaponCondition` | Number | Applies the 'RepairWeaponCondition' effect. |
| `Revive` | Number | Applies or references the 'Revive' effect/state. |
| `ReviveNextRound` | Block | Queues the character to be resurrected at the start of the next combat round. |
| `Rot` | Number | Applies or references the 'Rot' effect/state. |
| `SafeDie` | Number | Applies or references the 'SafeDie' effect/state. |
| `ScatterCoins` | Array |  |
| `Scrambled` | Number | Applies or references the 'Scrambled' effect/state. |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. |
| `SetItemAux` | Block | Applies or references the 'SetItemAux' effect/state. |
| `Shield` | Number | Applies or references the 'Shield' effect/state. |
| `Sleep` | Number | Applies the 'Sleep' effect. |
| `Slow` | Number | Applies or references the 'Slow' effect/state. |
| `SoulLink` | Number | Applies the 'SoulLink' effect. |
| `SpawnBearTrapOnMiss` | Number | Applies the 'SpawnBearTrapOnMiss' effect. |
| `SpawnCoinAnywhere` | Number | Applies the 'SpawnCoinAnywhere' effect. |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. |
| `SpeedUp_WithoutInitiative` | Number | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. |
| `SpellDamageUp` | Number | Applies the 'SpellDamageUp' effect. |
| `SpiderInfested` | Number | Applies or references the 'SpiderInfested' effect/state. |
| `SplashDamage` | Number | Applies the 'SplashDamage' effect. |
| `SpreadDisease` | Block | Provides a chance to transmit a disease status to adjacent targets. |
| `StackingSandstorm` | Number |  |
| `StatusAfterXStacks` | Block | Applies or references the 'StatusAfterXStacks' effect/state. |
| `StatusGroup` | Block | Groups multiple status effects together for batch application. |
| `Stealth` | Number | Applies the 'Stealth' effect. |
| `StealthUntilBasicAttack` | Number | Applies or references the 'StealthUntilBasicAttack' effect/state. |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Number | Applies the 'Stun' effect. |
| `TakeBonusTurnWithStatus` | Block | Grants the character an immediate extra turn while afflicted with specific statuses. |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. |
| `Tangled` | Array | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `Tarred` | Number | Applies or references the 'Tarred' effect/state. |
| `Tech` | Number | Applies the 'Tech' effect. |
| `TempCounterAttack` | Number | Applies or references the 'TempCounterAttack' effect/state. |
| `TempDamageUp` | Number | Applies the 'TempDamageUp' effect. |
| `TempMeleeRangeUp` | Number | Applies or references the 'TempMeleeRangeUp' effect/state. |
| `TempMovement` | Number | Applies the 'TempMovement' effect. |
| `TempNoManaRegen` | Number | Applies or references the 'TempNoManaRegen' effect/state. |
| `TempPassiveUntilSettled` | Block | Applies or references the 'TempPassiveUntilSettled' effect/state. |
| `TempRangeUp` | Number | Applies or references the 'TempRangeUp' effect/state. |
| `TempSpellDamageUp` | Number | Applies the 'TempSpellDamageUp' effect. |
| `TempStrengthUp` | Number | Applies or references the 'TempStrengthUp' effect/state. |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. |
| `TransformWeapon` | Block | Transforms the equipped weapon into another specific weapon state. |
| `UseAbility` | Enum |  |
| `UseAbility_Madness` | Enum | Applies the 'UseAbility_Madness' effect. |
| `UseAbility_NonStack` | Enum | Applies or references the 'UseAbility_NonStack' effect/state. |
| `VaporizeInanimate` | Number |  |
| `VisualFXTile` | Enum |  |
| `Weakness` | Number | Applies the 'Weakness' effect. |
| `Webbed` | Number | Applies or references the 'Webbed' effect/state. |
| `Wet` | Number | Applies or references the 'Wet' effect/state. |
| `Zombie` | Number |  |

</details>

### Known Explicit Parameters

These are hardcoded configuration keys found within these blocks (not dynamic IDs).

<details>
<summary><b>Expand</b></summary>

| Parameter | Type | Notes |
| :--- | :--- | :--- |
| `Conditional_Adjacent` | Block | Conditional block: Executes nested logic only if the target is/has Adjacent. |
| `Conditional_Ally` | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `Conditional_BadRoll` | Block | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. |
| `Conditional_Boss` | Block | Conditional trigger: Executes nested logic if the target is a Boss. |
| `Conditional_Corpse` | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| `Conditional_Enemy` | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `Conditional_FirstApplicationThisTurn` | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. |
| `Conditional_Flying` | Block |  |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Conditional_HasCleansableDebuffs` | Block |  |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Conditional_HasTag` | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `Conditional_ManaThreshold` | Block | Conditional constraint. Nested properties only trigger if this is true. |
| `Conditional_NotBoss` | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| `Conditional_PartyMember` | Block | Conditional constraint. Nested properties only trigger if this is true. |
| `Conditional_RandomChance` | Block |  |
| `Conditional_Shielded` | Block | Conditional trigger: Executes nested logic if the target currently has a Shield status. |
| `Conditional_SourceHasTag` | Block | Conditional block: Executes nested logic only if the target is/has SourceHasTag. |
| `Conditional_Tiny` | Block |  |
| `ally_chance` | Number |  |
| `cant_miss` | Boolean |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `count` | Number | Quantity. |
| `damage` | Number | The base damage properties of an attack. |
| `effects` | Block | Non-damaging status applications and logic triggers executed on impact. |
| `element` | Enum | The specific element type required or applied. |
| `elements` | Array |  |
| `end_of_round` | Boolean |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. |
| `exclude_self` | Boolean |  |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. |
| `knockback` | Number |  |
| `must_do_damage` | Boolean |  |
| `stacks` | Number | Number of stacks or intensity to apply. |
| `tag` | Enum | Specific entity tag required. |
| `triggers_limit` | Number |  |
| `type` | Enum | Classification/category type. |

</details>

