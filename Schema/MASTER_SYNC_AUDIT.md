# Master Schema Sync Audit

## Contexts Missing from Master (7)

These contexts exist in a split file but have no matching entry in Master.

| Split File | Context Name |
| :--- | :--- |
| `Combat_Rewards.md` | `1` |
| `Combat_Rewards.md` | `2` |
| `Combat_Rewards.md` | `3` |
| `Combat_Rewards.md` | `4` |
| `Difficulties.md` | `easy` |
| `Spawns_and_Enemy_Pools.md` | `editor` |
| `Spawns_and_Enemy_Pools.md` | `weather_element_alt` |

## Property Mismatches (1792 contexts differ)

These contexts exist in both files but have different property tables.

### `AddStatusToBasicAttack` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (43):** `ApplyStatusIfCrit`, `ApplyToSource`, `BigSplashDamage`, `Bleed`, `Blind`, `BounceObject`, `Bruise`, `BurgleCoin`, `Burn`, `ChangeTile`, `Charmed`, `Conditional_Adjacent`, `Conditional_Ally`, `Conditional_Enemy`, `Conditional_HasTag`, `Conditional_Shielded`, `Conditional_SourceHasTag`, `Confusion`, `DamageOrHealConditionally`, `DistanceBonusDamage`, `Else`, `Fear`, `Freeze`, `KnockOutCoin`, `Knockback`, `Leech`, `Leeches`, `LuckUp`, `Madness`, `MagicWeakness`, `ManaLeeches`, `OverrideChainKnockback`, `OverrideChainKnockbackDamage`, `Piercing`, `Poison`, `Rot`, `Slow`, `SoulLink`, `SpawnBearTrapOnMiss`, `SplashDamage`, `SpreadDisease`, `Stun`, `Weakness`

### `AlphaStatusOnTurnBegin` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DoubleCastSpellThisTurn`

### `ApplyMultipleTimes` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomStatusFromPool`

### `ApplyPassives` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `AddInitiative`, `AddTag`, `ElementImmune`, `Flying`, `IgnoreTiles`, `KnockbackImmunity`, `Plant`, `ReplaceBasicAttack`, `StatusOnBattleEnd`, `YOffset`

### `ApplyPassivesToSpawnerWhileAlive` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HideEquipment`

### `ApplyStatusIfCrit` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Purge`

### `ApplyStatusesNextTurnBegin` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Quivered`

### `ApplyToConsumed` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `DeleteObject`, `Die`

### `ApplyToOthersWithSharedTagAndFaction` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Marked`

### `ApplyToRandomClosestAlly` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `ForceMoveTowards`

### `ApplyToRandomPartyMemberIfPossible` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `GainDisorderFromPool`, `GainDisorderFromPool_PostCast`

### `ApplyToSource` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Shield`

### `ApplyToSourceOnKill` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `AlphaCat`, `CompleteItemQuest`, `EvolveAbilityFromPool`, `HealthGain`, `ManaGain`, `RefreshActPoints`, `RemoveItem`, `Revive`, `StrengthUp`, `TakeExtraTurn`, `TransformWeapon`, `WeaponAuxMultiplier`

### `ApplyToTile` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `ObjectOnHit`, `SpawnBearTrap`

### `AutocastEachRound` (from `Abilities_and_Spells.md`)

**In Master but NOT in split file (1):** `force_display_name`

### `CanApplyToInanimate` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `ApplyToSource`, `ObjectOnHitCharacter`, `Temporary`, `Vaporize`

### `CatPartsTransform` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `palette`

### `ChangeTile` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `chance`

### `CollectsPickupsWithAltEffects` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `LuckUp`, `Quivered`, `RandomStatUp`, `Shield`, `Tech`

### `Conditional_ActiveWeather_Any` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DestroyEquipmentAndAttachParasite`

### `Conditional_AffectedByElement` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `BonusCritChance`, `Burn`, `Conditional_Speculative`

### `Conditional_Ally` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `AllStatsUp`, `ApplyToSource`, `Cleanse`, `ClearNegativeEffects`, `DamageUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `TempSpeedUp`

### `Conditional_Backstab` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `BonusCritChance`, `Fear`

### `Conditional_BadRoll` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Temporary`

### `Conditional_Boss` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `Stun`

### `Conditional_BossOrBig` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Immobile`

### `Conditional_Buddy` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_InForm`, `Consumed`, `Else`

### `Conditional_CanBeHealed` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomStatusFromPool`

### `Conditional_Corpse` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Charmed`, `DamageUp`, `OverrideDamage`, `Revive`, `SafeDoomed`, `SpeedUp`, `TakeExtraTurn`

### `Conditional_DebuffRoll` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DestroyEquipmentAndAttachParasite`

### `Conditional_DestructibleCorpse` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `ApplyToTile`, `VaporizeCorpse`

### `Conditional_Displaceable` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `LaunchOffScreen`, `LaunchOffScreenInstakill`, `TempInitiativeChange`

### `Conditional_Enemy` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_PartyMember`, `Confusion`, `Else`, `RandomStatusFromPool`, `Stun`

### `Conditional_Familiar` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `BonusDamage`, `DamageUp`, `DivineShield`

### `Conditional_FinishedSpawning` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `Imprison`

### `Conditional_FirstApplicationThisTurn` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `key`, `{Logic Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FillMana`, `ManaGain`, `TakeExtraTurn`

### `Conditional_FormulaIsPositive` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (8):** `Burn`, `Freeze`, `Immobile`, `OverrideKnockbackDamage`, `Shield`, `Slow`, `SpeedUp`, `Stun`

### `Conditional_GoodRoll` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseRandomSpell_Madness`

### `Conditional_HasCleansableDebuffs` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `GenericBuff`, `PartialCleanse`, `RandomStatusFromPool`, `VisualFX`

### `Conditional_HasStatus` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

### `Conditional_HasTag` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `FlatLeechIfDamaged`

### `Conditional_HealthThreshold` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (12):** `ApplyToSource`, `BonusDamage`, `CaptureFamiliar`, `Conditional_OncePerBattle`, `Die`, `DieViolently`, `FactionConversion`, `FlatLeech`, `FullHeal`, `Instakill`, `SpawnThingIfHitKills`, `Vaporize`

### `Conditional_InForm` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `CritChanceUp`, `DamageUp`, `DodgeChance_Status`, `ForceImmediateMoveAndAttack`, `FormChange`, `SpeedUp`, `UseAbility`

### `Conditional_IsSelf` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `OverrideDamage`

### `Conditional_IsTrample` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `SetKnockback`

### `Conditional_LastHit` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `BonusDamage`, `Bruise`, `DelayCastAbility`, `KnockUpAndAway`

### `Conditional_LivingPlayerCat` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `ApplyToSource`, `Consumed`, `TempPassiveWhileHasStatus`

### `Conditional_NotAlly` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Confusion`, `Temporary`

### `Conditional_NotBig` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `DisplaceTowardsSource`

### `Conditional_NotBoss` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Enemy`

### `Conditional_NotBossOrBig` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Immobile`

### `Conditional_NotShielded` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Knockback`

### `Conditional_Object` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `CanApplyToInanimate`, `Conditional_HasTag`, `Else`, `RepairWeapon`

### `Conditional_OncePerBattle` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (6):** `CompleteItemQuest`, `ReduceManaCost`, `Shield`, `ShowText`, `SpellDamageUp`, `TriggerGameEnding`

### `Conditional_PlayerCat` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `Adrenaline`, `ApplyToSource`, `Charge`, `Cleanse`, `ConjureRandomAbilityFromCat`, `GenericDebuff`, `KnockOutClone`, `Scrambled`, `T2CopyCat`

### `Conditional_RandomChance` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `ApplyPassives`, `AutoReanimate`

### `Conditional_Shielded` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `BonusCritChance`

### `Conditional_SourceAbilityHasTag` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ApplyToSource`, `ScatterCoins`

### `Conditional_SourceHasStatus` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bruise`

### `Conditional_Speculative` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (8):** `BonusDamage`, `BonusDamageBasedOnDistance`, `CapDamage`, `Conditional_HealthThreshold`, `Else`, `IgnoreDamage`, `Knockback`, `RandomBonusDamage`

### `Consumed` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (12):** `do_not_pop_corpse`, `drop_body_ability`, `drop_on_death`, `drop_on_self_death`, `extra_statuses`, `force_contact`, `instant`, `kill_on_consume`, `mount_mode`, `struggle_ability`, `use_placeholder`, `wet`

### `Craft` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `temporary`, `works_with_tech`

### `CreateGlobalModifiers` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Global Modifier Keys}`

**In Master but NOT in split file (4):** `BloodRain`, `LowerAmbientLight`, `NextPlayerCatTakesExtraTurn`, `NoCorpses`

### `DelayedWindCone` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `damage`

### `DoDamage` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `Else` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `CaptureFamiliar`, `FactionConversion`, `Fear`, `Marked`, `PermanentCharm`, `TempSpeedUp`

### `KnockUpAndAway` (from `Abilities_and_Spells.md`)

**In Master but NOT in split file (2):** `displace`, `self_damage`

### `LateStatusApplication` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AddWeaponAux`, `CurrentWeaponDamageUp`

### `Math` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ApplyToSource`, `Stun`

### `MeleeRevengeDamage` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (6):** `Poison`, `SpreadDisease`, `Weakness`, `damage`, `effects`, `elements`

### `MergeDamageInstance` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `can_instapop`

### `NextBasicAttackCritsThisTurn` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `cant_miss`, `piercing`

### `NextBattleStatusStacks` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `MadnessChanceOnTurnBegin`

### `NukeQuestFinalBossModifications` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `self_damage`

### `ObjectOnHitCharacter` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `chance`

**In Master but NOT in split file (1):** `stacks`

### `OverHealToStatuses` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `RandomStatUp`, `TakeExtraTurn`

### `PassiveWhileNotTakingTurn` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AddStatusToBasicAttack`

### `PopAndSpawn` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `no_splatter`

### `ROOT` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (23):** `ai_ability`, `bonk_damage`, `bonus_passives`, `chain_ability`, `class`, `cloned_ability`, `cost`, `damage`, `damage_instance`, `empty_self_damage`, `graphics`, `keyword_tooltips`, `sounds`, `spawn`, `splash_damage`, `sub_ability`, `tags`, `target`, `template`, `temporary_effects`, `variant_of`, `{Damaging Keys}`, `{Event Keys}`

**In Master but NOT in split file (8):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `stock_fill_order`

### `RandomStatusFromPool` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (37):** `AllStatsUp`, `Bleed`, `BleedThorns`, `Blind`, `Brace`, `Bruise`, `Burn`, `Charge`, `Charmed`, `Confusion`, `ConstitutionUp`, `DiminishingHealthRegen`, `DivineShield`, `Fear`, `Freeze`, `Immobile`, `KineticSpikes`, `Madness`, `MagicWeakness`, `Marked`, `MoveQuivered`, `ObjectOnHitCharacter`, `Petrify`, `Poison`, `Quivered`, `Reflect`, `Shield`, `Sleep`, `Slow`, `SpawnCoinAnywhere`, `SpeedUp`, `StatusGroup`, `StrengthUp`, `Stun`, `Tarred`, `Thorns`, `Weakness`

### `RevengeDamage` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `effects`, `knockback`

### `ReviveNextRound` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AllStatsUp`, `DivineShield`, `Shield`

### `SetAnimationAlts` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (2):** `dead`, `dying`

### `SpreadDisease` (from `Abilities_and_Spells.md`)

**In Master but NOT in split file (1):** `can_apply_to_anything`

### `StatusGroup` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `DexterityUp`, `LuckUp`, `SpawnCoinAnywhere`, `SpeedUp`

### `StatusKillers` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Conditional_Boss`, `Conditional_NotBoss`

### `StatusOnBattleEnd` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `CureDisease`, `FindItemFromPool`, `NextBattleStatus`, `PermanentConstitution`, `PermanentIntelligence`, `PermanentSpeed`, `PermanentStrength`, `RandomMutation`, `RandomPermanentStat`

### `TakeBonusTurnWithAIControl` (from `Abilities_and_Spells.md`)

**In Master but NOT in split file (1):** `end_of_round`

### `TakeBonusTurnWithStatus` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Madness`

### `TempPassiveWhileHasStatus` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddManaRegen`, `HealthRegenUp`, `MeleeRevengeDamage`, `ReplaceSpell`

### `Temporary` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (3):** `data`, `expires_on_appliers_turn`, `expires_on_move`

### `TimeDelayStatusApplication` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (3):** `{Graphics Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `Cleanse`, `CreateGlobalModifiers`, `DoScreenShake`, `FormChange`, `FullHeal`, `GlobalSpawnCharacter`, `PlayBackground`, `RemoveAmbientLightEffects`, `SwitchMusic`, `Vaporize`, `delay`

### `VisualCountDownThenApplyStatus` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `XIsTargetHealth` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `BonusDamage`

### `additional_passives` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (15):** `AllStatsUp`, `ApplyPassivesToSpawnerWhileAlive`, `CaptureFamiliar`, `DamageUp`, `FadeInsteadOfDie`, `FillMana`, `HealthGain`, `HideEquipment`, `IllusionTint`, `InjuryImmunity`, `PermanentMadness`, `ReviveNextRound`, `SafeDoomed`, `SchizoIllusionAIModifier`, `SpeedUp`

### `bonk_damage` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `bonus_passives` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (75):** `AbilityDisableIfLivingCrow`, `AbilityEnableIfConsumedCharacterHasTag`, `AbilityEnabledAtHealthThreshold`, `AbilityEnabledIfBasicAttackUsedThisTurn`, `AbilityEnabledIfHasStatus`, `AbilityEnabledIfMovementTrapped`, `AbilityEnabledIfNoAggroTarget`, `AbilityEnabledIfNotHasStatus`, `AbilityEnabledIfSpecificItemEquipped`, `AbilityEnabledOncePerFightAtHealthThreshold`, `AbilityEnabledOncePerRound`, `AbilityEnabledPercentEachTurn`, `AbilityInheritsWeaponEffects`, `AbsorbManaFromOtherSpells`, `AddElementsToSpells`, `AddStatusToBasicAttack`, `AlphaDodgeChance`, `AlphaStatusOnTurnBegin`, `AutocastEachRound`, `BonusAbility_DelayedApplication`, `CapTechSpent`, `CatchBoomerang`, `CaveWomanBirthControl`, `ChargeSpiritBombAura`, `CopyBasicAttackEffects`, `CopyCatPassive_Initializer`, `CritChanceUp`, `DeadAltAbility`, `DownRankAIIfWeaponUsable`, `FistOfFateUniqueEnemyTracker`, `FreeFirstCast`, `FreeFirstCastAndAfterSpendMana`, `FreeFirstCastEachMatch`, `HealthRegenUp`, `IgnoreTiles`, `IntelligenceUp`, `InterchangeDisabler`, `KnockbackImmunity`, `ModifyAbility`, `MoonHeadFinisherEnabler`, `NukeQuestFinalBossModifications`, `PassiveWhileNotTakingTurn`, `ReloadOnAllyCatDies`, `ReloadOnAllyDies`, `ReloadOnAnyDamage`, `ReloadOnBackstab`, `ReloadOnElementalDamageReceived`, `ReloadOnGainCoins`, `ReloadOnGainDivineShield`, `ReloadOnKill`, `ReloadOnKillEnemy`, `ReloadOnKillTagged`, `ReloadOnSpendMana`, `ReloadOnTotalDamageReceived`, `ReloadOnUseAbilityWithManaCost`, `RevengeDamage`, `StatusKillers`, `TossTargetIsAggroTarget`, `TossTargetIsBuddy`, `TossTargetIsNotInWater`, `Trample`, `XIsConsumedCharacterMaxHP`, `XIsCountDeaths`, `XIsCountStatusStacks`, `XIsFormulaLockedUntilComplete`, `XIsFreeArmorSlots`, `XIsIncreaseEachTurn`, `XIsLivingAlliesWithTag`, `XIsLivingCharactersWithTag`, `XIsMultipliedPercentHealth`, `XIsOtherHealsThisTurn`, `XIsRampAndReset`, `XIsRecycleCostReduction`, `XIsSpellStormRampAndReset`, `XIsTimesDamageTaken`

### `damage` (from `Abilities_and_Spells.md`)

**In Master but NOT in split file (4):** `animation`, `good`, `label`, `stat`

### `damage_instance` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (3):** `{Damaging Keys}`, `{Event Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (32):** `HealthRegenUp`, `accuracy`, `blocked_damage`, `blocked_multiplier`, `can_collect_pickups`, `can_instapop`, `can_revive`, `cant_miss`, `crit_chance`, `custom_additional_ai_weight`, `damage_shield_only`, `disallow_modifications`, `effects`, `final_hit_bonus_damage`, `force_adjacent_and_diagonal_contact`, `force_no_contact`, `force_no_knockback`, `force_play_hit_animation`, `heal`, `hint_dont_lowgravboost`, `hit_animation_alt`, `incidentally_collects_pickups`, `layer`, `makes_contact`, `non_lethal`, `override_trample_damage`, `piercing`, `ranged`, `raw_damage`, `raw_heal`, `show_damage_on_0`, `two_way_contact`

### `effects` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `empty_self_damage` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `extra_statuses` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Burn`, `Conditional_HasTag`, `HealthGain`, `Poison`, `Tarred`

### `graphics` (from `Abilities_and_Spells.md`)

**In Master but NOT in split file (34):** `alt_animations`, `always_huge_mask`, `art_flip`, `custom_cat_data`, `default_attack_animation`, `default_face`, `depth_offset`, `desc`, `dont_sink`, `four_way_animations`, `hud_palette`, `move_speed_multiplier`, `move_speed_sync_frames`, `movieclip`, `name`, `no_horizontal_flip`, `no_splatter`, `non_blocking_animations`, `override_portrait`, `piece_alt_frame`, `portrait_face`, `projectile_spawn_offset`, `randomize_starting_frame`, `scale`, `shade_occluded_objects`, `shadow`, `shadow_size`, `show_infinity_damage_warning`, `spawnin_animation`, `status_display_count_max`, `tint`, `tooltip`, `uifloaters_offset`, `water_mask`

### `keyword_tooltips` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `TemporaryItem`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Weakness`

### `meta` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (14):** `ability_icon`, `class`, `icon_damage_display`, `icon_damage_display_eq`, `icon_damage_display_suffix`, `icon_damage_type`, `icon_shell_frame`, `is_basic_attack`, `is_move`, `is_trinket`, `is_weapon`, `tooltip_values`, `type_icon`, `{Graphics Keys}`

**In Master but NOT in split file (9):** `delay_enable_tooltips`, `house_shop`, `keeper`, `movieclip`, `npc_script`, `pick_n`, `shopkeeper_fights`, `treasure_room`, `welcome_message`

### `post_spawn_statuses` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DoDamage`, `EnterMount`, `VisualFXTile`

### `self_damage` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Event Keys}`

**In Master but NOT in split file (5):** `cant_miss`, `effects`, `heal`, `non_lethal`, `piercing`

### `spawn` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `custom_additional_ai_weight`, `layer`, `lob`, `spawnin_animation`

### `splash_damage` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (7):** `crit_chance`, `effects`, `force_no_knockback`, `force_play_hit_animation`, `layer`, `makes_contact`, `override_trample_damage`

### `target` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `aoe_spell_on_land`, `dont_orient`, `force_no_contact`, `min_range`

### `temporary_effects` (from `Abilities_and_Spells.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AfterImage`, `DoubleLoot`, `KnockbackImmunity`, `TileTrail`, `TileTrail_Ahead`, `Trample`

### `ROOT` (from `Boss_Cutscene_Info.md`)

**In split file but NOT in Master (4):** `frame_label`, `quotes`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `ROOT` (from `Cat_Classes.md`)

**In split file but NOT in Master (16):** `ability_groups`, `ability_pool`, `attack_pool`, `complicated_abilities`, `complicated_passives`, `graphics`, `innate_items`, `innate_passives`, `levelup_stats`, `move_pool`, `passive_pool`, `starter_abilities`, `stat_mods`, `tutorial_levelup_active_pool`, `tutorial_levelup_active_pool_2`, `tutorial_levelup_passive_pool`

**In Master but NOT in split file (8):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `stock_fill_order`

### `graphics` (from `Cat_Classes.md`)

**In Master but NOT in split file (147):** `affected_animation`, `affected_particle`, `air_animation`, `ally_animation`, `always_huge_mask`, `always_play_animations`, `animate_name`, `animation`, `animation_in`, `animation_out`, `aoe_spell_on_land`, `apex_distance`, `apex_time`, `area_particle`, `art_flip`, `beam_cap`, `beam_clip`, `bounce_on_hit`, `bypass_combatspeed`, `center_particle`, `chain_distance`, `chain_movieclip`, `custom_cat_data`, `custom_priming_animation`, `damage_threshold_altanimations`, `darken_screen`, `darken_screen_exclude_characters_on_tile`, `darken_screen_exclude_self`, `darken_screen_start_early`, `dash_animation`, `dash_attack_animation`, `dash_bonk_animation`, `dash_decelerating_animation`, `dash_end_animation`, `dash_start_animation`, `decelerate`, `default_attack_animation`, `delay`, `delay_from_map_center`, `delay_from_map_edge`, `delay_from_reverse_map_edge`, `depth_offset`, `desc`, `detatched_animation`, `detatched_animation_cutoff`, `detatched_animation_reach`, `do_animation_offscreen`, `do_damage_immediately`, `do_not_clear_placeholder`, `dont_orient`, `dont_sink`, `dont_visualize_ai`, `easing`, `empty_animation`, `end`, `face_targets`, `face_toss_target`, `fall_from_sky`, `fall_randomize_timing`, `first_castpoint_is_self_damage_only`, `fixed_jump_height`, `fixed_jump_speed`, `four_way_animations`, `full_jump_animation`, `full_jump_sync_frames`, `full_jump_windup_frames`, `fx_is_placeholder_animation`, `fx_random_flip`, `grab_animation`, `hang_time`, `ignore_slowtiles`, `jump_attack_animation`, `jump_height_multiplier`, `jump_speed_multiplier`, `jump_start_animation`, `land_animation`, `lob`, `lob_height`, `lob_speed`, `lob_yoff`, `lock_orientation_during_dash`, `loop`, `mask_center`, `mask_extent`, `max_range`, `max_throw_height`, `max_tiles_single_loop`, `min_range`, `min_throw_height`, `miss_particle`, `miss_random_delay`, `mode`, `move_end_animation`, `move_speed_multiplier`, `move_speed_sync_frames`, `move_start_animation`, `movieclip`, `name`, `no_horizontal_flip`, `no_splatter`, `non_blocking_animations`, `othercat_placeholder_available`, `override_portrait`, `particle`, `particle_mat`, `piece_alt_frame`, `precast_delay`, `preturn_animation`, `prime_animation`, `primed_alt_animation`, `projectile`, `projectile_spawn_offset`, `pseudoprojectile`, `random_delay`, `randomize_starting_frame`, `reverse_orientation`, `rocket_swirl`, `scale`, `self_damage_mid_port`, `shade_occluded_objects`, `shadow`, `shadow_size`, `show_infinity_damage_warning`, `single_projectile`, `spawn_offset`, `spawnin_animation`, `speed`, `start`, `status_display_count_max`, `sync_frames`, `sync_speed`, `throw_speed`, `tint`, `tooltip`, `uifloaters_offset`, `uncatchable`, `use_directional_animations`, `use_hit_alts`, `use_origin_offsets`, `use_placeholder`, `use_projectile`, `use_projectile_spawn_offset`, `use_rotation`, `use_rotation_once`, `use_super_armor`, `visual_delay_but_simultaneous_damage`, `water_mask`

### `innate_passives` (from `Cat_Classes.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddStartingMana`, `SpawnOnBattleStart`, `TinkererBasicAttackSwitching`

### `meta` (from `Cat_Classes.md`)

**In split file but NOT in Master (2):** `description`, `{Graphics Keys}`

**In Master but NOT in split file (9):** `delay_enable_tooltips`, `house_shop`, `keeper`, `movieclip`, `npc_script`, `pick_n`, `shopkeeper_fights`, `treasure_room`, `welcome_message`

### `AddStatusToBasicAttack` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (43):** `ApplyStatusIfCrit`, `ApplyToSource`, `BigSplashDamage`, `Bleed`, `Blind`, `BounceObject`, `Bruise`, `BurgleCoin`, `Burn`, `ChangeTile`, `Charmed`, `Conditional_Adjacent`, `Conditional_Ally`, `Conditional_Enemy`, `Conditional_HasTag`, `Conditional_Shielded`, `Conditional_SourceHasTag`, `Confusion`, `DamageOrHealConditionally`, `DistanceBonusDamage`, `Else`, `Fear`, `Freeze`, `KnockOutCoin`, `Knockback`, `Leech`, `Leeches`, `LuckUp`, `Madness`, `MagicWeakness`, `ManaLeeches`, `OverrideChainKnockback`, `OverrideChainKnockbackDamage`, `Piercing`, `Poison`, `Rot`, `Slow`, `SoulLink`, `SpawnBearTrapOnMiss`, `SplashDamage`, `SpreadDisease`, `Stun`, `Weakness`

### `AddStatusToBasicMeleeAttack` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Bruise`, `Confusion`, `FaceAway`, `SpreadDisease`, `Stun`

### `AddTemporaryEffectsToBasicAttack` (from `Cat_Mutations.md`)

**In Master but NOT in split file (1):** `CastAgain`

### `Conditional_FirstApplicationThisTurn` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FillMana`, `ManaGain`, `TakeExtraTurn`

### `Conditional_GoodRoll` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseRandomSpell_Madness`

### `Conditional_RandomChance` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ApplyPassives`, `AutoReanimate`

### `CounterAttack` (from `Cat_Mutations.md`)

**In Master but NOT in split file (3):** `melee_only`, `ranged_only`, `without_orienting`

### `KnockUpAndAway` (from `Cat_Mutations.md`)

**In Master but NOT in split file (4):** `circular_variance`, `displace`, `height`, `self_damage`

### `MeleeRevengeDamage` (from `Cat_Mutations.md`)

**In split file but NOT in Master (4):** `knockback`, `type`, `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Poison`, `SpreadDisease`, `Weakness`, `effects`, `elements`

### `MoveWhenDamaged` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `move_ability`

### `PassiveWhenAffectedByElement` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhenAtFullMana` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddMovement`, `AddStatusToBasicAttack`, `Brace`, `Flying`, `ReplaceBasicMove`

### `PassiveWhileHasStatus` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ROOT` (from `Cat_Mutations.md`)

**In split file but NOT in Master (15):** `attack`, `cha`, `con`, `dex`, `divine_shield`, `int`, `lck`, `override_move`, `shield`, `spd`, `speed`, `str`, `tag`, `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `RandomStatusFromPool` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (37):** `AllStatsUp`, `Bleed`, `BleedThorns`, `Blind`, `Brace`, `Bruise`, `Burn`, `Charge`, `Charmed`, `Confusion`, `ConstitutionUp`, `DiminishingHealthRegen`, `DivineShield`, `Fear`, `Freeze`, `Immobile`, `KineticSpikes`, `Madness`, `MagicWeakness`, `Marked`, `MoveQuivered`, `ObjectOnHitCharacter`, `Petrify`, `Poison`, `Quivered`, `Reflect`, `Shield`, `Sleep`, `Slow`, `SpawnCoinAnywhere`, `SpeedUp`, `StatusGroup`, `StrengthUp`, `Stun`, `Tarred`, `Thorns`, `Weakness`

### `RevengeDamage` (from `Cat_Mutations.md`)

**In split file but NOT in Master (3):** `damage`, `type`, `{Damaging Keys}`

**In Master but NOT in split file (2):** `effects`, `knockback`

### `SpawnEachTurn` (from `Cat_Mutations.md`)

**In Master but NOT in split file (1):** `number`

### `SpawnExtraThingsOnBattleStart` (from `Cat_Mutations.md`)

**In Master but NOT in split file (2):** `tile`, `trap`

### `SpawnThingOnDamage` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `chance`

**In Master but NOT in split file (2):** `consider_all_layers`, `spawn_on_death_hit`

### `StatusEachRoundEnd` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddRandomEliteBuff`, `DoDamage`, `UseAbility`

### `StatusEachTurnBegin` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Conditional_BadRoll`, `Conditional_GoodRoll`, `Fear`, `FillMana`, `ForceUseAbility`, `IntelligenceUp`, `RandomStatUp`

### `StatusEachTurnEnd` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `EmptyMana`, `ForceUseAbility`, `IntelligenceUp`, `KineticSpikes`, `NonStackingDivineShield`, `ObjectOnHitCharacter`, `PermanentMadness`, `RangeUp`, `SpeedUp`, `StrengthUp`, `UseAbility_Madness`

### `StatusEveryXSpellCasts` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `ReduceManaCost`, `RepairWeapon`, `RepairWeaponCondition`, `SpellDamageUp`

### `StatusEveryXSpellCastsEachTurn` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `StatusIfDidntMove` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charge`

### `StatusIfUnusedMovePoints` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `Brace`, `ConstitutionUp`, `HealthGain`, `ManaGain`, `MoveQuivered`, `Shield`

### `StatusKilledCharacters` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AutoReanimate`, `Conditional_Ally`

### `StatusOnAllyCatDeath` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `FillMana`, `HealthGain`, `PercentHeal`, `TakeExtraTurn`

### `StatusOnBattleEnd` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `CureDisease`, `FindItemFromPool`, `NextBattleStatus`, `PermanentConstitution`, `PermanentIntelligence`, `PermanentSpeed`, `PermanentStrength`, `RandomMutation`, `RandomPermanentStat`, `even_if_dead`

### `StatusOnCastSpell` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Charge`, `CurrentWeaponDamageUp`, `HealthGain`

### `StatusOnDie` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `Conditional_RandomChance`, `CreateGlobalModifiers`, `FindItemFromPool`, `GainCoinsRange`, `RandomMagicMissile`, `RandomStatusFromPool`, `RemoveAmbientLightEffects`, `RemoveGlobalModifiers`, `ScatterCoins`, `StackingSandstorm`

### `StatusOnEatFood` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Cleanse`, `IntelligenceUp`, `RandomStatUp`, `StrengthUp`

### `StatusOnEndMove` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceAttack`

### `StatusOnKill` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `Conditional_FirstApplicationThisTurn`, `DamageUp`, `EquipPermanentItem`, `HealthGain`, `LuckUp`, `RandomStatUp`, `RefreshActPoints`, `RefreshMovePoints`, `SpeedUp`, `Stealth`, `StrengthUp`, `TakeBonusTurnWithStatus`

### `StatusOnTookDamage` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (18):** `Conditional_HasStatus`, `ConstitutionUp`, `Craft`, `DamageUp`, `DiminishingHealthRegen`, `Else`, `IntelligenceUp`, `MovementUp`, `RandomInjury`, `RandomStatUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `StrengthUp`, `TempDamageUp`, `TempMovement`, `Temporary`, `Thorns`

### `StatusOnTookDamageFromAbility` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DiminishingHealthRegen`, `Shield`

### `effects` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `passives` (from `Cat_Mutations.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (424):** `AbilityOnBattleStart`, `AbilityReaction`, `AbilityWhenTaggedCharacterMovesNear`, `AbsorbManaAura`, `AddAllyNeighborsToAttackRange`, `AddBonusMeleeRange`, `AddBonusRange`, `AddCorpseHealth`, `AddCritMultiplier`, `AddDamageToBasicAttack`, `AddDamageToElementDamage`, `AddElementsToBasicAttack`, `AddHiddenTag`, `AddInitiative`, `AddKnockbackDamage`, `AddLevelUpRerolls`, `AddLevelUpStatMultiplier`, `AddManaRegen`, `AddMovement`, `AddPassiveToSpawnedRocks`, `AddPassivesToCharmed`, `AddPassivesToMinions`, `AddPassivesToSummonAbilityMinions`, `AddSelfStatusToBasicAttack`, `AddSelfStatusToWeapons`, `AddSpellDamage`, `AddStartingMana`, `AddStatusToAllDamage`, `AddStatusToBasicAttack`, `AddStatusToBasicAttackWithCooldown`, `AddStatusToBasicMeleeAttack`, `AddStatusToElementAbilities`, `AddStatusToElementDamage`, `AddStatusToExplosions`, `AddStatusToFirstBasicAttack`, `AddStatusToMeleeDamage`, `AddStatusToReceivedDamage_ExcludeStatuses`, `AddStatusToTrampleDamage`, `AddStatusToWeapons`, `AddStatusesIfPersistentWeatherElement`, `AddStatusesToReceivedElementalDamage`, `AddTag`, `AddTemporaryEffectsToBasicAttack`, `AddUnfilledMaxHealth`, `AddWeaponScaling`, `AfterImage`, `AllStatsUp`, `AllowPassTurn`, `AllyBonusAbilityAura`, `AllyDamageReaction`, `AllyDamageReduction`, `AllyHealthRegenAura`, `AllyManaRegenAura`, `AllyMoveAbilityAura`, `AllyMultiplyKnockbackDamage`, `AlphaTurns`, `AlternateCraftingPools`, `AmplifyKnockback`, `AmplifyPositiveStatus`, `AmplifyStatus`, `ApplyStatusesToRandomEnemiesEachTurn`, `Autism`, `AutoCritLowDamage`, `AutoEquipConsumables`, `AutocastEachRound`, `AutocastEachTurn`, `AutocastEachTurnBegin`, `BackstabCritChance`, `BackstabWeakness`, `BasicAttackAOEBonus`, `BasicAttackCritChance`, `BasicAttackDamageMultiplier`, `BasicAttackStatusCarefulness`, `BlacklistPickupType`, `BlastResistance`, `Bleed`, `BleedThorns`, `BonusAbility`, `BonusFoodEachBattle`, `BoobyTrapItems`, `BoostAllyStatsOnDeath`, `BoostDamageAura`, `BoostHeals`, `BoostRangeAura`, `BoostWeaponDamage`, `BouncyProjectiles`, `Brace`, `BraceForEachNeighboringEnemy`, `Bruise`, `BuffImmunity`, `Burn`, `CCImmunity`, `CanRemoveCursedItems`, `CantDodge`, `CapDamageFromAllies`, `CapMovementAbilityRange`, `CatAPultAnimation`, `CatchProjectiles`, `ChainKnockback`, `ChanceToBackflip`, `ChanceToBlockAndCounter`, `ChanceToRevive`, `ChangeTauntPriority`, `CharmAllFlies`, `ClassManaCostReduction`, `CobraReflex`, `CoinsAddDamage`, `CollectPickupsOnBattleEnd`, `Conductor`, `ConfusionEffectOnTaggedAbilities`, `ConjureCastSpellsForAllies`, `ConsumableEffectsMultiplierBonus`, `ConsumablesInfiniteRange`, `ConsumablesMeleeRange`, `CounterAttack`, `CritChanceUp`, `CritsApplyStatus`, `DamageEnemiesOnHeal`, `DamageEnemiesOnKill`, `DamageIfDidntUseSpecificAbility`, `DamageNeighborTilesWhenCastSpell`, `DamageNeighborsAfterMove`, `DamageNeighborsOnEndMove`, `DamageReductionAura`, `DamageUp`, `DeathChill`, `DeathRattle`, `DebuffImmunity`, `DejaVu`, `DepressionAura`, `Diabetes`, `DirtyClaws`, `DisableAbilities`, `DisableAbilitiesWithTag`, `DodgeChance`, `Doomed`, `DoubleCastWeapons`, `DukeOfFlies`, `Dyslexia`, `EMP`, `ElementImmune`, `ElementalAttunement`, `ElementalManaCostReduction`, `Empath`, `EnemiesGetPickupsKnockedOut`, `EnergyStorm`, `EquipTemporaryItem`, `EquipmentPassiveMultiplierBonus`, `EquipmentSetBonusBonus`, `EscapeSequence`, `Eternal`, `ExhaustionRoundChange`, `ExplodeOverkilledEnemies`, `ExtraBasicAttacks`, `ExtraBasicMoves_Status`, `ExtraInjuryOnDeath`, `ExtraMovePoints`, `ExtraStatusWhenDealingDamage`, `ExtraWeaponAttacks`, `FaceArmorPassiveMultiplierBonus`, `FaceShield`, `FamiliarSecondaryDamageImmunity`, `FlowerPowerAuraBrace`, `FlowerPowerAuraStrength`, `FlowersOnEndTurn`, `FlyDamageIncrease`, `Flying`, `FollowUp`, `ForceSpecificInjury`, `ForceUseAbility`, `FreePathfindElement`, `FreeSpellsAtFullMana`, `FreezePiercing`, `FrontstabBasicAttackCritChance`, `FullHeal`, `FullHealthCritChance`, `FullPower`, `FurnitureStats`, `GainExtraShield`, `GravityWell`, `HPGainBlock`, `HeadArmorPassiveMultiplierBonus`, `HealDamagesEnemies`, `HealsAlsoRegenMana`, `HealsCanRevive`, `HealthRegenUp`, `HolyShieldTransferToTaggedMinions`, `HouseFoodRequirementMultiplier`, `Hypomania`, `IgnoreTiles`, `ImmortalLeeches`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `IncreaseHealingSpellRange`, `IncreaseSpellRange`, `InfiniteRebirth`, `InnateElement`, `InvertBrainFaction`, `KillsHeal`, `KillsToMeat`, `KnockbackImmunity`, `LateBloomer`, `LevelUpClassOverride`, `LightningAspectCharge`, `LightningRod`, `LimitDamage`, `LimitHeal`, `LimitSelfKnockbackDamage`, `LimitedTileTrail`, `LineOfSightTrueSightAura`, `LobbedHook`, `LowHealthAllyDodgeChanceAura`, `Madness`, `MakeBasicAttackPassThroughThings`, `MakeSpellsRequireCharge`, `ManaCostReductionTagged`, `ManaRegenMultiplierIfManaEmpty`, `MaxAccuracy`, `MaxStartingMana`, `MegaMinions`, `MeleeRevengeDamage`, `Metal`, `MetalDetector`, `MinimumTech`, `MissChance`, `MoveAndUseAbilityEachTurnBeginIfPossible`, `MoveAwayFromDamageSource`, `MoveQuivered`, `MoveSpeedMultiplier`, `MoveTowardsDamageSource`, `MoveWhenDamaged`, `MovementReaction`, `MulticlassLevelUp`, `NeckArmorPassiveMultiplierBonus`, `NoManaRegen`, `NoReflection`, `NubbyTossPriority`, `NumbingLeeches`, `OverhealGainsBothShield`, `OverrideBasicAttack`, `OverrideMaxHealth`, `OverrideMaxMana`, `OverridePalette`, `Paranoia`, `ParasitesArentCursed`, `PassiveAfterXKills`, `PassiveAtFullHealth`, `PassiveAtHealthThreshold`, `PassiveAtInjuryThreshold`, `PassiveAtStatThreshold`, `PassiveIfAllArmorEmpty`, `PassiveIfEmptyFace`, `PassiveIfEmptyHead`, `PassiveIfEmptyNeck`, `PassiveLevelScaledStatus`, `PassiveLevelUpAtCombatEnd`, `PassiveUntilCastSpell`, `PassiveUntilGetKill`, `PassiveWhenAffectedByElement`, `PassiveWhenAtFullMana`, `PassiveWhenTheAlpha`, `PassiveWhileInMonkMeleeStance`, `PassiveWhileInMonkRangedStance`, `PassiveWhilePreviewingMonkRangedStance`, `PassiveWhileWearingMetal`, `PermanentImmobile`, `PermanentItems`, `PermanentKitten`, `PermanentMadness`, `Poison`, `PoisonThorns`, `PoopWhenHit`, `ProtectTargetedAllies`, `Quiver`, `Quivered`, `RandomPassivePool`, `RangedTrueShot`, `RealTimePressure_OneUnit`, `ReceivedStatusReplacement`, `RemoveLineOfSightRestrictions`, `RemoveOncePerFightRestriction`, `ReplaceBasicAttack`, `ReplaceBasicAttackWhenCastable`, `ReplaceBasicAttackWhenDead`, `ReplaceBasicMove`, `ReplaceSpawnedObjects`, `RevengeDamage`, `ReviveOnWin`, `RobotsInheritArmor`, `RockDetector`, `ScaledStatusOnBleedDamage`, `ScaledStatusOnOverMana`, `ScaledStatusOnSpendMana`, `SchrodingerDisorder`, `Scleroderma`, `SecurityBotProtect`, `SelfDamageWhenDealDamage`, `SetDefaultFacePassive`, `SetSpellCosts`, `ShareHealthRegen`, `SharePickups`, `ShoulderCheck`, `ShovingMatch`, `ShowHiddenThings`, `SizeScale`, `Slow`, `SmallEnemiesIgnoreYou`, `SmallRockBehavior`, `SmiteEnemiesWhoKill`, `SpawnCatCopyOnBattleStart`, `SpawnCreepOnHit`, `SpawnEachTurn`, `SpawnObjectOnPopCorpse`, `SpawnOnBattleStart`, `SpawnOnBattleStartRandomEmptyTile`, `SpawnThingOnDamage`, `SpawnThingOnDeath`, `SpecialFriends`, `SpeedUp`, `SplittableMove`, `SpreadExtraDebuffs`, `SpreadPainBonus`, `StatMinimum`, `StatsAtLowHealth`, `StatusAdjacentOnTheirTurnBegin`, `StatusAfterCastSpell`, `StatusAlliesOnBattleStart`, `StatusAlliesOnDeath`, `StatusAlliesOnGainCoins`, `StatusAlliesOnKill`, `StatusAllyWhenAllySpendsMana`, `StatusAnyCatAllyWhoKills`, `StatusDamagers`, `StatusEachTurnBegin`, `StatusEachTurnEnd`, `StatusEachTurnEndForEachTurn`, `StatusEachTurnEndPerEnemyKill`, `StatusEnemiesOnDeath`, `StatusEveryXSpellCasts`, `StatusEveryXTurnBegins`, `StatusIfBattleAlreadyBegan`, `StatusIfUnusedMovePoints`, `StatusImmunity`, `StatusKilledCharacters`, `StatusKillers`, `StatusOnAllyCatDeath`, `StatusOnAnyDeath`, `StatusOnBattleEnd`, `StatusOnBattleEndIfKillThresholdMet`, `StatusOnBattleStart`, `StatusOnBreakItem`, `StatusOnCastSpell`, `StatusOnCollectPickup`, `StatusOnCrit`, `StatusOnDealtDamage`, `StatusOnDealtDamageThreshold`, `StatusOnEatFood`, `StatusOnEatPill`, `StatusOnEndMove`, `StatusOnGainCoins`, `StatusOnGainShield`, `StatusOnHeal`, `StatusOnHealed`, `StatusOnKill`, `StatusOnKillEnemy`, `StatusOnLoseShield`, `StatusOnOverHealed`, `StatusOnOverMana`, `StatusOnPickupCoins`, `StatusOnPopCorpse`, `StatusOnStanceSwitch`, `StatusOnTakeHealthDamage`, `StatusOnTookDamage`, `StatusOnTookDamageFromAbility`, `StatusOnTookDamageFromEnemyAbility`, `StatusOnTriggerTrap`, `StatusOnTurnEndIfCastNSpells`, `StatusOnTurnEndIfDidntCastAbilityTypes`, `StatusOnTurnEndIfManaExact`, `StatusOnTurnEndIfManaOrHealthExact`, `StatusOnUseAbilityWithTag`, `StatusOnUseBasicAttack`, `StatusOnUseElementAbility`, `StatusPerInjury`, `StatusReplacement`, `StatusThingsKnockedBack`, `StatusWhenAllySpendsMana`, `Stealth`, `StrengthForEachNeighboringEnemy`, `StrengthInNumbersAura`, `StrengthUp`, `StrictLimitDamage`, `Study`, `TaggedPickupEffectReplacement`, `TauntAlways`, `TauntAtFullHealth`, `Tech`, `TempInitiativeChange`, `TheHunger`, `Thorns`, `TileDamageMultiplier`, `TileTrail`, `TourettesMeows`, `TowerDefense`, `TowerDefenseReflex`, `Trample`, `TrapEffectsMultiplier`, `TrinketActiveEffectsMultiplierBonus`, `TrinketPassiveMultiplierBonus`, `Triskaidekaphobia`, `UncappedHP`, `UncappedMana`, `UpgradeLevelUpClassActives`, `UpgradeLevelUpClassPassives`, `UpgradeSpawnedPickups`, `Vegan`, `Vengeful`, `WaterWalk`, `Weakness`, `WeaponActiveEffectsMultiplierBonus`, `WeaponCountsAsBasicAttack`, `WeaponDamageMultiplierBonus`, `WeaponPassiveMultiplierBonus`, `WobblyCat`

### `AbilityHealthThreshold` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `aux`, `threshold`

### `AbilityReaction` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (9):** `backstabs_only`, `cancel_knockback`, `enemies_only`, `even_on_0_damage`, `even_on_0_damage_if_knockback`, `match_knockback_direction`, `only_when_not_your_turn`, `ranged_only`, `verify_target`

**In Master but NOT in split file (1):** `chance`

### `AddStatusToBasicAttack` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (43):** `ApplyStatusIfCrit`, `ApplyToSource`, `BigSplashDamage`, `Bleed`, `Blind`, `BounceObject`, `Bruise`, `BurgleCoin`, `Burn`, `ChangeTile`, `Charmed`, `Conditional_Adjacent`, `Conditional_Ally`, `Conditional_Enemy`, `Conditional_HasTag`, `Conditional_Shielded`, `Conditional_SourceHasTag`, `Confusion`, `DamageOrHealConditionally`, `DistanceBonusDamage`, `Else`, `Fear`, `Freeze`, `KnockOutCoin`, `Knockback`, `Leech`, `Leeches`, `LuckUp`, `Madness`, `MagicWeakness`, `ManaLeeches`, `OverrideChainKnockback`, `OverrideChainKnockbackDamage`, `Piercing`, `Poison`, `Rot`, `Slow`, `SoulLink`, `SpawnBearTrapOnMiss`, `SplashDamage`, `SpreadDisease`, `Stun`, `Weakness`

### `AddStatusToReceivedDamage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Else`

### `AddStatusToSpells` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LeechPercent`

### `AddStatusToTrampleDamage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Cleave`

### `AddStatusToWeapons` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Bleed`, `Cleave`, `LeechPercent`, `PullSourceToKnockbackImmuneTarget`

### `AddTemporaryEffectsToBasicAttack` (from `Characters_and_Bosses.md`)

**In Master but NOT in split file (1):** `CastAgain`

### `AdventureTokenPassivePool` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (12):** `StacyMutant_Brace`, `StacyMutant_Counter`, `StacyMutant_Damage`, `StacyMutant_DoubleHead`, `StacyMutant_Fire`, `StacyMutant_Health`, `StacyMutant_Holy`, `StacyMutant_Ice`, `StacyMutant_Lightning`, `StacyMutant_Mirror`, `StacyMutant_Speed`, `StacyMutant_Thorns`

### `Alert` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `AllAlive` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `AutocastEachRound` (from `Characters_and_Bosses.md`)

**In Master but NOT in split file (1):** `force_display_name`

### `BellyFull` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Big` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `follow_character_tag`, `passives`, `position`

### `BigHolding` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `BigHoldingCat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Bishop` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `name`, `passives`, `tooltip`, `uifloaters_offset`

### `BlackHole` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `Bomb` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Boris` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `BossRewards` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `common`, `rare`

### `Bully` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Cat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `CatPartsTransform` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (4):** `eyebrow1`, `eyebrow2`, `mouth`, `palette`

### `CaveBaby` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveMan` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveManSpear` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveWoman` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveWomanHasCat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `Charging` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Close` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Conditional_BadRoll` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Temporary`

### `Conditional_GoodRoll` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseRandomSpell_Madness`

### `Conditional_HasKnockback` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `KnockUpAndAway`, `RemoveKnockback`, `TempPassiveUntilSettled`

### `Conditional_IsPhysicalAttack` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `KnockUpAndAway`, `RemoveKnockback`, `TempPassiveUntilSettled`

### `Consumed` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (12):** `do_not_pop_corpse`, `drop_body_ability`, `drop_on_death`, `drop_on_self_death`, `extra_statuses`, `force_contact`, `instant`, `kill_on_consume`, `mount_mode`, `struggle_ability`, `use_placeholder`, `wet`

### `CounterAttack` (from `Characters_and_Bosses.md`)

**In Master but NOT in split file (3):** `chance`, `melee_only`, `ranged_only`

### `CreateGlobalModifiers` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Global Modifier Keys}`

**In Master but NOT in split file (4):** `BloodRain`, `LowerAmbientLight`, `NextPlayerCatTakesExtraTurn`, `NoCorpses`

### `Cultist` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `DeathRattle` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (5):** `cancel_knockback`, `immediate`, `is_dying_animation`, `must_target_killer`, `target_killer`

### `Default` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `set_house`, `unlock_room`

### `Default_Ceiling` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Default_Ground` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Die` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `DiesToElement` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `instant`

### `Down` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `DualSword` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `move_speed_multiplier`, `passives`, `tooltip`

### `DualSword_Primed` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `move_speed_multiplier`, `passives`, `tooltip`

### `Dumb` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Else` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (6):** `CaptureFamiliar`, `FactionConversion`, `Fear`, `Marked`, `PermanentCharm`, `TempSpeedUp`

### `Explody` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Explosive` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FightPhase` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FinalBossBecomeTheChild` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (3):** `GlobalSpawnCharacter`, `PlayBackground`, `SwitchMusic`

### `FinalBossHitCountdownBoris` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `FinalBossHitCountdownExplosive` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `Fire` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (3):** `ai`, `attack`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `FireFull` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Flop` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Flop2` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FlushBubs` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FlushHost` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FlushNettle` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ForceUseAbility` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `show_name`

**In Master but NOT in split file (1):** `chance`

### `FormChangeHealthThreshold` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `FormChangeOnElementInfluence` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `particle`

### `FormChanger` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (3):** `{Graphics Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Die`, `Rain`, `passives`, `uifloaters_offset`

### `Full` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Grown` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `uifloaters_offset`

### `GuaranteedJackpot` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Guarding` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HalfDead` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HasCat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HasDeadCat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Headless` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HitlerExecute` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `Holding` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Holy` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `animation_suffix`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `FlatLeech`

### `HumanDead` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `tooltip`

### `InfiniteRebirth` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `immediate`

**In Master but NOT in split file (1):** `TempSpeedUp`

### `InitialPhase` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Insane_Ceiling` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Insane_Ground` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `JohnnyBubs` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `JohnnyHost` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `JohnnyNettle` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Joystick` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `KnockUpAndAway` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (3):** `circular_variance`, `height`, `self_damage`

### `Lifted` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Lit` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `MeleeRevengeDamage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (3):** `knockback`, `type`, `{Damaging Keys}`

**In Master but NOT in split file (4):** `Poison`, `SpreadDisease`, `Weakness`, `effects`

### `ModularPickup` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Cleanse`

### `MouthFull` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `MoveTowardsDamageSource` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (8):** `ability`, `can_move_zero`, `check_has_status`, `check_in_form`, `do_not_move_on_top`, `face_towards_after`, `ignore_tagged_sources`, `move_short`

### `MoveWhenDamaged` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `move_ability`

### `MovementReaction` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (5):** `blind_spot`, `forward_only`, `objects_too`, `on_self_move_too`, `self_move_exclude_self_abilities`

### `Mutant` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `move_speed_multiplier`, `name`, `passives`, `tooltip`

### `NeutronStar` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `NonCat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `Normal` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `NormalFull` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `NotPriming` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Nothing` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `Nuke` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Obey` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OffScreen` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OneAlive` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OneEye` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Open` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OpenCat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Out` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveGroup` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `CharismaUp`, `IntelligenceUp`, `SetDefaultFace`, `SpeedUp`

### `PassiveWhenAffectedByElement` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhenDead` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddStatusToTrampleDamage`, `AutocastEachRound`, `StatusEachRoundEnd`, `StatusEachTurnBegin`

### `PassiveWhileHasStatus` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhileNotHasStatus` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Possessing` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Primed` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Priming` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Pulp2` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp3` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp4` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp5` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp6` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp7` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `ROOT` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (23):** `abilities`, `ai`, `ai_if_spawned_as_enemy`, `alt_spawn_pool`, `animation_suffix`, `attack`, `brain`, `consider_spells`, `damage_instance`, `decision_weights`, `end_turn_on_formswitch`, `equipment`, `graphics`, `initial_form`, `move_weights`, `partial_animation_suffix`, `pattern`, `properties`, `sound`, `stats`, `variant_of`, `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `Rage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `move_speed_multiplier`, `passives`

### `Rain` (from `Characters_and_Bosses.md`)

**In Master but NOT in split file (5):** `adventure_weather`, `ambient_sound`, `particles`, `prewarm`, `skybox_frame`

### `RandomPassivePool` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PassiveGroup`

### `RandomStatusFromPool` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (37):** `AllStatsUp`, `Bleed`, `BleedThorns`, `Blind`, `Brace`, `Bruise`, `Burn`, `Charge`, `Charmed`, `Confusion`, `ConstitutionUp`, `DiminishingHealthRegen`, `DivineShield`, `Fear`, `Freeze`, `Immobile`, `KineticSpikes`, `Madness`, `MagicWeakness`, `Marked`, `MoveQuivered`, `ObjectOnHitCharacter`, `Petrify`, `Poison`, `Quivered`, `Reflect`, `Shield`, `Sleep`, `Slow`, `SpawnCoinAnywhere`, `SpeedUp`, `StatusGroup`, `StrengthUp`, `Stun`, `Tarred`, `Thorns`, `Weakness`

### `ReflectProjectiles` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `self_damage`

### `ReplaceBrain` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `pattern`

### `RevengeDamage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `damage`, `type`

**In Master but NOT in split file (1):** `effects`

### `Robot` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `alternate_energized_effect`

**In Master but NOT in split file (1):** `allow_energize_self`

### `SecurityBotProtect` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (3):** `enemies_only`, `not_on_kill`, `tag_restriction`

### `Sitting` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SmallHolding` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SmallHoldingCat` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SpawnThingOnDamage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (4):** `auto_cast`, `chance`, `coins`, `melee_ability_only`

### `SpawningPhase` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SquirrelForm` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `tooltip`

### `StacyMutant_Brace` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Brace`, `CatPartsTransform`

### `StacyMutant_Counter` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddStatusToBasicAttack`, `CatPartsTransform`, `CounterAttack`

### `StacyMutant_Damage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddDamage`, `AddMaxHealth`, `CatPartsTransform`

### `StacyMutant_DoubleHead` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CatPartsTransform`, `ExtraDispersedTurns`

### `StacyMutant_Fire` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `CatPartsTransform`, `ElementImmune`, `ReplaceBasicAttack`, `ReplaceBrain`

### `StacyMutant_Health` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddMaxHealth`, `AddSpeed`, `CatPartsTransform`, `SizeScale`

### `StacyMutant_Holy` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CatPartsTransform`, `DivineShield`

### `StacyMutant_Ice` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddMovement`, `CatPartsTransform`, `ElementImmune`, `ReplaceBasicAttack`, `ReplaceBrain`

### `StacyMutant_Lightning` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `CatPartsTransform`, `ElementImmune`, `ReplaceBasicAttack`, `ReplaceBrain`

### `StacyMutant_Mirror` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `CatPartsTransform`, `ReflectProjectiles`, `StatusEachTurnEndForEachTurn`

### `StacyMutant_Speed` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddDamage`, `AddSpeed`, `CatPartsTransform`, `SizeScale`

### `StacyMutant_Thorns` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CatPartsTransform`, `Thorns`

### `Standing` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Standing2` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Start_Ceiling` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `StatusAfterXTurns` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `StatusCollector` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Poison`, `Slow`, `StrengthUp`

### `StatusEachTurnBeginIfHasStatus` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `DamageUp`, `HealthGain`, `animation`

### `StatusEachTurnEnd` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `EmptyMana`, `ForceUseAbility`, `IntelligenceUp`, `KineticSpikes`, `NonStackingDivineShield`, `ObjectOnHitCharacter`, `PermanentMadness`, `RangeUp`, `SpeedUp`, `StrengthUp`, `UseAbility_Madness`

### `StatusEachTurnEndForEachTurn` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `StatusEachTurnEndIfEnabledAtStartOfTurn` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `StatusGroup` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `DexterityUp`, `LuckUp`, `SpawnCoinAnywhere`, `SpeedUp`

### `StatusOnDie` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `Conditional_RandomChance`, `CreateGlobalModifiers`, `FindItemFromPool`, `GainCoinsRange`, `RandomMagicMissile`, `RandomStatusFromPool`, `RemoveAmbientLightEffects`, `RemoveGlobalModifiers`, `ScatterCoins`, `StackingSandstorm`

### `StatusOnEndMove` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceAttack`

### `StatusOnEnemyConfused` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ImmediateUseAbility`

### `StatusOnGainCoins` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DivineShield`, `RandomStatusFromPool`

### `StatusOnKill` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `Conditional_FirstApplicationThisTurn`, `DamageUp`, `EquipPermanentItem`, `HealthGain`, `LuckUp`, `RandomStatUp`, `RefreshActPoints`, `RefreshMovePoints`, `SpeedUp`, `Stealth`, `StrengthUp`, `TakeBonusTurnWithStatus`

### `StatusOnSpawnIn` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CaptureFamiliar`, `SetHealth`

### `StatusOnTookDamage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (18):** `Conditional_HasStatus`, `ConstitutionUp`, `Craft`, `DamageUp`, `DiminishingHealthRegen`, `Else`, `IntelligenceUp`, `MovementUp`, `RandomInjury`, `RandomStatUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `StrengthUp`, `TempDamageUp`, `TempMovement`, `Temporary`, `Thorns`

### `StatusOnTookDamageFromAbility` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DiminishingHealthRegen`, `Shield`

### `StatusOverlappingCharactersAndDie` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Poison`

### `StatusWhenStatusCompletelyRemoved` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseAbility`

### `Stop` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SwitchMusic` (from `Characters_and_Bosses.md`)

**In Master but NOT in split file (1):** `crossfade_speed`

### `SwordAndShield` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SwordAndShield_Primed` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TVBotScreen` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `Die`

### `Tar` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TarFull` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TempPassiveUntilSettled` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `LimitHeal`, `MeleeRevengeDamage`

### `ThrobBubs` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ThrobHost` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ThrobNettle` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TransformInXTurns` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `TransformOnStatusThreshold` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `Transformed` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Turtled` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TwoAlive` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TwoEyes` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Unlit` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Up` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `tooltip`

### `Washed` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Washer` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `Water` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `partial_animation_suffix`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AOEPuddle`

### `WereMan` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `Zealot` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `ZealotBomb` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `abilities` (from `Characters_and_Bosses.md`)

**In Master but NOT in split file (1):** `spell0`

### `active` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `additional_statuses` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PermanentMadness`

### `ally_rewards` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_GoodRoll`, `FindItemFromPool`, `RandomStatusFromPool`

### `alternate_energized_effect` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `FormChange`, `SpellDamageUp`

### `damage_instance` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (39):** `HealthRegenUp`, `accuracy`, `ai_base_score`, `blocked_damage`, `blocked_multiplier`, `can_collect_pickups`, `can_instapop`, `can_revive`, `cant_miss`, `contact_requires_adjacency`, `crit_chance`, `custom_additional_ai_weight`, `damage`, `damage_shield_only`, `disallow_modifications`, `effects`, `elements`, `faction`, `final_hit_bonus_damage`, `force_adjacent_and_diagonal_contact`, `force_no_contact`, `force_no_knockback`, `force_play_hit_animation`, `heal`, `hint_dont_lowgravboost`, `hit_animation_alt`, `incidentally_collects_pickups`, `knockback`, `layer`, `makes_contact`, `non_lethal`, `override_trample_damage`, `piercing`, `ranged`, `raw_damage`, `raw_heal`, `show_damage_on_0`, `two_way_contact`, `type`

### `default` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (8):** `back`, `ear_rotation`, `eyebrow_rotation`, `eyebrow_up`, `eyes`, `face_offset`, `mouth`, `passives`

### `eat_damage` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (4):** `cant_miss`, `effects`, `makes_contact`, `piercing`

### `effects` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `graphics` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (8):** `dead`, `deadhit`, `dodge`, `dying`, `hit`, `stunned`, `walk`, `weak`

**In Master but NOT in split file (121):** `affected_animation`, `affected_particle`, `air_animation`, `ally_animation`, `always_play_animations`, `animate_name`, `animation`, `animation_in`, `animation_out`, `aoe_spell_on_land`, `apex_distance`, `apex_time`, `area_particle`, `beam_cap`, `beam_clip`, `bounce_on_hit`, `bypass_combatspeed`, `center_particle`, `chain_distance`, `chain_movieclip`, `custom_priming_animation`, `damage_threshold_altanimations`, `darken_screen`, `darken_screen_exclude_characters_on_tile`, `darken_screen_exclude_self`, `darken_screen_start_early`, `dash_animation`, `dash_attack_animation`, `dash_bonk_animation`, `dash_decelerating_animation`, `dash_end_animation`, `dash_start_animation`, `decelerate`, `default_face`, `delay`, `delay_from_map_center`, `delay_from_map_edge`, `delay_from_reverse_map_edge`, `detatched_animation`, `detatched_animation_cutoff`, `detatched_animation_reach`, `do_animation_offscreen`, `do_damage_immediately`, `do_not_clear_placeholder`, `dont_orient`, `dont_visualize_ai`, `easing`, `empty_animation`, `end`, `face_targets`, `face_toss_target`, `fall_from_sky`, `fall_randomize_timing`, `first_castpoint_is_self_damage_only`, `fixed_jump_height`, `fixed_jump_speed`, `full_jump_animation`, `full_jump_sync_frames`, `full_jump_windup_frames`, `fx_is_placeholder_animation`, `fx_random_flip`, `grab_animation`, `hang_time`, `hud_palette`, `ignore_slowtiles`, `jump_attack_animation`, `jump_height_multiplier`, `jump_speed_multiplier`, `jump_start_animation`, `land_animation`, `lob`, `lob_height`, `lob_speed`, `lob_yoff`, `lock_orientation_during_dash`, `loop`, `mask_center`, `mask_extent`, `max_range`, `max_throw_height`, `max_tiles_single_loop`, `min_range`, `min_throw_height`, `miss_particle`, `miss_random_delay`, `mode`, `move_end_animation`, `move_start_animation`, `othercat_placeholder_available`, `palette`, `particle`, `particle_mat`, `portrait_face`, `precast_delay`, `preturn_animation`, `prime_animation`, `primed_alt_animation`, `projectile`, `pseudoprojectile`, `random_delay`, `reverse_orientation`, `rocket_swirl`, `self_damage_mid_port`, `single_projectile`, `spawn_offset`, `speed`, `start`, `sync_frames`, `sync_speed`, `throw_speed`, `uncatchable`, `use_directional_animations`, `use_hit_alts`, `use_origin_offsets`, `use_placeholder`, `use_projectile`, `use_projectile_spawn_offset`, `use_rotation`, `use_rotation_once`, `use_super_armor`, `visual_delay_but_simultaneous_damage`

### `hot` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `name`, `passives`

### `keyword_tooltips` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (4):** `TVBotDie`, `TVBotDumb`, `TVBotObey`, `TVBotStop`

**In Master but NOT in split file (1):** `Weakness`

### `passive` (from `Characters_and_Bosses.md`)

**In Master but NOT in split file (1):** `Metal`

### `passives` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (6):** `ai`, `animation_suffix`, `attack`, `partial_animation_suffix`, `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (424):** `AbilityOnBattleStart`, `AbilityReaction`, `AbilityWhenTaggedCharacterMovesNear`, `AbsorbManaAura`, `AddAllyNeighborsToAttackRange`, `AddBonusMeleeRange`, `AddBonusRange`, `AddCorpseHealth`, `AddCritMultiplier`, `AddDamageToBasicAttack`, `AddDamageToElementDamage`, `AddElementsToBasicAttack`, `AddHiddenTag`, `AddInitiative`, `AddKnockbackDamage`, `AddLevelUpRerolls`, `AddLevelUpStatMultiplier`, `AddManaRegen`, `AddMovement`, `AddPassiveToSpawnedRocks`, `AddPassivesToCharmed`, `AddPassivesToMinions`, `AddPassivesToSummonAbilityMinions`, `AddSelfStatusToBasicAttack`, `AddSelfStatusToWeapons`, `AddSpellDamage`, `AddStartingMana`, `AddStatusToAllDamage`, `AddStatusToBasicAttack`, `AddStatusToBasicAttackWithCooldown`, `AddStatusToBasicMeleeAttack`, `AddStatusToElementAbilities`, `AddStatusToElementDamage`, `AddStatusToExplosions`, `AddStatusToFirstBasicAttack`, `AddStatusToMeleeDamage`, `AddStatusToReceivedDamage_ExcludeStatuses`, `AddStatusToTrampleDamage`, `AddStatusToWeapons`, `AddStatusesIfPersistentWeatherElement`, `AddStatusesToReceivedElementalDamage`, `AddTag`, `AddTemporaryEffectsToBasicAttack`, `AddUnfilledMaxHealth`, `AddWeaponScaling`, `AfterImage`, `AllStatsUp`, `AllowPassTurn`, `AllyBonusAbilityAura`, `AllyDamageReaction`, `AllyDamageReduction`, `AllyHealthRegenAura`, `AllyManaRegenAura`, `AllyMoveAbilityAura`, `AllyMultiplyKnockbackDamage`, `AlphaTurns`, `AlternateCraftingPools`, `AmplifyKnockback`, `AmplifyPositiveStatus`, `AmplifyStatus`, `ApplyStatusesToRandomEnemiesEachTurn`, `Autism`, `AutoCritLowDamage`, `AutoEquipConsumables`, `AutocastEachRound`, `AutocastEachTurn`, `AutocastEachTurnBegin`, `BackstabCritChance`, `BackstabWeakness`, `BasicAttackAOEBonus`, `BasicAttackCritChance`, `BasicAttackDamageMultiplier`, `BasicAttackStatusCarefulness`, `BlacklistPickupType`, `BlastResistance`, `Bleed`, `BleedThorns`, `BonusAbility`, `BonusFoodEachBattle`, `BoobyTrapItems`, `BoostAllyStatsOnDeath`, `BoostDamageAura`, `BoostHeals`, `BoostRangeAura`, `BoostWeaponDamage`, `BouncyProjectiles`, `Brace`, `BraceForEachNeighboringEnemy`, `Bruise`, `BuffImmunity`, `Burn`, `CCImmunity`, `CanRemoveCursedItems`, `CantDodge`, `CapDamageFromAllies`, `CapMovementAbilityRange`, `CatAPultAnimation`, `CatchProjectiles`, `ChainKnockback`, `ChanceToBackflip`, `ChanceToBlockAndCounter`, `ChanceToRevive`, `ChangeTauntPriority`, `CharmAllFlies`, `ClassManaCostReduction`, `CobraReflex`, `CoinsAddDamage`, `CollectPickupsOnBattleEnd`, `Conductor`, `ConfusionEffectOnTaggedAbilities`, `ConjureCastSpellsForAllies`, `ConsumableEffectsMultiplierBonus`, `ConsumablesInfiniteRange`, `ConsumablesMeleeRange`, `CounterAttack`, `CritChanceUp`, `CritsApplyStatus`, `DamageEnemiesOnHeal`, `DamageEnemiesOnKill`, `DamageIfDidntUseSpecificAbility`, `DamageNeighborTilesWhenCastSpell`, `DamageNeighborsAfterMove`, `DamageNeighborsOnEndMove`, `DamageReductionAura`, `DamageUp`, `DeathChill`, `DeathRattle`, `DebuffImmunity`, `DejaVu`, `DepressionAura`, `Diabetes`, `DirtyClaws`, `DisableAbilities`, `DisableAbilitiesWithTag`, `DodgeChance`, `Doomed`, `DoubleCastWeapons`, `DukeOfFlies`, `Dyslexia`, `EMP`, `ElementImmune`, `ElementalAttunement`, `ElementalManaCostReduction`, `Empath`, `EnemiesGetPickupsKnockedOut`, `EnergyStorm`, `EquipTemporaryItem`, `EquipmentPassiveMultiplierBonus`, `EquipmentSetBonusBonus`, `EscapeSequence`, `Eternal`, `ExhaustionRoundChange`, `ExplodeOverkilledEnemies`, `ExtraBasicAttacks`, `ExtraBasicMoves_Status`, `ExtraInjuryOnDeath`, `ExtraMovePoints`, `ExtraStatusWhenDealingDamage`, `ExtraWeaponAttacks`, `FaceArmorPassiveMultiplierBonus`, `FaceShield`, `FamiliarSecondaryDamageImmunity`, `FlowerPowerAuraBrace`, `FlowerPowerAuraStrength`, `FlowersOnEndTurn`, `FlyDamageIncrease`, `Flying`, `FollowUp`, `ForceSpecificInjury`, `ForceUseAbility`, `FreePathfindElement`, `FreeSpellsAtFullMana`, `FreezePiercing`, `FrontstabBasicAttackCritChance`, `FullHeal`, `FullHealthCritChance`, `FullPower`, `FurnitureStats`, `GainExtraShield`, `GravityWell`, `HPGainBlock`, `HeadArmorPassiveMultiplierBonus`, `HealDamagesEnemies`, `HealsAlsoRegenMana`, `HealsCanRevive`, `HealthRegenUp`, `HolyShieldTransferToTaggedMinions`, `HouseFoodRequirementMultiplier`, `Hypomania`, `IgnoreTiles`, `ImmortalLeeches`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `IncreaseHealingSpellRange`, `IncreaseSpellRange`, `InfiniteRebirth`, `InnateElement`, `InvertBrainFaction`, `KillsHeal`, `KillsToMeat`, `KnockbackImmunity`, `LateBloomer`, `LevelUpClassOverride`, `LightningAspectCharge`, `LightningRod`, `LimitDamage`, `LimitHeal`, `LimitSelfKnockbackDamage`, `LimitedTileTrail`, `LineOfSightTrueSightAura`, `LobbedHook`, `LowHealthAllyDodgeChanceAura`, `Madness`, `MakeBasicAttackPassThroughThings`, `MakeSpellsRequireCharge`, `ManaCostReductionTagged`, `ManaRegenMultiplierIfManaEmpty`, `MaxAccuracy`, `MaxStartingMana`, `MegaMinions`, `MeleeRevengeDamage`, `Metal`, `MetalDetector`, `MinimumTech`, `MissChance`, `MoveAndUseAbilityEachTurnBeginIfPossible`, `MoveAwayFromDamageSource`, `MoveQuivered`, `MoveSpeedMultiplier`, `MoveTowardsDamageSource`, `MoveWhenDamaged`, `MovementReaction`, `MulticlassLevelUp`, `NeckArmorPassiveMultiplierBonus`, `NoManaRegen`, `NoReflection`, `NubbyTossPriority`, `NumbingLeeches`, `OverhealGainsBothShield`, `OverrideBasicAttack`, `OverrideMaxHealth`, `OverrideMaxMana`, `OverridePalette`, `Paranoia`, `ParasitesArentCursed`, `PassiveAfterXKills`, `PassiveAtFullHealth`, `PassiveAtHealthThreshold`, `PassiveAtInjuryThreshold`, `PassiveAtStatThreshold`, `PassiveIfAllArmorEmpty`, `PassiveIfEmptyFace`, `PassiveIfEmptyHead`, `PassiveIfEmptyNeck`, `PassiveLevelScaledStatus`, `PassiveLevelUpAtCombatEnd`, `PassiveUntilCastSpell`, `PassiveUntilGetKill`, `PassiveWhenAffectedByElement`, `PassiveWhenAtFullMana`, `PassiveWhenTheAlpha`, `PassiveWhileInMonkMeleeStance`, `PassiveWhileInMonkRangedStance`, `PassiveWhilePreviewingMonkRangedStance`, `PassiveWhileWearingMetal`, `PermanentImmobile`, `PermanentItems`, `PermanentKitten`, `PermanentMadness`, `Poison`, `PoisonThorns`, `PoopWhenHit`, `ProtectTargetedAllies`, `Quiver`, `Quivered`, `RandomPassivePool`, `RangedTrueShot`, `RealTimePressure_OneUnit`, `ReceivedStatusReplacement`, `RemoveLineOfSightRestrictions`, `RemoveOncePerFightRestriction`, `ReplaceBasicAttack`, `ReplaceBasicAttackWhenCastable`, `ReplaceBasicAttackWhenDead`, `ReplaceBasicMove`, `ReplaceSpawnedObjects`, `RevengeDamage`, `ReviveOnWin`, `RobotsInheritArmor`, `RockDetector`, `ScaledStatusOnBleedDamage`, `ScaledStatusOnOverMana`, `ScaledStatusOnSpendMana`, `SchrodingerDisorder`, `Scleroderma`, `SecurityBotProtect`, `SelfDamageWhenDealDamage`, `SetDefaultFacePassive`, `SetSpellCosts`, `ShareHealthRegen`, `SharePickups`, `ShoulderCheck`, `ShovingMatch`, `ShowHiddenThings`, `SizeScale`, `Slow`, `SmallEnemiesIgnoreYou`, `SmallRockBehavior`, `SmiteEnemiesWhoKill`, `SpawnCatCopyOnBattleStart`, `SpawnCreepOnHit`, `SpawnEachTurn`, `SpawnObjectOnPopCorpse`, `SpawnOnBattleStart`, `SpawnOnBattleStartRandomEmptyTile`, `SpawnThingOnDamage`, `SpawnThingOnDeath`, `SpecialFriends`, `SpeedUp`, `SplittableMove`, `SpreadExtraDebuffs`, `SpreadPainBonus`, `StatMinimum`, `StatsAtLowHealth`, `StatusAdjacentOnTheirTurnBegin`, `StatusAfterCastSpell`, `StatusAlliesOnBattleStart`, `StatusAlliesOnDeath`, `StatusAlliesOnGainCoins`, `StatusAlliesOnKill`, `StatusAllyWhenAllySpendsMana`, `StatusAnyCatAllyWhoKills`, `StatusDamagers`, `StatusEachTurnBegin`, `StatusEachTurnEnd`, `StatusEachTurnEndForEachTurn`, `StatusEachTurnEndPerEnemyKill`, `StatusEnemiesOnDeath`, `StatusEveryXSpellCasts`, `StatusEveryXTurnBegins`, `StatusIfBattleAlreadyBegan`, `StatusIfUnusedMovePoints`, `StatusImmunity`, `StatusKilledCharacters`, `StatusKillers`, `StatusOnAllyCatDeath`, `StatusOnAnyDeath`, `StatusOnBattleEnd`, `StatusOnBattleEndIfKillThresholdMet`, `StatusOnBattleStart`, `StatusOnBreakItem`, `StatusOnCastSpell`, `StatusOnCollectPickup`, `StatusOnCrit`, `StatusOnDealtDamage`, `StatusOnDealtDamageThreshold`, `StatusOnEatFood`, `StatusOnEatPill`, `StatusOnEndMove`, `StatusOnGainCoins`, `StatusOnGainShield`, `StatusOnHeal`, `StatusOnHealed`, `StatusOnKill`, `StatusOnKillEnemy`, `StatusOnLoseShield`, `StatusOnOverHealed`, `StatusOnOverMana`, `StatusOnPickupCoins`, `StatusOnPopCorpse`, `StatusOnStanceSwitch`, `StatusOnTakeHealthDamage`, `StatusOnTookDamage`, `StatusOnTookDamageFromAbility`, `StatusOnTookDamageFromEnemyAbility`, `StatusOnTriggerTrap`, `StatusOnTurnEndIfCastNSpells`, `StatusOnTurnEndIfDidntCastAbilityTypes`, `StatusOnTurnEndIfManaExact`, `StatusOnTurnEndIfManaOrHealthExact`, `StatusOnUseAbilityWithTag`, `StatusOnUseBasicAttack`, `StatusOnUseElementAbility`, `StatusPerInjury`, `StatusReplacement`, `StatusThingsKnockedBack`, `StatusWhenAllySpendsMana`, `Stealth`, `StrengthForEachNeighboringEnemy`, `StrengthInNumbersAura`, `StrengthUp`, `StrictLimitDamage`, `Study`, `TaggedPickupEffectReplacement`, `TauntAlways`, `TauntAtFullHealth`, `Tech`, `TempInitiativeChange`, `TheHunger`, `Thorns`, `TileDamageMultiplier`, `TileTrail`, `TourettesMeows`, `TowerDefense`, `TowerDefenseReflex`, `Trample`, `TrapEffectsMultiplier`, `TrinketActiveEffectsMultiplierBonus`, `TrinketPassiveMultiplierBonus`, `Triskaidekaphobia`, `UncappedHP`, `UncappedMana`, `UpgradeLevelUpClassActives`, `UpgradeLevelUpClassPassives`, `UpgradeSpawnedPickups`, `Vegan`, `Vengeful`, `WaterWalk`, `Weakness`, `WeaponActiveEffectsMultiplierBonus`, `WeaponCountsAsBasicAttack`, `WeaponDamageMultiplierBonus`, `WeaponPassiveMultiplierBonus`, `WobblyCat`

### `properties` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `layer`, `scale`

### `stats` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (7):** `charisma`, `constitution`, `dexterity`, `intelligence`, `luck`, `speed`, `strength`

**In Master but NOT in split file (7):** `cha`, `con`, `dex`, `int`, `lck`, `spd`, `str`

### `statuses` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FindItemFromPool`, `HealthGain`, `PermanentDexterity`

### `statuses_on_enter_form` (from `Characters_and_Bosses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseAbility`

### `boss` (from `Combat_Rewards.md`)

**In Master but NOT in split file (7):** `boss_cutscene`, `is_final_boss`, `level`, `override_music`, `tileset`, `type`, `unlockcheck_on_complete`

### `ROOT` (from `Custom_Cats.md`)

**In split file but NOT in Master (23):** `arm1`, `arm2`, `body`, `class_anis`, `claws`, `default_frame`, `face`, `head`, `leftear`, `lefteye`, `lefteyebrow`, `leg1`, `leg2`, `mouth`, `pitch`, `rightear`, `righteye`, `righteyebrow`, `tail`, `texture`, `voice`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `ROOT` (from `Damage_Text_Styles.md`)

**In split file but NOT in Master (7):** `back_icon`, `color`, `outline_color`, `right_icon`, `suffix`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `ROOT` (from `Difficulties.md`)

**In split file but NOT in Master (10):** `bonus_itemroll_luck`, `boss_elite_buffs`, `boss_health_multiplier`, `coins_multiplier`, `easy`, `event_difficulty`, `food_multiplier`, `hard`, `wallet_size`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `hard` (from `Difficulties.md`)

**In split file but NOT in Master (6):** `champ_budget`, `champ_chance_mini`, `elite_budget`, `elite_buffs`, `elite_chance_mini`, `rare_elite_buffs`

**In Master but NOT in split file (4):** `coins`, `consumable_chance`, `food`, `item_chance`

### `AddStatusToBasicAttack` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (43):** `ApplyStatusIfCrit`, `ApplyToSource`, `BigSplashDamage`, `Bleed`, `Blind`, `BounceObject`, `Bruise`, `BurgleCoin`, `Burn`, `ChangeTile`, `Charmed`, `Conditional_Adjacent`, `Conditional_Ally`, `Conditional_Enemy`, `Conditional_HasTag`, `Conditional_Shielded`, `Conditional_SourceHasTag`, `Confusion`, `DamageOrHealConditionally`, `DistanceBonusDamage`, `Else`, `Fear`, `Freeze`, `KnockOutCoin`, `Knockback`, `Leech`, `Leeches`, `LuckUp`, `Madness`, `MagicWeakness`, `ManaLeeches`, `OverrideChainKnockback`, `OverrideChainKnockbackDamage`, `Piercing`, `Poison`, `Rot`, `Slow`, `SoulLink`, `SpawnBearTrapOnMiss`, `SplashDamage`, `SpreadDisease`, `Stun`, `Weakness`

### `ChanceToRevive` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `health`

### `DamageNeighborsAfterMove` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `MeleeRevengeDamage` (from `Elite_Buffs.md`)

**In split file but NOT in Master (2):** `knockback`, `{Damaging Keys}`

**In Master but NOT in split file (5):** `Poison`, `SpreadDisease`, `Weakness`, `damage`, `effects`

### `ROOT` (from `Elite_Buffs.md`)

**In split file but NOT in Master (11):** `icon_frame`, `minion_alt`, `only_at_battle_start`, `requires_corpse`, `roll_limit`, `rollable`, `specific_chapter`, `unique`, `value`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `ReflectProjectiles` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `self_damage`

### `RevengeDamage` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `effects`, `knockback`

### `SpawnOnBattleStart` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `prevent_chain_tag`

**In Master but NOT in split file (1):** `number`

### `StatusEachRoundBegin` (from `Elite_Buffs.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `NonStackingShield`

### `StatusEachRoundEnd` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (3):** `AddRandomEliteBuff`, `DoDamage`, `UseAbility`

### `StatusEachTurnEnd` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (11):** `EmptyMana`, `ForceUseAbility`, `IntelligenceUp`, `KineticSpikes`, `NonStackingDivineShield`, `ObjectOnHitCharacter`, `PermanentMadness`, `RangeUp`, `SpeedUp`, `StrengthUp`, `UseAbility_Madness`

### `StatusOnDie` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (10):** `Conditional_RandomChance`, `CreateGlobalModifiers`, `FindItemFromPool`, `GainCoinsRange`, `RandomMagicMissile`, `RandomStatusFromPool`, `RemoveAmbientLightEffects`, `RemoveGlobalModifiers`, `ScatterCoins`, `StackingSandstorm`

### `StatusOnEnemyCastSpell` (from `Elite_Buffs.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `HealthGain`

### `StatusOnKill` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `Conditional_FirstApplicationThisTurn`, `DamageUp`, `EquipPermanentItem`, `HealthGain`, `LuckUp`, `RandomStatUp`, `RefreshActPoints`, `RefreshMovePoints`, `SpeedUp`, `Stealth`, `StrengthUp`, `TakeBonusTurnWithStatus`

### `effects` (from `Elite_Buffs.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Logic Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `passives` (from `Elite_Buffs.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (424):** `AbilityOnBattleStart`, `AbilityReaction`, `AbilityWhenTaggedCharacterMovesNear`, `AbsorbManaAura`, `AddAllyNeighborsToAttackRange`, `AddBonusMeleeRange`, `AddBonusRange`, `AddCorpseHealth`, `AddCritMultiplier`, `AddDamageToBasicAttack`, `AddDamageToElementDamage`, `AddElementsToBasicAttack`, `AddHiddenTag`, `AddInitiative`, `AddKnockbackDamage`, `AddLevelUpRerolls`, `AddLevelUpStatMultiplier`, `AddManaRegen`, `AddMovement`, `AddPassiveToSpawnedRocks`, `AddPassivesToCharmed`, `AddPassivesToMinions`, `AddPassivesToSummonAbilityMinions`, `AddSelfStatusToBasicAttack`, `AddSelfStatusToWeapons`, `AddSpellDamage`, `AddStartingMana`, `AddStatusToAllDamage`, `AddStatusToBasicAttack`, `AddStatusToBasicAttackWithCooldown`, `AddStatusToBasicMeleeAttack`, `AddStatusToElementAbilities`, `AddStatusToElementDamage`, `AddStatusToExplosions`, `AddStatusToFirstBasicAttack`, `AddStatusToMeleeDamage`, `AddStatusToReceivedDamage_ExcludeStatuses`, `AddStatusToTrampleDamage`, `AddStatusToWeapons`, `AddStatusesIfPersistentWeatherElement`, `AddStatusesToReceivedElementalDamage`, `AddTag`, `AddTemporaryEffectsToBasicAttack`, `AddUnfilledMaxHealth`, `AddWeaponScaling`, `AfterImage`, `AllStatsUp`, `AllowPassTurn`, `AllyBonusAbilityAura`, `AllyDamageReaction`, `AllyDamageReduction`, `AllyHealthRegenAura`, `AllyManaRegenAura`, `AllyMoveAbilityAura`, `AllyMultiplyKnockbackDamage`, `AlphaTurns`, `AlternateCraftingPools`, `AmplifyKnockback`, `AmplifyPositiveStatus`, `AmplifyStatus`, `ApplyStatusesToRandomEnemiesEachTurn`, `Autism`, `AutoCritLowDamage`, `AutoEquipConsumables`, `AutocastEachRound`, `AutocastEachTurn`, `AutocastEachTurnBegin`, `BackstabCritChance`, `BackstabWeakness`, `BasicAttackAOEBonus`, `BasicAttackCritChance`, `BasicAttackDamageMultiplier`, `BasicAttackStatusCarefulness`, `BlacklistPickupType`, `BlastResistance`, `Bleed`, `BleedThorns`, `BonusAbility`, `BonusFoodEachBattle`, `BoobyTrapItems`, `BoostAllyStatsOnDeath`, `BoostDamageAura`, `BoostHeals`, `BoostRangeAura`, `BoostWeaponDamage`, `BouncyProjectiles`, `Brace`, `BraceForEachNeighboringEnemy`, `Bruise`, `BuffImmunity`, `Burn`, `CCImmunity`, `CanRemoveCursedItems`, `CantDodge`, `CapDamageFromAllies`, `CapMovementAbilityRange`, `CatAPultAnimation`, `CatchProjectiles`, `ChainKnockback`, `ChanceToBackflip`, `ChanceToBlockAndCounter`, `ChanceToRevive`, `ChangeTauntPriority`, `CharmAllFlies`, `ClassManaCostReduction`, `CobraReflex`, `CoinsAddDamage`, `CollectPickupsOnBattleEnd`, `Conductor`, `ConfusionEffectOnTaggedAbilities`, `ConjureCastSpellsForAllies`, `ConsumableEffectsMultiplierBonus`, `ConsumablesInfiniteRange`, `ConsumablesMeleeRange`, `CounterAttack`, `CritChanceUp`, `CritsApplyStatus`, `DamageEnemiesOnHeal`, `DamageEnemiesOnKill`, `DamageIfDidntUseSpecificAbility`, `DamageNeighborTilesWhenCastSpell`, `DamageNeighborsAfterMove`, `DamageNeighborsOnEndMove`, `DamageReductionAura`, `DamageUp`, `DeathChill`, `DeathRattle`, `DebuffImmunity`, `DejaVu`, `DepressionAura`, `Diabetes`, `DirtyClaws`, `DisableAbilities`, `DisableAbilitiesWithTag`, `DodgeChance`, `Doomed`, `DoubleCastWeapons`, `DukeOfFlies`, `Dyslexia`, `EMP`, `ElementImmune`, `ElementalAttunement`, `ElementalManaCostReduction`, `Empath`, `EnemiesGetPickupsKnockedOut`, `EnergyStorm`, `EquipTemporaryItem`, `EquipmentPassiveMultiplierBonus`, `EquipmentSetBonusBonus`, `EscapeSequence`, `Eternal`, `ExhaustionRoundChange`, `ExplodeOverkilledEnemies`, `ExtraBasicAttacks`, `ExtraBasicMoves_Status`, `ExtraInjuryOnDeath`, `ExtraMovePoints`, `ExtraStatusWhenDealingDamage`, `ExtraWeaponAttacks`, `FaceArmorPassiveMultiplierBonus`, `FaceShield`, `FamiliarSecondaryDamageImmunity`, `FlowerPowerAuraBrace`, `FlowerPowerAuraStrength`, `FlowersOnEndTurn`, `FlyDamageIncrease`, `Flying`, `FollowUp`, `ForceSpecificInjury`, `ForceUseAbility`, `FreePathfindElement`, `FreeSpellsAtFullMana`, `FreezePiercing`, `FrontstabBasicAttackCritChance`, `FullHeal`, `FullHealthCritChance`, `FullPower`, `FurnitureStats`, `GainExtraShield`, `GravityWell`, `HPGainBlock`, `HeadArmorPassiveMultiplierBonus`, `HealDamagesEnemies`, `HealsAlsoRegenMana`, `HealsCanRevive`, `HealthRegenUp`, `HolyShieldTransferToTaggedMinions`, `HouseFoodRequirementMultiplier`, `Hypomania`, `IgnoreTiles`, `ImmortalLeeches`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `IncreaseHealingSpellRange`, `IncreaseSpellRange`, `InfiniteRebirth`, `InnateElement`, `InvertBrainFaction`, `KillsHeal`, `KillsToMeat`, `KnockbackImmunity`, `LateBloomer`, `LevelUpClassOverride`, `LightningAspectCharge`, `LightningRod`, `LimitDamage`, `LimitHeal`, `LimitSelfKnockbackDamage`, `LimitedTileTrail`, `LineOfSightTrueSightAura`, `LobbedHook`, `LowHealthAllyDodgeChanceAura`, `Madness`, `MakeBasicAttackPassThroughThings`, `MakeSpellsRequireCharge`, `ManaCostReductionTagged`, `ManaRegenMultiplierIfManaEmpty`, `MaxAccuracy`, `MaxStartingMana`, `MegaMinions`, `MeleeRevengeDamage`, `Metal`, `MetalDetector`, `MinimumTech`, `MissChance`, `MoveAndUseAbilityEachTurnBeginIfPossible`, `MoveAwayFromDamageSource`, `MoveQuivered`, `MoveSpeedMultiplier`, `MoveTowardsDamageSource`, `MoveWhenDamaged`, `MovementReaction`, `MulticlassLevelUp`, `NeckArmorPassiveMultiplierBonus`, `NoManaRegen`, `NoReflection`, `NubbyTossPriority`, `NumbingLeeches`, `OverhealGainsBothShield`, `OverrideBasicAttack`, `OverrideMaxHealth`, `OverrideMaxMana`, `OverridePalette`, `Paranoia`, `ParasitesArentCursed`, `PassiveAfterXKills`, `PassiveAtFullHealth`, `PassiveAtHealthThreshold`, `PassiveAtInjuryThreshold`, `PassiveAtStatThreshold`, `PassiveIfAllArmorEmpty`, `PassiveIfEmptyFace`, `PassiveIfEmptyHead`, `PassiveIfEmptyNeck`, `PassiveLevelScaledStatus`, `PassiveLevelUpAtCombatEnd`, `PassiveUntilCastSpell`, `PassiveUntilGetKill`, `PassiveWhenAffectedByElement`, `PassiveWhenAtFullMana`, `PassiveWhenTheAlpha`, `PassiveWhileInMonkMeleeStance`, `PassiveWhileInMonkRangedStance`, `PassiveWhilePreviewingMonkRangedStance`, `PassiveWhileWearingMetal`, `PermanentImmobile`, `PermanentItems`, `PermanentKitten`, `PermanentMadness`, `Poison`, `PoisonThorns`, `PoopWhenHit`, `ProtectTargetedAllies`, `Quiver`, `Quivered`, `RandomPassivePool`, `RangedTrueShot`, `RealTimePressure_OneUnit`, `ReceivedStatusReplacement`, `RemoveLineOfSightRestrictions`, `RemoveOncePerFightRestriction`, `ReplaceBasicAttack`, `ReplaceBasicAttackWhenCastable`, `ReplaceBasicAttackWhenDead`, `ReplaceBasicMove`, `ReplaceSpawnedObjects`, `RevengeDamage`, `ReviveOnWin`, `RobotsInheritArmor`, `RockDetector`, `ScaledStatusOnBleedDamage`, `ScaledStatusOnOverMana`, `ScaledStatusOnSpendMana`, `SchrodingerDisorder`, `Scleroderma`, `SecurityBotProtect`, `SelfDamageWhenDealDamage`, `SetDefaultFacePassive`, `SetSpellCosts`, `ShareHealthRegen`, `SharePickups`, `ShoulderCheck`, `ShovingMatch`, `ShowHiddenThings`, `SizeScale`, `Slow`, `SmallEnemiesIgnoreYou`, `SmallRockBehavior`, `SmiteEnemiesWhoKill`, `SpawnCatCopyOnBattleStart`, `SpawnCreepOnHit`, `SpawnEachTurn`, `SpawnObjectOnPopCorpse`, `SpawnOnBattleStart`, `SpawnOnBattleStartRandomEmptyTile`, `SpawnThingOnDamage`, `SpawnThingOnDeath`, `SpecialFriends`, `SpeedUp`, `SplittableMove`, `SpreadExtraDebuffs`, `SpreadPainBonus`, `StatMinimum`, `StatsAtLowHealth`, `StatusAdjacentOnTheirTurnBegin`, `StatusAfterCastSpell`, `StatusAlliesOnBattleStart`, `StatusAlliesOnDeath`, `StatusAlliesOnGainCoins`, `StatusAlliesOnKill`, `StatusAllyWhenAllySpendsMana`, `StatusAnyCatAllyWhoKills`, `StatusDamagers`, `StatusEachTurnBegin`, `StatusEachTurnEnd`, `StatusEachTurnEndForEachTurn`, `StatusEachTurnEndPerEnemyKill`, `StatusEnemiesOnDeath`, `StatusEveryXSpellCasts`, `StatusEveryXTurnBegins`, `StatusIfBattleAlreadyBegan`, `StatusIfUnusedMovePoints`, `StatusImmunity`, `StatusKilledCharacters`, `StatusKillers`, `StatusOnAllyCatDeath`, `StatusOnAnyDeath`, `StatusOnBattleEnd`, `StatusOnBattleEndIfKillThresholdMet`, `StatusOnBattleStart`, `StatusOnBreakItem`, `StatusOnCastSpell`, `StatusOnCollectPickup`, `StatusOnCrit`, `StatusOnDealtDamage`, `StatusOnDealtDamageThreshold`, `StatusOnEatFood`, `StatusOnEatPill`, `StatusOnEndMove`, `StatusOnGainCoins`, `StatusOnGainShield`, `StatusOnHeal`, `StatusOnHealed`, `StatusOnKill`, `StatusOnKillEnemy`, `StatusOnLoseShield`, `StatusOnOverHealed`, `StatusOnOverMana`, `StatusOnPickupCoins`, `StatusOnPopCorpse`, `StatusOnStanceSwitch`, `StatusOnTakeHealthDamage`, `StatusOnTookDamage`, `StatusOnTookDamageFromAbility`, `StatusOnTookDamageFromEnemyAbility`, `StatusOnTriggerTrap`, `StatusOnTurnEndIfCastNSpells`, `StatusOnTurnEndIfDidntCastAbilityTypes`, `StatusOnTurnEndIfManaExact`, `StatusOnTurnEndIfManaOrHealthExact`, `StatusOnUseAbilityWithTag`, `StatusOnUseBasicAttack`, `StatusOnUseElementAbility`, `StatusPerInjury`, `StatusReplacement`, `StatusThingsKnockedBack`, `StatusWhenAllySpendsMana`, `Stealth`, `StrengthForEachNeighboringEnemy`, `StrengthInNumbersAura`, `StrengthUp`, `StrictLimitDamage`, `Study`, `TaggedPickupEffectReplacement`, `TauntAlways`, `TauntAtFullHealth`, `Tech`, `TempInitiativeChange`, `TheHunger`, `Thorns`, `TileDamageMultiplier`, `TileTrail`, `TourettesMeows`, `TowerDefense`, `TowerDefenseReflex`, `Trample`, `TrapEffectsMultiplier`, `TrinketActiveEffectsMultiplierBonus`, `TrinketPassiveMultiplierBonus`, `Triskaidekaphobia`, `UncappedHP`, `UncappedMana`, `UpgradeLevelUpClassActives`, `UpgradeLevelUpClassPassives`, `UpgradeSpawnedPickups`, `Vegan`, `Vengeful`, `WaterWalk`, `Weakness`, `WeaponActiveEffectsMultiplierBonus`, `WeaponCountsAsBasicAttack`, `WeaponDamageMultiplierBonus`, `WeaponPassiveMultiplierBonus`, `WobblyCat`

### `statuses` (from `Elite_Buffs.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FindItemFromPool`, `HealthGain`, `PermanentDexterity`

### `ROOT` (from `Enemy_AI.md`)

**In split file but NOT in Master (54):** `accurate_knockback`, `buff_ally`, `buff_enemy`, `buff_self`, `cap_distance_to_ally`, `cap_distance_to_character`, `cap_distance_to_enemy`, `cap_total_distance_moved`, `consider_aggro_target_enemy`, `consider_aoe`, `consider_overkill`, `consider_secondary_damage`, `consider_total_damage`, `count_nomove_in_eval`, `damage_ally`, `damage_ally_corpse`, `damage_enemy`, `damage_enemy_corpse`, `damage_self`, `danger_avoidance`, `debuff_ally`, `debuff_enemy`, `debuff_self`, `distance_to_aggro_target`, `distance_to_ally`, `distance_to_center`, `distance_to_character`, `distance_to_corpse`, `distance_to_enemy`, `distance_to_water`, `exclude_characters_tagged`, `face_aggro_target`, `face_camera`, `face_closest_enemy`, `flat_cast_bonus`, `heal_ally`, `heal_enemy`, `heal_self`, `kill_ally`, `kill_enemy`, `lava`, `negative_weight_scale`, `preferred_distance`, `randomness`, `revive_ally_corpse`, `revive_enemy_corpse`, `simple`, `spawn_object`, `spawn_object_distance_to_ally`, `spawn_object_distance_to_enemy`, `spawn_object_preferred_distance`, `spend_mana_scale`, `tall_grass`, `total_distance_moved`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `CharacterTypeGainsStatusAtBattleStart` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Conditional_Flying`, `Else`, `Fear`, `Stealth`, `Stun`

### `ROOT` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (27):** `animation_fail`, `buy2`, `buy3`, `cha`, `con`, `copy_results`, `destroy`, `dex`, `examine`, `good`, `ignore`, `int`, `intro`, `label`, `lck`, `main`, `open`, `pick`, `requirements`, `smash`, `spd`, `stat`, `stat_max`, `stat_min`, `str`, `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `StatusRandomEnemiesOnBattleStart` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Bleed`, `Charmed`, `Confusion`, `Fear`, `Freeze`

### `a` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `activate_p` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `activate_z` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `arm` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `attach_amplifier` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `attach_antenna` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `attach_leech` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `attack` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `bad`, `rare`

### `b` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `bad` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (22):** `battle`, `conditional_reward`, `cutscene`, `event_now`, `event_now_same_cat`, `gain_disorder_from_pool`, `gain_immortal_familiar`, `get_parasite`, `get_parasite_from_pool`, `injury`, `kill`, `lose_item`, `next_event_bonus`, `party_random_mutation_from_set`, `permanent_stats`, `play_animation`, `prompt`, `reward`, `select_item_from_pool_for_cutscene_only`, `self_status_next_fight`, `set_frame`, `set_legacy_token`

### `bash` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `bash_past_alt` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `bite` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (6):** `animation`, `bad`, `eyebrow_rotation`, `eyebrow_up`, `eyes`, `mouth`

### `bite_it_off` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `blue` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `blue_needle` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `body` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `boogers` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `book` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `brace` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `break_ice` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `break_lock` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `bribe` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `button` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `buy1` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `animation`, `prompt`, `self_status_next_fight`, `weight`

### `c` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `catch` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `challenge_to_game` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `charm` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `charm_past_alt` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `climb` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `comfort` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `common` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (55):** `add_weather`, `ally_ambush_next_fights`, `ambush_next_basic_fights`, `clear_adventure_token`, `clear_result_animation`, `conditional_reward`, `decrement_legacy_counter`, `event_now`, `event_now_same_cat`, `full_heal`, `gain_coins`, `gain_disorder`, `gain_disorder_from_pool`, `gain_familiar`, `gain_food`, `get_and_equip_item`, `get_item`, `get_item_from_pool`, `get_parasite`, `get_parasite_from_pool`, `global_effect_next_fight`, `heal`, `heal_disorder`, `heal_injury`, `increment_legacy_counter`, `injury`, `kill`, `learn_ability_from_pool`, `lose_item`, `lose_specific_item`, `mutation`, `next_event_bonus`, `next_event_from_set`, `override_end_option_prompt`, `party_damage`, `party_heal`, `party_heal_disorder`, `party_permanent_stats_exclude_self`, `party_status_next_fight`, `permanent_stats`, `play_animation`, `prompt`, `random_mutation`, `random_mutation_from_set`, `random_pool`, `self_damage`, `self_heal`, `self_status_next_fight`, `set_adventure_token`, `set_frame`, `set_legacy_token`, `shop_now`, `spawn_unit_next_fight`, `spin`, `upgrade_ability`

### `communicate` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `concheck` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `conditional_reward` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `prompt`, `reward`

### `counter` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `crack_open` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `cross` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `cut_wires` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `cutscene` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `cutscene`

### `d` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `damage` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (3):** `animation`, `damage`, `type`

### `damage_1` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `damage_full` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `damage_half` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `destroy` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `dexcheck` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `dig` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `disarm` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `dive` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `donate` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `donate_10` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `donate_15` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `donate_20` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `donate_5` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `double` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `drink` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `eat` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `eat_meat` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `else` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (15):** `conditional_reward`, `event_now`, `event_now_same_cat`, `gain_disorder`, `get_item_from_pool`, `increment_legacy_counter`, `next_event_bonus`, `party_damage`, `prompt`, `random_mutation`, `random_pool`, `self_status_next_fight`, `set_adventure_token`, `set_frame`, `set_legacy_token`

### `enter` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `enter_crater` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `examine` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (3):** `animation`, `bad`, `gain_coins`

### `fight` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `fill_jar` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `find_another_way` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `fire` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (4):** `good`, `label`, `stat`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `damage`, `effects`, `elements`, `type`

### `follow` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `free` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `future` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `spin_cats`

### `get_item_from_pool` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `prompt`

### `give_parasite` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `global_effect_next_fight` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `CharacterTypeGainsStatusAtBattleStart`, `Fights`, `StatusRandomEnemiesOnBattleStart`

### `go_around` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `good` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (58):** `add_weather`, `ally_ambush_next_fights`, `begin_chapter`, `clear_surviving_kaiju`, `clone_self_to_party`, `complete_item_quest`, `conditional_reward`, `copy_items_to_party`, `copy_party_items`, `cutscene`, `cutscene_on_exit`, `event_now`, `event_now_same_cat`, `full_heal`, `gain_clone_familiar`, `gain_disorder`, `gain_disorder_from_pool`, `gain_food`, `get_full_item_set_from_pool`, `get_item`, `get_item_from_pool`, `get_parasite`, `global_effect_next_fight`, `heal`, `heal_disorder`, `heal_injury`, `increment_legacy_counter`, `injury`, `kill`, `learn_ability_from_pool`, `learn_passive_from_pool`, `level_up`, `lose_item`, `lose_specific_item`, `mutation`, `next_event_bonus`, `next_event_from_set`, `override_end_option_prompt`, `party_gain_disorder_from_pool`, `play_animation`, `prompt`, `random_mutation`, `random_pool`, `random_pool_consider_luck`, `rare`, `reward`, `scramble_abilities`, `scramble_passives`, `set_adventure_token`, `set_frame`, `set_legacy_token`, `shop_now`, `transform_item`, `trigger_adventure_unlock`, `trigger_butterfly_effect`, `unlock_item_quest`, `upgrade_ability`, `upgrade_passive`

### `hack` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `holy` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `home` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `type`

### `hp` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `ice` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (4):** `good`, `label`, `stat`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `damage`, `effects`, `elements`, `type`

### `ignore` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `infinite` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `inspect` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `intcheck` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `intimidation` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `intro` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (14):** `cat_choice`, `choose_cat_with_highest_stat`, `choose_cat_with_item`, `choose_cat_with_item_slot_equipped`, `choose_cat_with_min_health`, `choose_cat_with_most_injuries`, `choose_cat_with_parasite`, `different_from_last_x_cats`, `event_clip`, `subject_clip`, `subject_frame`, `subject_frame_inner`, `title`, `{Event Keys}`

**In Master but NOT in split file (9):** `delay`, `dialog`, `dialog_and_autopass`, `lock_controls`, `set_mood`, `set_state`, `sfx`, `unlock_controls`, `wait_for`

### `investigate` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `itchies` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `join` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `jump` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `jump_over` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `keep_going` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `kiss` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `kiss_meat` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `knife` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `leave` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `leave_it_in` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `leg` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `lever` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `lick` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `lick_alt` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `lightning` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (4):** `good`, `label`, `stat`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `damage`, `effects`, `elements`, `type`

### `listen` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `loot` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (3):** `animation`, `bad`, `rare`

### `loot_heart` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `main` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (22):** `add_weather`, `bad`, `gain_familiar`, `goto`, `leave`, `max_options`, `next_event_from_set`, `options`, `outcome`, `party_heal`, `party_permanent_stats`, `play_animation`, `prompt`, `rare`, `requires_flag`, `self_damage`, `self_status_next_fight`, `set_frame`, `setup`, `shop_now`, `shuffle_options`, `weight`

### `makeup` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `mind` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `move_closer` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `nothanks` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `open` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `options` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (11):** `animation`, `bad`, `gain_familiar`, `get_item_from_pool`, `leave`, `play_animation`, `prompt`, `rare`, `scale`, `set_frame`, `weight`

### `outcome` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (3):** `add_weather`, `play_animation`, `random_pool`

### `party_status_next_fight` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `AbilityOnBattleStart_Immediate`, `Bleed`, `DivineShield`, `Fear`, `HealthRegenUp`, `Immobile`, `NoHealthRegen`, `Poison`, `Tangled`, `Tarred`, `Webbed`

### `past` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `patch_up` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pick_lock` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pilfer` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pirouette` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `place_gristle` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `play` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `poop` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `protection` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `pull` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pull_it_out` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pull_lever` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `purify` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `push_buttons` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `push_through` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `put_in_coins` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `put_out_of_misery` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `random_chance` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `get_item_from_pool`

### `rare` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (75):** `add_weather`, `ally_ambush_next_fights`, `ambush`, `ambush_next_basic_fights`, `battle`, `clear_result_animation`, `conditional_reward`, `decrement_legacy_counter`, `event_now`, `event_now_same_cat`, `full_heal`, `gain_cat_familiar`, `gain_coins`, `gain_disorder`, `gain_disorder_from_pool`, `gain_familiar`, `gain_food`, `gain_immortal_familiar`, `get_and_equip_item`, `get_item`, `get_item_from_pool`, `get_parasite`, `get_parasite_from_pool`, `global_effect_next_fight`, `heal_disorder`, `hide_appearance_changes`, `increment_legacy_counter`, `injury`, `kill`, `learn_ability`, `learn_ability_from_pool`, `learn_passive`, `learn_passive_from_pool`, `leave_party_temporarily`, `level_up`, `lose_all_equipped_items`, `lose_item`, `lose_item_from_inventory`, `lose_specific_item`, `make_old`, `mutation`, `next_event_bonus`, `next_event_from_set`, `override_end_option_prompt`, `party_damage`, `party_heal`, `party_heal_disorder`, `party_heal_injury`, `party_injury`, `party_permanent_stats`, `party_permanent_stats_exclude_self`, `party_random_mutation`, `party_random_mutation_from_set`, `party_status_next_fight`, `permanent_stats`, `play_animation`, `play_result_animation`, `prompt`, `random_mutation`, `random_mutation_from_set`, `random_pool`, `scramble_abilities`, `scramble_basic_attack`, `self_damage`, `self_status_next_fight`, `set_adventure_token`, `set_age`, `set_frame`, `set_legacy_token`, `shop_now`, `spawn_reflection_next_fight`, `spawn_unit_next_fight`, `trigger_adventure_unlock`, `upgrade_ability`, `upgrade_passive`

### `read` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `receive` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `red` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `red_needle` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `reflect` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `remove` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `remove_the_nail` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `repair` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `repell` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `requirements` (from `Events_and_Encounters.md`)

**In Master but NOT in split file (1):** `has_parasite`

### `rest` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `revive` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `reward` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (26):** `ambush_next_basic_fights`, `clear_adventure_token`, `common`, `cutscene_on_exit`, `event_now`, `gain_coins`, `gain_disorder_from_pool`, `get_item`, `get_item_from_pool`, `get_parasite_from_pool`, `injury`, `level_up`, `next_event_bonus`, `party_damage`, `play_animation`, `prompt`, `random_chance`, `random_pool`, `rare`, `set_adventure_token`, `set_frame`, `set_legacy_token`, `set_subject`, `spawn_unit_next_fight`, `trigger_adventure_unlock`, `weight`

### `rub` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `run` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `run_again` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `run_away` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sacrifice` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `sacrifice_full_favor` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `sacrifice_normal` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `sacrifice_partial_favor` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `sacrifice_quest` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `self_status_next_fight` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (39):** `AbilityOnBattleStart`, `AbilityOnBattleStart_Immediate`, `AddInitiative`, `AddStartingMana`, `AllStatsUp`, `AlphaTurns`, `Bleed`, `Blind`, `Bruise`, `Burn`, `ChangeTileUnderCharacterAtStart`, `CharismaUp`, `Confusion`, `ConstitutionUp`, `DexterityUp`, `DivineShield`, `Fear`, `Fights`, `HealthRegenUp`, `IntelligenceUp`, `LuckUp`, `Madness`, `MissChance`, `NoHealthRegen`, `NoManaRegen`, `PermanentConfusion`, `Poison`, `ProbeCharmed`, `RandomStatUp`, `Rot`, `Sleep`, `Slow`, `SpeedUp`, `SpiderInfested`, `StrengthUp`, `Stun`, `Tarred`, `TempStrengthUp`, `Webbed`

### `setup` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `conditional_reward`, `set_frame`

### `shake` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `skip` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `slip_through` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `smash` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sneak` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sneak_by` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sneak_past_alt` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `soul` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `spawn_reflection_next_fight` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `mutation`

### `speed` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `surprise` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `sweet_talk` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `swim` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `tail` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `take` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `take_blood` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `talk` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `talk_to` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `tappytoes` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `teleport` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `thorns` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `throw` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `touch` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `traverse` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (3):** `play_animation`, `prompt`, `shop_now`

### `turnon` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `upgrade_yourself` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_item` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_toilet_con` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_toilet_str` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_weapon` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (4):** `good`, `label`, `requirements`, `{Event Keys}`

**In Master but NOT in split file (7):** `dialog`, `dialog_and_autopass`, `get_token`, `set_state`, `sfx`, `unlock_controls`, `wait_for`

### `w1` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w2` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w3` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w4` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w5` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w6` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `wheezies` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `withstand` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `yank_it_out` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `yellow_needle` (from `Events_and_Encounters.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `ROOT` (from `Furniture_and_Metaprogression.md`)

**In split file but NOT in Master (15):** `Appeal`, `BreedSuppression`, `Comfort`, `Evolution`, `FightBonusRewards`, `FightRisk`, `FoodStorage`, `Health`, `Stimulation`, `can_be_rare`, `removed`, `set`, `special`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `ApplyPassives` (from `House_and_Environment.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `AddInitiative`, `AddTag`, `ElementImmune`, `Flying`, `IgnoreTiles`, `KnockbackImmunity`, `Plant`, `ReplaceBasicAttack`, `StatusOnBattleEnd`, `YOffset`

### `Big` (from `House_and_Environment.md`)

**In Master but NOT in split file (3):** `animation_suffix`, `attack`, `passives`

### `CharacterTypeGainsStatusAtBattleStart` (from `House_and_Environment.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Conditional_Flying`, `Else`, `Fear`, `Stealth`, `Stun`

### `Conditional_Corpse` (from `House_and_Environment.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Logic Keys}`

**In Master but NOT in split file (7):** `Charmed`, `DamageUp`, `OverrideDamage`, `Revive`, `SafeDoomed`, `SpeedUp`, `TakeExtraTurn`

### `Conditional_GoodRoll` (from `House_and_Environment.md`)

**In split file but NOT in Master (3):** `{Damaging Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseRandomSpell_Madness`

### `Conditional_HasTag` (from `House_and_Environment.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Logic Keys}`

**In Master but NOT in split file (2):** `Charmed`, `FlatLeechIfDamaged`

### `Conditional_PartyMember` (from `House_and_Environment.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Logic Keys}`

**In Master but NOT in split file (1):** `Charmed`

### `Default` (from `House_and_Environment.md`)

**In Master but NOT in split file (6):** `ai`, `attack`, `move`, `partial_animation_suffix`, `passives`, `turns`

### `Else` (from `House_and_Environment.md`)

**In split file but NOT in Master (3):** `{Damaging Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `CaptureFamiliar`, `FactionConversion`, `Fear`, `Marked`, `PermanentCharm`, `TempSpeedUp`

### `FactionUprising` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `extra_statuses`

### `Floor1_Large` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `Floor1_Small` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `ROOT` (from `House_and_Environment.md`)

**In split file but NOT in Master (36):** `BasementUpgrade`, `BasementUpgrade2`, `BasementUpgrade3`, `BasementUpgrade4`, `BasementUpgrade5`, `Default`, `Floor1_Large`, `Floor1_Small`, `House1`, `House2`, `House3`, `LargeHouse`, `LargeHouse_Floor2Large`, `LargeHouse_Floor2Small`, `MediumHouse`, `MediumHouse_SmallRoom`, `SmallAttic`, `SmallHouse_Attic`, `Thunderstorm`, `ambient_sound`, `amount`, `extra_bound_planes`, `height`, `hint_persistent_elements`, `id`, `interstitial_bg_frame`, `n`, `p`, `preset`, `reverb_empty`, `reverb_full`, `volume_adjustment`, `width`, `{Damaging Keys}`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `Rain` (from `House_and_Environment.md`)

**In Master but NOT in split file (1):** `ai`

### `RandomStatusFromPool` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (37):** `AllStatsUp`, `Bleed`, `BleedThorns`, `Blind`, `Brace`, `Bruise`, `Burn`, `Charge`, `Charmed`, `Confusion`, `ConstitutionUp`, `DiminishingHealthRegen`, `DivineShield`, `Fear`, `Freeze`, `Immobile`, `KineticSpikes`, `Madness`, `MagicWeakness`, `Marked`, `MoveQuivered`, `ObjectOnHitCharacter`, `Petrify`, `Poison`, `Quivered`, `Reflect`, `Shield`, `Sleep`, `Slow`, `SpawnCoinAnywhere`, `SpeedUp`, `StatusGroup`, `StrengthUp`, `Stun`, `Tarred`, `Thorns`, `Weakness`

### `SmallAttic` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `SolarFlare` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `StatusAllCharactersOnSpawn` (from `House_and_Environment.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_Boss`, `Conditional_PartyMember`, `Conditional_Tiny`, `Else`, `Poison`

### `StatusCharactersOnRoundEnd` (from `House_and_Environment.md`)

**In split file but NOT in Master (3):** `{Damaging Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Conditional_GoodRoll`, `FloatingRockTrap`, `Thorns`, `tag_filter`

### `StatusCharactersOnRoundStart` (from `House_and_Environment.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_GoodRoll`, `Else`, `Madness`

### `StatusOnBattleEnd` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (10):** `CureDisease`, `FindItemFromPool`, `NextBattleStatus`, `PermanentConstitution`, `PermanentIntelligence`, `PermanentSpeed`, `PermanentStrength`, `RandomMutation`, `RandomPermanentStat`, `even_if_dead`

### `effects` (from `House_and_Environment.md`)

**In split file but NOT in Master (4):** `{Damaging Keys}`, `{Global Modifier Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `extra_statuses` (from `House_and_Environment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Burn`, `Conditional_HasTag`, `HealthGain`, `Poison`, `Tarred`

### `ROOT` (from `Injuries.md`)

**In split file but NOT in Master (7):** `deathsound`, `id`, `scars`, `stats`, `text`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `ROOT` (from `Item_Pools.md`)

**In split file but NOT in Master (46):** `Antidote`, `BagOfSeeds`, `BirdFeed`, `BirdPoopHat`, `Catnip`, `CatnipBig`, `Chicken`, `DeadHummingbird`, `FoodBig`, `FoodMedium`, `GlowingSeed`, `GoldenEgg`, `HarpysClaw`, `LostSoul`, `MagicSeed`, `Parousworm`, `PeaceSymbol`, `PeaceSymbolFacePaint`, `RaptorEgg`, `RavenFeather`, `TieDyeBandana`, `Turkey`, `WeirdEgg`, `WishBone`, `basic_consumables`, `chapter`, `chapter_common`, `chapter_rare`, `consumables`, `consumables_consumable_common`, `consumables_consumable_rare`, `consumables_consumable_uncommon`, `consumables_consumable_very_rare`, `current_chapter_common`, `current_chapter_rare`, `current_chapter_uncommon`, `current_chapter_very_rare`, `general_common`, `general_rare`, `general_uncommon`, `general_very_rare`, `pills`, `shop_common`, `uncommon`, `very_rare`, `{Event Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `AbilityHealthThreshold` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `also_use_if_buddy_is_dead`, `threshold`, `threshold_min`, `use_ai`

### `AddAdvantageToEvent` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `options`

### `AddPassivesToCharmed` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddMaxHealth`, `AddSpeed`, `AddStatusToBasicAttack`, `DamageUp`

### `AddPassivesToMinions` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (27):** `AddMaxHealth`, `AddSpeed`, `AddStatusToBasicAttack`, `AddStatusToExplosions`, `AddUnfilledMaxHealth`, `DamageUp`, `DivineShield`, `EMP`, `FamiliarBonusAbility`, `ForceAttack`, `FreePathfindElement`, `GrassTileHealing`, `HealthGain`, `HealthRegenUp`, `HolyShieldTransferToSpawner`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `PassiveWhenAffectedByElement`, `PoisonThorns`, `Quivered`, `SafeExplosions`, `StatusAlliesOnKill`, `StatusOnKill`, `TakeExtraTurn`, `UncappedHP`, `WaterWalk`, `tag_filter`

### `AddSelfStatusToBasicAttack` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `AddSelfStatusToWeapons` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ChanceToBreak`

### `AddStatusToAllDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `must_do_damage`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Blind`, `Conditional_HasTag`, `LeaveBehindRockOnKnockback`, `NonLethal`

### `AddStatusToBackstabs` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bleed`

### `AddStatusToBasicAttack` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (43):** `ApplyStatusIfCrit`, `ApplyToSource`, `BigSplashDamage`, `Bleed`, `Blind`, `BounceObject`, `Bruise`, `BurgleCoin`, `Burn`, `ChangeTile`, `Charmed`, `Conditional_Adjacent`, `Conditional_Ally`, `Conditional_Enemy`, `Conditional_HasTag`, `Conditional_Shielded`, `Conditional_SourceHasTag`, `Confusion`, `DamageOrHealConditionally`, `DistanceBonusDamage`, `Else`, `Fear`, `Freeze`, `KnockOutCoin`, `Knockback`, `Leech`, `Leeches`, `LuckUp`, `Madness`, `MagicWeakness`, `ManaLeeches`, `OverrideChainKnockback`, `OverrideChainKnockbackDamage`, `Piercing`, `Poison`, `Rot`, `Slow`, `SoulLink`, `SpawnBearTrapOnMiss`, `SplashDamage`, `SpreadDisease`, `Stun`, `Weakness`

### `AddStatusToElementDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Burn`, `Conditional_Corpse`

### `AddStatusToKnockbackDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bruise`

### `AddStatusToSpells` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LeechPercent`

### `AddStatusToWeapons` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Bleed`, `Cleave`, `LeechPercent`, `PullSourceToKnockbackImmuneTarget`

### `AddTemporaryEffectsToBasicAttack` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `CastAgainWithStatus`

**In Master but NOT in split file (2):** `CastAgain`, `Fury`

### `ApplyPassives` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `AddInitiative`, `AddTag`, `ElementImmune`, `Flying`, `IgnoreTiles`, `KnockbackImmunity`, `Plant`, `ReplaceBasicAttack`, `StatusOnBattleEnd`, `YOffset`

### `ApplyStatusesToRandomEnemiesEachTurn` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bounty`

### `ApplyToRandomPartyMemberIfPossible` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `GainDisorderFromPool`, `GainDisorderFromPool_PostCast`

### `ApplyToSource` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Shield`

### `AutocastEachRound` (from `Items_and_Equipment.md`)

**In Master but NOT in split file (1):** `force_display_name`

### `BoostWeaponDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `crit_chance`

### `CastAgainWithStatus` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `OverrideDamage`

### `CatchProjectiles` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Quivered`

### `ChanceToRevive` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `health`

**In Master but NOT in split file (1):** `statuses`

### `Conditional_Adjacent` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Bleed`, `BonusCritChance`, `BonusDamage`

### `Conditional_Ally` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `AllStatsUp`, `ApplyToSource`, `Cleanse`, `ClearNegativeEffects`, `DamageUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `TempSpeedUp`

### `Conditional_BadRoll` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Temporary`

### `Conditional_Boss` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `Stun`

### `Conditional_Corpse` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Charmed`, `DamageUp`, `OverrideDamage`, `Revive`, `SafeDoomed`, `SpeedUp`, `TakeExtraTurn`

### `Conditional_Enemy` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_PartyMember`, `Confusion`, `Else`, `RandomStatusFromPool`, `Stun`

### `Conditional_GoodRoll` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseRandomSpell_Madness`

### `Conditional_HasStatus` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

### `Conditional_HasTag` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `FlatLeechIfDamaged`

### `Conditional_HealthThreshold` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (14):** `ApplyToSource`, `BonusDamage`, `CaptureFamiliar`, `Conditional_OncePerBattle`, `Die`, `DieViolently`, `FactionConversion`, `FlatLeech`, `FullHeal`, `Instakill`, `SpawnThingIfHitKills`, `Vaporize`, `threshold_expr`, `threshold_percent`

### `Conditional_ManaThreshold` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RepairTrinket`

### `Conditional_OncePerBattle` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `CompleteItemQuest`, `ReduceManaCost`, `Shield`, `ShowText`, `SpellDamageUp`, `TriggerGameEnding`

### `Conditional_PartyMember` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charmed`

### `Conditional_PlayerCat` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `Adrenaline`, `ApplyToSource`, `Charge`, `Cleanse`, `ConjureRandomAbilityFromCat`, `GenericDebuff`, `KnockOutClone`, `Scrambled`, `T2CopyCat`

### `Conditional_RandomChance` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `ApplyPassives`, `AutoReanimate`

### `Conditional_Shielded` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `BonusCritChance`

### `ConvertDamageToScaledStatus` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DelayedPain`

### `CounterAttack` (from `Items_and_Equipment.md`)

**In Master but NOT in split file (2):** `chance`, `without_orienting`

### `Craft` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `works_with_tech`

### `CreateGlobalModifiers` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Global Modifier Keys}`

**In Master but NOT in split file (4):** `BloodRain`, `LowerAmbientLight`, `NextPlayerCatTakesExtraTurn`, `NoCorpses`

### `CritsApplyStatus` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `Bleed`, `Bruise`, `Conditional_HasStatus`, `Confusion`, `Else`, `Immobile`, `ObjectOnHitCharacter`, `Stun`, `Weakness`

### `DoDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `effects`, `elements`

### `Else` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `CaptureFamiliar`, `FactionConversion`, `Fear`, `Marked`, `PermanentCharm`, `TempSpeedUp`

### `Eternal` (from `Items_and_Equipment.md`)

**In Master but NOT in split file (2):** `AllStatsUp`, `TakeExtraTurn`

### `ExtraStatusWhenDealingDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Ally`

### `KnockUpAndAway` (from `Items_and_Equipment.md`)

**In Master but NOT in split file (4):** `circular_variance`, `displace`, `height`, `self_damage`

### `MeleeRevengeDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `knockback`, `{Damaging Keys}`

**In Master but NOT in split file (5):** `Poison`, `SpreadDisease`, `Weakness`, `effects`, `elements`

### `MovementReaction` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `create_temp_ability`, `on_self_move_too`

### `PassiveAfterXKills` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveAtHealthThreshold` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `threshold`

### `PassiveAtStatThreshold` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `threshold`

### `PassiveIfStrAuxEquals` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveIfWeaponIsUsable` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Brace`

### `PassiveWhenAffectedByElement` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhenDead` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddStatusToTrampleDamage`, `AutocastEachRound`, `StatusEachRoundEnd`, `StatusEachTurnBegin`

### `PassiveWhenOnTile` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhileHasDurability` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `MovementReaction`

### `PassiveWhileInMonkMeleeStance` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Brace`, `HealthRegenUp`

### `PassiveWhileShielded` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthRegenUp`

### `ROOT` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (61):** `Set`, `ability`, `attack`, `aux`, `aux_is_catid`, `cant_equip_to_colorless`, `cha`, `con`, `consumable`, `cursed`, `degrade_after_adventure`, `dex`, `divine_shield`, `dont_destroy_on_0`, `durability`, `equip_sound`, `failable`, `force_sticky`, `fragile`, `frame`, `global_passives`, `global_tags`, `hint_destination`, `hint_prerequisite_flag`, `icon_hint`, `indestructible`, `int`, `keyword_tooltips`, `kind`, `lck`, `legacy_quest`, `max_durability`, `max_health`, `on_store`, `parasite`, `passive`, `prevent_level_up`, `quest_item`, `quest_item_alias`, `quest_reward_item`, `randomize_piece_frames`, `rarity`, `reset_aux_on_store`, `reset_str_aux_on_store`, `set`, `shield`, `spd`, `speed`, `sticky`, `str`, `str_aux`, `str_aux_initialize`, `str_aux_is_copy_ability`, `str_aux_is_copy_item_active`, `str_aux_is_copy_item_icon`, `str_aux_is_copy_item_passive`, `str_aux_is_copy_passive`, `variant_of`, `weightless`, `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `RandomStatusFromPool` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (37):** `AllStatsUp`, `Bleed`, `BleedThorns`, `Blind`, `Brace`, `Bruise`, `Burn`, `Charge`, `Charmed`, `Confusion`, `ConstitutionUp`, `DiminishingHealthRegen`, `DivineShield`, `Fear`, `Freeze`, `Immobile`, `KineticSpikes`, `Madness`, `MagicWeakness`, `Marked`, `MoveQuivered`, `ObjectOnHitCharacter`, `Petrify`, `Poison`, `Quivered`, `Reflect`, `Shield`, `Sleep`, `Slow`, `SpawnCoinAnywhere`, `SpeedUp`, `StatusGroup`, `StrengthUp`, `Stun`, `Tarred`, `Thorns`, `Weakness`

### `RevengeDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (3):** `damage`, `elements`, `{Damaging Keys}`

**In Master but NOT in split file (2):** `effects`, `knockback`

### `ReviveNextRound` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `DivineShield`, `Shield`, `stacks`

### `ScaldingOrbMoonBossOneShot` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `CompleteItemQuest`, `RemoveItem`

### `ScaledStatusAlliesOnSpendMana` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Adjacent`

### `ScaledStatusOnHolyShieldBlock` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `ScaledStatusOnSpendMana` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RepressedMemoriesMetronome`

### `SpawnEachTurn` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `stack_key`

**In Master but NOT in split file (2):** `good`, `number`

### `SpawnExtraThingsOnBattleStart` (from `Items_and_Equipment.md`)

**In Master but NOT in split file (2):** `tile`, `trap`

### `SpawnOnDeath` (from `Items_and_Equipment.md`)

**In Master but NOT in split file (1):** `additional_statuses`

### `SpawnThingOnDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `chance`, `number`

**In Master but NOT in split file (1):** `consider_all_layers`

### `StatDependentPassive` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AddDamageToBasicAttack`

### `StatusAdjacentOnTheirTurnEnd` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `ForceMoveAway`

### `StatusAfterCastSpell` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `TempDamageUp`, `TempSpellDamageUp`

### `StatusAfterXStacks` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `ExtraBasicMoves_Status`, `RefreshActPoints`, `threshold`

### `StatusAfterXTurns` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `StatusAllCharactersOnSpawn` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_Boss`, `Conditional_PartyMember`, `Conditional_Tiny`, `Else`, `Poison`

### `StatusAlliesEachTurn` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `RandomStatUp`, `exclude_self`

### `StatusAlliesOnBattleStart` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `EquipTemporaryItem`

### `StatusAlliesOnDeath` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `AllStatsUp`, `Freeze`, `FullHeal`, `HealAndOverhealToShield`, `Reanimate`, `TakeExtraTurn`, `triggers_limit`

### `StatusEachRoundEnd` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddRandomEliteBuff`, `DoDamage`, `UseAbility`

### `StatusEachTurnBegin` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Conditional_BadRoll`, `Conditional_GoodRoll`, `Fear`, `FillMana`, `ForceUseAbility`, `IntelligenceUp`, `RandomStatUp`

### `StatusEachTurnEnd` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `EmptyMana`, `ForceUseAbility`, `IntelligenceUp`, `KineticSpikes`, `NonStackingDivineShield`, `ObjectOnHitCharacter`, `PermanentMadness`, `RangeUp`, `SpeedUp`, `StrengthUp`, `UseAbility_Madness`

### `StatusEachTurnEndForEachTurn` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `StatusEveryXSpellCasts` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `ReduceManaCost`, `RepairWeapon`, `RepairWeaponCondition`, `SpellDamageUp`

### `StatusIfUnusedActPoints` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `BackflipWhenTargeted`, `Craft`

### `StatusIfUnusedMovePoints` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `Brace`, `ConstitutionUp`, `HealthGain`, `ManaGain`, `MoveQuivered`, `Shield`

### `StatusOnAllyCatDeath` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `FillMana`, `HealthGain`, `PercentHeal`, `TakeExtraTurn`

### `StatusOnBackstab` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `StatusOnBattleEnd` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `CureDisease`, `FindItemFromPool`, `NextBattleStatus`, `PermanentConstitution`, `PermanentIntelligence`, `PermanentSpeed`, `PermanentStrength`, `RandomMutation`, `RandomPermanentStat`

### `StatusOnBattleStart` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `FullHeal`, `Sleep`

### `StatusOnBreak` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (15):** `ApplyToRandomPartyMemberIfPossible`, `Bruise`, `ChangeTilesUnder`, `ConstitutionUp`, `DexterityUp`, `FindItem`, `FindItemFromPool`, `GainCoinsRange`, `GainDisorder`, `HealthGain`, `HealthRegenUp`, `IntelligenceUp`, `ObjectOnHitCharacter`, `PermanentConstitution`, `StrengthUp`

### `StatusOnBreakItem` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Shield`, `Thorns`

### `StatusOnCastSpell` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Charge`, `CurrentWeaponDamageUp`, `HealthGain`

### `StatusOnCollectPickup` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Tech`

### `StatusOnDie` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `Conditional_RandomChance`, `CreateGlobalModifiers`, `FindItemFromPool`, `GainCoinsRange`, `RandomMagicMissile`, `RandomStatusFromPool`, `RemoveAmbientLightEffects`, `RemoveGlobalModifiers`, `ScatterCoins`, `StackingSandstorm`

### `StatusOnDodge` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DodgeChance_Status`

### `StatusOnEatFood` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Cleanse`, `IntelligenceUp`, `RandomStatUp`, `StrengthUp`

### `StatusOnEndMove` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceAttack`

### `StatusOnEnemyDeath` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charge`

### `StatusOnFallAsleep` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AllStatsUp`, `FillMana`, `HealRandomInjury`

### `StatusOnFullMana` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `Conditional_OncePerBattle`

### `StatusOnGainCoins` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DivineShield`, `RandomStatusFromPool`

### `StatusOnHealed` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `ObjectOnHitCharacter`, `RandomStatusFromPool`, `Thorns`

### `StatusOnKill` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `Conditional_FirstApplicationThisTurn`, `DamageUp`, `EquipPermanentItem`, `HealthGain`, `LuckUp`, `RandomStatUp`, `RefreshActPoints`, `RefreshMovePoints`, `SpeedUp`, `Stealth`, `StrengthUp`, `TakeBonusTurnWithStatus`

### `StatusOnKillEnemy` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `DivineShield`, `HealthGain`, `ManaGain`, `RefreshMovePoints`

### `StatusOnPickupCoins` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DexterityUp`, `RefreshMovePoints`, `SpeedUp`

### `StatusOnPopCorpse` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `StatusOnTakeHealthOrShieldDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_GoodRoll`, `DivineShield`, `Metronome`

### `StatusOnTookDamage` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (18):** `Conditional_HasStatus`, `ConstitutionUp`, `Craft`, `DamageUp`, `DiminishingHealthRegen`, `Else`, `IntelligenceUp`, `MovementUp`, `RandomInjury`, `RandomStatUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `StrengthUp`, `TempDamageUp`, `TempMovement`, `Temporary`, `Thorns`

### `StatusOnTurnEndIfDidntCastAbilityTypes` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ManaGain`

### `StatusOnUseBasicAttack` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `FlippedFacingForceAttack`

### `StatusRandomEnemiesOnBattleStart` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Bleed`, `Charmed`, `Confusion`, `Fear`, `Freeze`

### `StatusWhenAllySpendsMana` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ManaGain`, `OneUseSpellDamageUp`

### `TempPassiveUntilSettled` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `LimitHeal`, `MeleeRevengeDamage`

### `TunnelVision` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `crit_chance`

### `bonus_passives` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (75):** `AbilityDisableIfLivingCrow`, `AbilityEnableIfConsumedCharacterHasTag`, `AbilityEnabledAtHealthThreshold`, `AbilityEnabledIfBasicAttackUsedThisTurn`, `AbilityEnabledIfHasStatus`, `AbilityEnabledIfMovementTrapped`, `AbilityEnabledIfNoAggroTarget`, `AbilityEnabledIfNotHasStatus`, `AbilityEnabledIfSpecificItemEquipped`, `AbilityEnabledOncePerFightAtHealthThreshold`, `AbilityEnabledOncePerRound`, `AbilityEnabledPercentEachTurn`, `AbilityInheritsWeaponEffects`, `AbsorbManaFromOtherSpells`, `AddElementsToSpells`, `AddStatusToBasicAttack`, `AlphaDodgeChance`, `AlphaStatusOnTurnBegin`, `AutocastEachRound`, `BonusAbility_DelayedApplication`, `CapTechSpent`, `CatchBoomerang`, `CaveWomanBirthControl`, `ChargeSpiritBombAura`, `CopyBasicAttackEffects`, `CopyCatPassive_Initializer`, `CritChanceUp`, `DeadAltAbility`, `DownRankAIIfWeaponUsable`, `FistOfFateUniqueEnemyTracker`, `FreeFirstCast`, `FreeFirstCastAndAfterSpendMana`, `FreeFirstCastEachMatch`, `HealthRegenUp`, `IgnoreTiles`, `IntelligenceUp`, `InterchangeDisabler`, `KnockbackImmunity`, `ModifyAbility`, `MoonHeadFinisherEnabler`, `NukeQuestFinalBossModifications`, `PassiveWhileNotTakingTurn`, `ReloadOnAllyCatDies`, `ReloadOnAllyDies`, `ReloadOnAnyDamage`, `ReloadOnBackstab`, `ReloadOnElementalDamageReceived`, `ReloadOnGainCoins`, `ReloadOnGainDivineShield`, `ReloadOnKill`, `ReloadOnKillEnemy`, `ReloadOnKillTagged`, `ReloadOnSpendMana`, `ReloadOnTotalDamageReceived`, `ReloadOnUseAbilityWithManaCost`, `RevengeDamage`, `StatusKillers`, `TossTargetIsAggroTarget`, `TossTargetIsBuddy`, `TossTargetIsNotInWater`, `Trample`, `XIsConsumedCharacterMaxHP`, `XIsCountDeaths`, `XIsCountStatusStacks`, `XIsFormulaLockedUntilComplete`, `XIsFreeArmorSlots`, `XIsIncreaseEachTurn`, `XIsLivingAlliesWithTag`, `XIsLivingCharactersWithTag`, `XIsMultipliedPercentHealth`, `XIsOtherHealsThisTurn`, `XIsRampAndReset`, `XIsRecycleCostReduction`, `XIsSpellStormRampAndReset`, `XIsTimesDamageTaken`

### `cost` (from `Items_and_Equipment.md`)

**In Master but NOT in split file (41):** `X_cant_be_zero`, `act_points`, `allow_offmap_casts`, `can_be_refreshed`, `can_cast_while_dead`, `can_pay_over_multiple_turns`, `can_self_refresh`, `cant_cast`, `cantrip`, `cantrip_group`, `coins`, `damage_cant_be_zero`, `disallow_cost_modification`, `durability`, `enabled_formula`, `infcantrip`, `initial_charge`, `main_turn_only`, `manacost_cant_be_zero`, `minimum_con`, `minimum_spd`, `move_points`, `must_be_consuming`, `must_be_first_action`, `must_be_first_nonmove_action`, `must_be_offmap`, `must_have_weapon`, `must_not_be_a_summon`, `must_not_be_consuming`, `once_per_fight`, `prime`, `require_default_size`, `requires_attack_damage_threshold`, `requires_consumed_trinket`, `requires_destructible_weapon`, `requires_empty_trinket`, `requires_exact_character_aux`, `requires_hp_threshold`, `requires_reload`, `requires_weapon`, `start_reloaded`

### `damage_instance` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (37):** `HealthRegenUp`, `accuracy`, `ai_base_score`, `blocked_damage`, `blocked_multiplier`, `can_collect_pickups`, `can_instapop`, `can_revive`, `cant_miss`, `contact_requires_adjacency`, `crit_chance`, `custom_additional_ai_weight`, `damage_shield_only`, `disallow_modifications`, `effects`, `elements`, `faction`, `final_hit_bonus_damage`, `force_adjacent_and_diagonal_contact`, `force_no_contact`, `force_no_knockback`, `force_play_hit_animation`, `heal`, `hint_dont_lowgravboost`, `hit_animation_alt`, `incidentally_collects_pickups`, `knockback`, `layer`, `makes_contact`, `non_lethal`, `override_trample_damage`, `piercing`, `ranged`, `raw_damage`, `raw_heal`, `show_damage_on_0`, `two_way_contact`

### `effects` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `global_passives` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Global Modifier Keys}`

**In Master but NOT in split file (1):** `NoCorpses`

### `keyword_tooltips` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Weakness`

### `meta` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (2):** `is_basic_attack`, `is_weapon`

**In Master but NOT in split file (9):** `delay_enable_tooltips`, `house_shop`, `keeper`, `movieclip`, `npc_script`, `pick_n`, `shopkeeper_fights`, `treasure_room`, `welcome_message`

### `passive` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Metal`, `attack`

### `passives` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (424):** `AbilityOnBattleStart`, `AbilityReaction`, `AbilityWhenTaggedCharacterMovesNear`, `AbsorbManaAura`, `AddAllyNeighborsToAttackRange`, `AddBonusMeleeRange`, `AddBonusRange`, `AddCorpseHealth`, `AddCritMultiplier`, `AddDamageToBasicAttack`, `AddDamageToElementDamage`, `AddElementsToBasicAttack`, `AddHiddenTag`, `AddInitiative`, `AddKnockbackDamage`, `AddLevelUpRerolls`, `AddLevelUpStatMultiplier`, `AddManaRegen`, `AddMovement`, `AddPassiveToSpawnedRocks`, `AddPassivesToCharmed`, `AddPassivesToMinions`, `AddPassivesToSummonAbilityMinions`, `AddSelfStatusToBasicAttack`, `AddSelfStatusToWeapons`, `AddSpellDamage`, `AddStartingMana`, `AddStatusToAllDamage`, `AddStatusToBasicAttack`, `AddStatusToBasicAttackWithCooldown`, `AddStatusToBasicMeleeAttack`, `AddStatusToElementAbilities`, `AddStatusToElementDamage`, `AddStatusToExplosions`, `AddStatusToFirstBasicAttack`, `AddStatusToMeleeDamage`, `AddStatusToReceivedDamage_ExcludeStatuses`, `AddStatusToTrampleDamage`, `AddStatusToWeapons`, `AddStatusesIfPersistentWeatherElement`, `AddStatusesToReceivedElementalDamage`, `AddTag`, `AddTemporaryEffectsToBasicAttack`, `AddUnfilledMaxHealth`, `AddWeaponScaling`, `AfterImage`, `AllStatsUp`, `AllowPassTurn`, `AllyBonusAbilityAura`, `AllyDamageReaction`, `AllyDamageReduction`, `AllyHealthRegenAura`, `AllyManaRegenAura`, `AllyMoveAbilityAura`, `AllyMultiplyKnockbackDamage`, `AlphaTurns`, `AlternateCraftingPools`, `AmplifyKnockback`, `AmplifyPositiveStatus`, `AmplifyStatus`, `ApplyStatusesToRandomEnemiesEachTurn`, `Autism`, `AutoCritLowDamage`, `AutoEquipConsumables`, `AutocastEachRound`, `AutocastEachTurn`, `AutocastEachTurnBegin`, `BackstabCritChance`, `BackstabWeakness`, `BasicAttackAOEBonus`, `BasicAttackCritChance`, `BasicAttackDamageMultiplier`, `BasicAttackStatusCarefulness`, `BlacklistPickupType`, `BlastResistance`, `Bleed`, `BleedThorns`, `BonusAbility`, `BonusFoodEachBattle`, `BoobyTrapItems`, `BoostAllyStatsOnDeath`, `BoostDamageAura`, `BoostHeals`, `BoostRangeAura`, `BoostWeaponDamage`, `BouncyProjectiles`, `Brace`, `BraceForEachNeighboringEnemy`, `Bruise`, `BuffImmunity`, `Burn`, `CCImmunity`, `CanRemoveCursedItems`, `CantDodge`, `CapDamageFromAllies`, `CapMovementAbilityRange`, `CatAPultAnimation`, `CatchProjectiles`, `ChainKnockback`, `ChanceToBackflip`, `ChanceToBlockAndCounter`, `ChanceToRevive`, `ChangeTauntPriority`, `CharmAllFlies`, `ClassManaCostReduction`, `CobraReflex`, `CoinsAddDamage`, `CollectPickupsOnBattleEnd`, `Conductor`, `ConfusionEffectOnTaggedAbilities`, `ConjureCastSpellsForAllies`, `ConsumableEffectsMultiplierBonus`, `ConsumablesInfiniteRange`, `ConsumablesMeleeRange`, `CounterAttack`, `CritChanceUp`, `CritsApplyStatus`, `DamageEnemiesOnHeal`, `DamageEnemiesOnKill`, `DamageIfDidntUseSpecificAbility`, `DamageNeighborTilesWhenCastSpell`, `DamageNeighborsAfterMove`, `DamageNeighborsOnEndMove`, `DamageReductionAura`, `DamageUp`, `DeathChill`, `DeathRattle`, `DebuffImmunity`, `DejaVu`, `DepressionAura`, `Diabetes`, `DirtyClaws`, `DisableAbilities`, `DisableAbilitiesWithTag`, `DodgeChance`, `Doomed`, `DoubleCastWeapons`, `DukeOfFlies`, `Dyslexia`, `EMP`, `ElementImmune`, `ElementalAttunement`, `ElementalManaCostReduction`, `Empath`, `EnemiesGetPickupsKnockedOut`, `EnergyStorm`, `EquipTemporaryItem`, `EquipmentPassiveMultiplierBonus`, `EquipmentSetBonusBonus`, `EscapeSequence`, `Eternal`, `ExhaustionRoundChange`, `ExplodeOverkilledEnemies`, `ExtraBasicAttacks`, `ExtraBasicMoves_Status`, `ExtraInjuryOnDeath`, `ExtraMovePoints`, `ExtraStatusWhenDealingDamage`, `ExtraWeaponAttacks`, `FaceArmorPassiveMultiplierBonus`, `FaceShield`, `FamiliarSecondaryDamageImmunity`, `FlowerPowerAuraBrace`, `FlowerPowerAuraStrength`, `FlowersOnEndTurn`, `FlyDamageIncrease`, `Flying`, `FollowUp`, `ForceSpecificInjury`, `ForceUseAbility`, `FreePathfindElement`, `FreeSpellsAtFullMana`, `FreezePiercing`, `FrontstabBasicAttackCritChance`, `FullHeal`, `FullHealthCritChance`, `FullPower`, `FurnitureStats`, `GainExtraShield`, `GravityWell`, `HPGainBlock`, `HeadArmorPassiveMultiplierBonus`, `HealDamagesEnemies`, `HealsAlsoRegenMana`, `HealsCanRevive`, `HealthRegenUp`, `HolyShieldTransferToTaggedMinions`, `HouseFoodRequirementMultiplier`, `Hypomania`, `IgnoreTiles`, `ImmortalLeeches`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `IncreaseHealingSpellRange`, `IncreaseSpellRange`, `InfiniteRebirth`, `InnateElement`, `InvertBrainFaction`, `KillsHeal`, `KillsToMeat`, `KnockbackImmunity`, `LateBloomer`, `LevelUpClassOverride`, `LightningAspectCharge`, `LightningRod`, `LimitDamage`, `LimitHeal`, `LimitSelfKnockbackDamage`, `LimitedTileTrail`, `LineOfSightTrueSightAura`, `LobbedHook`, `LowHealthAllyDodgeChanceAura`, `Madness`, `MakeBasicAttackPassThroughThings`, `MakeSpellsRequireCharge`, `ManaCostReductionTagged`, `ManaRegenMultiplierIfManaEmpty`, `MaxAccuracy`, `MaxStartingMana`, `MegaMinions`, `MeleeRevengeDamage`, `Metal`, `MetalDetector`, `MinimumTech`, `MissChance`, `MoveAndUseAbilityEachTurnBeginIfPossible`, `MoveAwayFromDamageSource`, `MoveQuivered`, `MoveSpeedMultiplier`, `MoveTowardsDamageSource`, `MoveWhenDamaged`, `MovementReaction`, `MulticlassLevelUp`, `NeckArmorPassiveMultiplierBonus`, `NoManaRegen`, `NoReflection`, `NubbyTossPriority`, `NumbingLeeches`, `OverhealGainsBothShield`, `OverrideBasicAttack`, `OverrideMaxHealth`, `OverrideMaxMana`, `OverridePalette`, `Paranoia`, `ParasitesArentCursed`, `PassiveAfterXKills`, `PassiveAtFullHealth`, `PassiveAtHealthThreshold`, `PassiveAtInjuryThreshold`, `PassiveAtStatThreshold`, `PassiveIfAllArmorEmpty`, `PassiveIfEmptyFace`, `PassiveIfEmptyHead`, `PassiveIfEmptyNeck`, `PassiveLevelScaledStatus`, `PassiveLevelUpAtCombatEnd`, `PassiveUntilCastSpell`, `PassiveUntilGetKill`, `PassiveWhenAffectedByElement`, `PassiveWhenAtFullMana`, `PassiveWhenTheAlpha`, `PassiveWhileInMonkMeleeStance`, `PassiveWhileInMonkRangedStance`, `PassiveWhilePreviewingMonkRangedStance`, `PassiveWhileWearingMetal`, `PermanentImmobile`, `PermanentItems`, `PermanentKitten`, `PermanentMadness`, `Poison`, `PoisonThorns`, `PoopWhenHit`, `ProtectTargetedAllies`, `Quiver`, `Quivered`, `RandomPassivePool`, `RangedTrueShot`, `RealTimePressure_OneUnit`, `ReceivedStatusReplacement`, `RemoveLineOfSightRestrictions`, `RemoveOncePerFightRestriction`, `ReplaceBasicAttack`, `ReplaceBasicAttackWhenCastable`, `ReplaceBasicAttackWhenDead`, `ReplaceBasicMove`, `ReplaceSpawnedObjects`, `RevengeDamage`, `ReviveOnWin`, `RobotsInheritArmor`, `RockDetector`, `ScaledStatusOnBleedDamage`, `ScaledStatusOnOverMana`, `ScaledStatusOnSpendMana`, `SchrodingerDisorder`, `Scleroderma`, `SecurityBotProtect`, `SelfDamageWhenDealDamage`, `SetDefaultFacePassive`, `SetSpellCosts`, `ShareHealthRegen`, `SharePickups`, `ShoulderCheck`, `ShovingMatch`, `ShowHiddenThings`, `SizeScale`, `Slow`, `SmallEnemiesIgnoreYou`, `SmallRockBehavior`, `SmiteEnemiesWhoKill`, `SpawnCatCopyOnBattleStart`, `SpawnCreepOnHit`, `SpawnEachTurn`, `SpawnObjectOnPopCorpse`, `SpawnOnBattleStart`, `SpawnOnBattleStartRandomEmptyTile`, `SpawnThingOnDamage`, `SpawnThingOnDeath`, `SpecialFriends`, `SpeedUp`, `SplittableMove`, `SpreadExtraDebuffs`, `SpreadPainBonus`, `StatMinimum`, `StatsAtLowHealth`, `StatusAdjacentOnTheirTurnBegin`, `StatusAfterCastSpell`, `StatusAlliesOnBattleStart`, `StatusAlliesOnDeath`, `StatusAlliesOnGainCoins`, `StatusAlliesOnKill`, `StatusAllyWhenAllySpendsMana`, `StatusAnyCatAllyWhoKills`, `StatusDamagers`, `StatusEachTurnBegin`, `StatusEachTurnEnd`, `StatusEachTurnEndForEachTurn`, `StatusEachTurnEndPerEnemyKill`, `StatusEnemiesOnDeath`, `StatusEveryXSpellCasts`, `StatusEveryXTurnBegins`, `StatusIfBattleAlreadyBegan`, `StatusIfUnusedMovePoints`, `StatusImmunity`, `StatusKilledCharacters`, `StatusKillers`, `StatusOnAllyCatDeath`, `StatusOnAnyDeath`, `StatusOnBattleEnd`, `StatusOnBattleEndIfKillThresholdMet`, `StatusOnBattleStart`, `StatusOnBreakItem`, `StatusOnCastSpell`, `StatusOnCollectPickup`, `StatusOnCrit`, `StatusOnDealtDamage`, `StatusOnDealtDamageThreshold`, `StatusOnEatFood`, `StatusOnEatPill`, `StatusOnEndMove`, `StatusOnGainCoins`, `StatusOnGainShield`, `StatusOnHeal`, `StatusOnHealed`, `StatusOnKill`, `StatusOnKillEnemy`, `StatusOnLoseShield`, `StatusOnOverHealed`, `StatusOnOverMana`, `StatusOnPickupCoins`, `StatusOnPopCorpse`, `StatusOnStanceSwitch`, `StatusOnTakeHealthDamage`, `StatusOnTookDamage`, `StatusOnTookDamageFromAbility`, `StatusOnTookDamageFromEnemyAbility`, `StatusOnTriggerTrap`, `StatusOnTurnEndIfCastNSpells`, `StatusOnTurnEndIfDidntCastAbilityTypes`, `StatusOnTurnEndIfManaExact`, `StatusOnTurnEndIfManaOrHealthExact`, `StatusOnUseAbilityWithTag`, `StatusOnUseBasicAttack`, `StatusOnUseElementAbility`, `StatusPerInjury`, `StatusReplacement`, `StatusThingsKnockedBack`, `StatusWhenAllySpendsMana`, `Stealth`, `StrengthForEachNeighboringEnemy`, `StrengthInNumbersAura`, `StrengthUp`, `StrictLimitDamage`, `Study`, `TaggedPickupEffectReplacement`, `TauntAlways`, `TauntAtFullHealth`, `Tech`, `TempInitiativeChange`, `TheHunger`, `Thorns`, `TileDamageMultiplier`, `TileTrail`, `TourettesMeows`, `TowerDefense`, `TowerDefenseReflex`, `Trample`, `TrapEffectsMultiplier`, `TrinketActiveEffectsMultiplierBonus`, `TrinketPassiveMultiplierBonus`, `Triskaidekaphobia`, `UncappedHP`, `UncappedMana`, `UpgradeLevelUpClassActives`, `UpgradeLevelUpClassPassives`, `UpgradeSpawnedPickups`, `Vegan`, `Vengeful`, `WaterWalk`, `Weakness`, `WeaponActiveEffectsMultiplierBonus`, `WeaponCountsAsBasicAttack`, `WeaponDamageMultiplierBonus`, `WeaponPassiveMultiplierBonus`, `WobblyCat`

### `threshold` (from `Items_and_Equipment.md`)

**In split file but NOT in Master (1):** `con`

**In Master but NOT in split file (2):** `cha`, `spd`

### `ROOT` (from `Map_Generation_and_Routing.md`)

**In split file but NOT in Master (129):** `BoneyardUnlocked`, `BothObelisksUnlocked`, `BunkerUnlocked`, `CavesUnlocked`, `ChaosAntennaAttached`, `CoreObeliskUnlocked`, `CoreUnlocked`, `CraterUnlocked`, `DimensionXUnlocked`, `EndOfTimeUnlocked`, `FutureUnlocked`, `GenFlag_Boss_Spewer`, `GenFlag_Boss_Stacy`, `HardPathUnlocked`, `IceAgeUnlocked`, `JunkyardUnlocked`, `JurassicUnlocked`, `MeatWorldUnlocked`, `MeatWorldUnlockedFull`, `MoonObeliskUnlocked`, `MoonUnlocked`, `SewersUnlocked`, `TheEndUnlocked`, `ThrobbingArteryDone`, `VolcanoAntennaAttached`, `WallOfFleshDone`, `abandonedones`, `advance`, `alley`, `boneyard`, `boss`, `bumblefoot`, `bunker`, `butchercat`, `cancreeper`, `cavecatfamily`, `caves`, `cerberubs`, `chapter_item_pool`, `choose_one`, `clericcat`, `core`, `crater`, `desert`, `dimensionx`, `dinocouple`, `drmangler`, `druidcat`, `easy`, `endoftime`, `event`, `exit0`, `exit1`, `exit_desert`, `exit_lab`, `fightercat`, `flushmaster`, `folder`, `future`, `gambit`, `hard`, `hard_initial`, `head_start`, `home`, `huntercat`, `iceage`, `iceelemental`, `include`, `infestedduo`, `jestercat`, `junkyard`, `jurassic`, `lab`, `large`, `lenny`, `level`, `lightningelemental`, `locked`, `magecat`, `mamamaggot`, `meatworld`, `medium`, `miniboss`, `miniboss_event`, `monkcat`, `moon`, `musiclayer`, `mw_altar`, `mw_battle1`, `mw_boss`, `mw_earlyhome`, `mw_event1`, `mw_hard1`, `mw_home`, `mw_quest_event`, `mw_treasure`, `necrocat`, `nemesis`, `normal`, `override_art`, `psychiccat`, `queenhippo`, `quest_event`, `radicalrat`, `ratking`, `repeat`, `rockybobo`, `sewers`, `shop_cheapwater`, `shop_water`, `slime`, `small`, `spawn_node`, `special`, `spewer`, `stacy`, `tankcat`, `thebloat`, `theend`, `thiefcat`, `time_machine`, `tinkerercat`, `trampy`, `treasure`, `type`, `weather_event`, `zodiac`, `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `battle` (from `Map_Generation_and_Routing.md`)

**In Master but NOT in split file (5):** `DecayTime`, `ReverbDelay`, `amount`, `preset`, `volume_adjustment`

### `boss` (from `Map_Generation_and_Routing.md`)

**In Master but NOT in split file (4):** `coins`, `consumable_chance`, `food`, `item_chance`

### `future` (from `Map_Generation_and_Routing.md`)

**In Master but NOT in split file (6):** `animation`, `good`, `hint_chapter_exit`, `label`, `requirements`, `stat`

### `home` (from `Map_Generation_and_Routing.md`)

**In Master but NOT in split file (5):** `animation`, `good`, `hint_chapter_exit`, `label`, `stat`

### `treasure` (from `Map_Generation_and_Routing.md`)

**In split file but NOT in Master (2):** `level`, `type`

**In Master but NOT in split file (1):** `Item`

### `AbilityHealthThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `AbilityReaction` (from `Miscellaneous.md`)

**In split file but NOT in Master (9):** `backstabs_only`, `cancel_knockback`, `enemies_only`, `even_on_0_damage`, `even_on_0_damage_if_knockback`, `match_knockback_direction`, `only_when_not_your_turn`, `ranged_only`, `verify_target`

### `AddAdvantageToEvent` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `options`

### `AddPassivesToCharmed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddMaxHealth`, `AddSpeed`, `AddStatusToBasicAttack`, `DamageUp`

### `AddPassivesToMinions` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (27):** `AddMaxHealth`, `AddSpeed`, `AddStatusToBasicAttack`, `AddStatusToExplosions`, `AddUnfilledMaxHealth`, `DamageUp`, `DivineShield`, `EMP`, `FamiliarBonusAbility`, `ForceAttack`, `FreePathfindElement`, `GrassTileHealing`, `HealthGain`, `HealthRegenUp`, `HolyShieldTransferToSpawner`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `PassiveWhenAffectedByElement`, `PoisonThorns`, `Quivered`, `SafeExplosions`, `StatusAlliesOnKill`, `StatusOnKill`, `TakeExtraTurn`, `UncappedHP`, `WaterWalk`, `tag_filter`

### `AddPassivesToSummonAbilityMinions` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DamageUp`, `Doomed`, `MovementUp`

### `AddSelfStatusToBasicAttack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `AddSelfStatusToWeapons` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ChanceToBreak`

### `AddStatusToAllDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `must_do_damage`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Blind`, `Conditional_HasTag`, `LeaveBehindRockOnKnockback`, `NonLethal`

### `AddStatusToAllDamageAbilities` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Bleed`, `Piercing`, `Weakness`

### `AddStatusToBackstabs` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bleed`

### `AddStatusToBasicAttack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (43):** `ApplyStatusIfCrit`, `ApplyToSource`, `BigSplashDamage`, `Bleed`, `Blind`, `BounceObject`, `Bruise`, `BurgleCoin`, `Burn`, `ChangeTile`, `Charmed`, `Conditional_Adjacent`, `Conditional_Ally`, `Conditional_Enemy`, `Conditional_HasTag`, `Conditional_Shielded`, `Conditional_SourceHasTag`, `Confusion`, `DamageOrHealConditionally`, `DistanceBonusDamage`, `Else`, `Fear`, `Freeze`, `KnockOutCoin`, `Knockback`, `Leech`, `Leeches`, `LuckUp`, `Madness`, `MagicWeakness`, `ManaLeeches`, `OverrideChainKnockback`, `OverrideChainKnockbackDamage`, `Piercing`, `Poison`, `Rot`, `Slow`, `SoulLink`, `SpawnBearTrapOnMiss`, `SplashDamage`, `SpreadDisease`, `Stun`, `Weakness`

### `AddStatusToBasicAttackWithCooldown` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `CharmedForceAttack`

### `AddStatusToBasicMeleeAttack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Bruise`, `Confusion`, `FaceAway`, `SpreadDisease`, `Stun`

### `AddStatusToElementAbilities` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Bleed`, `ChangeTile`, `Conditional_Ally`, `Conditional_Enemy`

### `AddStatusToElementDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Burn`, `Conditional_Corpse`

### `AddStatusToExplosions` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `AddStatusToFirstBasicAttack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charmed`

### `AddStatusToFirstSpellEachTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Conditional_IsSelf`, `Else`

### `AddStatusToKnockbackDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bruise`

### `AddStatusToMeleeDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `DelayedWindCone`

### `AddStatusToReceivedDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Else`

### `AddStatusToSpells` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LeechPercent`

### `AddStatusToTrampleDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Cleave`

### `AddStatusToWeapons` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Bleed`, `Cleave`, `LeechPercent`, `PullSourceToKnockbackImmuneTarget`

### `AddStatusesIfPersistentWeatherElement` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `AddStatusesToReceivedElementalDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `AddTemporaryEffectsToBasicAttack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `CastAgainWithStatus`

### `AdventureTokenPassivePool` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (12):** `StacyMutant_Brace`, `StacyMutant_Counter`, `StacyMutant_Damage`, `StacyMutant_DoubleHead`, `StacyMutant_Fire`, `StacyMutant_Health`, `StacyMutant_Holy`, `StacyMutant_Ice`, `StacyMutant_Lightning`, `StacyMutant_Mirror`, `StacyMutant_Speed`, `StacyMutant_Thorns`

### `Alert` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `AllAlive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `AlphaStatusOnTurnBegin` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DoubleCastSpellThisTurn`

### `ApplyMultipleTimes` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomStatusFromPool`

### `ApplyPassives` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `AddInitiative`, `AddTag`, `ElementImmune`, `Flying`, `IgnoreTiles`, `KnockbackImmunity`, `Plant`, `ReplaceBasicAttack`, `StatusOnBattleEnd`, `YOffset`

### `ApplyPassivesToSpawnerWhileAlive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HideEquipment`

### `ApplyStatusIfCrit` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Purge`

### `ApplyStatusesNextTurnBegin` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Quivered`

### `ApplyStatusesToRandomEnemiesEachTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bounty`

### `ApplyToConsumed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `DeleteObject`, `Die`

### `ApplyToOthersWithSharedTagAndFaction` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Marked`

### `ApplyToRandomClosestAlly` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `ForceMoveTowards`

### `ApplyToRandomPartyMemberIfPossible` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `GainDisorderFromPool`, `GainDisorderFromPool_PostCast`

### `ApplyToSource` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Shield`

### `ApplyToSourceOnKill` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `AlphaCat`, `CompleteItemQuest`, `EvolveAbilityFromPool`, `HealthGain`, `ManaGain`, `RefreshActPoints`, `RemoveItem`, `Revive`, `StrengthUp`, `TakeExtraTurn`, `TransformWeapon`, `WeaponAuxMultiplier`

### `ApplyToTile` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `ObjectOnHit`, `SpawnBearTrap`

### `BellyFull` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Big` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `BigHolding` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `BigHoldingCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Bishop` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `name`, `passives`, `tooltip`, `uifloaters_offset`

### `BlackHole` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `Bomb` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `BoostWeaponDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `crit_chance`

### `Boris` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `BossRewards` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `common`, `rare`

### `Bully` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `CanApplyToInanimate` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `ApplyToSource`, `ObjectOnHitCharacter`, `Temporary`, `Vaporize`

### `CastAgainWithStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `OverrideDamage`

### `Cat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `CatAPultAnimation` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `CatPartsTransform` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `palette`

### `CatchProjectiles` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Quivered`

### `CaveBaby` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveMan` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveManSpear` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveWoman` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CaveWomanHasCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `ChanceToRevive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `health`

### `ChangeTile` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `chance`

### `CharacterTypeGainsStatusAtBattleStart` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Conditional_Flying`, `Else`, `Fear`, `Stealth`, `Stun`

### `Charging` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Close` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `CollectsPickupsWithAltEffects` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `LuckUp`, `Quivered`, `RandomStatUp`, `Shield`, `Tech`

### `Conditional_ActiveWeather_Any` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DestroyEquipmentAndAttachParasite`

### `Conditional_Adjacent` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Bleed`, `BonusCritChance`, `BonusDamage`

### `Conditional_AffectedByElement` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `BonusCritChance`, `Burn`, `Conditional_Speculative`

### `Conditional_Ally` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `AllStatsUp`, `ApplyToSource`, `Cleanse`, `ClearNegativeEffects`, `DamageUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `TempSpeedUp`

### `Conditional_Backstab` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `BonusCritChance`, `Fear`

### `Conditional_BadRoll` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Temporary`

### `Conditional_Boss` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `Stun`

### `Conditional_BossOrBig` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Immobile`

### `Conditional_Buddy` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_InForm`, `Consumed`, `Else`

### `Conditional_CanBeHealed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomStatusFromPool`

### `Conditional_Corpse` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Charmed`, `DamageUp`, `OverrideDamage`, `Revive`, `SafeDoomed`, `SpeedUp`, `TakeExtraTurn`

### `Conditional_DebuffRoll` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DestroyEquipmentAndAttachParasite`

### `Conditional_DestructibleCorpse` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `ApplyToTile`, `VaporizeCorpse`

### `Conditional_Displaceable` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `LaunchOffScreen`, `LaunchOffScreenInstakill`, `TempInitiativeChange`

### `Conditional_DoesDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bleed`

### `Conditional_Enemy` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_PartyMember`, `Confusion`, `Else`, `RandomStatusFromPool`, `Stun`

### `Conditional_Familiar` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `BonusDamage`, `DamageUp`, `DivineShield`

### `Conditional_FinishedSpawning` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `Imprison`

### `Conditional_FirstApplicationThisTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `key`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FillMana`, `ManaGain`, `TakeExtraTurn`

### `Conditional_FormulaIsPositive` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (8):** `Burn`, `Freeze`, `Immobile`, `OverrideKnockbackDamage`, `Shield`, `Slow`, `SpeedUp`, `Stun`

### `Conditional_GoodRoll` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseRandomSpell_Madness`

### `Conditional_HasCleansableDebuffs` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `GenericBuff`, `PartialCleanse`, `RandomStatusFromPool`, `VisualFX`

### `Conditional_HasKnockback` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `KnockUpAndAway`, `RemoveKnockback`, `TempPassiveUntilSettled`

### `Conditional_HasStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

### `Conditional_HasTag` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `FlatLeechIfDamaged`

### `Conditional_HealthThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (12):** `ApplyToSource`, `BonusDamage`, `CaptureFamiliar`, `Conditional_OncePerBattle`, `Die`, `DieViolently`, `FactionConversion`, `FlatLeech`, `FullHeal`, `Instakill`, `SpawnThingIfHitKills`, `Vaporize`

### `Conditional_InForm` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `CritChanceUp`, `DamageUp`, `DodgeChance_Status`, `ForceImmediateMoveAndAttack`, `FormChange`, `SpeedUp`, `UseAbility`

### `Conditional_IsPhysicalAttack` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `KnockUpAndAway`, `RemoveKnockback`, `TempPassiveUntilSettled`

### `Conditional_IsSelf` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `OverrideDamage`

### `Conditional_IsTrample` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `SetKnockback`

### `Conditional_LastHit` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `BonusDamage`, `Bruise`, `DelayCastAbility`, `KnockUpAndAway`

### `Conditional_LivingPlayerCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `ApplyToSource`, `Consumed`, `TempPassiveWhileHasStatus`

### `Conditional_ManaThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RepairTrinket`

### `Conditional_NotAlly` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Confusion`, `Temporary`

### `Conditional_NotBig` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `DisplaceTowardsSource`

### `Conditional_NotBoss` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Enemy`

### `Conditional_NotBossOrBig` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Immobile`

### `Conditional_NotShielded` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Knockback`

### `Conditional_Object` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `CanApplyToInanimate`, `Conditional_HasTag`, `Else`, `RepairWeapon`

### `Conditional_OncePerBattle` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `CompleteItemQuest`, `ReduceManaCost`, `Shield`, `ShowText`, `SpellDamageUp`, `TriggerGameEnding`

### `Conditional_PartyMember` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charmed`

### `Conditional_PlayerCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `Adrenaline`, `ApplyToSource`, `Charge`, `Cleanse`, `ConjureRandomAbilityFromCat`, `GenericDebuff`, `KnockOutClone`, `Scrambled`, `T2CopyCat`

### `Conditional_RandomChance` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ApplyPassives`, `AutoReanimate`

### `Conditional_Shielded` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `BonusCritChance`

### `Conditional_SourceAbilityHasTag` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ApplyToSource`, `ScatterCoins`

### `Conditional_SourceHasStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bruise`

### `Conditional_SourceHasTag` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Ally`

### `Conditional_Speculative` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (8):** `BonusDamage`, `BonusDamageBasedOnDistance`, `CapDamage`, `Conditional_HealthThreshold`, `Else`, `IgnoreDamage`, `Knockback`, `RandomBonusDamage`

### `Consumed` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (12):** `do_not_pop_corpse`, `drop_body_ability`, `drop_on_death`, `drop_on_self_death`, `extra_statuses`, `force_contact`, `instant`, `kill_on_consume`, `mount_mode`, `struggle_ability`, `use_placeholder`, `wet`

### `ConvertDamageToScaledStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DelayedPain`

### `Craft` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `temporary`, `works_with_tech`

### `CreateGlobalModifiers` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Global Modifier Keys}`

**In Master but NOT in split file (4):** `BloodRain`, `LowerAmbientLight`, `NextPlayerCatTakesExtraTurn`, `NoCorpses`

### `CritsApplyStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `Bleed`, `Bruise`, `Conditional_HasStatus`, `Confusion`, `Else`, `Immobile`, `ObjectOnHitCharacter`, `Stun`, `Weakness`

### `Cultist` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `CyborgTurns` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `TakeBonusTurnWithAIControl`

### `DamageNeighborsAfterMove` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `DamageNeighborsOnEndMove` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `cant_miss`, `effects`

### `DeathRattle` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `cancel_knockback`, `immediate`, `is_dying_animation`, `must_target_killer`, `target_killer`

### `Default` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Default_Ceiling` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Default_Ground` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `DelayedWindCone` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `damage`

### `Diabetes` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Confusion`

### `Die` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `DiesToElement` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `instant`

### `DistanceBonusDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `min_range`

### `DoDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `Down` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `DualSword` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `move_speed_multiplier`, `passives`, `tooltip`

### `DualSword_Primed` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `move_speed_multiplier`, `passives`, `tooltip`

### `Dumb` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Electric` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Stun`

### `Else` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `CaptureFamiliar`, `FactionConversion`, `Fear`, `Marked`, `PermanentCharm`, `TempSpeedUp`

### `EscapeSequence` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `RandomDistanceDisplace`

### `Eternal` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `TakeExtraTurn`

### `Explody` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Explosive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ExtraStatusWhenDealingDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Ally`

### `FactionUprising` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `extra_statuses`

### `FightPhase` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FinalBossBecomeTheChild` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (3):** `GlobalSpawnCharacter`, `PlayBackground`, `SwitchMusic`

### `FinalBossHitCountdownBoris` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `FinalBossHitCountdownExplosive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `Fire` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `ai`, `attack`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `FireFull` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Floor1_Large` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `Floor1_Small` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `Flop` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Flop2` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FlushBubs` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FlushHost` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `FlushNettle` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Food` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `weight`

### `ForceUseAbility` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `show_name`

### `FormChangeHealthThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `FormChangeOnElementInfluence` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `particle`

### `FormChanger` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `{Graphics Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Die`, `Rain`, `passives`, `uifloaters_offset`

### `Full` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `GlobalFlowerTrapperAura` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Tangled`

### `Grass` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Poison`

### `Gravity` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Weakness`

### `GravityWell` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `cant_miss`, `effects`

### `Grown` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `uifloaters_offset`

### `GuaranteedJackpot` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Guarding` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HalfDead` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HasCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HasDeadCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Headless` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `HitlerExecute` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `Holding` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Holy` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `animation_suffix`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `FlatLeech`

### `HolyDamageBlessing` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `HumanDead` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `tooltip`

### `Ice` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Slow`

### `InfiniteRebirth` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `immediate`, `{Logic Keys}`

**In Master but NOT in split file (1):** `TempSpeedUp`

### `InitialPhase` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Insane_Ceiling` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Insane_Ground` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Item` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `weight`

### `JohnnyBubs` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `JohnnyHost` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `JohnnyNettle` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Joystick` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `KnockUpAndAway` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `self_damage`

### `LateBloomer` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AllStatsUp`

### `LateStatusApplication` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AddWeaponAux`, `CurrentWeaponDamageUp`

### `Lifted` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `LightningRod` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Tech`

### `Lit` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Math` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ApplyToSource`, `Stun`

### `MeleeRevengeDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (4):** `knockback`, `type`, `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Poison`, `SpreadDisease`, `Weakness`, `effects`

### `MergeDamageInstance` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `can_instapop`

### `ModularPickup` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Cleanse`

### `MouthFull` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `MoveTowardsDamageSource` (from `Miscellaneous.md`)

**In split file but NOT in Master (8):** `ability`, `can_move_zero`, `check_has_status`, `check_in_form`, `do_not_move_on_top`, `face_towards_after`, `ignore_tagged_sources`, `move_short`

### `MoveWhenDamaged` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `move_ability`

### `MovementReaction` (from `Miscellaneous.md`)

**In split file but NOT in Master (6):** `blind_spot`, `create_temp_ability`, `forward_only`, `objects_too`, `on_self_move_too`, `self_move_exclude_self_abilities`

### `Mutant` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `move_speed_multiplier`, `name`, `passives`, `tooltip`

### `NeutronStar` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `NextBasicAttackCritsThisTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `cant_miss`, `piercing`

### `NextBattleStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `FullHeal`

### `NextBattleStatusStacks` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `MadnessChanceOnTurnBegin`

### `NonCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `Normal` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `NormalFull` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `NotPriming` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Nothing` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `Nuke` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `NukeQuestFinalBossModifications` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `self_damage`

### `Obey` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ObjectOnHitCharacter` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `chance`

### `OffScreen` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OneAlive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OneEye` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Open` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OpenCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Out` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `OverHealToStatuses` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `RandomStatUp`, `TakeExtraTurn`

### `ParticleRandomForce` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `end`

### `PassiveAfterXKills` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveAtFullHealth` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ManaCostReduction`

### `PassiveAtHealthThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `threshold`

### `PassiveAtInjuryThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `injury`, `passives`, `threshold`

### `PassiveAtStatThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `threshold`

### `PassiveGroup` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `CharismaUp`, `IntelligenceUp`, `SetDefaultFace`, `SpeedUp`

### `PassiveIfAllArmorEmpty` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `AddSpellDamage`, `CounterAttack`, `CritsApplyStatus`, `ExtraMovePoints`, `Flying`, `ManaCostReduction`, `StatusOnStanceSwitch`

### `PassiveIfEmptyFace` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddCritMultiplier`, `CritChanceUp`, `DodgeChance`, `KineticSpikes`, `StatusOnStanceSwitch`

### `PassiveIfEmptyHead` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddCritMultiplier`, `CritChanceUp`, `DodgeChance`, `KineticSpikes`, `StatusOnStanceSwitch`

### `PassiveIfEmptyNeck` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddCritMultiplier`, `CritChanceUp`, `DodgeChance`, `KineticSpikes`, `StatusOnStanceSwitch`

### `PassiveIfStrAuxEquals` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveIfWeaponIsUsable` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Brace`

### `PassiveLevelScaledStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Shield`, `Trample`

### `PassiveUntilCastSpell` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `StatusAlliesEachTurn`

### `PassiveWhenAffectedByElement` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhenAtFullMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddMovement`, `AddStatusToBasicAttack`, `Brace`, `Flying`, `ReplaceBasicMove`

### `PassiveWhenDead` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddStatusToTrampleDamage`, `AutocastEachRound`, `StatusEachRoundEnd`, `StatusEachTurnBegin`

### `PassiveWhenOnTile` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhileHasDurability` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `MovementReaction`

### `PassiveWhileHasStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhileInMonkMeleeStance` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Brace`, `HealthRegenUp`

### `PassiveWhileInMonkRangedStance` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddBonusRange`, `AddSpellDamage`, `KineticSpikes`

### `PassiveWhileNotHasStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhileNotTakingTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AddStatusToBasicAttack`

### `PassiveWhilePreviewingMonkRangedStance` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AddBonusRange`

### `PassiveWhileShielded` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthRegenUp`

### `PopAndSpawn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `no_splatter`

### `Possessing` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Primed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Priming` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Pulp2` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp3` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp4` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp5` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp6` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `Pulp7` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `passives`, `tooltip`, `uifloaters_offset`

### `ROOT` (from `Miscellaneous.md`)

**In split file but NOT in Master (1526):** `Antidote`, `Appeal`, `BagOfSeeds`, `BasementUpgrade`, `BasementUpgrade2`, `BasementUpgrade3`, `BasementUpgrade4`, `BasementUpgrade5`, `BirdFeed`, `BirdPoopHat`, `BlankTile`, `BoneyardUnlocked`, `BothObelisksUnlocked`, `BreedSuppression`, `BunkerUnlocked`, `Butcher`, `Catnip`, `CatnipBig`, `CavesUnlocked`, `ChaosAntennaAttached`, `Chicken`, `Colorless`, `Colorless_Tutorial`, `Comfort`, `CompletionCheckmarkTooltip`, `CoreObeliskUnlocked`, `CoreUnlocked`, `CraterUnlocked`, `DeadHummingbird`, `Default`, `DimensionXUnlocked`, `Druid`, `EndOfTimeUnlocked`, `Evolution`, `FightBonusRewards`, `FightRisk`, `Fighter`, `Floor1_Large`, `Floor1_Small`, `FoodBig`, `FoodMedium`, `FoodStorage`, `FutureUnlocked`, `GenFlag_Boss_Spewer`, `GenFlag_Boss_Stacy`, `GlowingSeed`, `GoldenEgg`, `GrassTile`, `HardPathUnlocked`, `HarpysClaw`, `Health`, `House1`, `House2`, `House3`, `Hunter`, `ID`, `IceAgeUnlocked`, `Jack_Gainaltfurniture`, `Jester`, `JunkyardUnlocked`, `JurassicUnlocked`, `LargeHouse`, `LargeHouse_Floor2Large`, `LargeHouse_Floor2Small`, `LostSoul`, `Mage`, `MagicSeed`, `MeatWorldUnlocked`, `MeatWorldUnlockedFull`, `Medic`, `MediumHouse`, `MediumHouse_SmallRoom`, `Monk`, `MoonObeliskUnlocked`, `MoonUnlocked`, `Necromancer`, `One_Cat`, `One_Cat_EmptyHouse`, `Parousworm`, `PeaceSymbol`, `PeaceSymbolFacePaint`, `Plural_Team`, `Plural_Team_EmptyHouse`, `Psychic`, `RaptorEgg`, `RavenFeather`, `Set`, `SewersUnlocked`, `Singlular_Team`, `Singlular_Team_EmptyHouse`, `SmallAttic`, `SmallCompletionCheckmarkTooltip`, `SmallHouse_Attic`, `Stimulation`, `TallGrassTile`, `Tank`, `TheEndUnlocked`, `Thief`, `ThrobbingArteryDone`, `Thunderstorm`, `TieDyeBandana`, `Tinkerer`, `Turkey`, `VolcanoAntennaAttached`, `WallOfFleshDone`, `WeirdEgg`, `WishBone`, `abandonedones`, `abilities`, `ability`, `ability_groups`, `ability_pool`, `accurate_knockback`, `act`, `adjectives`, `advance`, `adventure_unlock`, `ai`, `ai_ability`, `ai_if_spawned_as_enemy`, `alias`, `alley`, `alpha`, `alpha_end`, `alpha_in`, `alpha_out`, `alpha_start`, `also`, `alt_spawn_pool`, `ambient_sound`, `amount`, `angry`, `animation_fail`, `animation_suffix`, `ankylosaurus`, `areas`, `arm1`, `arm2`, `arrival_unlock`, `asymmetric`, `attack`, `attack_pool`, `auto_plus_signs_on_name`, `aux`, `aux_is_catid`, `back`, `back_icon`, `background_extra_shader`, `background_shader`, `barf`, `barf_attack`, `barf_prep`, `base_stats`, `basic_consumables`, `beanies_begin_accepting_cats`, `beanies_bombquest_2`, `beanies_bombquest_3`, `beanies_bombquest_amnesia`, `beanies_bombquest_begin`, `beanies_bombquest_fail_jarofblood`, `beanies_bombquest_fail_jarofchaos`, `beanies_bombquest_fail_jarofradiation`, `beanies_bombquest_fail_nuke`, `beanies_future_intro`, `beanies_hitler3`, `beanies_hitler3_defeat`, `beanies_iloveyou`, `beanies_infinite_intro`, `beanies_jurassic_intro`, `beanies_lab_intro`, `beanies_quest_complete`, `beanies_quest_fail`, `beanies_quests_intro`, `beanies_quests_repeat`, `beanies_rift_intro`, `beanies_screenshake_test`, `beanies_seefuture`, `beanies_seetheend`, `beanies_terminator1_defeat`, `beanies_terminator2_defeat`, `beanies_theend_intro`, `beanies_timemachine_2`, `beanies_timemachine_intro`, `beanies_vscreator1`, `beanies_vscreator2`, `beanies_vscreator3`, `beanies_vscreator4`, `beanies_vscreatorintro`, `beaniesquest_complete_AI`, `beaniesquest_complete_AirHorn`, `beaniesquest_complete_AngryFace`, `beaniesquest_complete_AnimalHands`, `beaniesquest_complete_BubbleBoy`, `beaniesquest_complete_ChadImplant`, `beaniesquest_complete_ChaosDevice`, `beaniesquest_complete_DimensionalDivider`, `beaniesquest_complete_DiseaseJar`, `beaniesquest_complete_ExperimentalTreatment`, `beaniesquest_complete_FartFace`, `beaniesquest_complete_FigLeaf`, `beaniesquest_complete_Generic`, `beaniesquest_complete_GlassCannon`, `beaniesquest_complete_HardPill`, `beaniesquest_complete_HiveMind`, `beaniesquest_complete_MagicMirror`, `beaniesquest_complete_MeStone`, `beaniesquest_complete_MultilinkCable`, `beaniesquest_complete_MysteriousDice`, `beaniesquest_complete_MysteriousGlasses`, `beaniesquest_complete_NDEDevice`, `beaniesquest_complete_NuclearKnife`, `beaniesquest_complete_PartialLobotomy`, `beaniesquest_complete_PartyDetonator`, `beaniesquest_complete_PersonalHeater`, `beaniesquest_complete_PersuasionDevice`, `beaniesquest_complete_PrincessHat`, `beaniesquest_complete_RealityScrambler`, `beaniesquest_complete_Redacted`, `beaniesquest_complete_SpiderInjector`, `beaniesquest_complete_Stopwatch`, `beaniesquest_complete_StorageLocker`, `beaniesquest_complete_TheIOU`, `beaniesquest_complete_TheLoner`, `beaniesquest_complete_Trapfest99`, `beaniesquest_complete_UltraVision3000`, `beaniesquest_fail_AI`, `beaniesquest_fail_AirHorn`, `beaniesquest_fail_AngryFace`, `beaniesquest_fail_AnimalHands`, `beaniesquest_fail_BubbleBoy`, `beaniesquest_fail_ChadImplant`, `beaniesquest_fail_ChaosDevice`, `beaniesquest_fail_DimensionalDivider`, `beaniesquest_fail_DiseaseJar`, `beaniesquest_fail_ExperimentalTreatment`, `beaniesquest_fail_FartFace`, `beaniesquest_fail_FigLeaf`, `beaniesquest_fail_Generic`, `beaniesquest_fail_GlassCannon`, `beaniesquest_fail_HardPill`, `beaniesquest_fail_HiveMind`, `beaniesquest_fail_MagicMirror`, `beaniesquest_fail_MeStone`, `beaniesquest_fail_MultilinkCable`, `beaniesquest_fail_MysteriousDice`, `beaniesquest_fail_MysteriousGlasses`, `beaniesquest_fail_NDEDevice`, `beaniesquest_fail_NuclearKnife`, `beaniesquest_fail_PartialLobotomy`, `beaniesquest_fail_PartyDetonator`, `beaniesquest_fail_PersonalHeater`, `beaniesquest_fail_PersuasionDevice`, `beaniesquest_fail_PrincessHat`, `beaniesquest_fail_RealityScrambler`, `beaniesquest_fail_Redacted`, `beaniesquest_fail_SpiderInjector`, `beaniesquest_fail_Stopwatch`, `beaniesquest_fail_StorageLocker`, `beaniesquest_fail_TheIOU`, `beaniesquest_fail_TheLoner`, `beaniesquest_fail_Trapfest99`, `beaniesquest_fail_UltraVision3000`, `beaniesquest_intro_AI`, `beaniesquest_intro_AirHorn`, `beaniesquest_intro_AngryFace`, `beaniesquest_intro_AnimalHands`, `beaniesquest_intro_BubbleBoy`, `beaniesquest_intro_ChadImplant`, `beaniesquest_intro_ChaosDevice`, `beaniesquest_intro_DimensionalDivider`, `beaniesquest_intro_DiseaseJar`, `beaniesquest_intro_ExperimentalTreatment`, `beaniesquest_intro_FartFace`, `beaniesquest_intro_FigLeaf`, `beaniesquest_intro_Generic`, `beaniesquest_intro_GlassCannon`, `beaniesquest_intro_HardPill`, `beaniesquest_intro_HiveMind`, `beaniesquest_intro_MagicMirror`, `beaniesquest_intro_MeStone`, `beaniesquest_intro_MultilinkCable`, `beaniesquest_intro_MysteriousDice`, `beaniesquest_intro_MysteriousGlasses`, `beaniesquest_intro_NDEDevice`, `beaniesquest_intro_NuclearKnife`, `beaniesquest_intro_PartialLobotomy`, `beaniesquest_intro_PartyDetonator`, `beaniesquest_intro_PersonalHeater`, `beaniesquest_intro_PersuasionDevice`, `beaniesquest_intro_PrincessHat`, `beaniesquest_intro_RealityScrambler`, `beaniesquest_intro_Redacted`, `beaniesquest_intro_SpiderInjector`, `beaniesquest_intro_Stopwatch`, `beaniesquest_intro_StorageLocker`, `beaniesquest_intro_TheIOU`, `beaniesquest_intro_TheLoner`, `beaniesquest_intro_Trapfest99`, `beaniesquest_intro_UltraVision3000`, `beat_chapter_boss`, `beat_house_boss`, `bite`, `bloodthirsty`, `bloodthirsty_eyes_closed`, `body`, `boneyard`, `bonk_damage`, `bonus_itemroll_luck`, `bonus_items`, `bonus_passives`, `bored`, `boss`, `boss_background_alt`, `boss_elite_buffs`, `boss_fight_intro`, `boss_fight_round2`, `boss_health_multiplier`, `brain`, `buff_ally`, `buff_enemy`, `buff_self`, `built_in_collision`, `bumblefoot`, `bunker`, `butch_begin_accepting_cats`, `butch_boneyard_intro`, `butch_first_house_boss_beat`, `butch_pyro`, `butch_tina1`, `butch_tips_backstab`, `butch_tips_charisma`, `butch_tips_combat`, `butch_tips_disorders`, `butch_tips_drafting`, `butch_tips_elements`, `butch_tips_hard`, `butch_tips_headhome`, `butch_tips_houseboss`, `butch_tips_info`, `butch_tips_intelligence`, `butch_tips_intro`, `butch_tips_items`, `butch_tips_lesscats`, `butch_tips_magicdamage`, `butch_tips_passives`, `butch_tips_reorient`, `butch_tips_rewards`, `butch_tips_tacticalview`, `butch_tips_turnorder`, `butch_tips_wellrounded`, `butcher_portrait`, `butchercat`, `buy2`, `buy3`, `can_be_rare`, `can_still_use_attack`, `can_still_use_attack_didntspell`, `cancreeper`, `cant_afford`, `cant_afford_a`, `cant_afford_b`, `cant_afford_c`, `cant_afford_d`, `cant_afford_iceage`, `cant_afford_jurassic`, `cant_afford_moon`, `cant_afford_theend`, `cant_equip_to_colorless`, `cap_distance_to_ally`, `cap_distance_to_character`, `cap_distance_to_enemy`, `cap_total_distance_moved`, `catdata`, `category`, `cavecatfamily`, `caves`, `cerberubs`, `cha`, `chain`, `chain_ability`, `chain_chance`, `champ_budget`, `champ_chance_mini`, `chance`, `chapter`, `chapter_common`, `chapter_item_pool`, `chapter_rare`, `chapters`, `choose_cat_with_min_health`, `choose_one`, `class`, `class_anis`, `class_unlock_butcher`, `class_unlock_druid`, `class_unlock_jester`, `class_unlock_medic`, `class_unlock_monk`, `class_unlock_necromancer`, `class_unlock_psychic`, `class_unlock_thief`, `class_unlock_tinkerer`, `classes`, `claws`, `clericcat`, `cloned_ability`, `coins`, `coins_bonus`, `coins_multiplier`, `collected_new_items`, `collected_nothing`, `color`, `combat_background`, `combat_ui_background`, `combo`, `complete_act_difficulty`, `complete_adventure`, `complete_chapter`, `complete_chapter_with_class`, `complete_chapters`, `complete_checklist_with_class`, `complete_checkmarks`, `complete_house_boss`, `complicated_abilities`, `complicated_passives`, `con`, `concentrate`, `consider_aggro_target_enemy`, `consider_aoe`, `consider_overkill`, `consider_secondary_damage`, `consider_spells`, `consider_total_damage`, `consumable`, `consumable_chance`, `consumables`, `consumables_consumable_common`, `consumables_consumable_rare`, `consumables_consumable_uncommon`, `consumables_consumable_very_rare`, `continual_emission`, `copy_results`, `core`, `cost`, `cough`, `count`, `count_nomove_in_eval`, `crater`, `current_chapter_common`, `current_chapter_rare`, `current_chapter_uncommon`, `current_chapter_very_rare`, `cursed`, `damage`, `damage_ally`, `damage_ally_corpse`, `damage_enemy`, `damage_enemy_corpse`, `damage_instance`, `damage_self`, `danger_avoidance`, `dead_facecenter`, `dead_faceleft`, `deathsound`, `debris`, `debuff_ally`, `debuff_enemy`, `debuff_self`, `debug`, `decision_weights`, `default`, `default_frame`, `degrade_after_adventure`, `depth_bias`, `desc_multiclass`, `desert`, `destinations`, `destroy`, `devious`, `devious2`, `dex`, `dimensionx`, `dinocouple`, `distance_to_aggro_target`, `distance_to_ally`, `distance_to_center`, `distance_to_character`, `distance_to_corpse`, `distance_to_enemy`, `distance_to_water`, `distraught`, `divine_shield`, `do_not_end_turn`, `done_spitting_fail_ally`, `done_spitting_fail_miss`, `done_spitting_fail_rat`, `done_spitting_success`, `dont_destroy_on_0`, `dreamworks`, `dreamworks2`, `drmangler`, `druid_portrait`, `druidcat`, `durability`, `early_spawn`, `ears`, `ears_down`, `ears_down_overshoot`, `ears_left`, `ears_right`, `ears_up`, `ears_up_overshoot`, `easy`, `editor`, `element`, `elite_budget`, `elite_buffs`, `elite_chance_mini`, `else`, `emit_amount`, `emit_box`, `emit_direction`, `emit_radius`, `emit_rate`, `emit_shell`, `emit_spread`, `emit_timespread`, `emit_timespread_curve`, `emitshape_scale`, `empty_armor_scaled_stats`, `empty_self_damage`, `end_turn_on_formswitch`, `ending`, `ending_cutscene`, `ending_cutscene2`, `endoftime`, `equip_sound`, `equipment`, `euphoric`, `event`, `event_difficulty`, `event_piece_frame`, `examine`, `exclude_characters_tagged`, `exit0`, `exit1`, `exit_desert`, `exit_lab`, `extra_bound_planes`, `eyes_closed`, `face`, `face_aggro_target`, `face_camera`, `face_center`, `face_closest_enemy`, `face_down_wince`, `face_far_down`, `face_far_down_right`, `face_far_left`, `face_far_left_eyes_closed`, `face_far_right`, `face_far_up`, `face_far_up_left`, `face_far_up_right`, `face_left_wince`, `face_moving_direction`, `facecenter`, `facecenter_back`, `facecenter_eyes_closed`, `facecenter_happy`, `facecenter_happy_overshoot`, `facecenter_hardblink`, `facecenter_right`, `facecenter_shock`, `facecenter_suprise`, `facecenter_worried`, `facedown`, `facedown_back`, `facedown_eyes_closed`, `facedown_eyes_closed_overshoot`, `facedownleft`, `facedownleft_eyes_closed`, `facedownright`, `facedownright_eyes_closed`, `facedownright_focused`, `facedownright_more`, `faceleft`, `faceleft_back`, `faceleft_eyes_closed`, `faceleft_mouth_open`, `faceright`, `faceright_back`, `faceup`, `faceup_back`, `faceup_eyes_closed`, `faceup_shock`, `faceupleft`, `faceupleft_eyes_closed`, `faceupright`, `faceupright_supermad`, `fail_adventure`, `fail_item_quest`, `failable`, `female1`, `female10`, `female11`, `female12`, `female13`, `female14`, `female15`, `female16`, `female17`, `female18`, `female19`, `female2`, `female20`, `female21`, `female22`, `female23`, `female24`, `female25`, `female26`, `female27`, `female28`, `female29`, `female3`, `female30`, `female31`, `female32`, `female33`, `female34`, `female35`, `female36`, `female37`, `female38`, `female39`, `female4`, `female40`, `female41`, `female42`, `female43`, `female44`, `female45`, `female46`, `female47`, `female48`, `female49`, `female5`, `female50`, `female51`, `female52`, `female53`, `female54`, `female55`, `female56`, `female57`, `female58`, `female59`, `female6`, `female60`, `female61`, `female62`, `female63`, `female64`, `female7`, `female8`, `female9`, `fighter_portrait`, `fightercat`, `fights`, `fights_skipped`, `finish_adventure`, `finish_quest`, `first_fight_intro`, `first_house_boss_tomorrow`, `first_house_hint_retired`, `flat_cast_bonus`, `flat_movement`, `flushmaster`, `focused`, `folder`, `food`, `food_bonus`, `food_multiplier`, `force`, `force_end`, `force_start`, `force_sticky`, `forced_placement`, `format`, `format2`, `forward_to_tips`, `fragile`, `frame`, `frame_label`, `frank_caves_intro`, `frank_ending`, `frank_max1`, `frank_max2`, `frank_max3`, `frank_max4`, `frank_max5`, `frank_max_intro`, `frank_max_repeating`, `frank_terminator2`, `frank_tips_1`, `frank_tips_10`, `frank_tips_2`, `frank_tips_3`, `frank_tips_4`, `frank_tips_5`, `frank_tips_6`, `frank_tips_7`, `frank_tips_8`, `frank_tips_9`, `friction`, `friction_end`, `friction_start`, `fully_complete_difficulty`, `future`, `futurebot`, `gambit`, `gender`, `general_common`, `general_rare`, `general_uncommon`, `general_very_rare`, `global_objects`, `global_particles`, `global_passives`, `global_tags`, `gone`, `good`, `grant_ability`, `graphics`, `happy`, `happy_eyes_closed`, `happy_left`, `happy_up_eyes_closed`, `hard`, `hard_initial`, `hardblink`, `head`, `head_start`, `heal_ally`, `heal_enemy`, `heal_self`, `height`, `hide_text`, `hint_destination`, `hint_persistent_elements`, `hint_prerequisite_flag`, `home`, `house_intro`, `house_kitten_box`, `house_pass_day`, `house_pass_day2`, `house_pipe`, `house_retired_cat_box`, `house_starred_box`, `house_strays`, `house_upgrade_4throom`, `house_upgrade_attic`, `house_upgrade_basement`, `house_upgrade_basement2`, `house_upgrade_basement3`, `house_upgrade_basement4`, `house_upgrade_basement5`, `house_upgrade_largehouse`, `house_upgrade_mediumhouse`, `hunter_portrait`, `huntercat`, `iceage`, `iceelemental`, `icon`, `icon_frame`, `icon_hint`, `id`, `ignore`, `image`, `image_tint`, `include`, `increment_savefile_counter`, `indestructible`, `index`, `infestedduo`, `inherit_speed`, `initial_cooldown`, `initial_cutscene_day`, `initial_cutscene_night`, `initial_form`, `initial_health`, `innate_items`, `innate_passives`, `insane`, `int`, `interstitial_bg_frame`, `intro`, `introduce_hard_path`, `is_3D`, `item_chance`, `jack_begin_accepting_cats`, `jack_desert_intro`, `jack_introduction`, `jack_max1`, `jack_max2`, `jack_max3`, `jack_max4`, `jack_max5`, `jack_max_intro`, `jack_max_repeating`, `jack_shopupgrade1`, `jack_shopupgrade2`, `jack_shopupgrade3`, `jack_shopupgrade4`, `jack_zara`, `jester_portrait`, `jestercat`, `junkyard`, `jurassic`, `keyword_tooltips`, `kill_ally`, `kill_enemy`, `kind`, `lab`, `label`, `large`, `lava`, `lck`, `lead_time`, `leftear`, `lefteye`, `lefteyebrow`, `leg1`, `leg2`, `legacy_quest`, `lenny`, `level`, `level_up_didnt_select_sunburn`, `level_up_intro`, `level_up_selected_sunburn`, `levelup_stats`, `lightningelemental`, `live_bounds`, `lock_item_slot`, `locked`, `low_on_food`, `mad`, `mage_portrait`, `magecat`, `main`, `main_pool`, `major_class_checkmarks`, `male1`, `male10`, `male100`, `male101`, `male102`, `male103`, `male105`, `male106`, `male107`, `male108`, `male109`, `male11`, `male110`, `male111`, `male112`, `male113`, `male114`, `male115`, `male116`, `male117`, `male118`, `male119`, `male12`, `male120`, `male122`, `male123`, `male124`, `male125`, `male126`, `male127`, `male128`, `male129`, `male13`, `male130`, `male131`, `male132`, `male133`, `male134`, `male135`, `male136`, `male137`, `male138`, `male139`, `male14`, `male140`, `male141`, `male142`, `male15`, `male16`, `male17`, `male18`, `male19`, `male2`, `male20`, `male21`, `male22`, `male23`, `male24`, `male25`, `male26`, `male27`, `male28`, `male29`, `male3`, `male30`, `male31`, `male32`, `male33`, `male34`, `male35`, `male36`, `male37`, `male38`, `male39`, `male4`, `male40`, `male41`, `male42`, `male43`, `male44`, `male45`, `male46`, `male47`, `male48`, `male49`, `male5`, `male50`, `male51`, `male52`, `male53`, `male54`, `male55`, `male56`, `male57`, `male58`, `male59`, `male6`, `male60`, `male61`, `male62`, `male63`, `male64`, `male65`, `male66`, `male67`, `male68`, `male69`, `male7`, `male70`, `male71`, `male72`, `male73`, `male74`, `male75`, `male76`, `male77`, `male78`, `male79`, `male8`, `male80`, `male81`, `male82`, `male83`, `male84`, `male85`, `male86`, `male87`, `male88`, `male89`, `male9`, `male90`, `male91`, `male92`, `male93`, `male94`, `male95`, `male96`, `male97`, `male98`, `male99`, `mamamaggot`, `mammothbaby`, `map_areas`, `map_click_node`, `map_equip_items`, `map_equip_items2`, `material`, `max_durability`, `max_health`, `max_npc`, `max_particles`, `meatworld`, `medic_portrait`, `medium`, `melee_attack_rat`, `melee_cat_spit`, `melee_cat_spit_fail_ally`, `melee_cat_spit_fail_miss`, `melee_cat_spit_fail_rat`, `melee_cat_spit_ignore`, `melee_cat_spit_success`, `melee_killed_rat`, `melee_move2`, `melee_out_of_actions`, `min_difficulty`, `miniboss`, `miniboss_event`, `minion_alt`, `monk_portrait`, `monkcat`, `mono_cat_run`, `moon`, `mouth`, `mouth_open`, `move_pool`, `move_weights`, `movieclip_timescale`, `music`, `musiclayer`, `mw_altar`, `mw_battle1`, `mw_boss`, `mw_earlyhome`, `mw_event1`, `mw_hard1`, `mw_home`, `mw_quest_event`, `mw_treasure`, `n`, `name_mod`, `name_reference_applier`, `name_stacks_neg`, `necrocat`, `necromancer_portrait`, `negative_weight_scale`, `nemesis`, `new_adventure`, `no_breed`, `normal`, `nouns`, `object`, `on_store`, `one_eye_wink`, `only_at_battle_start`, `open`, `organ_boneyard_intro`, `organ_intro`, `organ_max1`, `organ_max2`, `organ_max3`, `organ_max4`, `organ_max5`, `organ_max_intro`, `organ_max_repeating`, `organ_rename`, `organ_throbbingdomain_intro`, `organ_tina3`, `organ_unlock`, `organ_upgrade1`, `organ_upgrade2`, `organ_upgrade3`, `organ_upgrade4`, `organ_upgrade5`, `organ_upgrade6`, `orientation`, `out_of_stock`, `outline_color`, `override_art`, `override_basic_attack`, `override_move`, `ownership`, `p`, `paint`, `parasaurolophus`, `parasite`, `partial_animation_suffix`, `particle_lifetime`, `passive`, `passive_pool`, `pattern`, `petted`, `petted2`, `pick`, `pieces_required`, `pills`, `pitch`, `pool`, `poopcat`, `popup`, `post_combat_cutscene`, `preempt_npc_sequence`, `preferred_distance`, `prereqs`, `preset`, `prevent_level_up`, `projection_matrix`, `properties`, `psychic_portrait`, `psychiccat`, `purchase_item`, `purchase_item_a`, `purchase_item_b`, `purchase_item_c`, `purchase_item_d`, `purchase_item_iceage`, `purchase_item_jurassic`, `purchase_item_moon`, `purchase_item_theend`, `queenhippo`, `quest_event`, `quest_item`, `quest_item_alias`, `quest_reward_item`, `queue_cutscene_immediate`, `quotes`, `radicalrat`, `random`, `randomize_piece_frames`, `randomness`, `ranged_attack_tomtom`, `ranged_attack_tomtom_fail_ally`, `ranged_attack_tomtom_fail_miss`, `ranged_attack_tomtom_fail_rat`, `ranged_cat_attack`, `ranged_cat_early_attack2_ally`, `ranged_cat_early_attack2_miss`, `ranged_cat_early_attack2_rat`, `ranged_cat_early_attack_ally`, `ranged_cat_early_attack_miss`, `ranged_cat_early_attack_rat`, `ranged_cat_failmove`, `ranged_cat_intro`, `ranged_cat_roll`, `ranged_cat_rolled_first`, `raptor`, `raptorbaby`, `rare_elite_buffs`, `rarity`, `ratking`, `real_wink`, `real_wink_overshoot`, `rematch_cooldown`, `rematch_cutscene_day`, `rematch_cutscene_night`, `removed`, `render_layer`, `render_mode`, `repeat`, `repeatable`, `require_beat_house_boss`, `require_mapgen_flag`, `required_difficulty`, `requirements`, `requires_corpse`, `requires_hard_path`, `requires_monoclass_run`, `requires_unlocked_npc`, `reset_aux_on_store`, `reset_npc_sequence`, `reset_str_aux_on_store`, `reset_unlock`, `restrict`, `return_as`, `return_during`, `reverb`, `reverb_empty`, `reverb_full`, `revive_ally_corpse`, `revive_enemy_corpse`, `right_icon`, `rightear`, `righteye`, `righteyebrow`, `robotom`, `rockybobo`, `roll_limit`, `rollable`, `rotation`, `rotation_speed`, `rotation_speed_end`, `rotation_speed_start`, `rotation_start`, `sabertoothcat`, `sad`, `sad_left`, `same_cat`, `save_file_flag`, `savefile_string`, `scars`, `schadenfreude_scaled_stats`, `scorpioncat`, `scripts`, `set`, `set_mapgen_flag`, `set_savefile_flag`, `sewers`, `shake1`, `shake2`, `shield`, `shock`, `shock_left`, `shop_cheapwater`, `shop_common`, `shop_water`, `simple`, `simulation_space`, `size`, `size_end`, `size_in`, `size_out`, `size_start`, `skip_result_screen`, `slime`, `small`, `smash`, `smile`, `smug`, `smug_left`, `solo_cat_run`, `sound`, `sounds`, `spawn`, `spawn_node`, `spawn_object`, `spawn_object_distance_to_ally`, `spawn_object_distance_to_enemy`, `spawn_object_preferred_distance`, `spawn_side`, `spd`, `special`, `specific_chapter`, `speed`, `speed_end`, `speed_scale`, `speed_start`, `spend_mana_scale`, `spewer`, `spidercat`, `splash_damage`, `spurt`, `stacy`, `starter_abilities`, `stat`, `stat_max`, `stat_min`, `stat_mods`, `states`, `static_1x1_a`, `static_1x1_b`, `static_1x1_c`, `static_2x2_a`, `static_2x2_b`, `static_tall_a`, `static_tall_b`, `stats`, `steven_100`, `steven_introduction`, `steven_milliontrashed`, `steven_postendgame`, `steven_resummon`, `steven_savescum_1`, `steven_savescum_100`, `steven_savescum_1alt1`, `steven_savescum_1alt2`, `steven_savescum_1alt3`, `steven_savescum_2`, `steven_savescum_2alt1`, `steven_savescum_2alt2`, `steven_savescum_2alt3`, `steven_savescum_3`, `steven_savescum_3alt1`, `steven_savescum_3alt2`, `steven_savescum_3alt3`, `steven_savescum_4`, `steven_savescum_4alt1`, `steven_savescum_4alt2`, `steven_savescum_4alt3`, `steven_savescum_houseboss_1`, `steven_savescum_houseboss_100`, `steven_savescum_houseboss_2`, `steven_savescum_houseboss_3`, `steven_savescum_intro`, `steven_savescum_intro_houseboss`, `steven_unlock_act1_crazy`, `steven_unlock_act1_impossible`, `steven_unlock_act2_crazy`, `steven_unlock_act2_hard`, `steven_unlock_act2_impossible`, `steven_unlock_act3_crazy`, `steven_unlock_act3_hard`, `steven_unlock_act3_impossible`, `sticky`, `str`, `str_aux`, `str_aux_initialize`, `str_aux_is_copy_ability`, `str_aux_is_copy_item_active`, `str_aux_is_copy_item_icon`, `str_aux_is_copy_item_passive`, `str_aux_is_copy_passive`, `sub_ability`, `subcategory`, `suffix`, `supermad`, `suprise`, `surviving_kaiju`, `tag`, `tag_location`, `tags`, `tail`, `take_cats_inside`, `tall_grass`, `tank_portrait`, `tankcat`, `tantrum_cry`, `target`, `template`, `temporary_effects`, `terminator`, `terminator_boss`, `terror`, `test_gamepad_prompts`, `text`, `texture`, `thebloat`, `theend`, `thief_portrait`, `thiefcat`, `tile`, `tile_layer`, `time_machine`, `tink_aggression`, `tink_basestats`, `tink_begin_accepting_cats`, `tink_inbreeding`, `tink_max1`, `tink_max10`, `tink_max2`, `tink_max3`, `tink_max4`, `tink_max5`, `tink_max6`, `tink_max7`, `tink_max8`, `tink_max9`, `tink_max_intro`, `tink_max_repeating`, `tink_prettybow`, `tink_relationships`, `tink_sexuality`, `tink_tags`, `tink_terminator`, `tink_tina2`, `tink_tips_appeal`, `tink_tips_basestats`, `tink_tips_cleaning`, `tink_tips_comfort`, `tink_tips_health`, `tink_tips_inbreeding`, `tink_tips_intro`, `tink_tips_multiclassing`, `tink_tips_mutation`, `tink_tips_stimulation`, `tinkerer_portrait`, `tinkerercat`, `tooltip_reference_applier`, `tooltip_stackless`, `tooltip_stackless_neg`, `tooltip_stackless_pos`, `tooltip_stacks`, `tooltip_stacks_neg`, `tooltip_stacks_pos`, `tooltip_stacks_singular`, `total_distance_moved`, `tracy_blankcollar1`, `tracy_blankcollar2`, `tracy_blankcollar3`, `tracy_foodbonus1`, `tracy_foodstorage1`, `tracy_foodstorage10`, `tracy_foodstorage2`, `tracy_foodstorage3`, `tracy_foodstorage4`, `tracy_foodstorage5`, `tracy_foodstorage6`, `tracy_foodstorage7`, `tracy_foodstorage8`, `tracy_foodstorage9`, `tracy_idol1`, `tracy_idol2`, `tracy_idol3`, `tracy_idol4`, `tracy_idol5`, `tracy_idol6`, `tracy_idol7`, `tracy_introduction`, `tracy_kaijufight`, `tracy_max1`, `tracy_max2`, `tracy_max3`, `tracy_max4`, `tracy_max5`, `tracy_max_intro`, `tracy_max_repeating`, `trampy`, `transitions`, `trap`, `treasure`, `trigger_house_boss`, `trigger_npc_sequence`, `trigger_npc_sequence_tomorrow`, `try_again_attack_rat`, `try_again_melee_move`, `tutorial`, `tutorial_cat_dies`, `tutorial_levelup_active_pool`, `tutorial_levelup_active_pool_2`, `tutorial_levelup_passive_pool`, `type`, `uncommon`, `unique`, `unknown`, `unlit`, `unlock_ability`, `unlock_act_difficulty`, `unlock_boss`, `unlock_item`, `unlock_item_immediate`, `unlock_levelgroup`, `unlock_npc_tomorrow`, `unlock_passive`, `unlock_quest_item`, `unlock_song`, `unprompted`, `unprompted1`, `unprompted2`, `unprompted3`, `unprompted4`, `unprompted5`, `unprompted6`, `unprompted_a`, `unprompted_b`, `unprompted_c`, `unprompted_d`, `unprompted_e`, `unprompted_f`, `unprompted_g`, `unprompted_h`, `unprompted_i`, `upgrade_storage_1`, `upgrade_storage_2`, `upgrade_storage_3`, `upgrade_storage_4`, `upgrade_storage_5`, `upgrade_storage_6`, `upgrade_storage_7`, `upgrade_storage_max1`, `upgrade_storage_max2`, `upgrade_storage_max3`, `upgrade_storage_max4`, `upgrade_storage_max5`, `upgrade_storage_repeating_crazy`, `upgrade_storage_repeating_hard`, `upgrade_storage_repeating_impossible`, `upgrade_storage_repeating_intro`, `upgrade_storage_repeating_normal`, `use_attack_after_used_weapon`, `use_weapon`, `utility`, `value`, `variant_of`, `very_rare`, `verymad`, `visit_chapter`, `voice`, `volume_adjustment`, `wallet_size`, `water_alt_shader`, `water_alt_shroud`, `water_alt_tile`, `weather_element_alt`, `weather_event`, `weightless`, `welcome`, `welcome_boneyard`, `welcome_bunker`, `welcome_caves`, `welcome_core`, `welcome_crater`, `welcome_desert`, `welcome_future`, `welcome_iceage`, `welcome_junkyard`, `welcome_jurassic`, `welcome_lab`, `welcome_moon`, `welcome_sewers`, `welcome_theend`, `welcome_water`, `welcome_water_cheap`, `width`, `wince`, `wink`, `wolfcat`, `worried`, `worried_left`, `yeticat`, `zodiac`, `{Damaging Keys}`, `{Event Keys}`, `{Graphics Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

### `Rage` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `move_speed_multiplier`, `passives`

### `RandomPassivePool` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PassiveGroup`

### `RandomStatusFromPool` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (37):** `AllStatsUp`, `Bleed`, `BleedThorns`, `Blind`, `Brace`, `Bruise`, `Burn`, `Charge`, `Charmed`, `Confusion`, `ConstitutionUp`, `DiminishingHealthRegen`, `DivineShield`, `Fear`, `Freeze`, `Immobile`, `KineticSpikes`, `Madness`, `MagicWeakness`, `Marked`, `MoveQuivered`, `ObjectOnHitCharacter`, `Petrify`, `Poison`, `Quivered`, `Reflect`, `Shield`, `Sleep`, `Slow`, `SpawnCoinAnywhere`, `SpeedUp`, `StatusGroup`, `StrengthUp`, `Stun`, `Tarred`, `Thorns`, `Weakness`

### `ReflectProjectiles` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `self_damage`

### `ReplaceBrain` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `pattern`

### `RevengeDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (4):** `damage`, `elements`, `type`, `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `ReviveNextRound` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AllStatsUp`, `DivineShield`, `Shield`

### `Robot` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `alternate_energized_effect`

### `ScaldingOrbMoonBossOneShot` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (2):** `CompleteItemQuest`, `RemoveItem`

### `ScaledStatusAlliesOnSpendMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Adjacent`

### `ScaledStatusOnBleedDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charge`

### `ScaledStatusOnHolyShieldBlock` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `ScaledStatusOnLoseShield` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Thorns`

### `ScaledStatusOnOverMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Cleanse`, `RandomMagicMissile`

### `ScaledStatusOnSpendMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

### `SecurityBotProtect` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `enemies_only`, `not_on_kill`, `tag_restriction`

### `SetAnimationAlts` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (2):** `dead`, `dying`

### `Shadow` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `crit_chance`

### `Sitting` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SmallAttic` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `SmallHolding` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SmallHoldingCat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SmiteEnemiesWhoKill` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `SolarFlare` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `SpawnEachTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `stack_key`

### `SpawnOnBattleStart` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `prevent_chain_tag`

### `SpawnThingOnDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (6):** `auto_cast`, `chance`, `coins`, `melee_ability_only`, `number`, `shield_only`

### `SpawningPhase` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SpecialFriends` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `HealthGain`

### `SquirrelForm` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `tooltip`

### `StacyMutant_Brace` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Brace`, `CatPartsTransform`

### `StacyMutant_Counter` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddStatusToBasicAttack`, `CatPartsTransform`, `CounterAttack`

### `StacyMutant_Damage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddDamage`, `AddMaxHealth`, `CatPartsTransform`

### `StacyMutant_DoubleHead` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CatPartsTransform`, `ExtraDispersedTurns`

### `StacyMutant_Fire` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `CatPartsTransform`, `ElementImmune`, `ReplaceBasicAttack`, `ReplaceBrain`

### `StacyMutant_Health` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddMaxHealth`, `AddSpeed`, `CatPartsTransform`, `SizeScale`

### `StacyMutant_Holy` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CatPartsTransform`, `DivineShield`

### `StacyMutant_Ice` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddMovement`, `CatPartsTransform`, `ElementImmune`, `ReplaceBasicAttack`, `ReplaceBrain`

### `StacyMutant_Lightning` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `CatPartsTransform`, `ElementImmune`, `ReplaceBasicAttack`, `ReplaceBrain`

### `StacyMutant_Mirror` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `CatPartsTransform`, `ReflectProjectiles`, `StatusEachTurnEndForEachTurn`

### `StacyMutant_Speed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddDamage`, `AddSpeed`, `CatPartsTransform`, `SizeScale`

### `StacyMutant_Thorns` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CatPartsTransform`, `Thorns`

### `Standing` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Standing2` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Start_Ceiling` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `StatDependentPassive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AddDamageToBasicAttack`

### `StatsAtLowHealth` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `StatusAdjacentOnTheirTurnBegin` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `ForceMoveAway`

### `StatusAdjacentOnTheirTurnEnd` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `ForceMoveAway`

### `StatusAfterCastSpell` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `TempDamageUp`, `TempSpellDamageUp`

### `StatusAfterXStacks` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `ExtraBasicMoves_Status`, `RefreshActPoints`, `threshold`

### `StatusAfterXTurns` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `StatusAllCharactersOnSpawn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_Boss`, `Conditional_PartyMember`, `Conditional_Tiny`, `Else`, `Poison`

### `StatusAlliesEachTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomStatUp`

### `StatusAlliesOnBattleStart` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `EquipTemporaryItem`

### `StatusAlliesOnDeath` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Freeze`, `FullHeal`, `HealAndOverhealToShield`, `Reanimate`, `TakeExtraTurn`

### `StatusAlliesOnGainCoins` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `HealthGain`, `LuckUp`

### `StatusAlliesOnKill` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AllStatsUp`, `DamageUp`, `HealthGain`

### `StatusAlliesOnSpendMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ManaGain`

### `StatusAlliesScaledByCursedOnDeath` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LuckUp`

### `StatusAllyWhenAllySpendsMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `threshold`

### `StatusAnyCatAllyWhoKills` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AlphaCat`

### `StatusCharactersOnRoundEnd` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Conditional_GoodRoll`, `FloatingRockTrap`, `Thorns`, `tag_filter`

### `StatusCharactersOnRoundStart` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_GoodRoll`, `Else`, `Madness`

### `StatusCollector` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Poison`, `Slow`, `StrengthUp`

### `StatusDamagers` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Fear`, `LuckUp`

### `StatusEachRoundBegin` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `NonStackingShield`

### `StatusEachRoundEnd` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddRandomEliteBuff`, `DoDamage`, `UseAbility`

### `StatusEachTurnBegin` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Conditional_BadRoll`, `Conditional_GoodRoll`, `Fear`, `FillMana`, `ForceUseAbility`, `IntelligenceUp`, `RandomStatUp`

### `StatusEachTurnBeginIfHasStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `DamageUp`, `HealthGain`, `animation`

### `StatusEachTurnEnd` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `EmptyMana`, `ForceUseAbility`, `IntelligenceUp`, `KineticSpikes`, `NonStackingDivineShield`, `ObjectOnHitCharacter`, `PermanentMadness`, `RangeUp`, `SpeedUp`, `StrengthUp`, `UseAbility_Madness`

### `StatusEachTurnEndForEachTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `StatusEachTurnEndIfEnabledAtStartOfTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `StatusEachTurnEndPerEnemyKill` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ObjectOnHitCharacter`

### `StatusEnemiesOnDeath` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Freeze`

### `StatusEveryXSpellCasts` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `ReduceManaCost`, `RepairWeapon`, `RepairWeaponCondition`, `SpellDamageUp`

### `StatusEveryXSpellCastsEachTurn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `StatusEveryXTurnBegins` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DivineShield`

### `StatusGroup` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `DexterityUp`, `LuckUp`, `SpawnCoinAnywhere`, `SpeedUp`

### `StatusIfBattleAlreadyBegan` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PermanentMadness`

### `StatusIfDidntMove` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charge`

### `StatusIfUnusedActPoints` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `BackflipWhenTargeted`, `Craft`

### `StatusIfUnusedMovePoints` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `Brace`, `ConstitutionUp`, `HealthGain`, `ManaGain`, `MoveQuivered`, `Shield`

### `StatusKilledCharacters` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AutoReanimate`, `Conditional_Ally`

### `StatusKillers` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Conditional_Boss`, `Conditional_NotBoss`

### `StatusOnAllyCatDeath` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `FillMana`, `HealthGain`, `PercentHeal`, `TakeExtraTurn`

### `StatusOnAnyDeath` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LuckUp`

### `StatusOnBackstab` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `StatusOnBattleEnd` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `CureDisease`, `FindItemFromPool`, `NextBattleStatus`, `PermanentConstitution`, `PermanentIntelligence`, `PermanentSpeed`, `PermanentStrength`, `RandomMutation`, `RandomPermanentStat`

### `StatusOnBattleStart` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `FullHeal`, `Sleep`

### `StatusOnBreak` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (15):** `ApplyToRandomPartyMemberIfPossible`, `Bruise`, `ChangeTilesUnder`, `ConstitutionUp`, `DexterityUp`, `FindItem`, `FindItemFromPool`, `GainCoinsRange`, `GainDisorder`, `HealthGain`, `HealthRegenUp`, `IntelligenceUp`, `ObjectOnHitCharacter`, `PermanentConstitution`, `StrengthUp`

### `StatusOnBreakItem` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Shield`, `Thorns`

### `StatusOnCastSpell` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Charge`, `CurrentWeaponDamageUp`, `HealthGain`

### `StatusOnCollectPickup` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Tech`

### `StatusOnCrit` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `CritChanceUp`, `DamageUp`, `LuckUp`, `RandomStatUp`, `Shield`

### `StatusOnDealtDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `TempDexterityUp`, `TempLuckUp`, `TempStrengthUp`

### `StatusOnDealtDamageThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `RefreshMovePoints`, `Shield`, `threshold`

### `StatusOnDie` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (10):** `Conditional_RandomChance`, `CreateGlobalModifiers`, `FindItemFromPool`, `GainCoinsRange`, `RandomMagicMissile`, `RandomStatusFromPool`, `RemoveAmbientLightEffects`, `RemoveGlobalModifiers`, `ScatterCoins`, `StackingSandstorm`

### `StatusOnDodge` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DodgeChance_Status`

### `StatusOnEatFood` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Cleanse`, `IntelligenceUp`, `RandomStatUp`, `StrengthUp`

### `StatusOnEatPill` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AllStatsUp`

### `StatusOnEndMove` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceAttack`

### `StatusOnEnemyCastSpell` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `HealthGain`

### `StatusOnEnemyConfused` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ImmediateUseAbility`

### `StatusOnEnemyDeath` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charge`

### `StatusOnFallAsleep` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AllStatsUp`, `FillMana`, `HealRandomInjury`

### `StatusOnFullMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `Conditional_OncePerBattle`

### `StatusOnGainCoins` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DivineShield`, `RandomStatusFromPool`

### `StatusOnGainShield` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Temporary`

### `StatusOnHeal` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `RandomStatUp`, `SpeedUp`

### `StatusOnHealed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `ObjectOnHitCharacter`, `RandomStatusFromPool`, `Thorns`

### `StatusOnKill` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `Conditional_FirstApplicationThisTurn`, `DamageUp`, `EquipPermanentItem`, `HealthGain`, `LuckUp`, `RandomStatUp`, `RefreshActPoints`, `RefreshMovePoints`, `SpeedUp`, `Stealth`, `StrengthUp`, `TakeBonusTurnWithStatus`

### `StatusOnKillEnemy` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `DivineShield`, `HealthGain`, `ManaGain`, `RefreshMovePoints`

### `StatusOnLoseShield` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Thorns`

### `StatusOnOverHealed` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `CurrentWeaponDamageUp`, `ForceUseAbility_NonStack`, `StrengthUp`

### `StatusOnOverMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DivineShield`, `IntelligenceUp`, `SpellDamageUp`

### `StatusOnPickupCoins` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DexterityUp`, `RefreshMovePoints`, `SpeedUp`

### `StatusOnPopCorpse` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `StatusOnSetPieceBreak` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (8):** `FindItemFromPool`, `PermanentCharisma`, `PermanentConstitution`, `PermanentDexterity`, `PermanentIntelligence`, `PermanentLuck`, `PermanentSpeed`, `PermanentStrength`

### `StatusOnSpawnIn` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `CaptureFamiliar`, `SetHealth`

### `StatusOnStanceSwitch` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `ForceUseAbility`, `NextBasicAttackCritsThisTurn`, `PartialCleanse`, `RandomMagicMissile`, `RandomStatUp`, `Shield`

### `StatusOnTakeHealthDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PermanentConstitution`

### `StatusOnTakeHealthOrShieldDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_GoodRoll`, `DivineShield`, `Metronome`

### `StatusOnTookDamage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (18):** `Conditional_HasStatus`, `ConstitutionUp`, `Craft`, `DamageUp`, `DiminishingHealthRegen`, `Else`, `IntelligenceUp`, `MovementUp`, `RandomInjury`, `RandomStatUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `StrengthUp`, `TempDamageUp`, `TempMovement`, `Temporary`, `Thorns`

### `StatusOnTookDamageFromAbility` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DiminishingHealthRegen`, `Shield`

### `StatusOnTookDamageFromEnemyAbility` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `MoveQuivered`, `Quivered`

### `StatusOnTriggerTrap` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DexterityUp`, `Quivered`

### `StatusOnTurnEndIfCastNSpells` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DoubleCastSpell`, `MoveQuivered`, `Quivered`

### `StatusOnTurnEndIfDidntCastAbilityTypes` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ManaGain`

### `StatusOnTurnEndIfManaExact` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `FreeSpell`, `MoveQuivered`, `Quivered`, `SpellDamageUp`

### `StatusOnTurnEndIfManaOrHealthExact` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `DivineShield`, `HealthGain`, `IntelligenceUp`, `KineticSpikes`, `Shield`, `SpellDamageUp`, `Temporary`

### `StatusOnUseAbilityWithTag` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_FirstApplicationThisTurn`, `DamageUp`, `HealthGain`, `RandomStatUp`, `RefreshActPoints`

### `StatusOnUseBasicAttack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `FlippedFacingForceAttack`

### `StatusOnUseElementAbility` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `SpeedUp`

### `StatusOverlappingCharactersAndDie` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Poison`

### `StatusPerInjury` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Shield`, `StrengthUp`, `injury`

### `StatusRandomEnemiesOnBattleStart` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Bleed`, `Charmed`, `Confusion`, `Fear`, `Freeze`

### `StatusWhenAllySpendsMana` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ManaGain`, `OneUseSpellDamageUp`

### `StatusWhenStatusCompletelyRemoved` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseAbility`

### `Stop` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SwordAndShield` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `SwordAndShield_Primed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TVBotScreen` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `Die`

### `TaggedPickupEffectReplacement` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `TakeBonusTurnWithStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Madness`

### `Tar` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TarFull` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TempPassiveUntilSettled` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `LimitHeal`, `MeleeRevengeDamage`

### `TempPassiveWhileHasStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddManaRegen`, `HealthRegenUp`, `MeleeRevengeDamage`, `ReplaceSpell`

### `Temporary` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `data`, `expires_on_appliers_turn`, `expires_on_move`

### `TheHunger` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Madness`

### `ThrobBubs` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ThrobHost` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `ThrobNettle` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TimeDelayStatusApplication` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `{Graphics Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `Cleanse`, `CreateGlobalModifiers`, `DoScreenShake`, `FormChange`, `FullHeal`, `GlobalSpawnCharacter`, `PlayBackground`, `RemoveAmbientLightEffects`, `SwitchMusic`, `Vaporize`, `delay`

### `TransformInXTurns` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `TransformOnStatusThreshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `Transformed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TunnelVision` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `crit_chance`

### `Turtled` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TwoAlive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `TwoEyes` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Unlit` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Up` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `tooltip`

### `VisualCountDownThenApplyStatus` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceUseAbility`

### `Washed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `Washer` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `Water` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `partial_animation_suffix`, `{Status and Passive Keys}`

### `WereMan` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `XIsTargetHealth` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `BonusDamage`

### `Zealot` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `ZealotBomb` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `name`, `passives`, `tooltip`

### `a` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `activate_p` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `activate_z` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `active` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `additional_passives` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (15):** `AllStatsUp`, `ApplyPassivesToSpawnerWhileAlive`, `CaptureFamiliar`, `DamageUp`, `FadeInsteadOfDie`, `FillMana`, `HealthGain`, `HideEquipment`, `IllusionTint`, `InjuryImmunity`, `PermanentMadness`, `ReviveNextRound`, `SafeDoomed`, `SchizoIllusionAIModifier`, `SpeedUp`

### `additional_statuses` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PermanentMadness`

### `ally_rewards` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Conditional_GoodRoll`, `FindItemFromPool`, `RandomStatusFromPool`

### `alternate_energized_effect` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `FormChange`, `SpellDamageUp`

### `arm` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `attach_amplifier` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `attach_antenna` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `attach_leech` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `attack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `bad`, `rare`

### `b` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `bad` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (22):** `battle`, `conditional_reward`, `cutscene`, `event_now`, `event_now_same_cat`, `gain_disorder_from_pool`, `gain_immortal_familiar`, `get_parasite`, `get_parasite_from_pool`, `injury`, `kill`, `lose_item`, `next_event_bonus`, `party_random_mutation_from_set`, `permanent_stats`, `play_animation`, `prompt`, `reward`, `select_item_from_pool_for_cutscene_only`, `self_status_next_fight`, `set_frame`, `set_legacy_token`

### `bash` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `bash_past_alt` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `beanies_infinite_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `beanies_quests_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `generate_beanies_quest`, `reward_text`

### `beanies_quests_repeat` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `generate_beanies_quest`, `level_display`, `repeat`, `reward_text`

### `beanies_rift_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `bite` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `bite_it_off` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `blue` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `blue_needle` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `body` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `bonk_damage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `bonus_passives` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (75):** `AbilityDisableIfLivingCrow`, `AbilityEnableIfConsumedCharacterHasTag`, `AbilityEnabledAtHealthThreshold`, `AbilityEnabledIfBasicAttackUsedThisTurn`, `AbilityEnabledIfHasStatus`, `AbilityEnabledIfMovementTrapped`, `AbilityEnabledIfNoAggroTarget`, `AbilityEnabledIfNotHasStatus`, `AbilityEnabledIfSpecificItemEquipped`, `AbilityEnabledOncePerFightAtHealthThreshold`, `AbilityEnabledOncePerRound`, `AbilityEnabledPercentEachTurn`, `AbilityInheritsWeaponEffects`, `AbsorbManaFromOtherSpells`, `AddElementsToSpells`, `AddStatusToBasicAttack`, `AlphaDodgeChance`, `AlphaStatusOnTurnBegin`, `AutocastEachRound`, `BonusAbility_DelayedApplication`, `CapTechSpent`, `CatchBoomerang`, `CaveWomanBirthControl`, `ChargeSpiritBombAura`, `CopyBasicAttackEffects`, `CopyCatPassive_Initializer`, `CritChanceUp`, `DeadAltAbility`, `DownRankAIIfWeaponUsable`, `FistOfFateUniqueEnemyTracker`, `FreeFirstCast`, `FreeFirstCastAndAfterSpendMana`, `FreeFirstCastEachMatch`, `HealthRegenUp`, `IgnoreTiles`, `IntelligenceUp`, `InterchangeDisabler`, `KnockbackImmunity`, `ModifyAbility`, `MoonHeadFinisherEnabler`, `NukeQuestFinalBossModifications`, `PassiveWhileNotTakingTurn`, `ReloadOnAllyCatDies`, `ReloadOnAllyDies`, `ReloadOnAnyDamage`, `ReloadOnBackstab`, `ReloadOnElementalDamageReceived`, `ReloadOnGainCoins`, `ReloadOnGainDivineShield`, `ReloadOnKill`, `ReloadOnKillEnemy`, `ReloadOnKillTagged`, `ReloadOnSpendMana`, `ReloadOnTotalDamageReceived`, `ReloadOnUseAbilityWithManaCost`, `RevengeDamage`, `StatusKillers`, `TossTargetIsAggroTarget`, `TossTargetIsBuddy`, `TossTargetIsNotInWater`, `Trample`, `XIsConsumedCharacterMaxHP`, `XIsCountDeaths`, `XIsCountStatusStacks`, `XIsFormulaLockedUntilComplete`, `XIsFreeArmorSlots`, `XIsIncreaseEachTurn`, `XIsLivingAlliesWithTag`, `XIsLivingCharactersWithTag`, `XIsMultipliedPercentHealth`, `XIsOtherHealsThisTurn`, `XIsRampAndReset`, `XIsRecycleCostReduction`, `XIsSpellStormRampAndReset`, `XIsTimesDamageTaken`

### `boogers` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `book` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `boss_fight_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `brace` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `break_ice` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `break_lock` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `bribe` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `button` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `buy1` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `animation`, `prompt`, `self_status_next_fight`, `weight`

### `c` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `catch` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `challenge_to_game` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `charm` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `charm_past_alt` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `climb` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `comfort` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `common` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (55):** `add_weather`, `ally_ambush_next_fights`, `ambush_next_basic_fights`, `clear_adventure_token`, `clear_result_animation`, `conditional_reward`, `decrement_legacy_counter`, `event_now`, `event_now_same_cat`, `full_heal`, `gain_coins`, `gain_disorder`, `gain_disorder_from_pool`, `gain_familiar`, `gain_food`, `get_and_equip_item`, `get_item`, `get_item_from_pool`, `get_parasite`, `get_parasite_from_pool`, `global_effect_next_fight`, `heal`, `heal_disorder`, `heal_injury`, `increment_legacy_counter`, `injury`, `kill`, `learn_ability_from_pool`, `lose_item`, `lose_specific_item`, `mutation`, `next_event_bonus`, `next_event_from_set`, `override_end_option_prompt`, `party_damage`, `party_heal`, `party_heal_disorder`, `party_permanent_stats_exclude_self`, `party_status_next_fight`, `permanent_stats`, `play_animation`, `prompt`, `random_mutation`, `random_mutation_from_set`, `random_pool`, `self_damage`, `self_heal`, `self_status_next_fight`, `set_adventure_token`, `set_frame`, `set_legacy_token`, `shop_now`, `spawn_unit_next_fight`, `spin`, `upgrade_ability`

### `communicate` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `concheck` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `conditional_reward` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `prompt`, `reward`

### `counter` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `crack_open` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `cross` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `cut_wires` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `cutscene` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `cutscene`

### `d` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `damage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `damage_1` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `damage_full` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `damage_half` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `damage_instance` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `{Damaging Keys}`, `{Event Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (32):** `HealthRegenUp`, `accuracy`, `blocked_damage`, `blocked_multiplier`, `can_collect_pickups`, `can_instapop`, `can_revive`, `cant_miss`, `crit_chance`, `custom_additional_ai_weight`, `damage_shield_only`, `disallow_modifications`, `effects`, `final_hit_bonus_damage`, `force_adjacent_and_diagonal_contact`, `force_no_contact`, `force_no_knockback`, `force_play_hit_animation`, `heal`, `hint_dont_lowgravboost`, `hit_animation_alt`, `incidentally_collects_pickups`, `layer`, `makes_contact`, `non_lethal`, `override_trample_damage`, `piercing`, `ranged`, `raw_damage`, `raw_heal`, `show_damage_on_0`, `two_way_contact`

### `default` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `destroy` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `dexcheck` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `dig` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `disarm` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `dive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `donate` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `donate_10` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `donate_15` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `donate_20` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `donate_5` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `double` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `drink` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `eat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `eat_damage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (4):** `cant_miss`, `effects`, `makes_contact`, `piercing`

### `eat_meat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `effects` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `{Global Modifier Keys}`, `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `else` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (15):** `conditional_reward`, `event_now`, `event_now_same_cat`, `gain_disorder`, `get_item_from_pool`, `increment_legacy_counter`, `next_event_bonus`, `party_damage`, `prompt`, `random_mutation`, `random_pool`, `self_status_next_fight`, `set_adventure_token`, `set_frame`, `set_legacy_token`

### `empty_self_damage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `enter` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `enter_crater` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `examine` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (3):** `animation`, `bad`, `gain_coins`

### `extra_statuses` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Burn`, `Conditional_HasTag`, `HealthGain`, `Poison`, `Tarred`

### `fight` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `fill_jar` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `find_another_way` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `fire` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `good`, `label`, `stat`, `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (1):** `effects`

### `first_fight_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `follow` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `frank_max_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (4):** `favor`, `gift_item_from_pool`, `level_display`, `reward_text`

### `frank_max_repeating` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `gift_item_from_pool`, `level_display`, `repeat`, `reward_text`

### `free` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `future` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `get_item_from_pool` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `prompt`

### `give_parasite` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `global_effect_next_fight` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `CharacterTypeGainsStatusAtBattleStart`, `Fights`, `StatusRandomEnemiesOnBattleStart`

### `global_passives` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Global Modifier Keys}`

**In Master but NOT in split file (1):** `NoCorpses`

### `go_around` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `good` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (58):** `add_weather`, `ally_ambush_next_fights`, `begin_chapter`, `clear_surviving_kaiju`, `clone_self_to_party`, `complete_item_quest`, `conditional_reward`, `copy_items_to_party`, `copy_party_items`, `cutscene`, `cutscene_on_exit`, `event_now`, `event_now_same_cat`, `full_heal`, `gain_clone_familiar`, `gain_disorder`, `gain_disorder_from_pool`, `gain_food`, `get_full_item_set_from_pool`, `get_item`, `get_item_from_pool`, `get_parasite`, `global_effect_next_fight`, `heal`, `heal_disorder`, `heal_injury`, `increment_legacy_counter`, `injury`, `kill`, `learn_ability_from_pool`, `learn_passive_from_pool`, `level_up`, `lose_item`, `lose_specific_item`, `mutation`, `next_event_bonus`, `next_event_from_set`, `override_end_option_prompt`, `party_gain_disorder_from_pool`, `play_animation`, `prompt`, `random_mutation`, `random_pool`, `random_pool_consider_luck`, `rare`, `reward`, `scramble_abilities`, `scramble_passives`, `set_adventure_token`, `set_frame`, `set_legacy_token`, `shop_now`, `transform_item`, `trigger_adventure_unlock`, `trigger_butterfly_effect`, `unlock_item_quest`, `upgrade_ability`, `upgrade_passive`

### `graphics` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (149):** `affected_animation`, `affected_particle`, `air_animation`, `ally_animation`, `alt_animations`, `always_huge_mask`, `always_play_animations`, `animate_name`, `animation`, `animation_in`, `animation_out`, `aoe_spell_on_land`, `apex_distance`, `apex_time`, `area_particle`, `art_flip`, `beam_cap`, `beam_clip`, `bounce_on_hit`, `bypass_combatspeed`, `center_particle`, `chain_distance`, `chain_movieclip`, `custom_cat_data`, `custom_priming_animation`, `damage_threshold_altanimations`, `darken_screen`, `darken_screen_exclude_characters_on_tile`, `darken_screen_exclude_self`, `darken_screen_start_early`, `dash_animation`, `dash_attack_animation`, `dash_bonk_animation`, `dash_decelerating_animation`, `dash_end_animation`, `dash_start_animation`, `decelerate`, `default_attack_animation`, `default_face`, `delay`, `delay_from_map_center`, `delay_from_map_edge`, `delay_from_reverse_map_edge`, `depth_offset`, `desc`, `detatched_animation`, `detatched_animation_cutoff`, `detatched_animation_reach`, `do_animation_offscreen`, `do_damage_immediately`, `do_not_clear_placeholder`, `dont_orient`, `dont_sink`, `dont_visualize_ai`, `easing`, `empty_animation`, `end`, `face_targets`, `face_toss_target`, `fall_from_sky`, `fall_randomize_timing`, `first_castpoint_is_self_damage_only`, `fixed_jump_height`, `fixed_jump_speed`, `four_way_animations`, `full_jump_animation`, `full_jump_sync_frames`, `full_jump_windup_frames`, `fx_is_placeholder_animation`, `fx_random_flip`, `grab_animation`, `hang_time`, `hud_palette`, `ignore_slowtiles`, `jump_attack_animation`, `jump_height_multiplier`, `jump_speed_multiplier`, `jump_start_animation`, `land_animation`, `lob`, `lob_height`, `lob_speed`, `lob_yoff`, `lock_orientation_during_dash`, `loop`, `mask_center`, `mask_extent`, `max_throw_height`, `max_tiles_single_loop`, `min_range`, `min_throw_height`, `miss_particle`, `miss_random_delay`, `move_end_animation`, `move_speed_multiplier`, `move_speed_sync_frames`, `move_start_animation`, `movieclip`, `name`, `no_horizontal_flip`, `no_splatter`, `non_blocking_animations`, `othercat_placeholder_available`, `override_portrait`, `palette`, `particle`, `particle_mat`, `piece_alt_frame`, `portrait_face`, `precast_delay`, `preturn_animation`, `prime_animation`, `primed_alt_animation`, `projectile`, `projectile_spawn_offset`, `pseudoprojectile`, `random_delay`, `randomize_starting_frame`, `reverse_orientation`, `rocket_swirl`, `scale`, `self_damage_mid_port`, `shade_occluded_objects`, `shadow`, `shadow_size`, `show_infinity_damage_warning`, `single_projectile`, `spawn_offset`, `spawnin_animation`, `start`, `status_display_count_max`, `sync_frames`, `sync_speed`, `throw_speed`, `tint`, `tooltip`, `uifloaters_offset`, `uncatchable`, `use_directional_animations`, `use_hit_alts`, `use_origin_offsets`, `use_placeholder`, `use_projectile`, `use_projectile_spawn_offset`, `use_rotation`, `use_rotation_once`, `use_super_armor`, `visual_delay_but_simultaneous_damage`, `water_mask`

### `hack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `holy` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `home` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `hot` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `name`, `passives`

### `house_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `house_strays` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `house_upgrade_4throom` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

### `house_upgrade_attic` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

### `house_upgrade_largehouse` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

### `house_upgrade_mediumhouse` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

### `hp` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `ice` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `good`, `label`, `stat`, `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (1):** `effects`

### `ignore` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `infinite` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `innate_passives` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddStartingMana`, `SpawnOnBattleStart`, `TinkererBasicAttackSwitching`

### `inspect` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `intcheck` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `intimidation` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (15):** `cat_choice`, `choose_cat_with_highest_stat`, `choose_cat_with_item`, `choose_cat_with_item_slot_equipped`, `choose_cat_with_min_health`, `choose_cat_with_most_injuries`, `choose_cat_with_parasite`, `different_from_last_x_cats`, `event_clip`, `subject_clip`, `subject_frame`, `subject_frame_inner`, `title`, `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `investigate` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `itchies` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `item_rarity_costs` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `common`, `rare`

### `jack_max_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (4):** `favor`, `level_display`, `rep_reward_count`, `reward_text`

### `jack_max_repeating` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `reward_text`

### `jack_shopupgrade1` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `jack_shopupgrade2` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `jack_shopupgrade3` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `jack_shopupgrade4` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `join` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `jump` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `jump_over` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `keep_going` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `keyword_tooltips` (from `Miscellaneous.md`)

**In split file but NOT in Master (6):** `TVBotDie`, `TVBotDumb`, `TVBotObey`, `TVBotStop`, `TemporaryItem`, `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Weakness`

### `kiss` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `kiss_meat` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `knife` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `leave` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `leave_it_in` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `leg` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `level_up_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `lever` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `lick` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `lick_alt` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `lightning` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `good`, `label`, `stat`, `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (1):** `effects`

### `listen` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `loot` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (3):** `animation`, `bad`, `rare`

### `loot_heart` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `main` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (22):** `add_weather`, `bad`, `gain_familiar`, `goto`, `leave`, `max_options`, `next_event_from_set`, `options`, `outcome`, `party_heal`, `party_permanent_stats`, `play_animation`, `prompt`, `rare`, `requires_flag`, `self_damage`, `self_status_next_fight`, `set_frame`, `setup`, `shop_now`, `shuffle_options`, `weight`

### `makeup` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `meta` (from `Miscellaneous.md`)

**In split file but NOT in Master (15):** `ability_icon`, `class`, `description`, `icon_damage_display`, `icon_damage_display_eq`, `icon_damage_display_suffix`, `icon_damage_type`, `icon_shell_frame`, `is_basic_attack`, `is_move`, `is_trinket`, `is_weapon`, `tooltip_values`, `type_icon`, `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `mind` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `move_closer` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `nothanks` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `on_throw` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `HitExplosion`

### `open` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `options` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (11):** `animation`, `bad`, `gain_familiar`, `get_item_from_pool`, `leave`, `play_animation`, `prompt`, `rare`, `scale`, `set_frame`, `weight`

### `organ_max_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (4):** `favor`, `gift_item`, `level_display`, `reward_text`

### `organ_max_repeating` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `gift_item`, `level_display`, `repeat`, `reward_text`

### `organ_unlock` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `organ_upgrade1` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `organ_upgrade2` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `organ_upgrade3` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `organ_upgrade4` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `organ_upgrade5` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `organ_upgrade6` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

### `outcome` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (3):** `add_weather`, `play_animation`, `random_pool`

### `party_status_next_fight` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `AbilityOnBattleStart_Immediate`, `Bleed`, `DivineShield`, `Fear`, `HealthRegenUp`, `Immobile`, `NoHealthRegen`, `Poison`, `Tangled`, `Tarred`, `Webbed`

### `passive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Metal`

### `passives` (from `Miscellaneous.md`)

**In split file but NOT in Master (7):** `ai`, `animation_suffix`, `attack`, `partial_animation_suffix`, `passive0`, `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (424):** `AbilityOnBattleStart`, `AbilityReaction`, `AbilityWhenTaggedCharacterMovesNear`, `AbsorbManaAura`, `AddAllyNeighborsToAttackRange`, `AddBonusMeleeRange`, `AddBonusRange`, `AddCorpseHealth`, `AddCritMultiplier`, `AddDamageToBasicAttack`, `AddDamageToElementDamage`, `AddElementsToBasicAttack`, `AddHiddenTag`, `AddInitiative`, `AddKnockbackDamage`, `AddLevelUpRerolls`, `AddLevelUpStatMultiplier`, `AddManaRegen`, `AddMovement`, `AddPassiveToSpawnedRocks`, `AddPassivesToCharmed`, `AddPassivesToMinions`, `AddPassivesToSummonAbilityMinions`, `AddSelfStatusToBasicAttack`, `AddSelfStatusToWeapons`, `AddSpellDamage`, `AddStartingMana`, `AddStatusToAllDamage`, `AddStatusToBasicAttack`, `AddStatusToBasicAttackWithCooldown`, `AddStatusToBasicMeleeAttack`, `AddStatusToElementAbilities`, `AddStatusToElementDamage`, `AddStatusToExplosions`, `AddStatusToFirstBasicAttack`, `AddStatusToMeleeDamage`, `AddStatusToReceivedDamage_ExcludeStatuses`, `AddStatusToTrampleDamage`, `AddStatusToWeapons`, `AddStatusesIfPersistentWeatherElement`, `AddStatusesToReceivedElementalDamage`, `AddTag`, `AddTemporaryEffectsToBasicAttack`, `AddUnfilledMaxHealth`, `AddWeaponScaling`, `AfterImage`, `AllStatsUp`, `AllowPassTurn`, `AllyBonusAbilityAura`, `AllyDamageReaction`, `AllyDamageReduction`, `AllyHealthRegenAura`, `AllyManaRegenAura`, `AllyMoveAbilityAura`, `AllyMultiplyKnockbackDamage`, `AlphaTurns`, `AlternateCraftingPools`, `AmplifyKnockback`, `AmplifyPositiveStatus`, `AmplifyStatus`, `ApplyStatusesToRandomEnemiesEachTurn`, `Autism`, `AutoCritLowDamage`, `AutoEquipConsumables`, `AutocastEachRound`, `AutocastEachTurn`, `AutocastEachTurnBegin`, `BackstabCritChance`, `BackstabWeakness`, `BasicAttackAOEBonus`, `BasicAttackCritChance`, `BasicAttackDamageMultiplier`, `BasicAttackStatusCarefulness`, `BlacklistPickupType`, `BlastResistance`, `Bleed`, `BleedThorns`, `BonusAbility`, `BonusFoodEachBattle`, `BoobyTrapItems`, `BoostAllyStatsOnDeath`, `BoostDamageAura`, `BoostHeals`, `BoostRangeAura`, `BoostWeaponDamage`, `BouncyProjectiles`, `Brace`, `BraceForEachNeighboringEnemy`, `Bruise`, `BuffImmunity`, `Burn`, `CCImmunity`, `CanRemoveCursedItems`, `CantDodge`, `CapDamageFromAllies`, `CapMovementAbilityRange`, `CatAPultAnimation`, `CatchProjectiles`, `ChainKnockback`, `ChanceToBackflip`, `ChanceToBlockAndCounter`, `ChanceToRevive`, `ChangeTauntPriority`, `CharmAllFlies`, `ClassManaCostReduction`, `CobraReflex`, `CoinsAddDamage`, `CollectPickupsOnBattleEnd`, `Conductor`, `ConfusionEffectOnTaggedAbilities`, `ConjureCastSpellsForAllies`, `ConsumableEffectsMultiplierBonus`, `ConsumablesInfiniteRange`, `ConsumablesMeleeRange`, `CounterAttack`, `CritChanceUp`, `CritsApplyStatus`, `DamageEnemiesOnHeal`, `DamageEnemiesOnKill`, `DamageIfDidntUseSpecificAbility`, `DamageNeighborTilesWhenCastSpell`, `DamageNeighborsAfterMove`, `DamageNeighborsOnEndMove`, `DamageReductionAura`, `DamageUp`, `DeathChill`, `DeathRattle`, `DebuffImmunity`, `DejaVu`, `DepressionAura`, `Diabetes`, `DirtyClaws`, `DisableAbilities`, `DisableAbilitiesWithTag`, `DodgeChance`, `Doomed`, `DoubleCastWeapons`, `DukeOfFlies`, `Dyslexia`, `EMP`, `ElementImmune`, `ElementalAttunement`, `ElementalManaCostReduction`, `Empath`, `EnemiesGetPickupsKnockedOut`, `EnergyStorm`, `EquipTemporaryItem`, `EquipmentPassiveMultiplierBonus`, `EquipmentSetBonusBonus`, `EscapeSequence`, `Eternal`, `ExhaustionRoundChange`, `ExplodeOverkilledEnemies`, `ExtraBasicAttacks`, `ExtraBasicMoves_Status`, `ExtraInjuryOnDeath`, `ExtraMovePoints`, `ExtraStatusWhenDealingDamage`, `ExtraWeaponAttacks`, `FaceArmorPassiveMultiplierBonus`, `FaceShield`, `FamiliarSecondaryDamageImmunity`, `FlowerPowerAuraBrace`, `FlowerPowerAuraStrength`, `FlowersOnEndTurn`, `FlyDamageIncrease`, `Flying`, `FollowUp`, `ForceSpecificInjury`, `ForceUseAbility`, `FreePathfindElement`, `FreeSpellsAtFullMana`, `FreezePiercing`, `FrontstabBasicAttackCritChance`, `FullHeal`, `FullHealthCritChance`, `FullPower`, `FurnitureStats`, `GainExtraShield`, `GravityWell`, `HPGainBlock`, `HeadArmorPassiveMultiplierBonus`, `HealDamagesEnemies`, `HealsAlsoRegenMana`, `HealsCanRevive`, `HealthRegenUp`, `HolyShieldTransferToTaggedMinions`, `HouseFoodRequirementMultiplier`, `Hypomania`, `IgnoreTiles`, `ImmortalLeeches`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `IncreaseHealingSpellRange`, `IncreaseSpellRange`, `InfiniteRebirth`, `InnateElement`, `InvertBrainFaction`, `KillsHeal`, `KillsToMeat`, `KnockbackImmunity`, `LateBloomer`, `LevelUpClassOverride`, `LightningAspectCharge`, `LightningRod`, `LimitDamage`, `LimitHeal`, `LimitSelfKnockbackDamage`, `LimitedTileTrail`, `LineOfSightTrueSightAura`, `LobbedHook`, `LowHealthAllyDodgeChanceAura`, `Madness`, `MakeBasicAttackPassThroughThings`, `MakeSpellsRequireCharge`, `ManaCostReductionTagged`, `ManaRegenMultiplierIfManaEmpty`, `MaxAccuracy`, `MaxStartingMana`, `MegaMinions`, `MeleeRevengeDamage`, `Metal`, `MetalDetector`, `MinimumTech`, `MissChance`, `MoveAndUseAbilityEachTurnBeginIfPossible`, `MoveAwayFromDamageSource`, `MoveQuivered`, `MoveSpeedMultiplier`, `MoveTowardsDamageSource`, `MoveWhenDamaged`, `MovementReaction`, `MulticlassLevelUp`, `NeckArmorPassiveMultiplierBonus`, `NoManaRegen`, `NoReflection`, `NubbyTossPriority`, `NumbingLeeches`, `OverhealGainsBothShield`, `OverrideBasicAttack`, `OverrideMaxHealth`, `OverrideMaxMana`, `OverridePalette`, `Paranoia`, `ParasitesArentCursed`, `PassiveAfterXKills`, `PassiveAtFullHealth`, `PassiveAtHealthThreshold`, `PassiveAtInjuryThreshold`, `PassiveAtStatThreshold`, `PassiveIfAllArmorEmpty`, `PassiveIfEmptyFace`, `PassiveIfEmptyHead`, `PassiveIfEmptyNeck`, `PassiveLevelScaledStatus`, `PassiveLevelUpAtCombatEnd`, `PassiveUntilCastSpell`, `PassiveUntilGetKill`, `PassiveWhenAffectedByElement`, `PassiveWhenAtFullMana`, `PassiveWhenTheAlpha`, `PassiveWhileInMonkMeleeStance`, `PassiveWhileInMonkRangedStance`, `PassiveWhilePreviewingMonkRangedStance`, `PassiveWhileWearingMetal`, `PermanentImmobile`, `PermanentItems`, `PermanentKitten`, `PermanentMadness`, `Poison`, `PoisonThorns`, `PoopWhenHit`, `ProtectTargetedAllies`, `Quiver`, `Quivered`, `RandomPassivePool`, `RangedTrueShot`, `RealTimePressure_OneUnit`, `ReceivedStatusReplacement`, `RemoveLineOfSightRestrictions`, `RemoveOncePerFightRestriction`, `ReplaceBasicAttack`, `ReplaceBasicAttackWhenCastable`, `ReplaceBasicAttackWhenDead`, `ReplaceBasicMove`, `ReplaceSpawnedObjects`, `RevengeDamage`, `ReviveOnWin`, `RobotsInheritArmor`, `RockDetector`, `ScaledStatusOnBleedDamage`, `ScaledStatusOnOverMana`, `ScaledStatusOnSpendMana`, `SchrodingerDisorder`, `Scleroderma`, `SecurityBotProtect`, `SelfDamageWhenDealDamage`, `SetDefaultFacePassive`, `SetSpellCosts`, `ShareHealthRegen`, `SharePickups`, `ShoulderCheck`, `ShovingMatch`, `ShowHiddenThings`, `SizeScale`, `Slow`, `SmallEnemiesIgnoreYou`, `SmallRockBehavior`, `SmiteEnemiesWhoKill`, `SpawnCatCopyOnBattleStart`, `SpawnCreepOnHit`, `SpawnEachTurn`, `SpawnObjectOnPopCorpse`, `SpawnOnBattleStart`, `SpawnOnBattleStartRandomEmptyTile`, `SpawnThingOnDamage`, `SpawnThingOnDeath`, `SpecialFriends`, `SpeedUp`, `SplittableMove`, `SpreadExtraDebuffs`, `SpreadPainBonus`, `StatMinimum`, `StatsAtLowHealth`, `StatusAdjacentOnTheirTurnBegin`, `StatusAfterCastSpell`, `StatusAlliesOnBattleStart`, `StatusAlliesOnDeath`, `StatusAlliesOnGainCoins`, `StatusAlliesOnKill`, `StatusAllyWhenAllySpendsMana`, `StatusAnyCatAllyWhoKills`, `StatusDamagers`, `StatusEachTurnBegin`, `StatusEachTurnEnd`, `StatusEachTurnEndForEachTurn`, `StatusEachTurnEndPerEnemyKill`, `StatusEnemiesOnDeath`, `StatusEveryXSpellCasts`, `StatusEveryXTurnBegins`, `StatusIfBattleAlreadyBegan`, `StatusIfUnusedMovePoints`, `StatusImmunity`, `StatusKilledCharacters`, `StatusKillers`, `StatusOnAllyCatDeath`, `StatusOnAnyDeath`, `StatusOnBattleEnd`, `StatusOnBattleEndIfKillThresholdMet`, `StatusOnBattleStart`, `StatusOnBreakItem`, `StatusOnCastSpell`, `StatusOnCollectPickup`, `StatusOnCrit`, `StatusOnDealtDamage`, `StatusOnDealtDamageThreshold`, `StatusOnEatFood`, `StatusOnEatPill`, `StatusOnEndMove`, `StatusOnGainCoins`, `StatusOnGainShield`, `StatusOnHeal`, `StatusOnHealed`, `StatusOnKill`, `StatusOnKillEnemy`, `StatusOnLoseShield`, `StatusOnOverHealed`, `StatusOnOverMana`, `StatusOnPickupCoins`, `StatusOnPopCorpse`, `StatusOnStanceSwitch`, `StatusOnTakeHealthDamage`, `StatusOnTookDamage`, `StatusOnTookDamageFromAbility`, `StatusOnTookDamageFromEnemyAbility`, `StatusOnTriggerTrap`, `StatusOnTurnEndIfCastNSpells`, `StatusOnTurnEndIfDidntCastAbilityTypes`, `StatusOnTurnEndIfManaExact`, `StatusOnTurnEndIfManaOrHealthExact`, `StatusOnUseAbilityWithTag`, `StatusOnUseBasicAttack`, `StatusOnUseElementAbility`, `StatusPerInjury`, `StatusReplacement`, `StatusThingsKnockedBack`, `StatusWhenAllySpendsMana`, `Stealth`, `StrengthForEachNeighboringEnemy`, `StrengthInNumbersAura`, `StrengthUp`, `StrictLimitDamage`, `Study`, `TaggedPickupEffectReplacement`, `TauntAlways`, `TauntAtFullHealth`, `Tech`, `TempInitiativeChange`, `TheHunger`, `Thorns`, `TileDamageMultiplier`, `TileTrail`, `TourettesMeows`, `TowerDefense`, `TowerDefenseReflex`, `Trample`, `TrapEffectsMultiplier`, `TrinketActiveEffectsMultiplierBonus`, `TrinketPassiveMultiplierBonus`, `Triskaidekaphobia`, `UncappedHP`, `UncappedMana`, `UpgradeLevelUpClassActives`, `UpgradeLevelUpClassPassives`, `UpgradeSpawnedPickups`, `Vegan`, `Vengeful`, `WaterWalk`, `Weakness`, `WeaponActiveEffectsMultiplierBonus`, `WeaponCountsAsBasicAttack`, `WeaponDamageMultiplierBonus`, `WeaponPassiveMultiplierBonus`, `WobblyCat`

### `past` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `patch_up` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pick_lock` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pilfer` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pirouette` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `place_gristle` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `play` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `poop` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `popup` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `prompt`

### `post_spawn_statuses` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DoDamage`, `EnterMount`, `VisualFXTile`

### `properties` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `layer`, `scale`

### `protection` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `pull` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pull_it_out` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `pull_lever` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `purify` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `push_buttons` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `push_through` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `put_in_coins` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `put_out_of_misery` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `random_chance` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `get_item_from_pool`

### `rare` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (75):** `add_weather`, `ally_ambush_next_fights`, `ambush`, `ambush_next_basic_fights`, `battle`, `clear_result_animation`, `conditional_reward`, `decrement_legacy_counter`, `event_now`, `event_now_same_cat`, `full_heal`, `gain_cat_familiar`, `gain_coins`, `gain_disorder`, `gain_disorder_from_pool`, `gain_familiar`, `gain_food`, `gain_immortal_familiar`, `get_and_equip_item`, `get_item`, `get_item_from_pool`, `get_parasite`, `get_parasite_from_pool`, `global_effect_next_fight`, `heal_disorder`, `hide_appearance_changes`, `increment_legacy_counter`, `injury`, `kill`, `learn_ability`, `learn_ability_from_pool`, `learn_passive`, `learn_passive_from_pool`, `leave_party_temporarily`, `level_up`, `lose_all_equipped_items`, `lose_item`, `lose_item_from_inventory`, `lose_specific_item`, `make_old`, `mutation`, `next_event_bonus`, `next_event_from_set`, `override_end_option_prompt`, `party_damage`, `party_heal`, `party_heal_disorder`, `party_heal_injury`, `party_injury`, `party_permanent_stats`, `party_permanent_stats_exclude_self`, `party_random_mutation`, `party_random_mutation_from_set`, `party_status_next_fight`, `permanent_stats`, `play_animation`, `play_result_animation`, `prompt`, `random_mutation`, `random_mutation_from_set`, `random_pool`, `scramble_abilities`, `scramble_basic_attack`, `self_damage`, `self_status_next_fight`, `set_adventure_token`, `set_age`, `set_frame`, `set_legacy_token`, `shop_now`, `spawn_reflection_next_fight`, `spawn_unit_next_fight`, `trigger_adventure_unlock`, `upgrade_ability`, `upgrade_passive`

### `read` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `receive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `red` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `red_needle` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `reflect` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `remove` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `remove_the_nail` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `repair` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `repell` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `rest` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `reverb` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `battle`

### `revive` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `reward` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (26):** `ambush_next_basic_fights`, `clear_adventure_token`, `common`, `cutscene_on_exit`, `event_now`, `gain_coins`, `gain_disorder_from_pool`, `get_item`, `get_item_from_pool`, `get_parasite_from_pool`, `injury`, `level_up`, `next_event_bonus`, `party_damage`, `play_animation`, `prompt`, `random_chance`, `random_pool`, `rare`, `set_adventure_token`, `set_frame`, `set_legacy_token`, `set_subject`, `spawn_unit_next_fight`, `trigger_adventure_unlock`, `weight`

### `rub` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `run` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `run_again` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `run_away` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sacrifice` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `sacrifice_full_favor` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `sacrifice_normal` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `sacrifice_partial_favor` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `sacrifice_quest` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `self_damage` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Event Keys}`

**In Master but NOT in split file (5):** `cant_miss`, `effects`, `heal`, `non_lethal`, `piercing`

### `self_status_next_fight` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (39):** `AbilityOnBattleStart`, `AbilityOnBattleStart_Immediate`, `AddInitiative`, `AddStartingMana`, `AllStatsUp`, `AlphaTurns`, `Bleed`, `Blind`, `Bruise`, `Burn`, `ChangeTileUnderCharacterAtStart`, `CharismaUp`, `Confusion`, `ConstitutionUp`, `DexterityUp`, `DivineShield`, `Fear`, `Fights`, `HealthRegenUp`, `IntelligenceUp`, `LuckUp`, `Madness`, `MissChance`, `NoHealthRegen`, `NoManaRegen`, `PermanentConfusion`, `Poison`, `ProbeCharmed`, `RandomStatUp`, `Rot`, `Sleep`, `Slow`, `SpeedUp`, `SpiderInfested`, `StrengthUp`, `Stun`, `Tarred`, `TempStrengthUp`, `Webbed`

### `setup` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `conditional_reward`, `set_frame`

### `shake` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `skip` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `slip_through` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `smash` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sneak` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sneak_by` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `sneak_past_alt` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `soul` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `spawn` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `custom_additional_ai_weight`, `layer`, `lob`, `spawnin_animation`

### `spawn_reflection_next_fight` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `mutation`

### `speed` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `spell_graphics_override` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (4):** `area_particle`, `center_particle`, `palette`, `particle`

### `splash_damage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (7):** `crit_chance`, `effects`, `force_no_knockback`, `force_play_hit_animation`, `layer`, `makes_contact`, `override_trample_damage`

### `stats` (from `Miscellaneous.md`)

**In split file but NOT in Master (7):** `charisma`, `constitution`, `dexterity`, `intelligence`, `luck`, `speed`, `strength`

### `statuses` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FindItemFromPool`, `HealthGain`, `PermanentDexterity`

### `statuses_on_enter_form` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `UseAbility`

### `steven_milliontrashed` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `level_display`, `repeat`

### `surprise` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `sweet_talk` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `swim` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `tail` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `take` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `take_blood` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `talk` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `talk_to` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `tappytoes` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `target` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (4):** `aoe_spell_on_land`, `dont_orient`, `force_no_contact`, `min_range`

### `teleport` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `temporary_effects` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AfterImage`, `DoubleLoot`, `KnockbackImmunity`, `TileTrail`, `TileTrail_Ahead`, `Trample`

### `thorns` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `threshold` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `con`

### `throw` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `tink_aggression` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

### `tink_basestats` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

### `tink_inbreeding` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

### `tink_max_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (4):** `coins`, `favor`, `level_display`, `reward_text`

### `tink_max_repeating` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `coins`, `favor`, `level_display`, `repeat`, `reward_text`

### `tink_prettybow` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `gift_item`, `reward_text`

### `tink_relationships` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

### `tink_sexuality` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

### `tink_tags` (from `Miscellaneous.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

### `touch` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `tracy_blankcollar1` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_blankcollar2` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_blankcollar3` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage1` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage10` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage2` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage3` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage4` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage5` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage6` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage7` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage8` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_foodstorage9` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_idol1` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_idol2` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_idol3` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_idol4` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_idol5` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_idol6` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_idol7` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

### `tracy_max_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `level_display`, `required_age`, `reward_text`, `tracy_special_item`

### `tracy_max_repeating` (from `Miscellaneous.md`)

**In split file but NOT in Master (6):** `favor`, `level_display`, `repeat`, `required_age`, `reward_text`, `tracy_special_item`

### `traverse` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (3):** `play_animation`, `prompt`, `shop_now`

### `treasure` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `level`, `type`

### `triattack` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `turnon` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `upgrade_storage_1` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

### `upgrade_storage_2` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

### `upgrade_storage_3` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

### `upgrade_storage_4` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

### `upgrade_storage_5` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

### `upgrade_storage_6` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

### `upgrade_storage_7` (from `Miscellaneous.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

### `upgrade_storage_repeating_crazy` (from `Miscellaneous.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

### `upgrade_storage_repeating_hard` (from `Miscellaneous.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

### `upgrade_storage_repeating_impossible` (from `Miscellaneous.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

### `upgrade_storage_repeating_intro` (from `Miscellaneous.md`)

**In split file but NOT in Master (7):** `favor`, `level_display`, `rep_reward_count`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

### `upgrade_storage_repeating_normal` (from `Miscellaneous.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

### `upgrade_yourself` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_item` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_toilet_con` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_toilet_str` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `use_weapon` (from `Miscellaneous.md`)

**In split file but NOT in Master (4):** `good`, `label`, `requirements`, `{Event Keys}`

### `w1` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w2` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w3` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w4` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w5` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `w6` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `welcome` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_boneyard` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_bunker` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_caves` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_core` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_crater` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_desert` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_future` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_iceage` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_junkyard` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_jurassic` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_lab` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_moon` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_sewers` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_theend` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_water` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_water_cheap` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `wheezies` (from `Miscellaneous.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Graphics Keys}`

**In Master but NOT in split file (2):** `animation`, `bad`

### `withstand` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `yank_it_out` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `yellow_needle` (from `Miscellaneous.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `bad`

### `ROOT` (from `NPC_Scripts.md`)

**In split file but NOT in Master (485):** `Jack_Gainaltfurniture`, `also`, `beanies_begin_accepting_cats`, `beanies_bombquest_2`, `beanies_bombquest_3`, `beanies_bombquest_amnesia`, `beanies_bombquest_begin`, `beanies_bombquest_fail_jarofblood`, `beanies_bombquest_fail_jarofchaos`, `beanies_bombquest_fail_jarofradiation`, `beanies_bombquest_fail_nuke`, `beanies_future_intro`, `beanies_hitler3`, `beanies_hitler3_defeat`, `beanies_iloveyou`, `beanies_infinite_intro`, `beanies_jurassic_intro`, `beanies_lab_intro`, `beanies_quest_complete`, `beanies_quest_fail`, `beanies_quests_intro`, `beanies_quests_repeat`, `beanies_rift_intro`, `beanies_screenshake_test`, `beanies_seefuture`, `beanies_seetheend`, `beanies_terminator1_defeat`, `beanies_terminator2_defeat`, `beanies_theend_intro`, `beanies_timemachine_2`, `beanies_timemachine_intro`, `beanies_vscreator1`, `beanies_vscreator2`, `beanies_vscreator3`, `beanies_vscreator4`, `beanies_vscreatorintro`, `beaniesquest_complete_AI`, `beaniesquest_complete_AirHorn`, `beaniesquest_complete_AngryFace`, `beaniesquest_complete_AnimalHands`, `beaniesquest_complete_BubbleBoy`, `beaniesquest_complete_ChadImplant`, `beaniesquest_complete_ChaosDevice`, `beaniesquest_complete_DimensionalDivider`, `beaniesquest_complete_DiseaseJar`, `beaniesquest_complete_ExperimentalTreatment`, `beaniesquest_complete_FartFace`, `beaniesquest_complete_FigLeaf`, `beaniesquest_complete_Generic`, `beaniesquest_complete_GlassCannon`, `beaniesquest_complete_HardPill`, `beaniesquest_complete_HiveMind`, `beaniesquest_complete_MagicMirror`, `beaniesquest_complete_MeStone`, `beaniesquest_complete_MultilinkCable`, `beaniesquest_complete_MysteriousDice`, `beaniesquest_complete_MysteriousGlasses`, `beaniesquest_complete_NDEDevice`, `beaniesquest_complete_NuclearKnife`, `beaniesquest_complete_PartialLobotomy`, `beaniesquest_complete_PartyDetonator`, `beaniesquest_complete_PersonalHeater`, `beaniesquest_complete_PersuasionDevice`, `beaniesquest_complete_PrincessHat`, `beaniesquest_complete_RealityScrambler`, `beaniesquest_complete_Redacted`, `beaniesquest_complete_SpiderInjector`, `beaniesquest_complete_Stopwatch`, `beaniesquest_complete_StorageLocker`, `beaniesquest_complete_TheIOU`, `beaniesquest_complete_TheLoner`, `beaniesquest_complete_Trapfest99`, `beaniesquest_complete_UltraVision3000`, `beaniesquest_fail_AI`, `beaniesquest_fail_AirHorn`, `beaniesquest_fail_AngryFace`, `beaniesquest_fail_AnimalHands`, `beaniesquest_fail_BubbleBoy`, `beaniesquest_fail_ChadImplant`, `beaniesquest_fail_ChaosDevice`, `beaniesquest_fail_DimensionalDivider`, `beaniesquest_fail_DiseaseJar`, `beaniesquest_fail_ExperimentalTreatment`, `beaniesquest_fail_FartFace`, `beaniesquest_fail_FigLeaf`, `beaniesquest_fail_Generic`, `beaniesquest_fail_GlassCannon`, `beaniesquest_fail_HardPill`, `beaniesquest_fail_HiveMind`, `beaniesquest_fail_MagicMirror`, `beaniesquest_fail_MeStone`, `beaniesquest_fail_MultilinkCable`, `beaniesquest_fail_MysteriousDice`, `beaniesquest_fail_MysteriousGlasses`, `beaniesquest_fail_NDEDevice`, `beaniesquest_fail_NuclearKnife`, `beaniesquest_fail_PartialLobotomy`, `beaniesquest_fail_PartyDetonator`, `beaniesquest_fail_PersonalHeater`, `beaniesquest_fail_PersuasionDevice`, `beaniesquest_fail_PrincessHat`, `beaniesquest_fail_RealityScrambler`, `beaniesquest_fail_Redacted`, `beaniesquest_fail_SpiderInjector`, `beaniesquest_fail_Stopwatch`, `beaniesquest_fail_StorageLocker`, `beaniesquest_fail_TheIOU`, `beaniesquest_fail_TheLoner`, `beaniesquest_fail_Trapfest99`, `beaniesquest_fail_UltraVision3000`, `beaniesquest_intro_AI`, `beaniesquest_intro_AirHorn`, `beaniesquest_intro_AngryFace`, `beaniesquest_intro_AnimalHands`, `beaniesquest_intro_BubbleBoy`, `beaniesquest_intro_ChadImplant`, `beaniesquest_intro_ChaosDevice`, `beaniesquest_intro_DimensionalDivider`, `beaniesquest_intro_DiseaseJar`, `beaniesquest_intro_ExperimentalTreatment`, `beaniesquest_intro_FartFace`, `beaniesquest_intro_FigLeaf`, `beaniesquest_intro_Generic`, `beaniesquest_intro_GlassCannon`, `beaniesquest_intro_HardPill`, `beaniesquest_intro_HiveMind`, `beaniesquest_intro_MagicMirror`, `beaniesquest_intro_MeStone`, `beaniesquest_intro_MultilinkCable`, `beaniesquest_intro_MysteriousDice`, `beaniesquest_intro_MysteriousGlasses`, `beaniesquest_intro_NDEDevice`, `beaniesquest_intro_NuclearKnife`, `beaniesquest_intro_PartialLobotomy`, `beaniesquest_intro_PartyDetonator`, `beaniesquest_intro_PersonalHeater`, `beaniesquest_intro_PersuasionDevice`, `beaniesquest_intro_PrincessHat`, `beaniesquest_intro_RealityScrambler`, `beaniesquest_intro_Redacted`, `beaniesquest_intro_SpiderInjector`, `beaniesquest_intro_Stopwatch`, `beaniesquest_intro_StorageLocker`, `beaniesquest_intro_TheIOU`, `beaniesquest_intro_TheLoner`, `beaniesquest_intro_Trapfest99`, `beaniesquest_intro_UltraVision3000`, `boss_fight_intro`, `boss_fight_round2`, `butch_begin_accepting_cats`, `butch_boneyard_intro`, `butch_first_house_boss_beat`, `butch_pyro`, `butch_tina1`, `butch_tips_backstab`, `butch_tips_charisma`, `butch_tips_combat`, `butch_tips_disorders`, `butch_tips_drafting`, `butch_tips_elements`, `butch_tips_hard`, `butch_tips_headhome`, `butch_tips_houseboss`, `butch_tips_info`, `butch_tips_intelligence`, `butch_tips_intro`, `butch_tips_items`, `butch_tips_lesscats`, `butch_tips_magicdamage`, `butch_tips_passives`, `butch_tips_reorient`, `butch_tips_rewards`, `butch_tips_tacticalview`, `butch_tips_turnorder`, `butch_tips_wellrounded`, `can_still_use_attack`, `can_still_use_attack_didntspell`, `cant_afford`, `cant_afford_a`, `cant_afford_b`, `cant_afford_c`, `cant_afford_d`, `cant_afford_iceage`, `cant_afford_jurassic`, `cant_afford_moon`, `cant_afford_theend`, `class_unlock_butcher`, `class_unlock_druid`, `class_unlock_jester`, `class_unlock_medic`, `class_unlock_monk`, `class_unlock_necromancer`, `class_unlock_psychic`, `class_unlock_thief`, `class_unlock_tinkerer`, `collected_new_items`, `collected_nothing`, `do_not_end_turn`, `done_spitting_fail_ally`, `done_spitting_fail_miss`, `done_spitting_fail_rat`, `done_spitting_success`, `ending`, `finish_adventure`, `first_fight_intro`, `first_house_boss_tomorrow`, `first_house_hint_retired`, `forward_to_tips`, `frank_caves_intro`, `frank_ending`, `frank_max1`, `frank_max2`, `frank_max3`, `frank_max4`, `frank_max5`, `frank_max_intro`, `frank_max_repeating`, `frank_terminator2`, `frank_tips_1`, `frank_tips_10`, `frank_tips_2`, `frank_tips_3`, `frank_tips_4`, `frank_tips_5`, `frank_tips_6`, `frank_tips_7`, `frank_tips_8`, `frank_tips_9`, `gone`, `hide_text`, `house_intro`, `house_kitten_box`, `house_pass_day`, `house_pass_day2`, `house_pipe`, `house_retired_cat_box`, `house_starred_box`, `house_strays`, `house_upgrade_4throom`, `house_upgrade_attic`, `house_upgrade_basement`, `house_upgrade_basement2`, `house_upgrade_basement3`, `house_upgrade_basement4`, `house_upgrade_basement5`, `house_upgrade_largehouse`, `house_upgrade_mediumhouse`, `intro`, `introduce_hard_path`, `jack_begin_accepting_cats`, `jack_desert_intro`, `jack_introduction`, `jack_max1`, `jack_max2`, `jack_max3`, `jack_max4`, `jack_max5`, `jack_max_intro`, `jack_max_repeating`, `jack_shopupgrade1`, `jack_shopupgrade2`, `jack_shopupgrade3`, `jack_shopupgrade4`, `jack_zara`, `level_up_didnt_select_sunburn`, `level_up_intro`, `level_up_selected_sunburn`, `low_on_food`, `map_click_node`, `map_equip_items`, `map_equip_items2`, `melee_attack_rat`, `melee_cat_spit`, `melee_cat_spit_fail_ally`, `melee_cat_spit_fail_miss`, `melee_cat_spit_fail_rat`, `melee_cat_spit_ignore`, `melee_cat_spit_success`, `melee_killed_rat`, `melee_move2`, `melee_out_of_actions`, `new_adventure`, `organ_boneyard_intro`, `organ_intro`, `organ_max1`, `organ_max2`, `organ_max3`, `organ_max4`, `organ_max5`, `organ_max_intro`, `organ_max_repeating`, `organ_rename`, `organ_throbbingdomain_intro`, `organ_tina3`, `organ_unlock`, `organ_upgrade1`, `organ_upgrade2`, `organ_upgrade3`, `organ_upgrade4`, `organ_upgrade5`, `organ_upgrade6`, `out_of_stock`, `purchase_item`, `purchase_item_a`, `purchase_item_b`, `purchase_item_c`, `purchase_item_d`, `purchase_item_iceage`, `purchase_item_jurassic`, `purchase_item_moon`, `purchase_item_theend`, `ranged_attack_tomtom`, `ranged_attack_tomtom_fail_ally`, `ranged_attack_tomtom_fail_miss`, `ranged_attack_tomtom_fail_rat`, `ranged_cat_attack`, `ranged_cat_early_attack2_ally`, `ranged_cat_early_attack2_miss`, `ranged_cat_early_attack2_rat`, `ranged_cat_early_attack_ally`, `ranged_cat_early_attack_miss`, `ranged_cat_early_attack_rat`, `ranged_cat_failmove`, `ranged_cat_intro`, `ranged_cat_roll`, `ranged_cat_rolled_first`, `states`, `steven_100`, `steven_introduction`, `steven_milliontrashed`, `steven_postendgame`, `steven_resummon`, `steven_savescum_1`, `steven_savescum_100`, `steven_savescum_1alt1`, `steven_savescum_1alt2`, `steven_savescum_1alt3`, `steven_savescum_2`, `steven_savescum_2alt1`, `steven_savescum_2alt2`, `steven_savescum_2alt3`, `steven_savescum_3`, `steven_savescum_3alt1`, `steven_savescum_3alt2`, `steven_savescum_3alt3`, `steven_savescum_4`, `steven_savescum_4alt1`, `steven_savescum_4alt2`, `steven_savescum_4alt3`, `steven_savescum_houseboss_1`, `steven_savescum_houseboss_100`, `steven_savescum_houseboss_2`, `steven_savescum_houseboss_3`, `steven_savescum_intro`, `steven_savescum_intro_houseboss`, `steven_unlock_act1_crazy`, `steven_unlock_act1_impossible`, `steven_unlock_act2_crazy`, `steven_unlock_act2_hard`, `steven_unlock_act2_impossible`, `steven_unlock_act3_crazy`, `steven_unlock_act3_hard`, `steven_unlock_act3_impossible`, `take_cats_inside`, `test_gamepad_prompts`, `tink_aggression`, `tink_basestats`, `tink_begin_accepting_cats`, `tink_inbreeding`, `tink_max1`, `tink_max10`, `tink_max2`, `tink_max3`, `tink_max4`, `tink_max5`, `tink_max6`, `tink_max7`, `tink_max8`, `tink_max9`, `tink_max_intro`, `tink_max_repeating`, `tink_prettybow`, `tink_relationships`, `tink_sexuality`, `tink_tags`, `tink_terminator`, `tink_tina2`, `tink_tips_appeal`, `tink_tips_basestats`, `tink_tips_cleaning`, `tink_tips_comfort`, `tink_tips_health`, `tink_tips_inbreeding`, `tink_tips_intro`, `tink_tips_multiclassing`, `tink_tips_mutation`, `tink_tips_stimulation`, `tracy_blankcollar1`, `tracy_blankcollar2`, `tracy_blankcollar3`, `tracy_foodbonus1`, `tracy_foodstorage1`, `tracy_foodstorage10`, `tracy_foodstorage2`, `tracy_foodstorage3`, `tracy_foodstorage4`, `tracy_foodstorage5`, `tracy_foodstorage6`, `tracy_foodstorage7`, `tracy_foodstorage8`, `tracy_foodstorage9`, `tracy_idol1`, `tracy_idol2`, `tracy_idol3`, `tracy_idol4`, `tracy_idol5`, `tracy_idol6`, `tracy_idol7`, `tracy_introduction`, `tracy_kaijufight`, `tracy_max1`, `tracy_max2`, `tracy_max3`, `tracy_max4`, `tracy_max5`, `tracy_max_intro`, `tracy_max_repeating`, `transitions`, `try_again_attack_rat`, `try_again_melee_move`, `tutorial_cat_dies`, `unknown`, `unprompted`, `unprompted1`, `unprompted2`, `unprompted3`, `unprompted4`, `unprompted5`, `unprompted6`, `unprompted_a`, `unprompted_b`, `unprompted_c`, `unprompted_d`, `unprompted_e`, `unprompted_f`, `unprompted_g`, `unprompted_h`, `unprompted_i`, `upgrade_storage_1`, `upgrade_storage_2`, `upgrade_storage_3`, `upgrade_storage_4`, `upgrade_storage_5`, `upgrade_storage_6`, `upgrade_storage_7`, `upgrade_storage_max1`, `upgrade_storage_max2`, `upgrade_storage_max3`, `upgrade_storage_max4`, `upgrade_storage_max5`, `upgrade_storage_repeating_crazy`, `upgrade_storage_repeating_hard`, `upgrade_storage_repeating_impossible`, `upgrade_storage_repeating_intro`, `upgrade_storage_repeating_normal`, `use_attack_after_used_weapon`, `use_weapon`, `welcome`, `welcome_boneyard`, `welcome_bunker`, `welcome_caves`, `welcome_core`, `welcome_crater`, `welcome_desert`, `welcome_future`, `welcome_iceage`, `welcome_junkyard`, `welcome_jurassic`, `welcome_lab`, `welcome_moon`, `welcome_sewers`, `welcome_theend`, `welcome_water`, `welcome_water_cheap`, `{Graphics Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `beanies_infinite_intro` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `beanies_rift_intro` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `boss_fight_intro` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `first_fight_intro` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `house_intro` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `house_strays` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `intro` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `level_up_intro` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_boneyard` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_bunker` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_caves` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_core` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_crater` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_desert` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_future` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_iceage` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_junkyard` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_jurassic` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_lab` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_moon` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_sewers` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_theend` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_water` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `welcome_water_cheap` (from `NPC_Scripts.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `delay`

### `AddPassivesToCharmed` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AddMaxHealth`, `AddSpeed`, `AddStatusToBasicAttack`, `DamageUp`

### `AddPassivesToMinions` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (27):** `AddMaxHealth`, `AddSpeed`, `AddStatusToBasicAttack`, `AddStatusToExplosions`, `AddUnfilledMaxHealth`, `DamageUp`, `DivineShield`, `EMP`, `FamiliarBonusAbility`, `ForceAttack`, `FreePathfindElement`, `GrassTileHealing`, `HealthGain`, `HealthRegenUp`, `HolyShieldTransferToSpawner`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `PassiveWhenAffectedByElement`, `PoisonThorns`, `Quivered`, `SafeExplosions`, `StatusAlliesOnKill`, `StatusOnKill`, `TakeExtraTurn`, `UncappedHP`, `WaterWalk`, `tag_filter`

### `AddPassivesToSummonAbilityMinions` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DamageUp`, `Doomed`, `MovementUp`

### `AddSelfStatusToBasicAttack` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `AddSelfStatusToWeapons` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ChanceToBreak`

### `AddStatusToAllDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Blind`, `Conditional_HasTag`, `LeaveBehindRockOnKnockback`, `NonLethal`

### `AddStatusToAllDamageAbilities` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Bleed`, `Piercing`, `Weakness`

### `AddStatusToBasicAttack` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (43):** `ApplyStatusIfCrit`, `ApplyToSource`, `BigSplashDamage`, `Bleed`, `Blind`, `BounceObject`, `Bruise`, `BurgleCoin`, `Burn`, `ChangeTile`, `Charmed`, `Conditional_Adjacent`, `Conditional_Ally`, `Conditional_Enemy`, `Conditional_HasTag`, `Conditional_Shielded`, `Conditional_SourceHasTag`, `Confusion`, `DamageOrHealConditionally`, `DistanceBonusDamage`, `Else`, `Fear`, `Freeze`, `KnockOutCoin`, `Knockback`, `Leech`, `Leeches`, `LuckUp`, `Madness`, `MagicWeakness`, `ManaLeeches`, `OverrideChainKnockback`, `OverrideChainKnockbackDamage`, `Piercing`, `Poison`, `Rot`, `Slow`, `SoulLink`, `SpawnBearTrapOnMiss`, `SplashDamage`, `SpreadDisease`, `Stun`, `Weakness`

### `AddStatusToBasicAttackWithCooldown` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `CharmedForceAttack`

### `AddStatusToBasicMeleeAttack` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Bruise`, `Confusion`, `FaceAway`, `SpreadDisease`, `Stun`

### `AddStatusToElementAbilities` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Bleed`, `ChangeTile`, `Conditional_Ally`, `Conditional_Enemy`

### `AddStatusToElementDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Burn`, `Conditional_Corpse`

### `AddStatusToExplosions` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `AddStatusToFirstBasicAttack` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charmed`

### `AddStatusToKnockbackDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bruise`

### `AddStatusToMeleeDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `DelayedWindCone`

### `AddStatusToSpells` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LeechPercent`

### `AddStatusToTrampleDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Cleave`

### `AddStatusToWeapons` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Bleed`, `Cleave`, `LeechPercent`, `PullSourceToKnockbackImmuneTarget`

### `AddStatusesIfPersistentWeatherElement` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `AddStatusesToReceivedElementalDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `ApplyStatusIfCrit` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Purge`

### `ApplyStatusesToRandomEnemiesEachTurn` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bounty`

### `ApplyToSource` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Shield`

### `BoostWeaponDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `crit_chance`

### `CatAPultAnimation` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `animation`

### `CatchProjectiles` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Quivered`

### `Conditional_Adjacent` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Bleed`, `BonusCritChance`, `BonusDamage`

### `Conditional_Ally` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `AllStatsUp`, `ApplyToSource`, `Cleanse`, `ClearNegativeEffects`, `DamageUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `TempSpeedUp`

### `Conditional_BadRoll` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Temporary`

### `Conditional_Boss` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `Stun`

### `Conditional_Corpse` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Charmed`, `DamageUp`, `OverrideDamage`, `Revive`, `SafeDoomed`, `SpeedUp`, `TakeExtraTurn`

### `Conditional_DoesDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Bleed`

### `Conditional_Enemy` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_PartyMember`, `Confusion`, `Else`, `RandomStatusFromPool`, `Stun`

### `Conditional_FirstApplicationThisTurn` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FillMana`, `ManaGain`, `TakeExtraTurn`

### `Conditional_GoodRoll` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `UseRandomSpell_Madness`

### `Conditional_HasTag` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Charmed`, `FlatLeechIfDamaged`

### `Conditional_NotBoss` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Enemy`

### `Conditional_PartyMember` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charmed`

### `Conditional_Shielded` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `BonusCritChance`

### `Conditional_SourceHasTag` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Ally`

### `CritsApplyStatus` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `Bleed`, `Bruise`, `Conditional_HasStatus`, `Confusion`, `Else`, `Immobile`, `ObjectOnHitCharacter`, `Stun`, `Weakness`

### `DamageNeighborsAfterMove` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `DamageNeighborsOnEndMove` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `cant_miss`, `effects`

### `Diabetes` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Confusion`

### `DistanceBonusDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `min_range`

### `Electric` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Stun`

### `Else` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `CaptureFamiliar`, `FactionConversion`, `Fear`, `Marked`, `PermanentCharm`, `TempSpeedUp`

### `EscapeSequence` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `RandomDistanceDisplace`

### `Eternal` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `TakeExtraTurn`

### `ExtraStatusWhenDealingDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Conditional_Ally`

### `Fire` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `Grass` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Poison`

### `Gravity` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Weakness`

### `GravityWell` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (2):** `cant_miss`, `effects`

### `Holy` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `FlatLeech`

### `HolyDamageBlessing` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Burn`

### `Ice` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Slow`

### `InfiniteRebirth` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `TempSpeedUp`

### `LateBloomer` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AllStatsUp`

### `LightningRod` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Tech`

### `MeleeRevengeDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Damaging Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Poison`, `SpreadDisease`, `Weakness`, `effects`

### `NextBattleStatus` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `FullHeal`

### `PassiveAfterXKills` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveAtFullHealth` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ManaCostReduction`

### `PassiveAtHealthThreshold` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `threshold`

### `PassiveAtInjuryThreshold` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `injury`, `passives`, `threshold`

### `PassiveAtStatThreshold` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `passives`, `threshold`

### `PassiveGroup` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `CharismaUp`, `IntelligenceUp`, `SetDefaultFace`, `SpeedUp`

### `PassiveIfAllArmorEmpty` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `AddSpellDamage`, `CounterAttack`, `CritsApplyStatus`, `ExtraMovePoints`, `Flying`, `ManaCostReduction`, `StatusOnStanceSwitch`

### `PassiveIfEmptyFace` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddCritMultiplier`, `CritChanceUp`, `DodgeChance`, `KineticSpikes`, `StatusOnStanceSwitch`

### `PassiveIfEmptyHead` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddCritMultiplier`, `CritChanceUp`, `DodgeChance`, `KineticSpikes`, `StatusOnStanceSwitch`

### `PassiveIfEmptyNeck` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddCritMultiplier`, `CritChanceUp`, `DodgeChance`, `KineticSpikes`, `StatusOnStanceSwitch`

### `PassiveLevelScaledStatus` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Shield`, `Trample`

### `PassiveUntilCastSpell` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `StatusAlliesEachTurn`

### `PassiveWhenAffectedByElement` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `passives`

### `PassiveWhenAtFullMana` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AddMovement`, `AddStatusToBasicAttack`, `Brace`, `Flying`, `ReplaceBasicMove`

### `PassiveWhileInMonkMeleeStance` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Brace`, `HealthRegenUp`

### `PassiveWhileInMonkRangedStance` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AddBonusRange`, `AddSpellDamage`, `KineticSpikes`

### `PassiveWhilePreviewingMonkRangedStance` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AddBonusRange`

### `ROOT` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (25):** `auto_plus_signs_on_name`, `bonus_items`, `cha`, `class`, `con`, `desc_multiclass`, `dex`, `divine_shield`, `empty_armor_scaled_stats`, `grant_ability`, `icon`, `int`, `keyword_tooltips`, `lck`, `lock_item_slot`, `name_mod`, `override_basic_attack`, `schadenfreude_scaled_stats`, `shield`, `spd`, `stats`, `str`, `tags`, `{Graphics Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `RandomPassivePool` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PassiveGroup`

### `RandomStatusFromPool` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (37):** `AllStatsUp`, `Bleed`, `BleedThorns`, `Blind`, `Brace`, `Bruise`, `Burn`, `Charge`, `Charmed`, `Confusion`, `ConstitutionUp`, `DiminishingHealthRegen`, `DivineShield`, `Fear`, `Freeze`, `Immobile`, `KineticSpikes`, `Madness`, `MagicWeakness`, `Marked`, `MoveQuivered`, `ObjectOnHitCharacter`, `Petrify`, `Poison`, `Quivered`, `Reflect`, `Shield`, `Sleep`, `Slow`, `SpawnCoinAnywhere`, `SpeedUp`, `StatusGroup`, `StrengthUp`, `Stun`, `Tarred`, `Thorns`, `Weakness`

### `RevengeDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `ScaledStatusOnBleedDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Charge`

### `ScaledStatusOnLoseShield` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Thorns`

### `ScaledStatusOnOverMana` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Cleanse`, `RandomMagicMissile`

### `Shadow` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `crit_chance`

### `SmiteEnemiesWhoKill` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `SpecialFriends` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `HealthGain`

### `StatsAtLowHealth` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `threshold`

### `StatusAdjacentOnTheirTurnBegin` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `ForceMoveAway`

### `StatusAfterCastSpell` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `TempDamageUp`, `TempSpellDamageUp`

### `StatusAlliesEachTurn` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomStatUp`

### `StatusAlliesOnBattleStart` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `EquipTemporaryItem`

### `StatusAlliesOnDeath` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `AllStatsUp`, `Freeze`, `FullHeal`, `HealAndOverhealToShield`, `Reanimate`, `TakeExtraTurn`

### `StatusAlliesOnGainCoins` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `HealthGain`, `LuckUp`

### `StatusAlliesOnKill` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `AllStatsUp`, `DamageUp`, `HealthGain`

### `StatusAlliesOnSpendMana` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ManaGain`

### `StatusAlliesScaledByCursedOnDeath` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LuckUp`

### `StatusAllyWhenAllySpendsMana` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `threshold`

### `StatusAnyCatAllyWhoKills` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AlphaCat`

### `StatusDamagers` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Fear`, `LuckUp`

### `StatusEachTurnBegin` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `Conditional_BadRoll`, `Conditional_GoodRoll`, `Fear`, `FillMana`, `ForceUseAbility`, `IntelligenceUp`, `RandomStatUp`

### `StatusEachTurnEnd` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (11):** `EmptyMana`, `ForceUseAbility`, `IntelligenceUp`, `KineticSpikes`, `NonStackingDivineShield`, `ObjectOnHitCharacter`, `PermanentMadness`, `RangeUp`, `SpeedUp`, `StrengthUp`, `UseAbility_Madness`

### `StatusEachTurnEndForEachTurn` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `RandomMagicMissile`

### `StatusEachTurnEndPerEnemyKill` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ObjectOnHitCharacter`

### `StatusEnemiesOnDeath` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AllStatsUp`, `Freeze`

### `StatusEveryXSpellCasts` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `ReduceManaCost`, `RepairWeapon`, `RepairWeaponCondition`, `SpellDamageUp`

### `StatusEveryXTurnBegins` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `DivineShield`

### `StatusGroup` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `DexterityUp`, `LuckUp`, `SpawnCoinAnywhere`, `SpeedUp`

### `StatusIfBattleAlreadyBegan` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PermanentMadness`

### `StatusIfUnusedMovePoints` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `Brace`, `ConstitutionUp`, `HealthGain`, `ManaGain`, `MoveQuivered`, `Shield`

### `StatusKilledCharacters` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `AutoReanimate`, `Conditional_Ally`

### `StatusKillers` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Conditional_Boss`, `Conditional_NotBoss`

### `StatusOnAllyCatDeath` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `AllStatsUp`, `FillMana`, `HealthGain`, `PercentHeal`, `TakeExtraTurn`

### `StatusOnAnyDeath` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `LuckUp`

### `StatusOnBattleEnd` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (9):** `CureDisease`, `FindItemFromPool`, `NextBattleStatus`, `PermanentConstitution`, `PermanentIntelligence`, `PermanentSpeed`, `PermanentStrength`, `RandomMutation`, `RandomPermanentStat`

### `StatusOnBattleStart` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `FullHeal`, `Sleep`

### `StatusOnBreakItem` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `Shield`, `Thorns`

### `StatusOnCastSpell` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Charge`, `CurrentWeaponDamageUp`, `HealthGain`

### `StatusOnCollectPickup` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Tech`

### `StatusOnCrit` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `CritChanceUp`, `DamageUp`, `LuckUp`, `RandomStatUp`, `Shield`

### `StatusOnDealtDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `TempDexterityUp`, `TempLuckUp`, `TempStrengthUp`

### `StatusOnDealtDamageThreshold` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `RefreshMovePoints`, `Shield`, `threshold`

### `StatusOnEatFood` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `Cleanse`, `IntelligenceUp`, `RandomStatUp`, `StrengthUp`

### `StatusOnEatPill` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `AllStatsUp`

### `StatusOnEndMove` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ForceAttack`

### `StatusOnGainCoins` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DivineShield`, `RandomStatusFromPool`

### `StatusOnGainShield` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Temporary`

### `StatusOnHeal` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `RandomStatUp`, `SpeedUp`

### `StatusOnHealed` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `ObjectOnHitCharacter`, `RandomStatusFromPool`, `Thorns`

### `StatusOnKill` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (13):** `AllStatsUp`, `Conditional_FirstApplicationThisTurn`, `DamageUp`, `EquipPermanentItem`, `HealthGain`, `LuckUp`, `RandomStatUp`, `RefreshActPoints`, `RefreshMovePoints`, `SpeedUp`, `Stealth`, `StrengthUp`, `TakeBonusTurnWithStatus`

### `StatusOnKillEnemy` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `DivineShield`, `HealthGain`, `ManaGain`, `RefreshMovePoints`

### `StatusOnLoseShield` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Thorns`

### `StatusOnOverHealed` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `CurrentWeaponDamageUp`, `ForceUseAbility_NonStack`, `StrengthUp`

### `StatusOnOverMana` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DivineShield`, `IntelligenceUp`, `SpellDamageUp`

### `StatusOnPickupCoins` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DexterityUp`, `RefreshMovePoints`, `SpeedUp`

### `StatusOnPopCorpse` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `StatusOnStanceSwitch` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (6):** `ForceUseAbility`, `NextBasicAttackCritsThisTurn`, `PartialCleanse`, `RandomMagicMissile`, `RandomStatUp`, `Shield`

### `StatusOnTakeHealthDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `PermanentConstitution`

### `StatusOnTookDamage` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (18):** `Conditional_HasStatus`, `ConstitutionUp`, `Craft`, `DamageUp`, `DiminishingHealthRegen`, `Else`, `IntelligenceUp`, `MovementUp`, `RandomInjury`, `RandomStatUp`, `RandomStatusFromPool`, `Shield`, `SpeedUp`, `StrengthUp`, `TempDamageUp`, `TempMovement`, `Temporary`, `Thorns`

### `StatusOnTookDamageFromAbility` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DiminishingHealthRegen`, `Shield`

### `StatusOnTookDamageFromEnemyAbility` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `MoveQuivered`, `Quivered`

### `StatusOnTriggerTrap` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `DexterityUp`, `Quivered`

### `StatusOnTurnEndIfCastNSpells` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `DoubleCastSpell`, `MoveQuivered`, `Quivered`

### `StatusOnTurnEndIfDidntCastAbilityTypes` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `ManaGain`

### `StatusOnTurnEndIfManaExact` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Logic Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `FreeSpell`, `MoveQuivered`, `Quivered`, `SpellDamageUp`

### `StatusOnTurnEndIfManaOrHealthExact` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (7):** `DivineShield`, `HealthGain`, `IntelligenceUp`, `KineticSpikes`, `Shield`, `SpellDamageUp`, `Temporary`

### `StatusOnUseAbilityWithTag` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (5):** `Conditional_FirstApplicationThisTurn`, `DamageUp`, `HealthGain`, `RandomStatUp`, `RefreshActPoints`

### `StatusOnUseBasicAttack` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `FlippedFacingForceAttack`

### `StatusOnUseElementAbility` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `SpeedUp`

### `StatusPerInjury` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (2):** `{Event Keys}`, `{Status and Passive Keys}`

**In Master but NOT in split file (3):** `Shield`, `StrengthUp`, `injury`

### `StatusWhenAllySpendsMana` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (2):** `ManaGain`, `OneUseSpellDamageUp`

### `TaggedPickupEffectReplacement` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `HealthGain`

### `TakeBonusTurnWithStatus` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Madness`

### `TheHunger` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Madness`

### `effects` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (17):** `Bleed`, `Bruise`, `Burn`, `Charmed`, `Fear`, `Freeze`, `Immobile`, `Leeches`, `Madness`, `Marked`, `Petrify`, `Poison`, `Slow`, `SpreadDisease`, `Stun`, `VisualFXTile`, `Weakness`

### `fire` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `ice` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `keyword_tooltips` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (1):** `Weakness`

### `lightning` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `on_throw` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Logic Keys}`

**In Master but NOT in split file (1):** `HitExplosion`

### `passives` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (424):** `AbilityOnBattleStart`, `AbilityReaction`, `AbilityWhenTaggedCharacterMovesNear`, `AbsorbManaAura`, `AddAllyNeighborsToAttackRange`, `AddBonusMeleeRange`, `AddBonusRange`, `AddCorpseHealth`, `AddCritMultiplier`, `AddDamageToBasicAttack`, `AddDamageToElementDamage`, `AddElementsToBasicAttack`, `AddHiddenTag`, `AddInitiative`, `AddKnockbackDamage`, `AddLevelUpRerolls`, `AddLevelUpStatMultiplier`, `AddManaRegen`, `AddMovement`, `AddPassiveToSpawnedRocks`, `AddPassivesToCharmed`, `AddPassivesToMinions`, `AddPassivesToSummonAbilityMinions`, `AddSelfStatusToBasicAttack`, `AddSelfStatusToWeapons`, `AddSpellDamage`, `AddStartingMana`, `AddStatusToAllDamage`, `AddStatusToBasicAttack`, `AddStatusToBasicAttackWithCooldown`, `AddStatusToBasicMeleeAttack`, `AddStatusToElementAbilities`, `AddStatusToElementDamage`, `AddStatusToExplosions`, `AddStatusToFirstBasicAttack`, `AddStatusToMeleeDamage`, `AddStatusToReceivedDamage_ExcludeStatuses`, `AddStatusToTrampleDamage`, `AddStatusToWeapons`, `AddStatusesIfPersistentWeatherElement`, `AddStatusesToReceivedElementalDamage`, `AddTag`, `AddTemporaryEffectsToBasicAttack`, `AddUnfilledMaxHealth`, `AddWeaponScaling`, `AfterImage`, `AllStatsUp`, `AllowPassTurn`, `AllyBonusAbilityAura`, `AllyDamageReaction`, `AllyDamageReduction`, `AllyHealthRegenAura`, `AllyManaRegenAura`, `AllyMoveAbilityAura`, `AllyMultiplyKnockbackDamage`, `AlphaTurns`, `AlternateCraftingPools`, `AmplifyKnockback`, `AmplifyPositiveStatus`, `AmplifyStatus`, `ApplyStatusesToRandomEnemiesEachTurn`, `Autism`, `AutoCritLowDamage`, `AutoEquipConsumables`, `AutocastEachRound`, `AutocastEachTurn`, `AutocastEachTurnBegin`, `BackstabCritChance`, `BackstabWeakness`, `BasicAttackAOEBonus`, `BasicAttackCritChance`, `BasicAttackDamageMultiplier`, `BasicAttackStatusCarefulness`, `BlacklistPickupType`, `BlastResistance`, `Bleed`, `BleedThorns`, `BonusAbility`, `BonusFoodEachBattle`, `BoobyTrapItems`, `BoostAllyStatsOnDeath`, `BoostDamageAura`, `BoostHeals`, `BoostRangeAura`, `BoostWeaponDamage`, `BouncyProjectiles`, `Brace`, `BraceForEachNeighboringEnemy`, `Bruise`, `BuffImmunity`, `Burn`, `CCImmunity`, `CanRemoveCursedItems`, `CantDodge`, `CapDamageFromAllies`, `CapMovementAbilityRange`, `CatAPultAnimation`, `CatchProjectiles`, `ChainKnockback`, `ChanceToBackflip`, `ChanceToBlockAndCounter`, `ChanceToRevive`, `ChangeTauntPriority`, `CharmAllFlies`, `ClassManaCostReduction`, `CobraReflex`, `CoinsAddDamage`, `CollectPickupsOnBattleEnd`, `Conductor`, `ConfusionEffectOnTaggedAbilities`, `ConjureCastSpellsForAllies`, `ConsumableEffectsMultiplierBonus`, `ConsumablesInfiniteRange`, `ConsumablesMeleeRange`, `CounterAttack`, `CritChanceUp`, `CritsApplyStatus`, `DamageEnemiesOnHeal`, `DamageEnemiesOnKill`, `DamageIfDidntUseSpecificAbility`, `DamageNeighborTilesWhenCastSpell`, `DamageNeighborsAfterMove`, `DamageNeighborsOnEndMove`, `DamageReductionAura`, `DamageUp`, `DeathChill`, `DeathRattle`, `DebuffImmunity`, `DejaVu`, `DepressionAura`, `Diabetes`, `DirtyClaws`, `DisableAbilities`, `DisableAbilitiesWithTag`, `DodgeChance`, `Doomed`, `DoubleCastWeapons`, `DukeOfFlies`, `Dyslexia`, `EMP`, `ElementImmune`, `ElementalAttunement`, `ElementalManaCostReduction`, `Empath`, `EnemiesGetPickupsKnockedOut`, `EnergyStorm`, `EquipTemporaryItem`, `EquipmentPassiveMultiplierBonus`, `EquipmentSetBonusBonus`, `EscapeSequence`, `Eternal`, `ExhaustionRoundChange`, `ExplodeOverkilledEnemies`, `ExtraBasicAttacks`, `ExtraBasicMoves_Status`, `ExtraInjuryOnDeath`, `ExtraMovePoints`, `ExtraStatusWhenDealingDamage`, `ExtraWeaponAttacks`, `FaceArmorPassiveMultiplierBonus`, `FaceShield`, `FamiliarSecondaryDamageImmunity`, `FlowerPowerAuraBrace`, `FlowerPowerAuraStrength`, `FlowersOnEndTurn`, `FlyDamageIncrease`, `Flying`, `FollowUp`, `ForceSpecificInjury`, `ForceUseAbility`, `FreePathfindElement`, `FreeSpellsAtFullMana`, `FreezePiercing`, `FrontstabBasicAttackCritChance`, `FullHeal`, `FullHealthCritChance`, `FullPower`, `FurnitureStats`, `GainExtraShield`, `GravityWell`, `HPGainBlock`, `HeadArmorPassiveMultiplierBonus`, `HealDamagesEnemies`, `HealsAlsoRegenMana`, `HealsCanRevive`, `HealthRegenUp`, `HolyShieldTransferToTaggedMinions`, `HouseFoodRequirementMultiplier`, `Hypomania`, `IgnoreTiles`, `ImmortalLeeches`, `IncreaseExplosionDamage`, `IncreaseExplosionSize`, `IncreaseHealingSpellRange`, `IncreaseSpellRange`, `InfiniteRebirth`, `InnateElement`, `InvertBrainFaction`, `KillsHeal`, `KillsToMeat`, `KnockbackImmunity`, `LateBloomer`, `LevelUpClassOverride`, `LightningAspectCharge`, `LightningRod`, `LimitDamage`, `LimitHeal`, `LimitSelfKnockbackDamage`, `LimitedTileTrail`, `LineOfSightTrueSightAura`, `LobbedHook`, `LowHealthAllyDodgeChanceAura`, `Madness`, `MakeBasicAttackPassThroughThings`, `MakeSpellsRequireCharge`, `ManaCostReductionTagged`, `ManaRegenMultiplierIfManaEmpty`, `MaxAccuracy`, `MaxStartingMana`, `MegaMinions`, `MeleeRevengeDamage`, `Metal`, `MetalDetector`, `MinimumTech`, `MissChance`, `MoveAndUseAbilityEachTurnBeginIfPossible`, `MoveAwayFromDamageSource`, `MoveQuivered`, `MoveSpeedMultiplier`, `MoveTowardsDamageSource`, `MoveWhenDamaged`, `MovementReaction`, `MulticlassLevelUp`, `NeckArmorPassiveMultiplierBonus`, `NoManaRegen`, `NoReflection`, `NubbyTossPriority`, `NumbingLeeches`, `OverhealGainsBothShield`, `OverrideBasicAttack`, `OverrideMaxHealth`, `OverrideMaxMana`, `OverridePalette`, `Paranoia`, `ParasitesArentCursed`, `PassiveAfterXKills`, `PassiveAtFullHealth`, `PassiveAtHealthThreshold`, `PassiveAtInjuryThreshold`, `PassiveAtStatThreshold`, `PassiveIfAllArmorEmpty`, `PassiveIfEmptyFace`, `PassiveIfEmptyHead`, `PassiveIfEmptyNeck`, `PassiveLevelScaledStatus`, `PassiveLevelUpAtCombatEnd`, `PassiveUntilCastSpell`, `PassiveUntilGetKill`, `PassiveWhenAffectedByElement`, `PassiveWhenAtFullMana`, `PassiveWhenTheAlpha`, `PassiveWhileInMonkMeleeStance`, `PassiveWhileInMonkRangedStance`, `PassiveWhilePreviewingMonkRangedStance`, `PassiveWhileWearingMetal`, `PermanentImmobile`, `PermanentItems`, `PermanentKitten`, `PermanentMadness`, `Poison`, `PoisonThorns`, `PoopWhenHit`, `ProtectTargetedAllies`, `Quiver`, `Quivered`, `RandomPassivePool`, `RangedTrueShot`, `RealTimePressure_OneUnit`, `ReceivedStatusReplacement`, `RemoveLineOfSightRestrictions`, `RemoveOncePerFightRestriction`, `ReplaceBasicAttack`, `ReplaceBasicAttackWhenCastable`, `ReplaceBasicAttackWhenDead`, `ReplaceBasicMove`, `ReplaceSpawnedObjects`, `RevengeDamage`, `ReviveOnWin`, `RobotsInheritArmor`, `RockDetector`, `ScaledStatusOnBleedDamage`, `ScaledStatusOnOverMana`, `ScaledStatusOnSpendMana`, `SchrodingerDisorder`, `Scleroderma`, `SecurityBotProtect`, `SelfDamageWhenDealDamage`, `SetDefaultFacePassive`, `SetSpellCosts`, `ShareHealthRegen`, `SharePickups`, `ShoulderCheck`, `ShovingMatch`, `ShowHiddenThings`, `SizeScale`, `Slow`, `SmallEnemiesIgnoreYou`, `SmallRockBehavior`, `SmiteEnemiesWhoKill`, `SpawnCatCopyOnBattleStart`, `SpawnCreepOnHit`, `SpawnEachTurn`, `SpawnObjectOnPopCorpse`, `SpawnOnBattleStart`, `SpawnOnBattleStartRandomEmptyTile`, `SpawnThingOnDamage`, `SpawnThingOnDeath`, `SpecialFriends`, `SpeedUp`, `SplittableMove`, `SpreadExtraDebuffs`, `SpreadPainBonus`, `StatMinimum`, `StatsAtLowHealth`, `StatusAdjacentOnTheirTurnBegin`, `StatusAfterCastSpell`, `StatusAlliesOnBattleStart`, `StatusAlliesOnDeath`, `StatusAlliesOnGainCoins`, `StatusAlliesOnKill`, `StatusAllyWhenAllySpendsMana`, `StatusAnyCatAllyWhoKills`, `StatusDamagers`, `StatusEachTurnBegin`, `StatusEachTurnEnd`, `StatusEachTurnEndForEachTurn`, `StatusEachTurnEndPerEnemyKill`, `StatusEnemiesOnDeath`, `StatusEveryXSpellCasts`, `StatusEveryXTurnBegins`, `StatusIfBattleAlreadyBegan`, `StatusIfUnusedMovePoints`, `StatusImmunity`, `StatusKilledCharacters`, `StatusKillers`, `StatusOnAllyCatDeath`, `StatusOnAnyDeath`, `StatusOnBattleEnd`, `StatusOnBattleEndIfKillThresholdMet`, `StatusOnBattleStart`, `StatusOnBreakItem`, `StatusOnCastSpell`, `StatusOnCollectPickup`, `StatusOnCrit`, `StatusOnDealtDamage`, `StatusOnDealtDamageThreshold`, `StatusOnEatFood`, `StatusOnEatPill`, `StatusOnEndMove`, `StatusOnGainCoins`, `StatusOnGainShield`, `StatusOnHeal`, `StatusOnHealed`, `StatusOnKill`, `StatusOnKillEnemy`, `StatusOnLoseShield`, `StatusOnOverHealed`, `StatusOnOverMana`, `StatusOnPickupCoins`, `StatusOnPopCorpse`, `StatusOnStanceSwitch`, `StatusOnTakeHealthDamage`, `StatusOnTookDamage`, `StatusOnTookDamageFromAbility`, `StatusOnTookDamageFromEnemyAbility`, `StatusOnTriggerTrap`, `StatusOnTurnEndIfCastNSpells`, `StatusOnTurnEndIfDidntCastAbilityTypes`, `StatusOnTurnEndIfManaExact`, `StatusOnTurnEndIfManaOrHealthExact`, `StatusOnUseAbilityWithTag`, `StatusOnUseBasicAttack`, `StatusOnUseElementAbility`, `StatusPerInjury`, `StatusReplacement`, `StatusThingsKnockedBack`, `StatusWhenAllySpendsMana`, `Stealth`, `StrengthForEachNeighboringEnemy`, `StrengthInNumbersAura`, `StrengthUp`, `StrictLimitDamage`, `Study`, `TaggedPickupEffectReplacement`, `TauntAlways`, `TauntAtFullHealth`, `Tech`, `TempInitiativeChange`, `TheHunger`, `Thorns`, `TileDamageMultiplier`, `TileTrail`, `TourettesMeows`, `TowerDefense`, `TowerDefenseReflex`, `Trample`, `TrapEffectsMultiplier`, `TrinketActiveEffectsMultiplierBonus`, `TrinketPassiveMultiplierBonus`, `Triskaidekaphobia`, `UncappedHP`, `UncappedMana`, `UpgradeLevelUpClassActives`, `UpgradeLevelUpClassPassives`, `UpgradeSpawnedPickups`, `Vegan`, `Vengeful`, `WaterWalk`, `Weakness`, `WeaponActiveEffectsMultiplierBonus`, `WeaponCountsAsBasicAttack`, `WeaponDamageMultiplierBonus`, `WeaponPassiveMultiplierBonus`, `WobblyCat`

### `spell_graphics_override` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (4):** `area_particle`, `center_particle`, `palette`, `particle`

### `statuses` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Status and Passive Keys}`

**In Master but NOT in split file (4):** `AllStatsUp`, `FindItemFromPool`, `HealthGain`, `PermanentDexterity`

### `triattack` (from `Passives_and_Statuses.md`)

**In split file but NOT in Master (1):** `{Damaging Keys}`

**In Master but NOT in split file (1):** `effects`

### `ROOT` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (117):** `beanies_quests_intro`, `beanies_quests_repeat`, `beat_chapter_boss`, `beat_house_boss`, `complete_act_difficulty`, `complete_adventure`, `complete_chapter`, `complete_chapter_with_class`, `complete_chapters`, `complete_checklist_with_class`, `destinations`, `fail_adventure`, `fail_item_quest`, `finish_quest`, `frank_max_intro`, `frank_max_repeating`, `fully_complete_difficulty`, `house_upgrade_4throom`, `house_upgrade_attic`, `house_upgrade_largehouse`, `house_upgrade_mediumhouse`, `increment_savefile_counter`, `intro`, `jack_max_intro`, `jack_max_repeating`, `jack_shopupgrade1`, `jack_shopupgrade2`, `jack_shopupgrade3`, `jack_shopupgrade4`, `main_pool`, `organ_max_intro`, `organ_max_repeating`, `organ_unlock`, `organ_upgrade1`, `organ_upgrade2`, `organ_upgrade3`, `organ_upgrade4`, `organ_upgrade5`, `organ_upgrade6`, `popup`, `post_combat_cutscene`, `preempt_npc_sequence`, `prereqs`, `queue_cutscene_immediate`, `repeat`, `repeatable`, `require_beat_house_boss`, `require_mapgen_flag`, `required_difficulty`, `requires_hard_path`, `requires_monoclass_run`, `requires_unlocked_npc`, `reset_npc_sequence`, `reset_unlock`, `set_mapgen_flag`, `set_savefile_flag`, `steven_milliontrashed`, `surviving_kaiju`, `tink_aggression`, `tink_basestats`, `tink_inbreeding`, `tink_max_intro`, `tink_max_repeating`, `tink_prettybow`, `tink_relationships`, `tink_sexuality`, `tink_tags`, `tracy_blankcollar1`, `tracy_blankcollar2`, `tracy_blankcollar3`, `tracy_foodstorage1`, `tracy_foodstorage10`, `tracy_foodstorage2`, `tracy_foodstorage3`, `tracy_foodstorage4`, `tracy_foodstorage5`, `tracy_foodstorage6`, `tracy_foodstorage7`, `tracy_foodstorage8`, `tracy_foodstorage9`, `tracy_idol1`, `tracy_idol2`, `tracy_idol3`, `tracy_idol4`, `tracy_idol5`, `tracy_idol6`, `tracy_idol7`, `tracy_max_intro`, `tracy_max_repeating`, `trigger_house_boss`, `trigger_npc_sequence`, `trigger_npc_sequence_tomorrow`, `unlock_ability`, `unlock_act_difficulty`, `unlock_boss`, `unlock_item`, `unlock_item_immediate`, `unlock_levelgroup`, `unlock_npc_tomorrow`, `unlock_passive`, `unlock_quest_item`, `unlock_song`, `upgrade_storage_1`, `upgrade_storage_2`, `upgrade_storage_3`, `upgrade_storage_4`, `upgrade_storage_5`, `upgrade_storage_6`, `upgrade_storage_7`, `upgrade_storage_repeating_crazy`, `upgrade_storage_repeating_hard`, `upgrade_storage_repeating_impossible`, `upgrade_storage_repeating_intro`, `upgrade_storage_repeating_normal`, `visit_chapter`, `{Event Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `beanies_quests_intro` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `generate_beanies_quest`, `reward_text`

**In Master but NOT in split file (5):** `dialog`, `do_sidequest_sequence`, `gather_questitem_info`, `get`, `set_state`

### `beanies_quests_repeat` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `generate_beanies_quest`, `level_display`, `repeat`, `reward_text`

**In Master but NOT in split file (5):** `dialog`, `do_sidequest_sequence`, `gather_questitem_info`, `get`, `set_state`

### `frank_max_intro` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (4):** `favor`, `gift_item_from_pool`, `level_display`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `frank_max_repeating` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `gift_item_from_pool`, `level_display`, `repeat`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `house_upgrade_4throom` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `house_upgrade_attic` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `house_upgrade_largehouse` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `house_upgrade_mediumhouse` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `house_upgrade`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `jack_max_intro` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (4):** `favor`, `level_display`, `rep_reward_count`, `reward_text`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `jack_max_repeating` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `jack_shopupgrade1` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `jack_shopupgrade2` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `jack_shopupgrade3` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `jack_shopupgrade4` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_max_intro` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (4):** `favor`, `gift_item`, `level_display`, `reward_text`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_max_repeating` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `gift_item`, `level_display`, `repeat`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `organ_unlock` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_upgrade1` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_upgrade2` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_upgrade3` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_upgrade4` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_upgrade5` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `organ_upgrade6` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `shop_level_up`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `popup` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `prompt`

### `steven_milliontrashed` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `level_display`, `repeat`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_aggression` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_basestats` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_inbreeding` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_max_intro` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (4):** `coins`, `favor`, `level_display`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_max_repeating` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `coins`, `favor`, `level_display`, `repeat`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `tink_prettybow` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `gift_item`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_relationships` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_sexuality` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tink_tags` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (3):** `favor`, `reward_text`, `set_savefile_flag`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `tracy_blankcollar1` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_blankcollar2` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_blankcollar3` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage1` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage10` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage2` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage3` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage4` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage5` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage6` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage7` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage8` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_foodstorage9` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_idol1` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_idol2` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_idol3` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_idol4` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_idol5` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_idol6` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_idol7` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_age`, `reward_text`, `shop_level_up`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_max_intro` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `level_display`, `required_age`, `reward_text`, `tracy_special_item`

**In Master but NOT in split file (5):** `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls`

### `tracy_max_repeating` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (6):** `favor`, `level_display`, `repeat`, `required_age`, `reward_text`, `tracy_special_item`

**In Master but NOT in split file (1):** `do_random_sequence`

### `upgrade_storage_1` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_2` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_3` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_4` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_5` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_6` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_7` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (5):** `favor`, `required_act`, `required_chapter`, `reward_text`, `storage_expansion`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_repeating_crazy` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `upgrade_storage_repeating_hard` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `upgrade_storage_repeating_impossible` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `upgrade_storage_repeating_intro` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (7):** `favor`, `level_display`, `rep_reward_count`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

**In Master but NOT in split file (3):** `dialog`, `get`, `set_state`

### `upgrade_storage_repeating_normal` (from `Progression_Unlocks.md`)

**In split file but NOT in Master (8):** `favor`, `level_display`, `rep_reward_count`, `repeat`, `required_act`, `required_chapter`, `required_difficulty`, `reward_text`

**In Master but NOT in split file (1):** `do_random_sequence`

### `Food` (from `Shops.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `weight`

### `Item` (from `Shops.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (1):** `weight`

### `item_rarity_costs` (from `Shops.md`)

**In split file but NOT in Master (1):** `{Event Keys}`

**In Master but NOT in split file (2):** `common`, `rare`

### `meta` (from `Shops.md`)

**In split file but NOT in Master (1):** `{Graphics Keys}`

**In Master but NOT in split file (1):** `movieclip`

### `ROOT` (from `Spawns_and_Enemy_Pools.md`)

**In split file but NOT in Master (14):** `early_spawn`, `editor`, `forced_placement`, `image`, `object`, `orientation`, `reserved`, `tag_location`, `trap`, `utility`, `value`, `weather_element_alt`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

### `ROOT` (from `Status_Effect_Keywords.md`)

**In split file but NOT in Master (14):** `alias`, `icon_frame`, `name_reference_applier`, `name_stacks_neg`, `tooltip_reference_applier`, `tooltip_stackless`, `tooltip_stackless_neg`, `tooltip_stackless_pos`, `tooltip_stacks`, `tooltip_stacks_neg`, `tooltip_stacks_pos`, `tooltip_stacks_singular`, `{Graphics Keys}`, `{Logic Keys}`

**In Master but NOT in split file (9):** `breakdown`, `breakdown2`, `breakdown3`, `breakdown4`, `button_nav`, `item_groups`, `item_rarity_costs`, `meta`, `stock_fill_order`

