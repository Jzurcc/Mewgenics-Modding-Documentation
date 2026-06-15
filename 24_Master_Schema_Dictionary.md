# Mewgenics Mod Developer Documentation: Master Schema Dictionary

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Abilities & Spells

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai_ability` | Enum/String | `SpawnBomb_AI, Magnetize_AI, NubsJump_AI` |
| `bonk_damage` | Block | `{ ... }` |
| `bonus_passives` | Block | `{ ... }` |
| `chain_ability` | Enum/String | `ControlPlantsPartTwo2, ControlPlantsPartTwo, Dump` |
| `class` | Enum/String | `SuplexAbility, PlaceholderMeleeAttackAbility, MultiHitMeleeAttackAbility` |
| `cloned_ability` | Enum/String | `attack` |
| `cost` | Block | `{ ... }` |
| `damage_instance` | Block | `{ ... }` |
| `damage` | Block | `{ ... }` |
| `effects` | Block | `{ ... }` |
| `empty_self_damage` | Block | `{ ... }` |
| `graphics` | Block | `{ ... }` |
| `keyword_tooltips` | Block | `{ ... }` |
| `meta` | Block | `{ ... }` |
| `self_damage` | Block | `{ ... }` |
| `sounds` | Block | `{ ... }` |
| `spawn` | Block | `{ ... }` |
| `splash_damage` | Block | `{ ... }` |
| `sub_ability` | Enum/String | `Spin, TeamFlex_Impl, Huddle_Impl` |
| `tags` | Array | `[ musical ], [ weapon_throw ], [ summon ]` |
| `target` | Block | `{ ... }` |
| `template` | Enum/String | `melee_attack, spell, targeted_status` |
| `temporary_effects` | Block | `{ ... }` |
| `variant_of` | Enum/String | `BasicMelee, Asteroid, BasicJump` |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `Bruise` | Number | `2` |

### Context: `AfterImage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `PlayerCat_ThiefShade` |
| `skilltemp` | Boolean | `true` |

### Context: `AlphaStatusOnTurnBegin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | `1` |

### Context: `ApplyMultipleTimes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomStatusFromPool` | Block | `{ ... }` |
| `stacks` | Number | `8, 4, X` |

### Context: `ApplyPassives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddTag` | Enum/String | `plant, squirrel` |
| `ElementImmune` | Enum/String | `Creep` |
| `Flying` | Number | `1` |
| `IgnoreTiles` | Number | `1` |
| `KnockbackImmunity` | Number | `1` |
| `Plant` | Number | `1` |
| `ReplaceBasicAttack` | Enum/String | `BasicPuke` |
| `StatusOnBattleEnd` | Block | `{ ... }` |
| `YOffset` | Enum/String | `.25` |

### Context: `ApplyPassivesToSpawnerWhileAlive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HideEquipment` | Enum/String | `neck` |

### Context: `ApplyStatusIfCrit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `Bleed` | Number | `1, 5` |
| `LuckUp` | Number | `-1` |

### Context: `ApplyStatusesNextTurnBegin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Quivered` | Number | `1` |

### Context: `ApplyToConsumed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DeleteObject` | Number | `1` |
| `Die` | Number | `1` |

### Context: `ApplyToOthersWithSharedTagAndFaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Marked` | Number | `1` |

### Context: `ApplyToRandomClosestAlly`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceMoveTowards` | Number | `1` |

### Context: `ApplyToRandomPartyMemberIfPossible`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `GainDisorderFromPool_PostCast` | Enum/String | `forbidden_spell_consequences_crippling, forbidden_spell_consequences` |

### Context: `ApplyToSource`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddLeechesStatus` | Number | `1` |
| `AddWeaponAux` | String | `"-max(min(X+1, item_aux), 0)", 1, -item_aux` |
| `AllStatsUp` | Number | `1` |
| `Brace` | Number | `1` |
| `Bruise` | Number | `1` |
| `Cleanse` | Number | `0` |
| `ConstitutionUp` | Number | `1, 2` |
| `Craft` | Block | `{ ... }` |
| `DisableWeapon` | Number | `1` |
| `DivineShield` | Number | `2` |
| `DoDamage` | Block | `{ ... }` |
| `EquipPermanentItem` | Enum/String | `Kidney, BoneClub` |
| `EvolveAbilityFromPool` | Enum/String | `Butcher, Medic, Thief` |
| `FindItemFromPool` | Block | `{ ... }` |
| `FindItem` | Enum/String | `Molars` |
| `ForceUseAbility` | Enum/String | `Ram_chained` |
| `FormChange` | Enum/String | `Default, HasCat, { ... }` |
| `FreeSpell` | Number | `1, 2` |
| `FullHeal` | Number | `1` |
| `GainCoinsRange` | Block | `{ ... }` |
| `HealthGain` | Number | `1, 8, 4` |
| `KineticSpikes` | Number | `1` |
| `KnockUpAndAway` | Block | `{ ... }` |
| `LuckUp` | Number | `1` |
| `ManaGain` | Number | `2` |
| `MoveQuivered` | Number | `1` |
| `RefreshActPoints` | Number | `1` |
| `RefreshMovePoints` | Number | `1` |
| `RemoveStatus` | Enum/String | `DodgeChance_Status, SpeedUp_WithoutInitiative` |
| `Shield` | Number | `1, 2, 5` |
| `SpecificInjury` | Enum/String | `str` |
| `StanceSwitchToMelee` | Number | `1` |
| `StanceSwitchToRanged` | Number | `1` |
| `StrengthUp` | Number | `1, 3` |
| `TakeExtraTurn` | Number | `1` |
| `Tech` | Number | `1` |
| `TempTrampleUntilSettled` | Number | `3` |

### Context: `ApplyToSourceOnKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `AlphaCat` | Number | `1` |
| `CompleteItemQuest` | Enum/String | `BlackShard` |
| `EvolveAbilityFromPool` | Enum/String | `Hunter` |
| `HealthGain` | Number | `5, 10` |
| `ManaGain` | Number | `5` |
| `RefreshActPoints` | Number | `1` |
| `RemoveItem` | Enum/String | `BlackShard, BlackShard_Glowing` |
| `Revive` | Number | `100%, 50%` |
| `StrengthUp` | Number | `2` |
| `TakeExtraTurn` | Number | `1` |
| `TransformWeapon` | Block | `{ ... }` |
| `WeaponAuxMultiplier` | Enum/String | `.5` |

### Context: `ApplyToTile`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ObjectOnHit` | Enum/String | `Bait` |
| `SpawnBearTrap` | Number | `1` |

### Context: `ArcLightning`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.5` |
| `enemies_only` | Boolean | `false, true` |
| `ignore_self` | Boolean | `true` |
| `max_distance` | Number | `1, 2, 3` |
| `stacks` | Number | `100` |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `Transcend2, SharpenNail2` |
| `even_if_stunned` | Boolean | `true` |

### Context: `BackflipWhenTargeted`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `DestroyerDodge, SZBBackflipDodge, Teleport` |
| `stacks` | Number | `1, 4` |

### Context: `BodyGuard`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `BodyGuardSwap2, BodyGuardSwap` |
| `stacks` | Number | `1` |

### Context: `BounceObject`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.25, .5` |
| `obj` | Enum/String | `SmallLavaRock, chapter_corpse_medium` |
| `slide` | Number | `10` |

### Context: `CanApplyToInanimate`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `BreakIntoRocks` | Enum/String | `Coin, SmallRock` |
| `GetAggroTarget` | Number | `1` |
| `ObjectOnHitCharacter` | Enum/String | `CharmedLeech, AllyRotFly, Fly` |
| `PreventDeathTransforms` | Number | `1` |
| `Temporary` | Block | `{ ... }` |
| `Vaporize` | Number | `1` |

### Context: `CatPartsSizeScaleStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `arm1` | Number | `1.1` |
| `arm2` | Number | `1.1` |
| `body` | Number | `1.1` |
| `mouth` | Number | `1.1` |

### Context: `CatPartsTransform`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `arm1` | Number | `1501, 1013, 338` |
| `arm2` | Number | `1501, 1013, 324` |
| `body` | Number | `1029, 31` |
| `ear1` | Number | `1501, 325, 23` |
| `ear2` | Number | `1501, 23, 1036` |
| `eye1` | Number | `1069` |
| `eye2` | Number | `1069` |
| `eyebrow1` | Number | `1069` |
| `eyebrow2` | Number | `1070` |
| `head` | Number | `12, 1504` |
| `leg1` | Number | `1501, 41, 338` |
| `leg2` | Number | `1501, 41, 338` |
| `mouth` | Number | `1501, 1005, 1071` |
| `palette` | Number | `86` |
| `tail` | Number | `1503, 4, 1502` |
| `texture` | Number | `1008, 322` |

### Context: `ChanceToBreakFree`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `XXX, LennyDrop, CHuskDrop` |
| `fail_ability` | Enum/String | `XXX, LennyStruggleFail, CHuskDropFail` |
| `stacks` | Number | `25` |

### Context: `ChangeTile`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `aoe` | Number | `1` |
| `chance` | Enum/String | `.25, 25%` |
| `tile` | Enum/String | `GlassTile, ToxicTile, [ TallGrassTile TallFlowerTile BrambleTile ]` |

### Context: `Cleave`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.25` |

### Context: `CollectsPickupsWithAltEffects`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CurrentWeaponAddPoison` | Number | `1` |
| `LuckUp` | Number | `2` |
| `Quivered` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `Shield` | Number | `1` |
| `Tech` | Number | `1` |

### Context: `Conditional_ActiveWeather_Any`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` |
| `weather` | Array | `[ FlySwarm FireflySwarm ButterflySwarm ]` |

### Context: `Conditional_AffectedByElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` |
| `Burn` | Number | `2` |
| `Conditional_Speculative` | Block | `{ ... }` |
| `element` | Enum/String | `Water, Fire` |

### Context: `Conditional_Ally`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `ApplyToSourceOnKill` | Block | `{ ... }` |
| `ApplyToSource` | Block | `{ ... }` |
| `BleedThorns` | Number | `3` |
| `ChanceToBreak` | Number | `5%` |
| `Charmed` | Number | `1` |
| `Cleanse` | Number | `0` |
| `Conditional_Corpse` | Block | `{ ... }` |
| `Conditional_PlayerCat` | Block | `{ ... }` |
| `DamageUp` | Number | `1, 2` |
| `FullHeal` | Number | `1` |
| `HealthGain` | Number | `4` |
| `KnockbackDamageImmuneUntilSettled` | Number | `1` |
| `OverrideDamage` | Number | `-10, 0` |
| `RandomStatUp` | String | `"ceil(X/2)", "ceil(X/3)"` |
| `RepairAll` | Number | `1` |
| `ShowText` | String | `"COMBAT_POPUP_REPAIRED"` |
| `TempDamageUp` | Number | `1` |
| `Temporary` | Block | `{ ... }` |
| `ThornsDamageImmuneUntilSettled` | Number | `1` |
| `Thorns` | Number | `1` |
| `TileDamageImmuneUntilSettled` | Number | `1` |

### Context: `Conditional_Backstab`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` |
| `Fear` | Number | `1` |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DieViolently` | Number | `1` |
| `Instakill` | Number | `25` |
| `odds` | Enum/String | `.16666666` |

### Context: `Conditional_Boss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusDamage` | Number | `25` |
| `Charmed` | Number | `1` |
| `Conditional_HasStatus` | Block | `{ ... }` |
| `Drowsy` | Number | `1` |
| `Else` | Block | `{ ... }` |
| `ExplodeCharacter_NoDie` | Number | `5` |
| `ExplodeCharacter_PartyBoss` | Number | `5` |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | `5, 9` |
| `Fear` | Number | `1` |
| `OverrideDamage` | Number | `25, 10` |
| `RemoveStatus` | Enum/String | `Petrify` |
| `Stun` | Number | `1` |
| `VisualFX` | Enum/String | `Explosion, PartyExplosion` |
| `XIsTargetHealth` | Block | `{ ... }` |

### Context: `Conditional_BossOrBig`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Immobile` | Array | `[ 1 .25 ]` |

### Context: `Conditional_Buddy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_InForm` | Block | `{ ... }` |
| `Consumed` | Block | `{ ... }` |
| `Else` | Block | `{ ... }` |

### Context: `Conditional_CanBeHealed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomStatusFromPool` | Block | `{ ... }` |

### Context: `Conditional_Corpse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Conditional_Enemy` | Block | `{ ... }` |
| `FlatAIBonus` | Number | `100` |
| `HealRandomInjury` | Number | `1` |
| `PermanentCharm` | Number | `1` |
| `Revive` | Number | `100%, 50%` |

### Context: `Conditional_DebuffRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` |
| `odds` | Number | `15%` |

### Context: `Conditional_DestructibleCorpse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToTile` | Block | `{ ... }` |
| `VaporizeCorpse` | Number | `1` |

### Context: `Conditional_Displaceable`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `LaunchOffScreenInstakill` | Number | `1` |
| `LaunchOffScreen` | Enum/String | `10+bonus_melee_ability_damage` |
| `TempInitiativeChange` | Number | `-100` |

### Context: `Conditional_Enemy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, -1` |
| `ApplyToSourceOnKill` | Block | `{ ... }` |
| `ApplyToSource` | Block | `{ ... }` |
| `Attraction` | Number | `1` |
| `BonusDamage` | Number | `1` |
| `Burn` | Number | `3` |
| `Charmed` | Number | `1` |
| `Conditional_FinishedSpawning` | Block | `{ ... }` |
| `Conditional_NotBoss` | Block | `{ ... }` |
| `Confusion` | Number | `1, [ 1 .2 ], 3` |
| `DisplaceToAbilityTarget` | Number | `1` |
| `Doomed` | Number | `1` |
| `Fear` | Number | `1` |
| `ForceMoveTowards` | Number | `1` |
| `Hex` | Number | `1` |
| `Madness` | Number | `1` |
| `Marked` | Number | `1` |
| `PermanentCharm` | Number | `1` |
| `Poison` | Number | `1` |
| `Stun` | Array | `[ 1, .25 ]` |
| `TakeExtraTurn` | Number | `1` |
| `TempDamageUp` | Number | `-1` |
| `Temporary` | Block | `{ ... }` |
| `Weakness` | Number | `1, 2` |

### Context: `Conditional_Familiar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `BonusDamage` | Number | `-2` |
| `DamageUp` | Number | `2, 3` |
| `DivineShield` | Number | `1` |

### Context: `Conditional_FinishedSpawning`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Imprison` | Enum/String | `Fly` |

### Context: `Conditional_FirstApplicationThisTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `TempPassiveWhileHasStatus` | Block | `{ ... }` |
| `key` | Enum/String | `TaintedOffering, TaintedOffering2, EtherSoakedRag` |

### Context: `Conditional_FormulaIsPositive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Enum/String | `X+1, X` |
| `Freeze` | Number | `1` |
| `Immobile` | Number | `1` |
| `OverrideKnockbackDamage` | Enum/String | `X*10` |
| `Shield` | Number | `6, 5` |
| `Slow` | Enum/String | `X` |
| `SpeedUp` | Number | `-1` |
| `Stun` | Number | `1` |
| `formula` | Enum/String | `X+1, X-1, X` |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToRandomPartyMemberIfPossible` | Block | `{ ... }` |
| `ApplyToSource` | Block | `{ ... }` |
| `GainDisorderFromPool_PostCast` | Enum/String | `forbidden_spell_consequences` |
| `GainDisorder` | Enum/String | `Chungus` |
| `ImmediateUseAbility` | Enum/String | `tk_ButterBean_Mega` |
| `RefreshWeaponAbility` | Number | `1` |
| `ShowText` | String | `"COMBAT_POPUP_RELOAD"` |
| `odds` | Number | `10%, 50%, 90%` |

### Context: `Conditional_HasCleansableDebuffs`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `GenericBuff` | Number | `5` |
| `PartialCleanse` | Number | `1` |
| `RandomStatusFromPool` | Block | `{ ... }` |

### Context: `Conditional_HasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `BonusDamage` | Number | `10, 20` |
| `Burn` | Number | `3` |
| `Confusion` | Number | `1` |
| `Fear` | Number | `1` |
| `FormChange` | Enum/String | `Bully` |
| `Quivered` | Number | `1` |
| `RemoveStatus` | Enum/String | `Petrify` |
| `Slow` | Number | `2` |
| `status` | Enum/String | `Undead, Freeze, Petrify` |

### Context: `Conditional_HasTag`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSourceOnKill` | Block | `{ ... }` |
| `ApplyToSource` | Block | `{ ... }` |
| `BonusDamage` | Number | `10` |
| `CanApplyToInanimate` | Block | `{ ... }` |
| `ChangeTilesUnder` | Enum/String | `LavaTile` |
| `Conditional_Boss` | Block | `{ ... }` |
| `Conditional_InForm` | Block | `{ ... }` |
| `Conditional_NotBoss` | Block | `{ ... }` |
| `CrackMoonHead` | Number | `1` |
| `DamageUp` | Number | `1` |
| `DeleteObject` | Number | `1` |
| `Die` | Number | `1` |
| `DisplaceTowardsSource` | Number | `1` |
| `Else` | Block | `{ ... }` |
| `EventBounty` | Number | `5` |
| `FaceAway` | Number | `1` |
| `FloatingRockTrap` | Number | `1` |
| `IgnoreDamage` | Number | `1` |
| `ImmediateUseAbility` | Enum/String | `HitlerCloneTransform, HitlerCloneHeil, MoonHandMegaSqueeze` |
| `Instakill` | Number | `25` |
| `MergeDamageInstance` | Block | `{ ... }` |
| `OverrideDamage` | Number | `1` |
| `PopAndSpawn` | Block | `{ ... }` |
| `RemoveStatus` | Enum/String | `Brace` |
| `ScatterRandomPickups` | Number | `5` |
| `SetAnimationAlts` | Block | `{ ... }` |
| `SetKnockback` | Number | `0` |
| `UseAbility` | Enum/String | `MoonHead_CommandHeadPunch` |
| `VaporizeCorpse` | Number | `1` |
| `Vaporize` | Number | `1` |
| `tag` | Enum/String | `poop, moonhead, food` |

### Context: `Conditional_HealthThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `BonusDamage` | Enum/String | `20+bonus_melee_damage` |
| `CaptureFamiliar` | Number | `1` |
| `DieViolently` | Number | `1` |
| `Die` | Number | `1` |
| `FactionConversion` | Number | `1` |
| `FlatLeech` | Number | `5` |
| `FullHeal` | Number | `1` |
| `Instakill` | Number | `999` |
| `SpawnThingIfHitKills` | Enum/String | `Food` |
| `Vaporize` | Number | `1` |
| `threshold_expr` | Enum/String | `item_aux` |
| `threshold_flat` | Number | `5, 10, 3` |
| `threshold_percent` | Number | `25%, 50%` |

### Context: `Conditional_InForm`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CritChanceUp` | Number | `20` |
| `DamageUp` | Number | `1` |
| `DodgeChance_Status` | Number | `20` |
| `ForceImmediateMoveAndAttack` | Block | `{ ... }` |
| `FormChange` | Enum/String | `Lifted, Big, Drunker` |
| `SpeedUp` | Number | `1` |
| `UseAbility` | Enum/String | `MoonHandPunchHead` |
| `form` | Enum/String | `Default, Small, Normal` |

### Context: `Conditional_IsSelf`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `OverrideDamage` | Number | `0` |

### Context: `Conditional_IsTrample`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `SetKnockback` | Number | `0` |

### Context: `Conditional_LastHit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusDamage` | Number | `3` |
| `Bruise` | Number | `1` |
| `DelayCastAbility` | Enum/String | `HitlerNuke` |
| `KnockUpAndAway` | Block | `{ ... }` |

### Context: `Conditional_LivingPlayerCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `Consumed` | Block | `{ ... }` |
| `TempPassiveWhileHasStatus` | Block | `{ ... }` |

### Context: `Conditional_NotAlly`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Confusion` | Number | `1` |
| `Temporary` | Block | `{ ... }` |

### Context: `Conditional_NotBig`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DisplaceTowardsSource` | Number | `1` |

### Context: `Conditional_NotBoss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CanApplyToInanimate` | Block | `{ ... }` |
| `CaptureFamiliar` | Number | `1` |
| `Conditional_HealthThreshold` | Block | `{ ... }` |
| `Doomed` | Number | `1` |
| `ExplodeCharacter_RockCrusher` | Number | `5, 9` |
| `FactionConversion` | Number | `1` |
| `Fear` | Array | `[ 1 .3 ]` |
| `PermanentCharm` | Number | `1` |
| `VaporizeInanimate` | Number | `1` |
| `Vaporize` | Number | `1` |

### Context: `Conditional_NotBossOrBig`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Immobile` | Number | `1` |

### Context: `Conditional_NotShielded`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Knockback` | Number | `10, 3` |

### Context: `Conditional_Object`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CanApplyToInanimate` | Block | `{ ... }` |
| `Conditional_HasTag` | Block | `{ ... }` |
| `Else` | Block | `{ ... }` |
| `RepairWeapon` | Number | `1` |

### Context: `Conditional_OncePerBattle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CompleteItemQuest` | Enum/String | `Nuke` |
| `TriggerGameEnding` | Number | `1, 0` |
| `key` | Enum/String | `gamewin` |

### Context: `Conditional_PlayerCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Adrenaline` | Number | `10` |
| `ApplyToSource` | Block | `{ ... }` |
| `Cleanse` | Number | `0` |
| `ConjureRandomAbilityFromCat` | Number | `1` |
| `GenericDebuff` | Number | `999999` |
| `KnockOutClone` | Enum/String | `PlayerCat_MiniMiniMe` |
| `Scrambled` | Number | `1` |
| `T2CopyCat` | Number | `1` |

### Context: `Conditional_RandomChance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyPassives` | Block | `{ ... }` |
| `odds` | Number | `10%` |

### Context: `Conditional_Shielded`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusDamage` | Enum/String | `str` |
| `Cleave` | Number | `1` |
| `Stun` | Number | `1` |

### Context: `Conditional_SourceAbilityHasTag`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `ScatterCoins` | Block | `{ ... }` |
| `tag` | Enum/String | `weapon_throw` |

### Context: `Conditional_SourceHasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bruise` | Number | `1` |
| `status` | Enum/String | `AlphaCat` |

### Context: `Conditional_Speculative`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusDamageBasedOnDistance` | Number | `1` |
| `BonusDamage` | Number | `-1` |
| `CapDamage` | Number | `1` |
| `Conditional_HealthThreshold` | Block | `{ ... }` |
| `Else` | Block | `{ ... }` |
| `IgnoreDamage` | Number | `1` |
| `Knockback` | Number | `10` |
| `RandomBonusDamage` | Number | `25` |

### Context: `ConjureBonusAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `Colorless, Class` |
| `upgraded` | Boolean | `true` |

### Context: `Consumed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_not_pop_corpse` | Boolean | `true` |
| `drop_body_ability` | Enum/String | `MoonHandDrop` |
| `drop_on_death` | Enum/String | `deferred, false, true` |
| `drop_on_self_death` | Boolean | `true` |
| `extra_statuses` | Block | `{ ... }` |
| `force_contact` | Boolean | `true` |
| `instant` | Boolean | `true` |
| `kill_on_consume` | Boolean | `true` |
| `mount_mode` | Enum/String | `auto, true` |
| `struggle_ability` | Enum/String | `TinaFlail, TinaFlailRage, Thrash` |
| `use_placeholder` | Boolean | `true` |
| `wet` | Boolean | `false, true` |

### Context: `CopySpells`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `1` |
| `upgraded` | Boolean | `true` |

### Context: `Craft`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Enum/String | `stick, allsticks, tinkerer_default` |
| `slot` | Enum/String | `weapon, random_empty_armor, trinket` |
| `temporary` | Boolean | `false` |
| `works_with_tech` | Boolean | `true` |

### Context: `CreateGlobalModifiers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BloodRain` | Number | `1` |
| `LowerAmbientLight` | Block | `{ ... }` |

### Context: `DelayCastAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `FetusAirstrike` |
| `lingering` | Boolean | `true` |
| `relative` | Boolean | `false` |

### Context: `DelayedWindCone`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `5` |
| `distance` | Number | `10` |

### Context: `DestroyEquipmentAndAttachParasite`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `1, .15` |
| `pool` | Enum/String | `parasites, [ FlyHat FlyMask FlyNeck ], [ AmoebaHat AmoebaNeck AmoebaFace ]` |

### Context: `DoDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage_tiles` | Enum/String | `all` |
| `damage` | Number | `5, 8, 0` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Water ], [ Fire ]` |
| `type` | Enum/String | `generic_physical, melee, spell` |

### Context: `DoDistortionRing`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `intensity` | Number | `1, 2, -1` |
| `radius` | Number | `5, 4` |
| `speed` | Number | `30, -30, 20` |

### Context: `DoScreenShake`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `intensity` | Number | `20, 10, 3` |
| `time` | Number | `2, .75, .5` |

### Context: `DustOnHit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `GasCloud` |

### Context: `DybbukPossessed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit_ability` | Enum/String | `DybbukReturn` |
| `punch_self_ability` | Enum/String | `Dybbuk_StopHittingYourself` |

### Context: `Else`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `ApplyToRandomPartyMemberIfPossible` | Block | `{ ... }` |
| `ApplyToSource` | Block | `{ ... }` |
| `BonusDamage` | Number | `1, 5, 20+bonus_melee_damage` |
| `Bruise` | Number | `4` |
| `CanApplyToInanimate` | Block | `{ ... }` |
| `CatPartsTransform` | Block | `{ ... }` |
| `Charmed` | Number | `2` |
| `Cleanse` | Number | `0` |
| `Cleave` | Number | `1` |
| `Conditional_Displaceable` | Block | `{ ... }` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `Conditional_HasStatus` | Block | `{ ... }` |
| `Conditional_HasTag` | Block | `{ ... }` |
| `Conditional_HealthThreshold` | Block | `{ ... }` |
| `Conditional_Object` | Block | `{ ... }` |
| `Conditional_Speculative` | Block | `{ ... }` |
| `Confusion` | Number | `1, 2` |
| `ConstitutionUp` | Number | `1` |
| `Consumed` | Block | `{ ... }` |
| `CritChanceUp` | Number | `5` |
| `DamageUp` | Number | `1` |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` |
| `DieViolently` | Number | `1` |
| `DoDamage` | Block | `{ ... }` |
| `DodgeChance_Status` | Number | `5` |
| `DybbukPossessed` | Block | `{ ... }` |
| `Else` | Block | `{ ... }` |
| `ExplodeCharacter_Party` | Number | `5` |
| `ExplodeCharacter` | Number | `5` |
| `FaceCamera` | Number | `1` |
| `FlatAIBonus` | Number | `-999999` |
| `ForceImmediateMove` | Number | `1` |
| `FormChange` | Enum/String | `LastHit, Nuke` |
| `FullHeal` | Number | `1, 0` |
| `GainCoinsRange` | Block | `{ ... }` |
| `GainDisorderFromPool_PostCast` | Enum/String | `forbidden_spell_consequences_crippling` |
| `GenericDebuff` | Number | `100` |
| `ImmediateUseAbility` | Enum/String | `tk_ButterBean_Normal` |
| `Immobile` | Number | `1` |
| `Instakill` | Number | `25` |
| `KnockUpAndAway` | Block | `{ ... }` |
| `Leeches` | Number | `2` |
| `ObjectOnHitCharacter` | Enum/String | `Maggot` |
| `OverrideDamage` | Number | `0` |
| `PartialCleanse` | Number | `1` |
| `PurgeAll` | Number | `1` |
| `RandomStatDown` | String | `"ceil(X/2)", "ceil(X/3)"` |
| `RandomStatUp` | Number | `1, 2` |
| `RandomStatusFromPool` | Block | `{ ... }` |
| `RemoveMovePoints` | Number | `1` |
| `RemoveTurnsThisRound` | Number | `1` |
| `Revive` | Number | `1, 100%` |
| `ScatterCoins` | Block | `{ ... }` |
| `SetHealth` | Number | `1` |
| `SetShield` | Number | `88` |
| `ShowFakeDamage` | Block | `{ ... }` |
| `Slow` | Number | `1` |
| `SpawnBearTrapIfHitKills` | Number | `1` |
| `SpawnThingIfHitKills` | Enum/String | `Bait` |
| `SpeculativeMoveSelfCorpseOffMap` | Number | `1` |
| `SpeedUp` | Number | `1` |
| `Temporary` | Block | `{ ... }` |
| `VaporizeInanimate` | Number | `1` |
| `Vaporize` | Number | `1, 20` |
| `XIsTargetHealth` | Block | `{ ... }` |

### Context: `EvolveAbilityFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Enum/String | `Hunter, Thief, Mage` |
| `upgraded` | Boolean | `true` |

### Context: `FindItemFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.02, .15` |
| `pool` | Enum/String | `chapter` |

### Context: `ForceAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `immediate` | Boolean | `true` |

### Context: `ForceImmediateMoveAndAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `G3GrabHead` |
| `even_if_cant_reach` | Boolean | `true` |

### Context: `ForceMoveTowardsTaggedObject`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MoveTwoTrample, MoveOneTrample` |
| `tag` | Enum/String | `food` |

### Context: `FormChange`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `30%` |
| `form` | String | `"Rage", "Turtled", Rage` |

### Context: `GainCoinsRange`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `max` | Number | `2, 4, 30` |
| `min` | Number | `1, 2, 10` |

### Context: `IncAuxCounterClamped`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `change` | Number | `-1, -2, -3` |
| `max` | Number | `3` |

### Context: `IncAuxCounterCycle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `change` | Number | `1` |
| `max` | Number | `3` |

### Context: `KnockOutCoin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.5` |
| `stacks` | Number | `1` |

### Context: `KnockUpAndAway`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `circular_variance` | Number | `2` |
| `distance` | Number | `2, -3, 3` |
| `height` | Number | `2, 0` |
| `stacks` | Number | `1, 5, 5+bonus_melee_ability_damage` |

### Context: `LateStatusApplication`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddWeaponAux` | Number | `2` |
| `CurrentWeaponDamageUp` | Number | `1, 5` |

### Context: `LeaveBehind`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `Fly, CharmedMaggot, Twister` |

### Context: `LowerAmbientLight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `amount` | Array | `[ 50% 60% 60% ]` |
| `speed` | Number | `4` |

### Context: `Madness`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `1` |
| `tickdown_this_turn` | Boolean | `true` |

### Context: `Math`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `Stun` | Number | `1` |
| `stacks` | Number | `1` |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `effects` | Block | `{ ... }` |

### Context: `MergeDamageInstance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `can_instapop` | Boolean | `false` |
| `force_no_hit_animation` | Boolean | `true` |

### Context: `Metronome`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `banned_abilities` | Array | `[ BatteryNuke WeAreOne Metronome SmartMetronome BecomeEnt...` |
| `stacks` | Number | `1` |

### Context: `NextAttackSpecialCrit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | `2` |
| `extra_coins_per_stack` | Number | `2` |
| `luck_increase` | Number | `1` |

### Context: `NextBasicAttackCritsThisTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |
| `piercing` | Boolean | `true` |
| `stacks` | Number | `1` |

### Context: `NextBattleStatusStacks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | `2` |
| `fights` | Number | `9999` |

### Context: `NukeQuestFinalBossModifications`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage_instance` | Block | `{ ... }` |
| `self_damage` | Block | `{ ... }` |
| `splash_damage` | Block | `{ ... }` |

### Context: `ObjectOnHit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `Poop` |

### Context: `ObjectOnHitCharacter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `1, .5` |
| `object` | Enum/String | `CharmedFlea` |

### Context: `OverHealToStatuses`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomStatUp` | Number | `1` |
| `TakeExtraTurn` | Number | `1` |
| `stack_scale` | Number | `0` |

### Context: `PassiveWhileNotTakingTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddStatusToBasicAttack` | Block | `{ ... }` |

### Context: `PoolMetronome`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Array | `[ Shockwave Ping Telefrag Stasis Reduce Zealot ]` |

### Context: `PopAndSpawn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `clone_items` | Boolean | `false` |
| `clone_referenced_catdata` | Boolean | `true` |
| `no_splatter` | Boolean | `false` |
| `object` | Enum/String | `PlayerCat_ClotClone, BoyShade` |

### Context: `QuakeAreaChance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `50%` |
| `radius` | Number | `1, 0` |

### Context: `RandomDistanceDisplace`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `min_dist` | Number | `4` |
| `stacks` | Number | `20` |

### Context: `RandomKnockback`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `max` | Number | `10, 3` |
| `min` | Number | `1` |

### Context: `RandomMagicMissile`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `full_size` | Boolean | `true` |
| `stacks` | Number | `4, 3` |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `BackflipWhenTargeted` | Number | `1` |
| `BleedThorns` | Number | `1` |
| `Bleed` | Number | `1` |
| `Blind` | Number | `1` |
| `BonusDamage` | String | `"ceil(X/2)", -5, -4` |
| `Brace` | Number | `1` |
| `Bruise` | Number | `1, 2` |
| `Burn` | Number | `1` |
| `Charge` | Number | `1, 8, 4` |
| `CharismaUp` | Number | `1` |
| `Charmed` | Number | `1` |
| `Confusion` | Number | `1` |
| `ConstitutionUp` | Number | `1` |
| `CritChanceUp` | Number | `1` |
| `DamageUp` | Number | `1` |
| `DelayedPain` | Number | `1` |
| `DexterityUp` | Number | `1` |
| `DiminishingHealthRegen` | Number | `1` |
| `DivineShield` | Number | `1` |
| `DodgeChance_Status` | Number | `1` |
| `Fear` | Number | `1` |
| `FormChange` | Block | `{ ... }` |
| `Freeze` | Number | `1` |
| `GainCoins` | Number | `1, 5, -5` |
| `HealthRegenUp` | Number | `1` |
| `Hex` | Number | `1` |
| `Immobile` | Number | `1` |
| `IncAuxCounterClamped` | Block | `{ ... }` |
| `Infested` | Number | `1` |
| `IntelligenceUp` | Number | `1` |
| `KineticSpikes` | Number | `1` |
| `Lifesteal` | Number | `1` |
| `LuckUp` | Number | `1` |
| `Madness` | Number | `1` |
| `MagicWeakness` | Number | `1, 2` |
| `ManaGain` | String | `"-ceil(X/2)", X` |
| `Marked` | Number | `1` |
| `MoveQuivered` | Number | `1` |
| `Ostracized` | Number | `1` |
| `Petrify` | Number | `1` |
| `PoisonLace` | Number | `1` |
| `Poison` | Number | `1` |
| `Quivered` | Number | `1` |
| `RandomStatDown` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `Reflect` | Number | `1` |
| `RefreshActPoints` | Number | `1` |
| `RefreshMovePoints` | Number | `1` |
| `Rot` | Number | `1` |
| `Scrambled` | Number | `2` |
| `Shield` | Number | `1, 2, 4` |
| `Sleep` | Number | `1` |
| `Slow` | Number | `1, 2` |
| `SpeedUp` | Number | `1` |
| `SpellDamageUp` | Number | `1` |
| `StrengthUp` | Number | `1` |
| `Stun` | Number | `1` |
| `Tarred` | Number | `1` |
| `TempCounterAttack` | Number | `1` |
| `Thorns` | Number | `1, 2` |
| `Weakness` | Number | `1, 2` |

### Context: `RemoveStatusStacks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `1` |
| `status` | Enum/String | `Brace` |

### Context: `ReplaceSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `None, MoonHeadCommandStopHittingYourself` |
| `slot` | Number | `1, 2, 0` |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `effects` | Block | `{ ... }` |

### Context: `ReviveNextRound`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, 2` |
| `DivineShield` | Number | `2` |
| `Shield` | Number | `15, 20` |
| `revive_health` | Number | `1, 100%, 50%` |
| `stacks` | Number | `2` |

### Context: `ScatterCoins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stackable` | Boolean | `true` |
| `stacks` | Enum/String | `item_aux, "max(min(X+1, item_aux), 0)"` |

### Context: `ScrambleLastUsedSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `permanent` | Boolean | `true` |

### Context: `SetAnimationAlts`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `dead` | Enum/String | `deadShot` |
| `dying` | Enum/String | `shot` |

### Context: `SetCrazyEyeBackgroundWeights`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `weights` | Array | `[ 1 0 0 ], [ 0 0 1 ], [ 0 1 0 ]` |

### Context: `ShowFakeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `999` |
| `style` | Array | `[ crit ]` |

### Context: `SmartMetronome`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `20` |
| `upgraded` | Boolean | `true` |

### Context: `SpreadDisease`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `30%` |
| `disease` | Enum/String | `Cancer` |

### Context: `StatusGroup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DamageOrHealConditionally` | Number | `1` |
| `Freeze` | Number | `2` |

### Context: `StatusKillers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Confusion` | Number | `10` |

### Context: `StatusOnBattleEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomMutation` | Number | `3` |
| `RandomTaggedMutation` | Enum/String | `bird, melted` |
| `even_if_dead` | Boolean | `true` |

### Context: `SwapWeapon`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Array | `[ TerminatorShotgun TerminatorSniper TerminatorUzi ]` |

### Context: `SwitchMusic`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `crossfade_speed` | Number | `1` |
| `new_layer` | Enum/String | `map, battle, event` |
| `new_song` | Enum/String | `same` |

### Context: `TakeBonusTurnWithAIControl`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `include_spells` | Boolean | `true` |

### Context: `TakeBonusTurnWithStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Confusion` | Number | `1` |
| `Madness` | Number | `1` |
| `Stun` | Number | `1, [ 1 .75 ]` |
| `TempNoManaRegen` | Number | `1` |

### Context: `Tangled`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `alt_art` | Enum/String | `TangledMeat` |
| `stacks` | Number | `1` |

### Context: `TeamCastAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `CollectiveCounterImpl, CollectiveSpinImpl` |
| `same_orientation` | Boolean | `true` |
| `tag_restriction` | Enum/String | `collective` |

### Context: `TempPassiveWhileHasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddManaRegen` | Number | `5` |
| `HealthRegenUp` | Number | `5` |
| `MeleeRevengeDamage` | Block | `{ ... }` |
| `ReplaceSpell` | Block | `{ ... }` |
| `status` | Enum/String | `Sleep, Consumed` |

### Context: `Temporary`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `data` | Number | `2` |
| `expires_on_appliers_turn` | Boolean | `true` |
| `expires_on_begin_turn` | Boolean | `true` |
| `expires_on_end_turn` | Boolean | `true` |
| `expires_on_move` | Boolean | `true` |
| `stacks` | Number | `1, 5, 10` |
| `status` | Enum/String | `AllDamageImmune, Brace, Thorns` |
| `turns` | Number | `1, 3` |

### Context: `TimeDelayStatusApplication`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Cleanse` | Number | `0` |
| `CreateGlobalModifiers` | Block | `{ ... }` |
| `DoScreenShake` | Block | `{ ... }` |
| `FormChange` | Enum/String | `DualSword` |
| `FullHeal` | Number | `1` |
| `GlobalSpawnCharacter` | Enum/String | `MegaGuppy` |
| `PlayBackground` | Number | `1` |
| `RemoveAmbientLightEffects` | Enum/String | `.5` |
| `SwitchMusic` | Block | `{ ... }` |
| `Vaporize` | Number | `1` |
| `delay` | Number | `1.13333, .25, 3` |

### Context: `TransformEquipment`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `from` | Enum/String | `JarOfChaos` |
| `to` | Enum/String | `JarOfNothing` |

### Context: `TransformWeapon`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `from` | Enum/String | `Necro_SoulDagger_Uncharged` |
| `to` | Enum/String | `Necro_SoulDagger_Charged` |

### Context: `TwisterDisplaceWithDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `1, inherit` |
| `exclude_prefix` | Enum/String | `Twister` |
| `max_dist` | Number | `2, 3, 20` |
| `min_dist` | Number | `2, 3` |

### Context: `UseAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `T3Pebbles_BoulderDrop` |
| `respect_prime` | Boolean | `true` |

### Context: `UseMoveAbilityWithAI`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `LEPortFar` |
| `move_weights` | Enum/String | `stay_far_move_far` |

### Context: `VisualCountDownThenApplyStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `neck_NukeExplode` |

### Context: `WaggleClone`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `1x1_object` | Enum/String | `cWaggle` |
| `2x2_object` | Enum/String | `cWaggle2x2` |
| `3x3_object` | Enum/String | `cWaggle3x3` |
| `stacks` | Number | `5` |

### Context: `XIsSpellStormRampAndReset`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `reset_percent` | Number | `50%` |
| `stacks` | Number | `0` |

### Context: `XIsTargetHealth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusDamage` | String | `"max(0, floor(X/6)-1)", "max(0, floor(X/2)-1)"` |

### Context: `additional_passives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` |
| `ApplyPassivesToSpawnerWhileAlive` | Block | `{ ... }` |
| `CaptureFamiliar` | Number | `1` |
| `DamageUp` | Number | `2` |
| `FadeInsteadOfDie` | Number | `1` |
| `FillMana` | Number | `1` |
| `HealthGain` | Number | `8` |
| `HideEquipment` | Enum/String | `neck` |
| `IllusionTint` | Number | `1` |
| `InjuryImmunity` | Number | `1` |
| `PermanentMadness` | Number | `1` |
| `ReviveNextRound` | Block | `{ ... }` |
| `SafeDoomed` | Number | `1, 2, level` |
| `SchizoIllusionAIModifier` | Number | `1` |
| `SpeedUp` | Number | `4` |

### Context: `bonk_damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `0` |
| `effects` | Block | `{ ... }` |

### Context: `bonus_passives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AbilityDisableIfLivingCrow` | Number | `1` |
| `AbilityEnableIfConsumedCharacterHasTag` | Enum/String | `sp_pill_normal, sp_pill_tar, sp_pill_fire` |
| `AbilityEnabledAtHealthThreshold` | Number | `50%` |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | `1` |
| `AbilityEnabledIfHasStatus` | Enum/String | `DemonicGlyph_Summon, DemonicGlyph_Bite` |
| `AbilityEnabledIfMovementTrapped` | Number | `1` |
| `AbilityEnabledIfNoAggroTarget` | Number | `1` |
| `AbilityEnabledIfNotHasStatus` | Enum/String | `BackflipWhenTargeted` |
| `AbilityEnabledIfSpecificItemEquipped` | Enum/String | `Neverstone` |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | `16, 25%, 50%` |
| `AbilityEnabledOncePerRound` | Number | `1` |
| `AbilityEnabledPercentEachTurn` | Number | `25%, 35%, 50%` |
| `AbilityInheritsWeaponEffects` | Number | `1, 2` |
| `AbsorbManaFromOtherSpells` | Number | `1` |
| `AddElementsToSpells` | Enum/String | `Earth` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `AlphaDodgeChance` | Number | `50%` |
| `AlphaStatusOnTurnBegin` | Block | `{ ... }` |
| `AutocastEachRound` | Block | `{ ... }` |
| `BonusAbility_DelayedApplication` | Enum/String | `Slap` |
| `CapTechSpent` | Number | `1` |
| `CatchBoomerang` | Number | `1` |
| `CaveWomanBirthControl` | Number | `1` |
| `ChargeSpiritBombAura` | Enum/String | `DonateEnergy2, DonateEnergy` |
| `CopyBasicAttackEffects` | Number | `1` |
| `CopyCatPassive_Initializer` | Number | `1, 2` |
| `CritChanceUp` | Number | `25` |
| `DeadAltAbility` | Enum/String | `LifeDrain_Afterlife, CarrionShot_Afterlife, CarrionShot_Afterlife2` |
| `DownRankAIIfWeaponUsable` | Enum/String | `.001` |
| `FistOfFateUniqueEnemyTracker` | Number | `1` |
| `FreeFirstCastAndAfterSpendMana` | Number | `1` |
| `FreeFirstCastEachMatch` | Number | `1` |
| `FreeFirstCast` | Number | `1, 4` |
| `HealthRegenUp` | Number | `3` |
| `IgnoreTiles` | Number | `1` |
| `IntelligenceUp` | Number | `2` |
| `InterchangeDisabler` | Number | `1` |
| `KnockbackImmunity` | Number | `1` |
| `MoonHeadFinisherEnabler` | Number | `1, -1, 0` |
| `NukeQuestFinalBossModifications` | Block | `{ ... }` |
| `PassiveWhileNotTakingTurn` | Block | `{ ... }` |
| `ReloadOnAllyCatDies` | Number | `1` |
| `ReloadOnAllyDies` | Number | `1` |
| `ReloadOnAnyDamage` | Number | `1` |
| `ReloadOnBackstab` | Number | `1` |
| `ReloadOnElementalDamageReceived` | Enum/String | `Holy` |
| `ReloadOnGainCoins` | Number | `1` |
| `ReloadOnGainDivineShield` | Number | `1` |
| `ReloadOnKillEnemy` | Number | `1` |
| `ReloadOnKillTagged` | Enum/String | `rock` |
| `ReloadOnKill` | Number | `1` |
| `ReloadOnSpendMana` | Number | `1` |
| `ReloadOnTotalDamageReceived` | Number | `25, 15` |
| `ReloadOnUseAbilityWithManaCost` | Number | `6` |
| `RevengeDamage` | Block | `{ ... }` |
| `StatusKillers` | Block | `{ ... }` |
| `TossTargetIsAggroTarget` | Number | `1` |
| `TossTargetIsBuddy` | Number | `1` |
| `TossTargetIsNotInWater` | Number | `1` |
| `Trample` | Number | `3` |
| `XIsConsumedCharacterMaxHP` | Number | `3` |
| `XIsCountDeaths` | Number | `1` |
| `XIsCountStatusStacks` | Enum/String | `DodgeChance_Status` |
| `XIsFormulaLockedUntilComplete` | Enum/String | `dex` |
| `XIsFreeArmorSlots` | Number | `1` |
| `XIsIncreaseEachTurn` | Number | `1` |
| `XIsLivingAlliesWithTag` | Enum/String | `terminator_mini, hitler_clone_fetus, dc_crow` |
| `XIsLivingCharactersWithTag` | Enum/String | `husk, rock` |
| `XIsMultipliedPercentHealth` | Array | `[ 1 12 ], [ 14 1 ], [ 6 2 ]` |
| `XIsOtherHealsThisTurn` | Number | `1` |
| `XIsRampAndReset` | Number | `0` |
| `XIsRecycleCostReduction` | Number | `5` |
| `XIsSpellStormRampAndReset` | Number | `0, { ... }` |
| `XIsTimesDamageTaken` | Number | `1` |

### Context: `cost`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `X_cant_be_zero` | Boolean | `true` |
| `act_points` | Number | `1, 0, 3` |
| `allow_offmap_casts` | Boolean | `true` |
| `can_be_refreshed` | Boolean | `false` |
| `can_cast_while_dead` | Boolean | `true` |
| `can_pay_over_multiple_turns` | Boolean | `true` |
| `can_self_refresh` | Boolean | `false` |
| `cant_cast` | Enum/String | `X-5, false, true` |
| `cantrip_group` | Enum/String | `THC_CoinRoll, kaiju_roar, spewer_suck` |
| `cantrip` | Boolean | `false, true` |
| `charge` | Number | `1, "1-clamp(spd,0,1)", 0` |
| `coins` | Number | `1, 5, 7` |
| `damage_cant_be_zero` | Boolean | `true` |
| `disallow_cost_modification` | Boolean | `true` |
| `durability` | Number | `0` |
| `enabled_formula` | Number | `1, 1-X, X` |
| `infcantrip` | Boolean | `false, true` |
| `initial_charge` | Number | `1` |
| `main_turn_only` | Boolean | `true` |
| `mana` | Number | `7, 5, 0` |
| `manacost_cant_be_zero` | Boolean | `true` |
| `minimum_con` | Number | `1` |
| `minimum_spd` | Number | `1` |
| `move_points` | Number | `1, 0` |
| `must_be_consuming` | Boolean | `true` |
| `must_be_first_action` | Boolean | `false, true` |
| `must_be_first_nonmove_action` | Boolean | `true` |
| `must_be_offmap` | Boolean | `true` |
| `must_have_weapon` | Boolean | `true` |
| `must_not_be_a_summon` | Boolean | `true` |
| `must_not_be_consuming` | Boolean | `true` |
| `once_per_fight` | Enum/String | `3-X, false, true` |
| `prime` | Number | `1` |
| `require_default_size` | Boolean | `true` |
| `requires_attack_damage_threshold` | Number | `2` |
| `requires_consumed_trinket` | Boolean | `true` |
| `requires_destructible_weapon` | Boolean | `true` |
| `requires_empty_trinket` | Boolean | `true` |
| `requires_exact_character_aux` | Number | `1, 2, 0` |
| `requires_hp_threshold` | Number | `200` |
| `requires_reload` | Boolean | `true` |
| `requires_weapon` | Boolean | `true` |
| `start_reloaded` | Boolean | `true` |

### Context: `damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `0` |
| `type` | Enum/String | `none` |

### Context: `damage_instance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthRegenUp` | Number | `2` |
| `accuracy` | Enum/String | `.5` |
| `ai_base_score` | Number | `1000, 9999, 999999` |
| `blocked_damage` | Enum/String | `3+bonus_melee_ability_damage, 5+bonus_melee_damage, 7+bonus_melee_ability_damage` |
| `blocked_multiplier` | Number | `2` |
| `can_collect_pickups` | Boolean | `true` |
| `can_instapop` | Boolean | `false` |
| `can_revive` | Boolean | `true` |
| `cant_miss` | Boolean | `true` |
| `contact_requires_adjacency` | Boolean | `false` |
| `crit_chance` | Number | `-999999, 100%, .5` |
| `custom_additional_ai_weight` | Enum/String | `toss_towards_buddy, prefer_dont_move, tile_close_to_enemy` |
| `damage_shield_only` | Boolean | `true` |
| `damage` | Number | `2, 0, 4` |
| `disallow_modifications` | Boolean | `true` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Gravity ], [ Holy ], [ Water ]` |
| `faction` | Enum/String | `auto` |
| `final_hit_bonus_damage` | Enum/String | `5+bonus_melee_ability_damage` |
| `force_adjacent_and_diagonal_contact` | Boolean | `true` |
| `force_no_contact` | Boolean | `true` |
| `force_no_knockback` | Boolean | `true` |
| `force_play_hit_animation` | Boolean | `true` |
| `heal` | Number | `1, 4, 10` |
| `hint_dont_lowgravboost` | Boolean | `true` |
| `hit_animation_alt` | Enum/String | `catch` |
| `incidentally_collects_pickups` | Boolean | `false, true` |
| `knockback` | Number | `1, 5, "ceil(X*.25/5)"` |
| `layer` | Enum/String | `characters, all, tiles` |
| `makes_contact` | Boolean | `false, true` |
| `non_lethal` | Boolean | `true` |
| `override_trample_damage` | Boolean | `true` |
| `piercing` | Boolean | `true` |
| `ranged` | Boolean | `true` |
| `raw_damage` | Enum/String | `int, "(con+1)/2", "max((X-1)*2, 0)"` |
| `raw_heal` | String | `"100-X", "(str+1)/2"` |
| `show_damage_on_0` | Boolean | `true` |
| `two_way_contact` | Boolean | `true` |
| `type` | Enum/String | `melee, physical_spell, status_spell` |

### Context: `damage_threshold_altanimations`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `heaviestMelee` | Number | `20` |
| `heavyMelee` | Number | `10` |

### Context: `effects`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AIFavorLowHealth` | Number | `100` |
| `AddSpiritBombCharges` | Number | `1, 2` |
| `AllStatsUp` | Enum/String | `item_aux, 1, -1` |
| `AlliesTakeExtraTurn` | Number | `1` |
| `AlphaCat` | Number | `1` |
| `AlternateIdleAnimation` | Enum/String | `berserkIdle` |
| `Ammo` | Number | `-99999, -1, 6` |
| `ApplyMultipleTimes` | Block | `{ ... }` |
| `ApplyPassives` | Block | `{ ... }` |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | `1` |
| `ApplyStatusIfCrit` | Block | `{ ... }` |
| `ApplyStatusesNextTurnBegin` | Block | `{ ... }` |
| `ApplyToConsumed` | Block | `{ ... }` |
| `ApplyToOthersWithSharedTagAndFaction` | Block | `{ ... }` |
| `ApplyToRandomClosestAlly` | Block | `{ ... }` |
| `ApplyToSourceOnKill` | Block | `{ ... }` |
| `ApplyToSource` | Block | `{ ... }` |
| `ArcLightning` | Block | `{ ... }` |
| `Attraction` | Number | `1` |
| `BackflipWhenTargeted` | Number | `1, 2, { ... }` |
| `Bleed` | Number | `1, 2, 10` |
| `Blind` | Number | `1, [ 1 .25 ], [ 2 .33 ]` |
| `Bloodzerked` | Number | `1` |
| `BodyGuard` | Block | `{ ... }` |
| `BombRatTurtle` | Number | `1` |
| `BonusDamageBasedOnMana` | Number | `1` |
| `BonusKnockbackDamage` | Number | `2` |
| `BounceObject` | Enum/String | `CharmedDip, SmallRock, CharmedFlea` |
| `BounceRock` | Enum/String | `SmallLavaRock, SmallRock, [ 1 .2 ]` |
| `Bound` | Number | `3` |
| `Brace` | Number | `1, 2, 4` |
| `BramblesOnHit` | Number | `1` |
| `Bruise` | Number | `5, 1, 2` |
| `BurgleCoin` | Number | `1, 3, [ 1 .5 ]` |
| `Burn` | Number | `1, 2, 3` |
| `BypassRockKnockback` | Number | `1` |
| `CanApplyToInanimate` | Block | `{ ... }` |
| `CancelPrimedAbilities` | Number | `1` |
| `CanceledQueuedInput` | Number | `1` |
| `CaptureFamiliar` | Number | `1` |
| `CatPartsSizeScaleStatus` | Block | `{ ... }` |
| `CatPartsTransform` | Block | `{ ... }` |
| `ChampionUpgradeNextMinion` | Number | `1` |
| `ChanceToBreakFree` | Block | `{ ... }` |
| `ChanceToBreak` | Number | `5, 15, 20` |
| `ChangeCatClass` | Enum/String | `Hunter, Fighter, Mage` |
| `ChangeFaction` | Enum/String | `sabertooths` |
| `ChangeTile` | Enum/String | `LavaTile, FireTile, WaterTile` |
| `ChangeTilesUnder` | Enum/String | `DirtTile` |
| `ChaosBossFlipMidTeleport` | Number | `1` |
| `ChaosBossFormChange` | Number | `1` |
| `ChargeFists` | Number | `1` |
| `Charge` | Number | `1, 2` |
| `CharismaUp` | Enum/String | `item_aux, 1, -2` |
| `CharmedFacingForceAttack` | Number | `1` |
| `CharmedForceAttack` | Number | `1` |
| `Charmed` | Number | `1, [ 1, .1+.02*cha ], level` |
| `Cleanse` | Number | `1, 0` |
| `ClearFinalBossBattlefield` | Number | `1` |
| `ClearStarving` | Number | `1` |
| `Cleave` | Number | `1, { ... }` |
| `CloneWeaponTemp` | Number | `1` |
| `CoinTossBounce` | Enum/String | `X` |
| `CollectsPickupsWithAltEffects` | Block | `{ ... }` |
| `CollectsPickups` | Number | `1, 2` |
| `CollideWithConsumed` | Enum/String | `1+bonus_melee_damage, 5+bonus_melee_damage, 4+bonus_melee_damage` |
| `CollideWithThrowTarget` | Number | `0` |
| `Conditional_AbilityTargetIsSelf` | Block | `{ ... }` |
| `Conditional_ActiveWeather_Any` | Block | `{ ... }` |
| `Conditional_AffectedByElement` | Block | `{ ... }` |
| `Conditional_Ally` | Block | `{ ... }` |
| `Conditional_Backstab` | Block | `{ ... }` |
| `Conditional_BadRoll` | Block | `{ ... }` |
| `Conditional_BossOrBig` | Block | `{ ... }` |
| `Conditional_Boss` | Block | `{ ... }` |
| `Conditional_Buddy` | Block | `{ ... }` |
| `Conditional_CanBeHealed` | Block | `{ ... }` |
| `Conditional_Corpse` | Block | `{ ... }` |
| `Conditional_DebuffRoll` | Block | `{ ... }` |
| `Conditional_DestructibleCorpse` | Block | `{ ... }` |
| `Conditional_Displaceable` | Block | `{ ... }` |
| `Conditional_Enemy` | Block | `{ ... }` |
| `Conditional_Familiar` | Block | `{ ... }` |
| `Conditional_FirstApplicationThisTurn` | Block | `{ ... }` |
| `Conditional_FormulaIsPositive` | Block | `{ ... }` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `Conditional_HasCleansableDebuffs` | Block | `{ ... }` |
| `Conditional_HasStatus` | Block | `{ ... }` |
| `Conditional_HasTag` | Block | `{ ... }` |
| `Conditional_HealthThreshold` | Block | `{ ... }` |
| `Conditional_InForm` | Block | `{ ... }` |
| `Conditional_IsSelf` | Block | `{ ... }` |
| `Conditional_IsTrample` | Block | `{ ... }` |
| `Conditional_LastHit` | Block | `{ ... }` |
| `Conditional_LivingPlayerCat` | Block | `{ ... }` |
| `Conditional_NotAlly` | Block | `{ ... }` |
| `Conditional_NotBig` | Block | `{ ... }` |
| `Conditional_NotBossOrBig` | Block | `{ ... }` |
| `Conditional_NotBoss` | Block | `{ ... }` |
| `Conditional_NotShielded` | Block | `{ ... }` |
| `Conditional_Object` | Block | `{ ... }` |
| `Conditional_OncePerBattle` | Block | `{ ... }` |
| `Conditional_PlayerCat` | Block | `{ ... }` |
| `Conditional_RandomChance` | Block | `{ ... }` |
| `Conditional_Shielded` | Block | `{ ... }` |
| `Conditional_SourceAbilityHasTag` | Block | `{ ... }` |
| `Conditional_SourceHasStatus` | Block | `{ ... }` |
| `Conditional_Speculative` | Block | `{ ... }` |
| `Confusion` | Number | `1, 2, 4` |
| `ConjureBonusAbility` | Enum/String | `Colorless, random, { ... }` |
| `ConjureSingleUseBonusAbility` | Enum/String | `random` |
| `ConstitutionUp` | Number | `1, -1, [ 1 .5 ]` |
| `Consumed` | Block | `{ ... }` |
| `ContextualHeal` | Number | `1` |
| `CopySpells` | Number | `1, { ... }` |
| `CorpseVaporizer` | Number | `1` |
| `Counterspell` | Number | `1` |
| `Craft` | Block | `{ ... }` |
| `CreateGlobalModifiers` | Block | `{ ... }` |
| `CritChanceUp` | Number | `2` |
| `CurrentWeaponAddElectricElement` | Number | `1` |
| `CurrentWeaponDamageUp` | Number | `1, 3` |
| `DamageBasedOnMissingHealth` | Number | `25, 50` |
| `DamageDistanceAOEFalloff` | Number | `1, 2` |
| `DamageOrHealConditionally` | Number | `1` |
| `DamageTrinket` | Number | `1` |
| `DamageUp` | Number | `1, -1, -2` |
| `DamageWeapon` | Number | `1` |
| `DeathwormUnderground` | Enum/String | `DeathWormEat` |
| `DecoySwapper` | Number | `1` |
| `DeferVaporize` | Number | `1` |
| `DelayCastAbility` | Block | `{ ... }` |
| `DelayedFury` | Number | `75, 0` |
| `DelayedWindCone` | Block | `{ ... }` |
| `DeleteObject` | Number | `1` |
| `DeleteTraps` | Number | `1` |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` |
| `DestroyNeckArmor` | Number | `1` |
| `DestroyTrinket` | Number | `1` |
| `DestroyWeaponThrow` | Number | `1` |
| `DestroyWeapon` | Number | `1` |
| `DexterityUp` | Enum/String | `item_aux, 1, 2` |
| `DieViaAbilityInternally` | Number | `1` |
| `DieViolently` | Number | `1` |
| `Die` | Number | `1` |
| `DiminishingHealthRegen` | Number | `2, 3` |
| `DinoLegAnimation` | Enum/String | `poop` |
| `Disguised` | Number | `1` |
| `DisplaceToOriginalPosition` | Number | `1` |
| `DisplaceTowardsSource` | Number | `1` |
| `Displace` | Number | `1` |
| `DissolveRandomArmorPiece` | Number | `1` |
| `DivineShield` | Number | `1, 2, 4` |
| `DoDistortionRing` | Block | `{ ... }` |
| `DoScreenShake` | Number | `1, { ... }` |
| `DodgeChance_Status` | Number | `10, 50, 20` |
| `DontHealEnemies` | Number | `1` |
| `Doomed` | Number | `1, 2, 3` |
| `DoubleCastSpell` | Number | `1` |
| `DoubleCastSpellsEachTurn_Status` | Number | `1` |
| `DoubleCast` | Number | `1` |
| `DoubleLoot` | Number | `1, 2` |
| `DoubleStatus` | Enum/String | `Burn, Poison, Bleed` |
| `DrainAllyCatsForFleshGolem` | Number | `7` |
| `DrinkWater` | Number | `1` |
| `Drowsy` | Number | `1, 8` |
| `DuplicateRandomEquippedItem` | Number | `1` |
| `DustOnHit` | Block | `{ ... }` |
| `EliteUpgradeNextMinion` | Number | `1` |
| `Else` | Block | `{ ... }` |
| `EmptyMind` | Number | `1` |
| `EnableWeather` | Enum/String | `KaijuMeteornado, KaijuFirestorm, KaijuMeteornadoSolo` |
| `EndTurn` | Number | `1` |
| `Enlarge` | Number | `3` |
| `EnterMount` | Enum/String | `enter` |
| `EvolveAbilityFromPool` | Enum/String | `Fighter, Mage, { ... }` |
| `ExistUntilIdleUpkeep` | Number | `1` |
| `ExplodeCharacter_DeathBloom2` | Number | `5` |
| `ExplodeCharacter_DeathBloom` | Number | `5` |
| `ExplodeCharacter_NoDie` | Number | `1` |
| `ExplodeCharacter` | Number | `5` |
| `ExplosionIfHitSomething` | Number | `5` |
| `ExtraBasicAttacks_Status` | Number | `1` |
| `ExtraBasicMoves_Status` | Number | `1` |
| `FaceAway` | Number | `1` |
| `FaceCamera` | Number | `1` |
| `FactionConversion` | Number | `1` |
| `FactionDisguiseSource` | Number | `1` |
| `FastKnockback` | Number | `4` |
| `Fear` | Number | `1, 2, [ 1 .25 ]` |
| `FillMana` | Number | `1` |
| `FinalBossQueueBeam` | Number | `1` |
| `FireArmor2` | Number | `1` |
| `FireArmor` | Number | `1` |
| `FlatAIBonus` | Number | `999999` |
| `FlatLeech` | Number | `2, 10` |
| `FlowersOnHit` | Number | `1` |
| `ForceAttack` | Number | `1, { ... }` |
| `ForceCollectsPickups` | Number | `1` |
| `ForceDisplace` | Number | `1` |
| `ForceMoveAndAttack` | Number | `1` |
| `ForceMoveAway` | Number | `1` |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | `4, 3` |
| `ForceMoveTowardsEnemies` | Number | `1, MoveOne, DumbMove_Impl` |
| `ForceMoveTowardsTaggedObject` | Block | `{ ... }` |
| `ForceMoveTowards` | Number | `1` |
| `ForceTransferWeapon` | Number | `1` |
| `ForceUseAbility` | Enum/String | `MotherTumorGrow` |
| `FormChange` | Enum/String | `Explosive, DualSword, Holy` |
| `FreeSpell` | Number | `1` |
| `Freeze` | Number | `1, [ 1 .1 ], [ 1 .25 ]` |
| `FullHeal` | Number | `1` |
| `GainCoinsRange` | Block | `{ ... }` |
| `GenericBuff` | Number | `100` |
| `GenericDebuff` | Number | `1, 999, 100` |
| `GiveBoundItemToTarget` | Number | `1` |
| `GlobalSpawnCharacter` | Enum/String | `MegaGuppy` |
| `Grappled` | Number | `1` |
| `HealPercentMaxHP` | Number | `100` |
| `HealRandomInjury` | Number | `1` |
| `HealTo` | Number | `50%` |
| `HealthGain` | Number | `5, 4` |
| `HealthRegenUp` | Number | `1, 2, 3` |
| `HeavyHits` | Number | `1` |
| `Hex` | Number | `1` |
| `HitExplosion` | Number | `5` |
| `IceArmor` | Number | `1` |
| `IgnoreDamage` | Number | `1` |
| `IgnoreDebuffs` | Number | `1` |
| `IgnoreSelf` | Number | `1, true` |
| `ImmediateUseAbility` | Enum/String | `cm_Lard_Impl, HitlerCloneTransform` |
| `ImmediateUseDirectionalAbility` | Enum/String | `BowlDash, BowlDash2` |
| `Immobile` | Number | `1, 2, 0` |
| `Imprison` | Enum/String | `BeefyCharmedLeech, CharmedLeech, Tumor` |
| `IncAuxCounterCycle` | Block | `{ ... }` |
| `IncreaseCumulativeBlastDamage` | Number | `1` |
| `IncreaseItemAuxOnKill` | Number | `1` |
| `Infested` | Number | `1` |
| `Instakill` | Number | `25, 50` |
| `InstantMaxHealthUp` | Number | `4, 20` |
| `IntelligenceUp` | Enum/String | `item_aux, 1, -int` |
| `InterchangeMoveActPoints` | Number | `1` |
| `Invulnerable` | Number | `1` |
| `JohnnyCriesForWashers` | Number | `1, 2` |
| `KineticSpikes` | Number | `1, 2` |
| `KnockOutCoin` | Number | `1, { ... }` |
| `KnockUpAndAway` | Block | `{ ... }` |
| `KnockbackDamageImmuneUntilSettled` | Number | `1` |
| `KnockbackDirectionIsFacingDirection` | Enum/String | `rotate_right, 1, flip` |
| `Knockback` | Number | `1, 5` |
| `LateStatusApplication` | Block | `{ ... }` |
| `LeaveBehindRockOnKnockback` | Number | `1` |
| `Leech` | Number | `1` |
| `Leeches` | Number | `1, 2, 3` |
| `Lifesteal` | Number | `1, 3` |
| `LuckUp` | Enum/String | `item_aux, 1, -2` |
| `MadnessChanceOnTurnBegin` | Number | `2` |
| `Madness` | Number | `1, 999, 3` |
| `MagicWeakness` | Number | `1, [ 1 .1 ], 4` |
| `MakeWeaponUnbreakable` | Number | `1` |
| `ManaGain` | Number | `5, 10, "max((X-1)*2, 0)"` |
| `ManaLeeches` | Number | `1, 2` |
| `ManaStealToHealth` | Number | `-1` |
| `ManaSteal` | Number | `5, -1` |
| `ManglerAttack` | Number | `1` |
| `ManglerShuffle` | Boolean | `false` |
| `Marked` | Number | `1, 5, [ 1 .1 ]` |
| `MassAttackThis` | Number | `1` |
| `Math` | Block | `{ ... }` |
| `MaxHPUp` | Number | `100` |
| `Meaty` | Number | `1` |
| `Metronome` | Number | `1, 2, { ... }` |
| `MimicMetronome` | Number | `1` |
| `MonkStanceSwitch` | Number | `1` |
| `MotherTumorDebugForcePass` | Number | `1` |
| `MoveQuivered` | Number | `1` |
| `MovementUp` | Number | `1, 2, -2` |
| `Muted` | Number | `1` |
| `NextAbilityHeals` | Number | `1` |
| `NextActionLuckUp` | Number | `99` |
| `NextAttackBonusRange` | Number | `1, 5, 3` |
| `NextAttackSpecialCrit` | Number | `1, { ... }` |
| `NextBasicAttackCritsThisTurn` | Block | `{ ... }` |
| `NextBattleStatusStacks` | Block | `{ ... }` |
| `NextDamageReduceAndHealAllies` | Number | `1` |
| `NextTurnDoubleRangedDamage` | Number | `1` |
| `NonStackingDivineShield` | Number | `1` |
| `ObjectOnHitCharacter` | Enum/String | `SmallRock, SkeletonCatFamiliar, { ... }` |
| `ObjectOnHitEmpty` | Enum/String | `SmallRock, AnimalEgg, AnimalEgg2` |
| `ObjectOnHitFullyEmpty` | Enum/String | `RandomArmorPickup` |
| `ObjectOnHit` | Enum/String | `FetusNoJar, BiggestFood, { ... }` |
| `Ostracized` | Number | `2, 4` |
| `OverHealToShield` | Number | `1` |
| `OverHealToStatuses` | Block | `{ ... }` |
| `OverrideChainKnockbackDamage` | Enum/String | `3+bonus_melee_ability_damage` |
| `OverrideChainKnockback` | Number | `1, 10, 3` |
| `OverrideDamage` | Number | `0` |
| `OverrideKnockbackDamage` | Number | `0, 3, str` |
| `PartialCleanse` | Number | `1, 9999` |
| `PartialPurge` | Number | `1` |
| `PermanentCharisma` | Number | `2` |
| `PermanentConstitution` | Number | `2, -1, -2` |
| `PermanentDexterity` | Number | `2` |
| `PermanentImmobile` | Number | `1` |
| `PermanentIntelligence` | Number | `2` |
| `PermanentLuck` | Number | `2` |
| `PermanentSpeed` | Number | `2` |
| `PermanentStrength` | Number | `1, 2` |
| `PermanentUpgradeRandomActiveOrPassive` | Number | `1` |
| `PermanentUpgradeRandomActive` | Number | `1, 4` |
| `Petrify` | Number | `1, [ 1 .1 ], [ 1, .1 ]` |
| `PlayBackground` | Number | `1, 0` |
| `PoisonLace` | Number | `1, "X/5", "X/3"` |
| `Poison` | Number | `2, 4, 3` |
| `PoolMetronome` | Block | `{ ... }` |
| `PopAndSpawn` | Enum/String | `TheDestroyer, Tormentor, StemCat_HalfHealth` |
| `Possessed` | Number | `1` |
| `ProbeCharmed` | Number | `1` |
| `PullSourceToKnockbackImmuneTarget` | Number | `1` |
| `PullSourceToTarget` | Number | `1` |
| `PurgeAll` | Number | `1` |
| `Purge` | Number | `0, 3` |
| `QuakeAreaChance` | Block | `{ ... }` |
| `QueueUseAbility` | Enum/String | `Spider_GoInsane` |
| `RNGCannonRandomDamage` | Number | `100` |
| `RandomDistanceDisplace` | Number | `20, { ... }` |
| `RandomInjury` | Number | `1` |
| `RandomKnockbackDirection` | Number | `4` |
| `RandomKnockback` | Block | `{ ... }` |
| `RandomMagicMissile` | Number | `1, 5, { ... }` |
| `RandomPermanentStat` | Number | `1` |
| `RandomStatDown` | Number | `1, [ 1 .25 ]` |
| `RandomStatUp` | Number | `1, -5, 10` |
| `RandomStatusFromPool` | Block | `{ ... }` |
| `RangeUp` | Number | `1` |
| `Reanimate` | Number | `100%, 50%` |
| `RebukeDamage` | Number | `1, 2` |
| `ReduceManaCostExcludeBrainstorm` | Number | `1` |
| `ReduceManaCost` | Number | `1` |
| `Reflect` | Number | `1, 5` |
| `ReformMoonHead` | Number | `1` |
| `RefreshActPoints` | Number | `1` |
| `RefreshItemAbilities` | Number | `1` |
| `RefreshMovePointsIfHit` | Number | `1` |
| `RefreshMovePoints` | Number | `1` |
| `RefreshNonManaItemAbilities` | Number | `1` |
| `RefreshOncePerFightAbilities` | Number | `1` |
| `RefreshWeaponAbility` | Number | `1` |
| `Regurge` | Number | `1` |
| `RemoveActPoints` | Number | `1` |
| `RemoveMovePoints` | Number | `1` |
| `RemoveStatusStacks` | Block | `{ ... }` |
| `RemoveStatus` | Enum/String | `Sleep, SleepParalysis, Drowsy` |
| `RepairAllCondition` | Number | `1` |
| `RepairAll` | Number | `1, 10` |
| `RepairArmorCondition` | Number | `1` |
| `RepairOnKill` | Number | `1, 2` |
| `RepairWeaponCondition` | Number | `1` |
| `RepairWeapon` | Number | `1, 99` |
| `RerollEnemy` | Number | `1` |
| `ResetArmorShield` | Number | `1` |
| `ReturnDinoLegs` | Number | `1` |
| `ReviveNextRound` | Number | `2, { ... }` |
| `Revive` | Number | `1, 100%, 50%` |
| `Rot` | Number | `1, 2, [ 1 .1 ]` |
| `SafeDie` | Number | `1` |
| `ScatterHeldCoin` | Number | `1, [ 1 .3 ], [ 1 .5 ]` |
| `ScatterRandomPickups` | Number | `2` |
| `ScrambleEverything` | Number | `0, 10%` |
| `ScrambleLastUsedSpell` | Block | `{ ... }` |
| `SelfStun` | Number | `1, [ 1 .5 ]` |
| `SendRock` | Number | `1` |
| `SetCrazyEyeBackgroundWeights` | Block | `{ ... }` |
| `SetDefaultFace` | Enum/String | `insane` |
| `SetDistanceDisplace` | Number | `5` |
| `SetHealth` | Number | `1, 100%` |
| `SetShield` | Number | `0` |
| `ShadowCrit` | Number | `1` |
| `Shatter` | Number | `15` |
| `Shield` | Number | `2, 5, "max((X-1)*2, 0)"` |
| `ShootHereCommand` | Number | `1` |
| `ShootHereReceiver` | Number | `1` |
| `ShortCircuit` | Number | `1` |
| `SignalFinalBossShieldBroke` | Number | `1` |
| `SizeScale` | Enum/String | `.6` |
| `Sleep` | Number | `1, [ 1 .1 ], 3` |
| `Slow` | Number | `1, [ 1 .1 ], [ 1 .25 ]` |
| `SmallHitExplosion` | Number | `1` |
| `SmartMetronome` | Number | `20, { ... }` |
| `SmellBlood` | Number | `1` |
| `SoulLink` | Number | `1` |
| `SoundEventOnHit` | Enum/String | `Batterup_Connect` |
| `SourceSwapsBackEndOfTurn` | Enum/String | `ThiefSwapBack` |
| `SpawnBearTrap` | Number | `1` |
| `SpawnCoinAnywhere` | Number | `1, [ 1 .5 ]` |
| `SpawnCreep` | Number | `1` |
| `SpawnCustomTrap` | Enum/String | `CharmTrap, EggSackTrap, SpikeTrap` |
| `SpawnFlames` | Array | `[ 1, .20 ], [ 1, .20+.1*level ]` |
| `SpawnNeutralWebTrapOnMiss` | Number | `1` |
| `SpawnRock` | Number | `1, [ 1, .20 ]` |
| `SpawnThingIfHitKills` | Enum/String | `Food, BiggestFood, BigFood` |
| `SpawnWebTrap` | Number | `1` |
| `SpecialBossMultipartInstakill` | Enum/String | `moonboss` |
| `SpecificInjury` | Enum/String | `int, str, spd` |
| `SpeculativeMoveSelfCorpseOffMap` | Number | `1` |
| `SpeedUp` | Number | `1, 2, -1` |
| `SpellDamageUp` | Number | `1, 3` |
| `SpellShield` | Number | `1` |
| `SpiderInfested` | Number | `1, 2, 4` |
| `SpitConsumed` | Number | `1` |
| `SplashDamage` | Number | `1` |
| `SpreadDisease` | Block | `{ ... }` |
| `StackingSandstorm` | Number | `1` |
| `StanceSwitchToMelee` | Number | `1` |
| `StatBounty` | Number | `1` |
| `StatusGroup` | Block | `{ ... }` |
| `StealDemonicGlyph` | Number | `1` |
| `StealEquipment` | Enum/String | `any` |
| `StealTurn` | Number | `1` |
| `StealthCritChance` | Number | `100` |
| `Stealth` | Number | `1, 2` |
| `StrengthUp` | Number | `1, 2, item_aux` |
| `Stun` | Number | `1, [ 1 .5 ], [ 1, .25 ]` |
| `SwallowSmallCharacter` | Number | `100%, 50%` |
| `SwapHighestAndLowestStat` | Number | `1` |
| `SwapWeapon` | Block | `{ ... }` |
| `SwitchMusic` | Block | `{ ... }` |
| `Switcheroo` | Number | `1` |
| `T3HitlerTriggerInitialSpawns` | Number | `1` |
| `TagMetronome` | Enum/String | `musical` |
| `TakeBonusTurnWithAIControl` | Block | `{ ... }` |
| `TakeBonusTurnWithStatus` | Block | `{ ... }` |
| `TakeExtraTurnEndOfRound` | Number | `1` |
| `TakeExtraTurn` | Number | `1` |
| `Tangled` | Number | `1, { ... }` |
| `TargetedMetronome` | Number | `20` |
| `Tarred` | Number | `2, [ 1 .1 ]` |
| `Taunting` | Number | `1` |
| `TeamBonusAbility` | Enum/String | `ShootHere` |
| `TeamCastAbility` | Enum/String | `Spin, TeamFlex_Impl, TeamFlex_Impl2` |
| `Tech` | Number | `1, 3` |
| `TeleportBackAtTurnEnd` | Enum/String | `FlashBack` |
| `TempBackstabBleed` | Number | `1` |
| `TempBackstabPiercing` | Number | `1` |
| `TempBackstabPoison` | Number | `1` |
| `TempBackstab` | Number | `75` |
| `TempBasicAttackBonusAOE` | Number | `1` |
| `TempBonusKnockbackDamage` | Number | `1` |
| `TempBonusKnockback` | Number | `1` |
| `TempCounterAttack` | Number | `1` |
| `TempCritChanceUp` | Number | `30, 100` |
| `TempDamageUp` | Number | `1, 2` |
| `TempDexterityUp` | Enum/String | `X` |
| `TempInitiativeChange` | Number | `9999, 100` |
| `TempInjuryImmunity` | Number | `1` |
| `TempLuckUp` | Number | `99` |
| `TempManaCostReduction` | Number | `1` |
| `TempMovement` | Number | `20, mov` |
| `TempPenetrate` | Number | `1` |
| `TempPreEmptiveCounterAttack` | Number | `1` |
| `TempRangeUp` | Number | `1, 20, 3` |
| `TempSpeedUp` | Number | `4, 10, X` |
| `TempSpellDamageUp` | Number | `1` |
| `TempStrengthUp` | Enum/String | `X` |
| `TempTrampleUntilSettled` | Number | `3` |
| `Temporary` | Block | `{ ... }` |
| `ThornsDamageImmuneUntilSettled` | Number | `1` |
| `Thorns` | Number | `6, 1, 2` |
| `TickDownStatus` | Enum/String | `ShortCircuit` |
| `TileDamageImmuneUntilSettled` | Number | `1` |
| `TilesMovedToCritChance` | Number | `1` |
| `TilesMovedToMana` | Number | `1` |
| `TilesMovedToNeighborHeal` | Enum/String | `level` |
| `TilesMovedToStrength` | Number | `1` |
| `TimeDelayStatusApplication` | Block | `{ ... }` |
| `TowerDefenseStatus2` | Number | `1` |
| `TowerDefenseStatus` | Number | `1` |
| `TradeLife` | Number | `1` |
| `TrailBlazer` | Number | `1, mov` |
| `Trample` | Number | `3` |
| `TransformAbility` | Enum/String | `MonkeyThrow, Pounce2, Pounce` |
| `TransformBasicAttack` | Enum/String | `ThrowPoop, TigerSwipes2, TigerSwipes` |
| `TransformBasicMove` | Enum/String | `BasicDashAttackMove_NoKnockback` |
| `TransformEquipment` | Block | `{ ... }` |
| `TransformNow` | Enum/String | `Hitler` |
| `Trapper_Status` | Number | `1` |
| `TriggerDOTStatuses` | Number | `1, 0` |
| `TriggerGameEnding` | Number | `1` |
| `TriggerMotherConsume` | Number | `1` |
| `TriggerMotherGrow` | Number | `4` |
| `TriggerWerewolfTransform` | Array | `[ 1 .5 ], [ 1 .15 ], .5` |
| `TurnAround` | Number | `1` |
| `TurnControlDelay` | Enum/String | `.25` |
| `TurnRight` | Number | `1` |
| `TwisterDisplaceWithDamage` | Block | `{ ... }` |
| `UndoDamage` | Number | `1` |
| `UpgradeRandomAbility` | Number | `1` |
| `UseAbility` | Enum/String | `MD_PoopChain, ManglerThrowRemote, GirlDinoPoop` |
| `UseMoveAbilityWithAI` | Block | `{ ... }` |
| `VaporizeCorpseFlipAdvantage` | Array | `[ 1 .33 ]` |
| `VaporizeCorpse` | Number | `1` |
| `VaporizeDice` | Number | `1` |
| `VaporizeInanimate` | Number | `1` |
| `VaporizeTarget` | Number | `1` |
| `Vaporize` | Number | `1, 20` |
| `VisualCountDownThenApplyStatus` | Block | `{ ... }` |
| `VisualFXTile` | Enum/String | `PoisonPoof, WaterConduct, FireBlastSmall` |
| `VisualFX` | Enum/String | `Holyatk, MagicMissleBlast, WaterConduct` |
| `WaggleClone` | Block | `{ ... }` |
| `Weakness` | Number | `1, 2, [ 1 .25 ]` |
| `Webbed` | Number | `1` |

### Context: `empty_self_damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `effects` | Block | `{ ... }` |

### Context: `extra_statuses`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Number | `4` |
| `Poison` | Number | `1` |
| `Tarred` | Number | `2` |

### Context: `graphics`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `affected_animation` | Enum/String | `statDown` |
| `affected_particle` | Enum/String | `HealBig, HealMed, fx_tentaclestrangle` |
| `air_animation` | Enum/String | `entrance, gravitySlam_air, bellyflop_air` |
| `ally_animation` | Enum/String | `lickAttack` |
| `always_play_animations` | Boolean | `true` |
| `animate_name` | Enum/String | `pointout` |
| `animation_in` | Enum/String | `shadowStepIn, teleportIn, digUp` |
| `animation_out` | Enum/String | `digDown, teleportOut, shadowStepOut` |
| `animation` | Enum/String | `sing3, attack, none` |
| `aoe_spell_on_land` | Boolean | `true` |
| `apex_distance` | Number | `0.875` |
| `apex_time` | Enum/String | `.35` |
| `area_particle` | Enum/String | `none, BurnTrigger, FireBlastSmall` |
| `beam_cap` | Enum/String | `greenmegalasercap, thinlasercap, greenlasercap` |
| `beam_clip` | Enum/String | `greenlaser, greenmegalaser, thinlaser` |
| `bounce_on_hit` | Boolean | `false, true` |
| `bypass_combatspeed` | Boolean | `true` |
| `center_particle` | Enum/String | `Explosion, FireBlastMushroom, none` |
| `chain_distance` | Enum/String | `.25, .38` |
| `chain_movieclip` | Enum/String | `Frogchain, Bramblechain, ChainLink` |
| `custom_priming_animation` | Enum/String | `priming, idleCommand3, idleCommand2` |
| `damage_threshold_altanimations` | Block | `{ ... }` |
| `darken_screen_exclude_characters_on_tile` | Boolean | `false, true` |
| `darken_screen_exclude_self` | Boolean | `true` |
| `darken_screen_start_early` | Boolean | `true` |
| `darken_screen` | Boolean | `false, true` |
| `dash_animation` | Enum/String | `headbuttdash, roll, spinattackloop` |
| `dash_attack_animation` | Enum/String | `headbuttdashEnd, none, spinattackloop` |
| `dash_bonk_animation` | Enum/String | `bonk` |
| `dash_decelerating_animation` | Enum/String | `dashslow` |
| `dash_end_animation` | Enum/String | `launchStop, dashend, timberEnd` |
| `dash_start_animation` | Enum/String | `none, dashstart, headbuttdashStart` |
| `decelerate` | Number | `5` |
| `delay_from_map_center` | Boolean | `true` |
| `delay_from_map_edge` | Boolean | `false, true` |
| `delay_from_reverse_map_edge` | Boolean | `true` |
| `delay` | Number | `2, 5, 4` |
| `detatched_animation_cutoff` | Boolean | `true` |
| `detatched_animation_reach` | Number | `3, 4, 20` |
| `detatched_animation` | Enum/String | `LiquidMetalSpear, WaterGush, TinaSpear` |
| `do_animation_offscreen` | Boolean | `true` |
| `do_damage_immediately` | Boolean | `true` |
| `do_not_clear_placeholder` | Boolean | `true` |
| `dont_orient` | Boolean | `true` |
| `dont_visualize_ai` | Boolean | `true` |
| `easing` | Number | `1` |
| `empty_animation` | Enum/String | `empty` |
| `end` | Enum/String | `spinattackend, lickAttack, attack` |
| `face_targets` | Boolean | `true` |
| `face_toss_target` | Boolean | `true` |
| `fall_from_sky` | Boolean | `true` |
| `fall_randomize_timing` | Enum/String | `.3` |
| `first_castpoint_is_self_damage_only` | Boolean | `true` |
| `fixed_jump_height` | Number | `3.5, 1` |
| `fixed_jump_speed` | Number | `1, 2, .8` |
| `full_jump_animation` | Enum/String | `attack, jumpmove, jumpattack` |
| `full_jump_sync_frames` | Number | `38, 46, 49` |
| `full_jump_windup_frames` | Number | `13, 22, 20` |
| `fx_is_placeholder_animation` | Boolean | `true` |
| `fx_random_flip` | Boolean | `true` |
| `grab_animation` | Enum/String | `grab` |
| `hang_time` | Enum/String | `.6` |
| `ignore_slowtiles` | Boolean | `true` |
| `jump_attack_animation` | Enum/String | `land, gravitySlamEnd, block` |
| `jump_height_multiplier` | Number | `2, .25` |
| `jump_speed_multiplier` | Number | `1.5` |
| `jump_start_animation` | Enum/String | `gravitySlamStart, leapattackwindup, none` |
| `land_animation` | Enum/String | `none` |
| `lob_height` | Number | `1, 0, 4` |
| `lob_speed` | Enum/String | `.5` |
| `lob_yoff` | Enum/String | `-.5` |
| `lob` | Boolean | `false, true` |
| `lock_orientation_during_dash` | Boolean | `true` |
| `loop` | Enum/String | `lickAttack, attack, spinattackloop` |
| `mask_center` | Enum/String | `SpearMaskCenter` |
| `mask_extent` | Enum/String | `SpearMaskExtent` |
| `max_range` | Number | `3` |
| `max_throw_height` | Number | `1.75` |
| `max_tiles_single_loop` | Number | `1, 5, 6` |
| `min_range` | Number | `1` |
| `min_throw_height` | Number | `1.75, 0, 4` |
| `miss_particle` | Enum/String | `fx_tentaclestrangleMiss` |
| `miss_random_delay` | Array | `[ 0, 20 ], [ 0, 60 ]` |
| `mode` | Enum/String | `yeet` |
| `move_end_animation` | Enum/String | `none, buttScootEnd, endroll` |
| `move_start_animation` | Enum/String | `buttScootStart, none, startroll` |
| `othercat_placeholder_available` | Boolean | `true` |
| `palette` | Number | `6` |
| `particle_mat` | Enum/String | `shadow_occluded_spelldissolve` |
| `particle` | Enum/String | `PoisonPoof, none, None` |
| `precast_delay` | Enum/String | `.25` |
| `preturn_animation` | Enum/String | `alertstart` |
| `prime_animation` | Enum/String | `chargeholy, prouder, pointout` |
| `primed_alt_animation` | String | `"shootPrimed"` |
| `projectile` | Enum/String | `MagicSpikeProjectile, NeedleProjectile, LeechProjectile` |
| `pseudoprojectile` | Enum/String | `RocketFromAbove` |
| `random_delay` | Array | `[ 0, 120 ], [ 30 50 ], [ 70 100 ]` |
| `reverse_orientation` | Boolean | `true` |
| `rocket_swirl` | Block | `{ ... }` |
| `self_damage_mid_port` | Boolean | `true` |
| `single_projectile` | Boolean | `true` |
| `spawn_offset` | Array | `[ 0, .5, 0 ]` |
| `speed` | Number | `2, 20, .5` |
| `start` | Enum/String | `spinattackstart, attack, lickAttack` |
| `sync_frames` | Number | `26, 34` |
| `sync_speed` | Number | `22, 28, 30` |
| `throw_speed` | Number | `3` |
| `uncatchable` | Boolean | `true` |
| `use_directional_animations` | Boolean | `true` |
| `use_hit_alts` | Boolean | `false` |
| `use_origin_offsets` | Boolean | `false` |
| `use_placeholder` | Boolean | `true` |
| `use_projectile_spawn_offset` | Boolean | `true` |
| `use_projectile` | Boolean | `true` |
| `use_rotation_once` | Boolean | `true` |
| `use_rotation` | Boolean | `false` |
| `use_super_armor` | Boolean | `false, true` |
| `visual_delay_but_simultaneous_damage` | Number | `8, 0, 3` |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `3` |
| `BonusAbility` | Enum/String | `TinkererThrow, ThrowSpiritBomb, DonateEnergy` |
| `Brace` | Number | `1` |
| `Charmed` | Number | `1` |
| `DamageUp` | Number | `-1` |
| `Madness` | Number | `1` |
| `PermanentMadness` | Number | `1` |
| `RandomMagicMissile` | Number | `1` |
| `Shield` | Number | `5` |
| `TemporaryItem` | Number | `1` |
| `Webbed` | Number | `1` |

### Context: `meta`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability_icon` | Enum/String | `BasicRanged, BasicMelee, Pestilence` |
| `animate_name` | Boolean | `false, true` |
| `animation` | Enum/String | `portin` |
| `class` | Enum/String | `Hunter, Fighter, Mage` |
| `desc` | String | `"ABILITY_CROWNOFPESTILENCE_DESC", "nothing", "ABILITY_MELEEATTACK_DESC"` |
| `dont_visualize_ai` | Boolean | `true` |
| `icon_damage_display_eq` | Enum/String | `item_aux, "10+bonus_melee_ability_damage", "3+bonus_melee_ability_damage"` |
| `icon_damage_display_suffix` | String | `"x2", "x10"` |
| `icon_damage_display` | String | `"?", "1-6", "0-25"` |
| `icon_damage_type` | Enum/String | `magic, physical` |
| `icon_shell_frame` | Enum/String | `attack, multihit_attack, "attack"` |
| `is_basic_attack` | Boolean | `true` |
| `is_move` | Enum/String | `auto, true` |
| `is_trinket` | Boolean | `true` |
| `is_weapon` | Boolean | `true` |
| `name` | String | `"ABILITY_CROWNOFPESTILENCE_NAME", "None", "ABILITY_MELEEATTACK_NAME"` |
| `tooltip_values` | Array | `[ "X" ], [ "max((X-1)*2, 0)" ], [ "max(X*3, 0)" ]` |
| `type_icon` | String | `"defense", "unknown", "misc"` |

### Context: `post_spawn_statuses`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DoDamage` | Block | `{ ... }` |
| `EnterMount` | Enum/String | `enter` |
| `VisualFXTile` | Enum/String | `PoisonPoof` |

### Context: `rocket_swirl`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `radius` | Array | `[ .5 1 ], [ .25 .5 ]` |
| `speed` | Array | `[ .25, 1.0 ], [ 1.5, 2.5 ]` |

### Context: `self_damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai_base_score` | Number | `9999` |
| `cant_miss` | Boolean | `true` |
| `damage` | Number | `2, "floor(X*.25)", 0` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Water ], [ Explosion ], [ Fire ]` |
| `heal` | Number | `25, 8, 4` |
| `knockback` | Number | `1, -10, -3` |
| `non_lethal` | Boolean | `true` |
| `piercing` | Boolean | `true` |
| `type` | Enum/String | `melee, none, spell` |

### Context: `sounds`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `oncast` | Enum/String | `AbilitySnd_Assassinate, AbilitySnd_BoulderDrop` |
| `oncastpoint` | Enum/String | `AirHorn, Batterup_Swing_Castpoint` |
| `ontrigger_intentional` | Enum/String | `Lenny_HereKitty` |
| `ontrigger` | Enum/String | `Spawn_Donate, SE_BullRushDash, Spiderweb_Break` |

### Context: `spawn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `additional_passives` | Block | `{ ... }` |
| `ai_base_score` | Number | `999999, 9999, 99999` |
| `appearance` | Enum/String | `GolemCat` |
| `auto_cast_on_spawn` | Enum/String | `Dash_Enemy` |
| `catdata` | Enum/String | `teamclone, clone, item_aux_catid` |
| `chapter` | Enum/String | `alley` |
| `clone_items` | Boolean | `true` |
| `custom_additional_ai_weight` | Enum/String | `tile_exists` |
| `face_camera` | Boolean | `true` |
| `faction` | Enum/String | `self, default, solitary_enemies` |
| `first_turn` | Enum/String | `end_of_round, next_turn, initiative` |
| `include_passives` | Boolean | `true` |
| `inherit_elite_buffs` | Boolean | `false` |
| `layer` | Enum/String | `gas, pickups, characters` |
| `lob` | Boolean | `false` |
| `object` | Enum/String | `Food, RANDOM_1X1_ENEMY, PlayerCat_ThiefShade` |
| `post_spawn_statuses` | Block | `{ ... }` |
| `redirect_location_if_blocked` | Boolean | `true` |
| `size` | Number | `2` |
| `spawnin_animation` | Enum/String | `summonspawnin` |
| `start_dead` | Boolean | `true` |
| `trigger_battle_start` | Boolean | `true` |

### Context: `splash_damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai_base_score` | Number | `9999` |
| `crit_chance` | Number | `100` |
| `damage` | Number | `8, 0, 4` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Fire Napalm Explosion ], [ Water ], [ Fire Explosion ]` |
| `force_no_knockback` | Boolean | `true` |
| `force_play_hit_animation` | Boolean | `true` |
| `knockback` | Number | `1, 2, 0` |
| `layer` | Enum/String | `tiles` |
| `makes_contact` | Boolean | `false, true` |
| `override_trample_damage` | Boolean | `true` |
| `type` | Enum/String | `knockblock, spell, status_spell` |

### Context: `target`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `,` | Array | `[ 0, -1 ], [ 1, 1 ], [ 0, 1 ]` |
| `-1,` | Number | `1, -1, 0` |
| `-2,` | Number | `0` |
| `-3,` | Number | `0` |
| `-4,` | Number | `0` |
| `0,-1` | Flag | `N/A` |
| `0,` | Number | `1, -1, 0` |
| `1,-1` | Flag | `N/A` |
| `1,` | Number | `1, -1, 0` |
| `2,-1` | Flag | `N/A` |
| `2,` | Number | `1, 2, 0` |
| `3,-1` | Flag | `N/A` |
| `3,-2` | Flag | `N/A` |
| `3,` | Number | `1, -1, 0` |
| `4,` | Number | `0, 4` |
| `5,` | Number | `5` |
| `6,` | Number | `6` |
| `7,` | Number | `7` |
| `8,` | Number | `8` |
| `9,` | Number | `9` |
| `N` | Number | `5, 2, 3` |
| `X_is` | Enum/String | `current_health, turn_count, custom` |
| `adjust_target` | Enum/String | `stalk` |
| `allow_any_orientation` | Boolean | `true` |
| `allow_diagonal_passthrough` | Boolean | `true` |
| `allow_diagonals` | Boolean | `true` |
| `ally_priority` | Number | `1` |
| `always_bounce` | Boolean | `true` |
| `aoe_chance` | Enum/String | `.4+.2*level, .33, .5` |
| `aoe_considers_character_size` | Boolean | `false, true` |
| `aoe_display_exclude_restrictions` | Boolean | `true` |
| `aoe_excludes_self` | Boolean | `false, true` |
| `aoe_hint_teamcast` | Boolean | `true` |
| `aoe_leading_edge_only` | Boolean | `true` |
| `aoe_mode` | Enum/String | `standard, all, custom` |
| `aoe_restrictions` | Array | `[ exclude_blocking ], enemies_only, must_have_tag` |
| `aoe_rotate_around_character_center` | Boolean | `true` |
| `aoe_spell_on_land` | Boolean | `true` |
| `aoe_symmetry` | Enum/String | `eight_way, four_way, none` |
| `aoe_tile_requires_element` | Enum/String | `Water, Grass, Earth` |
| `as_the_crow_flies` | Boolean | `true` |
| `bonus_pathing_leniency` | Number | `4` |
| `can_multihit` | Boolean | `false, true` |
| `consider_trample` | Boolean | `false, true` |
| `corpse_priority` | Number | `5, 10` |
| `custom_aoe_mirror` | Array | `[ [ 1 0 ]` |
| `custom_aoe_util_mirror` | Array | `[ [ 1, 1 ]` |
| `custom_aoe_util` | Array | `[ [ -1, 1 ], [ [ 1, 1 ], [ [ 0, 1 ]` |
| `custom_aoe` | Array | `[ [ -1, 0 ], [ [ 1, -1 ], [ [ 1, 1 ]` |
| `custom_range` | Array | `[ [ 1 2 ], [ [ 1, 1 ], [ [ -2 0 ]` |
| `damage_collided_only` | Boolean | `true` |
| `delayed_trigger` | Boolean | `false, true` |
| `distance_sort_targets` | Number | `1, true` |
| `dont_orient_aoe` | Boolean | `true` |
| `dont_orient` | Boolean | `true` |
| `enemy_priority` | Number | `10` |
| `force_ai_target_as_spell` | Boolean | `true` |
| `force_no_contact` | Boolean | `true` |
| `hint_can_target_empty` | Boolean | `false, true` |
| `hint_can_target_pickups` | Boolean | `true` |
| `hint_can_target_static` | Boolean | `true` |
| `knockback_mode` | Enum/String | `zero, tile_to_target, tile_to_character` |
| `knockback_modifier` | Enum/String | `rotate_cw` |
| `lingering` | Boolean | `true` |
| `low_gravity_boostable` | Boolean | `false, true` |
| `low_health_character_threshold` | Enum/String | `item_aux, 5, 10` |
| `max_aoe` | Number | `1, 2, 0` |
| `max_bounces` | Number | `-1, 10, 3` |
| `max_range` | Number | `1, 5, 20` |
| `max_targets` | Number | `1, 15, 7` |
| `min_aoe` | Number | `1, 0, 2+size` |
| `min_range` | Number | `1, 2, 3` |
| `min_targets` | Number | `5, 1, 2` |
| `mirror_custom_aoe` | Boolean | `true` |
| `mouse_offset` | Array | `[ .5 .5 ]` |
| `multihit_max` | Number | `5, 10, 3` |
| `multihit_min` | Number | `1, 5, 3` |
| `multihit` | Number | `2, 5, 3` |
| `prioritize_change_direction` | Boolean | `true` |
| `prioritize_dont_change_direction` | Number | `1, true` |
| `prioritize_face_camera` | Number | `1, true` |
| `prioritize_throw_target_with_passive` | Enum/String | `NubbyTossPriority` |
| `randomize_knockback_direction_except_for_finisher` | Boolean | `true` |
| `randomize_target_within_range` | Number | `2, 0, 3` |
| `range_bonuses` | Enum/String | `include_alpha` |
| `range_considers_character_size` | Boolean | `false` |
| `range_display_include_aoe` | Boolean | `true` |
| `range_display_include_character_size` | Boolean | `true` |
| `range_display_include_direction` | Boolean | `true` |
| `range_excludes_blocking` | Boolean | `false, true` |
| `range_excludes_self` | Boolean | `false` |
| `range_max` | Number | `4` |
| `range_min` | Number | `1` |
| `range_mode` | Enum/String | `water_move, cross, standard` |
| `range_symmetry` | Enum/String | `eight_way` |
| `recalc_target_on_castpoint` | Boolean | `true` |
| `redirect_location_if_blocked` | Boolean | `true` |
| `remain_off_map` | Boolean | `true` |
| `reorient_thrown_character` | Boolean | `true` |
| `restrictions` | Enum/String | `aoe_must_exist, none, [ must_have_buddy must_have_living_character ]` |
| `restructions` | Enum/String | `aoe_must_exist` |
| `reverse_target_direction` | Boolean | `true` |
| `shotgun_mode` | Boolean | `true` |
| `shuffle_tile_order` | Boolean | `true` |
| `special_tile_tag` | Enum/String | `ChaosValidPosition, FinalBossCloneSpot, FinalBossTheChildLocation` |
| `spin_steps` | Number | `-16` |
| `splash_damage_aoe_begin` | Number | `1, 999` |
| `stagger_multihit_targets` | Boolean | `true` |
| `straight_shot` | Boolean | `false, true` |
| `target_mode` | Enum/String | `random_tile, direction8, none` |
| `target_requires_element` | Array | `[ grass ], [ grass water ]` |
| `target_requires_tag` | Enum/String | `bowling_ball, pickup, food` |
| `throw_consumed_character` | Boolean | `true` |
| `toss_direction_restriction` | Enum/String | `forwards, backwards` |
| `track_target` | Boolean | `true` |
| `trample_allies_too` | Boolean | `true` |
| `uncounterable` | Boolean | `true` |
| `upgrade_straight_shot_to_boomerang` | Boolean | `true` |
| `upgrade_straight_shot_to_piercing` | Boolean | `true` |

### Context: `temporary_effects`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AfterImage` | Block | `{ ... }` |
| `BearTrapTrail` | Number | `1` |
| `CastAgain` | Number | `1, 2, 4` |
| `DashFury` | Number | `4` |
| `DelayedWindTrail` | Number | `1` |
| `DisableTrample` | Number | `1` |
| `DoubleLoot` | Number | `1` |
| `Fury` | Number | `55, 75` |
| `JumpAttackLeaveBehind` | Enum/String | `BungaThrone` |
| `JustInCaseTrample` | Number | `0` |
| `KnockbackImmunity` | Number | `1` |
| `LeaveBehind` | Enum/String | `Bait, { ... }` |
| `TileTrail_Ahead` | Enum/String | `FlowerTile` |
| `TileTrail` | Enum/String | `BrambleTile, FlowerTile, FloatingGlassTile` |
| `Trample` | Number | `1, 4, 3` |

---

## Characters & Bosses

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `abilities` | Block | `{ ... }` |
| `ai_if_spawned_as_enemy` | Block | `{ ... }` |
| `ai` | Block | `{ ... }` |
| `alt_spawn_pool` | Block | `{ ... }` |
| `damage_instance` | Block | `{ ... }` |
| `equipment` | Block | `{ ... }` |
| `graphics` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |
| `properties` | Block | `{ ... }` |
| `scale` | Enum/String | `.5` |
| `sound` | Block | `{ ... }` |
| `stats` | Block | `{ ... }` |
| `variant_of` | Enum/String | `BirdSmall, BirdBase, Cherub` |

### Context: `0`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Number | `1` |
| `partial_animation_suffix` | Number | `1` |
| `passives` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1.4` |

### Context: `2`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Number | `2` |
| `attack` | Enum/String | `BasicMelee_2Hits, BoneWormShotMed` |
| `partial_animation_suffix` | Number | `2` |
| `passives` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `2.2` |

### Context: `3`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Number | `3` |
| `attack` | Enum/String | `BasicMelee_3Hits, BoneWormShotTall` |
| `partial_animation_suffix` | Number | `3` |
| `passives` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `3` |

### Context: `4`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Number | `4` |
| `attack` | Enum/String | `BasicMelee_4Hits` |
| `partial_animation_suffix` | Number | `4` |
| `passives` | Block | `{ ... }` |

### Context: `5`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `attack` | Enum/String | `BasicMelee_5Hits` |
| `partial_animation_suffix` | Number | `5` |
| `passives` | Block | `{ ... }` |

### Context: `AbilityHealthThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `DybbukPossess, FormShrinkThree, FormShrinkFour` |
| `also_use_if_buddy_is_dead` | Boolean | `true` |
| `even_if_stunned` | Boolean | `true` |
| `immediate` | Boolean | `true` |
| `threshold_min` | Enum/String | `X` |
| `threshold` | Number | `1, 3*champion_multiplier, 4*champion_multiplier` |
| `use_ai` | Boolean | `true` |

### Context: `AbilityOnRoundEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `DestroyerRaise` |
| `force_display_name` | Boolean | `true` |

### Context: `AbilityReaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |
| `ability` | Enum/String | `attack, MoonHandDash, ButtFlip` |
| `backstabs_only` | Boolean | `true` |
| `cancel_knockback` | Boolean | `true` |
| `enemies_only` | Boolean | `true` |
| `even_on_0_damage_if_knockback` | Boolean | `true` |
| `even_on_0_damage` | Boolean | `true` |
| `match_knockback_direction` | Boolean | `true` |
| `only_when_not_your_turn` | Boolean | `true` |
| `ranged_only` | Boolean | `true` |
| `verify_target` | Boolean | `true` |

### Context: `AbilityWhenTaggedCharacterMovesNear`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MoveTwo` |
| `range` | Number | `2, 4` |
| `tag` | Enum/String | `food` |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1, 2` |
| `Bruise` | Number | `1` |
| `Burn` | Number | `1, 2, 4` |
| `Confusion` | Number | `1` |
| `DamageUp` | Number | `-1` |
| `Fear` | Number | `1` |
| `GainDisorderFromPool` | Block | `{ ... }` |
| `Knockback` | Number | `3` |
| `Leech` | Number | `2` |
| `Madness` | Number | `1` |
| `Poison` | Number | `1` |
| `Possessed` | Number | `1` |
| `RandomStatUp` | Number | `-1` |
| `RemoteFlatLeech` | Number | `1` |
| `RemoteLeech` | Number | `1` |
| `Rot` | Number | `1` |
| `Slow` | Number | `1` |
| `Stun` | Number | `1` |
| `Weakness` | Number | `1` |

### Context: `AddStatusToReceivedDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_IsPhysicalAttack` | Block | `{ ... }` |
| `Else` | Block | `{ ... }` |

### Context: `AddStatusToSpells`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Leech` | Number | `2` |

### Context: `AddStatusToTrampleDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bruise` | Number | `1` |

### Context: `AddStatusToWeapons`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |

### Context: `AddTemporaryEffectsToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Fury` | Number | `75` |

### Context: `AdventureTokenPassivePool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `StacyMutant_Brace` | Block | `{ ... }` |
| `StacyMutant_Counter` | Block | `{ ... }` |
| `StacyMutant_Damage` | Block | `{ ... }` |
| `StacyMutant_DoubleHead` | Block | `{ ... }` |
| `StacyMutant_Fire` | Block | `{ ... }` |
| `StacyMutant_Health` | Block | `{ ... }` |
| `StacyMutant_Holy` | Block | `{ ... }` |
| `StacyMutant_Ice` | Block | `{ ... }` |
| `StacyMutant_Lightning` | Block | `{ ... }` |
| `StacyMutant_Mirror` | Block | `{ ... }` |
| `StacyMutant_Speed` | Block | `{ ... }` |
| `StacyMutant_Thorns` | Block | `{ ... }` |

### Context: `AggroTargetIsGovernedByHitEffect`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `enemies_only` | Boolean | `false` |

### Context: `Alert`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | Enum/String | `Alert` |
| `passives` | Block | `{ ... }` |

### Context: `AllAlive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `AllStatsAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `aura_requires_tag` | Enum/String | `humanoid` |
| `range` | Enum/String | `global` |
| `stacks` | Number | `1` |

### Context: `Angry`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | String | `"Angry"` |

### Context: `ArmorPickup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `frame_range` | Array | `[ 6 6 ], [ 3 5 ], [ 1 2 ]` |
| `stacks` | Number | `6, 2, 4` |

### Context: `Attacker`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `ZombieTombstone` |
| `even_if_stunned` | Boolean | `true` |

### Context: `BackflipWhenTargeted`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `BackflipDodge` |
| `stacks` | Number | `1` |

### Context: `BaitAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `range` | Number | `3` |

### Context: `BattlefieldUniqueRandomPassive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | `1` |
| `DemonicGlyph_Bounce` | Number | `1` |
| `DemonicGlyph_Fire` | Number | `1` |
| `DemonicGlyph_Movement` | Number | `1` |
| `DemonicGlyph_Summon` | Number | `1` |

### Context: `BellyFull`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | String | `"Belly"` |
| `passives` | Block | `{ ... }` |

### Context: `Big`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `Big, "Big"` |
| `attack` | Enum/String | `GameteSpawn` |
| `passives` | Block | `{ ... }` |

### Context: `BigHolding`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHolding"` |
| `passives` | Block | `{ ... }` |

### Context: `BigHoldingCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHoldingCat"` |
| `passives` | Block | `{ ... }` |

### Context: `BirdRewards`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ally_rewards` | Block | `{ ... }` |
| `statuses` | Block | `{ ... }` |

### Context: `Bishop`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Bishop"` |
| `attack` | Enum/String | `BBXLightning` |
| `name` | String | `"ENEMY_CULTISTBISHOP_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CULTISTBISHOP_DESC"` |
| `turns` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `2.5` |

### Context: `BlackHole`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"BlackHole"` |
| `name` | String | `"OBJECT_BLACKHOLE_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"OBJECT_BLACKHOLE_DESC"` |

### Context: `Bomb`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Button` |
| `passives` | Block | `{ ... }` |

### Context: `Boris`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |
| `passives` | Block | `{ ... }` |

### Context: `BossRewards`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `common` | Enum/String | `Blubber, RatBomb, ChubsCollar` |
| `rare` | Enum/String | `SpiderBaby, RadGlasses, BorisBrain` |

### Context: `Buddy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `allies_only` | Boolean | `false` |
| `obj` | Enum/String | `ZaratanaVS, PyrophinaVS, Dice` |
| `reclaim_if_lost` | Boolean | `true` |

### Context: `Bully`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `BungaCheers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ally_damage` | Enum/String | `littleboo` |
| `ally_dead` | Enum/String | `bigboo` |
| `enemy_damage` | Enum/String | `littlecheer` |
| `enemy_dead` | Enum/String | `bigcheer` |
| `warrior_tag` | Enum/String | `bungawarrior` |

### Context: `BungaEntrance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `BecomeTheDestroyer, BungaEntrance` |
| `even_if_stunned` | Boolean | `true` |
| `health_threshold` | Number | `150, -1` |
| `warrior_tag` | Enum/String | `finalboss_clonecat, bungawarrior` |

### Context: `Cat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `spawnHoldingCat` |
| `formchange` | Enum/String | `SmallHoldingCat, BigHoldingCat` |
| `statuses` | Block | `{ ... }` |

### Context: `CatPartsTransform`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `arm1` | Number | `1044, 1043, 1045` |
| `arm2` | Number | `1044, 1043, 1045` |
| `body` | Number | `1024, 1013, 1012` |
| `ear1` | Number | `1028, 1013, 1029` |
| `ear2` | Number | `1013` |
| `eye1` | Number | `1013, 1057` |
| `eye2` | Number | `1013, 1057` |
| `head` | Number | `1020, 1019, 1027` |
| `leg1` | Number | `1044, 1043, 1045` |
| `leg2` | Number | `1044, 1043, 1045` |
| `palette` | Enum/String | `Hunter, Fighter, Mage` |
| `tail` | Number | `1034, 1035, 1036` |
| `texture` | Number | `19, 29, 60` |

### Context: `CaveBaby`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"CaveBaby"` |
| `attack` | Enum/String | `CaveBabyMelee` |
| `name` | String | `"ENEMY_CAVEBABY_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CAVEBABY_DESC"` |

### Context: `CaveFamilyEnrage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `CaveCatEnrageTwo, CaveCatEnrageOne` |
| `count` | Number | `1, 0` |
| `tag` | Enum/String | `cavefamily` |

### Context: `CaveMan`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"CaveMan"` |
| `attack` | Enum/String | `CaveMan3HitCombo` |
| `name` | String | `"ENEMY_CAVEMANMAN_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CAVEMANMAN_DESC"` |

### Context: `CaveManSpear`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"SpearCaveMan"` |
| `attack` | Enum/String | `CaveManThrowSpear` |
| `name` | String | `"ENEMY_SPEARCAVEMAN_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_SPEARCAVEMAN_DESC"` |

### Context: `CaveWoman`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"CaveWoman"` |
| `attack` | Enum/String | `CaveWomanKick` |
| `name` | String | `"ENEMY_CAVEMANWOMAN_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN_DESC"` |

### Context: `CaveWomanHasCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"CatCaveWoman"` |
| `attack` | Enum/String | `CaveWomanCatSlap` |
| `name` | String | `"ENEMY_CAVEMANWOMAN2_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN2_DESC"` |

### Context: `CerberubsAggroTargetBehavior`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `alert_form` | Enum/String | `Alert` |
| `default_form` | Enum/String | `Normal` |

### Context: `CerberubsJumpBlind`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `CerberubsJump` |
| `decision_weights` | Enum/String | `nubs_fakeblind` |

### Context: `CerberubsJumpNormal`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `CerberubsJump` |
| `decision_weights` | Enum/String | `default` |

### Context: `ChanceToBackflip`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `DybbukBackflipDodge` |
| `chance` | Number | `100%` |

### Context: `ChanceToFormChangeOnAbilityDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `15%` |
| `form` | Enum/String | `Flop2` |

### Context: `ChanceToSpitOnDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MoonHandDrop, TinaSpit, PteroEscape` |
| `backstabs_only` | Boolean | `true` |
| `chance_per_damage` | Number | `0%, 2%` |
| `even_on_0_damage_if_knockback` | Boolean | `true` |
| `flat_chance` | Number | `100%, 50%` |

### Context: `ChaosBossFormChangeGuide`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `active_pieces` | Array | `[ Johnny Throb Flush ]` |
| `passive_pieces` | Array | `[ Host Nettle Bubs ]` |
| `passives_health_threshold` | Number | `50%` |

### Context: `ChaosBossPieces`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `active_pieces` | Array | `[ Johnny Throb Flush ]` |
| `passive_pieces` | Array | `[ Host Nettle Bubs ]` |

### Context: `ChaosHeadDropIn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `ChaosSpawnIn` |
| `new_music` | Enum/String | `chaos_boss_part2` |
| `tag` | Enum/String | `riftheadguardian` |

### Context: `CharacterLightSource`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `color` | Array | `[ .8, .9, 1 ], [ .7, .8, .9 ], [ .3, .7, 1 ]` |
| `glow` | Array | `[ 1, 1, 1, .5 ], [ .7, .8, .9, .5 ], [ .3, .7, 1, .5 ]` |
| `size` | Number | `2, 1.5, 4` |

### Context: `Charging`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `MoonHead_Blow` |
| `partial_animation_suffix` | String | `"Charging"` |
| `passives` | Block | `{ ... }` |

### Context: `CherubimReaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Leave` | Enum/String | `LELeave, CherubimLeave` |
| `Return` | Enum/String | `LEReturn, CherubimReturn` |

### Context: `Close`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `CloseConvert`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MarshmallowConvert` |
| `move_weights` | Enum/String | `stay_close` |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Madness` | Number | `1` |
| `odds` | Number | `0.5` |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FindItemFromPool` | Enum/String | `chapter` |
| `odds` | Number | `5%, 33%` |

### Context: `Conditional_HasKnockback`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `KnockUpAndAway` | Block | `{ ... }` |
| `RemoveKnockback` | Number | `1` |
| `TempPassiveUntilSettled` | Block | `{ ... }` |

### Context: `Conditional_IsPhysicalAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `KnockUpAndAway` | Block | `{ ... }` |
| `RemoveKnockback` | Number | `1` |
| `TempPassiveUntilSettled` | Block | `{ ... }` |

### Context: `Consumed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_not_pop_corpse` | Boolean | `true` |
| `drop_on_death` | Enum/String | `deferred` |
| `force_contact` | Boolean | `true` |
| `instant` | Boolean | `true` |
| `mount_mode` | Enum/String | `auto` |
| `struggle_ability` | Enum/String | `Thrash` |
| `use_placeholder` | Boolean | `true` |

### Context: `CounterAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `StegoTailSwipe` |
| `without_orienting` | Boolean | `true` |

### Context: `CreateGlobalModifiers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BloodRain` | Number | `1` |
| `LowerAmbientLight` | Block | `{ ... }` |

### Context: `Cultist`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Cultist"` |
| `attack` | Enum/String | `BasicMelee` |
| `name` | String | `"ENEMY_CULTISTLACKEY_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CULTISTLACKEY_DESC"` |

### Context: `Damaged`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `DashRandomly`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `ShamblerDash` |
| `decision_weights` | Enum/String | `blind` |

### Context: `DeathRattle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `UFO_SpelunkyDeath, JarHeadDeath, MoonHandDrop_Deathrattle` |
| `cancel_knockback` | Boolean | `true` |
| `immediate` | Boolean | `true` |
| `is_dying_animation` | Boolean | `true` |
| `must_target_killer` | Boolean | `true` |
| `pop_corpse` | Boolean | `false` |
| `target_killer` | Boolean | `true` |

### Context: `DeathRattleRevive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `HitlerPulp1, AZ_LoseHead, HitlerPulp2` |
| `even_if_stunned` | Boolean | `true` |

### Context: `Default`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `LennyShove` |
| `move` | Enum/String | `LennyTrampleMove` |
| `partial_animation_suffix` | String | `""` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Default_Ceiling`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Default_Ground`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `DelayedAutoRevive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `health` | Number | `50%` |
| `rounds` | Number | `1` |

### Context: `DesireMech`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `DiceBehavior`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `dice_size` | Number | `6` |
| `knockback_damage` | Number | `5` |

### Context: `Die`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `DiesToElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Fire` |
| `instant` | Boolean | `true` |

### Context: `DiesToPiercingAndSpikes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `deferred` | Boolean | `true` |

### Context: `DodgeWhenTargeted`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `ShadowstepDodge` |

### Context: `Down`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Down"` |
| `attack` | Enum/String | `ButtFart` |
| `move` | Enum/String | `TeleportFlipUp` |
| `passives` | Block | `{ ... }` |

### Context: `Drunker`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Drunk` |

### Context: `DualSword`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"2"` |
| `attack` | Enum/String | `DestroyerAttack2` |
| `move_speed_multiplier` | Number | `1.5` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |

### Context: `DualSword_Primed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Holy2"` |
| `attack` | Enum/String | `DestroyerAttack2` |
| `move_speed_multiplier` | Number | `1.5` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |

### Context: `Dumb`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `DybbukPossessionFallback`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit_ability` | Enum/String | `DybbukReturn` |
| `form` | Enum/String | `Possessing` |

### Context: `Else`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_HasKnockback` | Block | `{ ... }` |

### Context: `Empty`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `""` |

### Context: `Escape`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `DybbukEscape` |
| `move_weights` | Enum/String | `keep_distance_always_move` |

### Context: `Explody`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Expl` |
| `attack` | Enum/String | `ToxExplode` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |

### Context: `Explosive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"3"` |
| `passives` | Block | `{ ... }` |

### Context: `FaceAwayLastDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |
| `override_hit_animation` | Boolean | `true` |
| `use_turn_animations` | Boolean | `true` |

### Context: `FaceLastDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `use_turn_animations` | Boolean | `true` |

### Context: `FightPhase`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `T3Shoot` |
| `move` | Enum/String | `FloatMove` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `FinalBossBeamQueue`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `queue` | Enum/String | `TheChild_TargetBeam` |
| `release` | Enum/String | `TheChild_ReleaseBeams` |
| `transform` | Enum/String | `TheChild_TransformBoris` |

### Context: `FinalBossBecomeTheChild`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `GlobalSpawnCharacter` | Enum/String | `MegaGuppy` |
| `PlayBackground` | Number | `1` |
| `SwitchMusic` | Block | `{ ... }` |

### Context: `FinalBossHitCountdownBoris`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `TheChild_TransformExplosive, { ... }` |
| `icon_ready` | Number | `803` |
| `icon` | Number | `802` |
| `stacks` | Number | `7` |

### Context: `FinalBossHitCountdownExplosive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `TheChild_TransformHoly, { ... }` |
| `icon_ready` | Number | `801` |
| `icon` | Number | `800` |
| `stacks` | Number | `7` |

### Context: `FinalBossHitCountdownHoly`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `icon_ready` | Number | `805` |
| `icon` | Number | `804` |
| `stacks` | Number | `7` |

### Context: `FinalBossPupils`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `look_at_offset` | Array | `[ 0 2.5 0 ]` |
| `radius` | Number | `13` |
| `reset_center_because_no_target_halflife` | Enum/String | `.1` |
| `reset_center_because_of_animation_halflife` | Enum/String | `.05` |
| `teleport_tracking_halflife` | Enum/String | `.01` |
| `tracking_acquisition_halflife` | Enum/String | `.1` |
| `virtual_head_position` | Array | `[ 11 2 11 ]` |

### Context: `FinalBossShieldHealth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `break_ability` | Enum/String | `DestroyerBreakShield` |
| `state_health` | Array | `[ 0 35 35 35 35 0 ]` |

### Context: `FinalBossSyncAnimations`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `other_character` | Enum/String | `MegaGuppy` |
| `other_form_change_abilities` | Block | `{ ... }` |

### Context: `Fire`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `SpewerLobbed_Lava` |
| `passives` | Block | `{ ... }` |

### Context: `FireFull`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Full` |
| `attack` | Enum/String | `SpewerSpit` |
| `passives` | Block | `{ ... }` |

### Context: `Flop`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Down"` |
| `passives` | Block | `{ ... }` |

### Context: `Flop2`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Down"` |
| `passives` | Block | `{ ... }` |

### Context: `Flush`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `FlushBubs`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `FlushHost`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | Enum/String | `Host` |
| `passives` | Block | `{ ... }` |

### Context: `FlushNettle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `FoodMove`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `CaveBabyFoodMove` |
| `move_weights` | Enum/String | `stay_close_move_if_possible` |

### Context: `ForceTrample`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `BirthwortTrample` |
| `decision_weights` | Enum/String | `always_cast_careless` |

### Context: `ForceUseAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `TheChild_Wrath, TheChild_Pulse` |
| `show_name` | Boolean | `true` |

### Context: `FormChangeDuringWeatherElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Water` |
| `form` | Enum/String | `Rain` |

### Context: `FormChangeHealthThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count_shield` | Boolean | `true` |
| `form_above` | Enum/String | `Full, Default, Standing` |
| `form_below` | Enum/String | `Standing2, DesireMech, Damaged` |
| `threshold` | Number | `25, 50, X-4` |

### Context: `FormChangeOffMap`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `form_offmap` | Enum/String | `Start_Ceiling, Default_Ceiling, Insane_Ceiling` |
| `form_onmap` | Enum/String | `Default_Ground, Default, Insane_Ground` |

### Context: `FormChangeOnElementInfluence`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `wind, very_hot, water` |
| `exclude` | Enum/String | `fire, water` |
| `form` | Enum/String | `hot, Unlit, default` |
| `particle` | Enum/String | `FireExtinguish` |
| `sfx` | Enum/String | `FireExtinguish` |

### Context: `FormChangeWhileHasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `form_has` | Enum/String | `Full, HasRock, HasCat` |
| `form_hasnot` | Enum/String | `Default, Small, Big` |
| `status` | Enum/String | `Consuming, Grappling, Counterspell` |

### Context: `FormChangeWhilePrimingAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `not_priming` | Enum/String | `SwordAndShield, DualSword, NotPriming` |
| `priming` | Enum/String | `SwordAndShield_Primed, Priming, DualSword_Primed` |

### Context: `FormChanger`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Alert` | Block | `{ ... }` |
| `AllAlive` | Block | `{ ... }` |
| `Angry` | Block | `{ ... }` |
| `Attacker` | Block | `{ ... }` |
| `BellyFull` | Block | `{ ... }` |
| `BigHoldingCat` | Block | `{ ... }` |
| `BigHolding` | Block | `{ ... }` |
| `Big` | Block | `{ ... }` |
| `Bishop` | Block | `{ ... }` |
| `BlackHole` | Block | `{ ... }` |
| `Bomb` | Block | `{ ... }` |
| `Boris` | Block | `{ ... }` |
| `Bully` | Block | `{ ... }` |
| `Butcher` | Block | `{ ... }` |
| `CaveBaby` | Block | `{ ... }` |
| `CaveManSpear` | Block | `{ ... }` |
| `CaveMan` | Block | `{ ... }` |
| `CaveWomanHasCat` | Block | `{ ... }` |
| `CaveWoman` | Block | `{ ... }` |
| `Charging` | Block | `{ ... }` |
| `Close` | Block | `{ ... }` |
| `Colorless` | Block | `{ ... }` |
| `Cultist` | Block | `{ ... }` |
| `Damaged` | Block | `{ ... }` |
| `Default_Ceiling` | Block | `{ ... }` |
| `Default_Ground` | Block | `{ ... }` |
| `Default` | Block | `{ ... }` |
| `DesireMech` | Block | `{ ... }` |
| `Die` | Block | `{ ... }` |
| `Down` | Block | `{ ... }` |
| `Druid` | Block | `{ ... }` |
| `Drunker` | Block | `{ ... }` |
| `DualSword_Primed` | Block | `{ ... }` |
| `DualSword` | Block | `{ ... }` |
| `Dumb` | Block | `{ ... }` |
| `Empty` | Block | `{ ... }` |
| `Explody` | Block | `{ ... }` |
| `Explosive` | Block | `{ ... }` |
| `FightPhase` | Block | `{ ... }` |
| `Fighter` | Block | `{ ... }` |
| `FireFull` | Block | `{ ... }` |
| `Fire` | Block | `{ ... }` |
| `Flop2` | Block | `{ ... }` |
| `Flop` | Block | `{ ... }` |
| `FlushBubs` | Block | `{ ... }` |
| `FlushHost` | Block | `{ ... }` |
| `FlushNettle` | Block | `{ ... }` |
| `Flush` | Block | `{ ... }` |
| `Full` | Block | `{ ... }` |
| `Grappling` | Block | `{ ... }` |
| `Grown` | Block | `{ ... }` |
| `GuaranteedJackpot` | Block | `{ ... }` |
| `Guarding` | Block | `{ ... }` |
| `HalfDead` | Block | `{ ... }` |
| `HasCat` | Block | `{ ... }` |
| `HasDeadCat` | Block | `{ ... }` |
| `HasRock` | Block | `{ ... }` |
| `Headless` | Block | `{ ... }` |
| `Hint_CrackedVisuals2` | Block | `{ ... }` |
| `Hint_CrackedVisuals3` | Block | `{ ... }` |
| `Hint_CrackedVisuals` | Block | `{ ... }` |
| `Holding` | Block | `{ ... }` |
| `Holy` | Block | `{ ... }` |
| `HumanDead` | Block | `{ ... }` |
| `Hunter` | Block | `{ ... }` |
| `InitialPhase` | Block | `{ ... }` |
| `Insane_Ceiling` | Block | `{ ... }` |
| `Insane_Ground` | Block | `{ ... }` |
| `JohnnyBubs` | Block | `{ ... }` |
| `JohnnyHost` | Block | `{ ... }` |
| `JohnnyNettle` | Block | `{ ... }` |
| `Johnny` | Block | `{ ... }` |
| `Joystick` | Block | `{ ... }` |
| `LastHit` | Block | `{ ... }` |
| `Lifted` | Block | `{ ... }` |
| `Lit` | Block | `{ ... }` |
| `Mage` | Block | `{ ... }` |
| `Medic` | Block | `{ ... }` |
| `Monk` | Block | `{ ... }` |
| `Mounted` | Block | `{ ... }` |
| `MouthFull` | Block | `{ ... }` |
| `Mutant` | Block | `{ ... }` |
| `Necromancer` | Block | `{ ... }` |
| `NeutronStar` | Block | `{ ... }` |
| `NoDeathRattle` | Block | `{ ... }` |
| `NoEyes` | Block | `{ ... }` |
| `NoStick` | Block | `{ ... }` |
| `NormalFull` | Block | `{ ... }` |
| `Normal` | Block | `{ ... }` |
| `NotPriming` | Block | `{ ... }` |
| `Nuke` | Block | `{ ... }` |
| `Obey` | Block | `{ ... }` |
| `OffMap` | Block | `{ ... }` |
| `OffScreen` | Block | `{ ... }` |
| `Off` | Block | `{ ... }` |
| `OneAlive` | Block | `{ ... }` |
| `OneEye` | Block | `{ ... }` |
| `OpenCat` | Block | `{ ... }` |
| `Open` | Block | `{ ... }` |
| `Out` | Block | `{ ... }` |
| `Possessing` | Block | `{ ... }` |
| `Primed` | Block | `{ ... }` |
| `Priming` | Block | `{ ... }` |
| `Psychic` | Block | `{ ... }` |
| `Pulp2` | Block | `{ ... }` |
| `Pulp3` | Block | `{ ... }` |
| `Pulp4` | Block | `{ ... }` |
| `Pulp5` | Block | `{ ... }` |
| `Pulp6` | Block | `{ ... }` |
| `Pulp7` | Block | `{ ... }` |
| `Rage` | Block | `{ ... }` |
| `Rain` | Block | `{ ... }` |
| `Sitting` | Block | `{ ... }` |
| `SmallHoldingCat` | Block | `{ ... }` |
| `SmallHolding` | Block | `{ ... }` |
| `Small` | Block | `{ ... }` |
| `SpawningPhase` | Block | `{ ... }` |
| `SquirrelForm` | Block | `{ ... }` |
| `Standing2` | Block | `{ ... }` |
| `Standing` | Block | `{ ... }` |
| `Start_Ceiling` | Block | `{ ... }` |
| `Stop` | Block | `{ ... }` |
| `SwordAndShield_Primed` | Block | `{ ... }` |
| `SwordAndShield` | Block | `{ ... }` |
| `Tank` | Block | `{ ... }` |
| `TarFull` | Block | `{ ... }` |
| `Tar` | Block | `{ ... }` |
| `Thief` | Block | `{ ... }` |
| `ThrobBubs` | Block | `{ ... }` |
| `ThrobHost` | Block | `{ ... }` |
| `ThrobNettle` | Block | `{ ... }` |
| `Throb` | Block | `{ ... }` |
| `Tinkerer` | Block | `{ ... }` |
| `Transformed` | Block | `{ ... }` |
| `Turtled` | Block | `{ ... }` |
| `TwoAlive` | Block | `{ ... }` |
| `TwoEyes` | Block | `{ ... }` |
| `Unlit` | Block | `{ ... }` |
| `Unmounted` | Block | `{ ... }` |
| `Unwashed` | Block | `{ ... }` |
| `Up` | Block | `{ ... }` |
| `Washed` | Block | `{ ... }` |
| `Washer` | Block | `{ ... }` |
| `Water` | Block | `{ ... }` |
| `WereMan` | Block | `{ ... }` |
| `ZealotBomb` | Block | `{ ... }` |
| `Zealot` | Block | `{ ... }` |
| `active` | Block | `{ ... }` |
| `default` | Block | `{ ... }` |
| `hot` | Block | `{ ... }` |
| `initial_form` | Enum/String | `Default, Flop, Up` |
| `passive` | Block | `{ ... }` |
| `sync_brain_patterns` | Boolean | `true` |

### Context: `Full`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Full"` |
| `attack` | Enum/String | `KirbySpit` |
| `passives` | Block | `{ ... }` |
| `statuses_on_enter_form` | Block | `{ ... }` |

### Context: `GainDisorderFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.1` |
| `pool` | Enum/String | `diseases` |

### Context: `Grappling`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit_animations` | Block | `{ ... }` |
| `partial_animation_suffix` | Enum/String | `Grapple` |

### Context: `Grown`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Grown` |
| `attack` | Enum/String | `HitlerCloneSwipes` |
| `name` | String | `"ENEMY_HITLERCLONE_NAME"` |
| `passives` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1.5` |
| `weak_threshold` | Number | `15` |

### Context: `GuaranteedJackpot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `Guarding`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | String | `"Guarding"` |
| `passives` | Block | `{ ... }` |

### Context: `HPAltStates`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `clipname` | Enum/String | `poopmain` |
| `thresholds` | Array | `[ [ 1 0 ]` |

### Context: `HalfDead`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"2"` |
| `attack` | Enum/String | `RatKingDash` |
| `passives` | Block | `{ ... }` |

### Context: `HasCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Grabbing", "Cat"` |
| `attack` | Enum/String | `MoonHead_ChewCat, PteroPeck, MoonHandSqueeze` |
| `move` | Enum/String | `None` |
| `partial_animation_suffix` | String | `"Swallowed"` |
| `passives` | Block | `{ ... }` |

### Context: `HasDeadCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"CatDead"` |
| `attack` | Enum/String | `LennyCatSlap` |
| `passives` | Block | `{ ... }` |

### Context: `HasRock`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"rock"` |
| `attack` | Enum/String | `AmoebaRockBash` |

### Context: `Headless`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Headless"` |
| `passives` | Block | `{ ... }` |

### Context: `HealNeighborsEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |
| `stacks` | Number | `3` |

### Context: `HealthPickup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `anything_eats` | Boolean | `true` |
| `force_frame` | Number | `12` |
| `frame_range` | Array | `[ 3 4 ], [ 5 5 ], [ 1 2 ]` |
| `stacks` | Number | `7, 4, 10` |
| `stored_food_value` | Number | `1, 2, 3` |

### Context: `Hint_CrackedVisuals`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"Cracked"` |

### Context: `Hint_CrackedVisuals2`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"ChargingCracked"` |

### Context: `Hint_CrackedVisuals3`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"SwallowedCracked"` |

### Context: `HitlerExecute`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `HitlerShoot` |
| `tag` | Enum/String | `grown_hitler_clone` |
| `threshold` | Number | `15` |

### Context: `Holding`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | String | `"Holding"` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Holy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |
| `passives` | Block | `{ ... }` |

### Context: `HumanDead`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `DH` |
| `attack` | Enum/String | `HCSpin` |
| `tooltip` | String | `"ENEMY_HUMANCAT2_DESC"` |

### Context: `ImmediateAbilityReaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |
| `ability` | Enum/String | `ButtWeb, ButtWeb_AlreadyEnraged, AlienBeastGoop` |
| `backstabs_only` | Boolean | `true` |
| `buddy_damage_only` | Boolean | `true` |
| `damage_threshold` | Number | `10` |
| `even_if_blocked` | Boolean | `true` |
| `even_if_stunned` | Boolean | `true` |
| `health_threshold` | Number | `70, 50` |
| `target_furthest_valid` | Boolean | `true` |

### Context: `InfiniteRebirth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `health` | Number | `25%` |
| `immediate` | Boolean | `true` |
| `playercat_health` | Number | `25%` |

### Context: `InitialPhase`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `T3Shoot` |
| `move` | Enum/String | `FloatMove` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Insane_Ceiling`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Insane"` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Insane_Ground`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Insane"` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Johnny`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `JohnnyBubs`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `JohnnyHost`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | Enum/String | `Host` |
| `passives` | Block | `{ ... }` |

### Context: `JohnnyNeedsWashing`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `form_unwashed` | Enum/String | `Unwashed` |
| `form_washed` | Enum/String | `Washed` |

### Context: `JohnnyNettle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `Joystick`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"Joystick"` |
| `passives` | Block | `{ ... }` |

### Context: `KnockUpAndAway`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `displace` | Boolean | `true` |
| `distance` | Number | `3` |
| `self_damage` | Boolean | `false` |
| `stacks` | Number | `5` |

### Context: `LastHit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `turns` | Block | `{ ... }` |

### Context: `LeapClose`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `GKLeap` |
| `move_weights` | Enum/String | `towards_aggro` |

### Context: `Lifted`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"Lift"` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Lit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Lit` |
| `passives` | Block | `{ ... }` |

### Context: `LowerAmbientLight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `amount` | Array | `[ 50% 60% 60% ]` |
| `speed` | Number | `4` |

### Context: `ManaPickup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `frame_range` | Array | `[ 6 6 ], [ 3 5 ], [ 1 2 ]` |
| `stacks` | Number | `6, 2, 4` |

### Context: `MegaDinoDropController`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `head_drop` | Enum/String | `MD_HeadDrop` |
| `leg_leave` | Enum/String | `MD_LegLeave` |
| `leg_return` | Enum/String | `MD_LegReturn` |
| `stable_legs` | Number | `3` |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |
| `damage` | Number | `5, 0` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Fire ]` |
| `knockback` | Number | `2, 4, 3` |
| `type` | Enum/String | `none, status` |

### Context: `ModularPickup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Cleanse` | Number | `0` |
| `sound_event` | Enum/String | `EatAntidote` |

### Context: `MonkCatReactionAbilities`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `attack` | Enum/String | `attack` |
| `move` | Enum/String | `move` |
| `spell` | Enum/String | `MCHadouken` |
| `trinket` | Enum/String | `MCHadouken` |
| `weapon` | Enum/String | `attack` |

### Context: `MotherGrowController`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `eat_damage` | Block | `{ ... }` |
| `tumor_object` | Enum/String | `MotherTumor` |

### Context: `MotherTumorPassive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Cat` | Block | `{ ... }` |
| `NonCat` | Block | `{ ... }` |
| `considered_forms` | Array | `[ Big BigHolding BigHoldingCat ]` |
| `grow_ability` | Enum/String | `MotherTumorGrow` |
| `pass_ani` | Enum/String | `pass` |
| `receive_ani` | Enum/String | `receive` |

### Context: `MotherTumorSpawnInCapture`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Cat` | Block | `{ ... }` |
| `NonCat` | Block | `{ ... }` |
| `Nothing` | Block | `{ ... }` |

### Context: `Mount`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `eject_ability` | Enum/String | `MechSuitEject` |
| `enter_ability` | Enum/String | `EnterMech` |

### Context: `Mounted`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"Cat"` |

### Context: `MouthFull`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | String | `"MouthFull"` |
| `passives` | Block | `{ ... }` |

### Context: `MoveAfterAnyAttemptedAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `weights` | Enum/String | `bat_chaos_runaway` |

### Context: `MoveAway`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MoveTwoCantrip, DoubleDistanceMove, ExtraMove` |
| `move_weights` | Enum/String | `keep_distance_always_move, stay_far, blind_move_far` |

### Context: `MoveAwayFromDamageSource`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `move_ability` | Enum/String | `BirdFly` |

### Context: `MoveAwayWhenEnemyAdjacent`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `move_ability` | Enum/String | `YA_Jetpack` |
| `once_per_turn` | Boolean | `true` |
| `weights` | Enum/String | `stay_far_always_move` |

### Context: `MoveCenter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_weights` | Enum/String | `stay_near_map_center` |

### Context: `MoveClose`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_for_ability` | Enum/String | `attack, Spin_Enemy` |
| `move_weights` | Enum/String | `stay_close_avoid_allies, stay_close, stay_close_always_move` |

### Context: `MoveForBarrage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_for_ability` | Enum/String | `ZaratanaVSBombardment` |
| `move_weights` | Enum/String | `stay_far` |

### Context: `MoveForDash`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_for_ability` | Enum/String | `attack` |
| `move_weights` | Enum/String | `keep_distance` |

### Context: `MoveForGrass`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `StegoGrassStomp` |
| `move_for_ability` | Enum/String | `StegoEatGrass` |
| `move_weights` | Enum/String | `minimum_move` |

### Context: `MoveForPounce`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_for_ability` | Enum/String | `attack` |
| `move_weights` | Enum/String | `keep_distance` |

### Context: `MoveForSpin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `PyrophinaVSRun` |
| `move_for_ability` | Enum/String | `PyrophinaVSSpinThrow` |
| `move_weights` | Enum/String | `stay_close` |

### Context: `MoveForThrow`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_for_ability` | Enum/String | `PyrophinaSoloCatThrow, PyrophinaVSCatThrow` |
| `move_weights` | Enum/String | `util_minmove` |

### Context: `MoveOneForPuke`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `AlienBeastMoveOne` |
| `move_for_ability` | Enum/String | `AlienBeastPuke` |
| `move_weights` | Enum/String | `keep_distance` |

### Context: `MoveSpaced`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_weights` | Enum/String | `terminator_keep_distance_always_move` |

### Context: `MoveToHead`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `G3RunToHead` |
| `move_for_ability` | Enum/String | `G3GrabHead` |
| `move_weights` | Enum/String | `minimum_move` |

### Context: `MoveTowards`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `move_for_ability` | Enum/String | `attack` |
| `move_weights` | Enum/String | `stay_close` |

### Context: `MoveTowardsDamageSource`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `can_move_zero` | Boolean | `true` |
| `check_has_status` | Enum/String | `FinalBossHitCountdownBoris` |
| `check_in_form` | Enum/String | `Boris, Default` |
| `do_not_move_on_top` | Boolean | `true` |
| `face_towards_after` | Boolean | `true` |
| `ignore_tagged_sources` | Enum/String | `megadino` |
| `move_ability` | Enum/String | `MD_WalkOne, MoveOne` |
| `move_far` | Boolean | `false` |
| `move_short` | Boolean | `true` |

### Context: `MoveTowardsKillers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `character_filter` | Array | `[ SpiderCat, TallSpiderCat ]` |
| `move_ability` | Enum/String | `SpiderReturn` |

### Context: `MoveWhenDamaged`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `move_ability` | Enum/String | `WaterTrailMove` |
| `weights` | Enum/String | `stay_near_allies_always_move, chaotic, stay_far_always_move` |

### Context: `MovementReaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MoonHead_EatCat, weapon, MoonHandGrab` |
| `blind_spot` | Boolean | `true` |
| `enemies_only` | Boolean | `false, true` |
| `forward_only` | Boolean | `true` |
| `objects_too` | Boolean | `true` |
| `on_self_move_too` | Boolean | `true` |
| `self_move_exclude_self_abilities` | Boolean | `true` |

### Context: `MultiSpawnOnDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count` | Array | `[ 0, 2 ]` |
| `obj` | Enum/String | `Maggot` |

### Context: `Mutant`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Mutant"` |
| `attack` | Enum/String | `BBMutantSwipe` |
| `move_speed_multiplier` | Enum/String | `.5` |
| `name` | String | `"ENEMY_CULTISTMUTANT_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CULTISTMUTANT_DESC"` |
| `turns` | Block | `{ ... }` |

### Context: `NCGravecrawlFAR`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `NCGravecrawl` |
| `move_weights` | Enum/String | `stay_far` |

### Context: `NeutronStar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `NoEyes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"0"` |

### Context: `NoStick`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `ManglerJab` |

### Context: `NonCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `spawnHolding` |
| `formchange` | Enum/String | `SmallHolding, BigHolding` |
| `statuses` | Block | `{ ... }` |

### Context: `Normal`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Up"` |
| `attack` | Enum/String | `SpewerLobbed_Normal, TinaBasicBigMeleeA` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `NormalFull`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Full` |
| `attack` | Enum/String | `SpewerSpit` |
| `passives` | Block | `{ ... }` |

### Context: `NotPriming`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Nothing`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `spawn` |

### Context: `Nuke`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Nuke` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Obey`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `Off`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `Off` |

### Context: `OffMap`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `OffScreen`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `OneAlive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `OneEye`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |
| `passives` | Block | `{ ... }` |

### Context: `Open`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Open` |
| `attack` | Enum/String | `GSOpenAttack` |
| `passives` | Block | `{ ... }` |

### Context: `OpenCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `OpenCat` |
| `passives` | Block | `{ ... }` |

### Context: `Out`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `PassiveGroup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` |
| `ExtraBasicAttacks` | Number | `1` |
| `FormChange` | Enum/String | `Hunter, Fighter, Mage` |
| `ReplaceBasicAttack` | Enum/String | `BasicRanged, BasicMelee, BasicMagicShortRanged` |
| `SelfStatusCarefulness` | Number | `1` |
| `StatusCarefulness` | Number | `1` |
| `TinkererBasicAttackSwitching` | Block | `{ ... }` |

### Context: `PassiveWhenAffectedByElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Fire` |
| `passives` | Block | `{ ... }` |

### Context: `PassiveWhenDead`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddStatusToTrampleDamage` | Block | `{ ... }` |

### Context: `PassiveWhileHasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `status` | Enum/String | `DemonicGlyph_Fire, DemonicGlyph_Summon, DemonicGlyph_Bite` |

### Context: `PassiveWhileNotHasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `status` | Enum/String | `DemonicGlyph_Movement, ExistUntilIdleUpkeep` |

### Context: `Possessing`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"Possessing"` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Primed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `GA_Telekinesis_Big` |
| `partial_animation_suffix` | Enum/String | `primed` |
| `passives` | Block | `{ ... }` |

### Context: `Priming`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `ProtectTargetedAllies`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `SwapPositions_TankCat` |
| `target_filter` | Enum/String | `any, Kitten` |

### Context: `Pulp2`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Number | `2` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |
| `turns` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1` |

### Context: `Pulp3`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Number | `3` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |
| `turns` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1` |

### Context: `Pulp4`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Number | `4` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |
| `turns` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1` |

### Context: `Pulp5`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Number | `5` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |
| `turns` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1` |

### Context: `Pulp6`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Number | `6` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |
| `turns` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1` |

### Context: `Pulp7`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | Number | `7` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |
| `turns` | Block | `{ ... }` |
| `uifloaters_offset` | Number | `1` |

### Context: `Rage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Rage"` |
| `attack` | Enum/String | `ChubsSpinRage` |
| `move_speed_multiplier` | Number | `2` |
| `partial_animation_suffix` | String | `"Rage"` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Rain`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `RandomPassivePool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `PassiveGroup` | Block | `{ ... }` |
| `TransformInXTurns` | Block | `{ ... }` |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `StatusGroup` | Block | `{ ... }` |

### Context: `ReflectProjectiles`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `self_damage` | Number | `2` |

### Context: `RemoveStatusStacks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `1, 10` |
| `status` | Enum/String | `DodgeChance_Status, Brace` |

### Context: `ReplaceBrain`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `brain` | Enum/String | `PatternBrain` |
| `decision_weights` | Enum/String | `default` |
| `move_weights` | Enum/String | `keep_distance, stay_close` |
| `pattern` | Block | `{ ... }` |

### Context: `ReturnA`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `HangerBotReturn` |
| `move_weights` | Enum/String | `stay_close` |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `0` |
| `knockback` | Number | `5` |
| `type` | Enum/String | `status` |

### Context: `Robot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `alternate_energized_effect` | Block | `{ ... }` |

### Context: `RunFar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `PyrophinaVSRun` |
| `move_weights` | Enum/String | `run_far` |

### Context: `RunWhenLastPlayerCatIsCharmed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | `true` |
| `legacy_savekey` | Enum/String | `Legacy_Marshmallow_StolenCatID` |

### Context: `ScalingAttackAnimation`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `10,` | Enum/String | `bite3` |
| `default` | Enum/String | `bite1` |
| `thresholds` | Array | `[ [ 5, bite2 ]` |

### Context: `SecurityBotProtect`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `SZBShoot, attack, CBShoot_ZodiacStyle` |
| `enemies_only` | Boolean | `true` |
| `move` | Enum/String | `None, SBotAngryMove` |
| `not_on_kill` | Boolean | `true` |
| `tag_restriction` | Enum/String | `dc_cat, dinofamily` |

### Context: `SharePickups`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `include_coins` | Boolean | `true` |

### Context: `Sitting`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Chair` |
| `attack` | Enum/String | `DoNothing` |
| `move` | Enum/String | `DoNothing` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `SkipFirstRounds`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pop_chance` | Number | `50%` |
| `stacks` | Number | `2` |

### Context: `SlotMachineRollPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `SlotResult_Explode` | Number | `1` |
| `SlotResult_Jackpot_Coins` | Number | `1` |
| `SlotResult_Nothing` | Number | `7` |
| `SlotResult_RandomPickup` | Number | `11` |

### Context: `Small`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `""` |
| `attack` | Enum/String | `GameteInflate` |

### Context: `SmallHolding`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"Holding"` |
| `passives` | Block | `{ ... }` |

### Context: `SmallHoldingCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"HoldingCat"` |
| `passives` | Block | `{ ... }` |

### Context: `SmallRockBehavior`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chain` | Boolean | `true` |
| `damage` | Number | `9, 5` |
| `knockback` | Number | `1, 2, 5` |

### Context: `SpawnOnDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `additional_statuses` | Block | `{ ... }` |
| `faction` | Enum/String | `allies, enemies` |
| `obj` | Array | `[ Spookie Spookie Scary Coin2 Coin3 Coin4 ], RiftKitten, [ Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCa...` |

### Context: `SpawnThingOnDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `auto_cast` | Enum/String | `Dash_Enemy` |
| `chance` | Number | `33%, .25, 50%` |
| `coins` | Number | `1` |
| `consider_all_layers` | Boolean | `true` |
| `good` | Boolean | `false, true` |
| `melee_ability_only` | Boolean | `true` |
| `object` | Enum/String | `Maggot, TinySpider, Rat` |
| `spawn_on_death_hit` | Boolean | `false` |

### Context: `SpawningPhase`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `SpearRun`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `CaveManSpearRun` |
| `move_for_ability` | Enum/String | `CaveManPickupSpear` |
| `move_weights` | Enum/String | `util_minmove` |

### Context: `SpewerAltGraphics`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FireFull` | Number | `1` |
| `Fire` | Number | `1` |
| `NormalFull` | Number | `0` |
| `Normal` | Number | `0` |
| `TarFull` | Number | `2` |
| `Tar` | Number | `2` |

### Context: `SquirrelForm`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `BasicMelee` |
| `passives` | Block | `{ ... }` |
| `tooltip` | Enum/String | `ENEMY_DRAVENSQUIRRELFORM_DESC` |

### Context: `StacyMutant_Brace`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Number | `3` |
| `CatPartsTransform` | Block | `{ ... }` |

### Context: `StacyMutant_Counter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `CatPartsTransform` | Block | `{ ... }` |
| `CounterAttack` | Enum/String | `SM_BleedCounter` |

### Context: `StacyMutant_Damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddDamage` | Number | `2` |
| `AddMaxHealth` | Number | `-25` |
| `CatPartsTransform` | Block | `{ ... }` |

### Context: `StacyMutant_DoubleHead`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` |
| `ExtraDispersedTurns` | Number | `1` |

### Context: `StacyMutant_Fire`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` |
| `ElementImmune` | Enum/String | `Fire` |
| `ReplaceBasicAttack` | Enum/String | `SM_Lavashot` |
| `ReplaceBrain` | Block | `{ ... }` |

### Context: `StacyMutant_Health`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddMaxHealth` | Number | `25` |
| `AddSpeed` | Number | `-3` |
| `CatPartsTransform` | Block | `{ ... }` |
| `SizeScale` | Number | `1.2` |

### Context: `StacyMutant_Holy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` |
| `DivineShield` | Number | `7` |

### Context: `StacyMutant_Ice`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddMovement` | Number | `-1` |
| `CatPartsTransform` | Block | `{ ... }` |
| `ElementImmune` | Enum/String | `Ice` |
| `ReplaceBasicAttack` | Enum/String | `SM_IceBreath` |
| `ReplaceBrain` | Block | `{ ... }` |

### Context: `StacyMutant_Lightning`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` |
| `ElementImmune` | Enum/String | `Electric` |
| `ReplaceBasicAttack` | Enum/String | `SM_LightningDash` |
| `ReplaceBrain` | Block | `{ ... }` |

### Context: `StacyMutant_Mirror`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` |
| `ReflectProjectiles` | Number | `100%` |
| `StatusEachTurnEndForEachTurn` | Block | `{ ... }` |

### Context: `StacyMutant_Speed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddDamage` | Number | `-1` |
| `AddSpeed` | Number | `6` |
| `CatPartsTransform` | Block | `{ ... }` |
| `SizeScale` | Enum/String | `.8` |

### Context: `StacyMutant_Thorns`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` |
| `Thorns` | Number | `3` |

### Context: `Standing`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `BungaSmash` |
| `move` | Enum/String | `DefaultMove` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Standing2`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `BungaSmash` |
| `move` | Enum/String | `BungaJumpMove` |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `Start_Ceiling`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `StatusAfterXTurns`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `CancerExplode` |
| `stacks` | Number | `3` |

### Context: `StatusCollector`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Poison` | Number | `2` |
| `Slow` | Number | `2` |
| `StrengthUp` | Number | `1` |

### Context: `StatusEachTurnBeginIfHasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` |
| `DamageUp` | Number | `2` |
| `HealthGain` | Number | `8` |
| `animation` | Enum/String | `pulse3` |
| `consume` | Boolean | `true` |
| `status` | Enum/String | `Counterspell` |

### Context: `StatusEachTurnEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Conditional_BadRoll` | Block | `{ ... }` |
| `DivineShield` | Number | `1` |
| `HealthGain` | Number | `4` |
| `SpeedUp` | Number | `2` |

### Context: `StatusEachTurnEndForEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` |

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `T2UnClone` |

### Context: `StatusGroup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FindItemFromPool` | Enum/String | `parasites, mutant_pool` |

### Context: `StatusOnDie`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RemoveAmbientLightEffects` | Number | `4` |
| `RemoveGlobalModifiers` | Array | `[ BloodRain ]` |

### Context: `StatusOnEndMove`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RemoveStatusStacks` | Block | `{ ... }` |
| `SpeedUp_WithoutInitiative` | Number | `1` |

### Context: `StatusOnEnemyConfused`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ImmediateUseAbility` | Enum/String | `FuzzerReact` |

### Context: `StatusOnGainCoins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BackflipWhenTargeted` | Block | `{ ... }` |

### Context: `StatusOnKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthGain` | Number | `5` |
| `UseAbility_NonStack` | Enum/String | `BBTransformZealot, GenericRage` |

### Context: `StatusOnSpawnIn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` |
| `SetHealth` | Number | `50%` |

### Context: `StatusOnTookDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ConstitutionUp` | Number | `-1` |
| `RemoveStatusStacks` | Block | `{ ... }` |
| `StrengthUp` | Number | `-1` |

### Context: `StatusOnTookDamageFromAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `ExtraBasicAttacks_Status` | Number | `1` |
| `HealthRegenUp` | Number | `1` |
| `TakeExtraTurn` | Number | `1` |

### Context: `StatusOverlappingCharactersAndDie`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Poison` | Number | `1` |

### Context: `StatusWhenStatusCompletelyRemoved`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `UseAbility` | Block | `{ ... }` |
| `status` | Enum/String | `BackflipWhenTargeted` |

### Context: `Stop`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `StunImmunity`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | `false` |

### Context: `SuckMF`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `TormentorSuck` |
| `decision_weights` | Enum/String | `careless` |
| `move_weights` | Enum/String | `keep_distance` |

### Context: `SupportDieInsteadOfRun`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `alt_dead_ani` | Enum/String | `off` |
| `alt_dying_ani` | Enum/String | `shutdown` |

### Context: `SupportFormChangeInsteadOfRun`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `SBotAnger, TVChangeDie` |
| `wait_till_turn` | Boolean | `true` |

### Context: `SwimmingFormChange`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `form_in` | Enum/String | `Water` |
| `form_out` | Enum/String | `Out` |

### Context: `SwitchMusic`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `new_layer` | Enum/String | `event` |
| `new_song` | Enum/String | `same` |

### Context: `SwordAndShield`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `DestroyerAttack` |
| `passives` | Block | `{ ... }` |

### Context: `SwordAndShield_Primed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Holy"` |
| `attack` | Enum/String | `DestroyerAttack` |
| `passives` | Block | `{ ... }` |

### Context: `SyncFormsWithBuddy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `no_buddy` | Enum/String | `Rage` |

### Context: `T3HitlerSpawningPhase`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `T3JoinFight` | Flag | `N/A` |
| `T3Spawn_Colorless` | Flag | `N/A` |
| `spell_use_groups` | Array | `[ [ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T...` |

### Context: `TF_TargetAllies`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `TwistingFlames` |
| `decision_weights` | Enum/String | `util_target_allies` |

### Context: `TF_TargetEnemies`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `TwistingFlames` |
| `decision_weights` | Enum/String | `util_target_enemies` |

### Context: `TVBotScreen`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Die` | Number | `6` |
| `Dumb` | Number | `3` |
| `Fuck` | Number | `5` |
| `Obey` | Number | `1` |
| `Shit` | Number | `4` |
| `Stop` | Number | `2` |

### Context: `Tar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `SpewerLobbed_Tar` |
| `passives` | Block | `{ ... }` |

### Context: `TarFull`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Full` |
| `attack` | Enum/String | `SpewerSpit` |
| `passives` | Block | `{ ... }` |

### Context: `TempPassiveUntilSettled`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `MeleeRevengeDamage` | Block | `{ ... }` |

### Context: `Terminator2Run`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `move_ability` | Enum/String | `T2GoopRun` |
| `move_weights` | Enum/String | `stay_far_always_move` |

### Context: `TerminatorChase`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `T1ChokeReaction` |
| `move` | Enum/String | `MoveOne` |

### Context: `TerminatorSkin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `groups` | Array | `[ { stacks 48 ParticleBurst Gibs_terminatorskin CatPartsT...` |
| `status` | Enum/String | `Brace` |

### Context: `Throb`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |

### Context: `ThrobBubs`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `ThrobHost`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | Enum/String | `Host` |
| `passives` | Block | `{ ... }` |

### Context: `ThrobNettle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `TinkererBasicAttackSwitching`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `craft_ability` | Enum/String | `TinkererCraft` |
| `throw_ability` | Enum/String | `TinkererThrow` |

### Context: `TransformInXTurns`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `hatch` |
| `initiative` | Enum/String | `keep_turns_end_turn` |
| `object` | Array | `[ Squirrel Crow Snake Turtle Toad Catepillar ], SkeletonCatRevived, TallSkeletonCatRevived` |
| `stacks` | Number | `1, 2, 3` |
| `turns` | Array | `[ 1 4 ]` |

### Context: `TransformOnDeathImmediately`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `first_turn` | Enum/String | `keep_turns` |
| `obj` | Enum/String | `SkeletonShamblerCorpse, TallSkeletonCatCorpse, SkeletonCatCorpse` |

### Context: `TransformOnElementInfluence`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Fire, Holy` |
| `object` | Enum/String | `CookedFood, CookedBigFood, CookedBiggestFood` |

### Context: `TransformOnElementInfluencex`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Holy` |
| `object` | Enum/String | `Bait, PurifiedPoisonFood` |

### Context: `TransformOnStatusThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `Moth` |
| `status` | Enum/String | `AllStatsUp` |
| `threshold` | Number | `5` |

### Context: `Transformed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `Trapper`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `HellHandGrab, BloatSideLaser, YA_Laser` |
| `cancel_movement` | Boolean | `false` |
| `pathfinding_avoidance` | Number | `250` |
| `range` | Number | `10` |

### Context: `Turtled`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | Enum/String | `Turtle` |
| `attack` | Enum/String | `None` |
| `move` | Enum/String | `None` |
| `passives` | Block | `{ ... }` |

### Context: `TwisterFling`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `5` |
| `max_dist` | Number | `5` |
| `min_dist` | Number | `3` |

### Context: `TwoAlive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `turns` | Block | `{ ... }` |

### Context: `TwoEyes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `Unflip`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `TeleportFlipUp` |
| `move_for_ability` | Enum/String | `Spin_Enemy` |
| `move_weights` | Enum/String | `stay_close_always_move` |

### Context: `UnlimitedDeathRattleRevive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MD_Lift` |
| `even_if_stunned` | Boolean | `true` |

### Context: `Unlit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Unlit` |
| `passives` | Block | `{ ... }` |

### Context: `Unwashed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `partial_animation_suffix` | Enum/String | `Unwashed` |

### Context: `Up`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Up"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"OBJECT_TIREUP_DESC"` |

### Context: `UseAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `Destroyer2HolyAttack` |
| `respect_prime` | Boolean | `true` |

### Context: `UseAbilityWhenOutOfStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `QueenHippoHeartAttack` |
| `status` | Enum/String | `Brace` |

### Context: `Washed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |

### Context: `Washer`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `attack` | Enum/String | `BasicMelee` |
| `name` | String | `"ENEMY_CULTISTWASHER_NAME"` |
| `partial_animation_suffix` | String | `"Cultist"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CULTISTWASHER_DESC"` |

### Context: `Water`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Water"` |
| `passives` | Block | `{ ... }` |

### Context: `WereMan`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"WereMan"` |
| `attack` | Enum/String | `WereManFurySwipes` |
| `name` | String | `"ENEMY_WEREMAN_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_WEREMAN_DESC"` |

### Context: `Zealot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"Zealot"` |
| `attack` | Enum/String | `BBStabby` |
| `name` | String | `"ENEMY_CULTISTZEALOT_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_CULTISTZEALOT_DESC"` |

### Context: `ZealotBomb`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ai` | Block | `{ ... }` |
| `animation_suffix` | String | `"BombZealot"` |
| `attack` | Enum/String | `BBExplode` |
| `name` | String | `"ENEMY_BOMBZEALOT_NAME"` |
| `passives` | Block | `{ ... }` |
| `tooltip` | String | `"ENEMY_BOMBZEALOT_DESC"` |

### Context: `abilities`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `attack` | Enum/String | `None, BasicMelee, DustMelee` |
| `can_get_bonus` | Boolean | `true` |
| `move` | Enum/String | `None, DefaultMove, DustMove` |
| `spells` | Array | `[ SpawnBomb BombRatTurtle RockToss_BomberRat ], [ BirdFly ], [ TrampleDash MoveOne ]` |

### Context: `active`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `additional_statuses`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` |

### Context: `ai`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animate_choice` | Boolean | `false, true` |
| `attack` | Enum/String | `JohnnyBlast` |
| `auto_orient` | Boolean | `false` |
| `bonusturn_pattern` | Block | `{ ... }` |
| `brain` | Enum/String | `PatternBrain, GenericBrain, PlayerBrain` |
| `clamp_pattern` | Boolean | `true` |
| `consider_spells` | Boolean | `false` |
| `decision_weights` | Enum/String | `simple, default, extra_careless` |
| `dice_abilities` | Array | `[ D6Fizzle D6Confused D6Poop D6Laser D6Quake D6Storm D6Wr...` |
| `dispersed_bonusturn_pattern` | Block | `{ ... }` |
| `end_turn_on_formswitch` | Boolean | `false, true` |
| `fallback_advances_pattern` | Boolean | `false, true` |
| `fallback` | Block | `{ ... }` |
| `mainturn_pattern` | Block | `{ ... }` |
| `move_weights` | Enum/String | `keep_distance_always_move, chaotic_runaway, bird` |
| `never_hit_ally_corpses` | Boolean | `true` |
| `pattern` | Block | `{ ... }` |
| `post_absorb_move_weights` | Enum/String | `minimum_move` |
| `random_orient` | Boolean | `true` |
| `randomize_pattern_start` | Boolean | `true` |
| `reset_pattern_on_formswitch` | Boolean | `false, true` |
| `reset_pattern_on_round_begin` | Boolean | `true` |
| `roll_ability` | Enum/String | `RollDice` |
| `round_end_bonusturn_pattern` | Block | `{ ... }` |
| `round_start_bonusturn_pattern` | Block | `{ ... }` |
| `stun_advances_pattern` | Boolean | `false, true` |
| `virtual_abilities` | Block | `{ ... }` |

### Context: `ai_if_spawned_as_enemy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `brain` | Enum/String | `PatternBrain` |
| `decision_weights` | Enum/String | `default` |
| `move_weights` | Enum/String | `keep_distance` |
| `pattern` | Block | `{ ... }` |

### Context: `ally_rewards`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `FindItemFromPool` | Enum/String | `dove_pool, chapter, blackbird_pool` |
| `RandomStatusFromPool` | Block | `{ ... }` |

### Context: `alt_spawn_pool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Antidote` | Number | `1, .5` |
| `Bear` | Number | `1` |
| `BigCatnip` | Number | `6, 1, 10` |
| `BigFood` | Number | `5, 20` |
| `BigScrap` | Number | `6, 1, 4.5` |
| `BiggestFood` | Number | `6, 1, 15` |
| `BlackBird` | Number | `3000` |
| `Blessing` | Number | `1, .5` |
| `Catepillar` | Number | `10` |
| `Catnip` | Number | `20` |
| `CharmedDip` | Number | `1` |
| `CharmedFloater` | Number | `1` |
| `CharmedPile` | Number | `1` |
| `Cherub` | Number | `1` |
| `Chicken` | Number | `3000` |
| `Coin10` | Number | `1, .1` |
| `Coin2` | Number | `1` |
| `Coin3` | Number | `1` |
| `Coin4` | Number | `1` |
| `Coin` | Number | `1, 70` |
| `Dove` | Number | `1000` |
| `Eagle` | Number | `300` |
| `Food` | Number | `20` |
| `Harpy` | Number | `1` |
| `HummingBird` | Number | `300` |
| `LargeBirdPool` | Number | `1` |
| `MedBirdPool` | Number | `1` |
| `MedCatnip` | Number | `5, 20` |
| `MedScrap` | Number | `5, 20` |
| `Mutant` | Number | `1` |
| `Pigeon` | Number | `3000` |
| `RandomArmorPickup` | Number | `40, 4.5` |
| `RandomBiggerArmorPickup` | Number | `4.5` |
| `RandomBiggerCatnipPickup` | Number | `10` |
| `RandomBiggerFoodPickup` | Number | `15` |
| `RandomCatnipPickup` | Number | `10, 30` |
| `RandomFoodPickup` | Number | `40, 15` |
| `Raven` | Number | `300` |
| `Scrap` | Number | `20` |
| `Seagull` | Number | `1000` |
| `SmallBirdPool` | Number | `1` |
| `Snake` | Number | `10` |
| `Squirrel` | Number | `10` |
| `Toad` | Number | `10` |
| `Turkey` | Number | `1000` |
| `Turtle` | Number | `10` |

### Context: `alternate_energized_effect`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FormChange` | Enum/String | `GuaranteedJackpot` |
| `SpellDamageUp` | Number | `1` |

### Context: `bonusturn_pattern`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_all` | Array | `[ TrembloSuck *TrembloEat TrembloEat ], [ CloseConvert, attack ], [ attack AlienBeastOpenEyes ]` |
| `do_priority` | Array | `[ TormentorBite TormentorSpawn attack ], [ TormentorSpawn TormentorBite attack ], [ G3GrabHead move *G3GrabHead ]` |
| `do_strict` | Array | `[ ], [ WizFlamethrower ], [ WizStorm ]` |
| `do` | Enum/String | `*SpawnBomb, move, DustDash` |
| `move_then_do` | Enum/String | `RatKingSpawn` |

### Context: `damage_instance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `effects` | Block | `{ ... }` |

### Context: `default`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `dispersed_bonusturn_pattern`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do` | Enum/String | `attack, Simon_Trash, Simon_Tentacle` |

### Context: `eat_damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |
| `damage` | Number | `0` |
| `effects` | Block | `{ ... }` |
| `makes_contact` | Boolean | `true` |
| `piercing` | Boolean | `true` |
| `type` | Enum/String | `melee` |

### Context: `effects`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BlackHoleSuck` | Number | `1` |
| `Burn` | Number | `2, 5` |
| `Confusion` | Number | `1` |
| `ConstitutionUp` | Number | `-1` |
| `Stun` | Number | `1` |
| `Thorns` | Number | `1` |
| `Vaporize` | Number | `20` |

### Context: `equipment`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `face` | Enum/String | `WesternHat, MetalPlate, AtomicMark` |
| `head` | Enum/String | `CoinBag, Banana, LoansharksFedora` |
| `neck` | Enum/String | `Slime, MageCollar, Poncho` |
| `weapon` | Enum/String | `ButcherHook, AstroTaser, GunslingerPistol` |

### Context: `exit_animations`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Default` | Enum/String | `release` |

### Context: `fallback`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_all` | Array | `[ move, *CoreFreakFury ]` |
| `do_best` | Array | `[ Magnetize, attack, GuillotinaTossCollide, YeetTowardsBu...` |
| `do_nothing` | Array | `[ ]` |
| `do_priority` | Array | `[ *attack RunFar ], [ attack TrembloEat ], [ attack, Magnetize, YeetTowardsBuddy ]` |
| `do_random` | Array | `[ CHSpawn CHCry ]` |
| `do` | Enum/String | `attack, RockToss_ColorlessCat_AsCloseAsPossible, JohnnyBlast` |
| `move_then_do` | Enum/String | `CerberubsCalm` |

### Context: `graphics`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `alt_animations` | Array | `[ [ idle girlyIdle ], [ [ idle cuteIdle ], [ [ idle twitchyIdle ]` |
| `always_huge_mask` | Boolean | `true` |
| `art_flip` | Number | `-1` |
| `custom_cat_data` | Enum/String | `Kitten, TomTom, Mangy` |
| `dead` | Enum/String | `empty, skeletonDead` |
| `deadhit` | Enum/String | `skeletonCorpseHit` |
| `default_attack_animation` | Enum/String | `bite1, attack2` |
| `depth_offset` | Number | `5, -.1, .01` |
| `desc` | String | `"OBJECT_DECOY_DESC", ENEMY_FATWOMAN_DESC` |
| `dodge` | Enum/String | `liquidmetaldodge` |
| `dont_sink` | Boolean | `true` |
| `dying` | Enum/String | `dyingDisassembled, dead` |
| `four_way_animations` | Boolean | `true` |
| `hit` | Enum/String | `hitDisassembled, skeletonCorpseHit` |
| `move_speed_multiplier` | Number | `1.75, .66, .5` |
| `move_speed_sync_frames` | Number | `22.5, 7, 40` |
| `movieclip` | Enum/String | `BirdMed, BirdSmall, BirdLarge` |
| `name` | String | `"ENEMY_LITTLEBIRD_NAME", "ENEMY_MEDBIRD_NAME", "ENEMY_BIRD_NAME"` |
| `no_horizontal_flip` | Boolean | `true` |
| `no_splatter` | Boolean | `true` |
| `non_blocking_animations` | Array | `[ "hit" , "critical" ]` |
| `override_portrait` | Enum/String | `Cherub` |
| `piece_alt_frame` | Number | `5, 7, 3` |
| `projectile_spawn_offset` | Array | `[ 0 1 ], [ .25 1 ], [ 0 1.5 ]` |
| `randomize_starting_frame` | Boolean | `false` |
| `scale` | Enum/String | `.9, .8, .5` |
| `shade_occluded_objects` | Boolean | `true` |
| `shadow_size` | Number | `2, 3, .5` |
| `shadow` | Enum/String | `MedSlimeShadow, none, TormentorShadow` |
| `show_infinity_damage_warning` | Boolean | `true` |
| `spawnin_animation` | String | `"digUp", digUp, "howl"` |
| `status_display_count_max` | Number | `5` |
| `stunned` | Enum/String | `idleDisassembled, dead` |
| `tint` | Array | `[ .7 1 .7 1 ], green, [ 0 0 0 1 ]` |
| `tooltip` | String | `"ENEMY_BIRD_DESC", "ENEMY_RADICALRAT_DESC", "ENEMY_CHERUB_FINALBOSS_DESC"` |
| `uifloaters_offset` | Number | `1.5, 2, 2.5` |
| `walk` | Enum/String | `stompwalk, raptorWalk, zombieWalk` |
| `water_mask` | Enum/String | `medmed, medium, square` |
| `weak` | Enum/String | `idleDisassembled, dead` |

### Context: `hot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_suffix` | String | `"Hot"` |
| `name` | String | `"OBJECT_HOTPETROCK_NAME", "OBJECT_HOTROCK_NAME", "OBJECT_HOTBOULDER_NAME"` |
| `passives` | Block | `{ ... }` |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `TVBotDie` | Number | `1` |
| `TVBotDumb` | Number | `1` |
| `TVBotObey` | Number | `1` |
| `TVBotStop` | Number | `1` |

### Context: `mainturn_pattern`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_all` | Array | `[ attack DustTeleport ], [ *AlienBeastScream *AlienBeastEat *AlienBeastPuke *Alien..., [ *MarshmallowZealot, CloseConvert, attack ]` |
| `do_priority` | Array | `[ *HitlerHeil attack move ], [ ChumShot_Damage, ChumShot_Maggot ], [ attack Simon_Shot ]` |
| `do_strict` | Array | `[ BasicMelee, RageUp ], [ *WizSpellShield, WizBlizzard ]` |
| `do` | Enum/String | `HealSelf, **TrampleDash, **BombRatTurtle` |
| `move_then_do` | Enum/String | `attack, RockSong` |

### Context: `other_form_change_abilities`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Boris` | Enum/String | `MegaGuppy_TransformBoris` |
| `Explosive` | Enum/String | `MegaGuppy_TransformExplosive` |
| `Holy` | Enum/String | `MegaGuppy_TransformHoly` |

### Context: `passive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `attack` | Enum/String | `DoNothing` |

### Context: `passives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AbilityAfterEnemyCastSpell_Stackable` | Enum/String | `ThornUp, ThornUpX` |
| `AbilityHealthThreshold` | Block | `{ ... }` |
| `AbilityOnBattleStart_UseAI` | Enum/String | `TheCreator_SpawnCloneTeam` |
| `AbilityOnRoundEnd` | Block | `{ ... }` |
| `AbilityReaction` | Enum/String | `attack, TC_DashReaction, { ... }` |
| `AbilityWhenBuddyDies` | Enum/String | `GirlDinoCry, ChubsRage, Guillotina2Rage` |
| `AbilityWhenTaggedCharacterMovesNear` | Block | `{ ... }` |
| `AddCorpseHealth` | Number | `-999` |
| `AddDamage` | Number | `1, 2, 4` |
| `AddElementsToBasicAttack` | Enum/String | `Fire` |
| `AddHiddenTag` | Enum/String | `grown_hitler_clone, hitler_clone_fetus, unlit_candle` |
| `AddInitiative` | Number | `-9999, -10, 999999` |
| `AddMaxHealth` | Number | `5` |
| `AddMeleeKnockback` | Number | `1, 2, 10` |
| `AddMovement` | Number | `1, 2, -2` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `AddStatusToReceivedDamage` | Block | `{ ... }` |
| `AddStatusToSpells` | Block | `{ ... }` |
| `AddStatusToWeapons` | Block | `{ ... }` |
| `AddTag` | Enum/String | `fetus, cat, tumor` |
| `AddTemporaryEffectsToBasicAttack` | Block | `{ ... }` |
| `AdvancedTint` | Array | `[ .6, .6, .6, 1 .5, .5, .5, 0 ]` |
| `AdventureTokenPassivePool` | Block | `{ ... }` |
| `AggroTargetIsBuddy` | Number | `1` |
| `AggroTargetIsCurrentTurn` | Number | `1` |
| `AggroTargetIsGovernedByHitEffect` | Block | `{ ... }` |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | `1` |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | `1` |
| `AggroTargetIsLowestMaxHealthCat` | Number | `1` |
| `AlienBeastDangerZones` | Array | `[ AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeas...` |
| `AlienBeastEyeStalks` | Number | `3` |
| `AllDamageImmune_IncludingSpeculative` | Number | `1` |
| `AllSpellsCostActPoints` | Number | `1` |
| `AllStatsAura` | Block | `{ ... }` |
| `AllStatsUp` | Number | `2` |
| `AlphaTurns` | Number | `1` |
| `AlwaysHitDifferentTargets` | Number | `1` |
| `Ammo` | Number | `6, 1, 3` |
| `Angel` | Number | `1` |
| `ArmorPickup` | Block | `{ ... }` |
| `AutocastEachRound` | Block | `{ ... }, SpiderReturn` |
| `AvoidDamagingCharmedEnemies` | Number | `1` |
| `AwardCoinsOnDeath` | Number | `10` |
| `BackstabAllDirections` | Number | `1` |
| `BackstabImmunity` | Number | `1` |
| `BaitAura` | Block | `{ ... }` |
| `BaseStatMultiply` | Enum/String | `.666, .25, .5` |
| `BasicAIDangerZone` | Number | `2` |
| `BattlefieldUniqueRandomPassive` | Block | `{ ... }` |
| `BirdRewards` | Block | `{ ... }` |
| `Bird` | Enum/String | `CookedChickenLeg` |
| `BlackHolePassive` | Number | `1` |
| `BloatEyePassive2` | Enum/String | `BloatEyeMovement2` |
| `BlockAllDamage` | Number | `1` |
| `BombBehavior` | Number | `1` |
| `BonusTurnPattern` | Array | `[ { evenly_dispersed_bonus_turns 1 round_end_bonus_turns ..., [ { dispersed_bonus_turns 2 round_end_bonus_turns 1 } { r..., [ { evenly_dispersed_bonus_turns 0 round_end_bonus_turns ...` |
| `BossRewards` | Block | `{ ... }` |
| `Brace` | Number | `1, 4, 10` |
| `Buddy` | Enum/String | `Nubs, Smough, Ornstein` |
| `BuffImmunity` | Number | `1` |
| `BungaCheers` | Block | `{ ... }` |
| `BungaEntrance` | Block | `{ ... }` |
| `Burn` | Number | `3` |
| `CCImmunity` | Number | `1` |
| `CanMutateTo` | Enum/String | `Hyde, [ TumorousMaggot, ChargeyMaggot, SwappyMaggot ], [ Lumpy, Leaper ]` |
| `CanShield` | Number | `1` |
| `CapReceivedDamage` | Number | `1` |
| `CatPartsTransform` | Block | `{ ... }` |
| `CaveFamilyEnrage` | Block | `{ ... }` |
| `CerberubsAggroTargetBehavior` | Block | `{ ... }` |
| `ChanceToBackflip` | Block | `{ ... }` |
| `ChanceToDisableActionsIfNotCharmed` | Number | `75%` |
| `ChanceToFormChangeOnAbilityDamage` | Block | `{ ... }` |
| `ChanceToSpitOnDamage` | Block | `{ ... }` |
| `ChangeTileOnDeath` | Enum/String | `WaterTile` |
| `ChangeTileOnPop` | Enum/String | `GlitchTile, OilTile, CreepTile` |
| `ChaosBossFormChangeGuide` | Block | `{ ... }` |
| `ChaosBossPieces` | Block | `{ ... }` |
| `ChaosHeadDropIn` | Block | `{ ... }` |
| `CharacterLightSource` | Block | `{ ... }` |
| `CherubimReaction` | Block | `{ ... }` |
| `CoinPickup` | Number | `1, 2, 3` |
| `ConjureBonusAbility` | Enum/String | `random` |
| `CountAsCorpse` | Number | `1` |
| `CounterAttackAfterEnemyCastSpell` | Enum/String | `Telekinesis` |
| `CounterAttack` | Enum/String | `YeticatSnowball_Counter, attack, BungaSwipe` |
| `CreateGlobalModifiers` | Block | `{ ... }` |
| `CrowAttackLink` | Number | `1` |
| `DamageFromBehindOnly` | Number | `1` |
| `DeathRattleRevive` | Block | `{ ... }, HCHumanDie, ToxPuff` |
| `DeathRattle` | Enum/String | `MoonHead_KillHands, BoomerCatExplode, { ... }` |
| `DebuffImmunity` | Number | `1` |
| `DelayedAutoRevive` | Block | `{ ... }` |
| `DemonicGlyphFrames` | Number | `1` |
| `DemonicGlyphStealer` | Number | `1` |
| `DiceBehavior` | Block | `{ ... }` |
| `DicerArt` | Array | `[ 59 52 65 50 54 63 64 ]` |
| `DieWhenOnlyGolemsLeft` | Number | `1` |
| `DieWhenSpawnerDies` | Number | `1` |
| `DiesToElement` | Enum/String | `Wind, { ... }` |
| `DiesToPiercingAndSpikes` | Block | `{ ... }` |
| `DigestDeadBodies` | Enum/String | `MoonHead_Digest, LennyCatDies, Digest` |
| `DisableSpells` | Number | `1` |
| `DisguisedTrapper` | Enum/String | `FearMelee` |
| `Disguised` | Number | `1` |
| `DisplayBuddyCatOnSpawn` | Number | `3` |
| `DisplayDangerAOE` | Enum/String | `MoonHead_Blow, attack, TheChild_Wrath` |
| `DissuadeInstakills` | Number | `1` |
| `Divide4OnDeath` | Enum/String | `Clot, BiggestFood, MedSlime` |
| `DivineShieldPickup` | Number | `1` |
| `DivineShield` | Number | `2` |
| `DodgeChanceWithBlindSpot` | Number | `25%` |
| `DodgeChance_Status` | Number | `100, 66` |
| `DodgeChance` | Number | `50%` |
| `DodgeWhenTargeted` | Block | `{ ... }` |
| `DustCloudBehavior` | Number | `1` |
| `Dybbuk1HPTracker` | Number | `1` |
| `DybbukPossessionFallback` | Block | `{ ... }` |
| `ElectricArcs` | Number | `1` |
| `ElementImmune` | Enum/String | `Ice, Fire, Creep` |
| `ElementWeakness` | Enum/String | `Fire` |
| `EnrageOnDamage` | Number | `1` |
| `EraseSpawnCoins` | Number | `1` |
| `EventBounterHunterPassive` | Number | `1` |
| `ExpireOnSpawnerTurnEnd` | Number | `1` |
| `ExtraDispersedTurns` | Number | `1` |
| `ExtraMovePoints` | Number | `1` |
| `ExtraTurnsPerTaggedUnit` | Enum/String | `sprout` |
| `FaceAwayLastDamage` | Block | `{ ... }` |
| `FaceLastDamage` | Number | `1, { ... }` |
| `FaceShield` | Number | `0` |
| `FadeInsteadOfDie` | Number | `1` |
| `FinalBossBeamQueue` | Block | `{ ... }` |
| `FinalBossBecomeTheChild` | Block | `{ ... }` |
| `FinalBossHitCountdownBoris` | Block | `{ ... }` |
| `FinalBossHitCountdownExplosive` | Block | `{ ... }` |
| `FinalBossHitCountdownHoly` | Block | `{ ... }` |
| `FinalBossPupils` | Block | `{ ... }` |
| `FinalBossShieldHealth` | Block | `{ ... }` |
| `FinalBossShield` | Enum/String | `None, DestroyerShieldBash` |
| `FinalBossSyncAnimations` | Block | `{ ... }` |
| `FlingObjectsOnTop` | Number | `8` |
| `FlushmasterCelebration` | Enum/String | `celebrate` |
| `Flying` | Number | `1` |
| `ForceDodgeEverything` | Number | `1` |
| `FormChangeDuringWeatherElement` | Block | `{ ... }` |
| `FormChangeHealthThreshold` | Block | `{ ... }` |
| `FormChangeOffMap` | Block | `{ ... }` |
| `FormChangeOnElementInfluence` | Block | `{ ... }` |
| `FormChangeWhenBuddyDies` | Enum/String | `Rage` |
| `FormChangeWhileHasStatus` | Block | `{ ... }` |
| `FormChangeWhilePrimingAbility` | Block | `{ ... }` |
| `FormChanger` | Block | `{ ... }` |
| `FreePathfindElement` | Enum/String | `Water` |
| `FullBlockEverythingTo0Damage` | Number | `1` |
| `FullBlockEverything` | Number | `1` |
| `GasCanBehavior` | Number | `1` |
| `GasCloudBehavior2` | Number | `2` |
| `GeminiTwin` | Number | `1` |
| `GlobalManaDrainAura` | Number | `-1` |
| `GoopImmunity` | Number | `1` |
| `GoopWalk` | Number | `1` |
| `GroundFlopper` | Enum/String | `DefaultMove, MoveOne` |
| `GuillotinaDeathHead` | Number | `1` |
| `HPAltStates` | Block | `{ ... }` |
| `HarpoonTrapPassive` | Enum/String | `HarpoonTrapPull` |
| `HealNeighborsEachTurn` | Block | `{ ... }` |
| `HealthGain` | Number | `1, 5, 8` |
| `HealthPickup` | Block | `{ ... }` |
| `HealthRegenUp` | Number | `2, 4` |
| `HiddenDoomed` | Number | `2` |
| `HitlerExecute` | Block | `{ ... }` |
| `IceBlockBehavior` | Number | `1` |
| `IgnoreTiles` | Number | `1` |
| `IllusionTint` | Number | `1` |
| `ImmediateAbilityReaction` | Enum/String | `ChubsGoop, BumbleButt, NubsGoop` |
| `ImmobilePassive` | Number | `1` |
| `InfiniteRebirth` | Block | `{ ... }` |
| `InheritSpawnerStats` | Number | `1` |
| `InjuryImmunity` | Number | `1` |
| `InnateElement` | Enum/String | `Water, Fire` |
| `InsertIntoBackgroundPlaceholder` | Number | `1` |
| `JohnnyNeedsWashing` | Block | `{ ... }` |
| `JohnnyWasher` | Enum/String | `BBTransformZealot` |
| `KaijuKnockbackImmune` | Number | `1` |
| `KaijuWinCon` | Enum/String | `pyrophina, zaratana` |
| `KineticSpikes` | Number | `1, 5` |
| `KnockbackImmunity` | Number | `1` |
| `LegacySpawnSavedCatIfExists` | Enum/String | `Legacy_Marshmallow_StolenCatID` |
| `LimitDamage` | Number | `1` |
| `LimitHeal` | Number | `1, 0` |
| `LockOrientationFaceTile` | Array | `[ 0 0 ]` |
| `LoopingSoundWhileAlive` | Enum/String | `Twister_loop, BigUFO_ambient_looping, Bomb_FuseLoop` |
| `MagicDamageImmune` | Number | `1` |
| `MamaCatAnimations` | Number | `1` |
| `ManaPickup` | Block | `{ ... }` |
| `ManglerMonsterPassive` | Enum/String | `ManglerMonsterDashAttack` |
| `MegaDinoDropController` | Block | `{ ... }` |
| `MeleeRevengeDamage` | Block | `{ ... }` |
| `MimicSpawnerAttacks` | Number | `1, -1` |
| `MiniVolcanoReaction` | Enum/String | `ThrobShot_Reaction, MiniVolcano_Spurt` |
| `MinimumKnockbackFromAllDamage` | Number | `1` |
| `MinimumKnockbackFromPhysicalAttacks` | Number | `1` |
| `MissChance` | Number | `20` |
| `ModularPickup` | Block | `{ ... }` |
| `MonkCatReactionAbilities` | Block | `{ ... }` |
| `MoonHeadCrackedVisual` | Enum/String | `Cracked` |
| `MotherGrowController` | Block | `{ ... }` |
| `MotherTumorPassive` | Block | `{ ... }` |
| `MotherTumorSpawnInCapture` | Block | `{ ... }` |
| `Mount` | Block | `{ ... }` |
| `MoveAfterAnyAttemptedAttack` | Block | `{ ... }` |
| `MoveAwayFromDamageSource` | Block | `{ ... }` |
| `MoveAwayWhenEnemyAdjacent` | Block | `{ ... }` |
| `MoveTowardsDamageSource` | Enum/String | `MoveOne, { ... }` |
| `MoveTowardsKillers` | Enum/String | `ReaperRevenge, { ... }` |
| `MoveWhenDamaged` | Enum/String | `move, TKNG_Hop, { ... }` |
| `MovementReaction` | Block | `{ ... }` |
| `MultiSpawnOnDeath` | Block | `{ ... }` |
| `MulticatHeads` | Number | `0` |
| `MutateAfterXTurns` | Number | `3` |
| `MutateViaAbility` | Enum/String | `BBTransformMutant` |
| `MuteDemonicGlyphDisplay` | Number | `1` |
| `NoHealthOnlyShield` | Number | `1` |
| `OrthogonalAIDangerZone` | Number | `10` |
| `OverrideMaxHealth` | Number | `25, 1` |
| `PackHunting` | Number | `1` |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` |
| `PassiveWhenDead` | Block | `{ ... }` |
| `PassiveWhileHasStatus` | Block | `{ ... }` |
| `PassiveWhileNotHasStatus` | Block | `{ ... }` |
| `PermanentMadness` | Number | `1` |
| `Phasing` | Number | `1` |
| `Plant` | Number | `1` |
| `PoisonThorns` | Number | `3` |
| `PrioritizeAggroTarget` | Number | `1` |
| `PrioritizeFarAwayTargets` | Number | `1, 10` |
| `PrioritizeHitDifferentTargets` | Number | `1` |
| `PrioritizePlayerCats` | Number | `1` |
| `PrioritizeWeakestEnemy` | Number | `1` |
| `ProtectTargetedAllies` | Block | `{ ... }` |
| `RandomPassivePool` | Block | `{ ... }` |
| `RandomizeAIWeightsEachTurn` | Array | `[ { decision_weights default move_weights keep_distance }..., [ { decision_weights blind move_weights chubs_and_nubs_bl..., [ { decision_weights default move_weights stay_close } { ...` |
| `ReflectProjectiles` | Number | `1, 100%, { ... }` |
| `ReturnBoundItemOnBattleEnd` | Number | `1` |
| `RevengeDamage` | Block | `{ ... }` |
| `Robot` | Number | `1, { ... }` |
| `RunInXTurns` | Number | `1, 2, 3` |
| `RunWhenKittensDead` | Number | `1` |
| `RunWhenLastPlayerCatIsCharmed` | Block | `{ ... }` |
| `SafeDoomed` | Number | `1` |
| `ScalingAttackAnimation` | Block | `{ ... }` |
| `SecurityBotProtect` | Block | `{ ... }` |
| `SetSpellCosts` | Number | `0` |
| `SharePickupsWithSpawner` | Number | `1, 0` |
| `SharePickups` | Block | `{ ... }` |
| `SharkySmellsBlood` | Number | `1` |
| `SkipFirstRounds` | Block | `{ ... }` |
| `SlotMachineRollPool` | Block | `{ ... }` |
| `SmallRockBehavior` | Number | `5, 0, { ... }` |
| `SpawnCreepOnHitKnockback` | Number | `1` |
| `SpawnCreepOnHit` | Number | `1` |
| `SpawnOnDeath` | Enum/String | `BiggestFood, FrankPinky, { ... }` |
| `SpawnThingOnDamage` | Block | `{ ... }` |
| `SpawnThingOnDeath` | Enum/String | `Food, Gamete, Boulder` |
| `SpawnerCatDataReference` | Number | `1` |
| `SpeedUp` | Number | `6, 2` |
| `SpewerAltGraphics` | Block | `{ ... }` |
| `SpreadWater` | Number | `1` |
| `SproutsGrantMovement` | Number | `1` |
| `StartDead` | Number | `100%` |
| `StartOffMap` | Number | `1` |
| `StatusAfterXTurns` | Block | `{ ... }` |
| `StatusCollector` | Block | `{ ... }` |
| `StatusEachTurnBeginIfHasStatus` | Block | `{ ... }` |
| `StatusEachTurnEndIfEnabledAtStartOfTurn` | Block | `{ ... }` |
| `StatusEachTurnEnd` | Block | `{ ... }` |
| `StatusImmunity` | Enum/String | `Poison, [ Poison, Bleed ], Webbed` |
| `StatusOnDie` | Block | `{ ... }` |
| `StatusOnEndMove` | Block | `{ ... }` |
| `StatusOnEnemyConfused` | Block | `{ ... }` |
| `StatusOnGainCoins` | Block | `{ ... }` |
| `StatusOnKill` | Block | `{ ... }` |
| `StatusOnSpawnIn` | Block | `{ ... }` |
| `StatusOnTookDamageFromAbility` | Block | `{ ... }` |
| `StatusOnTookDamage` | Block | `{ ... }` |
| `StatusOverlappingCharactersAndDie` | Block | `{ ... }` |
| `StatusWhenStatusCompletelyRemoved` | Block | `{ ... }` |
| `StrengthUp` | Number | `2` |
| `StripStatuses` | Number | `1` |
| `StunImmunity` | Number | `1, { ... }` |
| `SupportDieInsteadOfRun` | Block | `{ ... }` |
| `SupportFormChangeInsteadOfRun` | Enum/String | `Attacker, { ... }` |
| `SurviveAt1HP` | Number | `1` |
| `SwimmingFormChange` | Block | `{ ... }` |
| `SyncFormsWithBuddy` | Block | `{ ... }` |
| `T3HitlerSpawningPhase` | Block | `{ ... }` |
| `TVBotDisableAttack` | Number | `1` |
| `TVBotDisableMove` | Number | `1` |
| `TVBotDisableSpells` | Number | `1` |
| `TVBotScreen` | Block | `{ ... }` |
| `TagGreed` | Enum/String | `bishop_hat, pickup, food` |
| `TakeWeaponFromSpawner` | Number | `1` |
| `TallTumorManaBurn` | Enum/String | `TT_ManaBurn` |
| `Tall` | Number | `1` |
| `Terminator2Chase` | Enum/String | `move` |
| `Terminator2Run` | Block | `{ ... }` |
| `TerminatorChase` | Block | `{ ... }` |
| `TerminatorSkin` | Block | `{ ... }` |
| `Thorns` | Number | `5, 2, 3` |
| `TileElementDamageImmunity` | Enum/String | `Ice` |
| `TileTrail_Ahead` | Enum/String | `FireTile, OilTile, WaterTile` |
| `TileTrail` | Enum/String | `ShadowTile, CreepTile` |
| `TinkererBasicAttackSwitching` | Block | `{ ... }` |
| `TireBehavior` | Number | `1` |
| `TormentorHeal` | Number | `1` |
| `TowerDefenseReflex` | Enum/String | `attack` |
| `TrackAmountKilledByPlayer` | Enum/String | `BonusBirdsKilled` |
| `Trample` | Number | `6, 5, 3` |
| `TransformInXTurns` | Block | `{ ... }` |
| `TransformOnDeathImmediately` | Enum/String | `NoHead, { ... }` |
| `TransformOnDeath` | Enum/String | `RatKing, Carcus, SimonFlopper` |
| `TransformOnElementInfluence` | Block | `{ ... }` |
| `TransformOnElementInfluencex` | Block | `{ ... }` |
| `TransformOnStatusThreshold` | Block | `{ ... }` |
| `TransformWhenBuddyDies` | Enum/String | `UltraOrnstein, UltraSmough` |
| `Trapper` | Block | `{ ... }` |
| `TutorialBossRiggedFight` | Number | `16` |
| `TwisterFling` | Block | `{ ... }` |
| `UncappedHP` | Number | `1` |
| `Undead` | Number | `1` |
| `UnlimitedDeathRattleRevive` | Block | `{ ... }` |
| `UnlockOrientation` | Number | `1` |
| `UpTireBehavior` | Number | `5` |
| `UseAbilityWhenOutOfStatus` | Block | `{ ... }` |
| `UseAbilityWhenShieldDepleted` | Enum/String | `T3Pebbles_PrimeBoulderDrop` |
| `UseAbility` | Enum/String | `MegaGuppy_SummonTheChild, TormentorRuneAbsorb` |
| `Wall` | Number | `1` |
| `WaterWalk` | Number | `1` |
| `WeaponsDontLoseDurability` | Number | `1` |
| `WeremanTransformationReceiver` | Enum/String | `CaveManTransform, CaveWomanDropTransform` |
| `WhitelistPickupType` | Enum/String | `food` |
| `WideBackstab` | Number | `1` |
| `WispDodge` | Number | `1` |
| `YOffset` | Enum/String | `.35, -.18` |
| `ZeroKnockbackDamage` | Number | `1` |

### Context: `pattern`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_all_shuffle` | Array | `[ YetiSlam YetiSlam YetiSlam YetiBite YetiBite YetiBite Y..., [ attack DybbukWisps DybbukRePossess ]` |
| `do_all` | Array | `[ CovenFamine CovenRise3 ], [ CovenWar CovenRise4 ], [ CovenPestilence CovenRise2 ]` |
| `do_best_multiple` | Array | `[ attack spell0 spell1 spell2 spell3 spell4 weapon trinket ]` |
| `do_best` | Array | `[ JohnnyPush JohnnyPull ]` |
| `do_nothing` | Array | `[ ]` |
| `do_priority_alternating` | Array | `[ *BadBone, *GoodBone, BadBone_copy, GoodBone_copy, BadBo...` |
| `do_priority` | Array | `[ *QueenWeb, attack, QueenMinis ], [ BumblefootEatCorpse, BumblefootEatCat, BumblefootBoneSh..., [ *RockToss_BomberRat, RockToss_BomberRat ]` |
| `do_random` | Array | `[ Escape attack DybbukReanimate ], [ ScaryHaunt ScaryFear ], [ Escape attack DybbukReanimate DybbukWisps ]` |
| `do_strict` | Array | `[ MCBlizzard ], [ MCFlamethrower ], [ MCStorm ]` |
| `do` | Enum/String | `**SimonFlopper_WiggleChance, **SimonFlopper_WiggleGuaranteed, **SimonFlopper_WiggleFake` |
| `move_then_do_all` | Array | `[ LennyShove, LennyGrabDead, LennyGrab ]` |
| `move_then_do_priority` | Array | `[ BBPickupCrown, *attack, *BBToss ], [ DrinkUp attack ], [ BBPickupCrown, *BBToss, *attack ]` |
| `move_then_do_random` | Array | `[ CerberubsJumpBlind CerberubsJumpNormal ], [ ClotEvolve ClotFailEvolve ], [ ClotEvolveCatCopy ClotFailEvolve ]` |
| `move_then_do` | Enum/String | `SimonFlopper_SpawnMinion, NubsJump, attack` |

### Context: `properties`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `access_to_player_inventory` | Boolean | `false, true` |
| `act_points` | Number | `2, 0, 4` |
| `aggro_target_is_enemy` | Boolean | `true` |
| `ai_scale` | Enum/String | `.25, .5, .01` |
| `allow_flying_effect` | Boolean | `true` |
| `allow_offmap_corpse` | Boolean | `true` |
| `allow_passive_spelltransforming` | Boolean | `true` |
| `allow_replacebrain` | Boolean | `false` |
| `always_face_forward` | Boolean | `true` |
| `always_triggers_traps` | Boolean | `true` |
| `aoe_pierce_mode` | Enum/String | `block` |
| `auto_run_priority` | Enum/String | `support, default, stationary` |
| `banned_elite_buffs` | Array | `[ Protected ], [ Mad ], [ Twin ]` |
| `base_crit_chance` | Number | `0` |
| `base_health_regen` | Number | `0` |
| `base_health` | Number | `0` |
| `base_initial_mana` | Number | `0` |
| `base_initiative` | Number | `-1, 0` |
| `base_mana_regen` | Number | `999, 0, 3` |
| `base_mana` | Number | `0` |
| `base_movement` | Number | `4` |
| `blocking` | Boolean | `false` |
| `boss_minions_runaway` | Boolean | `false` |
| `can_be_backstabbed` | Boolean | `false` |
| `can_be_champion` | Boolean | `false, true` |
| `can_be_elite` | Boolean | `false` |
| `can_be_overkilled` | Boolean | `false, true` |
| `can_collect_coins` | Boolean | `false, true` |
| `can_eat_food` | Boolean | `false, true` |
| `can_grant_extra_turns` | Boolean | `false` |
| `can_run` | Boolean | `false` |
| `capture_as_cat` | Boolean | `true` |
| `catdata_ignore_skills` | Boolean | `true` |
| `champion` | Boolean | `true` |
| `corpse_health` | Enum/String | `indestructible, 0, 3` |
| `deathpoof_size` | Number | `1` |
| `disallow_items` | Enum/String | `Nuke, all` |
| `disperse_main_turns` | Boolean | `false, true` |
| `dispersed_bonus_turns_before_cats` | Boolean | `false, true` |
| `dispersed_bonus_turns_consider_initiative` | Boolean | `false` |
| `dispersed_bonus_turns` | Number | `2, 0, 3` |
| `divine_shield` | Number | `1, 2, 3` |
| `elements` | Array | `[ Rock ], [ Earth ], [ Dust ]` |
| `elite` | Boolean | `true` |
| `evenly_dispersed_bonus_turns` | Number | `1, 2, 3` |
| `exclude_from_hallucinate` | Boolean | `true` |
| `faction` | Enum/String | `none, enemies, birds` |
| `first_turn_is_main_turn` | Boolean | `true` |
| `flying` | Boolean | `true` |
| `force_not_familiar` | Boolean | `true` |
| `health` | Number | `2, 16, 7` |
| `held_coins` | Number | `5, 0, [ 5 10 ]` |
| `hidden_tag` | Enum/String | `angeljunk, [ bird bonusbird ], the_coven` |
| `hidden_tags` | Enum/String | `terminator_mini, [ terminator_mini dc_cat ]` |
| `hint_no_corpse` | Boolean | `true` |
| `ignore_mouseover` | Boolean | `true` |
| `ignore_tiles` | Boolean | `true` |
| `inanimate_can_receive_specific_statuses` | Array | `[ Burn ]` |
| `inanimate` | Boolean | `true` |
| `inherit_faction` | Boolean | `false, true` |
| `initial_health` | Number | `4, 14, 10` |
| `initiative` | Number | `999, -100, -999` |
| `is_player_cat` | Boolean | `false, true` |
| `kill_required` | Boolean | `false, true` |
| `knockback_immune` | Boolean | `true` |
| `last_turn_is_main_turn` | Boolean | `true` |
| `layer` | Enum/String | `gas, pickups, all` |
| `lock_orientation` | Array | `[ -1, 0 ], [ 0, -1 ], [ -1 0 ]` |
| `mana_matters` | Boolean | `false, true` |
| `mana_regen` | Number | `999` |
| `mana` | Number | `100` |
| `mouseover_priority` | Number | `10` |
| `move_block` | Enum/String | `nothing, everything_even_when_dead` |
| `move_points` | Number | `2` |
| `movement` | Number | `5, 4, 3` |
| `must_start_facing_camera` | Boolean | `false` |
| `pickup_type` | Number | `1` |
| `round_end_bonus_turns` | Number | `1` |
| `round_start_bonus_turns` | Number | `1` |
| `scale` | Number | `1.3` |
| `shield` | Number | `65, 50, 100` |
| `size` | Enum/String | `2x2, gemini, 3x3` |
| `speculative_inanimate` | Boolean | `false` |
| `static` | Boolean | `true` |
| `tag` | Array | `[ cat blob ], animal, rat` |
| `tags` | Array | `[ cat robot ]` |
| `takes_main_turn` | Boolean | `false` |
| `takes_turns` | Boolean | `false, true` |
| `tall` | Boolean | `true` |
| `tile_desire_cost` | Number | `200, 100` |
| `two_fronts_switch` | Boolean | `true` |
| `two_fronts` | Boolean | `true` |
| `type` | Enum/String | `object, boss, cat` |
| `uncapturable` | Boolean | `false, true` |
| `view_bleeding_characters_as_enemies` | Boolean | `true` |
| `view_bugs_as_enemies` | Boolean | `true` |
| `visually_spiky` | Boolean | `true` |
| `weak_threshold` | Number | `1, 5, 0` |

### Context: `round_end_bonusturn_pattern`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_all` | Array | `[ *QueenHippoUppercut QueenHippoAttack move QueenHippoTire ], [ MoonHead_ChewCat MoonHead_CallForHelp MoonHead_RefreshB..., [ MoonHead_CallForHelp MoonHead_RefreshBrace ]` |
| `do_nothing` | Array | `[ ]` |
| `do_one` | Array | `[ **ZaratanaVSWeatherRoar **ZaratanaVSRoar ], [ **PyrophinaVSWeatherRoar **PyrophinaVSRoar ]` |
| `do_priority` | Array | `[ NCReanimate NCGravecrawlFAR ]` |
| `do_random` | Array | `[ TKNG_Spread TKNG_Kneel TKNG_Roulette TKNG_GoAway ], [ SimonSays_Scatter, SimonSays_ComeHere, SimonSays_GoAway ]` |
| `do` | Enum/String | `RallyMaggots, CutterCut, SuckMF` |

### Context: `round_start_bonusturn_pattern`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `do_priority` | Array | `[ MutateAOE SpawnMaggots ]` |

### Context: `sound`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `SE_CatSwishThrow` | Enum/String | `SE_ThrowGrenade` |
| `SE_Cat_ShadowStepIn` | Enum/String | `SE_Terminator_ShadowStepIn` |
| `SE_Cat_ShadowStepOut` | Enum/String | `SE_Terminator_ShadowStepOut` |
| `SE_Cat_StompLegMove` | Enum/String | `SE_Terminator2_WalkLeg, SE_Terminator1_WalkLeg` |
| `SE_Cat_WeaponLower` | Enum/String | `SE_Terminator_WeaponLower` |
| `SE_Cat_WeaponRaise` | Enum/String | `SE_Terminator_WeaponRaise` |
| `SE_Cat_bearHug` | Enum/String | `SE_Terminator_bearHug` |
| `SE_Cat_equipWeapon` | Enum/String | `SE_TerminatorSwapWeapon` |
| `SE_PetRock_Dash` | Enum/String | `SE_PetBoulder_Dash` |
| `alt_sounds` | Array | `[ [ SE_BirdSmall_DyingCall SE_BirdDying_Dove ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Blackbird ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Hummingbird ]` |
| `animation_prefix` | Enum/String | `RattleSnake` |

### Context: `stats`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `charisma` | Number | `5, 8, 9` |
| `constitution` | Number | `5, 8, 9` |
| `dexterity` | Number | `5, 8, 9` |
| `intelligence` | Number | `5, 10, 9` |
| `luck` | Number | `5, 8, 3` |
| `speed` | Number | `5, 2, 7` |
| `strength` | Number | `5, 8, 4` |

### Context: `statuses`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Consumed` | Block | `{ ... }` |

### Context: `statuses_on_enter_form`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `UseAbility` | Enum/String | `KirbySpit` |

### Context: `turns`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `dispersed_bonus_turns` | Number | `1, 2, 0` |
| `evenly_dispersed_bonus_turns` | Number | `1, 2` |
| `round_end_bonus_turns` | Number | `1` |
| `round_start_bonus_turns` | Number | `1` |
| `takes_main_turn` | Boolean | `false, true` |
| `takes_turns` | Boolean | `false, true` |
| `wait_till_next_round_to_update_turns` | Boolean | `true` |

### Context: `virtual_abilities`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CerberubsJumpBlind` | Block | `{ ... }` |
| `CerberubsJumpNormal` | Block | `{ ... }` |
| `CloseConvert` | Block | `{ ... }` |
| `DashRandomly` | Block | `{ ... }` |
| `Escape` | Block | `{ ... }` |
| `FoodMove` | Block | `{ ... }` |
| `ForceTrample` | Block | `{ ... }` |
| `LeapClose` | Block | `{ ... }` |
| `MoveAway` | Block | `{ ... }` |
| `MoveCenter` | Block | `{ ... }` |
| `MoveClose` | Block | `{ ... }` |
| `MoveForBarrage` | Block | `{ ... }` |
| `MoveForDash` | Block | `{ ... }` |
| `MoveForGrass` | Block | `{ ... }` |
| `MoveForPounce` | Block | `{ ... }` |
| `MoveForSpin` | Block | `{ ... }` |
| `MoveForThrow` | Block | `{ ... }` |
| `MoveOneForPuke` | Block | `{ ... }` |
| `MoveSpaced` | Block | `{ ... }` |
| `MoveToHead` | Block | `{ ... }` |
| `MoveTowards` | Block | `{ ... }` |
| `NCGravecrawlFAR` | Block | `{ ... }` |
| `ReturnA` | Block | `{ ... }` |
| `RunFar` | Block | `{ ... }` |
| `SpearRun` | Block | `{ ... }` |
| `SuckMF` | Block | `{ ... }` |
| `TF_TargetAllies` | Block | `{ ... }` |
| `TF_TargetEnemies` | Block | `{ ... }` |
| `Unflip` | Block | `{ ... }` |

---

## Events & Encounters

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `10coins` | Block | `{ ... }` |
| `add_weather` | Enum/String | `SolarFlare` |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_twentyfive, choice_leave, choice_dex_alt` |
| `bad` | Block | `{ ... }` |
| `cha` | Number | `1` |
| `con` | Number | `1` |
| `copy_results` | Enum/String | `examine, smash` |
| `destroy` | Block | `{ ... }` |
| `dex` | Number | `1` |
| `gain_familiar` | Enum/String | `Toad` |
| `get_item_from_pool` | Enum/String | `chapter_rare, food` |
| `good` | Block | `{ ... }` |
| `ignore` | Block | `{ ... }` |
| `int` | Number | `1` |
| `intro` | Block | `{ ... }` |
| `label` | String | `"EVENT_PICK_ANSW", "EVENT_OPEN_ANSW", "EVENT_LEAVE_ANSW"` |
| `lck` | Number | `1` |
| `main` | Block | `{ ... }` |
| `next_event_bonus` | Number | `2` |
| `prompt` | String | `"EVENT_BEGGAR_NOTENOUGHMONEY", "EVENT_ABEGGAR_REW2", "EVENT_TRASHBIN_REW3"` |
| `requirements` | Block | `{ ... }` |
| `requires_flag` | Enum/String | `SolarFlareUnlocked` |
| `reward` | Block | `{ ... }` |
| `self_status_next_fight` | Block | `{ ... }` |
| `set_frame` | Number | `2, 5, 4` |
| `spd` | Number | `1` |
| `stat_max` | Number | `25, 15, 10` |
| `stat_min` | Number | `25, 15, 10` |
| `stat` | Enum/String | `lck, none, dex` |
| `str` | Number | `1` |
| `weight` | Number | `15, .25, .5` |

### Context: `10coins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_ten` |
| `get_item_from_pool` | Enum/String | `chapter_rare` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |
| `set_frame` | Number | `2` |
| `stat_max` | Number | `10` |
| `stat_min` | Number | `10` |
| `stat` | Enum/String | `coins` |
| `weight` | Number | `10` |

### Context: `5coins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_one` |
| `get_item_from_pool` | Enum/String | `chapter_rare` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |
| `set_frame` | Number | `2` |
| `stat_max` | Number | `5` |
| `stat_min` | Number | `5` |
| `stat` | Enum/String | `coins` |
| `weight` | Number | `5` |

### Context: `CharacterTypeGainsStatusAtBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Fear` | Number | `1` |
| `Stun` | Number | `1` |
| `tag` | Enum/String | `robot, rat` |

### Context: `KillEnemyOfTypeAtBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `enemy_type` | Enum/String | `any, cat` |
| `fallback_spawn` | Array | `[ TomTom Kitten CatCaller Mangy ]` |

### Context: `StatusRandomEnemiesOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `2` |
| `Fear` | Number | `2, 3` |
| `count` | Number | `1, 99, 2` |

### Context: `a`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"class ability pool", "1 injury", "1"` |
| `stat` | Enum/String | `none` |

### Context: `activate_p`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_OBELISK_CORE_ACTIVATE_ANSW, QEVENT_OBELISK_MOON_ACTIVATE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest, none` |

### Context: `activate_z`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_OBELISK_CORE_ACTIVATE_ANSW, QEVENT_OBELISK_MOON_ACTIVATE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest, none` |

### Context: `altar_sacrifice`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"king intro"` |
| `stat` | Enum/String | `none` |

### Context: `arm`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_ARMINSIDE_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `attach_amplifier`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_THEHEAD_AMPLIFIER_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `attach_antenna`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_GLOWINGORB_ANTENNA_ANSW, QEVENT_VOLCANO_ANTENNA_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `attach_leech`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_THROBBINGARTERY_ATTACH_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `attack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_ATTACK_ANSW", "EVENT_BREAK_ANSW", "EVENT_BASH_ANSW"` |
| `rare` | Block | `{ ... }` |
| `stat` | Enum/String | `str` |

### Context: `b`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"many injuries", "5", "set ability pool"` |
| `stat` | Enum/String | `none` |

### Context: `bad`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `battle` | String | `"events/Death.lvl"` |
| `conditional_reward` | Block | `{ ... }` |
| `cutscene` | Block | `{ ... }` |
| `event_now_same_cat` | Enum/String | `StevenFetus, random` |
| `event_now` | Enum/String | `StacyMutant2, StacyMutant3, StacyMutant4` |
| `gain_disorder_from_pool` | Enum/String | `diseases, all_disorders` |
| `gain_immortal_familiar` | Enum/String | `CharmedFlea` |
| `get_parasite_from_pool` | Enum/String | `parasites` |
| `get_parasite` | Enum/String | `CursedRock` |
| `injury` | Enum/String | `con, dex, str` |
| `kill` | Enum/String | `cat` |
| `lose_item` | Enum/String | `parasite` |
| `next_event_bonus` | Number | `-1` |
| `party_random_mutation_from_set` | Block | `{ ... }` |
| `permanent_stats` | Block | `{ ... }` |
| `play_animation` | Array | `[ resultLeave 0 ], resultVeryBad, resultHole` |
| `prompt` | String | `"QEVENT_STACYMUTANT1_REW4", "QEVENT_STACYMUTANT1_REW4_B", "EVENT_CLOSEDWINDOW_REW7"` |
| `reward` | Block | `{ ... }` |
| `select_item_from_pool_for_cutscene_only` | Enum/String | `glitched_items` |
| `self_status_next_fight` | Block | `{ ... }` |
| `set_frame` | Number | `2, 4, 3` |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_StacyMutant` |

### Context: `bash`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BASH_ANSW", "EVENT_BASHOPEN_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `str` |

### Context: `bash_past_alt`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BASH_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `str` |

### Context: `bite`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_con` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_WALLOFFLESH_BITE_ANSW, QEVENT_WALLOFFLESH_BITE2_ANSW, QEVENT_THROBBINGARTERY_BITE_ANSW` |
| `stat` | Enum/String | `con, str` |

### Context: `bite_it_off`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BIGTOE_BITE_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `blue`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `copy_results` | Enum/String | `red` |
| `fixed_chance` | Number | `50%` |
| `label` | String | `"EVENT_BLUE_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `blue_needle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_NEEDLES_BLUE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `lck` |

### Context: `body`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_CURSEBODY` |
| `stat` | Enum/String | `none` |

### Context: `boogers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BEEPIS_ANSW", "EVENT_BOOGERS_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `book`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SOMEOLDBOOK_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `brace`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW2"` |
| `stat` | Enum/String | `none` |

### Context: `break_ice`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_FROZENHUMANOID_BREAKICE_ANSW"` |

### Context: `break_lock`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_LOCKEDCRATE_BREAK_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `bribe`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_BRIBE_ANSW` |
| `stat` | Enum/String | `con` |

### Context: `button`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `copy_results` | Enum/String | `lever` |
| `fixed_chance` | Number | `50%` |
| `label` | String | `"EVENT_PUSHBUTTON_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `buy1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_one` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BUY_ANSW"` |
| `prompt` | String | `"EVENT_TRACY_REW4"` |
| `self_status_next_fight` | Block | `{ ... }` |
| `stat_max` | Number | `1` |
| `stat_min` | Number | `1` |
| `stat` | Enum/String | `coins` |
| `weight` | Number | `1` |

### Context: `c`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"specific disorder", "class passive pool", "all (symmetric)"` |
| `stat` | Enum/String | `none` |

### Context: `catch`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CATCH_ANSW"` |
| `stat` | Enum/String | `spd` |

### Context: `challenge_to_game`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DEATH_CHALLENGE_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `chaos_ending`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"chaos ending"` |
| `stat` | Enum/String | `none` |

### Context: `chapter_cutscene`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"chap"` |
| `stat` | Enum/String | `none` |

### Context: `charm`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_CHARM_ANSW, "EVENT_CHARM_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `cha` |

### Context: `charm_past_alt`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CHARM_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `cha` |

### Context: `climb`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CLIMB_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `comfort`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_COMFORT_ANSW"` |
| `stat` | Enum/String | `cha` |

### Context: `common`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `add_weather` | Enum/String | `RestlessDead, Sandstorm` |
| `ally_ambush_next_fights` | Number | `1, 2` |
| `ambush_next_basic_fights` | Number | `1` |
| `clear_adventure_token` | Enum/String | `AdventureToken_BlueNeedle, AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle` |
| `clear_result_animation` | Number | `1` |
| `conditional_reward` | Block | `{ ... }` |
| `damage` | Number | `5, [ 5 10 ], [ 3 6 ]` |
| `decrement_legacy_counter` | Enum/String | `WorldEventLegacyCounter_CrackInTheWall` |
| `event_now_same_cat` | Enum/String | `random, ElephantsFootCloser, UnmarkedGrave` |
| `event_now` | Enum/String | `random` |
| `full_heal` | Number | `1` |
| `gain_coins` | Array | `[ 5 15 ], 5, [ 4 8 ]` |
| `gain_disorder_from_pool` | Enum/String | `physical_disorders, all_disorders, mental_disorders` |
| `gain_disorder` | Enum/String | `Scatological, IntestinalProlapse, Stinky` |
| `gain_familiar` | Enum/String | `Snake, CharmedPinky, CharmedFetus` |
| `gain_food` | Number | `-5, [ 1 4 ], [ 5 10 ]` |
| `get_and_equip_item` | Enum/String | `Catnip` |
| `get_item_from_pool` | Enum/String | `consumables, [ CarvingKnife RazorBlade ButterflyKnife ], { ... }` |
| `get_item` | Enum/String | `EnchantingPoop, CatnipBig, SeedBombs` |
| `get_parasite_from_pool` | Enum/String | `parasites, [ AmoebaHat AmoebaNeck AmoebaFace ], [ CrimsonMask_Cursed RedCap_Cursed PoundOfFlesh_Cursed ]` |
| `get_parasite` | Enum/String | `PawShards, CursedHairball, EnchantingPoop_Cursed` |
| `global_effect_next_fight` | Block | `{ ... }` |
| `heal_disorder` | Number | `1` |
| `heal_injury` | Number | `1` |
| `heal` | Number | `1, 10, 3` |
| `increment_legacy_counter` | Enum/String | `WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyCounter_VolcanoSacrifices, WorldEventLegacyToken_StartDigging` |
| `injury` | Enum/String | `spd, radiated, str` |
| `kill` | Enum/String | `cat` |
| `learn_ability_from_pool` | Enum/String | `AnyUnlocked` |
| `lose_item` | Enum/String | `inventory, weapon, equipped` |
| `lose_specific_item` | Enum/String | `SlagTight` |
| `mutation` | Block | `{ ... }` |
| `next_event_bonus` | Number | `1, 2, -1` |
| `next_event_from_set` | Block | `{ ... }` |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN", "EVENT_LOCKEDDOOR_PROMPT1", "EVENT_MYSTERIOUSTENT_PROMPT"` |
| `party_damage` | Number | `5, [ 1 6 ], 3` |
| `party_heal_disorder` | Number | `2` |
| `party_heal` | Number | `1, 100%, 3` |
| `party_permanent_stats_exclude_self` | Block | `{ ... }` |
| `party_status_next_fight` | Block | `{ ... }` |
| `permanent_stats` | Block | `{ ... }` |
| `play_animation` | Enum/String | `resultLeave, [ resultLeave 0 ], resultConfused` |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW5", "EVENT_CLOSEDWINDOW_REW1", "EVENT_CLOSEDWINDOW_REW3"` |
| `random_mutation_from_set` | Block | `{ ... }` |
| `random_mutation` | Number | `1, 2, { ... }` |
| `random_pool` | Array | `[ { prompt "EVENT_KNIFEINTHEWALL_REW1" } { prompt "EVENT_..., [ { permanent_stats { str -1 } } { permanent_stats { dex ..., [ { party_heal 5 gain_food [ 2 4 ]` |
| `self_damage` | Number | `1, 99%, 50%` |
| `self_heal` | Number | `10` |
| `self_status_next_fight` | Block | `{ ... }` |
| `set_adventure_token` | Enum/String | `MysteriousStranger_HasLostFinger, AdventureToken_UnmarkedGraveForced, HasPlayedMysteriousStranger` |
| `set_frame` | Number | `2, 5, 3` |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_HasRunFromDeath` |
| `shop_now` | Enum/String | `Event_SmallShop, TreasureEasy` |
| `spawn_unit_next_fight` | Block | `{ ... }` |
| `spin` | Enum/String | `again` |
| `upgrade_ability` | Enum/String | `random` |

### Context: `communicate`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_COMMUNICATE_ANSW"` |
| `stat` | Enum/String | `cha` |

### Context: `concheck`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `conditional_reward`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `else` | Block | `{ ... }` |
| `prompt` | String | `"EVENT_CATSINHEAT_REW8", "EVENT_CATSINHEAT_REW6"` |
| `requirements` | Block | `{ ... }` |
| `reward` | Block | `{ ... }` |

### Context: `copy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_COPY_ANSW"` |

### Context: `counter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW2"` |
| `stat` | Enum/String | `none` |

### Context: `crack_open`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CRACKOPEN_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `cross`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CROSS_ANSW"` |

### Context: `cut_wires`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CUTWIRES_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `cutscene`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cutscene` | String | `"chaos_ending_good", "desert_intro", "time_machine"` |
| `skip_result_screen` | Boolean | `true` |

### Context: `d`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"all (asymmetric)", "set passive pool", "pool disorder"` |
| `stat` | Enum/String | `none` |

### Context: `damage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DAMAGE_ANSW", "EVENT_BAHPHOMET_HEALTH_ANSW", "QEVENT_STACYMUTANT3_ANSW2"` |
| `stat` | Enum/String | `none` |

### Context: `damage_1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DEMONICIDOL_1DAMAGE_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `damage_full`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DEMONICIDOL_FULLDAMAGE_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `damage_half`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DEMONICIDOL_HALFDAMAGE_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `desert_cutscene`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"desert"` |
| `stat` | Enum/String | `none` |

### Context: `destroy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DESTROY_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `dexcheck`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `dig`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DIG_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `str` |

### Context: `disarm`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DISARM_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `dive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DIVE_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `donate`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"Donate"` |
| `stat` | Enum/String | `none` |

### Context: `donate_10`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_ten` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DONATE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat_max` | Number | `10` |
| `stat_min` | Number | `10` |
| `stat` | Enum/String | `coins` |

### Context: `donate_15`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_ten` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DONATE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat_max` | Number | `15` |
| `stat_min` | Number | `15` |
| `stat` | Enum/String | `coins` |

### Context: `donate_20`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_twentyfive` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DONATE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat_max` | Number | `20` |
| `stat_min` | Number | `20` |
| `stat` | Enum/String | `coins` |

### Context: `donate_5`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_one` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DONATE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat_max` | Number | `5` |
| `stat_min` | Number | `5` |
| `stat` | Enum/String | `coins` |

### Context: `double`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW1"` |
| `stat` | Enum/String | `none` |

### Context: `drink`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_DRINK_ANSW, "EVENT_DRINK_ANSW"` |
| `stat` | Enum/String | `lck, con` |

### Context: `eat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_EAT_ANSW", EVENT_EAT_ANSW, "EVENT_DRINK_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `eat_meat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_LEAKINGMEAT_EAT_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `else`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `conditional_reward` | Block | `{ ... }` |
| `damage` | Number | `50%` |
| `event_now_same_cat` | Enum/String | `Needles` |
| `event_now` | Enum/String | `Mirage` |
| `gain_disorder` | Enum/String | `AcidReflux, Soulless` |
| `get_item_from_pool` | Array | `[ LeafyMask LeafyHat LeafyNecklace DinoHat DinoMask DinoN...` |
| `next_event_bonus` | Number | `1` |
| `party_damage` | Number | `1, 5, [ 10 15 ]` |
| `prompt` | String | `"QEVENT_STACYMUTANT1_QUES1", "EVENT_MIRAGE_REW3", "EVENT_MIRAGE_REW4"` |
| `random_mutation` | Block | `{ ... }` |
| `random_pool` | Array | `[ { get_item Catnip } { gain_food [ 2 5 ], [ { get_item FrozenHat get_item FrozenMask get_item Froze...` |
| `self_status_next_fight` | Block | `{ ... }` |
| `set_adventure_token` | Enum/String | `AdventureToken_Mirage1` |
| `set_frame` | Number | `4, 3` |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_HasRunFromDeath` |

### Context: `enter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `hint_chapter_exit` | Enum/String | `dimensionx` |
| `label` | String | `"EVENT_HOLEINTHEEARTH_ENTER_ANSW", "EVENT_ENTER_ANSW", QEVENT_DIMENSIONXPORTAL_ENTER_ANSW` |
| `stat` | Enum/String | `lck, con, none` |

### Context: `enter_crater`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSCRATER_ENTER_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `examine`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `copy_results` | Enum/String | `smash, open` |
| `gain_coins` | Array | `[ 5 15 ]` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_EXAMINE_ANSW, "EVENT_EXAMINE_ANSW"` |
| `stat` | Enum/String | `lck, int` |

### Context: `face`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GIFTOFGLORG_FACE_ANSW"` |

### Context: `fiddle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_EXAMINE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `fight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_FIGHT_ANSW", EVENT_FIGHT_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `str` |

### Context: `fill_jar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_THEHEAD_FILLJAR_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `find`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GOLEMFIND_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `find_another_way`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_AROUND", "EVENT_FINDANOTHERWAY_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `fire`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW1"` |
| `stat` | Enum/String | `none` |

### Context: `flush_yourself`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_FLUSHYOURSELF_ANSW"` |
| `requirements` | Block | `{ ... }` |

### Context: `follow`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_FOLLOW_ANSW"` |
| `stat` | Enum/String | `spd` |

### Context: `free`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_FREE_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `future`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `hint_chapter_exit` | Enum/String | `future` |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_FUTURE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `gain_clone_familiar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `PlayerCat_MachineClone` |

### Context: `gain_familiar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `initial_health` | Number | `10` |
| `object` | Enum/String | `CharmedCaveBaby` |

### Context: `get_item_from_pool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Enum/String | `chapter_common, chapter, chapter_rare` |
| `prompt` | String | `"EVENT_FRANK2_REW4"` |
| `restrict` | Array | `[ weapon, trinket, armor ], consumables, trinket` |

### Context: `give_parasite`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BODYOFGLORG_PARASITE_ANSW"` |
| `requirements` | Block | `{ ... }` |

### Context: `global_effect_next_fight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CharacterTypeGainsStatusAtBattleStart` | Block | `{ ... }` |
| `Fights` | Number | `1, 3` |
| `KillEnemyOfTypeAtBattleStart` | Block | `{ ... }` |
| `StatusRandomEnemiesOnBattleStart` | Block | `{ ... }` |

### Context: `go_around`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GOAROUND_ANSW", "EVENT_TAKELONGWAY_ANSW"` |
| `stat` | Enum/String | `lck, none, spd` |

### Context: `good`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `add_weather` | Enum/String | `MeteorShower, GeomagneticStorm, SolarFlare` |
| `ally_ambush_next_fights` | Number | `1` |
| `begin_chapter` | Enum/String | `iceage.gon, dimensionx.gon, future.gon` |
| `clear_surviving_kaiju` | Enum/String | `pyrophina, zaratana` |
| `clone_self_to_party` | Number | `1` |
| `complete_item_quest` | Enum/String | `GuillotinasHead, ThrobbingGristle, PutridLeech` |
| `conditional_reward` | Block | `{ ... }` |
| `copy_items_to_party` | Number | `1` |
| `copy_party_items` | Number | `1` |
| `cutscene_on_exit` | Enum/String | `king_intro` |
| `cutscene` | String | `"chapterintros/bunker", { ... }` |
| `event_now_same_cat` | Enum/String | `random, BodyOfGlorg_Gift, MysteriousTomb1` |
| `event_now` | Enum/String | `StacyMutant2, StacyMutant3, StacyMutant4` |
| `full_heal` | Number | `1` |
| `gain_clone_familiar` | Block | `{ ... }` |
| `gain_disorder_from_pool` | Enum/String | `all_disorders` |
| `gain_disorder` | Enum/String | `Depression, Anxiety, Gargantuan` |
| `gain_food` | Array | `[ 10 20 ]` |
| `get_full_item_set_from_pool` | Enum/String | `common` |
| `get_item_from_pool` | Enum/String | `bloody_items, glitched_items, godly_items` |
| `get_item` | Enum/String | `MomsKnife, CryogenicTimeChamber_Full, HumanBrain` |
| `get_parasite` | Enum/String | `Beepis, Cunch, Feebis` |
| `global_effect_next_fight` | Block | `{ ... }` |
| `heal_disorder` | Number | `1, Anxiety, mental_disorders` |
| `heal_injury` | Number | `1, 5` |
| `heal` | Number | `50%` |
| `increment_legacy_counter` | Enum/String | `WorldEventLegacyCounter_Jack, WorldEventLegacyCounter_SealedCrypt, WorldEventLegacyCounter_TestLegacyFoo` |
| `injury` | Enum/String | `random` |
| `kill` | Enum/String | `cat` |
| `learn_ability_from_pool` | Enum/String | `Necromancer, [ Smack Meow Hiss ]` |
| `learn_passive_from_pool` | Array | `[ MiniMe SkillShare ], Necromancer` |
| `level_up` | Enum/String | `self, all` |
| `lose_item` | Enum/String | `parasite` |
| `lose_specific_item` | Enum/String | `PyrophinasCollar, ThrobbingGristle, PutridLeech` |
| `mutation` | Block | `{ ... }` |
| `next_event_bonus` | Number | `1` |
| `next_event_from_set` | Block | `{ ... }` |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSTOMB1_END", "EVENT_MYSTERIOUSTOMB_END"` |
| `party_gain_disorder_from_pool` | Array | `[ Dwarfism ], [ Gigantism ]` |
| `play_animation` | Enum/String | `resultVeryGood, [ resultLeave 0 ], resultHole` |
| `prompt` | String | `"EVENT_SEALEDCRYPT_LEAVE", "EVENT_TRASHBIN_REW1", "EVENT_CLOSEDWINDOW_REW8"` |
| `random_mutation` | Number | `1, 5, 10` |
| `random_pool_consider_luck` | Array | `[ { prompt "EVENT_VENDINGMACHINE_REW4" set_frame 5 gain_d..., [ { prompt "EVENT_TRACY_REW1" weight 1 get_parasite_from_..., [ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo...` |
| `random_pool` | Array | `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { prompt "EVENT_TRAVERSETHENECROPOLIS_REW1" play_animat..., [ { weight 95 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran...` |
| `rare` | Block | `{ ... }` |
| `reward` | Block | `{ ... }` |
| `scramble_abilities` | Enum/String | `all` |
| `scramble_passives` | Enum/String | `all` |
| `set_adventure_token` | Enum/String | `StacyMutant_Thorns, StacyMutant_Holy, StacyMutant_Brace` |
| `set_frame` | Number | `2, 4, 3` |
| `set_legacy_token` | Enum/String | `mapflag_ThrobbingArteryDone, MeatWorldQuest_Leech, WorldEventLegacyToken_StacyMutant` |
| `shop_now` | Enum/String | `Event_SmallShop` |
| `transform_item` | Array | `[ JarOfRadiation JarOfRadiatedBlood ], [ JarOfRadiatedBlood JarOfChaos ], [ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ]` |
| `trigger_adventure_unlock` | Enum/String | `time_machine_quest_finalstep, legacy_event_unlock_momsknife, meat_world_open` |
| `trigger_butterfly_effect` | Number | `1` |
| `unlock_item_quest` | Enum/String | `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` |
| `upgrade_ability` | Enum/String | `random` |
| `upgrade_passive` | Enum/String | `random` |

### Context: `hack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_HACK_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `head`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GIFTOFGLORG_HEAD_ANSW"` |

### Context: `holy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW3"` |
| `stat` | Enum/String | `none` |

### Context: `home`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `hint_chapter_exit` | Enum/String | `home` |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_HOME_ANSW` |
| `stat` | Enum/String | `none` |

### Context: `hp`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW1"` |
| `stat` | Enum/String | `none` |

### Context: `ice`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW2"` |
| `stat` | Enum/String | `none` |

### Context: `ignore`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `hint_chapter_exit` | Enum/String | `home` |
| `label` | String | `"EVENT_LEAVE_ANSW", "EVENT_IGNORE_ANSW", EVENT_IGNORE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `con, none` |

### Context: `infinite`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `hint_chapter_exit` | Enum/String | `endoftime` |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_THEEND_INFINITE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `inspect`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_INSPECT_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `intcheck`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `intimidation`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_INTIMIDATION_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `intro`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cat_choice` | Enum/String | `random` |
| `choose_cat_with_highest_stat` | Enum/String | `int` |
| `choose_cat_with_item_slot_equipped` | Enum/String | `weapon` |
| `choose_cat_with_item` | Enum/String | `GuillotinasHead, ThrobbingGristle, PutridLeech` |
| `choose_cat_with_min_health` | Number | `75%` |
| `choose_cat_with_most_injuries` | Boolean | `true` |
| `choose_cat_with_parasite` | Boolean | `true` |
| `different_from_last_x_cats` | Number | `1, 2, 3` |
| `event_clip` | Enum/String | `NonWheelEvent` |
| `set_frame` | Number | `1` |
| `subject_clip` | Enum/String | `EventSubject` |
| `subject_frame_inner` | Number | `2, 4` |
| `subject_frame` | Enum/String | `trashcan, mouse_nest, brokenwindow` |
| `title` | String | `"EVENT_TRASHBIN_NAME", "EVENT_MOUSENEST_NAME", "EVENT_CLOSEDWINDOW_NAME"` |

### Context: `investigate`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_INVESTIGATE_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `itchies`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `label` | String | `"EVENT_ITCHIES_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `join`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_JOININ_ANSW"` |
| `stat` | Enum/String | `cha` |

### Context: `jump`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |
| `stat` | Enum/String | `spd` |

### Context: `jump_over`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `keep_going`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_KEEPGOING_ANSW"` |

### Context: `kiss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_KISS_ANSW"` |
| `stat` | Enum/String | `cha` |

### Context: `kiss_meat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_LEAKINGMEAT_KISS_ANSW"` |
| `stat` | Enum/String | `cha` |

### Context: `knife`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"Get a knife"` |
| `stat` | Enum/String | `none` |

### Context: `leave`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_IGNORE_ANSW", "EVENT_WALKAWAY_ANSW", "EVENT_LEAVE_ANSW"` |
| `stat` | Enum/String | `lck, none, spd` |

### Context: `leave_it_in`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW2"` |
| `stat` | Enum/String | `none` |

### Context: `leave_party_temporarily`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `fights_skipped` | Number | `1, 0` |
| `return_as` | Enum/String | `enemy` |
| `return_during` | Enum/String | `boss` |

### Context: `leg`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_LEGINSIDE_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `lever`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `fixed_chance` | Number | `50%` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_PULLLEVER_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `lick`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_GLOWINGORB_LICK_ANSW, "EVENT_GOLEMLICK_ANSW", "EVENT_LICK_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `cha, con, none` |

### Context: `lick_alt`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_LICK_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `con` |

### Context: `lightning`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW3"` |
| `stat` | Enum/String | `none` |

### Context: `listen`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_LISTEN_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `looks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_LOOKS` |
| `stat` | Enum/String | `none` |

### Context: `loot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc, choice_dex_alt` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_DEADKING_LOOTCORPSE_ANSW, "EVENT_LOOT_ANSW", EVENT_LOOT_ANSW` |
| `rare` | Block | `{ ... }` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `lck, dex` |

### Context: `loot_heart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_DEADKING_TAKEHEART_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `main`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `add_weather` | Enum/String | `MeteorShower` |
| `bad` | Block | `{ ... }` |
| `gain_familiar` | Enum/String | `Snake` |
| `goto` | Enum/String | `end` |
| `leave` | Block | `{ ... }` |
| `max_options` | Number | `2, 3` |
| `next_event_from_set` | Enum/String | `Tragedy` |
| `options` | Block | `{ ... }` |
| `outcome` | Block | `{ ... }` |
| `party_heal` | Number | `3` |
| `party_permanent_stats` | Block | `{ ... }` |
| `play_animation` | Enum/String | `resultVeryGood` |
| `prompt` | String | `"EVENT_MOUSENEST_QUES", "EVENT_TRASHBIN_QUES", "EVENT_CLOSEDWINDOW_QUES"` |
| `rare` | Block | `{ ... }` |
| `requires_flag` | Enum/String | `MeteorShowerUnlocked` |
| `self_damage` | Array | `[ 4 8 ]` |
| `self_status_next_fight` | Block | `{ ... }` |
| `set_frame` | Number | `15, 16, 3` |
| `setup` | Block | `{ ... }` |
| `shop_now` | Enum/String | `Event_RareShop` |
| `shuffle_options` | Boolean | `true` |
| `weight` | Enum/String | `.25, .5` |

### Context: `makeup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MAKEUP_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `mind`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_CURSEMIND` |
| `stat` | Enum/String | `none` |

### Context: `move_closer`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_ELEPHANTSFOOT_ANSW", "EVENT_ELEPHANTSFOOTCLOSER_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `mutation`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `arm1` | Number | `-2` |
| `arms` | Number | `900` |
| `body` | Number | `900` |
| `ear1` | Number | `-2` |
| `ears` | Number | `-2, 328, 310` |
| `eye1` | Number | `-1, -2` |
| `eye2` | Number | `-1` |
| `eyebrow1` | Number | `-2` |
| `eyebrows` | Number | `440, -2, 900` |
| `eyes` | Number | `-2, 702, 900` |
| `head` | Number | `305, 900` |
| `leg1` | Number | `-2` |
| `legs` | Number | `322, 900` |
| `mouth` | Number | `-2, 900, 705` |
| `tail` | Number | `900` |

### Context: `neck`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GIFTOFGLORG_NECK_ANSW"` |

### Context: `next_event_from_set`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count` | Number | `1, 4, 3` |
| `event` | Enum/String | `Tragedy, Death` |
| `same_cat` | Boolean | `true` |

### Context: `nothanks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_NOTHANKS_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `open`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `copy_results` | Enum/String | `smash` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_OPEN_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `options`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `5coins` | Block | `{ ... }` |
| `a` | Block | `{ ... }` |
| `activate_p` | Block | `{ ... }` |
| `activate_z` | Block | `{ ... }` |
| `altar_sacrifice` | Block | `{ ... }` |
| `arm` | Block | `{ ... }` |
| `attach_amplifier` | Block | `{ ... }` |
| `attach_antenna` | Block | `{ ... }` |
| `attach_leech` | Block | `{ ... }` |
| `attack` | Block | `{ ... }` |
| `b` | Block | `{ ... }` |
| `bad` | Block | `{ ... }` |
| `bash_past_alt` | Block | `{ ... }` |
| `bash` | Block | `{ ... }` |
| `bite_it_off` | Block | `{ ... }` |
| `bite` | Block | `{ ... }` |
| `blue_needle` | Block | `{ ... }` |
| `blue` | Block | `{ ... }` |
| `body` | Block | `{ ... }` |
| `boogers` | Block | `{ ... }` |
| `book` | Block | `{ ... }` |
| `brace` | Block | `{ ... }` |
| `break_ice` | Block | `{ ... }` |
| `break_lock` | Block | `{ ... }` |
| `bribe` | Block | `{ ... }` |
| `button` | Block | `{ ... }` |
| `buy1` | Block | `{ ... }` |
| `c` | Block | `{ ... }` |
| `catch` | Block | `{ ... }` |
| `challenge_to_game` | Block | `{ ... }` |
| `chaos_ending` | Block | `{ ... }` |
| `chapter_cutscene` | Block | `{ ... }` |
| `charm_past_alt` | Block | `{ ... }` |
| `charm` | Block | `{ ... }` |
| `climb` | Block | `{ ... }` |
| `comfort` | Block | `{ ... }` |
| `communicate` | Block | `{ ... }` |
| `concheck` | Block | `{ ... }` |
| `copy` | Block | `{ ... }` |
| `counter` | Block | `{ ... }` |
| `crack_open` | Block | `{ ... }` |
| `cross` | Block | `{ ... }` |
| `cut_wires` | Block | `{ ... }` |
| `d` | Block | `{ ... }` |
| `damage_1` | Block | `{ ... }` |
| `damage_full` | Block | `{ ... }` |
| `damage_half` | Block | `{ ... }` |
| `damage` | Block | `{ ... }` |
| `desert_cutscene` | Block | `{ ... }` |
| `destroy` | Block | `{ ... }` |
| `dexcheck` | Block | `{ ... }` |
| `dig` | Block | `{ ... }` |
| `disarm` | Block | `{ ... }` |
| `dive` | Block | `{ ... }` |
| `donate_10` | Block | `{ ... }` |
| `donate_15` | Block | `{ ... }` |
| `donate_20` | Block | `{ ... }` |
| `donate_5` | Block | `{ ... }` |
| `donate` | Block | `{ ... }` |
| `double` | Block | `{ ... }` |
| `drink` | Block | `{ ... }` |
| `eat_meat` | Block | `{ ... }` |
| `eat` | Block | `{ ... }` |
| `enter_crater` | Block | `{ ... }` |
| `enter` | Block | `{ ... }` |
| `examine` | Block | `{ ... }` |
| `face` | Block | `{ ... }` |
| `fiddle` | Block | `{ ... }` |
| `fight` | Block | `{ ... }` |
| `fill_jar` | Block | `{ ... }` |
| `find_another_way` | Block | `{ ... }` |
| `find` | Block | `{ ... }` |
| `fire` | Block | `{ ... }` |
| `flush_yourself` | Block | `{ ... }` |
| `follow` | Block | `{ ... }` |
| `free` | Block | `{ ... }` |
| `future` | Block | `{ ... }` |
| `gain_familiar` | Enum/String | `Squirrel` |
| `get_item_from_pool` | Enum/String | `flesh_items, any_chapter` |
| `give_parasite` | Block | `{ ... }` |
| `go_around` | Block | `{ ... }` |
| `hack` | Block | `{ ... }` |
| `head` | Block | `{ ... }` |
| `holy` | Block | `{ ... }` |
| `home` | Block | `{ ... }` |
| `hp` | Block | `{ ... }` |
| `ice` | Block | `{ ... }` |
| `ignore` | Block | `{ ... }` |
| `infinite` | Block | `{ ... }` |
| `inspect` | Block | `{ ... }` |
| `intcheck` | Block | `{ ... }` |
| `intimidation` | Block | `{ ... }` |
| `investigate` | Block | `{ ... }` |
| `itchies` | Block | `{ ... }` |
| `join` | Block | `{ ... }` |
| `jump_over` | Block | `{ ... }` |
| `jump` | Block | `{ ... }` |
| `keep_going` | Block | `{ ... }` |
| `kiss_meat` | Block | `{ ... }` |
| `kiss` | Block | `{ ... }` |
| `knife` | Block | `{ ... }` |
| `leave_it_in` | Block | `{ ... }` |
| `leave` | Block | `{ ... }` |
| `leg` | Block | `{ ... }` |
| `lever` | Block | `{ ... }` |
| `lick_alt` | Block | `{ ... }` |
| `lick` | Block | `{ ... }` |
| `lightning` | Block | `{ ... }` |
| `listen` | Block | `{ ... }` |
| `looks` | Block | `{ ... }` |
| `loot_heart` | Block | `{ ... }` |
| `loot` | Block | `{ ... }` |
| `makeup` | Block | `{ ... }` |
| `mind` | Block | `{ ... }` |
| `move_closer` | Block | `{ ... }` |
| `neck` | Block | `{ ... }` |
| `nothanks` | Block | `{ ... }` |
| `open` | Block | `{ ... }` |
| `outsmart` | Block | `{ ... }` |
| `past` | Block | `{ ... }` |
| `patch_up` | Block | `{ ... }` |
| `pick_lock` | Block | `{ ... }` |
| `pilfer` | Block | `{ ... }` |
| `pirouette` | Block | `{ ... }` |
| `place_gristle` | Block | `{ ... }` |
| `play_animation` | Enum/String | `resultGood` |
| `play` | Block | `{ ... }` |
| `poop` | Block | `{ ... }` |
| `power` | Block | `{ ... }` |
| `print` | Block | `{ ... }` |
| `prompt` | String | `"EVENT_TRACY_REW5", "EVENT_TRAVERSETHENECROPOLIS_REW6"` |
| `protection` | Block | `{ ... }` |
| `pull_it_out` | Block | `{ ... }` |
| `pull_lever` | Block | `{ ... }` |
| `pull` | Block | `{ ... }` |
| `purify` | Block | `{ ... }` |
| `push_buttons` | Block | `{ ... }` |
| `push_through` | Block | `{ ... }` |
| `put_in_coins` | Block | `{ ... }` |
| `put_out_of_misery` | Block | `{ ... }` |
| `rare` | Block | `{ ... }` |
| `reach_inside` | Block | `{ ... }` |
| `read` | Block | `{ ... }` |
| `receive` | Block | `{ ... }` |
| `red_needle` | Block | `{ ... }` |
| `red` | Block | `{ ... }` |
| `reflect` | Block | `{ ... }` |
| `remove_the_nail` | Block | `{ ... }` |
| `remove` | Block | `{ ... }` |
| `repair_quest` | Block | `{ ... }` |
| `repair` | Block | `{ ... }` |
| `repell` | Block | `{ ... }` |
| `rest` | Block | `{ ... }` |
| `revive` | Block | `{ ... }` |
| `rub` | Block | `{ ... }` |
| `run_again` | Block | `{ ... }` |
| `run_away` | Block | `{ ... }` |
| `run` | Block | `{ ... }` |
| `sacrifice_full_favor` | Block | `{ ... }` |
| `sacrifice_normal` | Block | `{ ... }` |
| `sacrifice_partial_favor` | Block | `{ ... }` |
| `sacrifice_quest` | Block | `{ ... }` |
| `sacrifice` | Block | `{ ... }` |
| `scale` | Block | `{ ... }` |
| `scream` | Block | `{ ... }` |
| `shake` | Block | `{ ... }` |
| `skip` | Block | `{ ... }` |
| `slip_through` | Block | `{ ... }` |
| `smash` | Block | `{ ... }` |
| `sneak_by` | Block | `{ ... }` |
| `sneak_past_alt` | Block | `{ ... }` |
| `sneak` | Block | `{ ... }` |
| `soul` | Block | `{ ... }` |
| `speed` | Block | `{ ... }` |
| `surprise` | Block | `{ ... }` |
| `sweet_talk` | Block | `{ ... }` |
| `swim` | Block | `{ ... }` |
| `tail` | Block | `{ ... }` |
| `take_blood` | Block | `{ ... }` |
| `take` | Block | `{ ... }` |
| `talk_to` | Block | `{ ... }` |
| `talk` | Block | `{ ... }` |
| `tappytoes` | Block | `{ ... }` |
| `teleport` | Block | `{ ... }` |
| `thorns` | Block | `{ ... }` |
| `throw` | Block | `{ ... }` |
| `timemachine` | Block | `{ ... }` |
| `touch` | Block | `{ ... }` |
| `traverse` | Block | `{ ... }` |
| `turnon` | Block | `{ ... }` |
| `upgrade_yourself` | Block | `{ ... }` |
| `use_item` | Block | `{ ... }` |
| `use_toilet_con` | Block | `{ ... }` |
| `use_toilet_str` | Block | `{ ... }` |
| `use_weapon` | Block | `{ ... }` |
| `w1` | Block | `{ ... }` |
| `w2` | Block | `{ ... }` |
| `w3` | Block | `{ ... }` |
| `w4` | Block | `{ ... }` |
| `w5` | Block | `{ ... }` |
| `w6` | Block | `{ ... }` |
| `wealth` | Block | `{ ... }` |
| `weight` | Enum/String | `.5` |
| `wheezies` | Block | `{ ... }` |
| `wish_genes` | Block | `{ ... }` |
| `wish_items` | Block | `{ ... }` |
| `wish_levelups` | Block | `{ ... }` |
| `wish_strength` | Block | `{ ... }` |
| `withstand` | Block | `{ ... }` |
| `yank_it_out` | Block | `{ ... }` |
| `yellow_needle` | Block | `{ ... }` |

### Context: `outcome`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `add_weather` | Enum/String | `Birdemic` |
| `play_animation` | Array | `[ resultBlessing .5 ], [ resultTragedy .5 ], [ resultWeather .5 ]` |
| `random_pool` | Array | `[ { set_frame 12 prompt "EVENT_ACAT_REW1" gain_cat_famili..., [ { set_frame 1 prompt "EVENT_BLESSING_REW1" heal 5 } { s..., [ { set_frame 1 prompt "EVENT_TRAGEDY_REW1" } { set_frame...` |
| `weather_roll` | Array | `[ { weight 1 set_frame 2 prompt "EVENT_HAPPENING_FOG_REW"...` |

### Context: `outsmart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BUTCHTUTORIAL_OUTSMART_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `party_permanent_stats`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `con` | Number | `1` |

### Context: `party_permanent_stats_exclude_self`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cha` | Number | `1, 2` |
| `con` | Number | `1, 2` |
| `dex` | Number | `1, 2` |
| `int` | Number | `1, 2` |
| `lck` | Number | `1, 2` |
| `spd` | Number | `1, 2` |
| `str` | Number | `1, 2` |

### Context: `party_random_mutation_from_set`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count` | Number | `1` |
| `ears` | Number | `-2` |
| `eyebrows` | Number | `-2` |
| `eyes` | Number | `-2` |
| `mouth` | Number | `-2` |

### Context: `party_status_next_fight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AbilityOnBattleStart_Immediate` | Enum/String | `RocksFallEvent, SummonBrambles2, GrassEvent` |
| `Bleed` | Number | `3` |
| `DivineShield` | Number | `1` |
| `Fear` | Number | `1` |
| `HealthRegenUp` | Number | `2` |
| `Immobile` | Number | `1` |
| `NoHealthRegen` | Number | `1` |
| `Poison` | Number | `1, 2, 3` |
| `Tangled` | Number | `2` |
| `Tarred` | Number | `1` |
| `Webbed` | Number | `1` |

### Context: `past`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `hint_chapter_exit` | Enum/String | `iceage, endoftime, jurassic` |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_ICEAGE_PAST_ANSW, QEVENT_TIMEMACHINE_PAST_ANSW, QEVENT_TIMEMACHINE_JURASSIC_INFINITE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `patch_up`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_PATCHUP_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `permanent_stats`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cha` | Enum/String | `+1, 1, -1` |
| `con` | Number | `1, 2, -1` |
| `dex` | Number | `1, 2, -1` |
| `int` | Number | `-4, 1, -1` |
| `lck` | Number | `1, -1, -2` |
| `random` | Number | `1, 2, -1` |
| `spd` | Number | `1, -1, -2` |
| `str` | Number | `1, 2, -1` |

### Context: `pick_lock`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_LOCKEDCRATE_PICK_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `pilfer`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_PILFER_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `pirouette`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_PIROUETTE_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `place_gristle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_WALLOFFLESH_PLACE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `play`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSSTRANGER_ANSW"` |
| `stat` | Enum/String | `spd` |

### Context: `poop`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_FEEBIS_ANSW", "EVENT_POOP_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `power`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_POWER` |
| `stat` | Enum/String | `none` |

### Context: `print`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_PRINT_ANSW"` |

### Context: `protection`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_PROTECTION_ANSW", "EVENT_CUTS_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `pull`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_PULLKNIFE_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `pull_it_out`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW1"` |
| `stat` | Enum/String | `none` |

### Context: `pull_lever`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_ODDDEVICE_PULLLEVER_ANSW"` |

### Context: `purify`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_PURIFY_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `push_buttons`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_ODDDEVICE_PUSHBUTTONS_ANSW"` |

### Context: `push_through`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_PUSH"` |
| `stat` | Enum/String | `str` |

### Context: `put_in_coins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |
| `animation` | Enum/String | `choice_coins_ten` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_VENDINGMACHINE_COINS_ANSW"` |
| `stat_max` | Number | `10` |
| `stat_min` | Number | `10` |
| `stat` | Enum/String | `coins` |

### Context: `put_out_of_misery`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_PUTOUTOFMISERY_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `random_chance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `50%` |
| `get_item_from_pool` | Enum/String | `chapter` |

### Context: `random_mutation`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `asymmetric` | Boolean | `false, true` |
| `count` | Number | `1, 2, 15` |
| `tag` | Enum/String | `animal, birth_defect, melted` |

### Context: `random_mutation_from_set`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `arm1` | Number | `-1, -2` |
| `arm2` | Number | `-1, -2` |
| `body` | Number | `758, -1` |
| `count` | Number | `1, 3` |
| `ears` | Number | `-1, 1500, -2` |
| `eyebrows` | Number | `-1, -2` |
| `eyes` | Number | `-1, -2, 1029` |
| `head` | Number | `-1, 759` |
| `leg1` | Number | `-1` |
| `leg2` | Number | `-1` |
| `legs` | Number | `-1, 306` |
| `mouth` | Number | `1026, -1, 1500` |
| `tail` | Number | `-1, 1500, 760` |
| `texture` | Number | `-1` |

### Context: `rare`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `add_weather` | Enum/String | `RestlessDead, HauntedNight` |
| `ally_ambush_next_fights` | Number | `1, 2` |
| `ambush_next_basic_fights` | Number | `1` |
| `ambush` | String | `"events/chupacabra.lvl"` |
| `battle` | String | `"events/crackinthewall.lvl", "events/bigtoe.lvl", "events/chupacabra.lvl"` |
| `clear_result_animation` | Number | `1` |
| `conditional_reward` | Block | `{ ... }` |
| `damage` | Number | `6, 99%, 10` |
| `decrement_legacy_counter` | Enum/String | `WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyToken_StartDigging` |
| `event_now_same_cat` | Enum/String | `BigToe, SpookieApparation, CatHole` |
| `event_now` | Enum/String | `MysteriousMachine_Bad, MysteriousMachine_Good` |
| `full_heal` | Number | `1` |
| `gain_cat_familiar` | Number | `1` |
| `gain_coins` | Array | `[ 10 30 ], [ 10 15 ], [ 20 100 ]` |
| `gain_disorder_from_pool` | Enum/String | `diseases, all_disorders, physical_disorders` |
| `gain_disorder` | Enum/String | `Dyslexia, Brave, BorrowedTime` |
| `gain_familiar` | Enum/String | `CharmedFetus2, CharmedHeadTumor, CharmedLeaper` |
| `gain_food` | Array | `[ 1 5 ], [ 2 5 ], [ 8 10 ]` |
| `gain_immortal_familiar` | Enum/String | `CharmedFleaSpecial` |
| `get_and_equip_item` | Enum/String | `FlyLarva` |
| `get_item_from_pool` | Enum/String | `treasure_easy, bone_equipment, { ... }` |
| `get_item` | Enum/String | `BigToe, MomsKnife, MomsToeNail` |
| `get_parasite_from_pool` | Enum/String | `parasites, sludge_armor, good_parasites` |
| `get_parasite` | Enum/String | `FaceShards, MetalRod, BigToeCursed` |
| `global_effect_next_fight` | Block | `{ ... }` |
| `heal_disorder` | Number | `2` |
| `hide_appearance_changes` | Number | `1` |
| `increment_legacy_counter` | Enum/String | `WorldEventLegacyCounter_ToiletFlushes, WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyToken_StartDigging` |
| `injury` | Enum/String | `radiated, cursed, str` |
| `kill` | Enum/String | `cat` |
| `learn_ability_from_pool` | Enum/String | `Necromancer` |
| `learn_ability` | Enum/String | `BarfBall, FutureSight` |
| `learn_passive_from_pool` | Enum/String | `AnyUnlocked` |
| `learn_passive` | Enum/String | `DeathProof, PoisonTips, CobraStyle` |
| `leave_party_temporarily` | Block | `{ ... }` |
| `level_up` | Enum/String | `self` |
| `lose_all_equipped_items` | Enum/String | `cat` |
| `lose_item_from_inventory` | Enum/String | `cat` |
| `lose_item` | Enum/String | `inventory, equipped` |
| `lose_specific_item` | Enum/String | `SlagTight` |
| `make_old` | Enum/String | `self` |
| `mutation` | Block | `{ ... }` |
| `next_event_bonus` | Number | `1, -1, -2` |
| `next_event_from_set` | Enum/String | `WatchingHead2, { ... }` |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_MYSTERIOUSTENT_PROMPT", "EVENT_LOCKEDDOOR_PROMPT2"` |
| `party_damage` | Number | `2, 5, [ 5 10 ]` |
| `party_heal_disorder` | Number | `2` |
| `party_heal_injury` | Number | `99` |
| `party_heal` | Number | `6, 5, 100%` |
| `party_injury` | Enum/String | `random` |
| `party_permanent_stats_exclude_self` | Block | `{ ... }` |
| `party_permanent_stats` | Block | `{ ... }` |
| `party_random_mutation_from_set` | Block | `{ ... }` |
| `party_random_mutation` | Number | `1` |
| `party_status_next_fight` | Block | `{ ... }` |
| `permanent_stats` | Block | `{ ... }` |
| `play_animation` | Array | `[ resultLeave 0 ], resultHole` |
| `play_result_animation` | Enum/String | `resultVeryGood` |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW2", "EVENT_CLOSEDWINDOW_REW6", "EVENT_CLOSEDWINDOW_REW4"` |
| `random_mutation_from_set` | Block | `{ ... }` |
| `random_mutation` | Number | `1, 2, { ... }` |
| `random_pool` | Array | `[ { party_heal 100% gain_food [ 10 25 ], [ { event_now_same_cat Crate } { event_now_same_cat Safe ..., [ { permanent_stats { str -1 } } { permanent_stats { dex ...` |
| `scramble_abilities` | Enum/String | `all` |
| `scramble_basic_attack` | Enum/String | `all` |
| `self_damage` | Number | `1, 99%, 50%` |
| `self_status_next_fight` | Block | `{ ... }` |
| `set_adventure_token` | Enum/String | `MysteriousStranger_HasLostFinger, AdventureToken_TrippedOnBigToe, HasPlayedMysteriousStranger` |
| `set_age` | Number | `1` |
| `set_frame` | Number | `6, 4, 3` |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_HeadInTireCompleted, WorldEventLegacyToken_MomsKnife, WorldEventLegacyToken_MonkeyPaw1` |
| `shop_now` | Enum/String | `Event_RareShop, Event_SmallShop, TreasureHard` |
| `spawn_reflection_next_fight` | Number | `1, { ... }` |
| `spawn_unit_next_fight` | Block | `{ ... }` |
| `trigger_adventure_unlock` | Enum/String | `legacy_event_unlock_momsknife` |
| `upgrade_ability` | Enum/String | `random` |
| `upgrade_passive` | Enum/String | `random` |

### Context: `reach_inside`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SMALLBLACKHOLE_REACHINSIDE_ANSW"` |
| `stat` | Enum/String | `spd` |

### Context: `read`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_READ_ANSW"` |
| `stat` | Enum/String | `int` |

### Context: `receive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"Receive"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `red`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `fixed_chance` | Number | `50%` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_RED_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `red_needle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_NEEDLES_RED_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `lck` |

### Context: `reflect`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW3"` |
| `stat` | Enum/String | `none` |

### Context: `remove`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_REMOVE_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `remove_the_nail`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BIGTOE_NAIL_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `repair`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_REPAIR_ANSW, "EVENT_REPAIR_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `lck, none` |

### Context: `repair_quest`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_REPAIR_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `repell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSCAVE3_CLIMB_ANSW", "EVENT_MYSTERIOUSCAVE1_RAPPEL_ANSW", "EVENT_MYSTERIOUSCAVE1_TALKTO_ANSW"` |
| `stat` | Enum/String | `cha, dex, str` |

### Context: `requirements`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cat_has_injury_count_min` | Number | `2` |
| `cat_has_item_equipped` | Enum/String | `GuillotinasHead, ThrobbingGristle, PutridLeech` |
| `cat_has_item_slot_equipped` | Enum/String | `weapon` |
| `cat_has_parasite` | Boolean | `true` |
| `counter_maximum` | Array | `[ WorldEventLegacyCounter_CrackInTheWall 3 ], [ WorldEventLegacyCounter_CrackInTheWall 0 ], [ WorldEventLegacyCounter_SealedCrypt 4 ]` |
| `counter_minimum` | Array | `[ WorldEventLegacyToken_StartDigging 4 ], [ WorldEventLegacyCounter_CrackInTheWall 4 ], [ WorldEventLegacyCounter_TestLegacyFoo 3 ]` |
| `counter_range` | Array | `[ WorldEventLegacyCounter_SealedCrypt 1 1 ], [ WorldEventLegacyCounter_SealedCrypt 0 0 ], [ WorldEventLegacyCounter_SealedCrypt 2 2 ]` |
| `has_token` | Enum/String | `AdventureToken_TrippedOnBigToe, HasPlayedMysteriousStranger, WorldEventLegacyToken_StacyMutant` |
| `is_chapter` | Array | `[ future theend ], [ future ], [ theend ]` |
| `is_not_chapter` | Array | `[ jurassic iceage ], [ future theend ], [ iceage jurassic ]` |
| `minimum_party_size` | Number | `2` |
| `not_cat_has_item_equipped` | Enum/String | `GuillotinasHead, CryogenicTimeChamber_Full` |
| `not_has_token` | Enum/String | `WorldEventLegacyToken_MomsKnife, AdventureToken_UnmarkedGraveForced, WorldEventLegacyToken_CryptOpened` |
| `not_on_quest` | Number | `1` |

### Context: `rest`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_REST_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `revive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_REVIVE_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `reward`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `clear_adventure_token` | Enum/String | `AdventureToken_BlueNeedle, AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle` |
| `common` | Block | `{ ... }` |
| `cutscene_on_exit` | Enum/String | `infinite_intro` |
| `event_now` | Enum/String | `MeatGolem` |
| `gain_coins` | Array | `[ 4 15 ]` |
| `gain_disorder_from_pool` | Enum/String | `diseases, Steven_disorders` |
| `get_item_from_pool` | Enum/String | `consumables, food, { ... }` |
| `get_item` | Enum/String | `BrokenWindow` |
| `get_parasite_from_pool` | Enum/String | `parasites` |
| `injury` | Enum/String | `random, con` |
| `next_event_bonus` | Number | `1, -1, -2` |
| `party_damage` | Array | `[ 5 10 ]` |
| `play_animation` | Enum/String | `resultVeryGood, resultBad` |
| `prompt` | String | `"EVENT_SEALEDCRYPT_QUES2", "EVENT_TRASHBIN_REW2", "EVENT_SEALEDCRYPT_QUES1"` |
| `random_chance` | Block | `{ ... }` |
| `random_pool` | Array | `[ { get_item_from_pool uncommon get_item_from_pool uncomm..., [ { get_item_from_pool rare get_item_from_pool rare } { g..., [ { weight 10 gain_disorder_from_pool diseases } { weight...` |
| `rare` | Block | `{ ... }` |
| `set_adventure_token` | Enum/String | `AdventureToken_Mirage2, HasPlayedMysteriousStranger, AdventureToken_StevenTryAgain3` |
| `set_frame` | Number | `1, 2, 3` |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_CryptOpened` |
| `set_subject` | Enum/String | `wall_of_flesh_noartery, dimensionx_head2, throbbing_artery_noflesh` |
| `spawn_unit_next_fight` | Block | `{ ... }` |
| `trigger_adventure_unlock` | Enum/String | `end_of_time_unlock, meat_world_unlock` |
| `weight` | Number | `3` |

### Context: `rub`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_RUB_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `run`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_RUN_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `spd` |

### Context: `run_again`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_RUN_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `spd` |

### Context: `run_away`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_RUNAWAY_ANSW"` |
| `stat` | Enum/String | `spd` |

### Context: `sacrifice`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW", "EVENT_BAHPHOMET_SACRIFICE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `sacrifice_full_favor`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `sacrifice_normal`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `lck` |

### Context: `sacrifice_partial_favor`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `sacrifice_quest`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `scale`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_SCALE_ANSW"` |

### Context: `scream`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GOLEMSCREAM_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `self_status_next_fight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AbilityOnBattleStart_Immediate` | Enum/String | `FlowerEventSleep, BrambleRandomTileEvent, SummonBrambles2` |
| `AbilityOnBattleStart` | Enum/String | `Flush` |
| `AddInitiative` | Number | `-99` |
| `AddStartingMana` | Number | `5` |
| `AllStatsUp` | Number | `1` |
| `AlphaTurns` | Number | `1` |
| `Bleed` | Number | `1, 2, 3` |
| `Blind` | Number | `6, 4` |
| `Bruise` | Number | `1` |
| `Burn` | Number | `6, 5, 4` |
| `ChangeTileUnderCharacterAtStart` | Enum/String | `GlassTile` |
| `CharismaUp` | Number | `2, -1, -2` |
| `Confusion` | Number | `2, 4` |
| `ConstitutionUp` | Number | `1, -1` |
| `DexterityUp` | Number | `2, -1` |
| `DivineShield` | Number | `2` |
| `Fear` | Number | `5, 1, 2` |
| `Fights` | Number | `99` |
| `HealthRegenUp` | Number | `1, 2` |
| `IntelligenceUp` | Number | `-3, 3` |
| `LuckUp` | Number | `1` |
| `Madness` | Number | `1` |
| `MissChance` | Number | `10` |
| `NoHealthRegen` | Number | `1` |
| `NoManaRegen` | Number | `1` |
| `PermanentConfusion` | Number | `1` |
| `Poison` | Number | `2, 10, 3` |
| `ProbeCharmed` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `Rot` | Number | `2` |
| `Sleep` | Number | `1, 2` |
| `Slow` | Number | `3` |
| `SpeedUp` | Number | `-4, 2, -2` |
| `SpiderInfested` | Number | `1` |
| `StrengthUp` | Number | `2, -1, -2` |
| `Stun` | Number | `1` |
| `Tarred` | Number | `1` |
| `TempStrengthUp` | Number | `1` |
| `Webbed` | Number | `1, 2` |

### Context: `setup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `conditional_reward` | Block | `{ ... }` |
| `set_frame` | Number | `4` |

### Context: `shake`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_VENDINGMACHINE_SHAKE_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `skip`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW4", "QEVENT_STACYMUTANT3_ANSW4", "QEVENT_STACYMUTANT1_ANSW4"` |
| `stat` | Enum/String | `none` |

### Context: `slip_through`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SLIPTHROUGH_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `smash`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `copy_results` | Enum/String | `open` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SMASH_ANSW", "EVENT_MYSTERIOUSTOMB_ANSW", "EVENT_GOLEMSMASH_ANSW"` |
| `stat` | Enum/String | `none, dex, str` |

### Context: `sneak`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SNEAKBY_ANSW", EVENT_SNEAKBY_ANSW, EVENT_RUN_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `dex, spd` |

### Context: `sneak_by`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |
| `stat` | Enum/String | `dex` |

### Context: `sneak_past_alt`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `dex` |

### Context: `soul`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_CURSESOUL` |
| `stat` | Enum/String | `none` |

### Context: `spawn_reflection_next_fight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `mutation` | Block | `{ ... }` |

### Context: `spawn_unit_next_fight`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count` | Number | `8, [ 3 6 ], 3` |
| `object` | Enum/String | `DeadPinky, [ Junk Junk TrashBag ], RandomNonCoinPickup` |
| `side` | Enum/String | `enemies` |
| `spawn_side` | Enum/String | `cats, anywhere, enemies` |

### Context: `speed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW3"` |
| `stat` | Enum/String | `none` |

### Context: `surprise`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SURPRISE_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `sweet_talk`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_DEATH_SWEETTALK_ANSW"` |
| `stat` | Enum/String | `cha` |

### Context: `swim`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_SWIM_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `tail`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_TAILINSIDE_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `take`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_dex_alt` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_GOAROUND_ANSW", "EVENT_TAKE_ANSW"` |
| `stat` | Enum/String | `lck, con, spd` |

### Context: `take_blood`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_DEADKING_DRAINBLOOD_ANSW` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `quest` |

### Context: `talk`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_TALKTO_ANSW` |
| `stat` | Enum/String | `cha` |

### Context: `talk_to`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_TALKTO_ANSW"` |
| `stat` | Enum/String | `cha` |

### Context: `tappytoes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_TAPPYTOES_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `teleport`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_TELEPORT_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `thorns`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW1"` |
| `stat` | Enum/String | `none` |

### Context: `throw`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_HOLEINTHEEARTH_THROW_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `timemachine`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"Go to The Past"` |
| `stat` | Enum/String | `none` |

### Context: `touch`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `QEVENT_OBELISK_MOON_TOUCH_ANSW, "EVENT_MYSTERIOUSOBELISK_TOUCH_ANSW", QEVENT_OBELISK_CORE_TOUCH_ANSW` |
| `stat` | Enum/String | `cha, none, lck` |

### Context: `traverse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_TRAVERSETHENECROPOLIS_ANSW"` |
| `play_animation` | Enum/String | `resultGood` |
| `prompt` | String | `"EVENT_TRAVERSETHENECROPOLIS_REW5"` |
| `shop_now` | Enum/String | `TreasureHard` |

### Context: `turnon`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_TURNONTV_ANSW", "EVENT_MYSTERIOUSMACHINE_TURNITON_ANSW"` |
| `stat` | Enum/String | `lck, int` |

### Context: `upgrade_yourself`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_UPGRADE_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `use_item`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_USE_ITEM_ANSW"` |
| `stat` | Enum/String | `lck` |

### Context: `use_toilet_con`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_USETOILET_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `use_toilet_str`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_USETOILET_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `use_weapon`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_USE_WEAPON_ANSW"` |
| `requirements` | Block | `{ ... }` |

### Context: `w1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW1"` |
| `stat` | Enum/String | `none` |

### Context: `w2`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW2"` |
| `stat` | Enum/String | `none` |

### Context: `w3`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW3"` |
| `stat` | Enum/String | `none` |

### Context: `w4`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW4"` |
| `stat` | Enum/String | `none` |

### Context: `w5`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW5"` |
| `stat` | Enum/String | `none` |

### Context: `w6`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW6"` |
| `stat` | Enum/String | `none` |

### Context: `wealth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_WEALTH` |
| `stat` | Enum/String | `none` |

### Context: `wheezies`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |
| `bad` | Block | `{ ... }` |
| `label` | String | `"EVENT_WHEEZIES_ANSW"` |
| `stat` | Enum/String | `none` |

### Context: `wish_genes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MONKEYPAW_WISH2"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `wish_items`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MONKEYPAW_WISH3"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `wish_levelups`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MONKEYPAW_WISH4"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `wish_strength`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_MONKEYPAW_WISH1"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `none` |

### Context: `withstand`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_ELEPHANTSFOOTEVENCLOSER_ANSW"` |
| `stat` | Enum/String | `con` |

### Context: `yank_it_out`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_BIGTOE_YANK_ANSW"` |
| `stat` | Enum/String | `str` |

### Context: `yellow_needle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bad` | Block | `{ ... }` |
| `good` | Block | `{ ... }` |
| `label` | String | `"EVENT_NEEDLES_YELLOW_ANSW"` |
| `requirements` | Block | `{ ... }` |
| `stat` | Enum/String | `lck` |

---

## Furniture & Metaprogression

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Appeal` | Number | `1, 5, 2` |
| `BreedSuppression` | Number | `1` |
| `Comfort` | Number | `5, -2, -5` |
| `Evolution` | Number | `1, 5, 2` |
| `FightBonusRewards` | Number | `1` |
| `FightRisk` | Number | `2` |
| `FoodStorage` | Number | `40` |
| `Health` | Number | `5, -1, -2` |
| `Stimulation` | Number | `1, 5, 2` |
| `can_be_rare` | Boolean | `false` |
| `desc` | Enum/String | `FURNITURE_DESC_AUTOFEEDER, FURNITURE_DESC_SPECIAL_FOODBOX, FURNITURE_DESC_POOP` |
| `name` | Enum/String | `FURNITURE_NAME_SPECIAL_FOODBOX, FURNITURE_NAME_AUTOFEEDER, FURNITURE_NAME_POOP` |
| `removed` | Boolean | `true` |
| `set` | Enum/String | `sewn, spider, junk` |
| `special` | Boolean | `true` |

---

## Items & Equipment

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Set` | Enum/String | `Monk` |
| `ability` | Enum/String | `wp_PartyDetonator, wp_PersuasionDevice, wp_PartyDetonatorFixed` |
| `attack` | Enum/String | `BasicSpin, BasicTankMelee, IsaacBasicAttack` |
| `aux_is_catid` | Boolean | `true` |
| `aux` | Number | `12, 24, 10` |
| `cant_equip_to_colorless` | Boolean | `true` |
| `cha` | Number | `1, 2, -1` |
| `con` | Number | `1, 2, 3` |
| `consumable` | Boolean | `true` |
| `cursed` | Boolean | `true` |
| `degrade_after_adventure` | Boolean | `false` |
| `desc` | String | `"ARMOR_SCRAPMETALARMOR_DESC", "ARMOR_SCRAPMETALMASK_DESC", "ARMOR_SCRAPMETALHAT_DESC"` |
| `dex` | Number | `1, -1, 3` |
| `divine_shield` | Number | `1, 2, 3` |
| `dont_destroy_on_0` | Boolean | `true` |
| `durability` | Number | `1, 2, 3` |
| `equip_sound` | Enum/String | `SE_CatWeaponPoke_Chainsaw` |
| `failable` | Boolean | `true` |
| `force_sticky` | Boolean | `true` |
| `fragile` | Boolean | `true` |
| `frame` | Number | `12, 2, 23` |
| `global_passives` | Block | `{ ... }` |
| `global_tags` | Array | `[ all_cats_are_jester ], [ fail_all_events ], [ always_ambushed ]` |
| `hint_destination` | Enum/String | `meatworld, boneyard, caves` |
| `hint_prerequisite_flag` | Enum/String | `mapflag_BothObelisksUnlocked, mapflag_MeatWorldUnlockedFull, mapflag_MeatWorldUnlocked` |
| `icon_hint` | Enum/String | `passive_syringe, ability_syringe` |
| `indestructible` | Boolean | `true` |
| `int` | Number | `1, -1, 7` |
| `keyword_tooltips` | Block | `{ ... }` |
| `kind` | Enum/String | `head, face, neck` |
| `lck` | Number | `1, 2, -3` |
| `legacy_quest` | Boolean | `true` |
| `max_durability` | Number | `2, 3, 9` |
| `max_health` | Number | `-1` |
| `name` | String | `"ARMOR_SCRAPMETALHAT_NAME", "ARMOR_SCRAPMETALMASK_NAME", "ARMOR_SCRAPMETALARMOR_NAME"` |
| `on_store` | Enum/String | `become_aux_coins, become_furniture, become_rare_furniture` |
| `parasite` | Boolean | `true` |
| `passive` | Block | `{ ... }` |
| `passives` | Block | `{ ... }` |
| `prevent_level_up` | Boolean | `true` |
| `quest_item_alias` | Enum/String | `NuclearKnife, BlackShard` |
| `quest_item` | Boolean | `false, true` |
| `quest_reward_item` | Enum/String | `PersuasionDevice_Fixed, MagicMirror_Fixed, ChaosDevice_Fixed` |
| `randomize_piece_frames` | Boolean | `true` |
| `rarity` | Enum/String | `rare, common, uncommon` |
| `reset_aux_on_store` | Number | `1` |
| `reset_str_aux_on_store` | Enum/String | `ModelingClay_Default` |
| `set` | Enum/String | `Rag, Leather, Scrap` |
| `shield` | Number | `1, 2, 4` |
| `spd` | Number | `-4, -1, 3` |
| `speed` | Number | `1` |
| `sticky` | Boolean | `true` |
| `str_aux_initialize` | Enum/String | `random_stat, random_class_passive, random_seed` |
| `str_aux_is_copy_ability` | Block | `{ ... }` |
| `str_aux_is_copy_item_active` | Boolean | `true` |
| `str_aux_is_copy_item_icon` | Boolean | `true` |
| `str_aux_is_copy_item_passive` | Boolean | `true` |
| `str_aux_is_copy_passive` | Boolean | `true` |
| `str_aux` | Enum/String | `ModelingClay_Default` |
| `str` | Number | `1, 2, aux` |
| `variant_of` | Enum/String | `PoundOfFlesh, RedCap, CrimsonMask` |
| `weightless` | Boolean | `true` |

### Context: `AIControlNextTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `include_spells` | Boolean | `true` |
| `stacks` | Number | `1` |

### Context: `AbilityHealthThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `cm_HealPercent_Auto` |
| `aux` | Number | `25` |
| `even_if_stunned` | Boolean | `true` |
| `immediate` | Boolean | `true` |
| `threshold` | String | `"max(X*.5, 1)"` |

### Context: `AbilityOnRoundEndOnce`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `wp_SignalAmplifierSpawnTerminator` |
| `even_of_stunned` | Boolean | `true` |

### Context: `AddAdvantageToEvent`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `add` | Number | `5` |
| `options` | Array | `[ smash bash open ]` |
| `type` | Enum/String | `treasure_box` |

### Context: `AddDamageToElementDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `1, 2` |
| `element` | Enum/String | `Ice, Fire, Electric` |

### Context: `AddPassivesToCharmed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |

### Context: `AddPassivesToMinions`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddMaxHealth` | Number | `2` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `AllStatsUp` | Number | `1` |
| `HealthGain` | Number | `2, 4` |
| `Shield` | Number | `2` |

### Context: `AddSelfStatusToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `ForceUseAbility` | Enum/String | `DustDash` |
| `Quivered` | Array | `[ 1 .10 ]` |
| `RandomMagicMissile` | Number | `1, 2, 3` |
| `Shield` | Number | `1` |

### Context: `AddSelfStatusToWeapons`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RepairWeapon` | Array | `[ 1 .25 ]` |

### Context: `AddStatusToAllDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_HasStatus` | Block | `{ ... }` |
| `Conditional_HasTag` | Block | `{ ... }` |
| `KnockbackIfCrit` | Block | `{ ... }` |
| `Rot` | Number | `1` |
| `must_do_damage` | Boolean | `true` |

### Context: `AddStatusToBackstabs`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `Bleed` | Number | `1` |
| `Blind` | Number | `1` |
| `Bruise` | Number | `1` |
| `Burn` | Number | `1` |
| `ChangeTile` | Enum/String | `TallGrassTile, GlassTile, BrambleTile` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `Confusion` | Number | `1` |
| `DamageOrHealConditionally` | Number | `1` |
| `Fear` | Array | `[ 1 .1 ], [ 1 .15 ], [ 1, .25 ]` |
| `ForceUseAbilityOnTarget` | Block | `{ ... }` |
| `Freeze` | Array | `[ 1 .1 ]` |
| `KnockOutCoin` | Number | `1` |
| `KnockUpAndAway` | Block | `{ ... }` |
| `Knockback` | Number | `1, 2` |
| `Leech` | Number | `1` |
| `Leeches` | Number | `1` |
| `MagicWeakness` | Number | `1` |
| `ManaLeeches` | Number | `1` |
| `Marked` | Number | `1` |
| `OverrideChainKnockback` | Number | `1` |
| `Poison` | Number | `1, 2` |
| `PullSourceToTarget` | Number | `1` |
| `Rot` | Number | `1` |
| `Slow` | Number | `1` |
| `SoulLink` | Number | `1` |
| `SpiderInfested` | Number | `1` |
| `Stun` | Array | `[ 1, .1 ]` |
| `Tangled` | Array | `[ 1, .05 ], [ 1, .33 ]` |
| `Weakness` | Number | `1, 3` |

### Context: `AddStatusToElementDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Number | `1` |
| `Stun` | Array | `[ 1 .1 ]` |
| `element` | Enum/String | `Fire, Electric` |

### Context: `AddStatusToKnockbackDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bruise` | Number | `1` |
| `Stun` | Array | `[ 1, .1 ]` |

### Context: `AddStatusToSpells`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Enemy` | Block | `{ ... }` |
| `Leech` | Number | `1` |

### Context: `AddStatusToWeapons`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Leech` | Number | `1` |

### Context: `AddTemporaryEffectsToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CastAgainWithStatus` | Block | `{ ... }` |

### Context: `AlluringDoodieEater`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `10%` |
| `damage_instance` | Block | `{ ... }` |

### Context: `AllyDodgeChanceAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `25%` |
| `range` | Number | `1` |

### Context: `ApplyPassives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `StatusOnBattleEnd` | Block | `{ ... }` |

### Context: `ApplyStatusesToRandomEnemiesEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bounty` | Number | `1` |
| `Marked` | Number | `1` |
| `count` | Number | `1` |

### Context: `ApplyToRandomPartyMemberIfPossible`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `GainDisorderFromPool` | Enum/String | `all_disorders` |

### Context: `ApplyToSource`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Charge` | Number | `1, 3` |
| `HealthGain` | Number | `3` |
| `SpeedUp` | Number | `1` |
| `StrengthUp` | Number | `1` |

### Context: `ArmorBreakOnHit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance_to_break` | Number | `5%, 10%` |
| `durability_loss` | Number | `0` |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `face_StevenMask2` |
| `even_if_stunned` | Boolean | `true` |

### Context: `BackflipWhenTargeted`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `BackflipDodge` |
| `stacks` | Number | `2` |

### Context: `BoostWeaponDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `crit_chance` | Number | `1, .5` |
| `damage` | Number | `0` |

### Context: `BouncyProjectiles`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `max_bounces` | Number | `1` |
| `max_range` | Number | `2` |

### Context: `BuffImmunity`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exclude` | Enum/String | `SpellDamageUp` |

### Context: `CastAgainWithStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `OverrideDamage` | Number | `1` |
| `stacks` | Number | `1` |

### Context: `CatPartsSizeScale`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `head` | Number | `1.3` |

### Context: `CatchProjectiles`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Quivered` | Number | `1` |
| `ally_chance` | Number | `15%` |
| `chance` | Number | `15%` |

### Context: `ChanceToBackflip`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `BlinkDodge, ShadowstepDodge` |
| `chance` | Number | `33%, 10%` |

### Context: `ChanceToBlockAndCounter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `backstab_only` | Boolean | `true` |
| `chance` | Number | `100%` |

### Context: `ChanceToForceEvent`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `25%` |
| `event` | Enum/String | `Blessing` |

### Context: `ChanceToRevive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `health` | Number | `34%` |
| `stacks` | Number | `50` |

### Context: `ClassManaCostReduction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `class` | Enum/String | `Colorless` |
| `reduction` | Number | `1, 2` |

### Context: `Conditional_Adjacent`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Ally` | Block | `{ ... }` |
| `Conditional_PlayerCat` | Block | `{ ... }` |

### Context: `Conditional_Ally`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ManaGain` | Number | `1` |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Temporary` | Block | `{ ... }` |
| `odds` | Enum/String | `.1, .3` |

### Context: `Conditional_Boss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1, -2` |

### Context: `Conditional_Corpse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomMutation` | Number | `1` |

### Context: `Conditional_Enemy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Leeches` | Number | `1` |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DestroyTrinket` | Number | `1` |
| `FindItemFromPool` | Enum/String | `parasites, consumables` |
| `ForceUseAbility_NonStack` | Enum/String | `Endeavor_Auto` |
| `ForceUseAbility` | Enum/String | `tk_WeirdEgg_Spawn, cm_RaptorEggSpawn, tk_Asteroid` |
| `Freeze` | Number | `1` |
| `RandomMutation` | Number | `1` |
| `odds` | Number | `15%, 1%, 10%` |

### Context: `Conditional_HasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |
| `FlatLeechIfDamaged` | Number | `3` |
| `ImmediateUseAbility_Instant` | Enum/String | `head_CrownOfHorns` |
| `RemoveStatusStacks` | Block | `{ ... }` |
| `status` | Enum/String | `Bleed, Thorns` |

### Context: `Conditional_HasTag`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusKnockbackDamage` | Number | `5` |
| `OverrideChainKnockback` | Number | `0` |
| `tag` | Enum/String | `rock` |

### Context: `Conditional_HealthThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_OncePerBattle` | Block | `{ ... }` |
| `threshold_flat` | Number | `3` |

### Context: `Conditional_ManaThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` |
| `threshold_flat` | Number | `0` |

### Context: `Conditional_OncePerBattle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ReduceManaCost` | Number | `1` |
| `Shield` | Number | `3` |
| `ShowText` | String | `"COMBAT_POPUP_BRAINSTORM"` |
| `SpellDamageUp` | Number | `1` |
| `key` | Enum/String | `JewelOfDrog` |

### Context: `Conditional_PartyMember`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_IsSelf` | Block | `{ ... }` |
| `Else` | Block | `{ ... }` |

### Context: `Conditional_PlayerCat`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `1` |

### Context: `Conditional_RandomChance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyPassives` | Block | `{ ... }` |
| `odds` | Number | `20%` |

### Context: `Conditional_Shielded`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `SetItemAux` | Block | `{ ... }` |

### Context: `ConvertDamageToScaledStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DelayedPain` | Number | `1` |
| `stacks` | Number | `3` |

### Context: `CounterAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `attack, neck_TentacleArmorCounter, head_IronJaw` |
| `melee_only` | Boolean | `true` |
| `ranged_only` | Boolean | `true` |

### Context: `Craft`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Enum/String | `tinkerer_default, bombs` |
| `slot` | Enum/String | `weapon` |
| `works_with_tech` | Boolean | `true` |

### Context: `CreateGlobalModifiers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Number | `1` |
| `NoCorpses` | Number | `1` |

### Context: `CritsApplyStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Fear` | Number | `1` |

### Context: `DelayedAutoRevive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `health` | Number | `15%, 50%` |
| `rounds` | Number | `1, 2` |

### Context: `DestroyEquipmentAndAttachParasite`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.75` |
| `pool` | Array | `[ FaceGrub HeadGrub NeckGrub ]` |

### Context: `DoDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage_tiles` | Enum/String | `all` |
| `damage` | Number | `0` |
| `effects` | Block | `{ ... }` |
| `type` | Enum/String | `spell` |

### Context: `DurabilityTransform`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `eq` | Array | `[ 0 JarOfNothing ], [ 0 WaterBottle_Empty ], [ 1 WaterBottle_Half ]` |
| `ge` | Array | `[ 3 EstusFlask_Full ], [ 2 WaterBottle_Full ]` |

### Context: `ElementalManaCostReduction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Array | `[ Fire Earth ], [ Holy ]` |
| `reduction` | Number | `1` |

### Context: `Else`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` |

### Context: `Eternal`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `health_percent` | Number | `100%` |
| `stacks` | Number | `1` |

### Context: `ExtraStatusWhenDealingDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_PartyMember` | Block | `{ ... }` |

### Context: `FlyDamageIncrease`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |
| `stacks` | Number | `2` |

### Context: `ForceUseAbilityOnTarget`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `head_MiniMoonArmorAsteroid` |
| `chance` | Number | `25%` |

### Context: `GainCoinsRange`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `max` | Number | `25, 30, 60` |
| `min` | Number | `1, 15, 30` |

### Context: `GlobalMeleeRevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `knockback` | Number | `5` |

### Context: `ImmediateUseAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `wp_NuclearKnifeExplode` |
| `even_if_stunned` | Boolean | `true` |

### Context: `ItemAuxTransform`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ge` | Array | `[ 10 NuclearKnife_Glowing ], [ 20 BlackShard_Glowing ]` |
| `le` | Array | `[ 50 MoneyBag_Large ], [ 25 MoneyBag_Medium ], [ 10 MoneyBag_Small ]` |
| `lt` | Array | `[ 10 NuclearKnife ]` |

### Context: `KnockUpAndAway`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `distance` | Number | `3` |
| `stacks` | Number | `5` |

### Context: `KnockbackIfCrit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `knockback` | Number | `10` |
| `override_chain_knockback` | Number | `10` |

### Context: `ManaGainRange`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `max` | Number | `4` |
| `min` | Number | `0` |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `0` |
| `effects` | Block | `{ ... }` |
| `knockback` | Number | `1, 2, 10` |

### Context: `ModifyAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cost` | Block | `{ ... }` |
| `meta` | Block | `{ ... }` |

### Context: `MovementReaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `wp_Blackjack_Auto, wp_ZodiacsSixshooter_Auto` |
| `create_temp_ability` | Boolean | `true` |
| `enemies_only` | Boolean | `true` |
| `on_self_move_too` | Boolean | `true` |

### Context: `ObjectDetector`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `10%` |
| `object` | Enum/String | `CharmedDip` |

### Context: `ObjectOnHitCharacter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `CharmedTinySpider, CharmedLeech` |
| `stacks` | Number | `1, "floor(lck/4)"` |

### Context: `PassiveAfterXKills`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `stacks` | Number | `3` |

### Context: `PassiveAtHealthThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal, equal, greater` |
| `passives` | Block | `{ ... }` |
| `threshold` | Number | `1, 5, 10` |

### Context: `PassiveAtStatThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal` |
| `passives` | Block | `{ ... }` |
| `threshold` | Block | `{ ... }` |

### Context: `PassiveIfStrAuxEquals`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `value` | Enum/String | `con, dex, str` |

### Context: `PassiveIfWeaponIsUsable`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Number | `1, 2` |

### Context: `PassiveWhenAffectedByElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `water` |
| `passives` | Block | `{ ... }` |

### Context: `PassiveWhenDead`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AutocastEachRound` | Block | `{ ... }` |
| `StatusEachRoundEnd` | Block | `{ ... }` |
| `StatusEachTurnBegin` | Block | `{ ... }` |

### Context: `PassiveWhenOnTile`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `tile` | Array | `[ TallGrassTile TallFlowerTile ], [ WaterTile ]` |

### Context: `PassiveWhileHasDurability`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `MovementReaction` | Block | `{ ... }` |

### Context: `PassiveWhileInMonkMeleeStance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Number | `1` |

### Context: `PassiveWhileShielded`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthRegenUp` | Number | `3` |

### Context: `PoopWhenHit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `25%` |
| `object` | Enum/String | `Poop` |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `PermanentCharisma` | Number | `1` |
| `PermanentConstitution` | Number | `1` |
| `PermanentDexterity` | Number | `1` |
| `PermanentIntelligence` | Number | `1` |
| `PermanentLuck` | Number | `1` |
| `PermanentSpeed` | Number | `1` |
| `PermanentStrength` | Number | `1` |

### Context: `RefreshEquipmentAbilityOnElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Electric` |
| `text` | String | `"COMBAT_POPUP_RECHARGED"` |

### Context: `RemoveStatusStacks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `1` |
| `status` | Enum/String | `Thorns` |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `1, 0` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Electric ]` |

### Context: `ReviveNextRound`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Shield` | Number | `2` |
| `revive_health` | Number | `100%` |

### Context: `ScaldingOrbMoonBossOneShot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CompleteItemQuest` | Enum/String | `ScaldingOrb` |
| `RemoveItem` | Enum/String | `ScaldingOrb` |

### Context: `ScaledStatusAlliesOnSpendMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Adjacent` | Block | `{ ... }` |

### Context: `ScaledStatusOnHolyShieldBlock`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` |

### Context: `ScaledStatusOnSpendMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `StatusAfterXStacks` | Block | `{ ... }` |

### Context: `SetItemAux`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `slot` | Enum/String | `head, face, trinket` |
| `value` | Enum/String | `item_aux+1, item_aux+2, item_aux-1` |

### Context: `SpawnEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.2, 5%, 100%` |
| `object` | Enum/String | `CharmedFlea, CharmedAmoeba, [ CharmedFly CharmedMaggot ]` |
| `stack_key` | Enum/String | `CATHIDE` |

### Context: `SpawnExtraThingsOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `number` | Number | `3, [ 1 2 ]` |
| `object` | Enum/String | `RandomPickup` |

### Context: `SpawnItemLinkedFamiliar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `break_on_pop_only` | Boolean | `true` |
| `object` | Enum/String | `ZaratanaFamiliar, PyrophinaFamiliar` |

### Context: `SpawnObjectOnPopCorpse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count` | Number | `2` |
| `except_tiny` | Boolean | `true` |
| `object` | Enum/String | `CharmedTinySpider` |

### Context: `SpawnOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `number` | Number | `1, [ 1, 3 ]` |
| `object` | Enum/String | `CharmedTinyTumor, Food, CharmedPinky` |

### Context: `SpawnOnBattleStartRandomEmptyTile`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `number` | Array | `[ 0 1 ], [ 3 6 ]` |
| `object` | Enum/String | `Coin, Bird` |

### Context: `SpawnOnDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `faction` | Enum/String | `solitary_enemies` |
| `obj` | Enum/String | `BeefyCharmedLeech` |

### Context: `SpawnRandomPickupsOnTaggedUnitKilled`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count` | Array | `[ 2 3 ]` |
| `tag` | Enum/String | `poop` |

### Context: `SpawnThingOnDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.25` |
| `good` | Boolean | `false` |
| `number` | Number | `1` |
| `object` | Enum/String | `Catnip, CharmedTinySpider, Scrap` |
| `spawn_on_death_hit` | Boolean | `false` |

### Context: `StackingFlowerTrail`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stack_key` | Enum/String | `FLOWER_SET` |
| `stacks` | Number | `1` |

### Context: `StatDependentPassive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String | `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha...` |

### Context: `StatusAdjacentOnTheirTurnEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceMoveAway` | Number | `1` |

### Context: `StatusAfterCastSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `TempMeleeRangeUp` | Number | `1` |
| `TempRangeUp` | Number | `1` |
| `UseAbility` | Enum/String | `neck_DarkFriend` |

### Context: `StatusAfterXStacks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ExtraBasicMoves_Status` | Number | `1` |
| `RefreshActPoints` | Number | `1` |
| `expires_on_end_turn` | Boolean | `true` |
| `stack_key` | Enum/String | `FANNY_PACK, EMPTY_GENERATOR` |
| `threshold` | Number | `12, 3` |

### Context: `StatusAfterXTurns`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `tk_MadGhost_Spawn` |
| `stacks` | Number | `3` |

### Context: `StatusAllCharactersOnSpawn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Boss` | Block | `{ ... }` |
| `Poison` | Number | `1` |

### Context: `StatusAlliesEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Adjacent` | Block | `{ ... }` |

### Context: `StatusAlliesOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Number | `1` |
| `ConstitutionUp` | Number | `1` |
| `DamageUp` | Number | `1` |
| `SpeedUp` | Number | `1, 2` |
| `StrengthUp` | Number | `1` |

### Context: `StatusAlliesOnDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `2` |

### Context: `StatusEachRoundEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DoDamage` | Block | `{ ... }` |

### Context: `StatusEachTurnBegin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BlessingOfPeace` | Number | `1` |
| `Burn` | Number | `1` |
| `Conditional_BadRoll` | Block | `{ ... }` |
| `DestroyTrinket` | Number | `1` |
| `DoubleCastSpellThisTurn` | Number | `1` |
| `DrinkWater` | Number | `1` |
| `ManaGainRange` | Block | `{ ... }` |
| `Revive` | Number | `1` |
| `SpeedUp` | Number | `2` |
| `Temporary` | Block | `{ ... }` |
| `UseAbility` | Enum/String | `neck_DarkFriend` |
| `Wet` | Number | `1` |

### Context: `StatusEachTurnEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddWeaponAux` | Number | `1` |
| `Burn` | Number | `3` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `Conditional_ManaThreshold` | Block | `{ ... }` |
| `ConstitutionUp` | Number | `1` |
| `ForceUseAbility` | Enum/String | `tk_JarOfRadiation, head_HitlersToupe, tk_SuckStone` |
| `ImmediateUseAbility` | Enum/String | `head_ThrobbingCrown, { ... }` |
| `PartialCleanse` | Number | `1` |
| `PreEmptiveCounterNextAttacks` | Number | `1` |
| `Shield` | Number | `1` |
| `SpawnCoinAnywhere` | Number | `1` |
| `Stealth` | Array | `[ 1 .1 ]` |

### Context: `StatusEachTurnEndForEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `face_FartFace` |

### Context: `StatusEveryXSpellCasts`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `3` |
| `IntelligenceUp` | Number | `2` |
| `ObjectOnHitCharacter` | Block | `{ ... }` |
| `stacks` | Number | `4, 3` |

### Context: `StatusIfUnusedActPoints`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BackflipWhenTargeted` | Enum/String | `X` |
| `Craft` | Block | `{ ... }` |

### Context: `StatusIfUnusedMovePoints`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `3` |
| `HealthGain` | Number | `3` |

### Context: `StatusOnAllyCatDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `1` |
| `RepairTrinket` | Number | `1` |

### Context: `StatusOnBackstab`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthGain` | Number | `2` |
| `SerratedClaws` | Number | `1` |

### Context: `StatusOnBattleEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Corpse` | Block | `{ ... }` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `Conditional_Shielded` | Block | `{ ... }` |
| `FindItemFromPool` | Enum/String | `pills, chapter_specific_item` |
| `GainCoins` | Number | `1, [ 3 5 ]` |
| `PermanentConstitution` | Number | `-1` |
| `PermanentIntelligence` | Number | `-1` |
| `RandomMutation` | Number | `1` |
| `RandomPermanentStat` | Number | `1, -1, -3` |
| `RepairAll` | Number | `1` |
| `RepairTrinket` | Number | `99` |
| `RepairWeapon` | Number | `6` |
| `SetItemAux` | Block | `{ ... }` |
| `TransformWeapon` | Block | `{ ... }` |
| `even_if_dead` | Boolean | `true` |

### Context: `StatusOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Enum/String | `item_aux` |
| `Craft` | Block | `{ ... }` |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` |
| `FindItemFromPool` | Enum/String | `common` |
| `ForceUseAbility` | Enum/String | `tk_DybbuksRib` |
| `ObjectOnHitCharacter` | Block | `{ ... }` |
| `RandomMagicMissile` | Number | `4` |
| `ReviveNextRound` | Block | `{ ... }` |
| `SafeDie` | Number | `1` |
| `SetHealth` | Number | `50%` |
| `StealthUntilBasicAttack` | Number | `1` |

### Context: `StatusOnBreak`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyToRandomPartyMemberIfPossible` | Block | `{ ... }` |
| `Bruise` | Number | `3` |
| `ChangeTilesUnder` | Enum/String | `WaterTile` |
| `ConstitutionUp` | Number | `1` |
| `DexterityUp` | Number | `1` |
| `FindItemFromPool` | Enum/String | `common` |
| `FindItem` | Enum/String | `Pearl` |
| `GainCoinsRange` | Block | `{ ... }` |
| `GainDisorder` | Enum/String | `Psychosis` |
| `HealthGain` | Number | `10` |
| `HealthRegenUp` | Number | `3` |
| `IntelligenceUp` | Number | `1` |
| `ObjectOnHitCharacter` | Enum/String | `BestBud` |
| `PermanentConstitution` | Number | `2` |
| `StrengthUp` | Number | `1` |

### Context: `StatusOnBreakItem`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DoDamage` | Block | `{ ... }` |
| `Shield` | Number | `3` |

### Context: `StatusOnCastSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `1` |
| `Shield` | Number | `1` |

### Context: `StatusOnCollectPickup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `StatusAfterXStacks` | Block | `{ ... }` |

### Context: `StatusOnDie`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_RandomChance` | Block | `{ ... }` |
| `CreateGlobalModifiers` | Block | `{ ... }` |
| `FindItemFromPool` | Enum/String | `chapter_common` |
| `GainCoinsRange` | Block | `{ ... }` |
| `RandomMagicMissile` | Number | `6` |
| `RandomStatusFromPool` | Block | `{ ... }` |

### Context: `StatusOnDodge`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DodgeChance_Status` | Number | `2` |

### Context: `StatusOnEatFood`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` |
| `TempPassiveUntilSettled` | Block | `{ ... }` |

### Context: `StatusOnEndMove`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `2` |
| `DivineShield` | Number | `1` |
| `ImmediateUseAbility` | Enum/String | `head_MagnetoAttract` |
| `SpeedUp` | Number | `1` |

### Context: `StatusOnEnemyDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `1` |

### Context: `StatusOnFallAsleep`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `FillMana` | Number | `1` |
| `HealRandomInjury` | Number | `1` |

### Context: `StatusOnFullMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_OncePerBattle` | Block | `{ ... }` |

### Context: `StatusOnGainCoins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `LuckUp` | Number | `2` |
| `Shield` | Enum/String | `X` |

### Context: `StatusOnHealed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Shield` | Number | `1` |

### Context: `StatusOnKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BrittleCharismaUp` | Number | `2` |
| `BrittleConstitutionUp` | Number | `2` |
| `BrittleDexterityUp` | Number | `2` |
| `BrittleIntelligenceUp` | Number | `2` |
| `BrittleLuckUp` | Number | `2` |
| `BrittleSpeedUp` | Number | `2` |
| `BrittleStrengthUp` | Number | `2` |
| `CharismaUp` | Number | `1` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `ConstitutionUp` | Number | `1` |
| `DexterityUp` | Number | `1` |
| `EquipPermanentItem` | Enum/String | `BoneClub` |
| `HealthGain` | Number | `5` |
| `HealthRegenUp` | Number | `1` |
| `IntelligenceUp` | Number | `1` |
| `LuckUp` | Number | `1` |
| `SpeedUp` | Number | `1` |
| `StrengthUp` | Number | `1` |

### Context: `StatusOnKillEnemy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Number | `1` |
| `DamageUp` | Number | `1` |
| `ForceUseAbility` | Enum/String | `head_CatChestPound` |
| `LuckUp` | Number | `1` |
| `ManaGain` | Number | `2` |

### Context: `StatusOnPickupCoins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `GainCoins` | Number | `1` |

### Context: `StatusOnPopCorpse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthGain` | Number | `5` |
| `RepairTrinket` | Number | `1` |
| `RepairWeapon` | Number | `1` |

### Context: `StatusOnTakeHealthOrShieldDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `DivineShield` | Array | `[ 1 .33 ], [ 1 .5 ]` |
| `Metronome` | Number | `1` |

### Context: `StatusOnTookDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `Charge` | Number | `1, 2` |
| `Conditional_HasStatus` | Block | `{ ... }` |
| `Conditional_HealthThreshold` | Block | `{ ... }` |
| `DamageUp` | Number | `2` |
| `DivineShield` | Array | `[ 1, .33 ]` |
| `DodgeChance_Status` | Number | `5` |
| `RemoveStatus` | Enum/String | `AlphaCat` |
| `StrengthUp` | Number | `1` |
| `Temporary` | Block | `{ ... }` |
| `Thorns` | Number | `1` |

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `1` |
| `DamageUp` | Number | `1` |
| `HealthRegenUp` | Number | `1` |
| `Shield` | Number | `1` |
| `SpellDamageUp` | Number | `1` |
| `Thorns` | Number | `1` |
| `type` | Enum/String | `move, attack, spell` |

### Context: `StatusOnUseBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DamageUp` | Number | `1` |
| `HealthGain` | Number | `1` |

### Context: `StatusRandomEnemiesOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charmed` | Number | `2` |
| `Confusion` | Number | `2` |
| `Fear` | Number | `2` |
| `Freeze` | Number | `2` |
| `count` | Number | `1, 99` |

### Context: `StatusWhenAllySpendsMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `2` |

### Context: `TempPassiveUntilSettled`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `LimitHeal` | Number | `0` |

### Context: `Temporary`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `expires_on_begin_turn` | Boolean | `true` |
| `expires_on_end_turn` | Boolean | `true` |
| `stacks` | Number | `1, 2, 3` |
| `status` | Enum/String | `SpeedUp, Brace, FreeSpell` |
| `turns` | Number | `1` |

### Context: `TintItem`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `add` | Array | `[ 0.05 0.05 0.05 ]` |
| `ignore_if_str_aux_equals` | Enum/String | `ModelingClay_Default` |
| `mul` | Array | `[ 0.45 0.3 0.25 ]` |

### Context: `TransformItemOnElementInfluence`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Fire, Greater_Water` |
| `full_repair` | Boolean | `true` |
| `item` | Enum/String | `EstusFlask_Full, GallonOfWater, WaterBottle_Full` |

### Context: `TransformWeapon`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `from` | Enum/String | `Necro_SoulDagger_Charged` |
| `to` | Enum/String | `Necro_SoulDagger_Uncharged` |

### Context: `TunnelVision`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `crit_chance` | Number | `50%` |

### Context: `bonus_passives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ModifyAbility` | Block | `{ ... }` |

### Context: `cost`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `charge` | Number | `1` |
| `mana` | Number | `0` |

### Context: `damage_instance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `0` |
| `effects` | Block | `{ ... }` |
| `type` | Enum/String | `status` |

### Context: `effects`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Blind` | Number | `1` |
| `BounceObject` | Enum/String | `CharmedDip, RandomPickup` |
| `Bruise` | Number | `1` |
| `Burn` | Number | `1` |
| `Cleave` | Number | `1` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `Confusion` | Number | `2` |
| `Fear` | Array | `[ 1, .15 ], [ 1, .5 ], [ 1, .25 ]` |
| `Freeze` | Array | `[ 1, .25 ]` |
| `Grappled` | Array | `[ 1, .75 ], [ 1, .50 ]` |
| `Immobile` | Number | `1` |
| `Poison` | Number | `1` |
| `Slow` | Number | `1` |
| `Stun` | Array | `[ 1, .25 ], [ 1, .1 ]` |
| `VisualFXTile` | Enum/String | `WaterConduct` |
| `VisualFX` | Enum/String | `Bolt` |

### Context: `global_passives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | `100%, 30%` |
| `NoCorpses` | Number | `1` |
| `RealTimePressure` | Number | `5` |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `1` |
| `Immobile` | Number | `1` |

### Context: `meta`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `is_basic_attack` | Boolean | `false` |
| `is_weapon` | Boolean | `true` |

### Context: `passive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Metal` | Number | `1` |

### Context: `passives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AIControlNextTurn` | Block | `{ ... }` |
| `AOEBonus` | Number | `1` |
| `AbilityHealthThreshold` | Block | `{ ... }` |
| `AbilityOnBattleStart` | Enum/String | `face_FartFaceFixed, face_FartFace, head_SpiderInjector` |
| `AbilityOnRoundEndOnce` | Block | `{ ... }` |
| `AbilityReaction` | Enum/String | `head_EmoSong` |
| `AddAdvantageToEvent` | Block | `{ ... }` |
| `AddBonusMeleeRange` | Number | `1` |
| `AddBonusRange` | Number | `1, 2, 10` |
| `AddCorpseHealth` | Number | `6, -999999` |
| `AddCritMultiplier` | Number | `33%` |
| `AddDamageToElementDamage` | Block | `{ ... }` |
| `AddElementsToBasicAttack` | Enum/String | `Holy` |
| `AddEndOfCombatRegen` | Number | `12, 999999` |
| `AddHiddenTag` | Enum/String | `the_nuke_bearer` |
| `AddInitiative` | Number | `-20, 100` |
| `AddKnockbackDamage` | Number | `1` |
| `AddLevelUpRerolls` | Number | `1, 2, 3` |
| `AddManaRegen` | Number | `1, 2, 3` |
| `AddPassivesToCharmed` | Block | `{ ... }` |
| `AddPassivesToMinions` | Block | `{ ... }` |
| `AddSelfStatusToBasicAttack` | Block | `{ ... }` |
| `AddSelfStatusToWeapons` | Block | `{ ... }` |
| `AddStatusToAllDamage` | Block | `{ ... }` |
| `AddStatusToBackstabs` | Block | `{ ... }` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `AddStatusToElementDamage` | Block | `{ ... }` |
| `AddStatusToKnockbackDamage` | Block | `{ ... }` |
| `AddStatusToSpells` | Block | `{ ... }` |
| `AddStatusToWeapons` | Block | `{ ... }` |
| `AddTag` | Enum/String | `bug, rock` |
| `AddTemporaryEffectsToBasicAttack` | Block | `{ ... }` |
| `AllSpellsCostCharge` | Number | `1` |
| `AllStatsUpPerDisorder` | Number | `1` |
| `AllStatsUp` | Number | `1` |
| `AllUnitsExplodeOnDeath` | Number | `5` |
| `AlliesScrambleSpellAfterCast` | Number | `1` |
| `AlluringDoodieEater` | Block | `{ ... }` |
| `AllyDamageReduction` | Number | `0` |
| `AllyDodgeChanceAura` | Block | `{ ... }` |
| `AlphaAllStatsUp` | Number | `1` |
| `AlphaCat` | Number | `1` |
| `AlphaTurns` | Number | `1, -1` |
| `AlwaysChosenForLevelUp` | Number | `1` |
| `AmplifyKnockback` | Number | `2, 10` |
| `AmplifyStatus` | Enum/String | `Poison, Bleed` |
| `ApplyStatusesToRandomEnemiesEachTurn` | Block | `{ ... }` |
| `ArmorBreakOnHit` | Block | `{ ... }` |
| `ArmorDodgeChance` | Number | `5%, 15%, 10%` |
| `AutoEquipConsumables` | Number | `1` |
| `BackflipWhenTargeted` | Block | `{ ... }` |
| `BackstabCritChance` | Enum/String | `.25` |
| `BalanceStats` | Number | `1` |
| `BasicAttackCantMiss` | Number | `1` |
| `BasicAttackCritChance` | Enum/String | `.1` |
| `BleedThorns` | Number | `6, 1, 3` |
| `Bleed` | Number | `6, 1, 3` |
| `Blind` | Number | `-1` |
| `BlockDamageUnderThreshold` | Number | `1` |
| `BlockNegativeStatus` | Number | `30%` |
| `BoneArmorPassive` | Number | `1` |
| `BonusAbility` | Enum/String | `WasteTime, neck_NukeBonus` |
| `BoostHeals` | Number | `1, 2` |
| `BoostReceivedHealing` | Number | `2` |
| `BoostWeaponDamage` | Block | `{ ... }` |
| `BouncyProjectiles` | Block | `{ ... }` |
| `Brace` | Number | `1, 2, 3` |
| `BreakAtAux` | Number | `0` |
| `BreakOnElement` | Enum/String | `water` |
| `BreakWhenNoShield` | Number | `1` |
| `BrittleDuringElement` | Enum/String | `water` |
| `Brittle` | Number | `1` |
| `Bruise` | Number | `1, 2` |
| `BuffImmunity` | Block | `{ ... }` |
| `Burn` | Number | `2` |
| `CanLevelUpWhenDead` | Number | `1` |
| `CanRemoveCursedItems` | Number | `1` |
| `CantCatchDiseases` | Number | `1` |
| `CantSpreadDiseases` | Number | `1` |
| `CapBasicAttackDamage` | Number | `1` |
| `CapMovementAbilityRange` | Number | `1` |
| `CatPartsSizeScale` | Block | `{ ... }` |
| `CatchProjectiles` | Block | `{ ... }` |
| `ChanceToAmbush` | Number | `25%` |
| `ChanceToBackflip` | Block | `{ ... }` |
| `ChanceToBlockAndCounter` | Number | `25%, { ... }` |
| `ChanceToBlock` | Number | `10%` |
| `ChanceToForceEvent` | Block | `{ ... }` |
| `ChanceToRevive` | Number | `25, 100, { ... }` |
| `Charge` | Number | `5` |
| `CharismaIsMaxStat` | Number | `1` |
| `CharmImmunity` | Number | `1` |
| `ClassManaCostReduction` | Block | `{ ... }` |
| `Confusion` | Number | `2, 99, 3` |
| `ConsumableEffectsMultiplierBonus` | Number | `1` |
| `ConvertDamageToScaledStatus` | Block | `{ ... }` |
| `CopyPassiveSlot` | Number | `1, 0` |
| `CounterAttack` | Block | `{ ... }` |
| `CounterNextAttacks` | Number | `2` |
| `CreateGlobalModifiers` | Block | `{ ... }` |
| `CritChanceUp` | Number | `5, 10, 100` |
| `CritsApplyStatus` | Block | `{ ... }` |
| `DamageUp` | Number | `6, 1, -2` |
| `DeathRattleRevive` | Enum/String | `DoNothing, tk_PetrifiedPinky` |
| `DeathRattle` | Enum/String | `neck_NukeExplode` |
| `DebuffImmunity` | Number | `1` |
| `DelayedAutoRevive` | Block | `{ ... }` |
| `DepressionAura` | Number | `1, 2` |
| `DisableAbilities` | Enum/String | `all_items, basic_attack, all_spells` |
| `DisablePassiveSlot` | Number | `1, 0` |
| `DodgeChance_Status` | Number | `40, 15, 10` |
| `DodgeChance` | Number | `15%, 25%` |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | `3` |
| `DoubleCastTaggedSpells` | Enum/String | `musical` |
| `DoubleCastWeapons` | Number | `1` |
| `DoubleReceivedNegativeStatus` | Number | `1` |
| `DoubleReceivedPositiveStatus` | Number | `1` |
| `DropAsFamiliarOnArmorBreak` | Enum/String | `FaceGrubFamiliar, NeckGrubFamiliar, HeadGrubFamiliar` |
| `DropAsFamiliarOnTookDamage` | Enum/String | `PhantomMaskRock` |
| `DropSoulJarOnDeath` | Enum/String | `SoulJar_Full` |
| `DurabilityTransform` | Block | `{ ... }` |
| `ElementImmune` | Enum/String | `Ice, Fire` |
| `ElementalManaCostReduction` | Block | `{ ... }` |
| `Eternal` | Block | `{ ... }` |
| `ExcludeFromEvents` | Enum/String | `Tragedy` |
| `ExplosionImmunity` | Number | `1` |
| `ExtraBasicAttacks_Status` | Number | `1` |
| `ExtraBasicAttacks` | Number | `1, 2` |
| `ExtraBasicMoves_Status` | Number | `1` |
| `ExtraMovePoints` | Number | `1` |
| `ExtraStatusWhenDealingDamage` | Block | `{ ... }` |
| `ExtraTrinketUses` | Number | `10` |
| `ExtraWeaponAttacks` | Number | `1, 2` |
| `FaceArmorPassiveMultiplierBonus` | Number | `1, 2` |
| `FaceShield` | Number | `1` |
| `FindExtraItemFromPoolOnBattleEnd` | Enum/String | `combat_reward_easy` |
| `Flammable` | Number | `1, 2` |
| `FlowersOnEndTurn` | Number | `1` |
| `FlyDamageIncrease` | Block | `{ ... }` |
| `Flying` | Number | `1` |
| `FragileDuringElement` | Enum/String | `water` |
| `Fragile` | Number | `1` |
| `FrankBolts` | Number | `1` |
| `FreezePiercing` | Number | `1` |
| `GainExtraShield` | Number | `4` |
| `GlobalMeleeRevengeDamage` | Block | `{ ... }` |
| `HPGainBlock` | Number | `1` |
| `HeadArmorPassiveMultiplierBonus` | Number | `1, 2` |
| `HealthRegenUp` | Number | `1, 2, 3` |
| `HideSomeHudStuff` | Number | `1` |
| `IgnoreTiles` | Number | `1` |
| `IncreaseExplosionDamage` | Number | `1, 2` |
| `IncreaseExplosionSize` | Number | `1, 7` |
| `IncreaseSpellRange` | Number | `2` |
| `InjuryImmunity` | Number | `1` |
| `InnateElement` | Enum/String | `Ice` |
| `ItemAuxTransform` | Block | `{ ... }` |
| `JesterLevelUpRerolls` | Number | `1` |
| `KillsToMeat` | Enum/String | `Food` |
| `KineticSpikes` | Number | `1, 3` |
| `KnockbackImmunity` | Number | `1` |
| `LeaveBehindOnceEachMove` | Enum/String | `Scrap, Poop` |
| `LevelUpClassOverride` | Enum/String | `Jester` |
| `Lifesteal` | Number | `1` |
| `LuckUp` | Number | `222` |
| `MakeBasicAttackPull` | Number | `1` |
| `MakeSpellsRequireCharge` | Number | `1` |
| `ManaCostReduction` | Number | `1, 2, -2` |
| `MeleeRevengeDamage` | Block | `{ ... }` |
| `Metal` | Number | `1` |
| `MissChance` | Number | `10` |
| `ModelingClayPassive` | Number | `1` |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | Enum/String | `face_EatNeverstone` |
| `MoveQuivered` | Number | `1, 2` |
| `MoveSpeedMultiplier` | Enum/String | `.5` |
| `MoveTowardsDamageSource` | Enum/String | `MoveOne` |
| `MovementReaction` | Block | `{ ... }` |
| `MultiplyCoinsOnBattleStart` | Number | `2` |
| `MultiplyReceivedHealing` | Number | `2` |
| `NeckArmorPassiveMultiplierBonus` | Number | `1` |
| `ObjectDetector` | Block | `{ ... }` |
| `OverrideBasicAttack` | Enum/String | `BasicSpin, BasicTankMelee, IsaacBasicAttack` |
| `PassiveAfterXKills` | Block | `{ ... }` |
| `PassiveAtHealthThreshold` | Block | `{ ... }` |
| `PassiveAtStatThreshold` | Block | `{ ... }` |
| `PassiveIfStrAuxEquals` | Block | `{ ... }` |
| `PassiveIfWeaponIsUsable` | Block | `{ ... }` |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` |
| `PassiveWhenDead` | Block | `{ ... }` |
| `PassiveWhenOnTile` | Block | `{ ... }` |
| `PassiveWhileHasDurability` | Block | `{ ... }` |
| `PassiveWhileInMonkMeleeStance` | Block | `{ ... }` |
| `PassiveWhileShielded` | Block | `{ ... }` |
| `PermanentMadness` | Number | `1` |
| `PhysicalAttacksMiss` | Number | `1` |
| `PoisonThorns` | Number | `1` |
| `Poison` | Number | `1, 2, 3` |
| `PoopWhenHit` | Block | `{ ... }` |
| `PreventSpecificInjury` | Enum/String | `int` |
| `Quivered` | Number | `1, 2` |
| `RandomSeededStatModifier` | Array | `[ 2 -1 ]` |
| `RangedTrueShot` | Number | `1` |
| `ReclaimItemOnBreak` | Number | `1` |
| `ReduceManaCost` | Number | `2` |
| `ReduceSpellCostsPerDisorder` | Number | `1` |
| `ReduceSpellCostsPerParasite` | Number | `1` |
| `ReflectProjectiles` | Number | `25%, 20%` |
| `RefreshEquipmentAbilityOnElement` | Block | `{ ... }` |
| `RemoveLineOfSightRestrictions` | Number | `1` |
| `ReplaceBasicAttack` | Enum/String | `head_Pestilence, BasicPoke` |
| `ReplaceBasicMove` | Enum/String | `head_HeadBrandJump, BellyFlop_BasicMove, BasicJump` |
| `ReplaceBlankTilesOnBattleStart` | Enum/String | `GlassTile` |
| `ReplaceSpawnedObjects` | Array | `[ FlamingPoop RandomLivingPoop ], [ Poop RandomLivingPoop ]` |
| `RerollItemsOnBattleEnd` | Number | `1` |
| `RevengeDamage` | Block | `{ ... }` |
| `RockyArmorPassive` | Number | `1` |
| `ScaldingOrbMoonBossOneShot` | Block | `{ ... }` |
| `ScaledStatusAlliesOnSpendMana` | Block | `{ ... }` |
| `ScaledStatusOnHolyShieldBlock` | Block | `{ ... }` |
| `ScaledStatusOnSpendMana` | Block | `{ ... }` |
| `SetBrittleImmune` | String | `""` |
| `SetDefaultFacePassive` | Enum/String | `euphoric` |
| `SetFaction` | Enum/String | `enemies` |
| `SetFragileImmune` | String | `""` |
| `SetSpellCosts` | Number | `0` |
| `SharkySmellsBlood` | Number | `1` |
| `SpawnCatCloneOnCorpsePopped` | Number | `1` |
| `SpawnEachTurn` | Block | `{ ... }` |
| `SpawnExtraThingsOnBattleStart` | Block | `{ ... }` |
| `SpawnItemLinkedFamiliar` | Block | `{ ... }` |
| `SpawnNearEnemies` | Number | `1` |
| `SpawnObjectOnPopCorpse` | Enum/String | `Coin, Food, { ... }` |
| `SpawnOnBattleStartRandomEmptyTile` | Block | `{ ... }` |
| `SpawnOnBattleStart` | Enum/String | `CharmedCultist, CharmedGamete, { ... }` |
| `SpawnOnDeath` | Block | `{ ... }` |
| `SpawnOnDowned` | Enum/String | `CharmedSpookie` |
| `SpawnRandomPickupsOnTaggedUnitKilled` | Block | `{ ... }` |
| `SpawnThingOnDamage` | Block | `{ ... }` |
| `SpawnThingOnDeath` | Enum/String | `CharmedTinyTumor, TheIntruder, CharmedPooter` |
| `SpellDamageUp` | Number | `1, 3` |
| `StackingFlowerTrail` | Block | `{ ... }` |
| `StatDependentPassive` | Block | `{ ... }` |
| `StatusAdjacentOnTheirTurnEnd` | Block | `{ ... }` |
| `StatusAfterCastSpell` | Block | `{ ... }` |
| `StatusAfterXTurns` | Block | `{ ... }` |
| `StatusAllCharactersOnSpawn` | Block | `{ ... }` |
| `StatusAlliesEachTurn` | Block | `{ ... }` |
| `StatusAlliesOnBattleStart` | Block | `{ ... }` |
| `StatusAlliesOnDeath` | Block | `{ ... }` |
| `StatusEachTurnBegin` | Block | `{ ... }` |
| `StatusEachTurnEndForEachTurn` | Block | `{ ... }` |
| `StatusEachTurnEnd` | Block | `{ ... }` |
| `StatusEveryXSpellCasts` | Block | `{ ... }` |
| `StatusIfUnusedActPoints` | Block | `{ ... }` |
| `StatusIfUnusedMovePoints` | Block | `{ ... }` |
| `StatusImmunity` | Enum/String | `Poison, [ Freeze, Slow ], [ Fear Confusion PermanentConfusion ]` |
| `StatusOnAllyCatDeath` | Block | `{ ... }` |
| `StatusOnBackstab` | Block | `{ ... }` |
| `StatusOnBattleEnd` | Block | `{ ... }` |
| `StatusOnBattleStart` | Block | `{ ... }` |
| `StatusOnBreakItem` | Block | `{ ... }` |
| `StatusOnBreak` | Block | `{ ... }` |
| `StatusOnCastSpell` | Block | `{ ... }` |
| `StatusOnCollectPickup` | Block | `{ ... }` |
| `StatusOnDie` | Block | `{ ... }` |
| `StatusOnDodge` | Block | `{ ... }` |
| `StatusOnEatFood` | Block | `{ ... }` |
| `StatusOnEndMove` | Block | `{ ... }` |
| `StatusOnEnemyDeath` | Block | `{ ... }` |
| `StatusOnFallAsleep` | Block | `{ ... }` |
| `StatusOnFullMana` | Block | `{ ... }` |
| `StatusOnGainCoins` | Block | `{ ... }` |
| `StatusOnHealed` | Block | `{ ... }` |
| `StatusOnKillEnemy` | Block | `{ ... }` |
| `StatusOnKill` | Block | `{ ... }` |
| `StatusOnPickupCoins` | Block | `{ ... }` |
| `StatusOnPopCorpse` | Block | `{ ... }` |
| `StatusOnTakeHealthOrShieldDamage` | Block | `{ ... }` |
| `StatusOnTookDamage` | Block | `{ ... }` |
| `StatusOnTurnEndIfDidntCastAbilityTypes` | Block | `{ ... }` |
| `StatusOnUseBasicAttack` | Block | `{ ... }` |
| `StatusRandomEnemiesOnBattleStart` | Block | `{ ... }` |
| `StatusWhenAllySpendsMana` | Block | `{ ... }` |
| `StevenBolts` | Number | `1` |
| `StripKnockback` | Number | `1` |
| `TauntAlways` | Number | `1` |
| `Thorns` | Number | `1, 2, 3` |
| `TintItem` | Block | `{ ... }` |
| `Trample` | Number | `3` |
| `TransformItemOnElementInfluence` | Block | `{ ... }` |
| `TrinketActiveEffectsMultiplierBonus` | Number | `1, 2` |
| `TrinketPassiveMultiplierBonus` | Number | `1, 2` |
| `TrueShot` | Number | `1` |
| `TunnelVision` | Block | `{ ... }` |
| `Uncontrollable` | Number | `1` |
| `Undead` | Number | `1` |
| `WeaponDamageMultiplierBonus` | Number | `1` |

### Context: `str_aux_is_copy_ability`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bonus_passives` | Block | `{ ... }` |

### Context: `threshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `con` | Number | `0` |
| `int` | Number | `0` |

---

## Map Generation & Routing

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `#include` | String | `"standard_nodes.gon"` |
| `BoneyardUnlocked` | Block | `{ ... }` |
| `BothObelisksUnlocked` | Block | `{ ... }` |
| `BunkerUnlocked` | Block | `{ ... }` |
| `CavesUnlocked` | Block | `{ ... }` |
| `ChaosAntennaAttached` | Block | `{ ... }` |
| `CoreObeliskUnlocked` | Block | `{ ... }` |
| `CoreUnlocked` | Block | `{ ... }` |
| `CraterUnlocked` | Block | `{ ... }` |
| `DimensionXUnlocked` | Block | `{ ... }` |
| `EndOfTimeUnlocked` | Block | `{ ... }` |
| `FutureUnlocked` | Block | `{ ... }` |
| `GenFlag_Boss_Spewer` | Block | `{ ... }` |
| `GenFlag_Boss_Stacy` | Block | `{ ... }` |
| `HardPathUnlocked` | Block | `{ ... }` |
| `IceAgeUnlocked` | Block | `{ ... }` |
| `JunkyardUnlocked` | Block | `{ ... }` |
| `JurassicUnlocked` | Block | `{ ... }` |
| `MeatWorldUnlockedFull` | Block | `{ ... }` |
| `MeatWorldUnlocked` | Block | `{ ... }` |
| `MoonObeliskUnlocked` | Block | `{ ... }` |
| `MoonUnlocked` | Block | `{ ... }` |
| `SewersUnlocked` | Block | `{ ... }` |
| `TheEndUnlocked` | Block | `{ ... }` |
| `ThrobbingArteryDone` | Block | `{ ... }` |
| `VolcanoAntennaAttached` | Block | `{ ... }` |
| `WallOfFleshDone` | Block | `{ ... }` |
| `abandonedones` | Enum/String | `auto` |
| `advance` | Number | `1` |
| `alley` | Block | `{ ... }` |
| `battle` | Block | `{ ... }` |
| `boneyard` | Block | `{ ... }` |
| `boss` | Block | `{ ... }, [ boss ]` |
| `bumblefoot` | Enum/String | `auto` |
| `bunker` | Block | `{ ... }` |
| `butchercat` | Enum/String | `auto` |
| `cancreeper` | Enum/String | `auto` |
| `cavecatfamily` | Enum/String | `auto` |
| `caves` | Block | `{ ... }` |
| `cerberubs` | Enum/String | `auto` |
| `chapter_item_pool` | Enum/String | `bunkeritems, boneyarditems, alleyitems` |
| `choose_one` | Array | `[ GenFlag_Boss_Stacy, GenFlag_Boss_Spewer ]` |
| `clericcat` | Enum/String | `auto` |
| `core` | Block | `{ ... }` |
| `crater` | Block | `{ ... }` |
| `desert` | Block | `{ ... }` |
| `dimensionx` | Block | `{ ... }` |
| `dinocouple` | Enum/String | `auto` |
| `drmangler` | Enum/String | `auto` |
| `druidcat` | Enum/String | `auto` |
| `easy` | Array | `[ easy ], [ easy bigsharklevels ]` |
| `endoftime` | Block | `{ ... }` |
| `event` | Block | `{ ... }` |
| `exit0` | Block | `{ ... }` |
| `exit1` | Block | `{ ... }` |
| `exit_desert` | Block | `{ ... }` |
| `exit_lab` | Block | `{ ... }` |
| `fightercat` | Enum/String | `auto` |
| `flushmaster` | Enum/String | `auto` |
| `folder` | Enum/String | `bunker, boneyard, alley` |
| `future` | Block | `{ ... }` |
| `gambit` | Enum/String | `auto` |
| `hard_initial` | Block | `{ ... }` |
| `hard` | Array | `[ easy ], [ easy bigsharklevels ], [ hard ]` |
| `head_start` | Number | `99` |
| `home` | Block | `{ ... }` |
| `huntercat` | Enum/String | `auto` |
| `iceage` | Block | `{ ... }` |
| `iceelemental` | Enum/String | `auto` |
| `infestedduo` | Enum/String | `auto` |
| `jestercat` | Enum/String | `auto` |
| `junkyard` | Block | `{ ... }` |
| `jurassic` | Block | `{ ... }` |
| `lab` | Block | `{ ... }` |
| `large` | Array | `[ KillDozer ], [ ], [ Shambler ]` |
| `lenny` | Enum/String | `auto` |
| `level` | Enum/String | `Treasure_LargeMeteor, TreasureHard, Treasure_SmallMeteor` |
| `lightningelemental` | Enum/String | `auto` |
| `locked` | Boolean | `true` |
| `magecat` | Enum/String | `auto` |
| `mamamaggot` | Enum/String | `auto` |
| `meatworld` | Block | `{ ... }` |
| `medium` | Array | `[ Rat Leaper Pooter Kitten TomTom Mangy CatCaller ], [ AtomicKitten RoboTom CatCultist Cultist CultistZealot C..., [ ZombieCat SkeletonCat TallSkeletonCat WolfCat Tatters S...` |
| `miniboss_event` | Block | `{ ... }` |
| `miniboss` | Array | `[ miniboss ]` |
| `monkcat` | Enum/String | `auto` |
| `moon` | Block | `{ ... }` |
| `musiclayer` | Enum/String | `boss` |
| `mw_altar` | Block | `{ ... }` |
| `mw_battle1` | Block | `{ ... }` |
| `mw_boss` | Block | `{ ... }` |
| `mw_earlyhome` | Block | `{ ... }` |
| `mw_event1` | Block | `{ ... }` |
| `mw_hard1` | Block | `{ ... }` |
| `mw_home` | Block | `{ ... }` |
| `mw_quest_event` | Block | `{ ... }` |
| `mw_treasure` | Block | `{ ... }` |
| `necrocat` | Enum/String | `auto` |
| `nemesis` | Array | `[ nemesis ]` |
| `normal` | Array | `[ common alley_events.gon ], [ common boneyard_events.gon ], [ common bunker_events.gon ]` |
| `override_art` | Enum/String | `MapNode_SmallMeteor, Rare_Treasure, MapNode_LargeMetor` |
| `psychiccat` | Enum/String | `auto` |
| `queenhippo` | Enum/String | `auto` |
| `quest_event` | Block | `{ ... }` |
| `radicalrat` | Enum/String | `auto` |
| `rare` | Array | `[ rare ]` |
| `ratking` | Enum/String | `auto` |
| `repeat` | Enum/String | `never` |
| `rockybobo` | Enum/String | `auto` |
| `sewers` | Block | `{ ... }` |
| `shop_cheapwater` | Block | `{ ... }` |
| `shop_water` | Block | `{ ... }` |
| `slime` | Enum/String | `auto` |
| `small` | Array | `[ Maggot Fly Flea Pinky ], [ ], [ Flea Wisp Fly Maggot ]` |
| `spawn_node` | Enum/String | `start` |
| `special` | Array | `[ special ]` |
| `spewer` | Enum/String | `auto` |
| `stacy` | Enum/String | `auto` |
| `start` | Block | `{ ... }` |
| `tankcat` | Enum/String | `auto` |
| `thebloat` | Enum/String | `auto` |
| `theend` | Block | `{ ... }` |
| `thiefcat` | Enum/String | `auto` |
| `time_machine` | Block | `{ ... }` |
| `tinkerercat` | Enum/String | `auto` |
| `trampy` | Enum/String | `auto` |
| `treasure` | Block | `{ ... }` |
| `type` | Enum/String | `battle, empty, npc` |
| `weather_event` | Block | `{ ... }` |
| `zodiac` | Enum/String | `auto` |

### Context: `BoneyardUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `BothObelisksUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `BunkerUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `CavesUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `ChaosAntennaAttached`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `CoreObeliskUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `CoreUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `CraterUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit1` | Block | `{ ... }` |

### Context: `DimensionXUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `EndOfTimeUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `FutureUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `GenFlag_Boss_Spewer`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `boss` | Block | `{ ... }` |

### Context: `GenFlag_Boss_Stacy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `boss` | Block | `{ ... }` |
| `miniboss_event` | Block | `{ ... }` |

### Context: `HardPathUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hard_initial` | Block | `{ ... }` |

### Context: `IceAgeUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `JunkyardUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit1` | Block | `{ ... }` |

### Context: `JurassicUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `MeatWorldUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |
| `quest_event` | Block | `{ ... }` |

### Context: `MeatWorldUnlockedFull`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `mw_battle1` | Block | `{ ... }` |
| `mw_boss` | Block | `{ ... }` |
| `mw_earlyhome` | Block | `{ ... }` |
| `mw_event1` | Block | `{ ... }` |
| `mw_hard1` | Block | `{ ... }` |
| `mw_home` | Block | `{ ... }` |
| `mw_quest_event` | Block | `{ ... }` |
| `mw_treasure` | Block | `{ ... }` |

### Context: `MoonObeliskUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `MoonUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `SewersUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `TheEndUnlocked`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |

### Context: `ThrobbingArteryDone`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `VolcanoAntennaAttached`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `WallOfFleshDone`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |

### Context: `battle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `type` | Enum/String | `battle` |

### Context: `boss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `boss_cutscene` | Enum/String | `dybbuk, johnny, spiderkitten` |
| `is_final_boss` | Boolean | `true` |
| `level` | Enum/String | `stacy, spewer` |
| `override_music` | Enum/String | `chaos_boss, finalboss` |
| `tileset` | Enum/String | `finalboss` |
| `type` | Enum/String | `boss` |
| `unlockcheck_on_complete` | Enum/String | `map_unlock_junkyard` |

### Context: `dimensionx`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |

### Context: `endoftime`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |

### Context: `event`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `Butch_Tutorial` |
| `type` | Enum/String | `event` |

### Context: `exit0`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |
| `locked` | Boolean | `false, true` |
| `next_map` | Enum/String | `meatworld.gon, core.gon, sewers.gon` |
| `override_art` | Enum/String | `MapNodeExit_MeatWorld, MapNodeExit_Core, MapNodeExit_Sewers` |
| `type` | Enum/String | `exit` |

### Context: `exit1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |
| `next_map` | Enum/String | `crater.gon, junkyard.gon, future.gon` |
| `override_art` | Enum/String | `MapNodeExit_Future, MapNodeExit_Junkyard, MapNodeExit_Crater` |
| `type` | Enum/String | `exit` |

### Context: `exit_desert`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `true` |
| `locked` | Boolean | `true` |
| `next_map` | Enum/String | `desert.gon` |
| `override_art` | Enum/String | `MapNodeExit_Desert` |
| `type` | Enum/String | `exit` |

### Context: `exit_lab`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `true` |
| `locked` | Boolean | `true` |
| `next_map` | Enum/String | `lab.gon` |
| `override_art` | Enum/String | `MapNodeExit_Lab` |
| `type` | Enum/String | `exit` |

### Context: `future`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |

### Context: `hard_initial`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |
| `type` | Enum/String | `hard` |

### Context: `home`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `type` | Enum/String | `home` |

### Context: `iceage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |

### Context: `jurassic`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |

### Context: `miniboss_event`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `StacyMutant1` |
| `type` | Enum/String | `special_event, empty` |

### Context: `mw_altar`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `Quest_MeatWorldAltar` |
| `override_art` | Enum/String | `MapNode_MeatAltar` |
| `type` | Enum/String | `special_event` |

### Context: `mw_battle1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |
| `type` | Enum/String | `battle` |

### Context: `mw_boss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `boss_cutscene` | Enum/String | `throbbingking` |
| `hidden` | Boolean | `false, true` |
| `override_music` | Enum/String | `throbbingking` |
| `type` | Enum/String | `boss` |

### Context: `mw_earlyhome`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `true` |
| `type` | Enum/String | `home` |

### Context: `mw_event1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |
| `type` | Enum/String | `event` |

### Context: `mw_hard1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |
| `musiclayer` | Enum/String | `boss` |
| `type` | Enum/String | `hard` |

### Context: `mw_home`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |
| `type` | Enum/String | `home` |

### Context: `mw_quest_event`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |
| `level` | Enum/String | `Quest_DeadKing` |
| `override_art` | Enum/String | `MapNode_DeadKing` |
| `type` | Enum/String | `special_event` |

### Context: `mw_treasure`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |
| `type` | Enum/String | `treasure` |

### Context: `quest_event`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `Quest_ThrobbingArtery2, Quest_ThrobbingArtery, Quest_WallOfFlesh` |
| `override_art` | Enum/String | `MapNode_VeinsDrained, MapNode_Veins, MapNode_Empty` |
| `type` | Enum/String | `special_event, empty` |

### Context: `shop_cheapwater`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `WaterShopCheap` |
| `override_art` | Enum/String | `cheapwatershop` |
| `type` | Enum/String | `shop` |

### Context: `shop_water`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `WaterShop` |
| `override_art` | Enum/String | `cheapwatershop` |
| `type` | Enum/String | `shop` |

### Context: `start`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `type` | Enum/String | `enter` |

### Context: `theend`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |

### Context: `time_machine`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `Quest_TimeMachineIceAge, Quest_TimeMachineFuture, Quest_TimeMachineJurassic` |
| `override_art` | Enum/String | `MapNode_TimeMachine` |
| `type` | Enum/String | `special_event` |

### Context: `treasure`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `TreasureTutorial` |
| `type` | Enum/String | `treasure` |

### Context: `weather_event`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `level` | Enum/String | `CraterWeatherEvent` |
| `type` | Enum/String | `special_event` |

---

## Passives & Statuses

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `auto_plus_signs_on_name` | Boolean | `false` |
| `bonus_items` | Array | `[ Eyeball ]` |
| `class` | Enum/String | `Colorless, Butcher, Disorder` |
| `desc_multiclass` | String | `"PASSIVE_BARBED_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK_MULTICLASS_DESC", "PASSIVE_HOOKED_MULTICLASS_DESC"` |
| `desc` | String | `"PASSIVE_MAINCOURSE_DESC", "PASSIVE_NEVERFULL_DESC", "PASSIVE_PUTREFY_DESCRIPTION"` |
| `grant_ability` | Enum/String | `Rest` |
| `lock_item_slot` | Block | `{ ... }` |
| `name_mod` | String | `"CAT_NAME_MOD_GIGANTISM", "CAT_NAME_MOD_DWARF", "CAT_NAME_MOD_VEGAN"` |
| `name` | String | `"PASSIVE_NEVERFULL_NAME", "PASSIVE_PUTREFY_NAME", "PASSIVE_MAINCOURSE_NAME"` |
| `override_basic_attack` | Enum/String | `BasicMelee, GerdShot` |
| `passives` | Block | `{ ... }` |
| `shield` | Number | `8, 4` |
| `stats` | Block | `{ ... }` |
| `tags` | Array | `[ noncopyable ]` |

### Context: `1`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bonus_items` | Array | `[ SpiderEgg ], [ Stick Stick Stick ], [ Pipe ]` |
| `desc` | String | `"DISORDER_DEJAVU_DESC"` |
| `divine_shield` | Number | `1` |
| `empty_armor_scaled_stats` | Block | `{ ... }` |
| `keyword_tooltips` | Block | `{ ... }` |
| `override_basic_attack` | Enum/String | `BasicDruidAbilityVersatile, BasicButcherMeleeWideSpin, BasicMagicMissile` |
| `passives` | Block | `{ ... }` |
| `schadenfreude_scaled_stats` | Block | `{ ... }` |
| `shield` | Number | `2, 4` |
| `stats` | Block | `{ ... }` |

### Context: `10`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `desc` | String | `"DISORDER_DISTEMPERMAX_DESC"` |
| `passives` | Block | `{ ... }` |

### Context: `2`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `bonus_items` | Array | `[ Stick Stick Stick ], [ FoodBig FoodBig FoodBig FoodBig ], [ SpiderWebber ]` |
| `desc_multiclass` | String | `"PASSIVE_BARBED2_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC", "PASSIVE_HOOKED2_MULTICLASS_DESC"` |
| `desc` | String | `"PASSIVE_PUTREFY2_DESCRIPTION", "PASSIVE_NEVERFULL2_DESC", "PASSIVE_MAINCOURSE2_DESC"` |
| `divine_shield` | Number | `1, 3` |
| `empty_armor_scaled_stats` | Block | `{ ... }` |
| `icon` | Enum/String | `DejaVu2` |
| `keyword_tooltips` | Block | `{ ... }` |
| `override_basic_attack` | Enum/String | `BasicDruidAbilityVersatile, BasicButcherMeleeWideDoubleSpin, BasicMagicMissile` |
| `passives` | Block | `{ ... }` |
| `schadenfreude_scaled_stats` | Block | `{ ... }` |
| `shield` | Number | `8, 4` |
| `stats` | Block | `{ ... }` |

### Context: `3`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `desc` | String | `"DISORDER_SEVEREDEJAVU_DESC"` |
| `icon` | Enum/String | `DejaVu3` |
| `name` | String | `"DISORDER_SEVEREDEJAVU_NAME"` |
| `passives` | Block | `{ ... }` |

### Context: `4`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `5`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `6`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `7`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `8`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `9`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |

### Context: `AbilityChargeRefundChance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `advantage_softcap` | Number | `3.5` |
| `chance` | Number | `50%` |

### Context: `AbilityReaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |
| `ability` | Enum/String | `SpontaneouslyCombust` |
| `chance` | Number | `15%` |

### Context: `AbilityWhenTaggedCharacterMovesNear`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `move` |
| `range` | Enum/String | `global, 2` |
| `tag` | Enum/String | `food` |

### Context: `AddDamageToElementDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `1, 2` |
| `element` | Enum/String | `Fire, Electric` |

### Context: `AddPassiveToSpawnedRocks`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | `7, 3` |
| `JoinSpawnerFaction` | Number | `1` |

### Context: `AddPassivesToCharmed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddMaxHealth` | Number | `5, 10` |
| `AddSpeed` | Number | `4` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `DamageUp` | Number | `2, 3` |

### Context: `AddPassivesToMinions`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddMaxHealth` | Number | `5, 10` |
| `AddSpeed` | Number | `4` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `AddStatusToExplosions` | Block | `{ ... }` |
| `AddUnfilledMaxHealth` | Number | `10` |
| `DamageUp` | Number | `2, 3` |
| `DivineShield` | Number | `1` |
| `EMP` | Block | `{ ... }` |
| `FamiliarBonusAbility` | Enum/String | `FamiliarSelfDestruct2, FamiliarSelfDestruct` |
| `ForceAttack` | Number | `1` |
| `FreePathfindElement` | Enum/String | `Water, Grass` |
| `GrassTileHealing` | Number | `1` |
| `HealthGain` | Number | `5, 10` |
| `HealthRegenUp` | Number | `3` |
| `HolyShieldTransferToSpawner` | Number | `1` |
| `IncreaseExplosionDamage` | Number | `2, 4, 3` |
| `IncreaseExplosionSize` | Number | `2` |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` |
| `PoisonThorns` | Number | `1, 2` |
| `Quivered` | Number | `1` |
| `SafeExplosions` | Number | `1` |
| `StatusAlliesOnKill` | Block | `{ ... }` |
| `StatusOnKill` | Block | `{ ... }` |
| `TakeExtraTurn` | Number | `1` |
| `UncappedHP` | Number | `1` |
| `WaterWalk` | Number | `1` |
| `tag_filter` | Enum/String | `crow` |

### Context: `AddPassivesToSummonAbilityMinions`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DamageUp` | Number | `2, 4` |
| `Doomed` | Number | `1` |
| `MovementUp` | Number | `2, 4` |

### Context: `AddSelfStatusToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` |

### Context: `AddSelfStatusToWeapons`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ChanceToBreak` | Number | `50, 100` |

### Context: `AddStatusToAllDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Blind` | Number | `1` |
| `Conditional_HasTag` | Block | `{ ... }` |
| `LeaveBehindRockOnKnockback` | Number | `1` |
| `NonLethal` | Number | `1` |

### Context: `AddStatusToAllDamageAbilities`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `Piercing` | Number | `1` |
| `Weakness` | Number | `2` |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ApplyStatusIfCrit` | Block | `{ ... }` |
| `ApplyToSource` | Block | `{ ... }` |
| `BigSplashDamage` | Number | `2` |
| `Bleed` | Number | `1, 2` |
| `Blind` | Number | `1` |
| `BounceObject` | Enum/String | `BeefyCharmedLeech, CharmedLeech, AllyRotFly` |
| `Bruise` | Number | `1, 2` |
| `BurgleCoin` | Number | `1` |
| `Burn` | Number | `5, 1, 2` |
| `ChangeTile` | Enum/String | `BrambleTile, { ... }` |
| `Charmed` | Array | `[ 1 .25 ]` |
| `Conditional_Adjacent` | Block | `{ ... }` |
| `Conditional_Ally` | Block | `{ ... }` |
| `Conditional_Enemy` | Block | `{ ... }` |
| `Conditional_HasTag` | Block | `{ ... }` |
| `Conditional_Shielded` | Block | `{ ... }` |
| `Conditional_SourceHasTag` | Block | `{ ... }` |
| `Confusion` | Number | `1` |
| `DamageOrHealConditionally` | Number | `1` |
| `DistanceBonusDamage` | Block | `{ ... }` |
| `Else` | Block | `{ ... }` |
| `Fear` | Array | `[ 1 .25 ]` |
| `Freeze` | Array | `[ 1 .5 ], [ 1 .20 ]` |
| `KnockOutCoin` | Number | `1, [ 1 .5 ]` |
| `Knockback` | Number | `1, 4, 3` |
| `Leech` | Number | `1` |
| `Leeches` | Number | `1` |
| `LuckUp` | Number | `-1` |
| `Madness` | Number | `1` |
| `MagicWeakness` | Number | `1, 2` |
| `ManaLeeches` | Number | `1` |
| `OverrideChainKnockbackDamage` | Number | `0` |
| `OverrideChainKnockback` | Number | `0` |
| `Piercing` | Number | `1` |
| `Poison` | Number | `1, 3, [ 1 .5 ]` |
| `Rot` | Number | `1, -999999` |
| `Slow` | Number | `5, 1, 2` |
| `SoulLink` | Number | `1` |
| `SpawnBearTrapOnMiss` | Number | `1` |
| `SplashDamage` | Number | `2` |
| `SpreadDisease` | Block | `{ ... }` |
| `Stun` | Array | `[ 1 .40 ], [ 1 .15 ]` |
| `Weakness` | Number | `1` |

### Context: `AddStatusToBasicAttackWithCooldown`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CharmedForceAttack` | Number | `1` |

### Context: `AddStatusToBasicMeleeAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bruise` | Number | `1` |
| `Confusion` | Number | `1` |
| `FaceAway` | Number | `1` |
| `SpreadDisease` | Block | `{ ... }` |
| `Stun` | Array | `[ 1 .15 ], [ 1 .2 ]` |

### Context: `AddStatusToElementAbilities`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `ChangeTile` | Enum/String | `FloatingGlassTile` |
| `Conditional_Ally` | Block | `{ ... }` |
| `Conditional_Enemy` | Block | `{ ... }` |
| `element` | Enum/String | `Gravity` |

### Context: `AddStatusToElementDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Number | `1, 3` |
| `Conditional_Corpse` | Block | `{ ... }` |
| `element` | Enum/String | `Fire, Electric` |

### Context: `AddStatusToExplosions`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddElement` | Enum/String | `Napalm, Fire` |
| `Burn` | Number | `6, 3` |

### Context: `AddStatusToFirstBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charmed` | Number | `5` |

### Context: `AddStatusToKnockbackDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bruise` | Number | `1` |

### Context: `AddStatusToMeleeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DelayedWindCone` | Block | `{ ... }` |
| `DelayedWind` | Block | `{ ... }` |

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_DoesDamage` | Block | `{ ... }` |

### Context: `AddStatusToSpells`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `LeechPercent` | Number | `50` |

### Context: `AddStatusToTrampleDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Cleave` | Number | `1` |

### Context: `AddStatusToWeapons`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `Cleave` | Number | `1` |
| `LeechPercent` | Number | `50` |
| `PullSourceToKnockbackImmuneTarget` | Number | `1` |

### Context: `AddStatusesIfPersistentWeatherElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Number | `3` |
| `elements` | Array | `[ Heat Fire ]` |

### Context: `AddStatusesToReceivedElementalDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Number | `3` |
| `elements` | Array | `[ Heat Fire ]` |

### Context: `AddTemporaryEffectsToBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CastAgain` | Number | `1, 2` |
| `Fury` | Number | `75` |

### Context: `AddTemporaryEffectsToEquipment`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CastAgain` | Number | `1` |

### Context: `AllyBonusAbilityAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `Bowl, Bowl2` |
| `square` | Boolean | `true` |

### Context: `AllyHealthRegenAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `range` | Enum/String | `global` |
| `stacks` | Number | `1, 2` |

### Context: `AllyManaRegenAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `range` | Enum/String | `global` |
| `stacks` | Number | `1, 2` |

### Context: `AlternateCraftingPools`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `tinkerer_0` | Enum/String | `tinkerer_0_bombs` |
| `tinkerer_1` | Enum/String | `tinkerer_1_bombs` |

### Context: `AmplifyStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `addstacks` | Number | `2` |
| `status` | Enum/String | `Burn, Poison, Bleed` |

### Context: `ApplyStatusIfCrit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Purge` | Number | `0` |

### Context: `ApplyStatusesToRandomEnemiesEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bounty` | Number | `1, 3` |
| `count` | Number | `2` |

### Context: `ApplyToSource`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Shield` | Number | `1` |

### Context: `Autism`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `innate` | Number | `-2` |
| `learned` | Number | `1` |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `MedicObey, RaiseTheDead, MedicObey2` |
| `even_if_stunned` | Boolean | `true` |
| `force_display_name` | Boolean | `true` |

### Context: `AutocastEachTurnBegin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `PoxScratch` |
| `advantage_polarity` | Number | `-1` |
| `chance` | Number | `10%` |

### Context: `BoobyTrapItems`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `on_break` | Block | `{ ... }` |
| `on_throw` | Block | `{ ... }` |

### Context: `BoostWeaponDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `crit_chance` | Enum/String | `.25, .5` |
| `damage` | Number | `2, 3` |

### Context: `BouncyProjectiles`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `max_bounces` | Number | `1, 2` |
| `max_range` | Number | `4, 3` |

### Context: `CatAPultAnimation`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `CatapultJump2, CatapultJump` |
| `animation` | Enum/String | `knockupatk` |

### Context: `CatchProjectiles`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Quivered` | Number | `1` |
| `ally_chance` | Number | `100%` |
| `chance` | Number | `33%, 50%` |

### Context: `ChanceToBackflip`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `BlinkDodge` |
| `chance` | Number | `33%, 50%` |

### Context: `ChanceToRevive`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `stacks` | Number | `33` |
| `statuses` | Block | `{ ... }` |

### Context: `ChangeTile`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `aoe` | Number | `1` |
| `tile` | Enum/String | `BrambleTile` |

### Context: `ClassManaCostReduction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `class` | Enum/String | `Colorless` |
| `reduction` | Number | `1, 2` |

### Context: `CollectPickupsOnBattleEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pop_corpses` | Boolean | `true` |

### Context: `Conditional_Adjacent`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1, 2` |
| `BonusCritChance` | Number | `25, 50` |
| `BonusDamage` | Number | `2, 3` |

### Context: `Conditional_Ally`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, [ 1 .5 ]` |
| `ApplyToSource` | Block | `{ ... }` |
| `Cleanse` | Number | `0` |
| `ClearNegativeEffects` | Number | `1` |
| `DamageUp` | Number | `1` |
| `RandomStatusFromPool` | Block | `{ ... }` |
| `Shield` | Number | `2, 3` |
| `SpeedUp` | Number | `1` |
| `TempSpeedUp` | Number | `4` |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Temporary` | Block | `{ ... }` |
| `odds` | Enum/String | `.1` |

### Context: `Conditional_Boss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charmed` | Number | `1` |
| `Stun` | Number | `3` |

### Context: `Conditional_Corpse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charmed` | Number | `1` |
| `DamageUp` | Number | `2` |
| `OverrideDamage` | Number | `0` |
| `Revive` | Number | `1` |
| `SafeDoomed` | Number | `1` |
| `SpeedUp` | Number | `8` |
| `TakeExtraTurn` | Number | `1` |

### Context: `Conditional_DoesDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Array | `[ 1 .1 ]` |

### Context: `Conditional_Enemy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_PartyMember` | Block | `{ ... }` |
| `Confusion` | Number | `2, 3` |
| `Else` | Block | `{ ... }` |
| `RandomStatusFromPool` | Block | `{ ... }` |
| `Stun` | Array | `[ 1 .5 ]` |

### Context: `Conditional_FirstApplicationThisTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `FillMana` | Number | `1` |
| `ManaGain` | Number | `5` |
| `TakeExtraTurn` | Number | `1` |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `UseRandomSpell_Madness` | Number | `1` |
| `odds` | Number | `33%` |

### Context: `Conditional_HasStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `status` | Enum/String | `Marked, Fear` |

### Context: `Conditional_HasTag`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charmed` | Number | `1` |
| `FlatLeechIfDamaged` | Number | `5` |
| `tag` | Enum/String | `poop, rat` |

### Context: `Conditional_NotBoss`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Enemy` | Block | `{ ... }` |

### Context: `Conditional_PartyMember`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charmed` | Number | `5` |

### Context: `Conditional_Shielded`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` |

### Context: `Conditional_SourceHasTag`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Ally` | Block | `{ ... }` |
| `tag` | Enum/String | `crow` |

### Context: `Craft`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Enum/String | `tinkerer_default` |
| `slot` | Enum/String | `random_empty_armor_or_weapon` |

### Context: `CritsApplyStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `Bruise` | Number | `1` |
| `Conditional_HasStatus` | Block | `{ ... }` |
| `Confusion` | Number | `1` |
| `Else` | Block | `{ ... }` |
| `Immobile` | Number | `1` |
| `ObjectOnHitCharacter` | Enum/String | `Coin, RandomPickup` |
| `Stun` | Number | `1, [ 1 .33 ], [ 1 .25 ]` |
| `Weakness` | Number | `1, 2` |

### Context: `CureDisease`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `can_apply_to_anything` | Boolean | `true` |
| `chance` | Number | `5%, 15%, 30%` |
| `disease` | Enum/String | `CommonCold, Pox, Ebola` |

### Context: `DamageIfDidntUseSpecificAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `Groom` |
| `damage` | Number | `2` |

### Context: `DamageNeighborTilesWhenCastSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `fire` | Block | `{ ... }` |
| `ice` | Block | `{ ... }` |
| `lightning` | Block | `{ ... }` |
| `triattack` | Block | `{ ... }` |

### Context: `DamageNeighborsAfterMove`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Enum/String | `X` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Electric ]` |
| `type` | Enum/String | `spell` |

### Context: `DamageNeighborsOnEndMove`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |
| `damage` | Number | `0` |
| `effects` | Block | `{ ... }` |
| `knockback` | Number | `1` |
| `type` | Enum/String | `status` |

### Context: `DamageReductionAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |
| `range` | Enum/String | `global` |
| `stacks` | Number | `1, 2` |

### Context: `DeathRattle`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `LastGasp2, LastGasp` |
| `pop_corpse` | Boolean | `false` |

### Context: `DelayedWind`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `distance` | Number | `2` |

### Context: `DelayedWindCone`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `distance` | Number | `10` |

### Context: `Diabetes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1` |
| `Confusion` | Number | `1` |

### Context: `DistanceBonusDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `min_range` | Number | `1, 3` |
| `stacks` | Number | `1` |

### Context: `EMP`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `spell_graphics_override` | Block | `{ ... }` |
| `status_explosion_override` | Enum/String | `WaterConduct` |

### Context: `Earth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Enum/String | `X` |

### Context: `Electric`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Stun` | Array | `[ 1 .1*X ]` |

### Context: `ElementalAttunement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Earth` | Block | `{ ... }` |
| `Electric` | Block | `{ ... }` |
| `Fire` | Block | `{ ... }` |
| `Grass` | Block | `{ ... }` |
| `Gravity` | Block | `{ ... }` |
| `Holy` | Block | `{ ... }` |
| `Ice` | Block | `{ ... }` |
| `Shadow` | Block | `{ ... }` |
| `Water` | Block | `{ ... }` |
| `Wind` | Block | `{ ... }` |

### Context: `ElementalManaCostReduction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Gravity, [ Fire Ice Electric Earth Wind Water Grass Holy Gravity ]` |
| `reduction` | Number | `1, 2` |

### Context: `Else`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` |
| `FactionConversion` | Number | `1` |
| `Fear` | Number | `1` |
| `Marked` | Number | `1` |
| `PermanentCharm` | Number | `1` |
| `TempSpeedUp` | Number | `4` |

### Context: `EnergyStorm`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cycle_start` | Number | `2` |
| `period` | Number | `3` |

### Context: `EscapeSequence`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomDistanceDisplace` | Number | `20` |
| `SafeExplosionIfHitSomething` | Number | `5, 10` |

### Context: `Eternal`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` |
| `TakeExtraTurn` | Number | `1` |
| `health_percent` | Number | `50%` |
| `stacks` | Number | `1` |

### Context: `ExtraStatusWhenDealingDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Ally` | Block | `{ ... }` |

### Context: `FindItemFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Enum/String | `.5` |
| `pool` | Enum/String | `pills` |

### Context: `Fire`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Enum/String | `X` |

### Context: `ForceMoveAway`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `free` | Boolean | `false` |

### Context: `ForceUseAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `DysenteryPoop, CrohnsPoop, TigerForm` |
| `chance` | Enum/String | `.2, 33%, .5` |

### Context: `FurnitureStats`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Appeal` | Number | `1` |
| `Comfort` | Number | `1` |
| `Stimulation` | Number | `1` |

### Context: `Grass`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Poison` | Enum/String | `X` |

### Context: `Gravity`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Weakness` | Enum/String | `X` |

### Context: `GravityWell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |
| `damage` | Number | `5, 0` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Gravity ]` |
| `type` | Enum/String | `status` |

### Context: `HealAlliesEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `exclude_self` | Boolean | `false` |
| `mana` | Number | `2, 3` |
| `stacks` | Number | `2, 3` |

### Context: `Holy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FlatLeech` | Enum/String | `X` |

### Context: `HolyDamageBlessing`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Burn` | Number | `2, 3` |
| `damage_multiplier` | Number | `2, 3` |

### Context: `Ice`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Slow` | Enum/String | `X` |

### Context: `InfiniteRebirth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `TempSpeedUp` | Number | `10` |
| `health` | Number | `1, 25%` |
| `playercat_health` | Number | `100%` |

### Context: `LateBloomer`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` |
| `stacks` | Number | `5, 3` |

### Context: `LightningRod`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Tech` | Number | `1` |

### Context: `LowHealthAllyDodgeChanceAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `50%` |
| `theshold` | Number | `5` |

### Context: `ManaCostReductionTagged`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `reduction` | Number | `1, 3, 50%` |
| `tag` | Enum/String | `musical, summon` |

### Context: `MegaMinions`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cycle_start` | Number | `3` |
| `stacks` | Number | `3` |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Poison` | Number | `3` |
| `SpreadDisease` | Block | `{ ... }` |
| `Weakness` | Number | `1` |
| `damage` | Number | `1, 0, 3` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Ice ], [ Fire ]` |

### Context: `MoveTowardsDamageSource`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `move_ability` | Enum/String | `move, TrampleMoveOne, TrampleMove` |
| `move_far` | Boolean | `false` |

### Context: `MoveWhenDamaged`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `weights` | Enum/String | `stay_far_always_move` |

### Context: `MovementReaction`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `weapon` |
| `enemies_only` | Boolean | `true` |

### Context: `NextBattleStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` |
| `FullHeal` | Number | `1` |

### Context: `ObjectOnHitCharacter`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `CharmedFlea` |
| `stacks` | Number | `1, 2` |

### Context: `PassiveAfterXKills`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |
| `stacks` | Number | `3` |

### Context: `PassiveAtFullHealth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ManaCostReduction` | Number | `2` |
| `TakeExtraDamage` | Number | `200%` |

### Context: `PassiveAtHealthThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal, equal` |
| `passives` | Block | `{ ... }` |
| `threshold` | Number | `1, 5` |

### Context: `PassiveAtInjuryThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `injury` | Enum/String | `spd` |
| `mode` | Enum/String | `greater_or_equal` |
| `passives` | Block | `{ ... }` |
| `threshold` | Number | `4` |

### Context: `PassiveAtStatThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal` |
| `passives` | Block | `{ ... }` |
| `threshold` | Block | `{ ... }` |

### Context: `PassiveGroup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `-2` |
| `CharismaUp` | Number | `5` |
| `IntelligenceUp` | Number | `5` |
| `SetDefaultFace` | Enum/String | `sad, happy` |
| `SpeedUp` | Number | `5` |

### Context: `PassiveIfAllArmorEmpty`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddSpellDamage` | Number | `1, 2` |
| `CounterAttack` | Enum/String | `attack` |
| `CritsApplyStatus` | Block | `{ ... }` |
| `ExtraMovePoints` | Number | `1` |
| `Flying` | Number | `1` |
| `ManaCostReduction` | Number | `1` |
| `StatusOnStanceSwitch` | Block | `{ ... }` |

### Context: `PassiveIfEmptyFace`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `40%, 25%` |
| `CritChanceUp` | Number | `10` |
| `DodgeChance` | Number | `15%, 10%` |
| `KineticSpikes` | Number | `1` |
| `StatusOnStanceSwitch` | Block | `{ ... }` |

### Context: `PassiveIfEmptyHead`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `40%, 25%` |
| `CritChanceUp` | Number | `10` |
| `DodgeChance` | Number | `15%, 10%` |
| `KineticSpikes` | Number | `1` |
| `StatusOnStanceSwitch` | Block | `{ ... }` |

### Context: `PassiveIfEmptyNeck`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `40%, 25%` |
| `CritChanceUp` | Number | `10` |
| `DodgeChance` | Number | `15%, 10%` |
| `KineticSpikes` | Number | `1` |
| `StatusOnStanceSwitch` | Block | `{ ... }` |

### Context: `PassiveLevelScaledStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Shield` | String | `"2*(X-1)"` |
| `SizeScalePercent` | String | `"sqrt(1.0+(.05*(X-1)))*100"` |
| `Trample` | Array | `[ 3, X-8 ]` |

### Context: `PassiveUntilCastSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealAlliesEachTurn` | Block | `{ ... }` |
| `StatusAlliesEachTurn` | Block | `{ ... }` |

### Context: `PassiveUntilGetKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HolyDamageBlessing` | Block | `{ ... }` |

### Context: `PassiveWhenAffectedByElement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `water` |
| `passives` | Block | `{ ... }` |

### Context: `PassiveWhenAtFullMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddMovement` | Number | `20` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `Brace` | Number | `2, 3` |
| `Flying` | Number | `1` |
| `ReplaceBasicMove` | Enum/String | `Teleport` |

### Context: `PassiveWhenTheAlpha`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | `1` |

### Context: `PassiveWhileInMonkMeleeStance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Number | `1, 2` |
| `HealthRegenUp` | Number | `2` |

### Context: `PassiveWhileInMonkRangedStance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddBonusRange` | Number | `1, 2` |
| `AddSpellDamage` | Number | `2` |
| `KineticSpikes` | Number | `2` |

### Context: `PassiveWhilePreviewingMonkRangedStance`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddBonusRange` | Number | `1, 2` |

### Context: `PassiveWhileWearingMetal`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AddElementsToWeapon` | Enum/String | `Electric` |

### Context: `RandomPassivePool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `PassiveGroup` | Block | `{ ... }` |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, -1` |
| `BleedThorns` | Number | `1` |
| `Bleed` | Number | `1` |
| `Blind` | Number | `1` |
| `Brace` | Number | `1` |
| `Bruise` | Number | `1` |
| `Burn` | Number | `1` |
| `Charge` | Number | `1` |
| `Charmed` | Number | `1` |
| `Confusion` | Number | `1` |
| `ConstitutionUp` | Number | `1` |
| `DiminishingHealthRegen` | Number | `1` |
| `DivineShield` | Number | `1` |
| `Fear` | Number | `1` |
| `Freeze` | Number | `1` |
| `Immobile` | Number | `1` |
| `KineticSpikes` | Number | `1` |
| `Madness` | Number | `1` |
| `MagicWeakness` | Number | `1` |
| `Marked` | Number | `1` |
| `MoveQuivered` | Number | `1` |
| `ObjectOnHitCharacter` | Enum/String | `BeefyCharmedLeech, CharmedLeech` |
| `Petrify` | Number | `1` |
| `Poison` | Number | `1` |
| `Quivered` | Number | `1` |
| `Reflect` | Number | `1` |
| `Shield` | Number | `1` |
| `Sleep` | Number | `1` |
| `Slow` | Number | `1` |
| `SpawnCoinAnywhere` | Number | `1` |
| `SpeedUp` | Number | `1` |
| `StatusGroup` | Block | `{ ... }` |
| `StrengthUp` | Number | `1` |
| `Stun` | Number | `1` |
| `Tarred` | Number | `1` |
| `Thorns` | Number | `1` |
| `Weakness` | Number | `1` |

### Context: `ReplaceBrain`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `brain` | Enum/String | `GenericBrain` |
| `decision_weights` | Enum/String | `default` |
| `move_weights` | Enum/String | `keep_distance` |

### Context: `RepressedMemoriesMetronome`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `pool` | Enum/String | `Jester, Psychic` |
| `stacks` | Number | `1` |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `effects` | Block | `{ ... }` |
| `knockback` | Number | `10` |

### Context: `Robot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `allow_energize_self` | Boolean | `true` |

### Context: `ScaledStatusOnBleedDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `2` |

### Context: `ScaledStatusOnLoseShield`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Thorns` | Number | `1` |

### Context: `ScaledStatusOnOverHealed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | `1` |

### Context: `ScaledStatusOnOverMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Cleanse` | Number | `0` |
| `RandomMagicMissile` | Number | `1` |

### Context: `ScaledStatusOnSpendMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RepressedMemoriesMetronome` | Block | `{ ... }` |

### Context: `SecurityBotProtect`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ability` | Enum/String | `attack` |
| `move` | Enum/String | `move, MoveThree` |

### Context: `SelfDamageWhenDealDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `1` |
| `type` | Enum/String | `status` |

### Context: `Shadow`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `crit_chance` | Enum/String | `.05*X` |

### Context: `SmiteEnemiesWhoKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `10` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Holy ]` |
| `type` | Enum/String | `spell` |

### Context: `SpawnCatCopyOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `object` | Enum/String | `PlayerCat_MiniMe, PlayerCat_MiniMiniMe` |
| `prevent_chain_tag` | Enum/String | `minime_clone` |

### Context: `SpawnEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `chance` | Number | `15%, .5, 50%` |
| `good` | Boolean | `false` |
| `number` | Number | `1` |
| `object` | Enum/String | `CharmedFlea, [ CharmedTumorousMaggot CharmedChargeyMaggot CharmedSwapp..., CharmedMaggot` |

### Context: `SpawnOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `number` | Number | `1, [ 2 3 ], 3` |
| `object` | Enum/String | `SmallRock, CharmedFlea, [ BuffFamiliarMaggot BuffFamiliarPooter BuffFamiliarFlea ...` |

### Context: `SpawnOnBattleStartRandomEmptyTile`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `number` | Array | `[ 2 3 ], 10, [ 1 2 ]` |
| `object` | Enum/String | `Coin, RandomPickup` |

### Context: `SpawnThingOnDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `consider_all_layers` | Boolean | `true` |
| `good` | Boolean | `false, true` |
| `object` | Enum/String | `Food, PoisonFood, CharmedLeech` |
| `spawn_on_death_hit` | Boolean | `false` |

### Context: `SpecialFriends`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` |
| `HealthGain` | Number | `8` |

### Context: `SpreadDisease`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `can_apply_to_anything` | Boolean | `true` |
| `chance` | Number | `100%, 25%, 50%` |
| `disease` | Enum/String | `Pox, CommonCold, Rabies` |

### Context: `StackingDodgeChanceOnTookDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `amount` | Number | `10%` |
| `cap` | Number | `50%` |

### Context: `StatsAtLowHealth`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `speed` | Number | `6` |
| `strength` | Number | `6` |
| `threshold` | Number | `5` |

### Context: `StatusAdjacentOnTheirTurnBegin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceMoveAway` | Block | `{ ... }` |

### Context: `StatusAfterCastSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `TempDamageUp` | Number | `1` |
| `TempSpellDamageUp` | Number | `1` |

### Context: `StatusAlliesEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomStatUp` | Number | `3` |
| `exclude_self` | Boolean | `false` |

### Context: `StatusAlliesOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `EquipTemporaryItem` | Enum/String | `SleepDart2, SleepDart` |

### Context: `StatusAlliesOnDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Freeze` | Number | `1` |
| `FullHeal` | Number | `1` |
| `HealAndOverhealToShield` | Number | `12, 20` |
| `Reanimate` | Number | `33%, 100%` |
| `TakeExtraTurn` | Number | `1` |
| `triggers_limit` | Number | `1` |

### Context: `StatusAlliesOnGainCoins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthGain` | Number | `1` |
| `LuckUp` | Number | `1` |
| `scaled` | Boolean | `true` |

### Context: `StatusAlliesOnKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `DamageUp` | Number | `1` |
| `HealthGain` | Number | `5` |

### Context: `StatusAlliesOnSpendMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ManaGain` | Number | `1` |

### Context: `StatusAlliesScaledByCursedOnDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `LuckUp` | Number | `1` |

### Context: `StatusAllyWhenAllySpendsMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `threshold` | Number | `7` |

### Context: `StatusAnyCatAllyWhoKills`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AlphaCat` | Number | `1` |

### Context: `StatusDamagers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Fear` | Array | `[ 1 .25 ]` |
| `LuckUp` | Number | `-1` |

### Context: `StatusEachTurnBegin`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_BadRoll` | Block | `{ ... }` |
| `Conditional_GoodRoll` | Block | `{ ... }` |
| `Fear` | Array | `[ 1 .15 ]` |
| `FillMana` | Array | `[ 1 .10 ], [ 1 .25 ]` |
| `ForceUseAbility` | Block | `{ ... }` |
| `IntelligenceUp` | Number | `1` |
| `RandomStatUp` | Number | `2, 3` |

### Context: `StatusEachTurnEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `EmptyMana` | Number | `1` |
| `ForceUseAbility` | Enum/String | `MiniFart, Rest, { ... }` |
| `IntelligenceUp` | Number | `1` |
| `KineticSpikes` | Number | `1` |
| `NonStackingDivineShield` | Number | `1` |
| `ObjectOnHitCharacter` | Block | `{ ... }` |
| `PermanentMadness` | Number | `1` |
| `RangeUp` | Number | `1` |
| `SpeedUp` | Number | `1, -2` |
| `StrengthUp` | Number | `1` |
| `UseAbility_Madness` | Enum/String | `weapon` |

### Context: `StatusEachTurnEndForEachTurn`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `2, 4` |

### Context: `StatusEachTurnEndPerEnemyKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ObjectOnHitCharacter` | Block | `{ ... }` |

### Context: `StatusEnemiesOnDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1, -2` |
| `Freeze` | Number | `2` |

### Context: `StatusEveryXSpellCasts`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `ReduceManaCost` | Number | `1` |
| `RepairWeaponCondition` | Number | `1` |
| `RepairWeapon` | Number | `1` |
| `SpellDamageUp` | Number | `1` |
| `stacks` | Number | `6, 3` |

### Context: `StatusEveryXTurnBegins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `1` |
| `turns` | Number | `2, 3` |

### Context: `StatusGroup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DexterityUp` | Number | `2` |
| `LuckUp` | Number | `2` |
| `SpawnCoinAnywhere` | Number | `1` |
| `SpeedUp` | Number | `2` |

### Context: `StatusIfBattleAlreadyBegan`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` |

### Context: `StatusIfUnusedMovePoints`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Brace` | Number | `1` |
| `ConstitutionUp` | Number | `2` |
| `HealthGain` | Number | `8` |
| `ManaGain` | Number | `5` |
| `MoveQuivered` | Number | `2` |
| `Shield` | Number | `2` |

### Context: `StatusKilledCharacters`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AutoReanimate` | Number | `100%, 50%` |
| `Conditional_Ally` | Block | `{ ... }` |

### Context: `StatusKillers`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_Boss` | Block | `{ ... }` |
| `Conditional_NotBoss` | Block | `{ ... }` |

### Context: `StatusOnAllyCatDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` |
| `FillMana` | Number | `1` |
| `HealthGain` | Number | `8` |
| `PercentHeal` | Number | `50` |
| `TakeExtraTurn` | Number | `1` |

### Context: `StatusOnAnyDeath`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `LuckUp` | Number | `1` |

### Context: `StatusOnBattleEnd`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CureDisease` | Block | `{ ... }` |
| `FindItemFromPool` | Enum/String | `consumables, chapter, { ... }` |
| `NextBattleStatus` | Block | `{ ... }` |
| `PermanentConstitution` | Number | `-1` |
| `PermanentIntelligence` | Number | `-1` |
| `PermanentSpeed` | Number | `-1` |
| `PermanentStrength` | Number | `2` |
| `RandomMutation` | Number | `1` |
| `RandomPermanentStat` | Number | `1, -3, 3` |
| `even_if_dead` | Boolean | `true` |

### Context: `StatusOnBattleEndIfKillThresholdMet`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `kills` | Number | `3` |
| `statuses` | Block | `{ ... }` |

### Context: `StatusOnBattleStart`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FullHeal` | Number | `1` |
| `Sleep` | Number | `1` |

### Context: `StatusOnBreakItem`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Shield` | Number | `3` |
| `Thorns` | Number | `1, 2` |

### Context: `StatusOnCastSpell`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Charge` | Number | `1, 2` |
| `CurrentWeaponDamageUp` | Number | `1` |
| `HealthGain` | Number | `1` |

### Context: `StatusOnCollectPickup`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Tech` | Number | `1` |

### Context: `StatusOnCrit`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CritChanceUp` | Number | `5` |
| `DamageUp` | Number | `1` |
| `LuckUp` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `Shield` | Number | `2, 3` |

### Context: `StatusOnDealtDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `TempDexterityUp` | Number | `2` |
| `TempLuckUp` | Number | `2` |
| `TempStrengthUp` | Number | `1, 2` |

### Context: `StatusOnDealtDamageThreshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `RefreshMovePoints` | Number | `1` |
| `Shield` | Number | `2` |
| `count_overkill` | Boolean | `true` |
| `ignore_during_movement` | Boolean | `true` |
| `threshold` | Number | `10` |

### Context: `StatusOnEatFood`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Cleanse` | Number | `0` |
| `IntelligenceUp` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `StrengthUp` | Number | `1` |

### Context: `StatusOnEatPill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` |

### Context: `StatusOnEndMove`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceAttack` | Number | `1` |

### Context: `StatusOnGainCoins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `1` |
| `RandomStatusFromPool` | Block | `{ ... }` |

### Context: `StatusOnGainShield`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Temporary` | Block | `{ ... }` |

### Context: `StatusOnHeal`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `RandomStatUp` | Number | `1` |
| `SpeedUp` | Number | `2, 4` |

### Context: `StatusOnHealed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ObjectOnHitCharacter` | Enum/String | `CharmedLeech` |
| `RandomStatusFromPool` | Block | `{ ... }` |
| `Thorns` | Number | `1` |

### Context: `StatusOnKill`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `Conditional_FirstApplicationThisTurn` | Block | `{ ... }` |
| `DamageUp` | Number | `1` |
| `EquipPermanentItem` | Enum/String | `BoneClub` |
| `HealthGain` | Number | `5` |
| `LuckUp` | Number | `2` |
| `RandomStatUp` | Number | `1` |
| `RefreshActPoints` | Number | `1` |
| `RefreshMovePoints` | Number | `1` |
| `SpeedUp` | Number | `2` |
| `Stealth` | Number | `1` |
| `StrengthUp` | Number | `2` |
| `TakeBonusTurnWithStatus` | Block | `{ ... }` |

### Context: `StatusOnKillEnemy`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `1` |
| `HealthGain` | Number | `2` |
| `ManaGain` | Number | `3` |
| `RefreshMovePoints` | Number | `1` |

### Context: `StatusOnLoseShield`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Thorns` | Number | `1` |

### Context: `StatusOnOverHealed`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Number | `1` |
| `ForceUseAbility_NonStack` | Enum/String | `Indigestion_Fart, Indigestion_Fart2` |
| `SpawnScaledRotFly` | Number | `0` |
| `StrengthUp` | Number | `1` |

### Context: `StatusOnOverMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `1` |
| `IntelligenceUp` | Number | `1` |
| `SpellDamageUp` | Number | `1` |

### Context: `StatusOnPickupCoins`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DexterityUp` | Number | `1` |
| `RefreshMovePoints` | Number | `1` |
| `SpeedUp` | Number | `1` |

### Context: `StatusOnPopCorpse`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthGain` | Number | `2, 8` |

### Context: `StatusOnStanceSwitch`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `RapidFlowSpin, RapidFlowSpin2` |
| `NextBasicAttackCritsThisTurn` | Number | `1` |
| `PartialCleanse` | Number | `1` |
| `RandomMagicMissile` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `Shield` | Number | `2, 3` |

### Context: `StatusOnTakeHealthDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `PermanentConstitution` | Number | `-1` |

### Context: `StatusOnTookDamage`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_HasStatus` | Block | `{ ... }` |
| `ConstitutionUp` | Number | `1, -1` |
| `Craft` | Block | `{ ... }` |
| `DamageUp` | Number | `1, 2` |
| `DiminishingHealthRegen` | Number | `1` |
| `Else` | Block | `{ ... }` |
| `IntelligenceUp` | Number | `-1, -2` |
| `MovementUp` | Number | `1` |
| `RandomInjury` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `RandomStatusFromPool` | Block | `{ ... }` |
| `Shield` | Number | `1, 2` |
| `SpeedUp` | Number | `1, 2` |
| `StrengthUp` | Number | `1, -1` |
| `TempDamageUp` | Number | `1, 2` |
| `TempMovement` | Number | `1` |
| `Temporary` | Block | `{ ... }` |
| `Thorns` | Number | `1` |

### Context: `StatusOnTookDamageFromAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DiminishingHealthRegen` | Number | `1, 2` |
| `Shield` | Number | `2` |

### Context: `StatusOnTookDamageFromEnemyAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `MoveQuivered` | Number | `1` |
| `Quivered` | Number | `1` |

### Context: `StatusOnTriggerTrap`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DexterityUp` | Number | `2` |
| `Quivered` | Number | `1` |

### Context: `StatusOnTurnEndIfCastNSpells`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DoubleCastSpell` | Number | `1, 2` |
| `MoveQuivered` | Number | `1` |
| `Quivered` | Number | `1` |
| `spells` | Number | `1, 2` |

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ManaGain` | Number | `7` |
| `type` | Enum/String | `attack` |

### Context: `StatusOnTurnEndIfManaExact`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FreeSpell` | Number | `1` |
| `MoveQuivered` | Number | `1` |
| `Quivered` | Number | `1` |
| `SpellDamageUp` | Number | `1` |
| `mana` | Number | `2, 0` |

### Context: `StatusOnTurnEndIfManaOrHealthExact`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `DivineShield` | Number | `1` |
| `HealthGain` | Number | `5` |
| `IntelligenceUp` | Number | `1` |
| `KineticSpikes` | Number | `1` |
| `Shield` | Number | `5` |
| `SpellDamageUp` | Number | `1` |
| `Temporary` | Block | `{ ... }` |
| `mana` | Number | `5, 4` |

### Context: `StatusOnUseAbilityWithTag`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Conditional_FirstApplicationThisTurn` | Block | `{ ... }` |
| `DamageUp` | Number | `1` |
| `HealthGain` | Number | `1` |
| `RandomStatUp` | Number | `1` |
| `RefreshActPoints` | Number | `1` |
| `exclude_basicattack` | Boolean | `true` |
| `tag` | Enum/String | `shapeshift, musical` |

### Context: `StatusOnUseBasicAttack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `FlippedFacingForceAttack` | Number | `1` |

### Context: `StatusOnUseElementAbility`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `SpeedUp` | Number | `1, 2` |
| `element` | Enum/String | `Gravity` |

### Context: `StatusPerInjury`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Shield` | Number | `3` |
| `StrengthUp` | Number | `1` |
| `cap` | Number | `10` |
| `injury` | Enum/String | `int` |

### Context: `StatusThingsKnockedBack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Drag` | Number | `1, 2` |

### Context: `StatusWhenAllySpendsMana`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ManaGain` | Number | `2` |
| `OneUseSpellDamageUp` | Number | `2` |

### Context: `StrengthInNumbersAura`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `count_self` | Boolean | `true` |
| `stacks` | Number | `1` |

### Context: `Study`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `marked` | Number | `2` |
| `stacks` | Number | `1` |

### Context: `TaggedPickupEffectReplacement`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HealthGain` | Enum/String | `2*X, 3*X` |
| `tag` | Enum/String | `scrap, money` |

### Context: `TakeBonusTurnWithStatus`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Madness` | Number | `1` |

### Context: `Temporary`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `expires_on_begin_turn` | Boolean | `true` |
| `expires_on_end_turn` | Boolean | `true` |
| `stacks` | Number | `5, 1, 2` |
| `status` | Enum/String | `Uncontrollable, Brace, Thorns` |
| `turns` | Number | `1` |

### Context: `TheHunger`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Madness` | Number | `1` |

### Context: `TileDamageMultiplier`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `ally_multiplier` | Number | `0` |
| `multiplier` | Number | `2` |

### Context: `TourettesMeows`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cooldown` | Array | `[ 8 15 ]` |
| `pool` | Array | `[ Hit Hiss Normal ]` |

### Context: `TowerDefense`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `1, 2` |
| `range` | Number | `1, 2` |

### Context: `Water`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AOEPuddle` | Enum/String | `X-1` |

### Context: `Wind`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `knockback` | Enum/String | `X` |

### Context: `effects`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `Bleed` | Number | `1` |
| `Bruise` | Number | `1` |
| `Burn` | Number | `1` |
| `Charmed` | Array | `[ 1, .40 ], [ 1, .25 ]` |
| `Fear` | Number | `1` |
| `Freeze` | Array | `[ 1, .15 ], [ 1, .05 ]` |
| `Immobile` | Number | `1` |
| `Leeches` | Number | `1` |
| `Madness` | Number | `1` |
| `Marked` | Number | `1` |
| `Petrify` | Array | `[ 1, .2 ], [ 1, .1 ]` |
| `Poison` | Number | `1` |
| `Slow` | Number | `2` |
| `SpreadDisease` | Block | `{ ... }` |
| `Stun` | Number | `1, [ 1, .05*X ], [ 1, .05 ]` |
| `VisualFXTile` | Enum/String | `WaterConduct, BurnTrigger, IcePoof` |
| `Weakness` | Number | `1` |

### Context: `empty_armor_scaled_stats`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cha` | Number | `1` |
| `int` | Number | `1` |
| `spd` | Number | `1, 2` |

### Context: `fire`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `3` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Fire ]` |
| `type` | Enum/String | `spell` |

### Context: `ice`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `3` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Ice ]` |
| `type` | Enum/String | `spell` |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `MagicWeakness` | Number | `1` |
| `Weakness` | Number | `1` |

### Context: `lightning`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `3` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Electric ]` |
| `type` | Enum/String | `spell` |

### Context: `lock_item_slot`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `frame` | Number | `11, 17, 16` |
| `slot` | Enum/String | `face, neck, trinket` |

### Context: `on_break`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | `5, 10` |

### Context: `on_throw`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `HitExplosion` | Number | `5, 10` |

### Context: `passives`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AbilityChargeRefundChance` | Block | `{ ... }` |
| `AbilityOnBattleStart` | Enum/String | `Heathens, neck_ChefsApron, MegaFart` |
| `AbilityReaction` | Enum/String | `PissYourself, Gassy_AssBlast, Gassy_AssBlast2` |
| `AbilityWhenTaggedCharacterMovesNear` | Block | `{ ... }` |
| `AbsorbManaAura` | Number | `1` |
| `AddAllyNeighborsToAbilityRange` | Number | `1` |
| `AddAllyNeighborsToAttackRange` | Number | `1` |
| `AddBonusMeleeRange` | Number | `1, 2, 10` |
| `AddBonusRange` | Number | `1, 2, 10` |
| `AddChaScalingSpellDamage` | Number | `3` |
| `AddCorpseHealth` | Number | `-999999, 96, 3` |
| `AddCritMultiplier` | Number | `100%, 25%, 50%` |
| `AddDamageToBasicAttack` | Number | `1, 2, 4` |
| `AddDamageToElementDamage` | Block | `{ ... }` |
| `AddElementsToBasicAttack` | Enum/String | `Ice, Fire, Electric` |
| `AddHiddenTag` | Enum/String | `bowling_ball` |
| `AddInitiative` | Number | `999, -100` |
| `AddKnockbackDamage` | Number | `1, 2, 3` |
| `AddKnockbackToEverything` | Number | `1` |
| `AddLevelUpRerolls` | Number | `1, 2, 3` |
| `AddLevelUpStatMultiplier` | Number | `1` |
| `AddManaRegen` | Number | `1, 7, 5` |
| `AddMovement` | Number | `1, 2, 4` |
| `AddPassiveToSpawnedRocks` | Block | `{ ... }` |
| `AddPassivesToCharmed` | Block | `{ ... }` |
| `AddPassivesToMinions` | Block | `{ ... }` |
| `AddPassivesToSummonAbilityMinions` | Block | `{ ... }` |
| `AddRangedCritChance` | Number | `25%` |
| `AddSelfStatusToBasicAttack` | Block | `{ ... }` |
| `AddSelfStatusToWeapons` | Block | `{ ... }` |
| `AddSpellDamage` | Number | `1` |
| `AddStartingMana` | Number | `5, 20` |
| `AddStatusToAllDamageAbilities` | Block | `{ ... }` |
| `AddStatusToAllDamage` | Block | `{ ... }` |
| `AddStatusToBasicAttackWithCooldown` | Block | `{ ... }` |
| `AddStatusToBasicAttack` | Block | `{ ... }` |
| `AddStatusToBasicMeleeAttack` | Block | `{ ... }` |
| `AddStatusToElementAbilities` | Block | `{ ... }` |
| `AddStatusToElementDamage` | Block | `{ ... }` |
| `AddStatusToExplosions` | Block | `{ ... }` |
| `AddStatusToFirstBasicAttack` | Block | `{ ... }` |
| `AddStatusToKnockbackDamage` | Block | `{ ... }` |
| `AddStatusToMeleeDamage` | Block | `{ ... }` |
| `AddStatusToReceivedDamage_ExcludeStatuses` | Block | `{ ... }` |
| `AddStatusToSpells` | Block | `{ ... }` |
| `AddStatusToTrampleDamage` | Block | `{ ... }` |
| `AddStatusToWeapons` | Block | `{ ... }` |
| `AddStatusesIfPersistentWeatherElement` | Block | `{ ... }` |
| `AddStatusesToReceivedElementalDamage` | Block | `{ ... }` |
| `AddTag` | Enum/String | `rock` |
| `AddTemporaryEffectsToBasicAttack` | Block | `{ ... }` |
| `AddTemporaryEffectsToEquipment` | Block | `{ ... }` |
| `AddUnfilledMaxHealth` | Number | `50, 20` |
| `AddWeaponScaling` | Number | `1` |
| `AfterImage` | Enum/String | `PlayerCat_ThiefShade2, PlayerCat_ThiefShade` |
| `AllDamageCrits` | Number | `1` |
| `AllStatsUp` | Number | `2, -1, -2` |
| `AlliesAvoidTraps` | Number | `1` |
| `AllowPassTurn` | Number | `1, 0` |
| `AllyBonusAbilityAura` | Enum/String | `NubbyToss, { ... }` |
| `AllyChainKnockback` | Number | `1` |
| `AllyDamageReaction` | Enum/String | `attack` |
| `AllyDamageReduction` | Number | `0` |
| `AllyHealthRegenAura` | Block | `{ ... }` |
| `AllyManaRegenAura` | Block | `{ ... }` |
| `AllyMoveAbilityAura` | Enum/String | `CatapultJump2, CatapultJump` |
| `AllyMultiplyKnockbackDamage` | Number | `2` |
| `AllyMultiplyKnockbackDistance` | Number | `2` |
| `AllyUncappedHPAura` | Number | `1` |
| `AlphaCat` | Number | `1` |
| `AlphaTurns` | Number | `1, -1` |
| `AlternateCraftingPools` | Block | `{ ... }` |
| `AmplifyKnockback` | Number | `2, 10` |
| `AmplifyNegativeStatus` | Number | `1` |
| `AmplifyPositiveStatus` | Number | `1, 2` |
| `AmplifyStatus` | Enum/String | `Burn, { ... }, Rot` |
| `ApplyStatusesToRandomEnemiesEachTurn` | Block | `{ ... }` |
| `ArmorDodgeChance` | Number | `10%` |
| `Autism` | Block | `{ ... }` |
| `AutoCritLowDamage` | Number | `2, 3` |
| `AutoEquipConsumables` | Number | `1` |
| `AutocastEachRound` | Block | `{ ... }` |
| `AutocastEachTurnBegin` | Enum/String | `MindCrack_EldritchVisage, MindCrack_EldritchVisage2, { ... }` |
| `AutocastEachTurn` | Enum/String | `DarkOneStrike, ViolentOutburst` |
| `BackstabCritChance` | Number | `1` |
| `BackstabImmunity` | Number | `1` |
| `BackstabWeakness` | Number | `0.75` |
| `BasicAttackAOEBonus` | Number | `1, 2` |
| `BasicAttackCritChance` | Number | `100%` |
| `BasicAttackDamageMultiplier` | Number | `33.333334%, 0, 50%` |
| `BasicAttackStatusCarefulness` | Number | `1` |
| `BasicAttackStatusSwap` | Array | `[ TempDamageUp DamageUp ]` |
| `BlacklistPickupType` | Enum/String | `food` |
| `BlastResistance` | Number | `2, 4, 3` |
| `BleedThorns` | Number | `2` |
| `Bleed` | Number | `1, 3` |
| `BonusAbility` | Enum/String | `Bloodzerk, FeralMelee, Groom` |
| `BonusFoodEachBattle` | Number | `2, 20` |
| `BonusHealthRegenBasedOnDex` | Number | `5` |
| `BonusRangeBasedOnDex` | Number | `5` |
| `BoobyTrapItems` | Block | `{ ... }` |
| `BoostAllyStatsOnDeath` | Number | `1, 2` |
| `BoostDamageAura` | Number | `1` |
| `BoostDamageGlobalAura` | Number | `1` |
| `BoostHeals` | Number | `1, 2, -2` |
| `BoostRangeAura` | Number | `1` |
| `BoostRangeGlobalAura` | Number | `1` |
| `BoostWeaponDamage` | Number | `2, 1, 5` |
| `BouncyProjectiles` | Block | `{ ... }` |
| `BraceForEachNeighboringEnemy` | Number | `1, 2` |
| `Brace` | Number | `1, 2, 3` |
| `Bruise` | Number | `1, 2` |
| `BuffImmunity` | Number | `1` |
| `Burn` | Number | `1` |
| `CCImmunity` | Number | `1` |
| `CanRemoveCursedItems` | Number | `1` |
| `CantDodge` | Number | `1` |
| `CapDamageFromAllies` | Number | `1` |
| `CapMovementAbilityRange` | Number | `1` |
| `CapTechSpent` | Number | `0` |
| `CatAPultAnimation` | Block | `{ ... }` |
| `CatchProjectiles` | Block | `{ ... }` |
| `ChainKnockback` | Number | `1` |
| `ChanceToBackflip` | Block | `{ ... }` |
| `ChanceToBlockAndCounter` | Number | `33%, 15%` |
| `ChanceToRevive` | Number | `25, { ... }` |
| `ChangeTauntPriority` | Number | `-1` |
| `CharmAllFlies` | Number | `1` |
| `ClassManaCostReduction` | Block | `{ ... }` |
| `CobraReflex` | Enum/String | `BasicMonkMelee` |
| `CoinsAddDamage` | Number | `1, 2` |
| `CollectPickupsOnBattleEnd` | Number | `1, { ... }` |
| `ConductorManaRegen` | Number | `2` |
| `Conductor` | Number | `2` |
| `ConfusionEffectOnTaggedAbilities` | Enum/String | `consumable` |
| `ConjureCastSpellsForAllies` | Number | `1, 2` |
| `ConsumableEffectsMultiplierBonus` | Number | `1` |
| `ConsumablesInfiniteRange` | Number | `1` |
| `ConsumablesMeleeRange` | Number | `1` |
| `CounterAttack` | Enum/String | `ReflexPunchJab2, ReflexPunchJab` |
| `CritChanceUp` | Number | `25, 5, 10` |
| `CritsApplyStatus` | Block | `{ ... }` |
| `DamageEnemiesOnHeal` | Number | `1, 2` |
| `DamageEnemiesOnKill` | Number | `1, 2` |
| `DamageIfDidntUseSpecificAbility` | Block | `{ ... }` |
| `DamageNeighborTilesWhenCastSpell` | Block | `{ ... }` |
| `DamageNeighborsAfterMove` | Block | `{ ... }` |
| `DamageNeighborsOnEndMove` | Block | `{ ... }` |
| `DamageReductionAura` | Block | `{ ... }` |
| `DamageUp` | Number | `1, 4, 3` |
| `DeathChill` | Number | `1` |
| `DeathRattle` | Block | `{ ... }, BoomerCatExplode` |
| `DebuffImmunity` | Number | `1` |
| `DejaVu` | Number | `10%` |
| `DepressionAura` | Number | `2` |
| `Diabetes` | Block | `{ ... }` |
| `DirtyClaws` | Number | `1` |
| `DisableAbilitiesWithTag` | Enum/String | `meat` |
| `DisableAbilities` | Enum/String | `all_items` |
| `DodgeChance` | Number | `15%, 25%, 10%` |
| `Doomed` | Number | `3` |
| `DoubleCastWeapons` | Number | `1, 2` |
| `DukeOfFlies` | Number | `1` |
| `Dyslexia` | Array | `[ 6 9 ], [ 3 5 ]` |
| `EMP` | Block | `{ ... }` |
| `EachSpellFreeAtFullMana` | Number | `1` |
| `ElementImmune` | Enum/String | `Ice, Fire, Electric` |
| `ElementalAttunement` | Block | `{ ... }` |
| `ElementalManaCostReduction` | Block | `{ ... }` |
| `Empath` | Number | `100%, 50%` |
| `EnemiesGetPickupsKnockedOut` | Number | `1, 2` |
| `EnergyStorm` | Number | `3, { ... }` |
| `EquipRandomTemporaryItemFromPool` | Enum/String | `weapons` |
| `EquipTemporaryItem` | Enum/String | `FoodBig, FoodMedium, ButcherHook_Temporary` |
| `EquipmentPassiveMultiplierBonus` | Number | `1` |
| `EquipmentSetBonusBonus` | Number | `1, 2` |
| `EscapeSequence` | Block | `{ ... }` |
| `Eternal` | Block | `{ ... }` |
| `ExhaustionRoundChange` | Number | `3` |
| `ExplodeOverkilledEnemies` | Number | `1, 2` |
| `ExplosionImmunity` | Number | `1` |
| `ExtraBasicAttacks` | Number | `1, 2` |
| `ExtraBasicMoves_Status` | Number | `1` |
| `ExtraInjuryOnDeath` | Number | `1` |
| `ExtraMovePoints` | Number | `1` |
| `ExtraStatusWhenDealingDamage` | Block | `{ ... }` |
| `ExtraTrinketUses` | Number | `1` |
| `ExtraWeaponAttacks` | Number | `1, 2` |
| `FaceArmorPassiveMultiplierBonus` | Number | `2` |
| `FaceShield` | Number | `0` |
| `FamiliarSecondaryDamageImmunity` | Number | `1` |
| `FlowerPowerAuraBrace` | Number | `1` |
| `FlowerPowerAuraStrength` | Number | `1` |
| `FlowersOnEndTurn` | Number | `4, 3` |
| `FlyDamageIncrease` | Number | `1, 4` |
| `Flying` | Number | `1` |
| `FollowUp` | Enum/String | `FollowUpDash, FollowUpDash2` |
| `ForceSpecificInjury` | Enum/String | `cha, lck, int` |
| `ForceUseAbility` | Enum/String | `MockingbirdForm` |
| `FreePathfindElement` | Enum/String | `Water, Grass` |
| `FreeSpellsAtFullMana` | Number | `1` |
| `FreezePiercing` | Number | `1` |
| `FrontstabBasicAttackCritChance` | Number | `100%` |
| `FrontstabCritChance` | Number | `100%` |
| `FullHeal` | Number | `1` |
| `FullHealthAllStatsUp` | Number | `1` |
| `FullHealthCritChance` | Number | `100` |
| `FullHealthManaRegen` | Number | `5` |
| `FullPower` | Number | `3` |
| `FurnitureStats` | Block | `{ ... }` |
| `GainExtraShield` | Number | `2` |
| `GrassTileHealing` | Number | `1` |
| `GravityWell` | Block | `{ ... }` |
| `HPGainBlock` | Number | `1` |
| `HeadArmorPassiveMultiplierBonus` | Number | `1, 2` |
| `HealAtStart` | Number | `100%` |
| `HealDamagesEnemies` | Number | `1` |
| `HealingAura` | Number | `1` |
| `HealsAlsoRegenMana` | Number | `2, 50%` |
| `HealsCanRevive` | Number | `1, 3` |
| `HealthRegenUp` | Number | `1, 2, 3` |
| `HolyDamageMultiplierBonus` | Number | `1` |
| `HolyShieldTransferToTaggedMinions` | Enum/String | `any, crow` |
| `HouseFoodRequirementMultiplier` | Number | `0` |
| `Hypomania` | Number | `3` |
| `IgnoreTiles` | Number | `1` |
| `ImmortalLeeches` | Number | `1` |
| `IncreaseExplosionDamage` | Number | `2, 4, 3` |
| `IncreaseExplosionSize` | Number | `2` |
| `IncreaseHealingSpellRange` | Number | `2` |
| `IncreaseItemUsesOnEquip` | Number | `1` |
| `IncreaseSpellRange` | Number | `5, 10` |
| `InfiniteRebirth` | Block | `{ ... }` |
| `InjuryImmunity` | Number | `1` |
| `InnateElement` | Enum/String | `Ice, Fire, Electric` |
| `InvertBrainFaction` | Number | `1` |
| `KillsHeal` | Number | `5, 50%` |
| `KillsToMeat` | Enum/String | `Food` |
| `KnockbackImmunity` | Number | `1` |
| `LateBloomer` | Block | `{ ... }` |
| `LevelUpClassOverride` | Enum/String | `Colorless, Jester` |
| `LightningAspectCharge` | Number | `1, 0` |
| `LightningRod` | Block | `{ ... }` |
| `LimitDamage` | Number | `1` |
| `LimitHeal` | Number | `1` |
| `LimitSelfKnockbackDamage` | Number | `1` |
| `LimitedTileTrail` | Enum/String | `FlowerTile` |
| `LineOfSightTrueSightAura` | Number | `0, .5` |
| `LobbedHook` | Number | `1, 2` |
| `LowHealthAllyDodgeChanceAura` | Block | `{ ... }` |
| `Madness` | Number | `1` |
| `MakeBasicAttackPassThroughThings` | Number | `1` |
| `MakeSpellsRequireCharge` | Number | `1` |
| `ManaCostReductionTagged` | Block | `{ ... }` |
| `ManaCostReduction` | Number | `25%` |
| `ManaRegenMultiplierIfManaEmpty` | Number | `2` |
| `MaxAccuracy` | Number | `1` |
| `MaxStartingMana` | Number | `1` |
| `MegaMinions` | Number | `3, { ... }` |
| `MeleeRevengeDamage` | Block | `{ ... }` |
| `MetalDetector` | Number | `5, 10` |
| `Metal` | Number | `1` |
| `MinimumTech` | Number | `1` |
| `MissChance` | Number | `5, 15, 10` |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | Enum/String | `EatShit, Cannibalize` |
| `MoveAwayFromDamageSource` | Enum/String | `MoveOne` |
| `MoveQuivered` | Number | `2` |
| `MoveRandomly` | Number | `1` |
| `MoveSpeedMultiplier` | Enum/String | `.5` |
| `MoveTowardsDamageSource` | Block | `{ ... }` |
| `MoveWhenDamaged` | Block | `{ ... }` |
| `MovementReaction` | Block | `{ ... }` |
| `MulticlassLevelUp` | Enum/String | `Hunter, Fighter, Mage` |
| `NeckArmorPassiveMultiplierBonus` | Number | `2` |
| `NoManaRegen` | Number | `1` |
| `NoReflection` | Number | `1` |
| `NubbyTossPriority` | Number | `1` |
| `NumbingLeeches` | Number | `3` |
| `OverhealGainsBothShield` | Number | `1, 2` |
| `OverrideBasicAttack` | Enum/String | `BasicMelee, GerdShot` |
| `OverrideMaxHealth` | Number | `1` |
| `OverrideMaxMana` | Number | `1` |
| `OverridePalette` | Number | `87` |
| `Paranoia` | Enum/String | `ParanoiaBasicMelee` |
| `ParasitesArentCursed` | Number | `1` |
| `PassiveAfterXKills` | Block | `{ ... }` |
| `PassiveAtFullHealth` | Block | `{ ... }` |
| `PassiveAtHealthThreshold` | Block | `{ ... }` |
| `PassiveAtInjuryThreshold` | Block | `{ ... }` |
| `PassiveAtStatThreshold` | Block | `{ ... }` |
| `PassiveIfAllArmorEmpty` | Block | `{ ... }` |
| `PassiveIfEmptyFace` | Block | `{ ... }` |
| `PassiveIfEmptyHead` | Block | `{ ... }` |
| `PassiveIfEmptyNeck` | Block | `{ ... }` |
| `PassiveLevelScaledStatus` | Block | `{ ... }` |
| `PassiveLevelUpAtCombatEnd` | Number | `1` |
| `PassiveUntilCastSpell` | Block | `{ ... }` |
| `PassiveUntilGetKill` | Block | `{ ... }` |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` |
| `PassiveWhenAtFullMana` | Block | `{ ... }` |
| `PassiveWhenTheAlpha` | Block | `{ ... }` |
| `PassiveWhileInMonkMeleeStance` | Block | `{ ... }` |
| `PassiveWhileInMonkRangedStance` | Block | `{ ... }` |
| `PassiveWhilePreviewingMonkRangedStance` | Block | `{ ... }` |
| `PassiveWhileWearingMetal` | Block | `{ ... }` |
| `PermanentImmobile` | Number | `1` |
| `PermanentItems` | Number | `1, 2` |
| `PermanentKitten` | Number | `1` |
| `PermanentMadness` | Number | `1` |
| `Phasing` | Number | `1` |
| `PoisonMultiplier` | Number | `2` |
| `PoisonThorns` | Number | `1, 2` |
| `Poison` | Number | `1` |
| `PoopWhenHit` | Enum/String | `Poop` |
| `ProtectTargetedAllies` | Enum/String | `SwapPositions_WideLoad, SwapPositions_WideLoad2` |
| `Quiver` | Number | `1, 2` |
| `Quivered` | Number | `5, 1, 2` |
| `RandomPassivePool` | Block | `{ ... }` |
| `RangedTrueShot` | Number | `1` |
| `RealTimePressure_OneUnit` | Number | `5` |
| `ReceivedStatusReplacement` | Array | `[ Sleep SleepParalysis ]` |
| `RefreshMoveOnWeaponConnect` | Number | `1` |
| `RemoveLineOfSightRestrictions` | Number | `1` |
| `RemoveOncePerFightRestriction` | Number | `1` |
| `ReplaceBasicAttackWhenCastable` | Enum/String | `Shank, BasicSuplex, Shank2` |
| `ReplaceBasicAttackWhenDead` | Enum/String | `Haunt` |
| `ReplaceBasicAttack` | Enum/String | `BasicDruidAbilityVersatile, BasicButcherMeleeWideSpin, BasicButcherMeleeWideDoubleSpin` |
| `ReplaceBasicMove` | Enum/String | `ToadJump_BasicMove, BellyFlop_BasicMove, BasicDashAttackMove` |
| `ReplaceBrain` | Block | `{ ... }` |
| `ReplaceSpawnedObjects` | Array | `[ Crow2 Crow3 ], [ Crow Crow2 ], [ Crow Crow3 ]` |
| `ReplaceSpellsWhenDead` | Enum/String | `Spook` |
| `RevengeDamage` | Block | `{ ... }` |
| `ReviveOnWin` | Number | `100%` |
| `Robot` | Block | `{ ... }` |
| `RobotsInheritArmor` | Number | `1, 2` |
| `RockDetector` | Number | `10` |
| `SafeExplosions` | Number | `1` |
| `ScaledStatusOnBleedDamage` | Block | `{ ... }` |
| `ScaledStatusOnLoseShield` | Block | `{ ... }` |
| `ScaledStatusOnOverHealed` | Block | `{ ... }` |
| `ScaledStatusOnOverMana` | Block | `{ ... }` |
| `ScaledStatusOnSpendMana` | Block | `{ ... }` |
| `SchrodingerDisorder` | Number | `50%` |
| `Scleroderma` | Number | `1` |
| `SecurityBotProtect` | Block | `{ ... }` |
| `SelfDamageWhenDealDamage` | Block | `{ ... }` |
| `SetDefaultFacePassive` | Enum/String | `insane` |
| `SetSpellCosts` | Number | `1, 0, 3` |
| `ShareHealthRegen` | Number | `1` |
| `SharePickups` | Number | `1` |
| `ShoulderCheck` | Number | `33%, 100%` |
| `ShovingMatch` | Enum/String | `attack` |
| `ShowHiddenThings` | Number | `1` |
| `SizeScale` | Enum/String | `.4, 1.3, .7` |
| `Slow` | Number | `5` |
| `SmallEnemiesIgnoreYou` | Number | `1` |
| `SmallRockBehavior` | Number | `5` |
| `SmiteEnemiesWhoKill` | Block | `{ ... }` |
| `SpawnCatCopyOnBattleStart` | Block | `{ ... }` |
| `SpawnCreepOnHit` | Number | `1` |
| `SpawnEachTurn` | Block | `{ ... }` |
| `SpawnMeatOnMove` | Enum/String | `Food` |
| `SpawnObjectOnPopCorpse` | Enum/String | `Food` |
| `SpawnOnBattleStartRandomEmptyTile` | Block | `{ ... }` |
| `SpawnOnBattleStart` | Enum/String | `BeefyCharmedLeech, CharmedTinySpider, { ... }` |
| `SpawnThingOnDamage` | Block | `{ ... }` |
| `SpawnThingOnDeath` | Enum/String | `CharmedDemonKitten, ZombieCatFamiliar` |
| `SpecialFriends` | Block | `{ ... }` |
| `SpeedUp` | Number | `6` |
| `SplittableMove` | Number | `1, 3` |
| `SpreadExtraDebuffs` | Number | `1, 2` |
| `SpreadPainBonusCrit` | Number | `1` |
| `SpreadPainBonus` | Number | `2` |
| `StackingDodgeChanceOnTookDamage` | Block | `{ ... }` |
| `StatMinimum` | Number | `5, 7` |
| `StatsAtLowHealth` | Block | `{ ... }` |
| `StatusAdjacentOnTheirTurnBegin` | Block | `{ ... }` |
| `StatusAfterCastSpell` | Block | `{ ... }` |
| `StatusAlliesOnBattleStart` | Block | `{ ... }` |
| `StatusAlliesOnDeath` | Block | `{ ... }` |
| `StatusAlliesOnGainCoins` | Block | `{ ... }` |
| `StatusAlliesOnKill` | Block | `{ ... }` |
| `StatusAlliesOnSpendMana` | Block | `{ ... }` |
| `StatusAlliesScaledByCursedOnDeath` | Block | `{ ... }` |
| `StatusAllyWhenAllySpendsMana` | Block | `{ ... }` |
| `StatusAnyCatAllyWhoKills` | Block | `{ ... }` |
| `StatusCarefulness` | Number | `1` |
| `StatusDamagers` | Block | `{ ... }` |
| `StatusEachTurnBegin` | Block | `{ ... }` |
| `StatusEachTurnEndForEachTurn` | Block | `{ ... }` |
| `StatusEachTurnEndPerEnemyKill` | Block | `{ ... }` |
| `StatusEachTurnEnd` | Block | `{ ... }` |
| `StatusEnemiesOnDeath` | Block | `{ ... }` |
| `StatusEveryXSpellCasts` | Block | `{ ... }` |
| `StatusEveryXTurnBegins` | Block | `{ ... }` |
| `StatusIfBattleAlreadyBegan` | Block | `{ ... }` |
| `StatusIfUnusedMovePoints` | Block | `{ ... }` |
| `StatusImmunity` | Array | `[ Sleep SleepParalysis ], Burn, [ Fear Madness PermanentMadness ]` |
| `StatusKilledCharacters` | Block | `{ ... }` |
| `StatusKillers` | Block | `{ ... }` |
| `StatusOnAllyCatDeath` | Block | `{ ... }` |
| `StatusOnAnyDeath` | Block | `{ ... }` |
| `StatusOnBattleEndIfKillThresholdMet` | Block | `{ ... }` |
| `StatusOnBattleEnd` | Block | `{ ... }` |
| `StatusOnBattleStart` | Block | `{ ... }` |
| `StatusOnBreakItem` | Block | `{ ... }` |
| `StatusOnCastSpell` | Block | `{ ... }` |
| `StatusOnCollectPickup` | Block | `{ ... }` |
| `StatusOnCrit` | Block | `{ ... }` |
| `StatusOnDealtDamageThreshold` | Block | `{ ... }` |
| `StatusOnDealtDamage` | Block | `{ ... }` |
| `StatusOnEatFood` | Block | `{ ... }` |
| `StatusOnEatPill` | Block | `{ ... }` |
| `StatusOnEndMove` | Block | `{ ... }` |
| `StatusOnGainCoins` | Block | `{ ... }` |
| `StatusOnGainShield` | Block | `{ ... }` |
| `StatusOnHeal` | Block | `{ ... }` |
| `StatusOnHealed` | Block | `{ ... }` |
| `StatusOnKillEnemy` | Block | `{ ... }` |
| `StatusOnKill` | Block | `{ ... }` |
| `StatusOnLoseShield` | Block | `{ ... }` |
| `StatusOnOverHealed` | Block | `{ ... }` |
| `StatusOnOverMana` | Block | `{ ... }` |
| `StatusOnPickupCoins` | Block | `{ ... }` |
| `StatusOnPopCorpse` | Block | `{ ... }` |
| `StatusOnStanceSwitch` | Block | `{ ... }` |
| `StatusOnTakeHealthDamage` | Block | `{ ... }` |
| `StatusOnTookDamageFromAbility` | Block | `{ ... }` |
| `StatusOnTookDamageFromEnemyAbility` | Block | `{ ... }` |
| `StatusOnTookDamage` | Block | `{ ... }` |
| `StatusOnTriggerTrap` | Block | `{ ... }` |
| `StatusOnTurnEndIfCastNSpells` | Block | `{ ... }` |
| `StatusOnTurnEndIfDidntCastAbilityTypes` | Block | `{ ... }` |
| `StatusOnTurnEndIfManaExact` | Block | `{ ... }` |
| `StatusOnTurnEndIfManaOrHealthExact` | Block | `{ ... }` |
| `StatusOnUseAbilityWithTag` | Block | `{ ... }` |
| `StatusOnUseBasicAttack` | Block | `{ ... }` |
| `StatusOnUseElementAbility` | Block | `{ ... }` |
| `StatusPerInjury` | Block | `{ ... }` |
| `StatusReplacement` | Array | `[ Petrify PetrifyCharmed ]` |
| `StatusThingsKnockedBack` | Block | `{ ... }` |
| `StatusWhenAllySpendsMana` | Block | `{ ... }` |
| `Stealth` | Number | `1` |
| `StrengthForEachNeighboringEnemy` | Number | `2, 3` |
| `StrengthInNumbersAura` | Number | `1, { ... }` |
| `StrengthUp` | Number | `2` |
| `StrictLimitDamage` | Number | `1` |
| `Study` | Number | `1, { ... }` |
| `TaggedPickupEffectReplacement` | Block | `{ ... }` |
| `TauntAlways` | Number | `1` |
| `TauntAtFullHealth` | Number | `1` |
| `Tech` | Number | `1` |
| `TempInitiativeChange` | Number | `-999` |
| `TheHunger` | Block | `{ ... }` |
| `Thorns` | Number | `2, 4` |
| `TileDamageMultiplier` | Number | `2, { ... }` |
| `TileTrail` | Enum/String | `FlowerTile, GrassTile` |
| `TourettesMeows` | Block | `{ ... }` |
| `TowerDefenseReflex` | Enum/String | `attack, BasicRanged_1DMG` |
| `TowerDefense` | Block | `{ ... }` |
| `Trample` | Number | `9, 3` |
| `TrapEffectsMultiplier` | Number | `2` |
| `TrinketActiveEffectsMultiplierBonus` | Number | `1, 2` |
| `TrinketPassiveMultiplierBonus` | Number | `1, 2` |
| `Triskaidekaphobia` | Number | `13` |
| `UncappedHPBonusStr` | Number | `5` |
| `UncappedHP` | Number | `1` |
| `UncappedMana` | Number | `1` |
| `UpgradeLevelUpClassActives` | Enum/String | `Colorless` |
| `UpgradeLevelUpClassPassives` | Enum/String | `Colorless` |
| `UpgradeSpawnedPickups` | Number | `1, 2` |
| `Vegan` | Number | `1` |
| `Vengeful` | Number | `1` |
| `WaterWalk` | Number | `1` |
| `Weakness` | Number | `1, 5` |
| `WeaponActiveEffectsMultiplierBonus` | Number | `2` |
| `WeaponCountsAsBasicAttack` | Number | `1` |
| `WeaponDamageMultiplierBonus` | Number | `2` |
| `WeaponPassiveMultiplierBonus` | Number | `2` |
| `WeaponsDontLoseDurability` | Number | `0` |
| `WobblyCat` | Number | `25%` |

### Context: `schadenfreude_scaled_stats`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cha` | Number | `2` |
| `con` | Number | `2` |
| `dex` | Number | `2` |
| `int` | Number | `2` |
| `lck` | Number | `2` |
| `spd` | Number | `2` |
| `str` | Number | `2` |

### Context: `spell_graphics_override`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `area_particle` | Enum/String | `WaterConduct` |
| `center_particle` | Enum/String | `WaterConduct` |
| `palette` | Number | `-1` |
| `particle` | Enum/String | `WaterConduct` |

### Context: `stats`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cha` | Number | `2, 4, 3` |
| `con` | Number | `2, -1, -2` |
| `dex` | Number | `6, -1, 3` |
| `int` | Number | `2, -1, -2` |
| `lck` | Number | `1, 2, 4` |
| `spd` | Number | `1, 2, 3` |
| `str` | Number | `2, -1, 4` |

### Context: `statuses`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |
| `FindItemFromPool` | Enum/String | `consumables, chapter` |
| `HealthGain` | Number | `10` |
| `PermanentDexterity` | Number | `1` |

### Context: `threshold`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `cha` | Number | `0` |
| `int` | Number | `-10, 0, 4` |
| `spd` | Number | `0` |

### Context: `triattack`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `damage` | Number | `6` |
| `effects` | Block | `{ ... }` |
| `elements` | Array | `[ Fire Ice Electric ]` |
| `type` | Enum/String | `spell` |

---

## Spawns & Enemy Pools

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `#` | Enum/String | `ID` |
| `early_spawn` | Boolean | `true` |
| `editor` | Block | `{ ... }` |
| `empty!` | Enum/String | `editor` |
| `forced_placement` | Boolean | `true` |
| `image` | String | `"empty.png"` |
| `name` | String | `"Empty"` |
| `object` | Enum/String | `Rat, Fly, Worm` |
| `orientation` | Enum/String | `south, north, east` |
| `reserved` | Enum/String | `for` |
| `tag_location` | Enum/String | `FinalBossCloneSpot, ChaosValidPosition, HitlerMiniInitial` |
| `trap` | Enum/String | `WaterKittenTrap, WebTrap` |
| `utility` | Enum/String | `PlayerSpawn` |
| `value` | Number | `1, 0, .5` |
| `weather_element_alt` | Block | `{ ... }` |

### Context: `editor`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `category` | Number | `1, 4, 3` |
| `image_tint` | Array | `[ blue ], [ yellow ], [ blue none ]` |
| `image` | Array | `[ "rat.png" ], [ "shadow.png" "cat.png" ], [ "fly.png" ]` |
| `layer` | Number | `2` |
| `name` | String | `"Player Cat Spawn", "Rat", "Fly"` |
| `paint` | Boolean | `false, true` |
| `subcategory` | Number | `1, 2, 3` |

### Context: `weather_element_alt`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `element` | Enum/String | `Ice` |
| `object` | Enum/String | `IceElemental` |

---

## Status Effect Keywords

### Context: `ROOT`
| Property Key | Inferred Type | Example Values |
| :--- | :--- | :--- |
| `alias` | Enum/String | `DodgeChance_Status, Infested, AllStatsUp` |
| `icon_frame` | Number | `152, 17, 141` |
| `name_reference_applier` | String | `"KEYWORD_MANALEECHES_NAME_APPLIER", "KEYWORD_ATTRACTION_REF", "KEYWORD_LEECHES_NAME_APPLIER"` |
| `name_stacks_neg` | String | `"KEYWORD_CONDOWN_NAME", "KEYWORD_ALLSTATSDOWN_NAME", "KEYWORD_CHADOWN_NAME"` |
| `name` | String | `"KEYWORD_ALPHA_NAME", "KEYWORD_ADRENALINE_NAME", "KEYWORD_ALLSTATSUP_NAME"` |
| `tooltip_reference_applier` | String | `"KEYWORD_MANALEECHES_DESC_APPLIER", "KEYWORD_LEECHES_DESC_APPLIER", "KEYWORD_ATTRACTION_DESC_REF"` |
| `tooltip_stackless_neg` | String | `"KEYWORD_TEMPINITDOWN_DESC", "KEYWORD_MOVEMENTDOWN_DESC_STACKLESS", "KEYWORD_DAMAGEDOWN_DESC_STACKLESS"` |
| `tooltip_stackless_pos` | String | `"KEYWORD_DAMAGEUP_DESC_STACKLESS", "KEYWORD_MOVEMENTUP_DESC_STACKLESS"` |
| `tooltip_stackless` | String | `"KEYWORD_ALPHA_DESC_STACKLESS", none, "KEYWORD_ATTRACTION_DESC_STACKLESS"` |
| `tooltip_stacks_neg` | String | `"KEYWORD_CHADOWN_DESC", "KEYWORD_PERMABLIND_DESC", "KEYWORD_ALLSTATSDOWN_DESC"` |
| `tooltip_stacks_pos` | String | `"KEYWORD_ALLSTATSUP_DESC", "KEYWORD_CONUP_DESC", "KEYWORD_CHAUP_DESC"` |
| `tooltip_stacks_singular` | String | `"KEYWORD_COUNTER_DESC", "KEYWORD_CHARGEFISTS_DESC_SINGULAR", "KEYWORD_BLIND_DESC_STACKLESS"` |
| `tooltip_stacks` | String | `"KEYWORD_AMMO_DESC", "KEYWORD_ATTRACTION_DESC", "KEYWORD_BLASTRESISTANCE_DESC"` |
| `tooltip` | String | `"KEYWORD_ADRENALINE_DESC", "KEYWORD_BACKFLIP_DESC", "KEYWORD_ALPHA_DESC"` |

---
