# Mewgenics Mod Developer Documentation: Master Schema Dictionary

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Abilities & Spells

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai_ability` | Enum/String | `SpawnBomb_AI, Magnetize_AI, NubsJump_AI` | Overrides the ability used when triggered by AI. |
| `bonk_damage` | Block | `{ ... }` | Damage dealt when knocked into a wall or obstacle. |
| `bonus_passives` | Block | `{ ... }` | Passives granted to the character while this ability is equipped. |
| `chain_ability` | Enum/String | `ControlPlantsPartTwo2, ControlPlantsPartTwo, Dump` | An ability that automatically executes sequentially after this one. |
| `class` | Enum/String | `SuplexAbility, PlaceholderMeleeAttackAbility, MultiHitMeleeAttackAbility` | The character class identifier this ability belongs to. |
| `cloned_ability` | Enum/String | `attack` | Copies the properties of another ability dynamically. |
| `cost` | Block | `{ ... }` | Block defining resource requirements (Mana, Act Points, Moves) needed to cast. |
| `damage_instance` | Block | `{ ... }` | Block defining the combat math and status effects applied upon successful hit. |
| `damage` | Block | `{ ... }` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `empty_self_damage` | Block | `{ ... }` | Recoil damage specifically applied when the attack misses all targets. |
| `graphics` | Block | `{ ... }` | Block defining visual animations and sequence timings. |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear when hovering over the ability. |
| `meta` | Block | `{ ... }` | Block defining UI display data (Name, Description, Icon). |
| `self_damage` | Block | `{ ... }` | Recoil or self-inflicted damage/effects applied to the caster. |
| `sounds` | Block | `{ ... }` | Audio cues triggered by the ability. |
| `spawn` | Block | `{ ... }` | Parameters for summoning new characters, objects, or entities. |
| `splash_damage` | Block | `{ ... }` | Secondary Area of Effect blast parameters. |
| `sub_ability` | Enum/String | `Spin, TeamFlex_Impl, Huddle_Impl` | A secondary ability component referenced by complex templates. |
| `tags` | Array | `[ musical ], [ weapon_throw ], [ summon ]` | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). |
| `target` | Block | `{ ... }` | Block defining the shape, range, and restrictions of the ability's aiming phase. |
| `template` | Enum/String | `melee_attack, spell, targeted_status` | Inherits baseline internal logic from a hardcoded engine template. |
| `temporary_effects` | Block | `{ ... }` | Status applications that wear off automatically or at the end of the turn. |
| `variant_of` | Enum/String | `BasicMelee, Asteroid, BasicJump` | Inherits properties from a previously defined ability (used for upgrading tiers). |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Bruise` | Number | `2` | Applies or references the 'Bruise' effect/state. |

### Context: `AfterImage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `PlayerCat_ThiefShade` | The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade). |
| `skilltemp` | Boolean | `true` | If true, the decoy is automatically destroyed once the skill finishes executing. |

### Context: `AlphaStatusOnTurnBegin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | `1` | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |

### Context: `ApplyMultipleTimes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `stacks` | Number | `8, 4, X` | The number of times the nested effects block should be repeatedly executed. |

### Context: `ApplyPassives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddTag` | Enum/String | `plant, squirrel` | Applies or references the 'AddTag' effect/state. |
| `ElementImmune` | Enum/String | `Creep` | Applies or references the 'ElementImmune' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `Plant` | Number | `1` | Applies or references the 'Plant' effect/state. |
| `ReplaceBasicAttack` | Enum/String | `BasicPuke` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `StatusOnBattleEnd` | Block | `{ ... }` | Applies the nested status effects when the encounter finishes. |
| `YOffset` | Enum/String | `.25` | Applies or references the 'YOffset' effect/state. |

### Context: `ApplyPassivesToSpawnerWhileAlive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HideEquipment` | Enum/String | `neck` | Applies or references the 'HideEquipment' effect/state. |

### Context: `ApplyStatusIfCrit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `Bleed` | Number | `1, 5` | Applies or references the 'Bleed' effect/state. |
| `LuckUp` | Number | `-1` | Applies or references the 'LuckUp' effect/state. |

### Context: `ApplyStatusesNextTurnBegin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |

### Context: `ApplyToConsumed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | Number | `1` | Applies or references the 'DeleteObject' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |

### Context: `ApplyToOthersWithSharedTagAndFaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |

### Context: `ApplyToRandomClosestAlly`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Number | `1` | Applies or references the 'ForceMoveTowards' effect/state. |

### Context: `ApplyToRandomPartyMemberIfPossible`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `GainDisorderFromPool_PostCast` | Enum/String | `forbidden_spell_consequences_crippling, forbidden_spell_consequences` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |

### Context: `ApplyToSource`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddLeechesStatus` | Number | `1` | Applies or references the 'AddLeechesStatus' effect/state. |
| `AddWeaponAux` | String | `"-max(min(X+1, item_aux), 0)", 1, -item_aux` | Applies or references the 'AddWeaponAux' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `ConstitutionUp` | Number | `1, 2` | Applies or references the 'ConstitutionUp' effect/state. |
| `Craft` | Block | `{ ... }` | Synthesizes or spawns a new item from a specific pool. |
| `DisableWeapon` | Number | `1` | Applies or references the 'DisableWeapon' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `DoDamage` | Block | `{ ... }` | Explicitly triggers a secondary damage instance independent of the main attack. |
| `EquipPermanentItem` | Enum/String | `Kidney, BoneClub` | Applies or references the 'EquipPermanentItem' effect/state. |
| `EvolveAbilityFromPool` | Enum/String | `Butcher, Medic, Thief` | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `FindItemFromPool` | Block | `{ ... }` | Generates an item drop from the specified loot pool. |
| `FindItem` | Enum/String | `Molars` | Applies or references the 'FindItem' effect/state. |
| `ForceUseAbility` | Enum/String | `Ram_chained` | Applies or references the 'ForceUseAbility' effect/state. |
| `FormChange` | Enum/String | `Default, HasCat, { ... }` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FreeSpell` | Number | `1, 2` | Applies or references the 'FreeSpell' effect/state. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `GainCoinsRange` | Block | `{ ... }` | Grants the player a randomized amount of coins within a min/max range. |
| `HealthGain` | Number | `1, 8, 4` | Applies or references the 'HealthGain' effect/state. |
| `KineticSpikes` | Number | `1` | Applies or references the 'KineticSpikes' effect/state. |
| `KnockUpAndAway` | Block | `{ ... }` | Displaces the target vertically and horizontally away from the source. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `ManaGain` | Number | `2` | Applies or references the 'ManaGain' effect/state. |
| `MoveQuivered` | Number | `1` | Applies or references the 'MoveQuivered' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `RefreshMovePoints` | Number | `1` | Applies or references the 'RefreshMovePoints' effect/state. |
| `RemoveStatus` | Enum/String | `DodgeChance_Status, SpeedUp_WithoutInitiative` | Applies or references the 'RemoveStatus' effect/state. |
| `Shield` | Number | `1, 2, 5` | Applies or references the 'Shield' effect/state. |
| `SpecificInjury` | Enum/String | `str` | Applies or references the 'SpecificInjury' effect/state. |
| `StanceSwitchToMelee` | Number | `1` | Applies or references the 'StanceSwitchToMelee' effect/state. |
| `StanceSwitchToRanged` | Number | `1` | Applies or references the 'StanceSwitchToRanged' effect/state. |
| `StrengthUp` | Number | `1, 3` | Applies or references the 'StrengthUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `Tech` | Number | `1` | Applies or references the 'Tech' effect/state. |
| `TempTrampleUntilSettled` | Number | `3` | Applies or references the 'TempTrampleUntilSettled' effect/state. |

### Context: `ApplyToSourceOnKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `AlphaCat` | Number | `1` | Applies or references the 'AlphaCat' effect/state. |
| `CompleteItemQuest` | Enum/String | `BlackShard` | Applies or references the 'CompleteItemQuest' effect/state. |
| `EvolveAbilityFromPool` | Enum/String | `Hunter` | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `HealthGain` | Number | `5, 10` | Applies or references the 'HealthGain' effect/state. |
| `ManaGain` | Number | `5` | Applies or references the 'ManaGain' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `RemoveItem` | Enum/String | `BlackShard, BlackShard_Glowing` | Applies or references the 'RemoveItem' effect/state. |
| `Revive` | Number | `100%, 50%` | Applies or references the 'Revive' effect/state. |
| `StrengthUp` | Number | `2` | Applies or references the 'StrengthUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `TransformWeapon` | Block | `{ ... }` | Transforms the equipped weapon into another specific weapon state. |
| `WeaponAuxMultiplier` | Enum/String | `.5` | Applies or references the 'WeaponAuxMultiplier' effect/state. |

### Context: `ApplyToTile`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHit` | Enum/String | `Bait` | Spawns a specific physics/item object upon impact. |
| `SpawnBearTrap` | Number | `1` | Applies or references the 'SpawnBearTrap' effect/state. |

### Context: `ArcLightning`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.5` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `enemies_only` | Boolean | `false, true` | If true, the arc will not bounce to friendly targets. |
| `ignore_self` | Boolean | `true` | If true, prevents the arc from bouncing back to the caster. |
| `max_distance` | Number | `1, 2, 3` | The maximum tile range the lightning can jump between bounces. |
| `stacks` | Number | `100` | The maximum number of targets the lightning can bounce to. |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `Transcend2, SharpenNail2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

### Context: `BackflipWhenTargeted`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `DestroyerDodge, SZBBackflipDodge, Teleport` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `1, 4` | Number of stacks or intensity to apply. |

### Context: `BodyGuard`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `BodyGuardSwap2, BodyGuardSwap` | The specific ability ID to use when intercepting (e.g., BodyGuardSwap). |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `BounceObject`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.25, .5` | Probability (0.0 to 1.0) of spawning the object. |
| `obj` | Enum/String | `SmallLavaRock, chapter_corpse_medium` | The entity ID of the object to spawn (e.g., chapter_corpse_medium). |
| `slide` | Number | `10` |  |

### Context: `CanApplyToInanimate`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BreakIntoRocks` | Enum/String | `Coin, SmallRock` | Applies or references the 'BreakIntoRocks' effect/state. |
| `GetAggroTarget` | Number | `1` | Applies or references the 'GetAggroTarget' effect/state. |
| `ObjectOnHitCharacter` | Enum/String | `CharmedLeech, AllyRotFly, Fly` | Spawns a specific character or entity upon impact. |
| `PreventDeathTransforms` | Number | `1` | Applies or references the 'PreventDeathTransforms' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |

### Context: `CatPartsSizeScaleStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | `1.1` | Scale multiplier for the front arm. |
| `arm2` | Number | `1.1` | Scale multiplier for the back arm. |
| `body` | Number | `1.1` |  |
| `mouth` | Number | `1.1` |  |

### Context: `CatPartsTransform`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | `1501, 1013, 338` | Sprite variant ID for the front arm. |
| `arm2` | Number | `1501, 1013, 324` |  |
| `body` | Number | `1029, 31` | Sprite variant ID for the body. |
| `ear1` | Number | `1501, 325, 23` | Sprite variant ID for the front ear. |
| `ear2` | Number | `1501, 23, 1036` |  |
| `eye1` | Number | `1069` |  |
| `eye2` | Number | `1069` |  |
| `eyebrow1` | Number | `1069` |  |
| `eyebrow2` | Number | `1070` |  |
| `head` | Number | `12, 1504` | Sprite variant ID for the head. |
| `leg1` | Number | `1501, 41, 338` | Sprite variant ID for the front leg. |
| `leg2` | Number | `1501, 41, 338` |  |
| `mouth` | Number | `1501, 1005, 1071` |  |
| `palette` | Number | `86` |  |
| `tail` | Number | `1503, 4, 1502` | Sprite variant ID for the tail. |
| `texture` | Number | `1008, 322` |  |

### Context: `ChanceToBreakFree`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `XXX, LennyDrop, CHuskDrop` | The ability triggered upon successfully breaking free. |
| `fail_ability` | Enum/String | `XXX, LennyStruggleFail, CHuskDropFail` | The ability triggered if the break free attempt fails. |
| `stacks` | Number | `25` | Percentage base chance to break free. |

### Context: `ChangeTile`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | `1` |  |
| `chance` | Enum/String | `.25, 25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `tile` | Enum/String | `GlassTile, ToxicTile, [ TallGrassTile TallFlowerTile BrambleTile ]` | The specific tile type to change into (e.g., GlassTile). |

### Context: `Cleave`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.25` | Probability (0.0 to 1.0) that the cleave effect triggers. |

### Context: `CollectsPickupsWithAltEffects`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponAddPoison` | Number | `1` | Applies or references the 'CurrentWeaponAddPoison' effect/state. |
| `LuckUp` | Number | `2` | Applies or references the 'LuckUp' effect/state. |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |
| `Tech` | Number | `1` | Applies or references the 'Tech' effect/state. |

### Context: `Conditional_ActiveWeather_Any`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `weather` | Array | `[ FlySwarm FireflySwarm ButterflySwarm ]` | An array of weather states to check against. |

### Context: `Conditional_AffectedByElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` | Applies or references the 'BonusCritChance' effect/state. |
| `Burn` | Number | `2` | Applies or references the 'Burn' effect/state. |
| `Conditional_Speculative` | Block | `{ ... }` | A simulation block used by the AI to test hypothetical outcomes before committing to an action. |
| `element` | Enum/String | `Water, Fire` | The specific element type to check for. |

### Context: `Conditional_Ally`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `ApplyToSourceOnKill` | Block | `{ ... }` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BleedThorns` | Number | `3` | Applies or references the 'BleedThorns' effect/state. |
| `ChanceToBreak` | Number | `5%` | Applies or references the 'ChanceToBreak' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `Conditional_Corpse` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| `Conditional_PlayerCat` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a player-controlled cat. |
| `DamageUp` | Number | `1, 2` | Applies or references the 'DamageUp' effect/state. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `HealthGain` | Number | `4` | Applies or references the 'HealthGain' effect/state. |
| `KnockbackDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. |
| `OverrideDamage` | Number | `-10, 0` | Applies or references the 'OverrideDamage' effect/state. |
| `RandomStatUp` | String | `"ceil(X/2)", "ceil(X/3)"` | Applies or references the 'RandomStatUp' effect/state. |
| `RepairAll` | Number | `1` | Applies or references the 'RepairAll' effect/state. |
| `ShowText` | String | `"COMBAT_POPUP_REPAIRED"` | Applies or references the 'ShowText' effect/state. |
| `TempDamageUp` | Number | `1` | Applies or references the 'TempDamageUp' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `ThornsDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `TileDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. |

### Context: `Conditional_Backstab`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` | Applies or references the 'BonusCritChance' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `Instakill` | Number | `25` | Applies or references the 'Instakill' effect/state. |
| `odds` | Enum/String | `.16666666` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

### Context: `Conditional_Boss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusDamage` | Number | `25` | Applies or references the 'BonusDamage' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Conditional_HasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Drowsy` | Number | `1` | Applies or references the 'Drowsy' effect/state. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `ExplodeCharacter_NoDie` | Number | `5` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. |
| `ExplodeCharacter_PartyBoss` | Number | `5` | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | `5, 9` | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `OverrideDamage` | Number | `25, 10` | Applies or references the 'OverrideDamage' effect/state. |
| `RemoveStatus` | Enum/String | `Petrify` | Applies or references the 'RemoveStatus' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `VisualFX` | Enum/String | `Explosion, PartyExplosion` | Applies or references the 'VisualFX' effect/state. |
| `XIsTargetHealth` | Block | `{ ... }` | Math variable assignment: Evaluates X as the target's current health. |

### Context: `Conditional_BossOrBig`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Immobile` | Array | `[ 1 .25 ]` | Applies or references the 'Immobile' effect/state. |

### Context: `Conditional_Buddy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_InForm` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. |
| `Consumed` | Block | `{ ... }` | State block triggered when this object or entity is eaten/consumed by another character. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |

### Context: `Conditional_CanBeHealed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |

### Context: `Conditional_Corpse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Conditional_Enemy` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `FlatAIBonus` | Number | `100` | Applies or references the 'FlatAIBonus' effect/state. |
| `HealRandomInjury` | Number | `1` | Applies or references the 'HealRandomInjury' effect/state. |
| `PermanentCharm` | Number | `1` | Applies or references the 'PermanentCharm' effect/state. |
| `Revive` | Number | `100%, 50%` | Applies or references the 'Revive' effect/state. |

### Context: `Conditional_DebuffRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `odds` | Number | `15%` | The probability (0.0 to 1.0) of applying the debuff. |

### Context: `Conditional_DestructibleCorpse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToTile` | Block | `{ ... }` | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. |
| `VaporizeCorpse` | Number | `1` | Applies or references the 'VaporizeCorpse' effect/state. |

### Context: `Conditional_Displaceable`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `LaunchOffScreenInstakill` | Number | `1` | Applies or references the 'LaunchOffScreenInstakill' effect/state. |
| `LaunchOffScreen` | Enum/String | `10+bonus_melee_ability_damage` | Applies or references the 'LaunchOffScreen' effect/state. |
| `TempInitiativeChange` | Number | `-100` | Applies or references the 'TempInitiativeChange' effect/state. |

### Context: `Conditional_Enemy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, -1` | Applies or references the 'AllStatsUp' effect/state. |
| `ApplyToSourceOnKill` | Block | `{ ... }` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `Attraction` | Number | `1` | Applies or references the 'Attraction' effect/state. |
| `BonusDamage` | Number | `1` | Applies or references the 'BonusDamage' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Conditional_FinishedSpawning` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. |
| `Conditional_NotBoss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| `Confusion` | Number | `1, [ 1 .2 ], 3` | Applies or references the 'Confusion' effect/state. |
| `DisplaceToAbilityTarget` | Number | `1` | Applies or references the 'DisplaceToAbilityTarget' effect/state. |
| `Doomed` | Number | `1` | Applies or references the 'Doomed' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `ForceMoveTowards` | Number | `1` | Applies or references the 'ForceMoveTowards' effect/state. |
| `Hex` | Number | `1` | Applies or references the 'Hex' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `PermanentCharm` | Number | `1` | Applies or references the 'PermanentCharm' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Stun` | Array | `[ 1, .25 ]` | Applies or references the 'Stun' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `TempDamageUp` | Number | `-1` | Applies or references the 'TempDamageUp' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `Weakness` | Number | `1, 2` | Applies or references the 'Weakness' effect/state. |

### Context: `Conditional_Familiar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `BonusDamage` | Number | `-2` | Applies or references the 'BonusDamage' effect/state. |
| `DamageUp` | Number | `2, 3` | Applies or references the 'DamageUp' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |

### Context: `Conditional_FinishedSpawning`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Imprison` | Enum/String | `Fly` | Applies or references the 'Imprison' effect/state. |

### Context: `Conditional_FirstApplicationThisTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `TempPassiveWhileHasStatus` | Block | `{ ... }` | Grants nested passives only while the character possesses the specified status. |
| `key` | Enum/String | `TaintedOffering, TaintedOffering2, EtherSoakedRag` | A unique string identifier to track this specific application. |

### Context: `Conditional_FormulaIsPositive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Enum/String | `X+1, X` | Applies or references the 'Burn' effect/state. |
| `Freeze` | Number | `1` | Applies or references the 'Freeze' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `OverrideKnockbackDamage` | Enum/String | `X*10` | Applies or references the 'OverrideKnockbackDamage' effect/state. |
| `Shield` | Number | `6, 5` | Applies or references the 'Shield' effect/state. |
| `Slow` | Enum/String | `X` | Applies or references the 'Slow' effect/state. |
| `SpeedUp` | Number | `-1` | Applies or references the 'SpeedUp' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `formula` | Enum/String | `X+1, X-1, X` | The math expression to evaluate. |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToRandomPartyMemberIfPossible` | Block | `{ ... }` | Redirects the nested effects to apply to a random living member of the player's party. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `GainDisorderFromPool_PostCast` | Enum/String | `forbidden_spell_consequences` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |
| `GainDisorder` | Enum/String | `Chungus` | Applies or references the 'GainDisorder' effect/state. |
| `ImmediateUseAbility` | Enum/String | `tk_ButterBean_Mega` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `RefreshWeaponAbility` | Number | `1` | Applies or references the 'RefreshWeaponAbility' effect/state. |
| `ShowText` | String | `"COMBAT_POPUP_RELOAD"` | Applies or references the 'ShowText' effect/state. |
| `odds` | Number | `10%, 50%, 90%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

### Context: `Conditional_HasCleansableDebuffs`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | Number | `5` | Applies or references the 'GenericBuff' effect/state. |
| `PartialCleanse` | Number | `1` | Applies or references the 'PartialCleanse' effect/state. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |

### Context: `Conditional_HasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BonusDamage` | Number | `10, 20` | Applies or references the 'BonusDamage' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `FormChange` | Enum/String | `Bully` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `RemoveStatus` | Enum/String | `Petrify` | Applies or references the 'RemoveStatus' effect/state. |
| `Slow` | Number | `2` | Applies or references the 'Slow' effect/state. |
| `status` | Enum/String | `Undead, Freeze, Petrify` | The specific status ID to check for. |

### Context: `Conditional_HasTag`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSourceOnKill` | Block | `{ ... }` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BonusDamage` | Number | `10` | Applies or references the 'BonusDamage' effect/state. |
| `CanApplyToInanimate` | Block | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `ChangeTilesUnder` | Enum/String | `LavaTile` | Applies or references the 'ChangeTilesUnder' effect/state. |
| `Conditional_Boss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a Boss. |
| `Conditional_InForm` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. |
| `Conditional_NotBoss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| `CrackMoonHead` | Number | `1` | Applies or references the 'CrackMoonHead' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `DeleteObject` | Number | `1` | Applies or references the 'DeleteObject' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |
| `DisplaceTowardsSource` | Number | `1` | Applies or references the 'DisplaceTowardsSource' effect/state. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `EventBounty` | Number | `5` | Applies or references the 'EventBounty' effect/state. |
| `FaceAway` | Number | `1` | Applies or references the 'FaceAway' effect/state. |
| `FloatingRockTrap` | Number | `1` | Applies or references the 'FloatingRockTrap' effect/state. |
| `IgnoreDamage` | Number | `1` | Applies or references the 'IgnoreDamage' effect/state. |
| `ImmediateUseAbility` | Enum/String | `HitlerCloneTransform, HitlerCloneHeil, MoonHandMegaSqueeze` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `Instakill` | Number | `25` | Applies or references the 'Instakill' effect/state. |
| `MergeDamageInstance` | Block | `{ ... }` | Combines damage numbers or visual hit effects. |
| `OverrideDamage` | Number | `1` | Applies or references the 'OverrideDamage' effect/state. |
| `PopAndSpawn` | Block | `{ ... }` | Destroys the target and replaces it with a new spawned entity. |
| `RemoveStatus` | Enum/String | `Brace` | Applies or references the 'RemoveStatus' effect/state. |
| `ScatterRandomPickups` | Number | `5` | Applies or references the 'ScatterRandomPickups' effect/state. |
| `SetAnimationAlts` | Block | `{ ... }` | Overrides specific animation states with alternative animations. |
| `SetKnockback` | Number | `0` | Applies or references the 'SetKnockback' effect/state. |
| `UseAbility` | Enum/String | `MoonHead_CommandHeadPunch` | Forces the character or target to instantly use a specified ability. |
| `VaporizeCorpse` | Number | `1` | Applies or references the 'VaporizeCorpse' effect/state. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |
| `tag` | Enum/String | `poop, moonhead, food` | The specific string tag to check for. |

### Context: `Conditional_HealthThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BonusDamage` | Enum/String | `20+bonus_melee_damage` | Applies or references the 'BonusDamage' effect/state. |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |
| `FactionConversion` | Number | `1` | Applies or references the 'FactionConversion' effect/state. |
| `FlatLeech` | Number | `5` | Applies or references the 'FlatLeech' effect/state. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `Instakill` | Number | `999` | Applies or references the 'Instakill' effect/state. |
| `SpawnThingIfHitKills` | Enum/String | `Food` | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |
| `threshold_expr` | Enum/String | `item_aux` |  |
| `threshold_flat` | Number | `5, 10, 3` | A flat numerical health value threshold. |
| `threshold_percent` | Number | `25%, 50%` | A percentage-based health threshold (e.g. 50%). |

### Context: `Conditional_InForm`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CritChanceUp` | Number | `20` | Applies or references the 'CritChanceUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `DodgeChance_Status` | Number | `20` | Applies or references the 'DodgeChance_Status' effect/state. |
| `ForceImmediateMoveAndAttack` | Block | `{ ... }` | Forces the character to immediately move to a target and use a specified ability. |
| `FormChange` | Enum/String | `Lifted, Big, Drunker` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `UseAbility` | Enum/String | `MoonHandPunchHead` | Forces the character or target to instantly use a specified ability. |
| `form` | Enum/String | `Default, Small, Normal` | The specific form ID to check for. |

### Context: `Conditional_IsSelf`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | `0` | Applies or references the 'OverrideDamage' effect/state. |

### Context: `Conditional_IsTrample`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `SetKnockback` | Number | `0` | Applies or references the 'SetKnockback' effect/state. |

### Context: `Conditional_LastHit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusDamage` | Number | `3` | Applies or references the 'BonusDamage' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `DelayCastAbility` | Enum/String | `HitlerNuke` | Queues an ability to be cast automatically after a certain delay or trigger. |
| `KnockUpAndAway` | Block | `{ ... }` | Displaces the target vertically and horizontally away from the source. |

### Context: `Conditional_LivingPlayerCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `Consumed` | Block | `{ ... }` | State block triggered when this object or entity is eaten/consumed by another character. |
| `TempPassiveWhileHasStatus` | Block | `{ ... }` | Grants nested passives only while the character possesses the specified status. |

### Context: `Conditional_NotAlly`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |

### Context: `Conditional_NotBig`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Number | `1` | Applies or references the 'DisplaceTowardsSource' effect/state. |

### Context: `Conditional_NotBoss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CanApplyToInanimate` | Block | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `Conditional_HealthThreshold` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `Doomed` | Number | `1` | Applies or references the 'Doomed' effect/state. |
| `ExplodeCharacter_RockCrusher` | Number | `5, 9` | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. |
| `FactionConversion` | Number | `1` | Applies or references the 'FactionConversion' effect/state. |
| `Fear` | Array | `[ 1 .3 ]` | Applies or references the 'Fear' effect/state. |
| `PermanentCharm` | Number | `1` | Applies or references the 'PermanentCharm' effect/state. |
| `VaporizeInanimate` | Number | `1` | Applies or references the 'VaporizeInanimate' effect/state. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |

### Context: `Conditional_NotBossOrBig`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |

### Context: `Conditional_NotShielded`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | `10, 3` | Applies or references the 'Knockback' effect/state. |

### Context: `Conditional_Object`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CanApplyToInanimate` | Block | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `Conditional_HasTag` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `RepairWeapon` | Number | `1` | Applies or references the 'RepairWeapon' effect/state. |

### Context: `Conditional_OncePerBattle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | Enum/String | `Nuke` | Applies or references the 'CompleteItemQuest' effect/state. |
| `TriggerGameEnding` | Number | `1, 0` | Applies or references the 'TriggerGameEnding' effect/state. |
| `key` | Enum/String | `gamewin` |  |

### Context: `Conditional_PlayerCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Adrenaline` | Number | `10` | Applies or references the 'Adrenaline' effect/state. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `ConjureRandomAbilityFromCat` | Number | `1` | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. |
| `GenericDebuff` | Number | `999999` | Applies or references the 'GenericDebuff' effect/state. |
| `KnockOutClone` | Enum/String | `PlayerCat_MiniMiniMe` | Applies or references the 'KnockOutClone' effect/state. |
| `Scrambled` | Number | `1` | Applies or references the 'Scrambled' effect/state. |
| `T2CopyCat` | Number | `1` | Applies or references the 'T2CopyCat' effect/state. |

### Context: `Conditional_RandomChance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyPassives` | Block | `{ ... }` | Grants the nested passive abilities dynamically. |
| `odds` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

### Context: `Conditional_Shielded`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum/String | `str` | Applies or references the 'BonusDamage' effect/state. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |

### Context: `Conditional_SourceAbilityHasTag`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `ScatterCoins` | Block | `{ ... }` | Throws coins out into the level randomly. |
| `tag` | Enum/String | `weapon_throw` | Specific entity tag required. |

### Context: `Conditional_SourceHasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `status` | Enum/String | `AlphaCat` | ID of the status effect to apply or check. |

### Context: `Conditional_Speculative`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusDamageBasedOnDistance` | Number | `1` | Applies or references the 'BonusDamageBasedOnDistance' effect/state. |
| `BonusDamage` | Number | `-1` | Applies or references the 'BonusDamage' effect/state. |
| `CapDamage` | Number | `1` | Applies or references the 'CapDamage' effect/state. |
| `Conditional_HealthThreshold` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `IgnoreDamage` | Number | `1` | Applies or references the 'IgnoreDamage' effect/state. |
| `Knockback` | Number | `10` | Applies or references the 'Knockback' effect/state. |
| `RandomBonusDamage` | Number | `25` | Applies or references the 'RandomBonusDamage' effect/state. |

### Context: `ConjureBonusAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `Colorless, Class` | The ID of the ability to conjure. |
| `upgraded` | Boolean | `true` | If true, conjures the upgraded version of the ability. |

### Context: `Consumed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_not_pop_corpse` | Boolean | `true` |  |
| `drop_body_ability` | Enum/String | `MoonHandDrop` |  |
| `drop_on_death` | Enum/String | `deferred, false, true` |  |
| `drop_on_self_death` | Boolean | `true` |  |
| `extra_statuses` | Block | `{ ... }` | Additional generic status applications. |
| `force_contact` | Boolean | `true` | If true, enforces physical overlap. |
| `instant` | Boolean | `true` |  |
| `kill_on_consume` | Boolean | `true` |  |
| `mount_mode` | Enum/String | `auto, true` | If true, treats the consumption as riding/mounting instead of eating. |
| `struggle_ability` | Enum/String | `TinaFlail, TinaFlailRage, Thrash` | Ability triggered by the consumed entity while inside the consumer. |
| `use_placeholder` | Boolean | `true` |  |
| `wet` | Boolean | `false, true` |  |

### Context: `CopySpells`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |
| `upgraded` | Boolean | `true` |  |

### Context: `Craft`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Enum/String | `stick, allsticks, tinkerer_default` |  |
| `slot` | Enum/String | `weapon, random_empty_armor, trinket` |  |
| `temporary` | Boolean | `false` |  |
| `works_with_tech` | Boolean | `true` |  |

### Context: `CreateGlobalModifiers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | `1` | Applies or references the 'BloodRain' effect/state. |
| `LowerAmbientLight` | Block | `{ ... }` | A visual effect that dims the map's lighting. |

### Context: `DelayCastAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `FetusAirstrike` | The ID of the ability to cast later. |
| `lingering` | Boolean | `true` |  |
| `relative` | Boolean | `false` |  |

### Context: `DelayedWindCone`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `5` | The base damage properties of an attack. |
| `distance` | Number | `10` | Distance or area of effect in tiles. |

### Context: `DestroyEquipmentAndAttachParasite`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `1, .15` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `pool` | Enum/String | `parasites, [ FlyHat FlyMask FlyNeck ], [ AmoebaHat AmoebaNeck AmoebaFace ]` | The item pool to draw the parasite from. |

### Context: `DoDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage_tiles` | Enum/String | `all` |  |
| `damage` | Number | `5, 8, 0` | The flat damage amount. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Water ], [ Fire ]` |  |
| `type` | Enum/String | `generic_physical, melee, spell` | The classification of the damage (e.g., spell, melee). |

### Context: `DoDistortionRing`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | `1, 2, -1` |  |
| `radius` | Number | `5, 4` | Distance or area of effect in tiles. |
| `speed` | Number | `30, -30, 20` |  |

### Context: `DoScreenShake`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | `20, 10, 3` |  |
| `time` | Number | `2, .75, .5` |  |

### Context: `DustOnHit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `GasCloud` | The ID of the object/particle to spawn. |

### Context: `DybbukPossessed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit_ability` | Enum/String | `DybbukReturn` |  |
| `punch_self_ability` | Enum/String | `Dybbuk_StopHittingYourself` |  |

### Context: `Else`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `ApplyToRandomPartyMemberIfPossible` | Block | `{ ... }` | Redirects the nested effects to apply to a random living member of the player's party. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BonusDamage` | Number | `1, 5, 20+bonus_melee_damage` | Applies or references the 'BonusDamage' effect/state. |
| `Bruise` | Number | `4` | Applies or references the 'Bruise' effect/state. |
| `CanApplyToInanimate` | Block | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `CatPartsTransform` | Block | `{ ... }` | Transforms specific body parts into different visual variants. |
| `Charmed` | Number | `2` | Applies or references the 'Charmed' effect/state. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Conditional_Displaceable` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Conditional_HasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Conditional_HasTag` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Conditional_HealthThreshold` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `Conditional_Object` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. |
| `Conditional_Speculative` | Block | `{ ... }` | A simulation block used by the AI to test hypothetical outcomes before committing to an action. |
| `Confusion` | Number | `1, 2` | Applies or references the 'Confusion' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `Consumed` | Block | `{ ... }` | State block triggered when this object or entity is eaten/consumed by another character. |
| `CritChanceUp` | Number | `5` | Applies or references the 'CritChanceUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `DoDamage` | Block | `{ ... }` | Explicitly triggers a secondary damage instance independent of the main attack. |
| `DodgeChance_Status` | Number | `5` | Applies or references the 'DodgeChance_Status' effect/state. |
| `DybbukPossessed` | Block | `{ ... }` | Defines the abilities and behaviors available when possessing another entity. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `ExplodeCharacter_Party` | Number | `5` | Applies or references the 'ExplodeCharacter_Party' effect/state. |
| `ExplodeCharacter` | Number | `5` | Applies or references the 'ExplodeCharacter' effect/state. |
| `FaceCamera` | Number | `1` | Applies or references the 'FaceCamera' effect/state. |
| `FlatAIBonus` | Number | `-999999` | Applies or references the 'FlatAIBonus' effect/state. |
| `ForceImmediateMove` | Number | `1` | Applies or references the 'ForceImmediateMove' effect/state. |
| `FormChange` | Enum/String | `LastHit, Nuke` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FullHeal` | Number | `1, 0` | Applies or references the 'FullHeal' effect/state. |
| `GainCoinsRange` | Block | `{ ... }` | Grants the player a randomized amount of coins within a min/max range. |
| `GainDisorderFromPool_PostCast` | Enum/String | `forbidden_spell_consequences_crippling` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |
| `GenericDebuff` | Number | `100` | Applies or references the 'GenericDebuff' effect/state. |
| `ImmediateUseAbility` | Enum/String | `tk_ButterBean_Normal` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Instakill` | Number | `25` | Applies or references the 'Instakill' effect/state. |
| `KnockUpAndAway` | Block | `{ ... }` | Displaces the target vertically and horizontally away from the source. |
| `Leeches` | Number | `2` | Applies or references the 'Leeches' effect/state. |
| `ObjectOnHitCharacter` | Enum/String | `Maggot` | Spawns a specific character or entity upon impact. |
| `OverrideDamage` | Number | `0` | Applies or references the 'OverrideDamage' effect/state. |
| `PartialCleanse` | Number | `1` | Applies or references the 'PartialCleanse' effect/state. |
| `PurgeAll` | Number | `1` | Applies or references the 'PurgeAll' effect/state. |
| `RandomStatDown` | String | `"ceil(X/2)", "ceil(X/3)"` | Applies or references the 'RandomStatDown' effect/state. |
| `RandomStatUp` | Number | `1, 2` | Applies or references the 'RandomStatUp' effect/state. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `RemoveMovePoints` | Number | `1` | Applies or references the 'RemoveMovePoints' effect/state. |
| `RemoveTurnsThisRound` | Number | `1` | Applies or references the 'RemoveTurnsThisRound' effect/state. |
| `Revive` | Number | `1, 100%` | Applies or references the 'Revive' effect/state. |
| `ScatterCoins` | Block | `{ ... }` | Throws coins out into the level randomly. |
| `SetHealth` | Number | `1` | Applies or references the 'SetHealth' effect/state. |
| `SetShield` | Number | `88` | Applies or references the 'SetShield' effect/state. |
| `ShowFakeDamage` | Block | `{ ... }` | Displays a visual damage number without actually modifying health. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `SpawnBearTrapIfHitKills` | Number | `1` | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. |
| `SpawnThingIfHitKills` | Enum/String | `Bait` | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| `SpeculativeMoveSelfCorpseOffMap` | Number | `1` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `VaporizeInanimate` | Number | `1` | Applies or references the 'VaporizeInanimate' effect/state. |
| `Vaporize` | Number | `1, 20` | Applies or references the 'Vaporize' effect/state. |
| `XIsTargetHealth` | Block | `{ ... }` | Math variable assignment: Evaluates X as the target's current health. |

### Context: `EvolveAbilityFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Enum/String | `Hunter, Thief, Mage` |  |
| `upgraded` | Boolean | `true` |  |

### Context: `FindItemFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.02, .15` | Probability of finding the item. |
| `pool` | Enum/String | `chapter` | The item pool to draw from. |

### Context: `ForceAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean | `true` |  |

### Context: `ForceImmediateMoveAndAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `G3GrabHead` | The ability to execute after moving. |
| `even_if_cant_reach` | Boolean | `true` | If true, executes the attack even if the move fails to reach the target. |

### Context: `ForceMoveTowardsTaggedObject`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MoveTwoTrample, MoveOneTrample` | The movement ability to use. |
| `tag` | Enum/String | `food` | The entity tag to seek out. |

### Context: `FormChange`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `30%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `form` | String | `"Rage", "Turtled", Rage` |  |

### Context: `GainCoinsRange`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `2, 4, 30` | Maximum coins granted. |
| `min` | Number | `1, 2, 10` | Minimum coins granted. |

### Context: `IncAuxCounterClamped`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `change` | Number | `-1, -2, -3` |  |
| `max` | Number | `3` |  |

### Context: `IncAuxCounterCycle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `change` | Number | `1` |  |
| `max` | Number | `3` |  |

### Context: `KnockOutCoin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.5` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `KnockUpAndAway`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `circular_variance` | Number | `2` |  |
| `distance` | Number | `2, -3, 3` | The distance in tiles to knock the target away. |
| `height` | Number | `2, 0` |  |
| `stacks` | Number | `1, 5, 5+bonus_melee_ability_damage` | Number of stacks or intensity to apply. |

### Context: `LateStatusApplication`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddWeaponAux` | Number | `2` | Applies or references the 'AddWeaponAux' effect/state. |
| `CurrentWeaponDamageUp` | Number | `1, 5` | Applies or references the 'CurrentWeaponDamageUp' effect/state. |

### Context: `LeaveBehind`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `Fly, CharmedMaggot, Twister` | The entity ID to spawn. |

### Context: `LowerAmbientLight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | Array | `[ 50% 60% 60% ]` | The target opacity/dimness level. |
| `speed` | Number | `4` | The transition speed. |

### Context: `Madness`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |
| `tickdown_this_turn` | Boolean | `true` |  |

### Context: `Math`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |

### Context: `MergeDamageInstance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | `false` | If false, prevents the damage from instantly popping the target. |
| `force_no_hit_animation` | Boolean | `true` | If true, suppresses the flinch/hit animation. |

### Context: `Metronome`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `banned_abilities` | Array | `[ BatteryNuke WeAreOne Metronome SmartMetronome BecomeEnt...` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `NextAttackSpecialCrit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | `2` | Flat addition to the critical damage multiplier. |
| `extra_coins_per_stack` | Number | `2` | Grants bonus coins based on stacks. |
| `luck_increase` | Number | `1` | Increases luck stat for the attack. |

### Context: `NextBasicAttackCritsThisTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` | If true, ensures the attack cannot be dodged. |
| `piercing` | Boolean | `true` | If true, the attack ignores armor. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `NextBattleStatusStacks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | `2` | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. |
| `fights` | Number | `9999` | The number of encounters this buff/debuff persists for. |

### Context: `NukeQuestFinalBossModifications`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage_instance` | Block | `{ ... }` |  |
| `self_damage` | Block | `{ ... }` | Recoil or self-inflicted damage/effects applied to the caster. |
| `splash_damage` | Block | `{ ... }` | Secondary Area of Effect blast parameters. |

### Context: `ObjectOnHit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `Poop` | The entity ID of the object to spawn (e.g., Poop). |

### Context: `ObjectOnHitCharacter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `1, .5` | Probability (0.0 to 1.0) of spawning. |
| `object` | Enum/String | `CharmedFlea` | The entity ID of the character to spawn (e.g., CharmedFlea). |

### Context: `OverHealToStatuses`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `stack_scale` | Number | `0` |  |

### Context: `PassiveWhileNotTakingTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |

### Context: `PoolMetronome`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Array | `[ Shockwave Ping Telefrag Stasis Reduce Zealot ]` | An array of ability IDs to randomly choose from. |

### Context: `PopAndSpawn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `clone_items` | Boolean | `false` | If true, transfers inventory to the new entity. |
| `clone_referenced_catdata` | Boolean | `true` | If true, copies the genetic data of the popped cat. |
| `no_splatter` | Boolean | `false` |  |
| `object` | Enum/String | `PlayerCat_ClotClone, BoyShade` | The entity ID to spawn in place. |

### Context: `QuakeAreaChance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | Probability of triggering the quake. |
| `radius` | Number | `1, 0` | The tile radius of the quake. |

### Context: `RandomDistanceDisplace`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `min_dist` | Number | `4` | The minimum tile distance they will be moved. |
| `stacks` | Number | `20` | Number of stacks or intensity to apply. |

### Context: `RandomKnockback`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `10, 3` | Maximum knockback distance. |
| `min` | Number | `1` | Minimum knockback distance. |

### Context: `RandomMagicMissile`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | `true` | If true, fires normal sized missiles instead of mini ones. |
| `stacks` | Number | `4, 3` | Number of stacks or intensity to apply. |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `BackflipWhenTargeted` | Number | `1` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BleedThorns` | Number | `1` | Applies or references the 'BleedThorns' effect/state. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `BonusDamage` | String | `"ceil(X/2)", -5, -4` | Applies or references the 'BonusDamage' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `Bruise` | Number | `1, 2` | Applies or references the 'Bruise' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Charge` | Number | `1, 8, 4` | Applies or references the 'Charge' effect/state. |
| `CharismaUp` | Number | `1` | Applies or references the 'CharismaUp' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `CritChanceUp` | Number | `1` | Applies or references the 'CritChanceUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `DelayedPain` | Number | `1` | Applies or references the 'DelayedPain' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `DiminishingHealthRegen` | Number | `1` | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `DodgeChance_Status` | Number | `1` | Applies or references the 'DodgeChance_Status' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `FormChange` | Block | `{ ... }` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `Freeze` | Number | `1` | Applies or references the 'Freeze' effect/state. |
| `GainCoins` | Number | `1, 5, -5` | Applies or references the 'GainCoins' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `Hex` | Number | `1` | Applies or references the 'Hex' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `IncAuxCounterClamped` | Block | `{ ... }` | Increments a generic auxiliary counter on the character, capped by a maximum value. |
| `Infested` | Number | `1` | Applies or references the 'Infested' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `KineticSpikes` | Number | `1` | Applies or references the 'KineticSpikes' effect/state. |
| `Lifesteal` | Number | `1` | Applies or references the 'Lifesteal' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `1, 2` | Applies or references the 'MagicWeakness' effect/state. |
| `ManaGain` | String | `"-ceil(X/2)", X` | Applies or references the 'ManaGain' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `MoveQuivered` | Number | `1` | Applies or references the 'MoveQuivered' effect/state. |
| `Ostracized` | Number | `1` | Applies or references the 'Ostracized' effect/state. |
| `Petrify` | Number | `1` | Applies or references the 'Petrify' effect/state. |
| `PoisonLace` | Number | `1` | Applies or references the 'PoisonLace' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `RandomStatDown` | Number | `1` | Applies or references the 'RandomStatDown' effect/state. |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `Reflect` | Number | `1` | Applies or references the 'Reflect' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `RefreshMovePoints` | Number | `1` | Applies or references the 'RefreshMovePoints' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `Scrambled` | Number | `2` | Applies or references the 'Scrambled' effect/state. |
| `Shield` | Number | `1, 2, 4` | Applies or references the 'Shield' effect/state. |
| `Sleep` | Number | `1` | Applies or references the 'Sleep' effect/state. |
| `Slow` | Number | `1, 2` | Applies or references the 'Slow' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `TempCounterAttack` | Number | `1` | Applies or references the 'TempCounterAttack' effect/state. |
| `Thorns` | Number | `1, 2` | Applies or references the 'Thorns' effect/state. |
| `Weakness` | Number | `1, 2` | Applies or references the 'Weakness' effect/state. |

### Context: `RemoveStatusStacks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | The number of stacks to remove. |
| `status` | Enum/String | `Brace` | The specific status effect ID to remove. |

### Context: `ReplaceSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `None, MoonHeadCommandStopHittingYourself` | The new ability ID to insert. |
| `slot` | Number | `1, 2, 0` | The spell slot index to replace. |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |

### Context: `ReviveNextRound`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, 2` | Applies or references the 'AllStatsUp' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `Shield` | Number | `15, 20` | Applies or references the 'Shield' effect/state. |
| `revive_health` | Number | `1, 100%, 50%` | The flat amount of health to revive with. |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

### Context: `ScatterCoins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | `true` | If true, multiple instances of this trigger can stack. |
| `stacks` | Enum/String | `item_aux, "max(min(X+1, item_aux), 0)"` | Number of stacks or intensity to apply. |

### Context: `ScrambleLastUsedSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | `true` | If true, the scramble persists for the rest of the run. |

### Context: `SetAnimationAlts`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `dead` | Enum/String | `deadShot` |  |
| `dying` | Enum/String | `shot` |  |

### Context: `SetCrazyEyeBackgroundWeights`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | Array | `[ 1 0 0 ], [ 0 0 1 ], [ 0 1 0 ]` |  |

### Context: `ShowFakeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `999` | Number of stacks or intensity to apply. |
| `style` | Array | `[ crit ]` | The visual font style for the text (e.g., [crit]). |

### Context: `SmartMetronome`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `20` | Number of stacks or intensity to apply. |
| `upgraded` | Boolean | `true` |  |

### Context: `SpreadDisease`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `30%` | Probability (0.0 to 1.0 or percentage) of transmitting. |
| `disease` | Enum/String | `Cancer` | The specific status effect ID representing the disease. |

### Context: `StatusGroup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DamageOrHealConditionally` | Number | `1` | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `Freeze` | Number | `2` | Applies or references the 'Freeze' effect/state. |

### Context: `StatusKillers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `10` | Applies or references the 'Confusion' effect/state. |

### Context: `StatusOnBattleEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | `3` | Applies or references the 'RandomMutation' effect/state. |
| `RandomTaggedMutation` | Enum/String | `bird, melted` | Applies or references the 'RandomTaggedMutation' effect/state. |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |

### Context: `SwapWeapon`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Array | `[ TerminatorShotgun TerminatorSniper TerminatorUzi ]` | An array of weapon item IDs to draw from. |

### Context: `SwitchMusic`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `crossfade_speed` | Number | `1` |  |
| `new_layer` | Enum/String | `map, battle, event` | The specific audio layer to transition to (e.g., map, battle). |
| `new_song` | Enum/String | `same` | The ID of the new music track. |

### Context: `TakeBonusTurnWithAIControl`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | `true` | If true, allows the AI to cast spells during this bonus turn. |

### Context: `TakeBonusTurnWithStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Stun` | Number | `1, [ 1 .75 ]` | Applies or references the 'Stun' effect/state. |
| `TempNoManaRegen` | Number | `1` | Applies or references the 'TempNoManaRegen' effect/state. |

### Context: `Tangled`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `alt_art` | Enum/String | `TangledMeat` | The alternative sprite art to use while tangled. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `TeamCastAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `CollectiveCounterImpl, CollectiveSpinImpl` | The underlying logic ability executed by the team. |
| `same_orientation` | Boolean | `true` |  |
| `tag_restriction` | Enum/String | `collective` | Requires participants to share this tag. |

### Context: `TempPassiveWhileHasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddManaRegen` | Number | `5` | Applies or references the 'AddManaRegen' effect/state. |
| `HealthRegenUp` | Number | `5` | Applies or references the 'HealthRegenUp' effect/state. |
| `MeleeRevengeDamage` | Block | `{ ... }` | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. |
| `ReplaceSpell` | Block | `{ ... }` | Replaces a spell in the character's hand/deck with a different one. |
| `status` | Enum/String | `Sleep, Consumed` | The required status effect. |

### Context: `Temporary`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `data` | Number | `2` |  |
| `expires_on_appliers_turn` | Boolean | `true` |  |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `expires_on_move` | Boolean | `true` |  |
| `stacks` | Number | `1, 5, 10` | Number of stacks or intensity to apply. |
| `status` | Enum/String | `AllDamageImmune, Brace, Thorns` | The status effect to apply. |
| `turns` | Number | `1, 3` | Duration in turns. |

### Context: `TimeDelayStatusApplication`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `CreateGlobalModifiers` | Block | `{ ... }` | Generates global map or encounter rules/modifiers. |
| `DoScreenShake` | Block | `{ ... }` | Triggers a camera screen shake effect. |
| `FormChange` | Enum/String | `DualSword` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `GlobalSpawnCharacter` | Enum/String | `MegaGuppy` | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `PlayBackground` | Number | `1` | Applies or references the 'PlayBackground' effect/state. |
| `RemoveAmbientLightEffects` | Enum/String | `.5` | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `SwitchMusic` | Block | `{ ... }` | Changes the background music track or layer during combat. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |
| `delay` | Number | `1.13333, .25, 3` | The float time delay in seconds. |

### Context: `TransformEquipment`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `from` | Enum/String | `JarOfChaos` | The original item ID. |
| `to` | Enum/String | `JarOfNothing` | The new item ID. |

### Context: `TransformWeapon`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `from` | Enum/String | `Necro_SoulDagger_Uncharged` | The original weapon ID. |
| `to` | Enum/String | `Necro_SoulDagger_Charged` | The transformed weapon ID. |

### Context: `TwisterDisplaceWithDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1, inherit` | The damage formula or inherit flag. |
| `exclude_prefix` | Enum/String | `Twister` |  |
| `max_dist` | Number | `2, 3, 20` | Maximum displacement distance. |
| `min_dist` | Number | `2, 3` | Minimum displacement distance. |

### Context: `UseAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `T3Pebbles_BoulderDrop` | The ID of the ability to trigger. |
| `respect_prime` | Boolean | `true` | If true, respects the ability's prime/cooldown state. |

### Context: `UseMoveAbilityWithAI`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `LEPortFar` | ID of the ability to trigger or reference. |
| `move_weights` | Enum/String | `stay_far_move_far` | The AI positioning logic profile to use. |

### Context: `VisualCountDownThenApplyStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `neck_NukeExplode` | Applies or references the 'ForceUseAbility' effect/state. |

### Context: `WaggleClone`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `1x1_object` | Enum/String | `cWaggle` | The 1x1 variant of the object. |
| `2x2_object` | Enum/String | `cWaggle2x2` | The 2x2 variant of the object. |
| `3x3_object` | Enum/String | `cWaggle3x3` | The 3x3 variant of the object. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

### Context: `XIsSpellStormRampAndReset`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | `50%` | The percentage of stacks to keep after resetting. |
| `stacks` | Number | `0` | Number of stacks or intensity to apply. |

### Context: `XIsTargetHealth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusDamage` | String | `"max(0, floor(X/6)-1)", "max(0, floor(X/2)-1)"` | Applies or references the 'BonusDamage' effect/state. |

### Context: `additional_passives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `ApplyPassivesToSpawnerWhileAlive` | Block | `{ ... }` | Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `FadeInsteadOfDie` | Number | `1` | Applies or references the 'FadeInsteadOfDie' effect/state. |
| `FillMana` | Number | `1` | Applies or references the 'FillMana' effect/state. |
| `HealthGain` | Number | `8` | Applies or references the 'HealthGain' effect/state. |
| `HideEquipment` | Enum/String | `neck` | Applies or references the 'HideEquipment' effect/state. |
| `IllusionTint` | Number | `1` | Applies or references the 'IllusionTint' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `ReviveNextRound` | Block | `{ ... }` | Queues the character to be resurrected at the start of the next combat round. |
| `SafeDoomed` | Number | `1, 2, level` | Applies or references the 'SafeDoomed' effect/state. |
| `SchizoIllusionAIModifier` | Number | `1` | Applies or references the 'SchizoIllusionAIModifier' effect/state. |
| `SpeedUp` | Number | `4` | Applies or references the 'SpeedUp' effect/state. |

### Context: `bonk_damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |

### Context: `bonus_passives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AbilityDisableIfLivingCrow` | Number | `1` | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. |
| `AbilityEnableIfConsumedCharacterHasTag` | Enum/String | `sp_pill_normal, sp_pill_tar, sp_pill_fire` | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. |
| `AbilityEnabledAtHealthThreshold` | Number | `50%` | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | `1` | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. |
| `AbilityEnabledIfHasStatus` | Enum/String | `DemonicGlyph_Summon, DemonicGlyph_Bite` | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. |
| `AbilityEnabledIfMovementTrapped` | Number | `1` | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. |
| `AbilityEnabledIfNoAggroTarget` | Number | `1` | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. |
| `AbilityEnabledIfNotHasStatus` | Enum/String | `BackflipWhenTargeted` | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. |
| `AbilityEnabledIfSpecificItemEquipped` | Enum/String | `Neverstone` | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | `16, 25%, 50%` | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. |
| `AbilityEnabledOncePerRound` | Number | `1` | Applies or references the 'AbilityEnabledOncePerRound' effect/state. |
| `AbilityEnabledPercentEachTurn` | Number | `25%, 35%, 50%` | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. |
| `AbilityInheritsWeaponEffects` | Number | `1, 2` | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. |
| `AbsorbManaFromOtherSpells` | Number | `1` | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. |
| `AddElementsToSpells` | Enum/String | `Earth` | Applies or references the 'AddElementsToSpells' effect/state. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `AlphaDodgeChance` | Number | `50%` | Applies or references the 'AlphaDodgeChance' effect/state. |
| `AlphaStatusOnTurnBegin` | Block | `{ ... }` | Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. |
| `AutocastEachRound` | Block | `{ ... }` | Forces the character to automatically cast a specific ability at the start of each combat round. |
| `BonusAbility_DelayedApplication` | Enum/String | `Slap` | Applies or references the 'BonusAbility_DelayedApplication' effect/state. |
| `CapTechSpent` | Number | `1` | Applies or references the 'CapTechSpent' effect/state. |
| `CatchBoomerang` | Number | `1` | Applies or references the 'CatchBoomerang' effect/state. |
| `CaveWomanBirthControl` | Number | `1` | Applies or references the 'CaveWomanBirthControl' effect/state. |
| `ChargeSpiritBombAura` | Enum/String | `DonateEnergy2, DonateEnergy` | Applies or references the 'ChargeSpiritBombAura' effect/state. |
| `CopyBasicAttackEffects` | Number | `1` | Applies or references the 'CopyBasicAttackEffects' effect/state. |
| `CopyCatPassive_Initializer` | Number | `1, 2` | Applies or references the 'CopyCatPassive_Initializer' effect/state. |
| `CritChanceUp` | Number | `25` | Applies or references the 'CritChanceUp' effect/state. |
| `DeadAltAbility` | Enum/String | `LifeDrain_Afterlife, CarrionShot_Afterlife, CarrionShot_Afterlife2` | Applies or references the 'DeadAltAbility' effect/state. |
| `DownRankAIIfWeaponUsable` | Enum/String | `.001` | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. |
| `FistOfFateUniqueEnemyTracker` | Number | `1` | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. |
| `FreeFirstCastAndAfterSpendMana` | Number | `1` | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. |
| `FreeFirstCastEachMatch` | Number | `1` | Applies or references the 'FreeFirstCastEachMatch' effect/state. |
| `FreeFirstCast` | Number | `1, 4` | Applies or references the 'FreeFirstCast' effect/state. |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `IntelligenceUp` | Number | `2` | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeDisabler` | Number | `1` | Applies or references the 'InterchangeDisabler' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `MoonHeadFinisherEnabler` | Number | `1, -1, 0` | Applies or references the 'MoonHeadFinisherEnabler' effect/state. |
| `NukeQuestFinalBossModifications` | Block | `{ ... }` | Special encounter trigger for the Nuke Quest ending. |
| `PassiveWhileNotTakingTurn` | Block | `{ ... }` | Grants nested passives that are only active while it is NOT the character's turn. |
| `ReloadOnAllyCatDies` | Number | `1` | Applies or references the 'ReloadOnAllyCatDies' effect/state. |
| `ReloadOnAllyDies` | Number | `1` | Applies or references the 'ReloadOnAllyDies' effect/state. |
| `ReloadOnAnyDamage` | Number | `1` | Applies or references the 'ReloadOnAnyDamage' effect/state. |
| `ReloadOnBackstab` | Number | `1` | Applies or references the 'ReloadOnBackstab' effect/state. |
| `ReloadOnElementalDamageReceived` | Enum/String | `Holy` | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. |
| `ReloadOnGainCoins` | Number | `1` | Applies or references the 'ReloadOnGainCoins' effect/state. |
| `ReloadOnGainDivineShield` | Number | `1` | Applies or references the 'ReloadOnGainDivineShield' effect/state. |
| `ReloadOnKillEnemy` | Number | `1` | Applies or references the 'ReloadOnKillEnemy' effect/state. |
| `ReloadOnKillTagged` | Enum/String | `rock` | Applies or references the 'ReloadOnKillTagged' effect/state. |
| `ReloadOnKill` | Number | `1` | Applies or references the 'ReloadOnKill' effect/state. |
| `ReloadOnSpendMana` | Number | `1` | Applies or references the 'ReloadOnSpendMana' effect/state. |
| `ReloadOnTotalDamageReceived` | Number | `25, 15` | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. |
| `ReloadOnUseAbilityWithManaCost` | Number | `6` | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. |
| `RevengeDamage` | Block | `{ ... }` | Reaction trigger: Deals damage to the attacker when hit. |
| `StatusKillers` | Block | `{ ... }` | Instantly kills the target if they possess the specified status effects. |
| `TossTargetIsAggroTarget` | Number | `1` | Applies or references the 'TossTargetIsAggroTarget' effect/state. |
| `TossTargetIsBuddy` | Number | `1` | Applies or references the 'TossTargetIsBuddy' effect/state. |
| `TossTargetIsNotInWater` | Number | `1` | Applies or references the 'TossTargetIsNotInWater' effect/state. |
| `Trample` | Number | `3` | Applies or references the 'Trample' effect/state. |
| `XIsConsumedCharacterMaxHP` | Number | `3` | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. |
| `XIsCountDeaths` | Number | `1` | Applies or references the 'XIsCountDeaths' effect/state. |
| `XIsCountStatusStacks` | Enum/String | `DodgeChance_Status` | Applies or references the 'XIsCountStatusStacks' effect/state. |
| `XIsFormulaLockedUntilComplete` | Enum/String | `dex` | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. |
| `XIsFreeArmorSlots` | Number | `1` | Applies or references the 'XIsFreeArmorSlots' effect/state. |
| `XIsIncreaseEachTurn` | Number | `1` | Applies or references the 'XIsIncreaseEachTurn' effect/state. |
| `XIsLivingAlliesWithTag` | Enum/String | `terminator_mini, hitler_clone_fetus, dc_crow` | Applies or references the 'XIsLivingAlliesWithTag' effect/state. |
| `XIsLivingCharactersWithTag` | Enum/String | `husk, rock` | Applies or references the 'XIsLivingCharactersWithTag' effect/state. |
| `XIsMultipliedPercentHealth` | Array | `[ 1 12 ], [ 14 1 ], [ 6 2 ]` | Applies or references the 'XIsMultipliedPercentHealth' effect/state. |
| `XIsOtherHealsThisTurn` | Number | `1` | Applies or references the 'XIsOtherHealsThisTurn' effect/state. |
| `XIsRampAndReset` | Number | `0` | Applies or references the 'XIsRampAndReset' effect/state. |
| `XIsRecycleCostReduction` | Number | `5` | Applies or references the 'XIsRecycleCostReduction' effect/state. |
| `XIsSpellStormRampAndReset` | Number | `0, { ... }` | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. |
| `XIsTimesDamageTaken` | Number | `1` | Applies or references the 'XIsTimesDamageTaken' effect/state. |

### Context: `cost`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `X_cant_be_zero` | Boolean | `true` | Applies or references the 'X_cant_be_zero' effect/state. |
| `act_points` | Number | `1, 0, 3` | Consumes primary action points (default 1). |
| `allow_offmap_casts` | Boolean | `true` | Can be used while the character is hidden/removed from grid. |
| `can_be_refreshed` | Boolean | `false` | Passives/Effects can reset this ability's cooldown. |
| `can_cast_while_dead` | Boolean | `true` | Usable by corpses (e.g., DeathRattle triggers). |
| `can_pay_over_multiple_turns` | Boolean | `true` | Allows channeling costs over time. |
| `can_self_refresh` | Boolean | `false` | The ability has mechanics to reset its own cooldown. |
| `cant_cast` | Enum/String | `X-5, false, true` | Explicitly disables casting (used for passive-triggered only abilities). |
| `cantrip_group` | Enum/String | `THC_CoinRoll, kaiju_roar, spewer_suck` | Groups cantrips so using one exhausts the others. |
| `cantrip` | Boolean | `false, true` | Does not end the turn when cast. |
| `charge` | Number | `1, "1-clamp(spd,0,1)", 0` | Cooldown timers measured in turns. |
| `coins` | Number | `1, 5, 7` | Consumes currency to cast. |
| `damage_cant_be_zero` | Boolean | `true` | Requires the ability to have >0 calculated damage to cast. |
| `disallow_cost_modification` | Boolean | `true` | Prevents passives from making this cheaper. |
| `durability` | Number | `0` | Consumes item durability. |
| `enabled_formula` | Number | `1, 1-X, X` | Mathematical string required to be >0 to cast. |
| `infcantrip` | Boolean | `false, true` | Can be cast infinitely as long as costs are met. |
| `initial_charge` | Number | `1` | How many turns it starts on cooldown at battle start. |
| `main_turn_only` | Boolean | `true` | Cannot be cast during bonus or dispersed turns. |
| `mana` | Number | `7, 5, 0` | MP pool and how much it restores per turn. |
| `manacost_cant_be_zero` | Boolean | `true` | Fails to cast if mana cost is reduced to 0. |
| `minimum_con` | Number | `1` | Stat thresholds required to cast. |
| `minimum_spd` | Number | `1` | Stat thresholds required to cast. |
| `move_points` | Number | `1, 0` | Consumes movement points. |
| `must_be_consuming` | Boolean | `true` | Requires the character to be eating/holding something. |
| `must_be_first_action` | Boolean | `false, true` | Can only be used at the very start of the turn. |
| `must_be_first_nonmove_action` | Boolean | `true` | Can move first, but cannot use other abilities first. |
| `must_be_offmap` | Boolean | `true` | Requires the character to be hidden/dug underground. |
| `must_have_weapon` | Boolean | `true` | Requires a weapon equipped in the item slot. |
| `must_not_be_a_summon` | Boolean | `true` | Summons/Familiars cannot cast this. |
| `must_not_be_consuming` | Boolean | `true` | Cannot be holding/eating an entity. |
| `once_per_fight` | Enum/String | `3-X, false, true` | Exhausts for the remainder of combat after one use. |
| `prime` | Number | `1` | Requires a "priming" turn before it fires. |
| `require_default_size` | Boolean | `true` | 2x2 or altered characters cannot cast this. |
| `requires_attack_damage_threshold` | Number | `2` | Needs a certain amount of innate damage. |
| `requires_consumed_trinket` | Boolean | `true` | Must have eaten a specific item type. |
| `requires_destructible_weapon` | Boolean | `true` | The equipped weapon must be breakable. |
| `requires_empty_trinket` | Boolean | `true` | Must not have an accessory equipped. |
| `requires_exact_character_aux` | Number | `1, 2, 0` | Hardcoded character specific lock. |
| `requires_hp_threshold` | Number | `200` | Must be below/above a certain health percentage. |
| `requires_reload` | Boolean | `true` | Must spend an action to reload before casting again. |
| `requires_weapon` | Boolean | `true` | Prerequisite: Must meet this condition. |
| `start_reloaded` | Boolean | `true` | Spawns with the ability pre-loaded. |

### Context: `damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `type` | Enum/String | `none` | Classification/category type. |

### Context: `damage_instance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | `2` | Modifies the target's native regeneration stat. |
| `accuracy` | Enum/String | `.5` | Hit chance modifier. |
| `ai_base_score` | Number | `1000, 9999, 999999` | How highly the AI values using this ability. |
| `blocked_damage` | Enum/String | `3+bonus_melee_ability_damage, 5+bonus_melee_damage, 7+bonus_melee_ability_damage` | Base damage dealt if the attack is blocked. |
| `blocked_multiplier` | Number | `2` | Multiplier applied when hitting a blocking target. |
| `can_collect_pickups` | Boolean | `true` | The damage instance can grab items on the ground. |
| `can_instapop` | Boolean | `false` | Allows the attack to instantly destroy specific weak entities. |
| `can_revive` | Boolean | `true` | Healing instance that can bring dead allies back to life. |
| `cant_miss` | Boolean | `true` | Guarantees the hit, bypassing dodge mechanics. |
| `contact_requires_adjacency` | Boolean | `false` | Contact effects only trigger if standing next to the target. |
| `crit_chance` | Number | `-999999, 100%, .5` | Override for base critical hit probability. |
| `custom_additional_ai_weight` | Enum/String | `toss_towards_buddy, prefer_dont_move, tile_close_to_enemy` | Granular AI preference adjustments (e.g., `prefer_dont_move`). |
| `damage_shield_only` | Boolean | `true` | Depletes shields but cannot harm base health. |
| `damage` | Number | `2, 0, 4` | The base damage properties of an attack. |
| `disallow_modifications` | Boolean | `true` | Prevents passives from altering this damage instance. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Gravity ], [ Holy ], [ Water ]` | Array of elemental tags to apply (e.g., `[Fire Holy]`). |
| `faction` | Enum/String | `auto` | Determines alignment (`enemies`, `cats`, `neutral`). |
| `final_hit_bonus_damage` | Enum/String | `5+bonus_melee_ability_damage` | Extra damage applied on the last hit of a multihit. |
| `force_adjacent_and_diagonal_contact` | Boolean | `true` | Treats diagonal hits as physical contact. |
| `force_no_contact` | Boolean | `true` | Bypasses all contact-based retaliation (Thorns, etc). |
| `force_no_knockback` | Boolean | `true` | Prevents the target from being pushed. |
| `force_play_hit_animation` | Boolean | `true` | Forces the flinch animation even on 0 damage. |
| `heal` | Number | `1, 4, 10` | Restores health instead of dealing damage. |
| `hint_dont_lowgravboost` | Boolean | `true` | AI hint to ignore wind physics. |
| `hit_animation_alt` | Enum/String | `catch` | Custom flinch animation for the target. |
| `incidentally_collects_pickups` | Boolean | `false, true` | Automatically grabs items in the AoE. |
| `knockback` | Number | `1, 5, "ceil(X*.25/5)"` | The base physics pushing power (in tiles). |
| `layer` | Enum/String | `characters, all, tiles` | Z-index targeting (e.g., `characters`, `self`). |
| `makes_contact` | Boolean | `false, true` | If false, explicitly avoids triggering contact-based passives. |
| `non_lethal` | Boolean | `true` | Reduces target to 1 HP but will never kill. |
| `override_trample_damage` | Boolean | `true` | Custom damage value for trample moves. |
| `piercing` | Boolean | `true` | Ignores a percentage of target defense/armor. |
| `ranged` | Boolean | `true` | Boolean flagging the damage as explicitly ranged. |
| `raw_damage` | Enum/String | `int, "(con+1)/2", "max((X-1)*2, 0)"` | Unmitigated, unscaled base numbers. |
| `raw_heal` | String | `"100-X", "(str+1)/2"` | Unmitigated, unscaled base numbers. |
| `show_damage_on_0` | Boolean | `true` | Forces the "-0" floater text to appear. |
| `two_way_contact` | Boolean | `true` | Both caster and target trigger contact effects on each other. |
| `type` | Enum/String | `melee, physical_spell, status_spell` | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). |

### Context: `damage_threshold_altanimations`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Number | `20` | Animation trigger for massive damage. |
| `heavyMelee` | Number | `10` | Animation trigger if damage exceeds this threshold. |

### Context: `effects`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AIFavorLowHealth` | Number | `100` | Applies or references the 'AIFavorLowHealth' effect/state. |
| `AddSpiritBombCharges` | Number | `1, 2` | Applies or references the 'AddSpiritBombCharges' effect/state. |
| `AllStatsUp` | Enum/String | `item_aux, 1, -1` | Applies or references the 'AllStatsUp' effect/state. |
| `AlliesTakeExtraTurn` | Number | `1` | Applies or references the 'AlliesTakeExtraTurn' effect/state. |
| `AlphaCat` | Number | `1` | Applies or references the 'AlphaCat' effect/state. |
| `AlternateIdleAnimation` | Enum/String | `berserkIdle` | Applies or references the 'AlternateIdleAnimation' effect/state. |
| `Ammo` | Number | `-99999, -1, 6` | Applies or references the 'Ammo' effect/state. |
| `ApplyMultipleTimes` | Block | `{ ... }` | A loop block that executes its nested logic multiple times. |
| `ApplyPassives` | Block | `{ ... }` | Grants the nested passive abilities dynamically. |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | `1` | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. |
| `ApplyStatusIfCrit` | Block | `{ ... }` | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. |
| `ApplyStatusesNextTurnBegin` | Block | `{ ... }` | Delays the application of the nested status effects until the start of the target's next turn. |
| `ApplyToConsumed` | Block | `{ ... }` | Redirects the nested effects to apply to the entity that just consumed this object. |
| `ApplyToOthersWithSharedTagAndFaction` | Block | `{ ... }` | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. |
| `ApplyToRandomClosestAlly` | Block | `{ ... }` | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. |
| `ApplyToSourceOnKill` | Block | `{ ... }` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `ArcLightning` | Block | `{ ... }` | Executes a chain-lightning logic block that bounces between targets. |
| `Attraction` | Number | `1` | Applies or references the 'Attraction' effect/state. |
| `BackflipWhenTargeted` | Number | `1, 2, { ... }` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `Bleed` | Number | `1, 2, 10` | Applies or references the 'Bleed' effect/state. |
| `Blind` | Number | `1, [ 1 .25 ], [ 2 .33 ]` | Applies or references the 'Blind' effect/state. |
| `Bloodzerked` | Number | `1` | Applies or references the 'Bloodzerked' effect/state. |
| `BodyGuard` | Block | `{ ... }` | Protects an ally by intercepting attacks directed at them. |
| `BombRatTurtle` | Number | `1` | Applies or references the 'BombRatTurtle' effect/state. |
| `BonusDamageBasedOnMana` | Number | `1` | Applies or references the 'BonusDamageBasedOnMana' effect/state. |
| `BonusKnockbackDamage` | Number | `2` | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `BounceObject` | Enum/String | `CharmedDip, SmallRock, CharmedFlea` | Spawns a physics object that visually bounces off the target. |
| `BounceRock` | Enum/String | `SmallLavaRock, SmallRock, [ 1 .2 ]` | Applies or references the 'BounceRock' effect/state. |
| `Bound` | Number | `3` | Applies or references the 'Bound' effect/state. |
| `Brace` | Number | `1, 2, 4` | Applies or references the 'Brace' effect/state. |
| `BramblesOnHit` | Number | `1` | Applies or references the 'BramblesOnHit' effect/state. |
| `Bruise` | Number | `5, 1, 2` | Applies or references the 'Bruise' effect/state. |
| `BurgleCoin` | Number | `1, 3, [ 1 .5 ]` | Applies or references the 'BurgleCoin' effect/state. |
| `Burn` | Number | `1, 2, 3` | Applies or references the 'Burn' effect/state. |
| `BypassRockKnockback` | Number | `1` | Applies or references the 'BypassRockKnockback' effect/state. |
| `CanApplyToInanimate` | Block | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `CancelPrimedAbilities` | Number | `1` | Applies or references the 'CancelPrimedAbilities' effect/state. |
| `CanceledQueuedInput` | Number | `1` | Applies or references the 'CanceledQueuedInput' effect/state. |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `CatPartsSizeScaleStatus` | Block | `{ ... }` | Visually scales specific body parts of a character. |
| `CatPartsTransform` | Block | `{ ... }` | Transforms specific body parts into different visual variants. |
| `ChampionUpgradeNextMinion` | Number | `1` | Applies or references the 'ChampionUpgradeNextMinion' effect/state. |
| `ChanceToBreakFree` | Block | `{ ... }` | Provides a probability to escape a grapple or restraining effect. |
| `ChanceToBreak` | Number | `5, 15, 20` | Applies or references the 'ChanceToBreak' effect/state. |
| `ChangeCatClass` | Enum/String | `Hunter, Fighter, Mage` | Applies or references the 'ChangeCatClass' effect/state. |
| `ChangeFaction` | Enum/String | `sabertooths` | Applies or references the 'ChangeFaction' effect/state. |
| `ChangeTile` | Enum/String | `LavaTile, FireTile, WaterTile` | Transforms the terrain tile under the target. |
| `ChangeTilesUnder` | Enum/String | `DirtTile` | Applies or references the 'ChangeTilesUnder' effect/state. |
| `ChaosBossFlipMidTeleport` | Number | `1` | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. |
| `ChaosBossFormChange` | Number | `1` | Applies or references the 'ChaosBossFormChange' effect/state. |
| `ChargeFists` | Number | `1` | Applies or references the 'ChargeFists' effect/state. |
| `Charge` | Number | `1, 2` | Applies or references the 'Charge' effect/state. |
| `CharismaUp` | Enum/String | `item_aux, 1, -2` | Applies or references the 'CharismaUp' effect/state. |
| `CharmedFacingForceAttack` | Number | `1` | Applies or references the 'CharmedFacingForceAttack' effect/state. |
| `CharmedForceAttack` | Number | `1` | Applies or references the 'CharmedForceAttack' effect/state. |
| `Charmed` | Number | `1, [ 1, .1+.02*cha ], level` | Applies or references the 'Charmed' effect/state. |
| `Cleanse` | Number | `1, 0` | Applies or references the 'Cleanse' effect/state. |
| `ClearFinalBossBattlefield` | Number | `1` | Applies or references the 'ClearFinalBossBattlefield' effect/state. |
| `ClearStarving` | Number | `1` | Applies or references the 'ClearStarving' effect/state. |
| `Cleave` | Number | `1, { ... }` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `CloneWeaponTemp` | Number | `1` | Applies or references the 'CloneWeaponTemp' effect/state. |
| `CoinTossBounce` | Enum/String | `X` | Applies or references the 'CoinTossBounce' effect/state. |
| `CollectsPickupsWithAltEffects` | Block | `{ ... }` | Triggers alternative nested effects when collecting items or pickups. |
| `CollectsPickups` | Number | `1, 2` | Applies or references the 'CollectsPickups' effect/state. |
| `CollideWithConsumed` | Enum/String | `1+bonus_melee_damage, 5+bonus_melee_damage, 4+bonus_melee_damage` | Applies or references the 'CollideWithConsumed' effect/state. |
| `CollideWithThrowTarget` | Number | `0` | Applies or references the 'CollideWithThrowTarget' effect/state. |
| `Conditional_AbilityTargetIsSelf` | Block | `{ ... }` | Conditional constraint. Nested properties only trigger if this is true. |
| `Conditional_ActiveWeather_Any` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the current map weather matches any in the list. |
| `Conditional_AffectedByElement` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. |
| `Conditional_Ally` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `Conditional_Backstab` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. |
| `Conditional_BadRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. |
| `Conditional_BossOrBig` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. |
| `Conditional_Boss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a Boss. |
| `Conditional_Buddy` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. |
| `Conditional_CanBeHealed` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. |
| `Conditional_Corpse` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| `Conditional_DebuffRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized debuff probability. |
| `Conditional_DestructibleCorpse` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. |
| `Conditional_Displaceable` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. |
| `Conditional_Enemy` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `Conditional_Familiar` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a familiar. |
| `Conditional_FirstApplicationThisTurn` | Block | `{ ... }` | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. |
| `Conditional_FormulaIsPositive` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Conditional_HasCleansableDebuffs` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. |
| `Conditional_HasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Conditional_HasTag` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Conditional_HealthThreshold` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `Conditional_InForm` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. |
| `Conditional_IsSelf` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is the caster themselves. |
| `Conditional_IsTrample` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. |
| `Conditional_LastHit` | Block | `{ ... }` | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. |
| `Conditional_LivingPlayerCat` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. |
| `Conditional_NotAlly` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. |
| `Conditional_NotBig` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is NOT classified as large. |
| `Conditional_NotBossOrBig` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. |
| `Conditional_NotBoss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| `Conditional_NotShielded` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. |
| `Conditional_Object` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. |
| `Conditional_OncePerBattle` | Block | `{ ... }` | Conditional trigger: Executes nested logic only once per encounter/battle. |
| `Conditional_PlayerCat` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a player-controlled cat. |
| `Conditional_RandomChance` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a flat percentage random roll. |
| `Conditional_Shielded` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has a Shield status. |
| `Conditional_SourceAbilityHasTag` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. |
| `Conditional_SourceHasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the caster currently has the specified status. |
| `Conditional_Speculative` | Block | `{ ... }` | A simulation block used by the AI to test hypothetical outcomes before committing to an action. |
| `Confusion` | Number | `1, 2, 4` | Applies or references the 'Confusion' effect/state. |
| `ConjureBonusAbility` | Enum/String | `Colorless, random, { ... }` | Adds a temporary bonus ability to the character's hand/deck. |
| `ConjureSingleUseBonusAbility` | Enum/String | `random` | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. |
| `ConstitutionUp` | Number | `1, -1, [ 1 .5 ]` | Applies or references the 'ConstitutionUp' effect/state. |
| `Consumed` | Block | `{ ... }` | State block triggered when this object or entity is eaten/consumed by another character. |
| `ContextualHeal` | Number | `1` | Applies or references the 'ContextualHeal' effect/state. |
| `CopySpells` | Number | `1, { ... }` | Duplicates existing spells currently in the character's hand. |
| `CorpseVaporizer` | Number | `1` | Applies or references the 'CorpseVaporizer' effect/state. |
| `Counterspell` | Number | `1` | Applies or references the 'Counterspell' effect/state. |
| `Craft` | Block | `{ ... }` | Synthesizes or spawns a new item from a specific pool. |
| `CreateGlobalModifiers` | Block | `{ ... }` | Generates global map or encounter rules/modifiers. |
| `CritChanceUp` | Number | `2` | Applies or references the 'CritChanceUp' effect/state. |
| `CurrentWeaponAddElectricElement` | Number | `1` | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. |
| `CurrentWeaponDamageUp` | Number | `1, 3` | Applies or references the 'CurrentWeaponDamageUp' effect/state. |
| `DamageBasedOnMissingHealth` | Number | `25, 50` | Applies or references the 'DamageBasedOnMissingHealth' effect/state. |
| `DamageDistanceAOEFalloff` | Number | `1, 2` | Applies or references the 'DamageDistanceAOEFalloff' effect/state. |
| `DamageOrHealConditionally` | Number | `1` | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `DamageTrinket` | Number | `1` | Applies or references the 'DamageTrinket' effect/state. |
| `DamageUp` | Number | `1, -1, -2` | Applies or references the 'DamageUp' effect/state. |
| `DamageWeapon` | Number | `1` | Applies or references the 'DamageWeapon' effect/state. |
| `DeathwormUnderground` | Enum/String | `DeathWormEat` | Applies or references the 'DeathwormUnderground' effect/state. |
| `DecoySwapper` | Number | `1` | Applies or references the 'DecoySwapper' effect/state. |
| `DeferVaporize` | Number | `1` | Applies or references the 'DeferVaporize' effect/state. |
| `DelayCastAbility` | Block | `{ ... }` | Queues an ability to be cast automatically after a certain delay or trigger. |
| `DelayedFury` | Number | `75, 0` | Applies or references the 'DelayedFury' effect/state. |
| `DelayedWindCone` | Block | `{ ... }` | Creates a delayed Area of Effect cone. |
| `DeleteObject` | Number | `1` | Applies or references the 'DeleteObject' effect/state. |
| `DeleteTraps` | Number | `1` | Applies or references the 'DeleteTraps' effect/state. |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DestroyNeckArmor` | Number | `1` | Applies or references the 'DestroyNeckArmor' effect/state. |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |
| `DestroyWeaponThrow` | Number | `1` | Applies or references the 'DestroyWeaponThrow' effect/state. |
| `DestroyWeapon` | Number | `1` | Applies or references the 'DestroyWeapon' effect/state. |
| `DexterityUp` | Enum/String | `item_aux, 1, 2` | Applies or references the 'DexterityUp' effect/state. |
| `DieViaAbilityInternally` | Number | `1` | Applies or references the 'DieViaAbilityInternally' effect/state. |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |
| `DiminishingHealthRegen` | Number | `2, 3` | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DinoLegAnimation` | Enum/String | `poop` | Applies or references the 'DinoLegAnimation' effect/state. |
| `Disguised` | Number | `1` | Applies or references the 'Disguised' effect/state. |
| `DisplaceToOriginalPosition` | Number | `1` | Applies or references the 'DisplaceToOriginalPosition' effect/state. |
| `DisplaceTowardsSource` | Number | `1` | Applies or references the 'DisplaceTowardsSource' effect/state. |
| `Displace` | Number | `1` | Applies or references the 'Displace' effect/state. |
| `DissolveRandomArmorPiece` | Number | `1` | Applies or references the 'DissolveRandomArmorPiece' effect/state. |
| `DivineShield` | Number | `1, 2, 4` | Applies or references the 'DivineShield' effect/state. |
| `DoDistortionRing` | Block | `{ ... }` | Creates a visual distortion ring effect on the screen. |
| `DoScreenShake` | Number | `1, { ... }` | Triggers a camera screen shake effect. |
| `DodgeChance_Status` | Number | `10, 50, 20` | Applies or references the 'DodgeChance_Status' effect/state. |
| `DontHealEnemies` | Number | `1` | Applies or references the 'DontHealEnemies' effect/state. |
| `Doomed` | Number | `1, 2, 3` | Applies or references the 'Doomed' effect/state. |
| `DoubleCastSpell` | Number | `1` | Applies or references the 'DoubleCastSpell' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number | `1` | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. |
| `DoubleCast` | Number | `1` | Applies or references the 'DoubleCast' effect/state. |
| `DoubleLoot` | Number | `1, 2` | Applies or references the 'DoubleLoot' effect/state. |
| `DoubleStatus` | Enum/String | `Burn, Poison, Bleed` | Applies or references the 'DoubleStatus' effect/state. |
| `DrainAllyCatsForFleshGolem` | Number | `7` | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. |
| `DrinkWater` | Number | `1` | Applies or references the 'DrinkWater' effect/state. |
| `Drowsy` | Number | `1, 8` | Applies or references the 'Drowsy' effect/state. |
| `DuplicateRandomEquippedItem` | Number | `1` | Applies or references the 'DuplicateRandomEquippedItem' effect/state. |
| `DustOnHit` | Block | `{ ... }` | Spawns a specific particle or cloud object upon impact. |
| `EliteUpgradeNextMinion` | Number | `1` | Applies or references the 'EliteUpgradeNextMinion' effect/state. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `EmptyMind` | Number | `1` | Applies or references the 'EmptyMind' effect/state. |
| `EnableWeather` | Enum/String | `KaijuMeteornado, KaijuFirestorm, KaijuMeteornadoSolo` | Applies or references the 'EnableWeather' effect/state. |
| `EndTurn` | Number | `1` | Applies or references the 'EndTurn' effect/state. |
| `Enlarge` | Number | `3` | Applies or references the 'Enlarge' effect/state. |
| `EnterMount` | Enum/String | `enter` | Applies or references the 'EnterMount' effect/state. |
| `EvolveAbilityFromPool` | Enum/String | `Fighter, Mage, { ... }` | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `ExistUntilIdleUpkeep` | Number | `1` | Applies or references the 'ExistUntilIdleUpkeep' effect/state. |
| `ExplodeCharacter_DeathBloom2` | Number | `5` | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. |
| `ExplodeCharacter_DeathBloom` | Number | `5` | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. |
| `ExplodeCharacter_NoDie` | Number | `1` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. |
| `ExplodeCharacter` | Number | `5` | Applies or references the 'ExplodeCharacter' effect/state. |
| `ExplosionIfHitSomething` | Number | `5` | Applies or references the 'ExplosionIfHitSomething' effect/state. |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `FaceAway` | Number | `1` | Applies or references the 'FaceAway' effect/state. |
| `FaceCamera` | Number | `1` | Applies or references the 'FaceCamera' effect/state. |
| `FactionConversion` | Number | `1` | Applies or references the 'FactionConversion' effect/state. |
| `FactionDisguiseSource` | Number | `1` | Applies or references the 'FactionDisguiseSource' effect/state. |
| `FastKnockback` | Number | `4` | Applies or references the 'FastKnockback' effect/state. |
| `Fear` | Number | `1, 2, [ 1 .25 ]` | Applies or references the 'Fear' effect/state. |
| `FillMana` | Number | `1` | Applies or references the 'FillMana' effect/state. |
| `FinalBossQueueBeam` | Number | `1` | Applies or references the 'FinalBossQueueBeam' effect/state. |
| `FireArmor2` | Number | `1` | Applies or references the 'FireArmor2' effect/state. |
| `FireArmor` | Number | `1` | Applies or references the 'FireArmor' effect/state. |
| `FlatAIBonus` | Number | `999999` | Applies or references the 'FlatAIBonus' effect/state. |
| `FlatLeech` | Number | `2, 10` | Applies or references the 'FlatLeech' effect/state. |
| `FlowersOnHit` | Number | `1` | Applies or references the 'FlowersOnHit' effect/state. |
| `ForceAttack` | Number | `1, { ... }` | Forces the character to execute an immediate attack. |
| `ForceCollectsPickups` | Number | `1` | Applies or references the 'ForceCollectsPickups' effect/state. |
| `ForceDisplace` | Number | `1` | Applies or references the 'ForceDisplace' effect/state. |
| `ForceMoveAndAttack` | Number | `1` | Applies or references the 'ForceMoveAndAttack' effect/state. |
| `ForceMoveAway` | Number | `1` | Applies or references the 'ForceMoveAway' effect/state. |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | `4, 3` | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. |
| `ForceMoveTowardsEnemies` | Number | `1, MoveOne, DumbMove_Impl` | Applies or references the 'ForceMoveTowardsEnemies' effect/state. |
| `ForceMoveTowardsTaggedObject` | Block | `{ ... }` | Forces the character to move towards the nearest object with a specific tag. |
| `ForceMoveTowards` | Number | `1` | Applies or references the 'ForceMoveTowards' effect/state. |
| `ForceTransferWeapon` | Number | `1` | Applies or references the 'ForceTransferWeapon' effect/state. |
| `ForceUseAbility` | Enum/String | `MotherTumorGrow` | Applies or references the 'ForceUseAbility' effect/state. |
| `FormChange` | Enum/String | `Explosive, DualSword, Holy` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FreeSpell` | Number | `1` | Applies or references the 'FreeSpell' effect/state. |
| `Freeze` | Number | `1, [ 1 .1 ], [ 1 .25 ]` | Applies or references the 'Freeze' effect/state. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `GainCoinsRange` | Block | `{ ... }` | Grants the player a randomized amount of coins within a min/max range. |
| `GenericBuff` | Number | `100` | Applies or references the 'GenericBuff' effect/state. |
| `GenericDebuff` | Number | `1, 999, 100` | Applies or references the 'GenericDebuff' effect/state. |
| `GiveBoundItemToTarget` | Number | `1` | Applies or references the 'GiveBoundItemToTarget' effect/state. |
| `GlobalSpawnCharacter` | Enum/String | `MegaGuppy` | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `Grappled` | Number | `1` | Applies or references the 'Grappled' effect/state. |
| `HealPercentMaxHP` | Number | `100` | Applies or references the 'HealPercentMaxHP' effect/state. |
| `HealRandomInjury` | Number | `1` | Applies or references the 'HealRandomInjury' effect/state. |
| `HealTo` | Number | `50%` | Applies or references the 'HealTo' effect/state. |
| `HealthGain` | Number | `5, 4` | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | `1, 2, 3` | Applies or references the 'HealthRegenUp' effect/state. |
| `HeavyHits` | Number | `1` | Applies or references the 'HeavyHits' effect/state. |
| `Hex` | Number | `1` | Applies or references the 'Hex' effect/state. |
| `HitExplosion` | Number | `5` | Applies or references the 'HitExplosion' effect/state. |
| `IceArmor` | Number | `1` | Applies or references the 'IceArmor' effect/state. |
| `IgnoreDamage` | Number | `1` | Applies or references the 'IgnoreDamage' effect/state. |
| `IgnoreDebuffs` | Number | `1` | Applies or references the 'IgnoreDebuffs' effect/state. |
| `IgnoreSelf` | Number | `1, true` | Applies or references the 'IgnoreSelf' effect/state. |
| `ImmediateUseAbility` | Enum/String | `cm_Lard_Impl, HitlerCloneTransform` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `ImmediateUseDirectionalAbility` | Enum/String | `BowlDash, BowlDash2` | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. |
| `Immobile` | Number | `1, 2, 0` | Applies or references the 'Immobile' effect/state. |
| `Imprison` | Enum/String | `BeefyCharmedLeech, CharmedLeech, Tumor` | Applies or references the 'Imprison' effect/state. |
| `IncAuxCounterCycle` | Block | `{ ... }` | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. |
| `IncreaseCumulativeBlastDamage` | Number | `1` | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. |
| `IncreaseItemAuxOnKill` | Number | `1` | Applies or references the 'IncreaseItemAuxOnKill' effect/state. |
| `Infested` | Number | `1` | Applies or references the 'Infested' effect/state. |
| `Instakill` | Number | `25, 50` | Applies or references the 'Instakill' effect/state. |
| `InstantMaxHealthUp` | Number | `4, 20` | Applies or references the 'InstantMaxHealthUp' effect/state. |
| `IntelligenceUp` | Enum/String | `item_aux, 1, -int` | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeMoveActPoints` | Number | `1` | Applies or references the 'InterchangeMoveActPoints' effect/state. |
| `Invulnerable` | Number | `1` | Applies or references the 'Invulnerable' effect/state. |
| `JohnnyCriesForWashers` | Number | `1, 2` | Applies or references the 'JohnnyCriesForWashers' effect/state. |
| `KineticSpikes` | Number | `1, 2` | Applies or references the 'KineticSpikes' effect/state. |
| `KnockOutCoin` | Number | `1, { ... }` | Forces the target to drop coins. |
| `KnockUpAndAway` | Block | `{ ... }` | Displaces the target vertically and horizontally away from the source. |
| `KnockbackDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. |
| `KnockbackDirectionIsFacingDirection` | Enum/String | `rotate_right, 1, flip` | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. |
| `Knockback` | Number | `1, 5` | Applies or references the 'Knockback' effect/state. |
| `LateStatusApplication` | Block | `{ ... }` | Applies a status effect after all primary damage and effects have fully resolved. |
| `LeaveBehindRockOnKnockback` | Number | `1` | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |
| `Leeches` | Number | `1, 2, 3` | Applies or references the 'Leeches' effect/state. |
| `Lifesteal` | Number | `1, 3` | Applies or references the 'Lifesteal' effect/state. |
| `LuckUp` | Enum/String | `item_aux, 1, -2` | Applies or references the 'LuckUp' effect/state. |
| `MadnessChanceOnTurnBegin` | Number | `2` | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. |
| `Madness` | Number | `1, 999, 3` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `1, [ 1 .1 ], 4` | Applies or references the 'MagicWeakness' effect/state. |
| `MakeWeaponUnbreakable` | Number | `1` | Applies or references the 'MakeWeaponUnbreakable' effect/state. |
| `ManaGain` | Number | `5, 10, "max((X-1)*2, 0)"` | Applies or references the 'ManaGain' effect/state. |
| `ManaLeeches` | Number | `1, 2` | Applies or references the 'ManaLeeches' effect/state. |
| `ManaStealToHealth` | Number | `-1` | Applies or references the 'ManaStealToHealth' effect/state. |
| `ManaSteal` | Number | `5, -1` | Applies or references the 'ManaSteal' effect/state. |
| `ManglerAttack` | Number | `1` | Applies or references the 'ManglerAttack' effect/state. |
| `ManglerShuffle` | Boolean | `false` | Applies or references the 'ManglerShuffle' effect/state. |
| `Marked` | Number | `1, 5, [ 1 .1 ]` | Applies or references the 'Marked' effect/state. |
| `MassAttackThis` | Number | `1` | Applies or references the 'MassAttackThis' effect/state. |
| `Math` | Block | `{ ... }` | Triggers the Tinkerer's Math ability sequence. |
| `MaxHPUp` | Number | `100` | Applies or references the 'MaxHPUp' effect/state. |
| `Meaty` | Number | `1` | Applies or references the 'Meaty' effect/state. |
| `Metronome` | Number | `1, 2, { ... }` | Executes a random musical or metronome ability. |
| `MimicMetronome` | Number | `1` | Applies or references the 'MimicMetronome' effect/state. |
| `MonkStanceSwitch` | Number | `1` | Applies or references the 'MonkStanceSwitch' effect/state. |
| `MotherTumorDebugForcePass` | Number | `1` | Applies or references the 'MotherTumorDebugForcePass' effect/state. |
| `MoveQuivered` | Number | `1` | Applies or references the 'MoveQuivered' effect/state. |
| `MovementUp` | Number | `1, 2, -2` | Applies or references the 'MovementUp' effect/state. |
| `Muted` | Number | `1` | Applies or references the 'Muted' effect/state. |
| `NextAbilityHeals` | Number | `1` | Applies or references the 'NextAbilityHeals' effect/state. |
| `NextActionLuckUp` | Number | `99` | Applies or references the 'NextActionLuckUp' effect/state. |
| `NextAttackBonusRange` | Number | `1, 5, 3` | Applies or references the 'NextAttackBonusRange' effect/state. |
| `NextAttackSpecialCrit` | Number | `1, { ... }` | Modifies the character's next attack to have special critical properties. |
| `NextBasicAttackCritsThisTurn` | Block | `{ ... }` | Guarantees the next basic attack executed this turn will be a critical hit. |
| `NextBattleStatusStacks` | Block | `{ ... }` | Carries over the specified status effects into the next encounter/battle. |
| `NextDamageReduceAndHealAllies` | Number | `1` | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. |
| `NextTurnDoubleRangedDamage` | Number | `1` | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. |
| `NonStackingDivineShield` | Number | `1` | Applies or references the 'NonStackingDivineShield' effect/state. |
| `ObjectOnHitCharacter` | Enum/String | `SmallRock, SkeletonCatFamiliar, { ... }` | Spawns a specific character or entity upon impact. |
| `ObjectOnHitEmpty` | Enum/String | `SmallRock, AnimalEgg, AnimalEgg2` | Applies or references the 'ObjectOnHitEmpty' effect/state. |
| `ObjectOnHitFullyEmpty` | Enum/String | `RandomArmorPickup` | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. |
| `ObjectOnHit` | Enum/String | `FetusNoJar, BiggestFood, { ... }` | Spawns a specific physics/item object upon impact. |
| `Ostracized` | Number | `2, 4` | Applies or references the 'Ostracized' effect/state. |
| `OverHealToShield` | Number | `1` | Applies or references the 'OverHealToShield' effect/state. |
| `OverHealToStatuses` | Block | `{ ... }` | Converts excessive healing beyond maximum health into specific status effects. |
| `OverrideChainKnockbackDamage` | Enum/String | `3+bonus_melee_ability_damage` | Applies or references the 'OverrideChainKnockbackDamage' effect/state. |
| `OverrideChainKnockback` | Number | `1, 10, 3` | Applies or references the 'OverrideChainKnockback' effect/state. |
| `OverrideDamage` | Number | `0` | Applies or references the 'OverrideDamage' effect/state. |
| `OverrideKnockbackDamage` | Number | `0, 3, str` | Applies or references the 'OverrideKnockbackDamage' effect/state. |
| `PartialCleanse` | Number | `1, 9999` | Applies or references the 'PartialCleanse' effect/state. |
| `PartialPurge` | Number | `1` | Applies or references the 'PartialPurge' effect/state. |
| `PermanentCharisma` | Number | `2` | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentConstitution` | Number | `2, -1, -2` | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Number | `2` | Applies or references the 'PermanentDexterity' effect/state. |
| `PermanentImmobile` | Number | `1` | Applies or references the 'PermanentImmobile' effect/state. |
| `PermanentIntelligence` | Number | `2` | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Number | `2` | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentSpeed` | Number | `2` | Applies or references the 'PermanentSpeed' effect/state. |
| `PermanentStrength` | Number | `1, 2` | Applies or references the 'PermanentStrength' effect/state. |
| `PermanentUpgradeRandomActiveOrPassive` | Number | `1` | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. |
| `PermanentUpgradeRandomActive` | Number | `1, 4` | Applies or references the 'PermanentUpgradeRandomActive' effect/state. |
| `Petrify` | Number | `1, [ 1 .1 ], [ 1, .1 ]` | Applies or references the 'Petrify' effect/state. |
| `PlayBackground` | Number | `1, 0` | Applies or references the 'PlayBackground' effect/state. |
| `PoisonLace` | Number | `1, "X/5", "X/3"` | Applies or references the 'PoisonLace' effect/state. |
| `Poison` | Number | `2, 4, 3` | Applies or references the 'Poison' effect/state. |
| `PoolMetronome` | Block | `{ ... }` | Executes a random ability drawn from a specific pool. |
| `PopAndSpawn` | Enum/String | `TheDestroyer, Tormentor, StemCat_HalfHealth` | Destroys the target and replaces it with a new spawned entity. |
| `Possessed` | Number | `1` | Applies or references the 'Possessed' effect/state. |
| `ProbeCharmed` | Number | `1` | Applies or references the 'ProbeCharmed' effect/state. |
| `PullSourceToKnockbackImmuneTarget` | Number | `1` | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. |
| `PullSourceToTarget` | Number | `1` | Applies or references the 'PullSourceToTarget' effect/state. |
| `PurgeAll` | Number | `1` | Applies or references the 'PurgeAll' effect/state. |
| `Purge` | Number | `0, 3` | Applies or references the 'Purge' effect/state. |
| `QuakeAreaChance` | Block | `{ ... }` | Provides a probability to trigger an earthquake Area of Effect. |
| `QueueUseAbility` | Enum/String | `Spider_GoInsane` | Applies or references the 'QueueUseAbility' effect/state. |
| `RNGCannonRandomDamage` | Number | `100` | Applies or references the 'RNGCannonRandomDamage' effect/state. |
| `RandomDistanceDisplace` | Number | `20, { ... }` | Displaces the target by a randomized distance. |
| `RandomInjury` | Number | `1` | Applies or references the 'RandomInjury' effect/state. |
| `RandomKnockbackDirection` | Number | `4` | Applies or references the 'RandomKnockbackDirection' effect/state. |
| `RandomKnockback` | Block | `{ ... }` | Applies a randomized amount of knockback force. |
| `RandomMagicMissile` | Number | `1, 5, { ... }` | Fires a randomized number of magic missiles. |
| `RandomPermanentStat` | Number | `1` | Applies or references the 'RandomPermanentStat' effect/state. |
| `RandomStatDown` | Number | `1, [ 1 .25 ]` | Applies or references the 'RandomStatDown' effect/state. |
| `RandomStatUp` | Number | `1, -5, 10` | Applies or references the 'RandomStatUp' effect/state. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `RangeUp` | Number | `1` | Applies or references the 'RangeUp' effect/state. |
| `Reanimate` | Number | `100%, 50%` | Applies or references the 'Reanimate' effect/state. |
| `RebukeDamage` | Number | `1, 2` | Applies or references the 'RebukeDamage' effect/state. |
| `ReduceManaCostExcludeBrainstorm` | Number | `1` | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. |
| `ReduceManaCost` | Number | `1` | Applies or references the 'ReduceManaCost' effect/state. |
| `Reflect` | Number | `1, 5` | Applies or references the 'Reflect' effect/state. |
| `ReformMoonHead` | Number | `1` | Applies or references the 'ReformMoonHead' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `RefreshItemAbilities` | Number | `1` | Applies or references the 'RefreshItemAbilities' effect/state. |
| `RefreshMovePointsIfHit` | Number | `1` | Applies or references the 'RefreshMovePointsIfHit' effect/state. |
| `RefreshMovePoints` | Number | `1` | Applies or references the 'RefreshMovePoints' effect/state. |
| `RefreshNonManaItemAbilities` | Number | `1` | Applies or references the 'RefreshNonManaItemAbilities' effect/state. |
| `RefreshOncePerFightAbilities` | Number | `1` | Applies or references the 'RefreshOncePerFightAbilities' effect/state. |
| `RefreshWeaponAbility` | Number | `1` | Applies or references the 'RefreshWeaponAbility' effect/state. |
| `Regurge` | Number | `1` | Applies or references the 'Regurge' effect/state. |
| `RemoveActPoints` | Number | `1` | Applies or references the 'RemoveActPoints' effect/state. |
| `RemoveMovePoints` | Number | `1` | Applies or references the 'RemoveMovePoints' effect/state. |
| `RemoveStatusStacks` | Block | `{ ... }` | Removes a specific number of stacks of a status effect. |
| `RemoveStatus` | Enum/String | `Sleep, SleepParalysis, Drowsy` | Applies or references the 'RemoveStatus' effect/state. |
| `RepairAllCondition` | Number | `1` | Applies or references the 'RepairAllCondition' effect/state. |
| `RepairAll` | Number | `1, 10` | Applies or references the 'RepairAll' effect/state. |
| `RepairArmorCondition` | Number | `1` | Applies or references the 'RepairArmorCondition' effect/state. |
| `RepairOnKill` | Number | `1, 2` | Applies or references the 'RepairOnKill' effect/state. |
| `RepairWeaponCondition` | Number | `1` | Applies or references the 'RepairWeaponCondition' effect/state. |
| `RepairWeapon` | Number | `1, 99` | Applies or references the 'RepairWeapon' effect/state. |
| `RerollEnemy` | Number | `1` | Applies or references the 'RerollEnemy' effect/state. |
| `ResetArmorShield` | Number | `1` | Applies or references the 'ResetArmorShield' effect/state. |
| `ReturnDinoLegs` | Number | `1` | Applies or references the 'ReturnDinoLegs' effect/state. |
| `ReviveNextRound` | Number | `2, { ... }` | Queues the character to be resurrected at the start of the next combat round. |
| `Revive` | Number | `1, 100%, 50%` | Applies or references the 'Revive' effect/state. |
| `Rot` | Number | `1, 2, [ 1 .1 ]` | Applies or references the 'Rot' effect/state. |
| `SafeDie` | Number | `1` | Applies or references the 'SafeDie' effect/state. |
| `ScatterHeldCoin` | Number | `1, [ 1 .3 ], [ 1 .5 ]` | Applies or references the 'ScatterHeldCoin' effect/state. |
| `ScatterRandomPickups` | Number | `2` | Applies or references the 'ScatterRandomPickups' effect/state. |
| `ScrambleEverything` | Number | `0, 10%` | Applies or references the 'ScrambleEverything' effect/state. |
| `ScrambleLastUsedSpell` | Block | `{ ... }` | Randomizes or scrambles the properties of the last spell cast. |
| `SelfStun` | Number | `1, [ 1 .5 ]` | Applies or references the 'SelfStun' effect/state. |
| `SendRock` | Number | `1` | Applies or references the 'SendRock' effect/state. |
| `SetCrazyEyeBackgroundWeights` | Block | `{ ... }` | Adjusts visual rendering weights for the 'Crazy Eye' background effect. |
| `SetDefaultFace` | Enum/String | `insane` | Applies or references the 'SetDefaultFace' effect/state. |
| `SetDistanceDisplace` | Number | `5` | Applies or references the 'SetDistanceDisplace' effect/state. |
| `SetHealth` | Number | `1, 100%` | Applies or references the 'SetHealth' effect/state. |
| `SetShield` | Number | `0` | Applies or references the 'SetShield' effect/state. |
| `ShadowCrit` | Number | `1` | Applies or references the 'ShadowCrit' effect/state. |
| `Shatter` | Number | `15` | Applies or references the 'Shatter' effect/state. |
| `Shield` | Number | `2, 5, "max((X-1)*2, 0)"` | Applies or references the 'Shield' effect/state. |
| `ShootHereCommand` | Number | `1` | Applies or references the 'ShootHereCommand' effect/state. |
| `ShootHereReceiver` | Number | `1` | Applies or references the 'ShootHereReceiver' effect/state. |
| `ShortCircuit` | Number | `1` | Applies or references the 'ShortCircuit' effect/state. |
| `SignalFinalBossShieldBroke` | Number | `1` | Applies or references the 'SignalFinalBossShieldBroke' effect/state. |
| `SizeScale` | Enum/String | `.6` | Applies or references the 'SizeScale' effect/state. |
| `Sleep` | Number | `1, [ 1 .1 ], 3` | Applies or references the 'Sleep' effect/state. |
| `Slow` | Number | `1, [ 1 .1 ], [ 1 .25 ]` | Applies or references the 'Slow' effect/state. |
| `SmallHitExplosion` | Number | `1` | Applies or references the 'SmallHitExplosion' effect/state. |
| `SmartMetronome` | Number | `20, { ... }` | Executes a 'smart' random ability that aims to be beneficial based on context. |
| `SmellBlood` | Number | `1` | Applies or references the 'SmellBlood' effect/state. |
| `SoulLink` | Number | `1` | Applies or references the 'SoulLink' effect/state. |
| `SoundEventOnHit` | Enum/String | `Batterup_Connect` | Applies or references the 'SoundEventOnHit' effect/state. |
| `SourceSwapsBackEndOfTurn` | Enum/String | `ThiefSwapBack` | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. |
| `SpawnBearTrap` | Number | `1` | Applies or references the 'SpawnBearTrap' effect/state. |
| `SpawnCoinAnywhere` | Number | `1, [ 1 .5 ]` | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `SpawnCreep` | Number | `1` | Applies or references the 'SpawnCreep' effect/state. |
| `SpawnCustomTrap` | Enum/String | `CharmTrap, EggSackTrap, SpikeTrap` | Applies or references the 'SpawnCustomTrap' effect/state. |
| `SpawnFlames` | Array | `[ 1, .20 ], [ 1, .20+.1*level ]` | Applies or references the 'SpawnFlames' effect/state. |
| `SpawnNeutralWebTrapOnMiss` | Number | `1` | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. |
| `SpawnRock` | Number | `1, [ 1, .20 ]` | Applies or references the 'SpawnRock' effect/state. |
| `SpawnThingIfHitKills` | Enum/String | `Food, BiggestFood, BigFood` | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| `SpawnWebTrap` | Number | `1` | Applies or references the 'SpawnWebTrap' effect/state. |
| `SpecialBossMultipartInstakill` | Enum/String | `moonboss` | Applies or references the 'SpecialBossMultipartInstakill' effect/state. |
| `SpecificInjury` | Enum/String | `int, str, spd` | Applies or references the 'SpecificInjury' effect/state. |
| `SpeculativeMoveSelfCorpseOffMap` | Number | `1` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. |
| `SpeedUp` | Number | `1, 2, -1` | Applies or references the 'SpeedUp' effect/state. |
| `SpellDamageUp` | Number | `1, 3` | Applies or references the 'SpellDamageUp' effect/state. |
| `SpellShield` | Number | `1` | Applies or references the 'SpellShield' effect/state. |
| `SpiderInfested` | Number | `1, 2, 4` | Applies or references the 'SpiderInfested' effect/state. |
| `SpitConsumed` | Number | `1` | Applies or references the 'SpitConsumed' effect/state. |
| `SplashDamage` | Number | `1` | Applies or references the 'SplashDamage' effect/state. |
| `SpreadDisease` | Block | `{ ... }` | Provides a chance to transmit a disease status to adjacent targets. |
| `StackingSandstorm` | Number | `1` | Applies or references the 'StackingSandstorm' effect/state. |
| `StanceSwitchToMelee` | Number | `1` | Applies or references the 'StanceSwitchToMelee' effect/state. |
| `StatBounty` | Number | `1` | Applies or references the 'StatBounty' effect/state. |
| `StatusGroup` | Block | `{ ... }` | Groups multiple status effects together for batch application. |
| `StealDemonicGlyph` | Number | `1` | Applies or references the 'StealDemonicGlyph' effect/state. |
| `StealEquipment` | Enum/String | `any` | Applies or references the 'StealEquipment' effect/state. |
| `StealTurn` | Number | `1` | Applies or references the 'StealTurn' effect/state. |
| `StealthCritChance` | Number | `100` | Applies or references the 'StealthCritChance' effect/state. |
| `Stealth` | Number | `1, 2` | Applies or references the 'Stealth' effect/state. |
| `StrengthUp` | Number | `1, 2, item_aux` | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Number | `1, [ 1 .5 ], [ 1, .25 ]` | Applies or references the 'Stun' effect/state. |
| `SwallowSmallCharacter` | Number | `100%, 50%` | Applies or references the 'SwallowSmallCharacter' effect/state. |
| `SwapHighestAndLowestStat` | Number | `1` | Applies or references the 'SwapHighestAndLowestStat' effect/state. |
| `SwapWeapon` | Block | `{ ... }` | Replaces the character's currently equipped weapon with one from a specified pool. |
| `SwitchMusic` | Block | `{ ... }` | Changes the background music track or layer during combat. |
| `Switcheroo` | Number | `1` | Applies or references the 'Switcheroo' effect/state. |
| `T3HitlerTriggerInitialSpawns` | Number | `1` | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. |
| `TagMetronome` | Enum/String | `musical` | Applies or references the 'TagMetronome' effect/state. |
| `TakeBonusTurnWithAIControl` | Block | `{ ... }` | Grants the character an immediate extra turn, but forces the AI to control them during it. |
| `TakeBonusTurnWithStatus` | Block | `{ ... }` | Grants the character an immediate extra turn while afflicted with specific statuses. |
| `TakeExtraTurnEndOfRound` | Number | `1` | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `Tangled` | Number | `1, { ... }` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `TargetedMetronome` | Number | `20` | Applies or references the 'TargetedMetronome' effect/state. |
| `Tarred` | Number | `2, [ 1 .1 ]` | Applies or references the 'Tarred' effect/state. |
| `Taunting` | Number | `1` | Applies or references the 'Taunting' effect/state. |
| `TeamBonusAbility` | Enum/String | `ShootHere` | Applies or references the 'TeamBonusAbility' effect/state. |
| `TeamCastAbility` | Enum/String | `Spin, TeamFlex_Impl, TeamFlex_Impl2` | Requires or involves multiple characters to execute the ability. |
| `Tech` | Number | `1, 3` | Applies or references the 'Tech' effect/state. |
| `TeleportBackAtTurnEnd` | Enum/String | `FlashBack` | Applies or references the 'TeleportBackAtTurnEnd' effect/state. |
| `TempBackstabBleed` | Number | `1` | Applies or references the 'TempBackstabBleed' effect/state. |
| `TempBackstabPiercing` | Number | `1` | Applies or references the 'TempBackstabPiercing' effect/state. |
| `TempBackstabPoison` | Number | `1` | Applies or references the 'TempBackstabPoison' effect/state. |
| `TempBackstab` | Number | `75` | Applies or references the 'TempBackstab' effect/state. |
| `TempBasicAttackBonusAOE` | Number | `1` | Applies or references the 'TempBasicAttackBonusAOE' effect/state. |
| `TempBonusKnockbackDamage` | Number | `1` | Applies or references the 'TempBonusKnockbackDamage' effect/state. |
| `TempBonusKnockback` | Number | `1` | Applies or references the 'TempBonusKnockback' effect/state. |
| `TempCounterAttack` | Number | `1` | Applies or references the 'TempCounterAttack' effect/state. |
| `TempCritChanceUp` | Number | `30, 100` | Applies or references the 'TempCritChanceUp' effect/state. |
| `TempDamageUp` | Number | `1, 2` | Applies or references the 'TempDamageUp' effect/state. |
| `TempDexterityUp` | Enum/String | `X` | Applies or references the 'TempDexterityUp' effect/state. |
| `TempInitiativeChange` | Number | `9999, 100` | Applies or references the 'TempInitiativeChange' effect/state. |
| `TempInjuryImmunity` | Number | `1` | Applies or references the 'TempInjuryImmunity' effect/state. |
| `TempLuckUp` | Number | `99` | Applies or references the 'TempLuckUp' effect/state. |
| `TempManaCostReduction` | Number | `1` | Applies or references the 'TempManaCostReduction' effect/state. |
| `TempMovement` | Number | `20, mov` | Applies or references the 'TempMovement' effect/state. |
| `TempPenetrate` | Number | `1` | Applies or references the 'TempPenetrate' effect/state. |
| `TempPreEmptiveCounterAttack` | Number | `1` | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. |
| `TempRangeUp` | Number | `1, 20, 3` | Applies or references the 'TempRangeUp' effect/state. |
| `TempSpeedUp` | Number | `4, 10, X` | Applies or references the 'TempSpeedUp' effect/state. |
| `TempSpellDamageUp` | Number | `1` | Applies or references the 'TempSpellDamageUp' effect/state. |
| `TempStrengthUp` | Enum/String | `X` | Applies or references the 'TempStrengthUp' effect/state. |
| `TempTrampleUntilSettled` | Number | `3` | Applies or references the 'TempTrampleUntilSettled' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `ThornsDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. |
| `Thorns` | Number | `6, 1, 2` | Applies or references the 'Thorns' effect/state. |
| `TickDownStatus` | Enum/String | `ShortCircuit` | Applies or references the 'TickDownStatus' effect/state. |
| `TileDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. |
| `TilesMovedToCritChance` | Number | `1` | Applies or references the 'TilesMovedToCritChance' effect/state. |
| `TilesMovedToMana` | Number | `1` | Applies or references the 'TilesMovedToMana' effect/state. |
| `TilesMovedToNeighborHeal` | Enum/String | `level` | Applies or references the 'TilesMovedToNeighborHeal' effect/state. |
| `TilesMovedToStrength` | Number | `1` | Applies or references the 'TilesMovedToStrength' effect/state. |
| `TimeDelayStatusApplication` | Block | `{ ... }` | Delays the nested effects by a specified amount of real-time seconds. |
| `TowerDefenseStatus2` | Number | `1` | Applies or references the 'TowerDefenseStatus2' effect/state. |
| `TowerDefenseStatus` | Number | `1` | Applies or references the 'TowerDefenseStatus' effect/state. |
| `TradeLife` | Number | `1` | Applies or references the 'TradeLife' effect/state. |
| `TrailBlazer` | Number | `1, mov` | Applies or references the 'TrailBlazer' effect/state. |
| `Trample` | Number | `3` | Applies or references the 'Trample' effect/state. |
| `TransformAbility` | Enum/String | `MonkeyThrow, Pounce2, Pounce` | Applies or references the 'TransformAbility' effect/state. |
| `TransformBasicAttack` | Enum/String | `ThrowPoop, TigerSwipes2, TigerSwipes` | Applies or references the 'TransformBasicAttack' effect/state. |
| `TransformBasicMove` | Enum/String | `BasicDashAttackMove_NoKnockback` | Applies or references the 'TransformBasicMove' effect/state. |
| `TransformEquipment` | Block | `{ ... }` | Upgrades or transforms a specific equipped item into another. |
| `TransformNow` | Enum/String | `Hitler` | Applies or references the 'TransformNow' effect/state. |
| `Trapper_Status` | Number | `1` | Applies or references the 'Trapper_Status' effect/state. |
| `TriggerDOTStatuses` | Number | `1, 0` | Applies or references the 'TriggerDOTStatuses' effect/state. |
| `TriggerGameEnding` | Number | `1` | Applies or references the 'TriggerGameEnding' effect/state. |
| `TriggerMotherConsume` | Number | `1` | Applies or references the 'TriggerMotherConsume' effect/state. |
| `TriggerMotherGrow` | Number | `4` | Applies or references the 'TriggerMotherGrow' effect/state. |
| `TriggerWerewolfTransform` | Array | `[ 1 .5 ], [ 1 .15 ], .5` | Applies or references the 'TriggerWerewolfTransform' effect/state. |
| `TurnAround` | Number | `1` | Applies or references the 'TurnAround' effect/state. |
| `TurnControlDelay` | Enum/String | `.25` | Applies or references the 'TurnControlDelay' effect/state. |
| `TurnRight` | Number | `1` | Applies or references the 'TurnRight' effect/state. |
| `TwisterDisplaceWithDamage` | Block | `{ ... }` | A whirlwind effect that randomly displaces targets and deals damage. |
| `UndoDamage` | Number | `1` | Applies or references the 'UndoDamage' effect/state. |
| `UpgradeRandomAbility` | Number | `1` | Applies or references the 'UpgradeRandomAbility' effect/state. |
| `UseAbility` | Enum/String | `MD_PoopChain, ManglerThrowRemote, GirlDinoPoop` | Forces the character or target to instantly use a specified ability. |
| `UseMoveAbilityWithAI` | Block | `{ ... }` | Forces the character to execute a movement ability using specific AI weights. |
| `VaporizeCorpseFlipAdvantage` | Array | `[ 1 .33 ]` | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. |
| `VaporizeCorpse` | Number | `1` | Applies or references the 'VaporizeCorpse' effect/state. |
| `VaporizeDice` | Number | `1` | Applies or references the 'VaporizeDice' effect/state. |
| `VaporizeInanimate` | Number | `1` | Applies or references the 'VaporizeInanimate' effect/state. |
| `VaporizeTarget` | Number | `1` | Applies or references the 'VaporizeTarget' effect/state. |
| `Vaporize` | Number | `1, 20` | Applies or references the 'Vaporize' effect/state. |
| `VisualCountDownThenApplyStatus` | Block | `{ ... }` | Displays a visual countdown above the target before applying the nested effects. |
| `VisualFXTile` | Enum/String | `PoisonPoof, WaterConduct, FireBlastSmall` | Applies or references the 'VisualFXTile' effect/state. |
| `VisualFX` | Enum/String | `Holyatk, MagicMissleBlast, WaterConduct` | Applies or references the 'VisualFX' effect/state. |
| `WaggleClone` | Block | `{ ... }` | Spawns visual clones or alternative hitbox variants of the projectile. |
| `Weakness` | Number | `1, 2, [ 1 .25 ]` | Applies or references the 'Weakness' effect/state. |
| `Webbed` | Number | `1` | Applies or references the 'Webbed' effect/state. |

### Context: `empty_self_damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |

### Context: `extra_statuses`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `4` | Applies or references the 'Burn' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Tarred` | Number | `2` | Applies or references the 'Tarred' effect/state. |

### Context: `graphics`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `affected_animation` | Enum/String | `statDown` | Visuals applied to the target receiving the effect. |
| `affected_particle` | Enum/String | `HealBig, HealMed, fx_tentaclestrangle` | Visuals applied to the target receiving the effect. |
| `air_animation` | Enum/String | `entrance, gravitySlam_air, bellyflop_air` | Animation played while entity is airborne. |
| `ally_animation` | Enum/String | `lickAttack` | Distinct animation used when targeting a friendly unit. |
| `always_play_animations` | Boolean | `true` | Bypasses speed-up/skip logic. |
| `animate_name` | Enum/String | `pointout` | Animates the ability name text on cast. |
| `animation_in` | Enum/String | `shadowStepIn, teleportIn, digUp` | Used for transition states (like burrowing). |
| `animation_out` | Enum/String | `digDown, teleportOut, shadowStepOut` | Used for transition states (like burrowing). |
| `animation` | Enum/String | `sing3, attack, none` | The primary flash animation label triggered. |
| `aoe_spell_on_land` | Boolean | `true` | Visual trigger when a jump lands. |
| `apex_distance` | Number | `0.875` | Calculations for the peak of a jump/lob arc. |
| `apex_time` | Enum/String | `.35` | Calculations for the peak of a jump/lob arc. |
| `area_particle` | Enum/String | `none, BurnTrigger, FireBlastSmall` | Specific spawn points for particles. |
| `beam_cap` | Enum/String | `greenmegalasercap, thinlasercap, greenlasercap` | Flash movieclips used to render continuous laser beams. |
| `beam_clip` | Enum/String | `greenlaser, greenmegalaser, thinlaser` | Flash movieclips used to render continuous laser beams. |
| `bounce_on_hit` | Boolean | `false, true` | Visual hop when striking a target. |
| `bypass_combatspeed` | Boolean | `true` |  |
| `center_particle` | Enum/String | `Explosion, FireBlastMushroom, none` | Specific spawn points for particles. |
| `chain_distance` | Enum/String | `.25, .38` | Creates a tethered repeating graphic (like a hook). |
| `chain_movieclip` | Enum/String | `Frogchain, Bramblechain, ChainLink` | Creates a tethered repeating graphic (like a hook). |
| `custom_priming_animation` | Enum/String | `priming, idleCommand3, idleCommand2` | Animation used while charging an ability. |
| `damage_threshold_altanimations` | Block | `{ ... }` | Triggers different hit animations based on the amount of damage dealt. |
| `darken_screen_exclude_characters_on_tile` | Boolean | `false, true` |  |
| `darken_screen_exclude_self` | Boolean | `true` |  |
| `darken_screen_start_early` | Boolean | `true` |  |
| `darken_screen` | Boolean | `false, true` | Dims the background during the ability cast. |
| `dash_animation` | Enum/String | `headbuttdash, roll, spinattackloop` | State-specific animations for trample/dash abilities. |
| `dash_attack_animation` | Enum/String | `headbuttdashEnd, none, spinattackloop` |  |
| `dash_bonk_animation` | Enum/String | `bonk` |  |
| `dash_decelerating_animation` | Enum/String | `dashslow` |  |
| `dash_end_animation` | Enum/String | `launchStop, dashend, timberEnd` |  |
| `dash_start_animation` | Enum/String | `none, dashstart, headbuttdashStart` |  |
| `decelerate` | Number | `5` | Visual slowdown at the end of a movement. |
| `delay_from_map_center` | Boolean | `true` | Positional based timing delays. |
| `delay_from_map_edge` | Boolean | `false, true` | Delays effect based on distance from the screen edge. |
| `delay_from_reverse_map_edge` | Boolean | `true` |  |
| `delay` | Number | `2, 5, 4` | Frame delay before firing projectile/effect. |
| `detatched_animation_cutoff` | Boolean | `true` |  |
| `detatched_animation_reach` | Number | `3, 4, 20` |  |
| `detatched_animation` | Enum/String | `LiquidMetalSpear, WaterGush, TinaSpear` | Plays an animation separated from the character body. |
| `do_animation_offscreen` | Boolean | `true` |  |
| `do_damage_immediately` | Boolean | `true` | Applies math before the animation actually hits. |
| `do_not_clear_placeholder` | Boolean | `true` |  |
| `dont_orient` | Boolean | `true` | Prevents the character from turning to face the target. |
| `dont_visualize_ai` | Boolean | `true` |  |
| `easing` | Number | `1` | Smoothing function for movement animations. |
| `empty_animation` | Enum/String | `empty` |  |
| `end` | Enum/String | `spinattackend, lickAttack, attack` | Segments for continuous channeled animations. |
| `face_targets` | Boolean | `true` | Forces the sprite to look at the target tile. |
| `face_toss_target` | Boolean | `true` |  |
| `fall_from_sky` | Boolean | `true` | Spawns the projectile from the top of the screen. |
| `fall_randomize_timing` | Enum/String | `.3` |  |
| `first_castpoint_is_self_damage_only` | Boolean | `true` |  |
| `fixed_jump_height` | Number | `3.5, 1` |  |
| `fixed_jump_speed` | Number | `1, 2, .8` |  |
| `full_jump_animation` | Enum/String | `attack, jumpmove, jumpattack` |  |
| `full_jump_sync_frames` | Number | `38, 46, 49` |  |
| `full_jump_windup_frames` | Number | `13, 22, 20` |  |
| `fx_is_placeholder_animation` | Boolean | `true` |  |
| `fx_random_flip` | Boolean | `true` |  |
| `grab_animation` | Enum/String | `grab` |  |
| `hang_time` | Enum/String | `.6` |  |
| `ignore_slowtiles` | Boolean | `true` |  |
| `jump_attack_animation` | Enum/String | `land, gravitySlamEnd, block` | Overrides for jump physics. |
| `jump_height_multiplier` | Number | `2, .25` | Overrides for jump physics. |
| `jump_speed_multiplier` | Number | `1.5` |  |
| `jump_start_animation` | Enum/String | `gravitySlamStart, leapattackwindup, none` |  |
| `land_animation` | Enum/String | `none` |  |
| `lob_height` | Number | `1, 0, 4` | Adjustments for arcing projectiles. |
| `lob_speed` | Enum/String | `.5` | Adjustments for arcing projectiles. |
| `lob_yoff` | Enum/String | `-.5` | Adjustments for arcing projectiles. |
| `lob` | Boolean | `false, true` |  |
| `lock_orientation_during_dash` | Boolean | `true` | Prevents the sprite from flipping mid-dash. |
| `loop` | Enum/String | `lickAttack, attack, spinattackloop` | Segments for continuous channeled animations. |
| `mask_center` | Enum/String | `SpearMaskCenter` |  |
| `mask_extent` | Enum/String | `SpearMaskExtent` |  |
| `max_range` | Number | `3` | The maximum and minimum distance required to cast. |
| `max_throw_height` | Number | `1.75` |  |
| `max_tiles_single_loop` | Number | `1, 5, 6` |  |
| `min_range` | Number | `1` | The maximum and minimum distance required to cast. |
| `min_throw_height` | Number | `1.75, 0, 4` |  |
| `miss_particle` | Enum/String | `fx_tentaclestrangleMiss` | Specific spawn points for particles. |
| `miss_random_delay` | Array | `[ 0, 20 ], [ 0, 60 ]` |  |
| `mode` | Enum/String | `yeet` |  |
| `move_end_animation` | Enum/String | `none, buttScootEnd, endroll` |  |
| `move_start_animation` | Enum/String | `buttScootStart, none, startroll` |  |
| `othercat_placeholder_available` | Boolean | `true` |  |
| `palette` | Number | `6` | Swaps the color palette ID. |
| `particle_mat` | Enum/String | `shadow_occluded_spelldissolve` |  |
| `particle` | Enum/String | `PoisonPoof, none, None` | References an impact or cast particle effect. |
| `precast_delay` | Enum/String | `.25` |  |
| `preturn_animation` | Enum/String | `alertstart` |  |
| `prime_animation` | Enum/String | `chargeholy, prouder, pointout` |  |
| `primed_alt_animation` | String | `"shootPrimed"` |  |
| `projectile` | Enum/String | `MagicSpikeProjectile, NeedleProjectile, LeechProjectile` | References a projectile entity. |
| `pseudoprojectile` | Enum/String | `RocketFromAbove` |  |
| `random_delay` | Array | `[ 0, 120 ], [ 30 50 ], [ 70 100 ]` | Adds chaotic timing to multi-projectile casts. |
| `reverse_orientation` | Boolean | `true` |  |
| `rocket_swirl` | Block | `{ ... }` | Visual parameters for swirling projectile paths. |
| `self_damage_mid_port` | Boolean | `true` |  |
| `single_projectile` | Boolean | `true` |  |
| `spawn_offset` | Array | `[ 0, .5, 0 ]` |  |
| `speed` | Number | `2, 20, .5` | Base speed of the projectile/animation. |
| `start` | Enum/String | `spinattackstart, attack, lickAttack` | Segments for continuous channeled animations. |
| `sync_frames` | Number | `26, 34` |  |
| `sync_speed` | Number | `22, 28, 30` |  |
| `throw_speed` | Number | `3` |  |
| `uncatchable` | Boolean | `true` |  |
| `use_directional_animations` | Boolean | `true` |  |
| `use_hit_alts` | Boolean | `false` |  |
| `use_origin_offsets` | Boolean | `false` |  |
| `use_placeholder` | Boolean | `true` |  |
| `use_projectile_spawn_offset` | Boolean | `true` |  |
| `use_projectile` | Boolean | `true` |  |
| `use_rotation_once` | Boolean | `true` |  |
| `use_rotation` | Boolean | `false` |  |
| `use_super_armor` | Boolean | `false, true` | Prevents flinch animations from interrupting this cast. |
| `visual_delay_but_simultaneous_damage` | Number | `8, 0, 3` |  |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `3` | Applies or references the 'Bleed' effect/state. |
| `BonusAbility` | Enum/String | `TinkererThrow, ThrowSpiritBomb, DonateEnergy` | Applies or references the 'BonusAbility' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `DamageUp` | Number | `-1` | Applies or references the 'DamageUp' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |
| `Shield` | Number | `5` | Applies or references the 'Shield' effect/state. |
| `TemporaryItem` | Number | `1` | Applies or references the 'TemporaryItem' effect/state. |
| `Webbed` | Number | `1` | Applies or references the 'Webbed' effect/state. |

### Context: `meta`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability_icon` | Enum/String | `BasicRanged, BasicMelee, Pestilence` | The UI icon to display in the action bar. |
| `animate_name` | Boolean | `false, true` | If true, adds a visual pop/animation to the name text when cast. |
| `animation` | Enum/String | `portin` |  |
| `class` | Enum/String | `Hunter, Fighter, Mage` | Categorizes the ability for specific UI filters. |
| `desc` | String | `"ABILITY_CROWNOFPESTILENCE_DESC", "nothing", "ABILITY_MELEEATTACK_DESC"` | The localization key for the ability's display description. |
| `dont_visualize_ai` | Boolean | `true` |  |
| `icon_damage_display_eq` | Enum/String | `item_aux, "10+bonus_melee_ability_damage", "3+bonus_melee_ability_damage"` |  |
| `icon_damage_display_suffix` | String | `"x2", "x10"` |  |
| `icon_damage_display` | String | `"?", "1-6", "0-25"` |  |
| `icon_damage_type` | Enum/String | `magic, physical` |  |
| `icon_shell_frame` | Enum/String | `attack, multihit_attack, "attack"` |  |
| `is_basic_attack` | Boolean | `true` |  |
| `is_move` | Enum/String | `auto, true` |  |
| `is_trinket` | Boolean | `true` |  |
| `is_weapon` | Boolean | `true` |  |
| `name` | String | `"ABILITY_CROWNOFPESTILENCE_NAME", "None", "ABILITY_MELEEATTACK_NAME"` | The localization key for the ability's display name. |
| `tooltip_values` | Array | `[ "X" ], [ "max((X-1)*2, 0)" ], [ "max(X*3, 0)" ]` |  |
| `type_icon` | String | `"defense", "unknown", "misc"` |  |

### Context: `post_spawn_statuses`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DoDamage` | Block | `{ ... }` | Explicitly triggers a secondary damage instance independent of the main attack. |
| `EnterMount` | Enum/String | `enter` | Applies or references the 'EnterMount' effect/state. |
| `VisualFXTile` | Enum/String | `PoisonPoof` | Applies or references the 'VisualFXTile' effect/state. |

### Context: `rocket_swirl`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `radius` | Array | `[ .5 1 ], [ .25 .5 ]` | Swirl radius. |
| `speed` | Array | `[ .25, 1.0 ], [ 1.5, 2.5 ]` | Rotations per second. |

### Context: `self_damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai_base_score` | Number | `9999` |  |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `2, "floor(X*.25)", 0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Water ], [ Explosion ], [ Fire ]` |  |
| `heal` | Number | `25, 8, 4` |  |
| `knockback` | Number | `1, -10, -3` |  |
| `non_lethal` | Boolean | `true` |  |
| `piercing` | Boolean | `true` |  |
| `type` | Enum/String | `melee, none, spell` | Classification/category type. |

### Context: `sounds`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `oncast` | Enum/String | `AbilitySnd_Assassinate, AbilitySnd_BoulderDrop` |  |
| `oncastpoint` | Enum/String | `AirHorn, Batterup_Swing_Castpoint` |  |
| `ontrigger_intentional` | Enum/String | `Lenny_HereKitty` |  |
| `ontrigger` | Enum/String | `Spawn_Donate, SE_BullRushDash, Spiderweb_Break` |  |

### Context: `spawn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `additional_passives` | Block | `{ ... }` | Passives granted intrinsically to a spawned entity. |
| `ai_base_score` | Number | `999999, 9999, 99999` |  |
| `appearance` | Enum/String | `GolemCat` |  |
| `auto_cast_on_spawn` | Enum/String | `Dash_Enemy` |  |
| `catdata` | Enum/String | `teamclone, clone, item_aux_catid` | Defines genetic/clone data cloning. |
| `chapter` | Enum/String | `alley` |  |
| `clone_items` | Boolean | `true` | If true, transfers inventory to the clone. |
| `custom_additional_ai_weight` | Enum/String | `tile_exists` |  |
| `face_camera` | Boolean | `true` |  |
| `faction` | Enum/String | `self, default, solitary_enemies` |  |
| `first_turn` | Enum/String | `end_of_round, next_turn, initiative` |  |
| `include_passives` | Boolean | `true` |  |
| `inherit_elite_buffs` | Boolean | `false` |  |
| `layer` | Enum/String | `gas, pickups, characters` |  |
| `lob` | Boolean | `false` |  |
| `object` | Enum/String | `Food, RANDOM_1X1_ENEMY, PlayerCat_ThiefShade` |  |
| `post_spawn_statuses` | Block | `{ ... }` | Status effects applied immediately after an entity spawns. |
| `redirect_location_if_blocked` | Boolean | `true` |  |
| `size` | Number | `2` |  |
| `spawnin_animation` | Enum/String | `summonspawnin` |  |
| `start_dead` | Boolean | `true` |  |
| `trigger_battle_start` | Boolean | `true` |  |

### Context: `splash_damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai_base_score` | Number | `9999` |  |
| `crit_chance` | Number | `100` |  |
| `damage` | Number | `8, 0, 4` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Fire Napalm Explosion ], [ Water ], [ Fire Explosion ]` |  |
| `force_no_knockback` | Boolean | `true` |  |
| `force_play_hit_animation` | Boolean | `true` |  |
| `knockback` | Number | `1, 2, 0` | Knockback force of the splash blast. |
| `layer` | Enum/String | `tiles` |  |
| `makes_contact` | Boolean | `false, true` |  |
| `override_trample_damage` | Boolean | `true` |  |
| `type` | Enum/String | `knockblock, spell, status_spell` | Classification/category type. |

### Context: `target`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `,` | Array | `[ 0, -1 ], [ 1, 1 ], [ 0, 1 ]` |  |
| `-1,` | Number | `1, -1, 0` |  |
| `-2,` | Number | `0` |  |
| `-3,` | Number | `0` |  |
| `-4,` | Number | `0` |  |
| `0,-1` | Flag | `N/A` |  |
| `0,` | Number | `1, -1, 0` |  |
| `1,-1` | Flag | `N/A` |  |
| `1,` | Number | `1, -1, 0` |  |
| `2,-1` | Flag | `N/A` |  |
| `2,` | Number | `1, 2, 0` |  |
| `3,-1` | Flag | `N/A` |  |
| `3,-2` | Flag | `N/A` |  |
| `3,` | Number | `1, -1, 0` |  |
| `4,` | Number | `0, 4` |  |
| `5,` | Number | `5` |  |
| `6,` | Number | `6` |  |
| `7,` | Number | `7` |  |
| `8,` | Number | `8` |  |
| `9,` | Number | `9` |  |
| `N` | Number | `5, 2, 3` | Variable modifier parameter. |
| `X_is` | Enum/String | `current_health, turn_count, custom` | Applies or references the 'X_is' effect/state. |
| `adjust_target` | Enum/String | `stalk` | Tweaks target selection post-cast. |
| `allow_any_orientation` | Boolean | `true` | Allows casting regardless of the character's facing direction. |
| `allow_diagonal_passthrough` | Boolean | `true` | Permits diagonal targeting through tight corners. |
| `allow_diagonals` | Boolean | `true` | Allows targeting on diagonal grid axes. |
| `ally_priority` | Number | `1` | AI preference for targeting allies. |
| `always_bounce` | Boolean | `true` | Forces the attack/projectile to bounce regardless of hit. |
| `aoe_chance` | Enum/String | `.4+.2*level, .33, .5` | Percentage chance for the AoE to trigger. |
| `aoe_considers_character_size` | Boolean | `false, true` | Scales the AoE based on the caster's tile size (e.g., 2x2). |
| `aoe_display_exclude_restrictions` | Boolean | `true` | Visual only: Hides invalid tiles from the AoE preview. |
| `aoe_excludes_self` | Boolean | `false, true` | Prevents the AoE from hitting the caster. |
| `aoe_hint_teamcast` | Boolean | `true` | Visual hint for cooperative casting abilities. |
| `aoe_leading_edge_only` | Boolean | `true` | Only the outermost edge of the AoE shape applies effects. |
| `aoe_mode` | Enum/String | `standard, all, custom` | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). |
| `aoe_restrictions` | Array | `[ exclude_blocking ], enemies_only, must_have_tag` | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). |
| `aoe_rotate_around_character_center` | Boolean | `true` | Anchors the AoE rotation to the character rather than the tile. |
| `aoe_spell_on_land` | Boolean | `true` | Visual trigger when a jump lands. |
| `aoe_symmetry` | Enum/String | `eight_way, four_way, none` | Determines if the AoE mirrors on axes. |
| `aoe_tile_requires_element` | Enum/String | `Water, Grass, Earth` | Only affects tiles painted with a specific element. |
| `as_the_crow_flies` | Boolean | `true` | Calculates range ignoring all pathing terrain obstacles. |
| `bonus_pathing_leniency` | Number | `4` | Gives the AI leeway when calculating complex paths. |
| `can_multihit` | Boolean | `false, true` | If true, overlapping AoEs can hit the same target multiple times. |
| `consider_trample` | Boolean | `false, true` | AI consideration for moving through units. |
| `corpse_priority` | Number | `5, 10` | AI preference for targeting dead bodies. |
| `custom_aoe_mirror` | Array | `[ [ 1 0 ]` | How the custom shape mirrors when facing left vs right. |
| `custom_aoe_util_mirror` | Array | `[ [ 1, 1 ]` |  |
| `custom_aoe_util` | Array | `[ [ -1, 1 ], [ [ 1, 1 ], [ [ 0, 1 ]` | Utility variants of custom AoE definitions. |
| `custom_aoe` | Array | `[ [ -1, 0 ], [ [ 1, -1 ], [ [ 1, 1 ]` | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). |
| `custom_range` | Array | `[ [ 1 2 ], [ [ 1, 1 ], [ [ -2 0 ]` | Overrides standard range scaling. |
| `damage_collided_only` | Boolean | `true` | Only damages the first entity the projectile/dash hits. |
| `delayed_trigger` | Boolean | `false, true` | Delays the actual execution of the target effect. |
| `distance_sort_targets` | Number | `1, true` | Prioritizes targets based on proximity. |
| `dont_orient_aoe` | Boolean | `true` | Prevents the AoE shape from rotating with the character. |
| `dont_orient` | Boolean | `true` | Prevents the character from turning to face the target. |
| `enemy_priority` | Number | `10` | AI preference for targeting enemies. |
| `force_ai_target_as_spell` | Boolean | `true` | Forces the AI to treat a physical move like a spell for targeting logic. |
| `force_no_contact` | Boolean | `true` | Bypasses all contact-based retaliation (Thorns, etc). |
| `hint_can_target_empty` | Boolean | `false, true` | UI hint that the player can click an empty tile. |
| `hint_can_target_pickups` | Boolean | `true` | UI hint that the player can target items on the ground. |
| `hint_can_target_static` | Boolean | `true` | UI hint that the player can target inanimate objects. |
| `knockback_mode` | Enum/String | `zero, tile_to_target, tile_to_character` | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). |
| `knockback_modifier` | Enum/String | `rotate_cw` | Multiplier for the knockback physics force. |
| `lingering` | Boolean | `true` | Target zone remains active across multiple turns. |
| `low_gravity_boostable` | Boolean | `false, true` | Can be affected by low gravity wind/effects. |
| `low_health_character_threshold` | Enum/String | `item_aux, 5, 10` | AI targeting threshold for seeking weak targets. |
| `max_aoe` | Number | `1, 2, 0` | The maximum and minimum radius/length of the AoE. |
| `max_bounces` | Number | `-1, 10, 3` | Hard cap on how many times a bouncing effect can trigger. |
| `max_range` | Number | `1, 5, 20` | The maximum and minimum distance required to cast. |
| `max_targets` | Number | `1, 15, 7` | Limits on how many distinct entities can be targeted. |
| `min_aoe` | Number | `1, 0, 2+size` | The maximum and minimum radius/length of the AoE. |
| `min_range` | Number | `1, 2, 3` | The maximum and minimum distance required to cast. |
| `min_targets` | Number | `5, 1, 2` | Limits on how many distinct entities can be targeted. |
| `mirror_custom_aoe` | Boolean | `true` | Flips the custom AoE array. |
| `mouse_offset` | Array | `[ .5 .5 ]` | Visual offset for the targeting cursor. |
| `multihit_max` | Number | `5, 10, 3` | Variable limits for random multihit abilities. |
| `multihit_min` | Number | `1, 5, 3` | Variable limits for random multihit abilities. |
| `multihit` | Number | `2, 5, 3` | Hardcoded number of times the ability hits the target. |
| `prioritize_change_direction` | Boolean | `true` | AI preference to attack from different angles. |
| `prioritize_dont_change_direction` | Number | `1, true` | AI preference to maintain current facing angle. |
| `prioritize_face_camera` | Number | `1, true` | AI preference to face South. |
| `prioritize_throw_target_with_passive` | Enum/String | `NubbyTossPriority` | AI prefers throwing targets that have specific passives. |
| `randomize_knockback_direction_except_for_finisher` | Boolean | `true` | Chaotic knockback unless it kills the target. |
| `randomize_target_within_range` | Number | `2, 0, 3` | Picks a random valid tile instead of the user's click. |
| `range_bonuses` | Enum/String | `include_alpha` | How much extra range is added by stats/passives. |
| `range_considers_character_size` | Boolean | `false` | Range calculation accounts for large entities. |
| `range_display_include_aoe` | Boolean | `true` | Visual: shows the full AoE potential when previewing range. |
| `range_display_include_character_size` | Boolean | `true` | Visual: offsets the range indicator for 2x2 units. |
| `range_display_include_direction` | Boolean | `true` | Visual: shows directional arrows. |
| `range_excludes_blocking` | Boolean | `false, true` | Cannot target through walls/obstacles. |
| `range_excludes_self` | Boolean | `false` | Cannot click on the caster's tile. |
| `range_max` | Number | `4` | Alternate syntax for `max_range`/`min_range`. |
| `range_min` | Number | `1` | Alternate syntax for `max_range`/`min_range`. |
| `range_mode` | Enum/String | `water_move, cross, standard` | How range is counted (`standard`, `ground_move`). |
| `range_symmetry` | Enum/String | `eight_way` | Mirrors the range grid. |
| `recalc_target_on_castpoint` | Boolean | `true` | Re-checks if target is valid at the exact frame of cast. |
| `redirect_location_if_blocked` | Boolean | `true` | Shifts target to adjacent tile if original is invalid. |
| `remain_off_map` | Boolean | `true` | Keeps entity removed from the grid. |
| `reorient_thrown_character` | Boolean | `true` | Forces a thrown entity to face a certain way. |
| `restrictions` | Enum/String | `aoe_must_exist, none, [ must_have_buddy must_have_living_character ]` | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). |
| `restructions` | Enum/String | `aoe_must_exist` | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). |
| `reverse_target_direction` | Boolean | `true` | Inverts the targeting vector. |
| `shotgun_mode` | Boolean | `true` | Deals more damage/hits if targets are closer. |
| `shuffle_tile_order` | Boolean | `true` | Randomizes the execution order of AoE tiles. |
| `special_tile_tag` | Enum/String | `ChaosValidPosition, FinalBossCloneSpot, FinalBossTheChildLocation` | Targets only tiles with this specific tag. |
| `spin_steps` | Number | `-16` | Number of rotational increments for spin targeting. |
| `splash_damage_aoe_begin` | Number | `1, 999` | At what radius splash damage starts applying. |
| `stagger_multihit_targets` | Boolean | `true` | Delays hits slightly between multiple targets. |
| `straight_shot` | Boolean | `false, true` | Ensures projectiles do not arc. |
| `target_mode` | Enum/String | `random_tile, direction8, none` | How the cursor operates (`tile`, `direction`, `none`). |
| `target_requires_element` | Array | `[ grass ], [ grass water ]` | Target must be afflicted with this element. |
| `target_requires_tag` | Enum/String | `bowling_ball, pickup, food` | Target must possess this exact character tag. |
| `throw_consumed_character` | Boolean | `true` | Throws the entity currently held/eaten. |
| `toss_direction_restriction` | Enum/String | `forwards, backwards` | Limits which ways an entity can be tossed. |
| `track_target` | Boolean | `true` | Projectile/Effect follows moving targets. |
| `trample_allies_too` | Boolean | `true` | Trample movement damages allies in the path. |
| `uncounterable` | Boolean | `true` | Bypasses counter-attack passives. |
| `upgrade_straight_shot_to_boomerang` | Boolean | `true` | Makes the projectile return to caster. |
| `upgrade_straight_shot_to_piercing` | Boolean | `true` | Allows the projectile to pass through multiple targets. |

### Context: `temporary_effects`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AfterImage` | Block | `{ ... }` | Spawns a visual decoy or shade at the caster's previous location. |
| `BearTrapTrail` | Number | `1` | Applies or references the 'BearTrapTrail' effect/state. |
| `CastAgain` | Number | `1, 2, 4` | Applies or references the 'CastAgain' effect/state. |
| `DashFury` | Number | `4` | Applies or references the 'DashFury' effect/state. |
| `DelayedWindTrail` | Number | `1` | Applies or references the 'DelayedWindTrail' effect/state. |
| `DisableTrample` | Number | `1` | Applies or references the 'DisableTrample' effect/state. |
| `DoubleLoot` | Number | `1` | Applies or references the 'DoubleLoot' effect/state. |
| `Fury` | Number | `55, 75` | Applies or references the 'Fury' effect/state. |
| `JumpAttackLeaveBehind` | Enum/String | `BungaThrone` | Applies or references the 'JumpAttackLeaveBehind' effect/state. |
| `JustInCaseTrample` | Number | `0` | Applies or references the 'JustInCaseTrample' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `LeaveBehind` | Enum/String | `Bait, { ... }` | Spawns a specific object at the character's previous location when they move. |
| `TileTrail_Ahead` | Enum/String | `FlowerTile` | Applies or references the 'TileTrail_Ahead' effect/state. |
| `TileTrail` | Enum/String | `BrambleTile, FlowerTile, FloatingGlassTile` | Applies or references the 'TileTrail' effect/state. |
| `Trample` | Number | `1, 4, 3` | Applies or references the 'Trample' effect/state. |

---

## Characters & Bosses

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `abilities` | Block | `{ ... }` | Lists the ability IDs the character possesses. |
| `ai_if_spawned_as_enemy` | Block | `{ ... }` | AI logic override used only if the character is spawned as an enemy. |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `alt_spawn_pool` | Block | `{ ... }` | Alternative pools to draw minions from. |
| `damage_instance` | Block | `{ ... }` | Defines damage logic on contact. |
| `equipment` | Block | `{ ... }` | List of item IDs the character spawns equipped with. |
| `graphics` | Block | `{ ... }` | Visual parameters and animation bindings. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `properties` | Block | `{ ... }` | General engine properties. |
| `scale` | Enum/String | `.5` |  |
| `sound` | Block | `{ ... }` | Audio bindings. |
| `stats` | Block | `{ ... }` | Core character metrics (Health, Strength, etc.). |
| `variant_of` | Enum/String | `BirdSmall, BirdBase, Cherub` |  |

### Context: `0`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Number | `1` |  |
| `partial_animation_suffix` | Number | `1` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `uifloaters_offset` | Number | `1.4` |  |

### Context: `2`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Number | `2` |  |
| `attack` | Enum/String | `BasicMelee_2Hits, BoneWormShotMed` |  |
| `partial_animation_suffix` | Number | `2` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `uifloaters_offset` | Number | `2.2` |  |

### Context: `3`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Number | `3` |  |
| `attack` | Enum/String | `BasicMelee_3Hits, BoneWormShotTall` |  |
| `partial_animation_suffix` | Number | `3` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `uifloaters_offset` | Number | `3` |  |

### Context: `4`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Number | `4` |  |
| `attack` | Enum/String | `BasicMelee_4Hits` |  |
| `partial_animation_suffix` | Number | `4` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `5`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | Enum/String | `BasicMelee_5Hits` |  |
| `partial_animation_suffix` | Number | `5` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `AbilityHealthThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `DybbukPossess, FormShrinkThree, FormShrinkFour` | The specific ability ID to cast. |
| `also_use_if_buddy_is_dead` | Boolean | `true` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `threshold_min` | Enum/String | `X` |  |
| `threshold` | Number | `1, 3*champion_multiplier, 4*champion_multiplier` |  |
| `use_ai` | Boolean | `true` |  |

### Context: `AbilityOnRoundEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `DestroyerRaise` | The specific ability ID to cast. |
| `force_display_name` | Boolean | `true` |  |

### Context: `AbilityReaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |  |
| `ability` | Enum/String | `attack, MoonHandDash, ButtFlip` | The specific ability ID to cast. |
| `backstabs_only` | Boolean | `true` |  |
| `cancel_knockback` | Boolean | `true` |  |
| `enemies_only` | Boolean | `true` |  |
| `even_on_0_damage_if_knockback` | Boolean | `true` |  |
| `even_on_0_damage` | Boolean | `true` |  |
| `match_knockback_direction` | Boolean | `true` |  |
| `only_when_not_your_turn` | Boolean | `true` |  |
| `ranged_only` | Boolean | `true` |  |
| `verify_target` | Boolean | `true` |  |

### Context: `AbilityWhenTaggedCharacterMovesNear`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MoveTwo` | The specific ability ID to cast. |
| `range` | Number | `2, 4` | Distance or area of effect in tiles. |
| `tag` | Enum/String | `food` | Specific entity tag required. |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1, 2` | Applies or references the 'Bleed' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Burn` | Number | `1, 2, 4` | Applies or references the 'Burn' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `DamageUp` | Number | `-1` | Applies or references the 'DamageUp' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `GainDisorderFromPool` | Block | `{ ... }` | Logic: Applies a negative mutation/disorder from a specific pool. |
| `Knockback` | Number | `3` | Applies or references the 'Knockback' effect/state. |
| `Leech` | Number | `2` | Applies or references the 'Leech' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Possessed` | Number | `1` | Applies or references the 'Possessed' effect/state. |
| `RandomStatUp` | Number | `-1` | Applies or references the 'RandomStatUp' effect/state. |
| `RemoteFlatLeech` | Number | `1` | Applies or references the 'RemoteFlatLeech' effect/state. |
| `RemoteLeech` | Number | `1` | Applies or references the 'RemoteLeech' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Weakness` | Number | `1` | Applies or references the 'Weakness' effect/state. |

### Context: `AddStatusToReceivedDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_IsPhysicalAttack` | Block | `{ ... }` | Conditional: Executes logic if the triggering attack is physical. |
| `Else` | Block | `{ ... }` | Fallback logic block for conditionals. |

### Context: `AddStatusToSpells`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `2` | Applies or references the 'Leech' effect/state. |

### Context: `AddStatusToTrampleDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |

### Context: `AddStatusToWeapons`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |

### Context: `AddTemporaryEffectsToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | `75` | Applies or references the 'Fury' effect/state. |

### Context: `AdventureTokenPassivePool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `StacyMutant_Brace` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Brace' state. |
| `StacyMutant_Counter` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Counter' state. |
| `StacyMutant_Damage` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Damage' state. |
| `StacyMutant_DoubleHead` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state. |
| `StacyMutant_Fire` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Fire' state. |
| `StacyMutant_Health` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Health' state. |
| `StacyMutant_Holy` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Holy' state. |
| `StacyMutant_Ice` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Ice' state. |
| `StacyMutant_Lightning` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Lightning' state. |
| `StacyMutant_Mirror` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Mirror' state. |
| `StacyMutant_Speed` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Speed' state. |
| `StacyMutant_Thorns` | Block | `{ ... }` | Character Form: Behavior and stats for the 'StacyMutant_Thorns' state. |

### Context: `AggroTargetIsGovernedByHitEffect`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | `false` |  |

### Context: `Alert`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | Enum/String | `Alert` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `AllAlive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `AllStatsAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `aura_requires_tag` | Enum/String | `humanoid` |  |
| `range` | Enum/String | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `Angry`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | String | `"Angry"` |  |

### Context: `ArmorPickup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | Array | `[ 6 6 ], [ 3 5 ], [ 1 2 ]` |  |
| `stacks` | Number | `6, 2, 4` | Number of stacks or intensity to apply. |

### Context: `Attacker`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `ZombieTombstone` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

### Context: `BackflipWhenTargeted`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `BackflipDodge` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `BaitAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `range` | Number | `3` | Distance or area of effect in tiles. |

### Context: `BattlefieldUniqueRandomPassive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | `1` | Applies or references the 'DemonicGlyph_Bite' effect/state. |
| `DemonicGlyph_Bounce` | Number | `1` | Applies or references the 'DemonicGlyph_Bounce' effect/state. |
| `DemonicGlyph_Fire` | Number | `1` | Applies or references the 'DemonicGlyph_Fire' effect/state. |
| `DemonicGlyph_Movement` | Number | `1` | Applies or references the 'DemonicGlyph_Movement' effect/state. |
| `DemonicGlyph_Summon` | Number | `1` | Applies or references the 'DemonicGlyph_Summon' effect/state. |

### Context: `BellyFull`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | String | `"Belly"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Big`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `Big, "Big"` |  |
| `attack` | Enum/String | `GameteSpawn` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `BigHolding`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHolding"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `BigHoldingCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHoldingCat"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `BirdRewards`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ally_rewards` | Block | `{ ... }` | Loot logic triggered if an ally dies. |
| `statuses` | Block | `{ ... }` | Status effects possessed by the character. |

### Context: `Bishop`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Bishop"` |  |
| `attack` | Enum/String | `BBXLightning` |  |
| `name` | String | `"ENEMY_CULTISTBISHOP_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CULTISTBISHOP_DESC"` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |
| `uifloaters_offset` | Number | `2.5` |  |

### Context: `BlackHole`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"BlackHole"` |  |
| `name` | String | `"OBJECT_BLACKHOLE_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"OBJECT_BLACKHOLE_DESC"` |  |

### Context: `Bomb`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Button` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Boris`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `BossRewards`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `common` | Enum/String | `Blubber, RatBomb, ChubsCollar` |  |
| `rare` | Enum/String | `SpiderBaby, RadGlasses, BorisBrain` |  |

### Context: `Buddy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `false` |  |
| `obj` | Enum/String | `ZaratanaVS, PyrophinaVS, Dice` |  |
| `reclaim_if_lost` | Boolean | `true` |  |

### Context: `Bully`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `BungaCheers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ally_damage` | Enum/String | `littleboo` |  |
| `ally_dead` | Enum/String | `bigboo` |  |
| `enemy_damage` | Enum/String | `littlecheer` |  |
| `enemy_dead` | Enum/String | `bigcheer` |  |
| `warrior_tag` | Enum/String | `bungawarrior` |  |

### Context: `BungaEntrance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `BecomeTheDestroyer, BungaEntrance` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |
| `health_threshold` | Number | `150, -1` |  |
| `warrior_tag` | Enum/String | `finalboss_clonecat, bungawarrior` |  |

### Context: `Cat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `spawnHoldingCat` |  |
| `formchange` | Enum/String | `SmallHoldingCat, BigHoldingCat` |  |
| `statuses` | Block | `{ ... }` | Status effects possessed by the character. |

### Context: `CatPartsTransform`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | `1044, 1043, 1045` | Sprite variant ID for the front arm. |
| `arm2` | Number | `1044, 1043, 1045` |  |
| `body` | Number | `1024, 1013, 1012` | Sprite variant ID for the body. |
| `ear1` | Number | `1028, 1013, 1029` | Sprite variant ID for the front ear. |
| `ear2` | Number | `1013` |  |
| `eye1` | Number | `1013, 1057` |  |
| `eye2` | Number | `1013, 1057` |  |
| `head` | Number | `1020, 1019, 1027` | Sprite variant ID for the head. |
| `leg1` | Number | `1044, 1043, 1045` | Sprite variant ID for the front leg. |
| `leg2` | Number | `1044, 1043, 1045` |  |
| `palette` | Enum/String | `Hunter, Fighter, Mage` |  |
| `tail` | Number | `1034, 1035, 1036` | Sprite variant ID for the tail. |
| `texture` | Number | `19, 29, 60` |  |

### Context: `CaveBaby`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"CaveBaby"` |  |
| `attack` | Enum/String | `CaveBabyMelee` |  |
| `name` | String | `"ENEMY_CAVEBABY_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CAVEBABY_DESC"` |  |

### Context: `CaveFamilyEnrage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `CaveCatEnrageTwo, CaveCatEnrageOne` | The specific ability ID to cast. |
| `count` | Number | `1, 0` | The numerical quantity. |
| `tag` | Enum/String | `cavefamily` | Specific entity tag required. |

### Context: `CaveMan`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"CaveMan"` |  |
| `attack` | Enum/String | `CaveMan3HitCombo` |  |
| `name` | String | `"ENEMY_CAVEMANMAN_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CAVEMANMAN_DESC"` |  |

### Context: `CaveManSpear`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"SpearCaveMan"` |  |
| `attack` | Enum/String | `CaveManThrowSpear` |  |
| `name` | String | `"ENEMY_SPEARCAVEMAN_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_SPEARCAVEMAN_DESC"` |  |

### Context: `CaveWoman`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"CaveWoman"` |  |
| `attack` | Enum/String | `CaveWomanKick` |  |
| `name` | String | `"ENEMY_CAVEMANWOMAN_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN_DESC"` |  |

### Context: `CaveWomanHasCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"CatCaveWoman"` |  |
| `attack` | Enum/String | `CaveWomanCatSlap` |  |
| `name` | String | `"ENEMY_CAVEMANWOMAN2_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN2_DESC"` |  |

### Context: `CerberubsAggroTargetBehavior`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `alert_form` | Enum/String | `Alert` |  |
| `default_form` | Enum/String | `Normal` |  |

### Context: `CerberubsJumpBlind`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `CerberubsJump` | The specific ability ID to cast. |
| `decision_weights` | Enum/String | `nubs_fakeblind` |  |

### Context: `CerberubsJumpNormal`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `CerberubsJump` | The specific ability ID to cast. |
| `decision_weights` | Enum/String | `default` |  |

### Context: `ChanceToBackflip`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `DybbukBackflipDodge` | The specific ability ID to cast. |
| `chance` | Number | `100%` | Probability (0.0 to 1.0) of executing this action. |

### Context: `ChanceToFormChangeOnAbilityDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `15%` | Probability (0.0 to 1.0) of executing this action. |
| `form` | Enum/String | `Flop2` |  |

### Context: `ChanceToSpitOnDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MoonHandDrop, TinaSpit, PteroEscape` | The specific ability ID to cast. |
| `backstabs_only` | Boolean | `true` |  |
| `chance_per_damage` | Number | `0%, 2%` |  |
| `even_on_0_damage_if_knockback` | Boolean | `true` |  |
| `flat_chance` | Number | `100%, 50%` |  |

### Context: `ChaosBossFormChangeGuide`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `active_pieces` | Array | `[ Johnny Throb Flush ]` |  |
| `passive_pieces` | Array | `[ Host Nettle Bubs ]` |  |
| `passives_health_threshold` | Number | `50%` |  |

### Context: `ChaosBossPieces`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `active_pieces` | Array | `[ Johnny Throb Flush ]` |  |
| `passive_pieces` | Array | `[ Host Nettle Bubs ]` |  |

### Context: `ChaosHeadDropIn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `ChaosSpawnIn` | The specific ability ID to cast. |
| `new_music` | Enum/String | `chaos_boss_part2` |  |
| `tag` | Enum/String | `riftheadguardian` | Specific entity tag required. |

### Context: `CharacterLightSource`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `color` | Array | `[ .8, .9, 1 ], [ .7, .8, .9 ], [ .3, .7, 1 ]` |  |
| `glow` | Array | `[ 1, 1, 1, .5 ], [ .7, .8, .9, .5 ], [ .3, .7, 1, .5 ]` |  |
| `size` | Number | `2, 1.5, 4` |  |

### Context: `Charging`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `MoonHead_Blow` |  |
| `partial_animation_suffix` | String | `"Charging"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `CherubimReaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Leave` | Enum/String | `LELeave, CherubimLeave` | Applies or references the 'Leave' effect/state. |
| `Return` | Enum/String | `LEReturn, CherubimReturn` | Applies or references the 'Return' effect/state. |

### Context: `Close`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `CloseConvert`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MarshmallowConvert` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `stay_close` |  |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `odds` | Number | `0.5` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | Enum/String | `chapter` | Generates an item drop from the specified loot pool. |
| `odds` | Number | `5%, 33%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

### Context: `Conditional_HasKnockback`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `KnockUpAndAway` | Block | `{ ... }` | Logic: Applies vertical and horizontal displacement. |
| `RemoveKnockback` | Number | `1` | Applies or references the 'RemoveKnockback' effect/state. |
| `TempPassiveUntilSettled` | Block | `{ ... }` | Passive: Active only until the physics engine stops moving the character. |

### Context: `Conditional_IsPhysicalAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `KnockUpAndAway` | Block | `{ ... }` | Logic: Applies vertical and horizontal displacement. |
| `RemoveKnockback` | Number | `1` | Applies or references the 'RemoveKnockback' effect/state. |
| `TempPassiveUntilSettled` | Block | `{ ... }` | Passive: Active only until the physics engine stops moving the character. |

### Context: `Consumed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_not_pop_corpse` | Boolean | `true` |  |
| `drop_on_death` | Enum/String | `deferred` |  |
| `force_contact` | Boolean | `true` | If true, enforces physical overlap. |
| `instant` | Boolean | `true` |  |
| `mount_mode` | Enum/String | `auto` | If true, treats the consumption as riding/mounting instead of eating. |
| `struggle_ability` | Enum/String | `Thrash` | Ability triggered by the consumed entity while inside the consumer. |
| `use_placeholder` | Boolean | `true` |  |

### Context: `CounterAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `StegoTailSwipe` | The specific ability ID to cast. |
| `without_orienting` | Boolean | `true` |  |

### Context: `CreateGlobalModifiers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | `1` | Applies or references the 'BloodRain' effect/state. |
| `LowerAmbientLight` | Block | `{ ... }` | Visual: Dims the map lighting. |

### Context: `Cultist`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Cultist"` |  |
| `attack` | Enum/String | `BasicMelee` |  |
| `name` | String | `"ENEMY_CULTISTLACKEY_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CULTISTLACKEY_DESC"` |  |

### Context: `Damaged`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `DashRandomly`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `ShamblerDash` | The specific ability ID to cast. |
| `decision_weights` | Enum/String | `blind` |  |

### Context: `DeathRattle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `UFO_SpelunkyDeath, JarHeadDeath, MoonHandDrop_Deathrattle` | The specific ability ID to cast. |
| `cancel_knockback` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `is_dying_animation` | Boolean | `true` |  |
| `must_target_killer` | Boolean | `true` |  |
| `pop_corpse` | Boolean | `false` |  |
| `target_killer` | Boolean | `true` |  |

### Context: `DeathRattleRevive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `HitlerPulp1, AZ_LoseHead, HitlerPulp2` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |

### Context: `Default`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `LennyShove` |  |
| `move` | Enum/String | `LennyTrampleMove` |  |
| `partial_animation_suffix` | String | `""` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Default_Ceiling`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Default_Ground`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `DelayedAutoRevive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%` |  |
| `rounds` | Number | `1` |  |

### Context: `DesireMech`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `DiceBehavior`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number | `6` |  |
| `knockback_damage` | Number | `5` |  |

### Context: `Die`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `DiesToElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Fire` | Specific element type required or applied. |
| `instant` | Boolean | `true` |  |

### Context: `DiesToPiercingAndSpikes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean | `true` |  |

### Context: `DodgeWhenTargeted`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `ShadowstepDodge` | The specific ability ID to cast. |

### Context: `Down`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Down"` |  |
| `attack` | Enum/String | `ButtFart` |  |
| `move` | Enum/String | `TeleportFlipUp` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Drunker`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Drunk` |  |

### Context: `DualSword`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"2"` |  |
| `attack` | Enum/String | `DestroyerAttack2` |  |
| `move_speed_multiplier` | Number | `1.5` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |  |

### Context: `DualSword_Primed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Holy2"` |  |
| `attack` | Enum/String | `DestroyerAttack2` |  |
| `move_speed_multiplier` | Number | `1.5` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |  |

### Context: `Dumb`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `DybbukPossessionFallback`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit_ability` | Enum/String | `DybbukReturn` |  |
| `form` | Enum/String | `Possessing` |  |

### Context: `Else`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_HasKnockback` | Block | `{ ... }` | Conditional: Executes logic if the triggering attack deals knockback. |

### Context: `Empty`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `""` |  |

### Context: `Escape`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `DybbukEscape` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `keep_distance_always_move` |  |

### Context: `Explody`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Expl` |  |
| `attack` | Enum/String | `ToxExplode` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Explosive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"3"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `FaceAwayLastDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |  |
| `override_hit_animation` | Boolean | `true` |  |
| `use_turn_animations` | Boolean | `true` |  |

### Context: `FaceLastDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | `true` |  |

### Context: `FightPhase`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `T3Shoot` |  |
| `move` | Enum/String | `FloatMove` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `FinalBossBeamQueue`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `queue` | Enum/String | `TheChild_TargetBeam` |  |
| `release` | Enum/String | `TheChild_ReleaseBeams` |  |
| `transform` | Enum/String | `TheChild_TransformBoris` |  |

### Context: `FinalBossBecomeTheChild`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | Enum/String | `MegaGuppy` | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `PlayBackground` | Number | `1` | Applies or references the 'PlayBackground' effect/state. |
| `SwitchMusic` | Block | `{ ... }` | Event Trigger: Changes background music track. |

### Context: `FinalBossHitCountdownBoris`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `TheChild_TransformExplosive, { ... }` | Logic: Forces the execution of a specific ability. |
| `icon_ready` | Number | `803` |  |
| `icon` | Number | `802` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

### Context: `FinalBossHitCountdownExplosive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `TheChild_TransformHoly, { ... }` | Logic: Forces the execution of a specific ability. |
| `icon_ready` | Number | `801` |  |
| `icon` | Number | `800` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

### Context: `FinalBossHitCountdownHoly`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `icon_ready` | Number | `805` |  |
| `icon` | Number | `804` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

### Context: `FinalBossPupils`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `look_at_offset` | Array | `[ 0 2.5 0 ]` |  |
| `radius` | Number | `13` | Distance or area of effect in tiles. |
| `reset_center_because_no_target_halflife` | Enum/String | `.1` |  |
| `reset_center_because_of_animation_halflife` | Enum/String | `.05` |  |
| `teleport_tracking_halflife` | Enum/String | `.01` |  |
| `tracking_acquisition_halflife` | Enum/String | `.1` |  |
| `virtual_head_position` | Array | `[ 11 2 11 ]` |  |

### Context: `FinalBossShieldHealth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `break_ability` | Enum/String | `DestroyerBreakShield` |  |
| `state_health` | Array | `[ 0 35 35 35 35 0 ]` |  |

### Context: `FinalBossSyncAnimations`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `other_character` | Enum/String | `MegaGuppy` |  |
| `other_form_change_abilities` | Block | `{ ... }` | Lists secondary abilities used to change forms. |

### Context: `Fire`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `SpewerLobbed_Lava` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `FireFull`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Full` |  |
| `attack` | Enum/String | `SpewerSpit` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Flop`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Down"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Flop2`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Down"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Flush`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `FlushBubs`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `FlushHost`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | Enum/String | `Host` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `FlushNettle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `FoodMove`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `CaveBabyFoodMove` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `stay_close_move_if_possible` |  |

### Context: `ForceTrample`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `BirthwortTrample` | The specific ability ID to cast. |
| `decision_weights` | Enum/String | `always_cast_careless` |  |

### Context: `ForceUseAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `TheChild_Wrath, TheChild_Pulse` | The specific ability ID to cast. |
| `show_name` | Boolean | `true` |  |

### Context: `FormChangeDuringWeatherElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Water` | Specific element type required or applied. |
| `form` | Enum/String | `Rain` |  |

### Context: `FormChangeHealthThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count_shield` | Boolean | `true` |  |
| `form_above` | Enum/String | `Full, Default, Standing` |  |
| `form_below` | Enum/String | `Standing2, DesireMech, Damaged` |  |
| `threshold` | Number | `25, 50, X-4` |  |

### Context: `FormChangeOffMap`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `form_offmap` | Enum/String | `Start_Ceiling, Default_Ceiling, Insane_Ceiling` |  |
| `form_onmap` | Enum/String | `Default_Ground, Default, Insane_Ground` |  |

### Context: `FormChangeOnElementInfluence`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `wind, very_hot, water` | Specific element type required or applied. |
| `exclude` | Enum/String | `fire, water` |  |
| `form` | Enum/String | `hot, Unlit, default` |  |
| `particle` | Enum/String | `FireExtinguish` |  |
| `sfx` | Enum/String | `FireExtinguish` |  |

### Context: `FormChangeWhileHasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `form_has` | Enum/String | `Full, HasRock, HasCat` |  |
| `form_hasnot` | Enum/String | `Default, Small, Big` |  |
| `status` | Enum/String | `Consuming, Grappling, Counterspell` | ID of the status effect to apply or check. |

### Context: `FormChangeWhilePrimingAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `not_priming` | Enum/String | `SwordAndShield, DualSword, NotPriming` |  |
| `priming` | Enum/String | `SwordAndShield_Primed, Priming, DualSword_Primed` |  |

### Context: `FormChanger`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Alert` | Block | `{ ... }` | AI State: The behavior profile used when the character is alerted to enemies. |
| `AllAlive` | Block | `{ ... }` | Encounter State: Logic executed when all specific entities are currently alive. |
| `Angry` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'Angry' state. |
| `Attacker` | Block | `{ ... }` | AI Role: Designates the character as an attacker rather than support. |
| `BellyFull` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'BellyFull' state. |
| `BigHoldingCat` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'BigHoldingCat' state. |
| `BigHolding` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'BigHolding' state. |
| `Big` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'Big' state. |
| `Bishop` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'Bishop' state. |
| `BlackHole` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'BlackHole' state. |
| `Bomb` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'Bomb' state. |
| `Boris` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'Boris' state. |
| `Bully` | Block | `{ ... }` | Character Form / AI State: Behavior and stats for the 'Bully' state. |
| `Butcher` | Block | `{ ... }` | Applies or references the 'Butcher' effect/state. |
| `CaveBaby` | Block | `{ ... }` | Character Form: Behavior and stats for the 'CaveBaby' state. |
| `CaveManSpear` | Block | `{ ... }` | Character Form: Behavior and stats for the 'CaveManSpear' state. |
| `CaveMan` | Block | `{ ... }` | Character Form: Behavior and stats for the 'CaveMan' state. |
| `CaveWomanHasCat` | Block | `{ ... }` | Character Form: Behavior and stats for the 'CaveWomanHasCat' state. |
| `CaveWoman` | Block | `{ ... }` | Character Form: Behavior and stats for the 'CaveWoman' state. |
| `Charging` | Block | `{ ... }` | Character Form / AI State: Behavior when charging an attack. |
| `Close` | Block | `{ ... }` | AI Movement logic: Maneuvers into close/melee range. |
| `Colorless` | Block | `{ ... }` | Applies or references the 'Colorless' effect/state. |
| `Cultist` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Cultist' state. |
| `Damaged` | Block | `{ ... }` | Character Form / AI State: Behavior when health is critically low. |
| `Default_Ceiling` | Block | `{ ... }` | Character Form: The baseline behavior state while attached to the ceiling. |
| `Default_Ground` | Block | `{ ... }` | Character Form: The baseline behavior state while on the ground. |
| `Default` | Block | `{ ... }` | Character Form: The baseline default behavior state. |
| `DesireMech` | Block | `{ ... }` | Character Form: Behavior and stats for the 'DesireMech' state. |
| `Die` | Block | `{ ... }` | Character Form / Logic: Forces the character to die. |
| `Down` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Down' state. |
| `Druid` | Block | `{ ... }` | Applies or references the 'Druid' effect/state. |
| `Drunker` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Drunker' state. |
| `DualSword_Primed` | Block | `{ ... }` | Character Form: Behavior and stats for the 'DualSword_Primed' state. |
| `DualSword` | Block | `{ ... }` | Character Form: Behavior and stats for the 'DualSword' state. |
| `Dumb` | Block | `{ ... }` | AI Profile: A simplified, less optimal decision-making profile. |
| `Empty` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Empty' state. |
| `Explody` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Explody' state. |
| `Explosive` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Explosive' state. |
| `FightPhase` | Block | `{ ... }` | Boss Logic: Main combat phase. |
| `Fighter` | Block | `{ ... }` | Applies or references the 'Fighter' effect/state. |
| `FireFull` | Block | `{ ... }` | Character Form: Behavior and stats for the 'FireFull' state. |
| `Fire` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Fire' state. |
| `Flop2` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Flop2' state. |
| `Flop` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Flop' state. |
| `FlushBubs` | Block | `{ ... }` | Character Form: Behavior and stats for the 'FlushBubs' state. |
| `FlushHost` | Block | `{ ... }` | Character Form: Behavior and stats for the 'FlushHost' state. |
| `FlushNettle` | Block | `{ ... }` | Character Form: Behavior and stats for the 'FlushNettle' state. |
| `Flush` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Flush' state. |
| `Full` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Full' state. |
| `Grappling` | Block | `{ ... }` | Character Form / AI State: Behavior while grappling an opponent. |
| `Grown` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Grown' state. |
| `GuaranteedJackpot` | Block | `{ ... }` | Loot Logic: Guarantees a high-tier drop. |
| `Guarding` | Block | `{ ... }` | Character Form / AI State: Defensive behavior state. |
| `HalfDead` | Block | `{ ... }` | Character Form: Behavior and stats for the 'HalfDead' state. |
| `HasCat` | Block | `{ ... }` | Character Form: Behavior and stats for the 'HasCat' state. |
| `HasDeadCat` | Block | `{ ... }` | Character Form: Behavior and stats for the 'HasDeadCat' state. |
| `HasRock` | Block | `{ ... }` | Character Form: Behavior and stats for the 'HasRock' state. |
| `Headless` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Headless' state. |
| `Hint_CrackedVisuals2` | Block | `{ ... }` | Visual: Secondary cracked visual overlay. |
| `Hint_CrackedVisuals3` | Block | `{ ... }` | Visual: Tertiary cracked visual overlay. |
| `Hint_CrackedVisuals` | Block | `{ ... }` | Visual: Overlay effects for cracked/damaged terrain or objects. |
| `Holding` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Holding' state. |
| `Holy` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Holy' state. |
| `HumanDead` | Block | `{ ... }` | Character Form: Behavior and stats for the 'HumanDead' state. |
| `Hunter` | Block | `{ ... }` | Applies or references the 'Hunter' effect/state. |
| `InitialPhase` | Block | `{ ... }` | Boss Logic: The starting phase of an encounter. |
| `Insane_Ceiling` | Block | `{ ... }` | Character Form: Insane behavior state while attached to the ceiling. |
| `Insane_Ground` | Block | `{ ... }` | Character Form: Insane behavior state while on the ground. |
| `JohnnyBubs` | Block | `{ ... }` | Character Form: Behavior and stats for the 'JohnnyBubs' state. |
| `JohnnyHost` | Block | `{ ... }` | Character Form: Behavior and stats for the 'JohnnyHost' state. |
| `JohnnyNettle` | Block | `{ ... }` | Character Form: Behavior and stats for the 'JohnnyNettle' state. |
| `Johnny` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Johnny' state. |
| `Joystick` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Joystick' state. |
| `LastHit` | Block | `{ ... }` | Logic: Executes logic on the final hit of a multi-hit attack. |
| `Lifted` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Lifted' state. |
| `Lit` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Lit' state. |
| `Mage` | Block | `{ ... }` | Applies or references the 'Mage' effect/state. |
| `Medic` | Block | `{ ... }` | Applies or references the 'Medic' effect/state. |
| `Monk` | Block | `{ ... }` | Applies or references the 'Monk' effect/state. |
| `Mounted` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Mounted' state. |
| `MouthFull` | Block | `{ ... }` | Character Form: Behavior and stats for the 'MouthFull' state. |
| `Mutant` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Mutant' state. |
| `Necromancer` | Block | `{ ... }` | Applies or references the 'Necromancer' effect/state. |
| `NeutronStar` | Block | `{ ... }` | Character Form: Behavior and stats for the 'NeutronStar' state. |
| `NoDeathRattle` | Block | `{ ... }` | Applies or references the 'NoDeathRattle' effect/state. |
| `NoEyes` | Block | `{ ... }` | Character Form: Behavior and stats for the 'NoEyes' state. |
| `NoStick` | Block | `{ ... }` | Character Form: Behavior and stats for the 'NoStick' state. |
| `NormalFull` | Block | `{ ... }` | Character Form: Behavior and stats for the 'NormalFull' state. |
| `Normal` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Normal' state. |
| `NotPriming` | Block | `{ ... }` | Character Form: Behavior and stats when not charging an ability. |
| `Nuke` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Nuke' state. |
| `Obey` | Block | `{ ... }` | AI State: Enforced compliance logic (e.g., when Charmed). |
| `OffMap` | Block | `{ ... }` | Character Form: Behavior and stats for the 'OffMap' state. |
| `OffScreen` | Block | `{ ... }` | Character Form: Behavior and stats for the 'OffScreen' state. |
| `Off` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Off' state. |
| `OneAlive` | Block | `{ ... }` | Encounter State: Logic executed when exactly one target is alive. |
| `OneEye` | Block | `{ ... }` | Character Form: Behavior and stats for the 'OneEye' state. |
| `OpenCat` | Block | `{ ... }` | Character Form: Behavior and stats for the 'OpenCat' state. |
| `Open` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Open' state. |
| `Out` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Out' state. |
| `Possessing` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Possessing' state. |
| `Primed` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Primed' state. |
| `Priming` | Block | `{ ... }` | Character Form: Behavior and stats when charging an ability. |
| `Psychic` | Block | `{ ... }` | Applies or references the 'Psychic' effect/state. |
| `Pulp2` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Pulp2' state. |
| `Pulp3` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Pulp3' state. |
| `Pulp4` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Pulp4' state. |
| `Pulp5` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Pulp5' state. |
| `Pulp6` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Pulp6' state. |
| `Pulp7` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Pulp7' state. |
| `Rage` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Rage' state. |
| `Rain` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Rain' state. |
| `Sitting` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Sitting' state. |
| `SmallHoldingCat` | Block | `{ ... }` | Character Form: Behavior and stats for the 'SmallHoldingCat' state. |
| `SmallHolding` | Block | `{ ... }` | Character Form: Behavior and stats for the 'SmallHolding' state. |
| `Small` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Small' state. |
| `SpawningPhase` | Block | `{ ... }` | Boss Logic: Phase focused on summoning minions. |
| `SquirrelForm` | Block | `{ ... }` | Character Form: Behavior and stats for the 'SquirrelForm' state. |
| `Standing2` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Standing2' state. |
| `Standing` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Standing' state. |
| `Start_Ceiling` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Start_Ceiling' state. |
| `Stop` | Block | `{ ... }` | AI Movement: Forces the character to cease movement. |
| `SwordAndShield_Primed` | Block | `{ ... }` | Character Form: Behavior and stats for the 'SwordAndShield_Primed' state. |
| `SwordAndShield` | Block | `{ ... }` | Character Form: Behavior and stats for the 'SwordAndShield' state. |
| `Tank` | Block | `{ ... }` | Applies or references the 'Tank' effect/state. |
| `TarFull` | Block | `{ ... }` | Character Form: Behavior and stats for the 'TarFull' state. |
| `Tar` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Tar' state. |
| `Thief` | Block | `{ ... }` | Applies or references the 'Thief' effect/state. |
| `ThrobBubs` | Block | `{ ... }` | Character Form: Behavior and stats for the 'ThrobBubs' state. |
| `ThrobHost` | Block | `{ ... }` | Character Form: Behavior and stats for the 'ThrobHost' state. |
| `ThrobNettle` | Block | `{ ... }` | Character Form: Behavior and stats for the 'ThrobNettle' state. |
| `Throb` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Throb' state. |
| `Tinkerer` | Block | `{ ... }` | Applies or references the 'Tinkerer' effect/state. |
| `Transformed` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Transformed' state. |
| `Turtled` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Turtled' state. |
| `TwoAlive` | Block | `{ ... }` | Encounter State: Logic executed when exactly two targets are alive. |
| `TwoEyes` | Block | `{ ... }` | Character Form: Behavior and stats for the 'TwoEyes' state. |
| `Unlit` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Unlit' state. |
| `Unmounted` | Block | `{ ... }` | Applies or references the 'Unmounted' effect/state. |
| `Unwashed` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Unwashed' state. |
| `Up` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Up' state. |
| `Washed` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Washed' state. |
| `Washer` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Washer' state. |
| `Water` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Water' state. |
| `WereMan` | Block | `{ ... }` | Character Form: Behavior and stats for the 'WereMan' state. |
| `ZealotBomb` | Block | `{ ... }` | Character Form: Behavior and stats for the 'ZealotBomb' state. |
| `Zealot` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Zealot' state. |
| `active` | Block | `{ ... }` | Defines actively executed abilities. |
| `default` | Block | `{ ... }` | Baseline configuration. |
| `hot` | Block | `{ ... }` | Visual effect indicator. |
| `initial_form` | Enum/String | `Default, Flop, Up` |  |
| `passive` | Block | `{ ... }` | Intrinsic passive modifier. |
| `sync_brain_patterns` | Boolean | `true` |  |

### Context: `Full`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Full"` |  |
| `attack` | Enum/String | `KirbySpit` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `statuses_on_enter_form` | Block | `{ ... }` | Status effects instantly applied upon transitioning into this form. |

### Context: `GainDisorderFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.1` | Probability (0.0 to 1.0) of executing this action. |
| `pool` | Enum/String | `diseases` |  |

### Context: `Grappling`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit_animations` | Block | `{ ... }` | Animations played when leaving a form/state. |
| `partial_animation_suffix` | Enum/String | `Grapple` |  |

### Context: `Grown`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Grown` |  |
| `attack` | Enum/String | `HitlerCloneSwipes` |  |
| `name` | String | `"ENEMY_HITLERCLONE_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `uifloaters_offset` | Number | `1.5` |  |
| `weak_threshold` | Number | `15` |  |

### Context: `GuaranteedJackpot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Guarding`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | String | `"Guarding"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `HPAltStates`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `clipname` | Enum/String | `poopmain` |  |
| `thresholds` | Array | `[ [ 1 0 ]` |  |

### Context: `HalfDead`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"2"` |  |
| `attack` | Enum/String | `RatKingDash` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `HasCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Grabbing", "Cat"` |  |
| `attack` | Enum/String | `MoonHead_ChewCat, PteroPeck, MoonHandSqueeze` |  |
| `move` | Enum/String | `None` |  |
| `partial_animation_suffix` | String | `"Swallowed"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `HasDeadCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"CatDead"` |  |
| `attack` | Enum/String | `LennyCatSlap` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `HasRock`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"rock"` |  |
| `attack` | Enum/String | `AmoebaRockBash` |  |

### Context: `Headless`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Headless"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `HealNeighborsEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

### Context: `HealthPickup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `anything_eats` | Boolean | `true` |  |
| `force_frame` | Number | `12` |  |
| `frame_range` | Array | `[ 3 4 ], [ 5 5 ], [ 1 2 ]` |  |
| `stacks` | Number | `7, 4, 10` | Number of stacks or intensity to apply. |
| `stored_food_value` | Number | `1, 2, 3` |  |

### Context: `Hint_CrackedVisuals`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cracked"` |  |

### Context: `Hint_CrackedVisuals2`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"ChargingCracked"` |  |

### Context: `Hint_CrackedVisuals3`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"SwallowedCracked"` |  |

### Context: `HitlerExecute`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `HitlerShoot` | The specific ability ID to cast. |
| `tag` | Enum/String | `grown_hitler_clone` | Specific entity tag required. |
| `threshold` | Number | `15` |  |

### Context: `Holding`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | String | `"Holding"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Holy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `HumanDead`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `DH` |  |
| `attack` | Enum/String | `HCSpin` |  |
| `tooltip` | String | `"ENEMY_HUMANCAT2_DESC"` |  |

### Context: `ImmediateAbilityReaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |  |
| `ability` | Enum/String | `ButtWeb, ButtWeb_AlreadyEnraged, AlienBeastGoop` | The specific ability ID to cast. |
| `backstabs_only` | Boolean | `true` |  |
| `buddy_damage_only` | Boolean | `true` |  |
| `damage_threshold` | Number | `10` |  |
| `even_if_blocked` | Boolean | `true` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `health_threshold` | Number | `70, 50` |  |
| `target_furthest_valid` | Boolean | `true` |  |

### Context: `InfiniteRebirth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `25%` |  |
| `immediate` | Boolean | `true` |  |
| `playercat_health` | Number | `25%` |  |

### Context: `InitialPhase`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `T3Shoot` |  |
| `move` | Enum/String | `FloatMove` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Insane_Ceiling`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Insane"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Insane_Ground`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Insane"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Johnny`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `JohnnyBubs`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `JohnnyHost`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | Enum/String | `Host` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `JohnnyNeedsWashing`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `form_unwashed` | Enum/String | `Unwashed` |  |
| `form_washed` | Enum/String | `Washed` |  |

### Context: `JohnnyNettle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Joystick`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Joystick"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `KnockUpAndAway`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean | `true` |  |
| `distance` | Number | `3` | The distance in tiles to knock the target away. |
| `self_damage` | Boolean | `false` | Recoil or self-inflicted damage/effects applied to the caster. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

### Context: `LastHit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `LeapClose`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `GKLeap` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `towards_aggro` |  |

### Context: `Lifted`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Lift"` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Lit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Lit` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `LowerAmbientLight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | Array | `[ 50% 60% 60% ]` | The target opacity/dimness level. |
| `speed` | Number | `4` | The transition speed. |

### Context: `ManaPickup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | Array | `[ 6 6 ], [ 3 5 ], [ 1 2 ]` |  |
| `stacks` | Number | `6, 2, 4` | Number of stacks or intensity to apply. |

### Context: `MegaDinoDropController`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `head_drop` | Enum/String | `MD_HeadDrop` |  |
| `leg_leave` | Enum/String | `MD_LegLeave` |  |
| `leg_return` | Enum/String | `MD_LegReturn` |  |
| `stable_legs` | Number | `3` |  |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `5, 0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging impact triggers. |
| `elements` | Array | `[ Fire ]` |  |
| `knockback` | Number | `2, 4, 3` |  |
| `type` | Enum/String | `none, status` | Classification/category type. |

### Context: `ModularPickup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `sound_event` | Enum/String | `EatAntidote` |  |

### Context: `MonkCatReactionAbilities`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | Enum/String | `attack` |  |
| `move` | Enum/String | `move` |  |
| `spell` | Enum/String | `MCHadouken` |  |
| `trinket` | Enum/String | `MCHadouken` |  |
| `weapon` | Enum/String | `attack` | Weapon item constraint. |

### Context: `MotherGrowController`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `eat_damage` | Block | `{ ... }` | Damage dealt when this entity consumes another. |
| `tumor_object` | Enum/String | `MotherTumor` |  |

### Context: `MotherTumorPassive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Cat` | Block | `{ ... }` | Character Form: Base form for standard cats. |
| `NonCat` | Block | `{ ... }` | Character Form: Behavior and stats for the 'NonCat' state. |
| `considered_forms` | Array | `[ Big BigHolding BigHoldingCat ]` |  |
| `grow_ability` | Enum/String | `MotherTumorGrow` |  |
| `pass_ani` | Enum/String | `pass` |  |
| `receive_ani` | Enum/String | `receive` |  |

### Context: `MotherTumorSpawnInCapture`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Cat` | Block | `{ ... }` | Character Form: Base form for standard cats. |
| `NonCat` | Block | `{ ... }` | Character Form: Behavior and stats for the 'NonCat' state. |
| `Nothing` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Nothing' state. |

### Context: `Mount`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `eject_ability` | Enum/String | `MechSuitEject` |  |
| `enter_ability` | Enum/String | `EnterMech` |  |

### Context: `Mounted`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cat"` |  |

### Context: `MouthFull`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | String | `"MouthFull"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `MoveAfterAnyAttemptedAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | Enum/String | `bat_chaos_runaway` |  |

### Context: `MoveAway`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MoveTwoCantrip, DoubleDistanceMove, ExtraMove` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `keep_distance_always_move, stay_far, blind_move_far` |  |

### Context: `MoveAwayFromDamageSource`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | Enum/String | `BirdFly` |  |

### Context: `MoveAwayWhenEnemyAdjacent`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | Enum/String | `YA_Jetpack` |  |
| `once_per_turn` | Boolean | `true` |  |
| `weights` | Enum/String | `stay_far_always_move` |  |

### Context: `MoveCenter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `stay_near_map_center` |  |

### Context: `MoveClose`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `attack, Spin_Enemy` |  |
| `move_weights` | Enum/String | `stay_close_avoid_allies, stay_close, stay_close_always_move` |  |

### Context: `MoveForBarrage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `ZaratanaVSBombardment` |  |
| `move_weights` | Enum/String | `stay_far` |  |

### Context: `MoveForDash`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `attack` |  |
| `move_weights` | Enum/String | `keep_distance` |  |

### Context: `MoveForGrass`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `StegoGrassStomp` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `StegoEatGrass` |  |
| `move_weights` | Enum/String | `minimum_move` |  |

### Context: `MoveForPounce`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `attack` |  |
| `move_weights` | Enum/String | `keep_distance` |  |

### Context: `MoveForSpin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `PyrophinaVSRun` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `PyrophinaVSSpinThrow` |  |
| `move_weights` | Enum/String | `stay_close` |  |

### Context: `MoveForThrow`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `PyrophinaSoloCatThrow, PyrophinaVSCatThrow` |  |
| `move_weights` | Enum/String | `util_minmove` |  |

### Context: `MoveOneForPuke`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `AlienBeastMoveOne` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `AlienBeastPuke` |  |
| `move_weights` | Enum/String | `keep_distance` |  |

### Context: `MoveSpaced`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `terminator_keep_distance_always_move` |  |

### Context: `MoveToHead`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `G3RunToHead` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `G3GrabHead` |  |
| `move_weights` | Enum/String | `minimum_move` |  |

### Context: `MoveTowards`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `attack` |  |
| `move_weights` | Enum/String | `stay_close` |  |

### Context: `MoveTowardsDamageSource`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The specific ability ID to cast. |
| `can_move_zero` | Boolean | `true` |  |
| `check_has_status` | Enum/String | `FinalBossHitCountdownBoris` |  |
| `check_in_form` | Enum/String | `Boris, Default` |  |
| `do_not_move_on_top` | Boolean | `true` |  |
| `face_towards_after` | Boolean | `true` |  |
| `ignore_tagged_sources` | Enum/String | `megadino` |  |
| `move_ability` | Enum/String | `MD_WalkOne, MoveOne` |  |
| `move_far` | Boolean | `false` |  |
| `move_short` | Boolean | `true` |  |

### Context: `MoveTowardsKillers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `character_filter` | Array | `[ SpiderCat, TallSpiderCat ]` |  |
| `move_ability` | Enum/String | `SpiderReturn` |  |

### Context: `MoveWhenDamaged`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | Enum/String | `WaterTrailMove` |  |
| `weights` | Enum/String | `stay_near_allies_always_move, chaotic, stay_far_always_move` |  |

### Context: `MovementReaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MoonHead_EatCat, weapon, MoonHandGrab` | The specific ability ID to cast. |
| `blind_spot` | Boolean | `true` |  |
| `enemies_only` | Boolean | `false, true` |  |
| `forward_only` | Boolean | `true` |  |
| `objects_too` | Boolean | `true` |  |
| `on_self_move_too` | Boolean | `true` |  |
| `self_move_exclude_self_abilities` | Boolean | `true` |  |

### Context: `MultiSpawnOnDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Array | `[ 0, 2 ]` | The numerical quantity. |
| `obj` | Enum/String | `Maggot` |  |

### Context: `Mutant`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Mutant"` |  |
| `attack` | Enum/String | `BBMutantSwipe` |  |
| `move_speed_multiplier` | Enum/String | `.5` |  |
| `name` | String | `"ENEMY_CULTISTMUTANT_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CULTISTMUTANT_DESC"` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `NCGravecrawlFAR`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `NCGravecrawl` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `stay_far` |  |

### Context: `NeutronStar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `NoEyes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"0"` |  |

### Context: `NoStick`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `ManglerJab` |  |

### Context: `NonCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `spawnHolding` |  |
| `formchange` | Enum/String | `SmallHolding, BigHolding` |  |
| `statuses` | Block | `{ ... }` | Status effects possessed by the character. |

### Context: `Normal`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Up"` |  |
| `attack` | Enum/String | `SpewerLobbed_Normal, TinaBasicBigMeleeA` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `NormalFull`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Full` |  |
| `attack` | Enum/String | `SpewerSpit` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `NotPriming`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Nothing`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `spawn` |  |

### Context: `Nuke`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Nuke` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Obey`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Off`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `Off` |  |

### Context: `OffMap`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `OffScreen`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `OneAlive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `OneEye`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Open`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Open` |  |
| `attack` | Enum/String | `GSOpenAttack` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `OpenCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum/String | `OpenCat` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Out`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `PassiveGroup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `ExtraBasicAttacks` | Number | `1` | Applies or references the 'ExtraBasicAttacks' effect/state. |
| `FormChange` | Enum/String | `Hunter, Fighter, Mage` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `ReplaceBasicAttack` | Enum/String | `BasicRanged, BasicMelee, BasicMagicShortRanged` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `SelfStatusCarefulness` | Number | `1` | Applies or references the 'SelfStatusCarefulness' effect/state. |
| `StatusCarefulness` | Number | `1` | Applies or references the 'StatusCarefulness' effect/state. |
| `TinkererBasicAttackSwitching` | Block | `{ ... }` | Logic: Allows Tinkerer to swap basic attacks. |

### Context: `PassiveWhenAffectedByElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Fire` | Specific element type required or applied. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `PassiveWhenDead`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToTrampleDamage` | Block | `{ ... }` | Modifier: Injects a status effect into the character's trample damage. |

### Context: `PassiveWhileHasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `status` | Enum/String | `DemonicGlyph_Fire, DemonicGlyph_Summon, DemonicGlyph_Bite` | ID of the status effect to apply or check. |

### Context: `PassiveWhileNotHasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `status` | Enum/String | `DemonicGlyph_Movement, ExistUntilIdleUpkeep` | ID of the status effect to apply or check. |

### Context: `Possessing`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Possessing"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Primed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `GA_Telekinesis_Big` |  |
| `partial_animation_suffix` | Enum/String | `primed` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Priming`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `ProtectTargetedAllies`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `SwapPositions_TankCat` | The specific ability ID to cast. |
| `target_filter` | Enum/String | `any, Kitten` |  |

### Context: `Pulp2`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `2` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |
| `uifloaters_offset` | Number | `1` |  |

### Context: `Pulp3`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `3` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |
| `uifloaters_offset` | Number | `1` |  |

### Context: `Pulp4`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `4` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |
| `uifloaters_offset` | Number | `1` |  |

### Context: `Pulp5`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `5` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |
| `uifloaters_offset` | Number | `1` |  |

### Context: `Pulp6`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `6` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |
| `uifloaters_offset` | Number | `1` |  |

### Context: `Pulp7`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `7` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | Enum/String | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `turns` | Block | `{ ... }` | Turn counter tracking. |
| `uifloaters_offset` | Number | `1` |  |

### Context: `Rage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Rage"` |  |
| `attack` | Enum/String | `ChubsSpinRage` |  |
| `move_speed_multiplier` | Number | `2` |  |
| `partial_animation_suffix` | String | `"Rage"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Rain`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `RandomPassivePool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Modifier: Injects a status effect payload into the character's basic attacks. |
| `PassiveGroup` | Block | `{ ... }` | Passive: A collection of passives grouped together for easier management. |
| `TransformInXTurns` | Block | `{ ... }` | Logic: Forces a form change after X turns. |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `StatusGroup` | Block | `{ ... }` | Logic: Groups statuses for batch application. |

### Context: `ReflectProjectiles`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | `2` | Recoil or self-inflicted damage/effects applied to the caster. |

### Context: `RemoveStatusStacks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1, 10` | The number of stacks to remove. |
| `status` | Enum/String | `DodgeChance_Status, Brace` | The specific status effect ID to remove. |

### Context: `ReplaceBrain`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | Enum/String | `PatternBrain` |  |
| `decision_weights` | Enum/String | `default` |  |
| `move_weights` | Enum/String | `keep_distance, stay_close` |  |
| `pattern` | Block | `{ ... }` | AI sequence logic. |

### Context: `ReturnA`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `HangerBotReturn` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `stay_close` |  |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `knockback` | Number | `5` |  |
| `type` | Enum/String | `status` | Classification/category type. |

### Context: `Robot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `alternate_energized_effect` | Block | `{ ... }` | Overrides default energized visuals. |

### Context: `RunFar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `PyrophinaVSRun` | The specific ability ID to cast. |
| `move_weights` | Enum/String | `run_far` |  |

### Context: `RunWhenLastPlayerCatIsCharmed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | `true` |  |
| `legacy_savekey` | Enum/String | `Legacy_Marshmallow_StolenCatID` |  |

### Context: `ScalingAttackAnimation`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `10,` | Enum/String | `bite3` |  |
| `default` | Enum/String | `bite1` | Baseline configuration. |
| `thresholds` | Array | `[ [ 5, bite2 ]` |  |

### Context: `SecurityBotProtect`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `SZBShoot, attack, CBShoot_ZodiacStyle` | The specific ability ID to cast. |
| `enemies_only` | Boolean | `true` |  |
| `move` | Enum/String | `None, SBotAngryMove` |  |
| `not_on_kill` | Boolean | `true` |  |
| `tag_restriction` | Enum/String | `dc_cat, dinofamily` |  |

### Context: `SharePickups`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | `true` |  |

### Context: `Sitting`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Chair` |  |
| `attack` | Enum/String | `DoNothing` |  |
| `move` | Enum/String | `DoNothing` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `SkipFirstRounds`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number | `50%` |  |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

### Context: `SlotMachineRollPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `SlotResult_Explode` | Number | `1` | Applies or references the 'SlotResult_Explode' effect/state. |
| `SlotResult_Jackpot_Coins` | Number | `1` | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. |
| `SlotResult_Nothing` | Number | `7` | Applies or references the 'SlotResult_Nothing' effect/state. |
| `SlotResult_RandomPickup` | Number | `11` | Applies or references the 'SlotResult_RandomPickup' effect/state. |

### Context: `Small`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `""` |  |
| `attack` | Enum/String | `GameteInflate` |  |

### Context: `SmallHolding`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Holding"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `SmallHoldingCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"HoldingCat"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `SmallRockBehavior`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chain` | Boolean | `true` |  |
| `damage` | Number | `9, 5` | The base damage properties of an attack. |
| `knockback` | Number | `1, 2, 5` |  |

### Context: `SpawnOnDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `additional_statuses` | Block | `{ ... }` | Generic statuses added to the character. |
| `faction` | Enum/String | `allies, enemies` |  |
| `obj` | Array | `[ Spookie Spookie Scary Coin2 Coin3 Coin4 ], RiftKitten, [ Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCa...` |  |

### Context: `SpawnThingOnDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `auto_cast` | Enum/String | `Dash_Enemy` |  |
| `chance` | Number | `33%, .25, 50%` | Probability (0.0 to 1.0) of executing this action. |
| `coins` | Number | `1` |  |
| `consider_all_layers` | Boolean | `true` |  |
| `good` | Boolean | `false, true` |  |
| `melee_ability_only` | Boolean | `true` |  |
| `object` | Enum/String | `Maggot, TinySpider, Rat` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |

### Context: `SpawningPhase`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `SpearRun`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `CaveManSpearRun` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `CaveManPickupSpear` |  |
| `move_weights` | Enum/String | `util_minmove` |  |

### Context: `SpewerAltGraphics`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FireFull` | Number | `1` | Character Form: Behavior and stats for the 'FireFull' state. |
| `Fire` | Number | `1` | Character Form: Behavior and stats for the 'Fire' state. |
| `NormalFull` | Number | `0` | Character Form: Behavior and stats for the 'NormalFull' state. |
| `Normal` | Number | `0` | Character Form: Behavior and stats for the 'Normal' state. |
| `TarFull` | Number | `2` | Character Form: Behavior and stats for the 'TarFull' state. |
| `Tar` | Number | `2` | Character Form: Behavior and stats for the 'Tar' state. |

### Context: `SquirrelForm`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `BasicMelee` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | Enum/String | `ENEMY_DRAVENSQUIRRELFORM_DESC` |  |

### Context: `StacyMutant_Brace`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `3` | Applies or references the 'Brace' effect/state. |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |

### Context: `StacyMutant_Counter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Modifier: Injects a status effect payload into the character's basic attacks. |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `CounterAttack` | Enum/String | `SM_BleedCounter` | Reaction: Executes a counter-attack ability when hit. |

### Context: `StacyMutant_Damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | `2` | Applies or references the 'AddDamage' effect/state. |
| `AddMaxHealth` | Number | `-25` | Applies or references the 'AddMaxHealth' effect/state. |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |

### Context: `StacyMutant_DoubleHead`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `ExtraDispersedTurns` | Number | `1` | Applies or references the 'ExtraDispersedTurns' effect/state. |

### Context: `StacyMutant_Fire`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `ElementImmune` | Enum/String | `Fire` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | Enum/String | `SM_Lavashot` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `ReplaceBrain` | Block | `{ ... }` | AI Logic: Completely overrides the character's AI profile with a new one. |

### Context: `StacyMutant_Health`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `25` | Applies or references the 'AddMaxHealth' effect/state. |
| `AddSpeed` | Number | `-3` | Applies or references the 'AddSpeed' effect/state. |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `SizeScale` | Number | `1.2` | Applies or references the 'SizeScale' effect/state. |

### Context: `StacyMutant_Holy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `DivineShield` | Number | `7` | Applies or references the 'DivineShield' effect/state. |

### Context: `StacyMutant_Ice`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddMovement` | Number | `-1` | Applies or references the 'AddMovement' effect/state. |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `ElementImmune` | Enum/String | `Ice` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | Enum/String | `SM_IceBreath` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `ReplaceBrain` | Block | `{ ... }` | AI Logic: Completely overrides the character's AI profile with a new one. |

### Context: `StacyMutant_Lightning`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `ElementImmune` | Enum/String | `Electric` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | Enum/String | `SM_LightningDash` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `ReplaceBrain` | Block | `{ ... }` | AI Logic: Completely overrides the character's AI profile with a new one. |

### Context: `StacyMutant_Mirror`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `ReflectProjectiles` | Number | `100%` | Passive: Reflects incoming projectiles back at the attacker. |
| `StatusEachTurnEndForEachTurn` | Block | `{ ... }` | Event Trigger: Applies a scaling status at the end of every turn based on turn count. |

### Context: `StacyMutant_Speed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | `-1` | Applies or references the 'AddDamage' effect/state. |
| `AddSpeed` | Number | `6` | Applies or references the 'AddSpeed' effect/state. |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `SizeScale` | Enum/String | `.8` | Applies or references the 'SizeScale' effect/state. |

### Context: `StacyMutant_Thorns`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `Thorns` | Number | `3` | Applies or references the 'Thorns' effect/state. |

### Context: `Standing`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `BungaSmash` |  |
| `move` | Enum/String | `DefaultMove` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Standing2`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `BungaSmash` |  |
| `move` | Enum/String | `BungaJumpMove` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `Start_Ceiling`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `StatusAfterXTurns`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `CancerExplode` | Logic: Forces the execution of a specific ability. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

### Context: `StatusCollector`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `2` | Applies or references the 'Poison' effect/state. |
| `Slow` | Number | `2` | Applies or references the 'Slow' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

### Context: `StatusEachTurnBeginIfHasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `HealthGain` | Number | `8` | Applies or references the 'HealthGain' effect/state. |
| `animation` | Enum/String | `pulse3` |  |
| `consume` | Boolean | `true` |  |
| `status` | Enum/String | `Counterspell` | ID of the status effect to apply or check. |

### Context: `StatusEachTurnEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Conditional_BadRoll` | Block | `{ ... }` | Conditional: Executes logic on a bad RNG roll. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `HealthGain` | Number | `4` | Applies or references the 'HealthGain' effect/state. |
| `SpeedUp` | Number | `2` | Applies or references the 'SpeedUp' effect/state. |

### Context: `StatusEachTurnEndForEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `T2UnClone` | Logic: Forces the execution of a specific ability. |

### Context: `StatusGroup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | Enum/String | `parasites, mutant_pool` | Generates an item drop from the specified loot pool. |

### Context: `StatusOnDie`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveAmbientLightEffects` | Number | `4` | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `RemoveGlobalModifiers` | Array | `[ BloodRain ]` | Applies or references the 'RemoveGlobalModifiers' effect/state. |

### Context: `StatusOnEndMove`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveStatusStacks` | Block | `{ ... }` | Logic: Removes stacks of a specific status effect. |
| `SpeedUp_WithoutInitiative` | Number | `1` | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. |

### Context: `StatusOnEnemyConfused`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ImmediateUseAbility` | Enum/String | `FuzzerReact` | Applies or references the 'ImmediateUseAbility' effect/state. |

### Context: `StatusOnGainCoins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BackflipWhenTargeted` | Block | `{ ... }` | Reaction: Character executes a backflip dodge when targeted by an attack. |

### Context: `StatusOnKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |
| `UseAbility_NonStack` | Enum/String | `BBTransformZealot, GenericRage` | Applies or references the 'UseAbility_NonStack' effect/state. |

### Context: `StatusOnSpawnIn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `SetHealth` | Number | `50%` | Applies or references the 'SetHealth' effect/state. |

### Context: `StatusOnTookDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ConstitutionUp` | Number | `-1` | Applies or references the 'ConstitutionUp' effect/state. |
| `RemoveStatusStacks` | Block | `{ ... }` | Logic: Removes stacks of a specific status effect. |
| `StrengthUp` | Number | `-1` | Applies or references the 'StrengthUp' effect/state. |

### Context: `StatusOnTookDamageFromAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |

### Context: `StatusOverlappingCharactersAndDie`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |

### Context: `StatusWhenStatusCompletelyRemoved`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility` | Block | `{ ... }` | Logic: Forces execution of an ability. |
| `status` | Enum/String | `BackflipWhenTargeted` | ID of the status effect to apply or check. |

### Context: `Stop`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `StunImmunity`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | `false` |  |

### Context: `SuckMF`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `TormentorSuck` | The specific ability ID to cast. |
| `decision_weights` | Enum/String | `careless` |  |
| `move_weights` | Enum/String | `keep_distance` |  |

### Context: `SupportDieInsteadOfRun`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `alt_dead_ani` | Enum/String | `off` |  |
| `alt_dying_ani` | Enum/String | `shutdown` |  |

### Context: `SupportFormChangeInsteadOfRun`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `SBotAnger, TVChangeDie` | The specific ability ID to cast. |
| `wait_till_turn` | Boolean | `true` |  |

### Context: `SwimmingFormChange`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `form_in` | Enum/String | `Water` |  |
| `form_out` | Enum/String | `Out` |  |

### Context: `SwitchMusic`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `new_layer` | Enum/String | `event` | The specific audio layer to transition to (e.g., map, battle). |
| `new_song` | Enum/String | `same` | The ID of the new music track. |

### Context: `SwordAndShield`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `DestroyerAttack` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `SwordAndShield_Primed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Holy"` |  |
| `attack` | Enum/String | `DestroyerAttack` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `SyncFormsWithBuddy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `no_buddy` | Enum/String | `Rage` |  |

### Context: `T3HitlerSpawningPhase`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `T3JoinFight` | Flag | `N/A` | Applies or references the 'T3JoinFight' effect/state. |
| `T3Spawn_Colorless` | Flag | `N/A` | Applies or references the 'T3Spawn_Colorless' effect/state. |
| `spell_use_groups` | Array | `[ [ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T...` |  |

### Context: `TF_TargetAllies`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `TwistingFlames` | The specific ability ID to cast. |
| `decision_weights` | Enum/String | `util_target_allies` |  |

### Context: `TF_TargetEnemies`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `TwistingFlames` | The specific ability ID to cast. |
| `decision_weights` | Enum/String | `util_target_enemies` |  |

### Context: `TVBotScreen`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Die` | Number | `6` | Character Form / Logic: Forces the character to die. |
| `Dumb` | Number | `3` | AI Profile: A simplified, less optimal decision-making profile. |
| `Fuck` | Number | `5` | Applies or references the 'Fuck' effect/state. |
| `Obey` | Number | `1` | AI State: Enforced compliance logic (e.g., when Charmed). |
| `Shit` | Number | `4` | Applies or references the 'Shit' effect/state. |
| `Stop` | Number | `2` | AI Movement: Forces the character to cease movement. |

### Context: `Tar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `SpewerLobbed_Tar` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `TarFull`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Full` |  |
| `attack` | Enum/String | `SpewerSpit` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `TempPassiveUntilSettled`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `MeleeRevengeDamage` | Block | `{ ... }` | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. |

### Context: `Terminator2Run`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | Enum/String | `T2GoopRun` |  |
| `move_weights` | Enum/String | `stay_far_always_move` |  |

### Context: `TerminatorChase`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `T1ChokeReaction` | The specific ability ID to cast. |
| `move` | Enum/String | `MoveOne` |  |

### Context: `TerminatorSkin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `groups` | Array | `[ { stacks 48 ParticleBurst Gibs_terminatorskin CatPartsT...` |  |
| `status` | Enum/String | `Brace` | ID of the status effect to apply or check. |

### Context: `Throb`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |

### Context: `ThrobBubs`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `ThrobHost`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | Enum/String | `Host` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `ThrobNettle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `TinkererBasicAttackSwitching`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `craft_ability` | Enum/String | `TinkererCraft` |  |
| `throw_ability` | Enum/String | `TinkererThrow` |  |

### Context: `TransformInXTurns`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `hatch` |  |
| `initiative` | Enum/String | `keep_turns_end_turn` |  |
| `object` | Array | `[ Squirrel Crow Snake Turtle Toad Catepillar ], SkeletonCatRevived, TallSkeletonCatRevived` |  |
| `stacks` | Number | `1, 2, 3` | Number of stacks or intensity to apply. |
| `turns` | Array | `[ 1 4 ]` | Turn counter tracking. |

### Context: `TransformOnDeathImmediately`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `first_turn` | Enum/String | `keep_turns` |  |
| `obj` | Enum/String | `SkeletonShamblerCorpse, TallSkeletonCatCorpse, SkeletonCatCorpse` |  |

### Context: `TransformOnElementInfluence`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Fire, Holy` | Specific element type required or applied. |
| `object` | Enum/String | `CookedFood, CookedBigFood, CookedBiggestFood` |  |

### Context: `TransformOnElementInfluencex`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Holy` | Specific element type required or applied. |
| `object` | Enum/String | `Bait, PurifiedPoisonFood` |  |

### Context: `TransformOnStatusThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `Moth` |  |
| `status` | Enum/String | `AllStatsUp` | ID of the status effect to apply or check. |
| `threshold` | Number | `5` |  |

### Context: `Transformed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Trapper`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `HellHandGrab, BloatSideLaser, YA_Laser` | The specific ability ID to cast. |
| `cancel_movement` | Boolean | `false` |  |
| `pathfinding_avoidance` | Number | `250` |  |
| `range` | Number | `10` | Distance or area of effect in tiles. |

### Context: `Turtled`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | Enum/String | `Turtle` |  |
| `attack` | Enum/String | `None` |  |
| `move` | Enum/String | `None` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `TwisterFling`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `5` | The base damage properties of an attack. |
| `max_dist` | Number | `5` |  |
| `min_dist` | Number | `3` |  |

### Context: `TwoAlive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `turns` | Block | `{ ... }` | Turn counter tracking. |

### Context: `TwoEyes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Unflip`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `TeleportFlipUp` | The specific ability ID to cast. |
| `move_for_ability` | Enum/String | `Spin_Enemy` |  |
| `move_weights` | Enum/String | `stay_close_always_move` |  |

### Context: `UnlimitedDeathRattleRevive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MD_Lift` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |

### Context: `Unlit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum/String | `Unlit` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Unwashed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `partial_animation_suffix` | Enum/String | `Unwashed` |  |

### Context: `Up`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Up"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"OBJECT_TIREUP_DESC"` |  |

### Context: `UseAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `Destroyer2HolyAttack` | The ID of the ability to trigger. |
| `respect_prime` | Boolean | `true` | If true, respects the ability's prime/cooldown state. |

### Context: `UseAbilityWhenOutOfStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `QueenHippoHeartAttack` | The specific ability ID to cast. |
| `status` | Enum/String | `Brace` | ID of the status effect to apply or check. |

### Context: `Washed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `Washer`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `attack` | Enum/String | `BasicMelee` |  |
| `name` | String | `"ENEMY_CULTISTWASHER_NAME"` | Localization key for the character's name. |
| `partial_animation_suffix` | String | `"Cultist"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CULTISTWASHER_DESC"` |  |

### Context: `Water`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Water"` |  |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `WereMan`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"WereMan"` |  |
| `attack` | Enum/String | `WereManFurySwipes` |  |
| `name` | String | `"ENEMY_WEREMAN_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_WEREMAN_DESC"` |  |

### Context: `Zealot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"Zealot"` |  |
| `attack` | Enum/String | `BBStabby` |  |
| `name` | String | `"ENEMY_CULTISTZEALOT_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_CULTISTZEALOT_DESC"` |  |

### Context: `ZealotBomb`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ai` | Block | `{ ... }` | Core block defining the AI behavior logic and weights. |
| `animation_suffix` | String | `"BombZealot"` |  |
| `attack` | Enum/String | `BBExplode` |  |
| `name` | String | `"ENEMY_BOMBZEALOT_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |
| `tooltip` | String | `"ENEMY_BOMBZEALOT_DESC"` |  |

### Context: `abilities`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | Enum/String | `None, BasicMelee, DustMelee` |  |
| `can_get_bonus` | Boolean | `true` |  |
| `move` | Enum/String | `None, DefaultMove, DustMove` |  |
| `spells` | Array | `[ SpawnBomb BombRatTurtle RockToss_BomberRat ], [ BirdFly ], [ TrampleDash MoveOne ]` |  |

### Context: `active`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `additional_statuses`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |

### Context: `ai`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animate_choice` | Boolean | `false, true` |  |
| `attack` | Enum/String | `JohnnyBlast` |  |
| `auto_orient` | Boolean | `false` |  |
| `bonusturn_pattern` | Block | `{ ... }` | AI Logic: Determines ability usage during bonus turns. |
| `brain` | Enum/String | `PatternBrain, GenericBrain, PlayerBrain` |  |
| `clamp_pattern` | Boolean | `true` |  |
| `consider_spells` | Boolean | `false` |  |
| `decision_weights` | Enum/String | `simple, default, extra_careless` |  |
| `dice_abilities` | Array | `[ D6Fizzle D6Confused D6Poop D6Laser D6Quake D6Storm D6Wr...` |  |
| `dispersed_bonusturn_pattern` | Block | `{ ... }` | AI Logic: Alternative bonus turn ability pattern. |
| `end_turn_on_formswitch` | Boolean | `false, true` |  |
| `fallback_advances_pattern` | Boolean | `false, true` |  |
| `fallback` | Block | `{ ... }` | Logic executed if primary options fail. |
| `mainturn_pattern` | Block | `{ ... }` | AI Logic: Determines standard ability usage during the main turn. |
| `move_weights` | Enum/String | `keep_distance_always_move, chaotic_runaway, bird` |  |
| `never_hit_ally_corpses` | Boolean | `true` |  |
| `pattern` | Block | `{ ... }` | AI sequence logic. |
| `post_absorb_move_weights` | Enum/String | `minimum_move` |  |
| `random_orient` | Boolean | `true` |  |
| `randomize_pattern_start` | Boolean | `true` |  |
| `reset_pattern_on_formswitch` | Boolean | `false, true` |  |
| `reset_pattern_on_round_begin` | Boolean | `true` |  |
| `roll_ability` | Enum/String | `RollDice` |  |
| `round_end_bonusturn_pattern` | Block | `{ ... }` | AI Logic: Ability usage pattern during round-end bonus turns. |
| `round_start_bonusturn_pattern` | Block | `{ ... }` | AI Logic: Ability usage pattern during round-start bonus turns. |
| `stun_advances_pattern` | Boolean | `false, true` |  |
| `virtual_abilities` | Block | `{ ... }` | Abilities that are evaluated but not directly castable by the player. |

### Context: `ai_if_spawned_as_enemy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | Enum/String | `PatternBrain` |  |
| `decision_weights` | Enum/String | `default` |  |
| `move_weights` | Enum/String | `keep_distance` |  |
| `pattern` | Block | `{ ... }` | AI sequence logic. |

### Context: `ally_rewards`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional: Executes logic on a good RNG roll. |
| `FindItemFromPool` | Enum/String | `dove_pool, chapter, blackbird_pool` | Generates an item drop from the specified loot pool. |
| `RandomStatusFromPool` | Block | `{ ... }` | Logic: Applies a random status from the pool. |

### Context: `alt_spawn_pool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Antidote` | Number | `1, .5` | Applies or references the 'Antidote' effect/state. |
| `Bear` | Number | `1` | Applies or references the 'Bear' effect/state. |
| `BigCatnip` | Number | `6, 1, 10` | Applies or references the 'BigCatnip' effect/state. |
| `BigFood` | Number | `5, 20` | Applies or references the 'BigFood' effect/state. |
| `BigScrap` | Number | `6, 1, 4.5` | Applies or references the 'BigScrap' effect/state. |
| `BiggestFood` | Number | `6, 1, 15` | Applies or references the 'BiggestFood' effect/state. |
| `BlackBird` | Number | `3000` | Applies or references the 'BlackBird' effect/state. |
| `Blessing` | Number | `1, .5` | Applies or references the 'Blessing' effect/state. |
| `Catepillar` | Number | `10` | Applies or references the 'Catepillar' effect/state. |
| `Catnip` | Number | `20` | Applies or references the 'Catnip' effect/state. |
| `CharmedDip` | Number | `1` | Applies or references the 'CharmedDip' effect/state. |
| `CharmedFloater` | Number | `1` | Applies or references the 'CharmedFloater' effect/state. |
| `CharmedPile` | Number | `1` | Applies or references the 'CharmedPile' effect/state. |
| `Cherub` | Number | `1` | Applies or references the 'Cherub' effect/state. |
| `Chicken` | Number | `3000` | Applies or references the 'Chicken' effect/state. |
| `Coin10` | Number | `1, .1` | Applies or references the 'Coin10' effect/state. |
| `Coin2` | Number | `1` | Applies or references the 'Coin2' effect/state. |
| `Coin3` | Number | `1` | Applies or references the 'Coin3' effect/state. |
| `Coin4` | Number | `1` | Applies or references the 'Coin4' effect/state. |
| `Coin` | Number | `1, 70` | Applies or references the 'Coin' effect/state. |
| `Dove` | Number | `1000` | Applies or references the 'Dove' effect/state. |
| `Eagle` | Number | `300` | Applies or references the 'Eagle' effect/state. |
| `Food` | Number | `20` | Applies or references the 'Food' effect/state. |
| `Harpy` | Number | `1` | Applies or references the 'Harpy' effect/state. |
| `HummingBird` | Number | `300` | Applies or references the 'HummingBird' effect/state. |
| `LargeBirdPool` | Number | `1` | Applies or references the 'LargeBirdPool' effect/state. |
| `MedBirdPool` | Number | `1` | Applies or references the 'MedBirdPool' effect/state. |
| `MedCatnip` | Number | `5, 20` | Applies or references the 'MedCatnip' effect/state. |
| `MedScrap` | Number | `5, 20` | Applies or references the 'MedScrap' effect/state. |
| `Mutant` | Number | `1` | Character Form: Behavior and stats for the 'Mutant' state. |
| `Pigeon` | Number | `3000` | Applies or references the 'Pigeon' effect/state. |
| `RandomArmorPickup` | Number | `40, 4.5` | Applies or references the 'RandomArmorPickup' effect/state. |
| `RandomBiggerArmorPickup` | Number | `4.5` | Applies or references the 'RandomBiggerArmorPickup' effect/state. |
| `RandomBiggerCatnipPickup` | Number | `10` | Applies or references the 'RandomBiggerCatnipPickup' effect/state. |
| `RandomBiggerFoodPickup` | Number | `15` | Applies or references the 'RandomBiggerFoodPickup' effect/state. |
| `RandomCatnipPickup` | Number | `10, 30` | Applies or references the 'RandomCatnipPickup' effect/state. |
| `RandomFoodPickup` | Number | `40, 15` | Applies or references the 'RandomFoodPickup' effect/state. |
| `Raven` | Number | `300` | Applies or references the 'Raven' effect/state. |
| `Scrap` | Number | `20` | Applies or references the 'Scrap' effect/state. |
| `Seagull` | Number | `1000` | Applies or references the 'Seagull' effect/state. |
| `SmallBirdPool` | Number | `1` | Applies or references the 'SmallBirdPool' effect/state. |
| `Snake` | Number | `10` | Applies or references the 'Snake' effect/state. |
| `Squirrel` | Number | `10` | Applies or references the 'Squirrel' effect/state. |
| `Toad` | Number | `10` | Applies or references the 'Toad' effect/state. |
| `Turkey` | Number | `1000` | Applies or references the 'Turkey' effect/state. |
| `Turtle` | Number | `10` | Applies or references the 'Turtle' effect/state. |

### Context: `alternate_energized_effect`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FormChange` | Enum/String | `GuaranteedJackpot` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |

### Context: `bonusturn_pattern`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_all` | Array | `[ TrembloSuck *TrembloEat TrembloEat ], [ CloseConvert, attack ], [ attack AlienBeastOpenEyes ]` |  |
| `do_priority` | Array | `[ TormentorBite TormentorSpawn attack ], [ TormentorSpawn TormentorBite attack ], [ G3GrabHead move *G3GrabHead ]` |  |
| `do_strict` | Array | `[ ], [ WizFlamethrower ], [ WizStorm ]` |  |
| `do` | Enum/String | `*SpawnBomb, move, DustDash` |  |
| `move_then_do` | Enum/String | `RatKingSpawn` |  |

### Context: `damage_instance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | Block | `{ ... }` | Non-damaging impact triggers. |

### Context: `default`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `dispersed_bonusturn_pattern`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do` | Enum/String | `attack, Simon_Trash, Simon_Tentacle` |  |

### Context: `eat_damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging impact triggers. |
| `makes_contact` | Boolean | `true` |  |
| `piercing` | Boolean | `true` |  |
| `type` | Enum/String | `melee` | Classification/category type. |

### Context: `effects`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BlackHoleSuck` | Number | `1` | Applies or references the 'BlackHoleSuck' effect/state. |
| `Burn` | Number | `2, 5` | Applies or references the 'Burn' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `ConstitutionUp` | Number | `-1` | Applies or references the 'ConstitutionUp' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `Vaporize` | Number | `20` | Applies or references the 'Vaporize' effect/state. |

### Context: `equipment`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `face` | Enum/String | `WesternHat, MetalPlate, AtomicMark` |  |
| `head` | Enum/String | `CoinBag, Banana, LoansharksFedora` |  |
| `neck` | Enum/String | `Slime, MageCollar, Poncho` |  |
| `weapon` | Enum/String | `ButcherHook, AstroTaser, GunslingerPistol` | Weapon item constraint. |

### Context: `exit_animations`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Default` | Enum/String | `release` | Character Form: The baseline default behavior state. |

### Context: `fallback`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_all` | Array | `[ move, *CoreFreakFury ]` |  |
| `do_best` | Array | `[ Magnetize, attack, GuillotinaTossCollide, YeetTowardsBu...` |  |
| `do_nothing` | Array | `[ ]` |  |
| `do_priority` | Array | `[ *attack RunFar ], [ attack TrembloEat ], [ attack, Magnetize, YeetTowardsBuddy ]` |  |
| `do_random` | Array | `[ CHSpawn CHCry ]` |  |
| `do` | Enum/String | `attack, RockToss_ColorlessCat_AsCloseAsPossible, JohnnyBlast` |  |
| `move_then_do` | Enum/String | `CerberubsCalm` |  |

### Context: `graphics`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `alt_animations` | Array | `[ [ idle girlyIdle ], [ [ idle cuteIdle ], [ [ idle twitchyIdle ]` |  |
| `always_huge_mask` | Boolean | `true` |  |
| `art_flip` | Number | `-1` |  |
| `custom_cat_data` | Enum/String | `Kitten, TomTom, Mangy` |  |
| `dead` | Enum/String | `empty, skeletonDead` |  |
| `deadhit` | Enum/String | `skeletonCorpseHit` |  |
| `default_attack_animation` | Enum/String | `bite1, attack2` |  |
| `depth_offset` | Number | `5, -.1, .01` |  |
| `desc` | String | `"OBJECT_DECOY_DESC", ENEMY_FATWOMAN_DESC` | Localization key for the character's desc. |
| `dodge` | Enum/String | `liquidmetaldodge` |  |
| `dont_sink` | Boolean | `true` |  |
| `dying` | Enum/String | `dyingDisassembled, dead` |  |
| `four_way_animations` | Boolean | `true` |  |
| `hit` | Enum/String | `hitDisassembled, skeletonCorpseHit` |  |
| `move_speed_multiplier` | Number | `1.75, .66, .5` |  |
| `move_speed_sync_frames` | Number | `22.5, 7, 40` |  |
| `movieclip` | Enum/String | `BirdMed, BirdSmall, BirdLarge` |  |
| `name` | String | `"ENEMY_LITTLEBIRD_NAME", "ENEMY_MEDBIRD_NAME", "ENEMY_BIRD_NAME"` | Localization key for the character's name. |
| `no_horizontal_flip` | Boolean | `true` |  |
| `no_splatter` | Boolean | `true` |  |
| `non_blocking_animations` | Array | `[ "hit" , "critical" ]` |  |
| `override_portrait` | Enum/String | `Cherub` |  |
| `piece_alt_frame` | Number | `5, 7, 3` |  |
| `projectile_spawn_offset` | Array | `[ 0 1 ], [ .25 1 ], [ 0 1.5 ]` |  |
| `randomize_starting_frame` | Boolean | `false` |  |
| `scale` | Enum/String | `.9, .8, .5` |  |
| `shade_occluded_objects` | Boolean | `true` |  |
| `shadow_size` | Number | `2, 3, .5` |  |
| `shadow` | Enum/String | `MedSlimeShadow, none, TormentorShadow` |  |
| `show_infinity_damage_warning` | Boolean | `true` |  |
| `spawnin_animation` | String | `"digUp", digUp, "howl"` |  |
| `status_display_count_max` | Number | `5` |  |
| `stunned` | Enum/String | `idleDisassembled, dead` |  |
| `tint` | Array | `[ .7 1 .7 1 ], green, [ 0 0 0 1 ]` |  |
| `tooltip` | String | `"ENEMY_BIRD_DESC", "ENEMY_RADICALRAT_DESC", "ENEMY_CHERUB_FINALBOSS_DESC"` |  |
| `uifloaters_offset` | Number | `1.5, 2, 2.5` |  |
| `walk` | Enum/String | `stompwalk, raptorWalk, zombieWalk` |  |
| `water_mask` | Enum/String | `medmed, medium, square` |  |
| `weak` | Enum/String | `idleDisassembled, dead` |  |

### Context: `hot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Hot"` |  |
| `name` | String | `"OBJECT_HOTPETROCK_NAME", "OBJECT_HOTROCK_NAME", "OBJECT_HOTBOULDER_NAME"` | Localization key for the character's name. |
| `passives` | Block | `{ ... }` | Block listing intrinsic passive modifiers. |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `TVBotDie` | Number | `1` | Applies or references the 'TVBotDie' effect/state. |
| `TVBotDumb` | Number | `1` | Applies or references the 'TVBotDumb' effect/state. |
| `TVBotObey` | Number | `1` | Applies or references the 'TVBotObey' effect/state. |
| `TVBotStop` | Number | `1` | Applies or references the 'TVBotStop' effect/state. |

### Context: `mainturn_pattern`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_all` | Array | `[ attack DustTeleport ], [ *AlienBeastScream *AlienBeastEat *AlienBeastPuke *Alien..., [ *MarshmallowZealot, CloseConvert, attack ]` |  |
| `do_priority` | Array | `[ *HitlerHeil attack move ], [ ChumShot_Damage, ChumShot_Maggot ], [ attack Simon_Shot ]` |  |
| `do_strict` | Array | `[ BasicMelee, RageUp ], [ *WizSpellShield, WizBlizzard ]` |  |
| `do` | Enum/String | `HealSelf, **TrampleDash, **BombRatTurtle` |  |
| `move_then_do` | Enum/String | `attack, RockSong` |  |

### Context: `other_form_change_abilities`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Boris` | Enum/String | `MegaGuppy_TransformBoris` | Character Form / AI State: Behavior and stats for the 'Boris' state. |
| `Explosive` | Enum/String | `MegaGuppy_TransformExplosive` | Character Form: Behavior and stats for the 'Explosive' state. |
| `Holy` | Enum/String | `MegaGuppy_TransformHoly` | Character Form: Behavior and stats for the 'Holy' state. |

### Context: `passive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | Enum/String | `DoNothing` |  |

### Context: `passives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AbilityAfterEnemyCastSpell_Stackable` | Enum/String | `ThornUp, ThornUpX` | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. |
| `AbilityHealthThreshold` | Block | `{ ... }` | AI Trigger: Executes an ability when health drops below a specific threshold. |
| `AbilityOnBattleStart_UseAI` | Enum/String | `TheCreator_SpawnCloneTeam` | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. |
| `AbilityOnRoundEnd` | Block | `{ ... }` | AI Trigger: Executes an ability at the end of the combat round. |
| `AbilityReaction` | Enum/String | `attack, TC_DashReaction, { ... }` | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). |
| `AbilityWhenBuddyDies` | Enum/String | `GirlDinoCry, ChubsRage, Guillotina2Rage` | Applies or references the 'AbilityWhenBuddyDies' effect/state. |
| `AbilityWhenTaggedCharacterMovesNear` | Block | `{ ... }` | AI Trigger: Executes an ability when a character with a specific tag moves adjacent. |
| `AddCorpseHealth` | Number | `-999` | Applies or references the 'AddCorpseHealth' effect/state. |
| `AddDamage` | Number | `1, 2, 4` | Applies or references the 'AddDamage' effect/state. |
| `AddElementsToBasicAttack` | Enum/String | `Fire` | Applies or references the 'AddElementsToBasicAttack' effect/state. |
| `AddHiddenTag` | Enum/String | `grown_hitler_clone, hitler_clone_fetus, unlit_candle` | Applies or references the 'AddHiddenTag' effect/state. |
| `AddInitiative` | Number | `-9999, -10, 999999` | Applies or references the 'AddInitiative' effect/state. |
| `AddMaxHealth` | Number | `5` | Applies or references the 'AddMaxHealth' effect/state. |
| `AddMeleeKnockback` | Number | `1, 2, 10` | Applies or references the 'AddMeleeKnockback' effect/state. |
| `AddMovement` | Number | `1, 2, -2` | Applies or references the 'AddMovement' effect/state. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Modifier: Injects a status effect payload into the character's basic attacks. |
| `AddStatusToReceivedDamage` | Block | `{ ... }` | Modifier: Applies a status effect whenever the character takes damage. |
| `AddStatusToSpells` | Block | `{ ... }` | Modifier: Injects a status effect payload into all spells cast by the character. |
| `AddStatusToWeapons` | Block | `{ ... }` | Modifier: Injects a status effect into attacks made with weapons. |
| `AddTag` | Enum/String | `fetus, cat, tumor` | Applies or references the 'AddTag' effect/state. |
| `AddTemporaryEffectsToBasicAttack` | Block | `{ ... }` | Modifier: Adds temporary statuses to the character's basic attacks. |
| `AdvancedTint` | Array | `[ .6, .6, .6, 1 .5, .5, .5, 0 ]` | Applies or references the 'AdvancedTint' effect/state. |
| `AdventureTokenPassivePool` | Block | `{ ... }` | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. |
| `AggroTargetIsBuddy` | Number | `1` | Applies or references the 'AggroTargetIsBuddy' effect/state. |
| `AggroTargetIsCurrentTurn` | Number | `1` | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. |
| `AggroTargetIsGovernedByHitEffect` | Block | `{ ... }` | AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity. |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | `1` | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | `1` | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. |
| `AggroTargetIsLowestMaxHealthCat` | Number | `1` | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. |
| `AlienBeastDangerZones` | Array | `[ AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeas...` | Applies or references the 'AlienBeastDangerZones' effect/state. |
| `AlienBeastEyeStalks` | Number | `3` | Applies or references the 'AlienBeastEyeStalks' effect/state. |
| `AllDamageImmune_IncludingSpeculative` | Number | `1` | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. |
| `AllSpellsCostActPoints` | Number | `1` | Applies or references the 'AllSpellsCostActPoints' effect/state. |
| `AllStatsAura` | Block | `{ ... }` | Passive: Projects an aura that modifies all primary stats of nearby characters. |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `AlphaTurns` | Number | `1` | Applies or references the 'AlphaTurns' effect/state. |
| `AlwaysHitDifferentTargets` | Number | `1` | Applies or references the 'AlwaysHitDifferentTargets' effect/state. |
| `Ammo` | Number | `6, 1, 3` | Applies or references the 'Ammo' effect/state. |
| `Angel` | Number | `1` | Applies or references the 'Angel' effect/state. |
| `ArmorPickup` | Block | `{ ... }` | Pickup Logic: Defines what happens when an armor item is collected. |
| `AutocastEachRound` | Block | `{ ... }, SpiderReturn` | AI Trigger: Forces the character to cast a specific ability at the start of each round. |
| `AvoidDamagingCharmedEnemies` | Number | `1` | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. |
| `AwardCoinsOnDeath` | Number | `10` | Applies or references the 'AwardCoinsOnDeath' effect/state. |
| `BackstabAllDirections` | Number | `1` | Applies or references the 'BackstabAllDirections' effect/state. |
| `BackstabImmunity` | Number | `1` | Applies or references the 'BackstabImmunity' effect/state. |
| `BaitAura` | Block | `{ ... }` | Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots). |
| `BaseStatMultiply` | Enum/String | `.666, .25, .5` | Applies or references the 'BaseStatMultiply' effect/state. |
| `BasicAIDangerZone` | Number | `2` | Applies or references the 'BasicAIDangerZone' effect/state. |
| `BattlefieldUniqueRandomPassive` | Block | `{ ... }` | Map Rule: Grants a unique random passive modifier to the battlefield. |
| `BirdRewards` | Block | `{ ... }` | Loot logic: Rewards dropped by bird-type enemies. |
| `Bird` | Enum/String | `CookedChickenLeg` | Applies or references the 'Bird' effect/state. |
| `BlackHolePassive` | Number | `1` | Applies or references the 'BlackHolePassive' effect/state. |
| `BloatEyePassive2` | Enum/String | `BloatEyeMovement2` | Applies or references the 'BloatEyePassive2' effect/state. |
| `BlockAllDamage` | Number | `1` | Applies or references the 'BlockAllDamage' effect/state. |
| `BombBehavior` | Number | `1` | Applies or references the 'BombBehavior' effect/state. |
| `BonusTurnPattern` | Array | `[ { evenly_dispersed_bonus_turns 1 round_end_bonus_turns ..., [ { dispersed_bonus_turns 2 round_end_bonus_turns 1 } { r..., [ { evenly_dispersed_bonus_turns 0 round_end_bonus_turns ...` | Applies or references the 'BonusTurnPattern' effect/state. |
| `BossRewards` | Block | `{ ... }` | Loot logic: Rewards dropped upon defeating a boss. |
| `Brace` | Number | `1, 4, 10` | Applies or references the 'Brace' effect/state. |
| `Buddy` | Enum/String | `Nubs, Smough, Ornstein` | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. |
| `BuffImmunity` | Number | `1` | Applies or references the 'BuffImmunity' effect/state. |
| `BungaCheers` | Block | `{ ... }` | Animation/AI State: Bunga cheering animation logic. |
| `BungaEntrance` | Block | `{ ... }` | Animation/AI State: Bunga entering the arena. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `CCImmunity` | Number | `1` | Applies or references the 'CCImmunity' effect/state. |
| `CanMutateTo` | Enum/String | `Hyde, [ TumorousMaggot, ChargeyMaggot, SwappyMaggot ], [ Lumpy, Leaper ]` | Applies or references the 'CanMutateTo' effect/state. |
| `CanShield` | Number | `1` | Applies or references the 'CanShield' effect/state. |
| `CapReceivedDamage` | Number | `1` | Applies or references the 'CapReceivedDamage' effect/state. |
| `CatPartsTransform` | Block | `{ ... }` | Visual: Transforms specific body parts of the character. |
| `CaveFamilyEnrage` | Block | `{ ... }` | AI Trigger: Enrage logic triggered when a cave family member is killed. |
| `CerberubsAggroTargetBehavior` | Block | `{ ... }` | AI Logic: Custom aggro targeting rules for Cerberubs. |
| `ChanceToBackflip` | Block | `{ ... }` | Reaction: Probability to execute a backflip dodge. |
| `ChanceToDisableActionsIfNotCharmed` | Number | `75%` | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. |
| `ChanceToFormChangeOnAbilityDamage` | Block | `{ ... }` | Reaction: Probability to change forms when taking ability damage. |
| `ChanceToSpitOnDamage` | Block | `{ ... }` | Reaction: Probability to use a spit counter-attack when damaged. |
| `ChangeTileOnDeath` | Enum/String | `WaterTile` | Applies or references the 'ChangeTileOnDeath' effect/state. |
| `ChangeTileOnPop` | Enum/String | `GlitchTile, OilTile, CreepTile` | Applies or references the 'ChangeTileOnPop' effect/state. |
| `ChaosBossFormChangeGuide` | Block | `{ ... }` | Boss Logic: Maps the form transition phases for the Chaos Boss. |
| `ChaosBossPieces` | Block | `{ ... }` | Boss Logic: Defines the separate destructible pieces of the Chaos Boss. |
| `ChaosHeadDropIn` | Block | `{ ... }` | Boss Logic: Drop-in attack/animation for the Chaos Head. |
| `CharacterLightSource` | Block | `{ ... }` | Visual: Attaches a dynamic lighting source to the character. |
| `CherubimReaction` | Block | `{ ... }` | Reaction: Custom reaction triggers for Cherubim enemies. |
| `CoinPickup` | Number | `1, 2, 3` | Applies or references the 'CoinPickup' effect/state. |
| `ConjureBonusAbility` | Enum/String | `random` | Adds a temporary bonus ability to the character's hand/deck. |
| `CountAsCorpse` | Number | `1` | Applies or references the 'CountAsCorpse' effect/state. |
| `CounterAttackAfterEnemyCastSpell` | Enum/String | `Telekinesis` | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. |
| `CounterAttack` | Enum/String | `YeticatSnowball_Counter, attack, BungaSwipe` | Reaction: Executes a counter-attack ability when hit. |
| `CreateGlobalModifiers` | Block | `{ ... }` | Encounter Rule: Generates map-wide modifiers. |
| `CrowAttackLink` | Number | `1` | Applies or references the 'CrowAttackLink' effect/state. |
| `DamageFromBehindOnly` | Number | `1` | Applies or references the 'DamageFromBehindOnly' effect/state. |
| `DeathRattleRevive` | Block | `{ ... }, HCHumanDie, ToxPuff` | Event Trigger: Revives the character immediately upon death. |
| `DeathRattle` | Enum/String | `MoonHead_KillHands, BoomerCatExplode, { ... }` | Event Trigger: Executes logic or abilities exactly when the character dies. |
| `DebuffImmunity` | Number | `1` | Applies or references the 'DebuffImmunity' effect/state. |
| `DelayedAutoRevive` | Block | `{ ... }` | Logic: Character revives automatically after a set delay. |
| `DemonicGlyphFrames` | Number | `1` | Applies or references the 'DemonicGlyphFrames' effect/state. |
| `DemonicGlyphStealer` | Number | `1` | Applies or references the 'DemonicGlyphStealer' effect/state. |
| `DiceBehavior` | Block | `{ ... }` | AI Logic: Custom behavior for Dice enemies. |
| `DicerArt` | Array | `[ 59 52 65 50 54 63 64 ]` | Applies or references the 'DicerArt' effect/state. |
| `DieWhenOnlyGolemsLeft` | Number | `1` | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. |
| `DieWhenSpawnerDies` | Number | `1` | Applies or references the 'DieWhenSpawnerDies' effect/state. |
| `DiesToElement` | Enum/String | `Wind, { ... }` | Vulnerability: Character dies instantly if hit by this element. |
| `DiesToPiercingAndSpikes` | Block | `{ ... }` | Vulnerability: Character dies instantly if hit by piercing attacks or spikes. |
| `DigestDeadBodies` | Enum/String | `MoonHead_Digest, LennyCatDies, Digest` | Applies or references the 'DigestDeadBodies' effect/state. |
| `DisableSpells` | Number | `1` | Applies or references the 'DisableSpells' effect/state. |
| `DisguisedTrapper` | Enum/String | `FearMelee` | Applies or references the 'DisguisedTrapper' effect/state. |
| `Disguised` | Number | `1` | Applies or references the 'Disguised' effect/state. |
| `DisplayBuddyCatOnSpawn` | Number | `3` | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. |
| `DisplayDangerAOE` | Enum/String | `MoonHead_Blow, attack, TheChild_Wrath` | Applies or references the 'DisplayDangerAOE' effect/state. |
| `DissuadeInstakills` | Number | `1` | Applies or references the 'DissuadeInstakills' effect/state. |
| `Divide4OnDeath` | Enum/String | `Clot, BiggestFood, MedSlime` | Applies or references the 'Divide4OnDeath' effect/state. |
| `DivineShieldPickup` | Number | `1` | Applies or references the 'DivineShieldPickup' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `DodgeChanceWithBlindSpot` | Number | `25%` | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. |
| `DodgeChance_Status` | Number | `100, 66` | Applies or references the 'DodgeChance_Status' effect/state. |
| `DodgeChance` | Number | `50%` | Applies or references the 'DodgeChance' effect/state. |
| `DodgeWhenTargeted` | Block | `{ ... }` | Reaction: Executes a dodge maneuver when targeted. |
| `DustCloudBehavior` | Number | `1` | Applies or references the 'DustCloudBehavior' effect/state. |
| `Dybbuk1HPTracker` | Number | `1` | Applies or references the 'Dybbuk1HPTracker' effect/state. |
| `DybbukPossessionFallback` | Block | `{ ... }` | Logic: Fallback state when a Dybbuk possession fails. |
| `ElectricArcs` | Number | `1` | Applies or references the 'ElectricArcs' effect/state. |
| `ElementImmune` | Enum/String | `Ice, Fire, Creep` | Applies or references the 'ElementImmune' effect/state. |
| `ElementWeakness` | Enum/String | `Fire` | Applies or references the 'ElementWeakness' effect/state. |
| `EnrageOnDamage` | Number | `1` | Applies or references the 'EnrageOnDamage' effect/state. |
| `EraseSpawnCoins` | Number | `1` | Applies or references the 'EraseSpawnCoins' effect/state. |
| `EventBounterHunterPassive` | Number | `1` | Applies or references the 'EventBounterHunterPassive' effect/state. |
| `ExpireOnSpawnerTurnEnd` | Number | `1` | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. |
| `ExtraDispersedTurns` | Number | `1` | Applies or references the 'ExtraDispersedTurns' effect/state. |
| `ExtraMovePoints` | Number | `1` | Applies or references the 'ExtraMovePoints' effect/state. |
| `ExtraTurnsPerTaggedUnit` | Enum/String | `sprout` | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. |
| `FaceAwayLastDamage` | Block | `{ ... }` | Reaction: Forces the character to face away from the last damage source. |
| `FaceLastDamage` | Number | `1, { ... }` | Reaction: Forces the character to face towards the last damage source. |
| `FaceShield` | Number | `0` | Applies or references the 'FaceShield' effect/state. |
| `FadeInsteadOfDie` | Number | `1` | Applies or references the 'FadeInsteadOfDie' effect/state. |
| `FinalBossBeamQueue` | Block | `{ ... }` | Boss Logic: Attack queue for the final boss beam. |
| `FinalBossBecomeTheChild` | Block | `{ ... }` | Boss Logic: Phase transition for the final boss. |
| `FinalBossHitCountdownBoris` | Block | `{ ... }` | Boss Logic: Countdown trigger for Boris. |
| `FinalBossHitCountdownExplosive` | Block | `{ ... }` | Boss Logic: Countdown trigger for explosives. |
| `FinalBossHitCountdownHoly` | Block | `{ ... }` | Boss Logic: Countdown trigger for holy attacks. |
| `FinalBossPupils` | Block | `{ ... }` | Boss Logic: Pupil state management. |
| `FinalBossShieldHealth` | Block | `{ ... }` | Boss Logic: Shield health management. |
| `FinalBossShield` | Enum/String | `None, DestroyerShieldBash` | Applies or references the 'FinalBossShield' effect/state. |
| `FinalBossSyncAnimations` | Block | `{ ... }` | Boss Logic: Synchronizes multi-part boss animations. |
| `FlingObjectsOnTop` | Number | `8` | Applies or references the 'FlingObjectsOnTop' effect/state. |
| `FlushmasterCelebration` | Enum/String | `celebrate` | Applies or references the 'FlushmasterCelebration' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `ForceDodgeEverything` | Number | `1` | Applies or references the 'ForceDodgeEverything' effect/state. |
| `FormChangeDuringWeatherElement` | Block | `{ ... }` | Logic: Changes form automatically during specific weather conditions. |
| `FormChangeHealthThreshold` | Block | `{ ... }` | Logic: Changes form when health crosses a threshold. |
| `FormChangeOffMap` | Block | `{ ... }` | Logic: Changes form when pushed off the map. |
| `FormChangeOnElementInfluence` | Block | `{ ... }` | Logic: Changes form when affected by an element. |
| `FormChangeWhenBuddyDies` | Enum/String | `Rage` | Applies or references the 'FormChangeWhenBuddyDies' effect/state. |
| `FormChangeWhileHasStatus` | Block | `{ ... }` | Logic: Changes form automatically while possessing a specific status. |
| `FormChangeWhilePrimingAbility` | Block | `{ ... }` | Logic: Changes form while preparing/priming a specific ability. |
| `FormChanger` | Block | `{ ... }` | AI Role: Designates the character as one that frequently shifts forms. |
| `FreePathfindElement` | Enum/String | `Water` | Applies or references the 'FreePathfindElement' effect/state. |
| `FullBlockEverythingTo0Damage` | Number | `1` | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. |
| `FullBlockEverything` | Number | `1` | Applies or references the 'FullBlockEverything' effect/state. |
| `GasCanBehavior` | Number | `1` | Applies or references the 'GasCanBehavior' effect/state. |
| `GasCloudBehavior2` | Number | `2` | Applies or references the 'GasCloudBehavior2' effect/state. |
| `GeminiTwin` | Number | `1` | Applies or references the 'GeminiTwin' effect/state. |
| `GlobalManaDrainAura` | Number | `-1` | Applies or references the 'GlobalManaDrainAura' effect/state. |
| `GoopImmunity` | Number | `1` | Applies or references the 'GoopImmunity' effect/state. |
| `GoopWalk` | Number | `1` | Applies or references the 'GoopWalk' effect/state. |
| `GroundFlopper` | Enum/String | `DefaultMove, MoveOne` | Applies or references the 'GroundFlopper' effect/state. |
| `GuillotinaDeathHead` | Number | `1` | Applies or references the 'GuillotinaDeathHead' effect/state. |
| `HPAltStates` | Block | `{ ... }` | Visual: Alternative sprite states based on current health. |
| `HarpoonTrapPassive` | Enum/String | `HarpoonTrapPull` | Applies or references the 'HarpoonTrapPassive' effect/state. |
| `HealNeighborsEachTurn` | Block | `{ ... }` | Passive: Restores health to adjacent allies at the start of the turn. |
| `HealthGain` | Number | `1, 5, 8` | Applies or references the 'HealthGain' effect/state. |
| `HealthPickup` | Block | `{ ... }` | Pickup Logic: Defines what happens when a health item is collected. |
| `HealthRegenUp` | Number | `2, 4` | Applies or references the 'HealthRegenUp' effect/state. |
| `HiddenDoomed` | Number | `2` | Applies or references the 'HiddenDoomed' effect/state. |
| `HitlerExecute` | Block | `{ ... }` | Boss Logic: Specific execution or ultimate attack state. |
| `IceBlockBehavior` | Number | `1` | Applies or references the 'IceBlockBehavior' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `IllusionTint` | Number | `1` | Applies or references the 'IllusionTint' effect/state. |
| `ImmediateAbilityReaction` | Enum/String | `ChubsGoop, BumbleButt, NubsGoop` | Reaction: Executes an ability instantly, interrupting the current sequence. |
| `ImmobilePassive` | Number | `1` | Applies or references the 'ImmobilePassive' effect/state. |
| `InfiniteRebirth` | Block | `{ ... }` | Logic: Allows the character to revive endlessly. |
| `InheritSpawnerStats` | Number | `1` | Applies or references the 'InheritSpawnerStats' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `InnateElement` | Enum/String | `Water, Fire` | Applies or references the 'InnateElement' effect/state. |
| `InsertIntoBackgroundPlaceholder` | Number | `1` | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. |
| `JohnnyNeedsWashing` | Block | `{ ... }` | Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state. |
| `JohnnyWasher` | Enum/String | `BBTransformZealot` | Applies or references the 'JohnnyWasher' effect/state. |
| `KaijuKnockbackImmune` | Number | `1` | Applies or references the 'KaijuKnockbackImmune' effect/state. |
| `KaijuWinCon` | Enum/String | `pyrophina, zaratana` | Applies or references the 'KaijuWinCon' effect/state. |
| `KineticSpikes` | Number | `1, 5` | Applies or references the 'KineticSpikes' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `LegacySpawnSavedCatIfExists` | Enum/String | `Legacy_Marshmallow_StolenCatID` | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. |
| `LimitDamage` | Number | `1` | Applies or references the 'LimitDamage' effect/state. |
| `LimitHeal` | Number | `1, 0` | Applies or references the 'LimitHeal' effect/state. |
| `LockOrientationFaceTile` | Array | `[ 0 0 ]` | Applies or references the 'LockOrientationFaceTile' effect/state. |
| `LoopingSoundWhileAlive` | Enum/String | `Twister_loop, BigUFO_ambient_looping, Bomb_FuseLoop` | Applies or references the 'LoopingSoundWhileAlive' effect/state. |
| `MagicDamageImmune` | Number | `1` | Applies or references the 'MagicDamageImmune' effect/state. |
| `MamaCatAnimations` | Number | `1` | Applies or references the 'MamaCatAnimations' effect/state. |
| `ManaPickup` | Block | `{ ... }` | Pickup Logic: Defines what happens when a mana item is collected. |
| `ManglerMonsterPassive` | Enum/String | `ManglerMonsterDashAttack` | Applies or references the 'ManglerMonsterPassive' effect/state. |
| `MegaDinoDropController` | Block | `{ ... }` | Boss Logic: Manages loot drops for the Mega Dino. |
| `MeleeRevengeDamage` | Block | `{ ... }` | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. |
| `MimicSpawnerAttacks` | Number | `1, -1` | Applies or references the 'MimicSpawnerAttacks' effect/state. |
| `MiniVolcanoReaction` | Enum/String | `ThrobShot_Reaction, MiniVolcano_Spurt` | Applies or references the 'MiniVolcanoReaction' effect/state. |
| `MinimumKnockbackFromAllDamage` | Number | `1` | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. |
| `MinimumKnockbackFromPhysicalAttacks` | Number | `1` | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. |
| `MissChance` | Number | `20` | Applies or references the 'MissChance' effect/state. |
| `ModularPickup` | Block | `{ ... }` | Pickup Logic: Defines what happens when a modular item is collected. |
| `MonkCatReactionAbilities` | Block | `{ ... }` | Reaction: Specific counter-attack or dodge abilities used by the Monk class. |
| `MoonHeadCrackedVisual` | Enum/String | `Cracked` | Applies or references the 'MoonHeadCrackedVisual' effect/state. |
| `MotherGrowController` | Block | `{ ... }` | Boss Logic: Manages the growth phases of the Mother boss. |
| `MotherTumorPassive` | Block | `{ ... }` | Boss Logic: Passive effects applied to the Mother's tumors. |
| `MotherTumorSpawnInCapture` | Block | `{ ... }` | Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning. |
| `Mount` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Mount' state. |
| `MoveAfterAnyAttemptedAttack` | Block | `{ ... }` | AI Movement: Forces a move action immediately after attacking, even if it missed. |
| `MoveAwayFromDamageSource` | Block | `{ ... }` | AI Movement: Moves away from the source of recent damage. |
| `MoveAwayWhenEnemyAdjacent` | Block | `{ ... }` | AI Movement: Moves away if an enemy enters an adjacent tile. |
| `MoveTowardsDamageSource` | Enum/String | `MoveOne, { ... }` | AI Movement: Closes distance on the last source of damage. |
| `MoveTowardsKillers` | Enum/String | `ReaperRevenge, { ... }` | AI Movement: Seeks out entities that have recently killed an ally. |
| `MoveWhenDamaged` | Enum/String | `move, TKNG_Hop, { ... }` | AI Movement: Forces a reposition when taking damage. |
| `MovementReaction` | Block | `{ ... }` | Reaction: Triggers an effect or ability when forced to move. |
| `MultiSpawnOnDeath` | Block | `{ ... }` | Event Trigger: Spawns multiple entities upon death. |
| `MulticatHeads` | Number | `0` | Applies or references the 'MulticatHeads' effect/state. |
| `MutateAfterXTurns` | Number | `3` | Applies or references the 'MutateAfterXTurns' effect/state. |
| `MutateViaAbility` | Enum/String | `BBTransformMutant` | Applies or references the 'MutateViaAbility' effect/state. |
| `MuteDemonicGlyphDisplay` | Number | `1` | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. |
| `NoHealthOnlyShield` | Number | `1` | Applies or references the 'NoHealthOnlyShield' effect/state. |
| `OrthogonalAIDangerZone` | Number | `10` | Applies or references the 'OrthogonalAIDangerZone' effect/state. |
| `OverrideMaxHealth` | Number | `25, 1` | Applies or references the 'OverrideMaxHealth' effect/state. |
| `PackHunting` | Number | `1` | Applies or references the 'PackHunting' effect/state. |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` | Passive: Activates only when afflicted by the specified element. |
| `PassiveWhenDead` | Block | `{ ... }` | Passive: Activates only while the character is dead (e.g., corpse effects). |
| `PassiveWhileHasStatus` | Block | `{ ... }` | Passive: Activates only while the character has the specified status. |
| `PassiveWhileNotHasStatus` | Block | `{ ... }` | Passive: Activates only while the character does NOT have the specified status. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `Phasing` | Number | `1` | Applies or references the 'Phasing' effect/state. |
| `Plant` | Number | `1` | Applies or references the 'Plant' effect/state. |
| `PoisonThorns` | Number | `3` | Applies or references the 'PoisonThorns' effect/state. |
| `PrioritizeAggroTarget` | Number | `1` | Applies or references the 'PrioritizeAggroTarget' effect/state. |
| `PrioritizeFarAwayTargets` | Number | `1, 10` | Applies or references the 'PrioritizeFarAwayTargets' effect/state. |
| `PrioritizeHitDifferentTargets` | Number | `1` | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. |
| `PrioritizePlayerCats` | Number | `1` | Applies or references the 'PrioritizePlayerCats' effect/state. |
| `PrioritizeWeakestEnemy` | Number | `1` | Applies or references the 'PrioritizeWeakestEnemy' effect/state. |
| `ProtectTargetedAllies` | Block | `{ ... }` | AI Logic: Navigates to intercept attacks directed at allies. |
| `RandomPassivePool` | Block | `{ ... }` | Logic: Grants a random passive from the specified pool upon spawning. |
| `RandomizeAIWeightsEachTurn` | Array | `[ { decision_weights default move_weights keep_distance }..., [ { decision_weights blind move_weights chubs_and_nubs_bl..., [ { decision_weights default move_weights stay_close } { ...` | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. |
| `ReflectProjectiles` | Number | `1, 100%, { ... }` | Passive: Reflects incoming projectiles back at the attacker. |
| `ReturnBoundItemOnBattleEnd` | Number | `1` | Applies or references the 'ReturnBoundItemOnBattleEnd' effect/state. |
| `RevengeDamage` | Block | `{ ... }` | Reaction: Deals damage when taking damage. |
| `Robot` | Number | `1, { ... }` | Character Form: Behavior and stats for the 'Robot' state. |
| `RunInXTurns` | Number | `1, 2, 3` | Applies or references the 'RunInXTurns' effect/state. |
| `RunWhenKittensDead` | Number | `1` | Applies or references the 'RunWhenKittensDead' effect/state. |
| `RunWhenLastPlayerCatIsCharmed` | Block | `{ ... }` | AI Logic: Flee logic when the player team is entirely crowd-controlled. |
| `SafeDoomed` | Number | `1` | Applies or references the 'SafeDoomed' effect/state. |
| `ScalingAttackAnimation` | Block | `{ ... }` | Visual: Animation scales based on damage output. |
| `SecurityBotProtect` | Block | `{ ... }` | AI Logic: Guarding behavior for Security Bot units. |
| `SetSpellCosts` | Number | `0` | Applies or references the 'SetSpellCosts' effect/state. |
| `SharePickupsWithSpawner` | Number | `1, 0` | Applies or references the 'SharePickupsWithSpawner' effect/state. |
| `SharePickups` | Block | `{ ... }` | Passive: Item pickups collected by this unit are shared with others. |
| `SharkySmellsBlood` | Number | `1` | Applies or references the 'SharkySmellsBlood' effect/state. |
| `SkipFirstRounds` | Block | `{ ... }` | AI Logic: Passes turn for the first X rounds of combat. |
| `SlotMachineRollPool` | Block | `{ ... }` | Logic: Defines the possible outcomes for slot machine enemies. |
| `SmallRockBehavior` | Number | `5, 0, { ... }` | AI Logic: Movement/interaction profile for small rocks. |
| `SpawnCreepOnHitKnockback` | Number | `1` | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. |
| `SpawnCreepOnHit` | Number | `1` | Applies or references the 'SpawnCreepOnHit' effect/state. |
| `SpawnOnDeath` | Enum/String | `BiggestFood, FrankPinky, { ... }` | Event Trigger: Spawns a specific entity when killed. |
| `SpawnThingOnDamage` | Block | `{ ... }` | Event Trigger: Spawns an entity when taking damage. |
| `SpawnThingOnDeath` | Enum/String | `Food, Gamete, Boulder` | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `SpawnerCatDataReference` | Number | `1` | Applies or references the 'SpawnerCatDataReference' effect/state. |
| `SpeedUp` | Number | `6, 2` | Applies or references the 'SpeedUp' effect/state. |
| `SpewerAltGraphics` | Block | `{ ... }` | Visual: Alternative graphics for Spewer enemies. |
| `SpreadWater` | Number | `1` | Applies or references the 'SpreadWater' effect/state. |
| `SproutsGrantMovement` | Number | `1` | Applies or references the 'SproutsGrantMovement' effect/state. |
| `StartDead` | Number | `100%` | Applies or references the 'StartDead' effect/state. |
| `StartOffMap` | Number | `1` | Applies or references the 'StartOffMap' effect/state. |
| `StatusAfterXTurns` | Block | `{ ... }` | Event Trigger: Applies a status effect after X turns have passed. |
| `StatusCollector` | Block | `{ ... }` | Passive: Gains benefits based on the number of statuses applied to them. |
| `StatusEachTurnBeginIfHasStatus` | Block | `{ ... }` | Event Trigger: Applies a status at the start of the turn if a prerequisite status is met. |
| `StatusEachTurnEndIfEnabledAtStartOfTurn` | Block | `{ ... }` | Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start. |
| `StatusEachTurnEnd` | Block | `{ ... }` | Event Trigger: Applies a status at the end of every turn. |
| `StatusImmunity` | Enum/String | `Poison, [ Poison, Bleed ], Webbed` | Applies or references the 'StatusImmunity' effect/state. |
| `StatusOnDie` | Block | `{ ... }` | Event Trigger: Applies statuses when the character dies. |
| `StatusOnEndMove` | Block | `{ ... }` | Event Trigger: Applies statuses when the character finishes moving. |
| `StatusOnEnemyConfused` | Block | `{ ... }` | Event Trigger: Applies statuses when an enemy becomes confused. |
| `StatusOnGainCoins` | Block | `{ ... }` | Event Trigger: Applies statuses when coins are collected. |
| `StatusOnKill` | Block | `{ ... }` | Event Trigger: Applies statuses when the character kills an enemy. |
| `StatusOnSpawnIn` | Block | `{ ... }` | Event Trigger: Applies statuses immediately when spawned. |
| `StatusOnTookDamageFromAbility` | Block | `{ ... }` | Event Trigger: Applies statuses when taking damage from an ability. |
| `StatusOnTookDamage` | Block | `{ ... }` | Event Trigger: Applies statuses when the character takes damage. |
| `StatusOverlappingCharactersAndDie` | Block | `{ ... }` | Event Trigger: Applies statuses to overlapping entities, then destroys self. |
| `StatusWhenStatusCompletelyRemoved` | Block | `{ ... }` | Event Trigger: Applies statuses when a tracked status effect is fully cleansed. |
| `StrengthUp` | Number | `2` | Applies or references the 'StrengthUp' effect/state. |
| `StripStatuses` | Number | `1` | Applies or references the 'StripStatuses' effect/state. |
| `StunImmunity` | Number | `1, { ... }` | Passive: Prevents Stun from being applied. |
| `SupportDieInsteadOfRun` | Block | `{ ... }` | AI Logic: Forces a support unit to die rather than flee. |
| `SupportFormChangeInsteadOfRun` | Enum/String | `Attacker, { ... }` | AI Logic: Forces a support unit to transform rather than flee. |
| `SurviveAt1HP` | Number | `1` | Applies or references the 'SurviveAt1HP' effect/state. |
| `SwimmingFormChange` | Block | `{ ... }` | Logic: Automates form change when entering/exiting water. |
| `SyncFormsWithBuddy` | Block | `{ ... }` | Logic: Forces this character's form to match their familiar/buddy. |
| `T3HitlerSpawningPhase` | Block | `{ ... }` | Boss Logic: Minion spawn phase for the T3 Hitler boss. |
| `TVBotDisableAttack` | Number | `1` | Applies or references the 'TVBotDisableAttack' effect/state. |
| `TVBotDisableMove` | Number | `1` | Applies or references the 'TVBotDisableMove' effect/state. |
| `TVBotDisableSpells` | Number | `1` | Applies or references the 'TVBotDisableSpells' effect/state. |
| `TVBotScreen` | Block | `{ ... }` | Visual: TV Bot screen state. |
| `TagGreed` | Enum/String | `bishop_hat, pickup, food` | Applies or references the 'TagGreed' effect/state. |
| `TakeWeaponFromSpawner` | Number | `1` | Applies or references the 'TakeWeaponFromSpawner' effect/state. |
| `TallTumorManaBurn` | Enum/String | `TT_ManaBurn` | Applies or references the 'TallTumorManaBurn' effect/state. |
| `Tall` | Number | `1` | Applies or references the 'Tall' effect/state. |
| `Terminator2Chase` | Enum/String | `move` | Applies or references the 'Terminator2Chase' effect/state. |
| `Terminator2Run` | Block | `{ ... }` | AI Movement: Specific run logic for Terminator2. |
| `TerminatorChase` | Block | `{ ... }` | AI Movement: Specific chase logic for Terminator. |
| `TerminatorSkin` | Block | `{ ... }` | Visual: Skin definition for Terminator. |
| `Thorns` | Number | `5, 2, 3` | Applies or references the 'Thorns' effect/state. |
| `TileElementDamageImmunity` | Enum/String | `Ice` | Applies or references the 'TileElementDamageImmunity' effect/state. |
| `TileTrail_Ahead` | Enum/String | `FireTile, OilTile, WaterTile` | Applies or references the 'TileTrail_Ahead' effect/state. |
| `TileTrail` | Enum/String | `ShadowTile, CreepTile` | Applies or references the 'TileTrail' effect/state. |
| `TinkererBasicAttackSwitching` | Block | `{ ... }` | Logic: Allows Tinkerer to swap basic attacks. |
| `TireBehavior` | Number | `1` | Applies or references the 'TireBehavior' effect/state. |
| `TormentorHeal` | Number | `1` | Applies or references the 'TormentorHeal' effect/state. |
| `TowerDefenseReflex` | Enum/String | `attack` | Applies or references the 'TowerDefenseReflex' effect/state. |
| `TrackAmountKilledByPlayer` | Enum/String | `BonusBirdsKilled` | Applies or references the 'TrackAmountKilledByPlayer' effect/state. |
| `Trample` | Number | `6, 5, 3` | Applies or references the 'Trample' effect/state. |
| `TransformInXTurns` | Block | `{ ... }` | Logic: Forces a form change after X turns. |
| `TransformOnDeathImmediately` | Enum/String | `NoHead, { ... }` | Logic: Bypasses death sequence to instantly assume a new form. |
| `TransformOnDeath` | Enum/String | `RatKing, Carcus, SimonFlopper` | Applies or references the 'TransformOnDeath' effect/state. |
| `TransformOnElementInfluence` | Block | `{ ... }` | Logic: Changes form when affected by elements. |
| `TransformOnElementInfluencex` | Block | `{ ... }` | Logic: Variant element influence transformation. |
| `TransformOnStatusThreshold` | Block | `{ ... }` | Logic: Changes form when a status effect reaches a certain stack count. |
| `TransformWhenBuddyDies` | Enum/String | `UltraOrnstein, UltraSmough` | Applies or references the 'TransformWhenBuddyDies' effect/state. |
| `Trapper` | Block | `{ ... }` | Character Form: Behavior and stats for the 'Trapper' state. |
| `TutorialBossRiggedFight` | Number | `16` | Applies or references the 'TutorialBossRiggedFight' effect/state. |
| `TwisterFling` | Block | `{ ... }` | Logic: Fling behavior for tornado attacks. |
| `UncappedHP` | Number | `1` | Applies or references the 'UncappedHP' effect/state. |
| `Undead` | Number | `1` | Applies or references the 'Undead' effect/state. |
| `UnlimitedDeathRattleRevive` | Block | `{ ... }` | Logic: Endless resurrection on death. |
| `UnlockOrientation` | Number | `1` | Applies or references the 'UnlockOrientation' effect/state. |
| `UpTireBehavior` | Number | `5` | Applies or references the 'UpTireBehavior' effect/state. |
| `UseAbilityWhenOutOfStatus` | Block | `{ ... }` | Logic: Casts a specific ability the moment a status effect expires. |
| `UseAbilityWhenShieldDepleted` | Enum/String | `T3Pebbles_PrimeBoulderDrop` | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. |
| `UseAbility` | Enum/String | `MegaGuppy_SummonTheChild, TormentorRuneAbsorb` | Logic: Forces execution of an ability. |
| `Wall` | Number | `1` | Applies or references the 'Wall' effect/state. |
| `WaterWalk` | Number | `1` | Applies or references the 'WaterWalk' effect/state. |
| `WeaponsDontLoseDurability` | Number | `1` | Applies or references the 'WeaponsDontLoseDurability' effect/state. |
| `WeremanTransformationReceiver` | Enum/String | `CaveManTransform, CaveWomanDropTransform` | Applies or references the 'WeremanTransformationReceiver' effect/state. |
| `WhitelistPickupType` | Enum/String | `food` | Applies or references the 'WhitelistPickupType' effect/state. |
| `WideBackstab` | Number | `1` | Applies or references the 'WideBackstab' effect/state. |
| `WispDodge` | Number | `1` | Applies or references the 'WispDodge' effect/state. |
| `YOffset` | Enum/String | `.35, -.18` | Applies or references the 'YOffset' effect/state. |
| `ZeroKnockbackDamage` | Number | `1` | Applies or references the 'ZeroKnockbackDamage' effect/state. |

### Context: `pattern`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_all_shuffle` | Array | `[ YetiSlam YetiSlam YetiSlam YetiBite YetiBite YetiBite Y..., [ attack DybbukWisps DybbukRePossess ]` |  |
| `do_all` | Array | `[ CovenFamine CovenRise3 ], [ CovenWar CovenRise4 ], [ CovenPestilence CovenRise2 ]` |  |
| `do_best_multiple` | Array | `[ attack spell0 spell1 spell2 spell3 spell4 weapon trinket ]` |  |
| `do_best` | Array | `[ JohnnyPush JohnnyPull ]` |  |
| `do_nothing` | Array | `[ ]` |  |
| `do_priority_alternating` | Array | `[ *BadBone, *GoodBone, BadBone_copy, GoodBone_copy, BadBo...` |  |
| `do_priority` | Array | `[ *QueenWeb, attack, QueenMinis ], [ BumblefootEatCorpse, BumblefootEatCat, BumblefootBoneSh..., [ *RockToss_BomberRat, RockToss_BomberRat ]` |  |
| `do_random` | Array | `[ Escape attack DybbukReanimate ], [ ScaryHaunt ScaryFear ], [ Escape attack DybbukReanimate DybbukWisps ]` |  |
| `do_strict` | Array | `[ MCBlizzard ], [ MCFlamethrower ], [ MCStorm ]` |  |
| `do` | Enum/String | `**SimonFlopper_WiggleChance, **SimonFlopper_WiggleGuaranteed, **SimonFlopper_WiggleFake` |  |
| `move_then_do_all` | Array | `[ LennyShove, LennyGrabDead, LennyGrab ]` |  |
| `move_then_do_priority` | Array | `[ BBPickupCrown, *attack, *BBToss ], [ DrinkUp attack ], [ BBPickupCrown, *BBToss, *attack ]` |  |
| `move_then_do_random` | Array | `[ CerberubsJumpBlind CerberubsJumpNormal ], [ ClotEvolve ClotFailEvolve ], [ ClotEvolveCatCopy ClotFailEvolve ]` |  |
| `move_then_do` | Enum/String | `SimonFlopper_SpawnMinion, NubsJump, attack` |  |

### Context: `properties`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `access_to_player_inventory` | Boolean | `false, true` |  |
| `act_points` | Number | `2, 0, 4` |  |
| `aggro_target_is_enemy` | Boolean | `true` |  |
| `ai_scale` | Enum/String | `.25, .5, .01` |  |
| `allow_flying_effect` | Boolean | `true` |  |
| `allow_offmap_corpse` | Boolean | `true` |  |
| `allow_passive_spelltransforming` | Boolean | `true` |  |
| `allow_replacebrain` | Boolean | `false` |  |
| `always_face_forward` | Boolean | `true` |  |
| `always_triggers_traps` | Boolean | `true` |  |
| `aoe_pierce_mode` | Enum/String | `block` |  |
| `auto_run_priority` | Enum/String | `support, default, stationary` |  |
| `banned_elite_buffs` | Array | `[ Protected ], [ Mad ], [ Twin ]` |  |
| `base_crit_chance` | Number | `0` |  |
| `base_health_regen` | Number | `0` |  |
| `base_health` | Number | `0` |  |
| `base_initial_mana` | Number | `0` |  |
| `base_initiative` | Number | `-1, 0` |  |
| `base_mana_regen` | Number | `999, 0, 3` |  |
| `base_mana` | Number | `0` |  |
| `base_movement` | Number | `4` |  |
| `blocking` | Boolean | `false` |  |
| `boss_minions_runaway` | Boolean | `false` |  |
| `can_be_backstabbed` | Boolean | `false` |  |
| `can_be_champion` | Boolean | `false, true` |  |
| `can_be_elite` | Boolean | `false` |  |
| `can_be_overkilled` | Boolean | `false, true` |  |
| `can_collect_coins` | Boolean | `false, true` |  |
| `can_eat_food` | Boolean | `false, true` |  |
| `can_grant_extra_turns` | Boolean | `false` |  |
| `can_run` | Boolean | `false` |  |
| `capture_as_cat` | Boolean | `true` |  |
| `catdata_ignore_skills` | Boolean | `true` |  |
| `champion` | Boolean | `true` |  |
| `corpse_health` | Enum/String | `indestructible, 0, 3` |  |
| `deathpoof_size` | Number | `1` |  |
| `disallow_items` | Enum/String | `Nuke, all` |  |
| `disperse_main_turns` | Boolean | `false, true` |  |
| `dispersed_bonus_turns_before_cats` | Boolean | `false, true` |  |
| `dispersed_bonus_turns_consider_initiative` | Boolean | `false` |  |
| `dispersed_bonus_turns` | Number | `2, 0, 3` |  |
| `divine_shield` | Number | `1, 2, 3` |  |
| `elements` | Array | `[ Rock ], [ Earth ], [ Dust ]` |  |
| `elite` | Boolean | `true` |  |
| `evenly_dispersed_bonus_turns` | Number | `1, 2, 3` |  |
| `exclude_from_hallucinate` | Boolean | `true` |  |
| `faction` | Enum/String | `none, enemies, birds` |  |
| `first_turn_is_main_turn` | Boolean | `true` |  |
| `flying` | Boolean | `true` |  |
| `force_not_familiar` | Boolean | `true` |  |
| `health` | Number | `2, 16, 7` |  |
| `held_coins` | Number | `5, 0, [ 5 10 ]` |  |
| `hidden_tag` | Enum/String | `angeljunk, [ bird bonusbird ], the_coven` |  |
| `hidden_tags` | Enum/String | `terminator_mini, [ terminator_mini dc_cat ]` |  |
| `hint_no_corpse` | Boolean | `true` |  |
| `ignore_mouseover` | Boolean | `true` |  |
| `ignore_tiles` | Boolean | `true` |  |
| `inanimate_can_receive_specific_statuses` | Array | `[ Burn ]` |  |
| `inanimate` | Boolean | `true` |  |
| `inherit_faction` | Boolean | `false, true` |  |
| `initial_health` | Number | `4, 14, 10` |  |
| `initiative` | Number | `999, -100, -999` |  |
| `is_player_cat` | Boolean | `false, true` |  |
| `kill_required` | Boolean | `false, true` |  |
| `knockback_immune` | Boolean | `true` |  |
| `last_turn_is_main_turn` | Boolean | `true` |  |
| `layer` | Enum/String | `gas, pickups, all` |  |
| `lock_orientation` | Array | `[ -1, 0 ], [ 0, -1 ], [ -1 0 ]` |  |
| `mana_matters` | Boolean | `false, true` |  |
| `mana_regen` | Number | `999` |  |
| `mana` | Number | `100` | Base maximum mana pool. |
| `mouseover_priority` | Number | `10` |  |
| `move_block` | Enum/String | `nothing, everything_even_when_dead` |  |
| `move_points` | Number | `2` |  |
| `movement` | Number | `5, 4, 3` |  |
| `must_start_facing_camera` | Boolean | `false` |  |
| `pickup_type` | Number | `1` |  |
| `round_end_bonus_turns` | Number | `1` |  |
| `round_start_bonus_turns` | Number | `1` |  |
| `scale` | Number | `1.3` |  |
| `shield` | Number | `65, 50, 100` |  |
| `size` | Enum/String | `2x2, gemini, 3x3` |  |
| `speculative_inanimate` | Boolean | `false` |  |
| `static` | Boolean | `true` |  |
| `tag` | Array | `[ cat blob ], animal, rat` | Specific entity tag required. |
| `tags` | Array | `[ cat robot ]` |  |
| `takes_main_turn` | Boolean | `false` |  |
| `takes_turns` | Boolean | `false, true` |  |
| `tall` | Boolean | `true` |  |
| `tile_desire_cost` | Number | `200, 100` |  |
| `two_fronts_switch` | Boolean | `true` |  |
| `two_fronts` | Boolean | `true` |  |
| `type` | Enum/String | `object, boss, cat` | Classification/category type. |
| `uncapturable` | Boolean | `false, true` |  |
| `view_bleeding_characters_as_enemies` | Boolean | `true` |  |
| `view_bugs_as_enemies` | Boolean | `true` |  |
| `visually_spiky` | Boolean | `true` |  |
| `weak_threshold` | Number | `1, 5, 0` |  |

### Context: `round_end_bonusturn_pattern`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_all` | Array | `[ *QueenHippoUppercut QueenHippoAttack move QueenHippoTire ], [ MoonHead_ChewCat MoonHead_CallForHelp MoonHead_RefreshB..., [ MoonHead_CallForHelp MoonHead_RefreshBrace ]` |  |
| `do_nothing` | Array | `[ ]` |  |
| `do_one` | Array | `[ **ZaratanaVSWeatherRoar **ZaratanaVSRoar ], [ **PyrophinaVSWeatherRoar **PyrophinaVSRoar ]` |  |
| `do_priority` | Array | `[ NCReanimate NCGravecrawlFAR ]` |  |
| `do_random` | Array | `[ TKNG_Spread TKNG_Kneel TKNG_Roulette TKNG_GoAway ], [ SimonSays_Scatter, SimonSays_ComeHere, SimonSays_GoAway ]` |  |
| `do` | Enum/String | `RallyMaggots, CutterCut, SuckMF` |  |

### Context: `round_start_bonusturn_pattern`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `do_priority` | Array | `[ MutateAOE SpawnMaggots ]` |  |

### Context: `sound`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `SE_CatSwishThrow` | Enum/String | `SE_ThrowGrenade` | Applies or references the 'SE_CatSwishThrow' effect/state. |
| `SE_Cat_ShadowStepIn` | Enum/String | `SE_Terminator_ShadowStepIn` | Applies or references the 'SE_Cat_ShadowStepIn' effect/state. |
| `SE_Cat_ShadowStepOut` | Enum/String | `SE_Terminator_ShadowStepOut` | Applies or references the 'SE_Cat_ShadowStepOut' effect/state. |
| `SE_Cat_StompLegMove` | Enum/String | `SE_Terminator2_WalkLeg, SE_Terminator1_WalkLeg` | Applies or references the 'SE_Cat_StompLegMove' effect/state. |
| `SE_Cat_WeaponLower` | Enum/String | `SE_Terminator_WeaponLower` | Applies or references the 'SE_Cat_WeaponLower' effect/state. |
| `SE_Cat_WeaponRaise` | Enum/String | `SE_Terminator_WeaponRaise` | Applies or references the 'SE_Cat_WeaponRaise' effect/state. |
| `SE_Cat_bearHug` | Enum/String | `SE_Terminator_bearHug` | Applies or references the 'SE_Cat_bearHug' effect/state. |
| `SE_Cat_equipWeapon` | Enum/String | `SE_TerminatorSwapWeapon` | Applies or references the 'SE_Cat_equipWeapon' effect/state. |
| `SE_PetRock_Dash` | Enum/String | `SE_PetBoulder_Dash` | Applies or references the 'SE_PetRock_Dash' effect/state. |
| `alt_sounds` | Array | `[ [ SE_BirdSmall_DyingCall SE_BirdDying_Dove ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Blackbird ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Hummingbird ]` |  |
| `animation_prefix` | Enum/String | `RattleSnake` |  |

### Context: `stats`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `charisma` | Number | `5, 8, 9` |  |
| `constitution` | Number | `5, 8, 9` |  |
| `dexterity` | Number | `5, 8, 9` |  |
| `intelligence` | Number | `5, 10, 9` |  |
| `luck` | Number | `5, 8, 3` |  |
| `speed` | Number | `5, 2, 7` | Base speed/initiative stat. |
| `strength` | Number | `5, 8, 4` |  |

### Context: `statuses`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Consumed` | Block | `{ ... }` | State triggered when the entity is eaten/consumed. |

### Context: `statuses_on_enter_form`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility` | Enum/String | `KirbySpit` | Logic: Forces execution of an ability. |

### Context: `turns`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `dispersed_bonus_turns` | Number | `1, 2, 0` |  |
| `evenly_dispersed_bonus_turns` | Number | `1, 2` |  |
| `round_end_bonus_turns` | Number | `1` |  |
| `round_start_bonus_turns` | Number | `1` |  |
| `takes_main_turn` | Boolean | `false, true` |  |
| `takes_turns` | Boolean | `false, true` |  |
| `wait_till_next_round_to_update_turns` | Boolean | `true` |  |

### Context: `virtual_abilities`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CerberubsJumpBlind` | Block | `{ ... }` | AI Logic: Blind jump attack pattern for Cerberubs. |
| `CerberubsJumpNormal` | Block | `{ ... }` | AI Logic: Normal jump attack pattern for Cerberubs. |
| `CloseConvert` | Block | `{ ... }` | AI State: Logic for converting adjacent units. |
| `DashRandomly` | Block | `{ ... }` | AI Movement: Dashes to a random valid tile. |
| `Escape` | Block | `{ ... }` | AI Movement: Logic for fleeing or escaping the map. |
| `FoodMove` | Block | `{ ... }` | AI Movement: Logic for seeking out food items. |
| `ForceTrample` | Block | `{ ... }` | Logic: Forces movement to act as a trample attack. |
| `LeapClose` | Block | `{ ... }` | AI Movement: Executes a jumping maneuver to close distance. |
| `MoveAway` | Block | `{ ... }` | AI Movement: Moves away from the target. |
| `MoveCenter` | Block | `{ ... }` | AI Movement: Moves toward the center of the map. |
| `MoveClose` | Block | `{ ... }` | AI Movement: Moves into melee range. |
| `MoveForBarrage` | Block | `{ ... }` | AI Movement: Repositions to optimize a barrage attack. |
| `MoveForDash` | Block | `{ ... }` | AI Movement: Repositions to set up a dash attack line. |
| `MoveForGrass` | Block | `{ ... }` | AI Movement: Moves toward grass tiles. |
| `MoveForPounce` | Block | `{ ... }` | AI Movement: Repositions to optimize a pounce trajectory. |
| `MoveForSpin` | Block | `{ ... }` | AI Movement: Repositions into a cluster of enemies for a spin attack. |
| `MoveForThrow` | Block | `{ ... }` | AI Movement: Repositions to gain line of sight for throwing. |
| `MoveOneForPuke` | Block | `{ ... }` | AI Movement: Specific positioning logic for puke attacks. |
| `MoveSpaced` | Block | `{ ... }` | AI Movement: Moves to maintain a specific distance from targets. |
| `MoveToHead` | Block | `{ ... }` | AI Movement: Navigates toward the 'head' or primary target. |
| `MoveTowards` | Block | `{ ... }` | AI Movement: Moves toward the nearest target. |
| `NCGravecrawlFAR` | Block | `{ ... }` | AI Movement: Specific grapple/crawl logic. |
| `ReturnA` | Block | `{ ... }` | Boss Logic: Specific phase return trigger. |
| `RunFar` | Block | `{ ... }` | AI Movement: Maximize distance from targets. |
| `SpearRun` | Block | `{ ... }` | AI Movement: Specific movement logic for Spear enemies. |
| `SuckMF` | Block | `{ ... }` | Character Form: Behavior and stats for the 'SuckMF' state. |
| `TF_TargetAllies` | Block | `{ ... }` | AI Targeting: Prioritizes allies. |
| `TF_TargetEnemies` | Block | `{ ... }` | AI Targeting: Prioritizes enemies. |
| `Unflip` | Block | `{ ... }` | Logic: Reverses a flipped state. |

---

## Events & Encounters

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `10coins` | Block | `{ ... }` | Event Action: Grants or consumes 10 coins. |
| `add_weather` | Enum/String | `SolarFlare` |  |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_twentyfive, choice_leave, choice_dex_alt` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `cha` | Number | `1` |  |
| `con` | Number | `1` |  |
| `copy_results` | Enum/String | `examine, smash` |  |
| `destroy` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Destroy' action. |
| `dex` | Number | `1` |  |
| `gain_familiar` | Enum/String | `Toad` | Event Action: Adds a specific familiar to the party. |
| `get_item_from_pool` | Enum/String | `chapter_rare, food` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `ignore` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Ignore' action. |
| `int` | Number | `1` |  |
| `intro` | Block | `{ ... }` | Event Node: The initial text block when a story event first loads. |
| `label` | String | `"EVENT_PICK_ANSW", "EVENT_OPEN_ANSW", "EVENT_LEAVE_ANSW"` |  |
| `lck` | Number | `1` |  |
| `main` | Block | `{ ... }` | Event Node: The central hub or recurring menu of a story event. |
| `next_event_bonus` | Number | `2` |  |
| `prompt` | String | `"EVENT_BEGGAR_NOTENOUGHMONEY", "EVENT_ABEGGAR_REW2", "EVENT_TRASHBIN_REW3"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `requires_flag` | Enum/String | `SolarFlareUnlocked` | Prerequisite: Must meet this condition. |
| `reward` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `self_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_frame` | Number | `2, 5, 4` |  |
| `spd` | Number | `1` |  |
| `stat_max` | Number | `25, 15, 10` |  |
| `stat_min` | Number | `25, 15, 10` |  |
| `stat` | Enum/String | `lck, none, dex` |  |
| `str` | Number | `1` |  |
| `weight` | Number | `15, .25, .5` | Probability weight for this outcome. |

### Context: `10coins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_ten` |  |
| `get_item_from_pool` | Enum/String | `chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |  |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |  |
| `set_frame` | Number | `2` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |
| `stat` | Enum/String | `coins` |  |
| `weight` | Number | `10` | Probability weight for this outcome. |

### Context: `5coins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_one` |  |
| `get_item_from_pool` | Enum/String | `chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |  |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |  |
| `set_frame` | Number | `2` |  |
| `stat_max` | Number | `5` |  |
| `stat_min` | Number | `5` |  |
| `stat` | Enum/String | `coins` |  |
| `weight` | Number | `5` | Probability weight for this outcome. |

### Context: `CharacterTypeGainsStatusAtBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `tag` | Enum/String | `robot, rat` | Specific entity tag required. |

### Context: `KillEnemyOfTypeAtBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `enemy_type` | Enum/String | `any, cat` |  |
| `fallback_spawn` | Array | `[ TomTom Kitten CatCaller Mangy ]` |  |

### Context: `StatusRandomEnemiesOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `2` | Applies or references the 'Bleed' effect/state. |
| `Fear` | Number | `2, 3` | Applies or references the 'Fear' effect/state. |
| `count` | Number | `1, 99, 2` | Quantity. |

### Context: `a`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"class ability pool", "1 injury", "1"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `activate_p`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_OBELISK_CORE_ACTIVATE_ANSW, QEVENT_OBELISK_MOON_ACTIVATE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest, none` |  |

### Context: `activate_z`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_OBELISK_CORE_ACTIVATE_ANSW, QEVENT_OBELISK_MOON_ACTIVATE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest, none` |  |

### Context: `altar_sacrifice`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"king intro"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `arm`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_ARMINSIDE_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `attach_amplifier`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_THEHEAD_AMPLIFIER_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `attach_antenna`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_GLOWINGORB_ANTENNA_ANSW, QEVENT_VOLCANO_ANTENNA_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `attach_leech`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_THROBBINGARTERY_ATTACH_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `attack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_ATTACK_ANSW", "EVENT_BREAK_ANSW", "EVENT_BASH_ANSW"` |  |
| `rare` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `stat` | Enum/String | `str` |  |

### Context: `b`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"many injuries", "5", "set ability pool"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `bad`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `battle` | String | `"events/Death.lvl"` |  |
| `conditional_reward` | Block | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `cutscene` | Block | `{ ... }` | Event Node: Triggers a narrative cutscene. |
| `event_now_same_cat` | Enum/String | `StevenFetus, random` |  |
| `event_now` | Enum/String | `StacyMutant2, StacyMutant3, StacyMutant4` |  |
| `gain_disorder_from_pool` | Enum/String | `diseases, all_disorders` |  |
| `gain_immortal_familiar` | Enum/String | `CharmedFlea` |  |
| `get_parasite_from_pool` | Enum/String | `parasites` |  |
| `get_parasite` | Enum/String | `CursedRock` |  |
| `injury` | Enum/String | `con, dex, str` |  |
| `kill` | Enum/String | `cat` |  |
| `lose_item` | Enum/String | `parasite` |  |
| `next_event_bonus` | Number | `-1` |  |
| `party_random_mutation_from_set` | Block | `{ ... }` | Event Reward: Applies a random mutation to the entire party from a specific pool. |
| `permanent_stats` | Block | `{ ... }` | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| `play_animation` | Array | `[ resultLeave 0 ], resultVeryBad, resultHole` |  |
| `prompt` | String | `"QEVENT_STACYMUTANT1_REW4", "QEVENT_STACYMUTANT1_REW4_B", "EVENT_CLOSEDWINDOW_REW7"` |  |
| `reward` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `select_item_from_pool_for_cutscene_only` | Enum/String | `glitched_items` |  |
| `self_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_frame` | Number | `2, 4, 3` |  |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_StacyMutant` |  |

### Context: `bash`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BASH_ANSW", "EVENT_BASHOPEN_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `str` |  |

### Context: `bash_past_alt`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BASH_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `str` |  |

### Context: `bite`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_con` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_WALLOFFLESH_BITE_ANSW, QEVENT_WALLOFFLESH_BITE2_ANSW, QEVENT_THROBBINGARTERY_BITE_ANSW` |  |
| `stat` | Enum/String | `con, str` |  |

### Context: `bite_it_off`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BIGTOE_BITE_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `blue`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `copy_results` | Enum/String | `red` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_BLUE_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `blue_needle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_NEEDLES_BLUE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `lck` |  |

### Context: `body`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_CURSEBODY` |  |
| `stat` | Enum/String | `none` |  |

### Context: `boogers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BEEPIS_ANSW", "EVENT_BOOGERS_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `book`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SOMEOLDBOOK_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `brace`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW2"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `break_ice`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_FROZENHUMANOID_BREAKICE_ANSW"` |  |

### Context: `break_lock`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_LOCKEDCRATE_BREAK_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `bribe`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_BRIBE_ANSW` |  |
| `stat` | Enum/String | `con` |  |

### Context: `button`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `copy_results` | Enum/String | `lever` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_PUSHBUTTON_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `buy1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_one` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BUY_ANSW"` |  |
| `prompt` | String | `"EVENT_TRACY_REW4"` |  |
| `self_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `stat_max` | Number | `1` |  |
| `stat_min` | Number | `1` |  |
| `stat` | Enum/String | `coins` |  |
| `weight` | Number | `1` | Probability weight for this outcome. |

### Context: `c`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"specific disorder", "class passive pool", "all (symmetric)"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `catch`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CATCH_ANSW"` |  |
| `stat` | Enum/String | `spd` |  |

### Context: `challenge_to_game`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DEATH_CHALLENGE_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `chaos_ending`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"chaos ending"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `chapter_cutscene`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"chap"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `charm`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_CHARM_ANSW, "EVENT_CHARM_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `cha` |  |

### Context: `charm_past_alt`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CHARM_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `cha` |  |

### Context: `climb`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CLIMB_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `comfort`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_COMFORT_ANSW"` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `common`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `add_weather` | Enum/String | `RestlessDead, Sandstorm` |  |
| `ally_ambush_next_fights` | Number | `1, 2` |  |
| `ambush_next_basic_fights` | Number | `1` |  |
| `clear_adventure_token` | Enum/String | `AdventureToken_BlueNeedle, AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle` |  |
| `clear_result_animation` | Number | `1` |  |
| `conditional_reward` | Block | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `damage` | Number | `5, [ 5 10 ], [ 3 6 ]` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `decrement_legacy_counter` | Enum/String | `WorldEventLegacyCounter_CrackInTheWall` |  |
| `event_now_same_cat` | Enum/String | `random, ElephantsFootCloser, UnmarkedGrave` |  |
| `event_now` | Enum/String | `random` |  |
| `full_heal` | Number | `1` |  |
| `gain_coins` | Array | `[ 5 15 ], 5, [ 4 8 ]` |  |
| `gain_disorder_from_pool` | Enum/String | `physical_disorders, all_disorders, mental_disorders` |  |
| `gain_disorder` | Enum/String | `Scatological, IntestinalProlapse, Stinky` |  |
| `gain_familiar` | Enum/String | `Snake, CharmedPinky, CharmedFetus` | Event Action: Adds a specific familiar to the party. |
| `gain_food` | Number | `-5, [ 1 4 ], [ 5 10 ]` |  |
| `get_and_equip_item` | Enum/String | `Catnip` |  |
| `get_item_from_pool` | Enum/String | `consumables, [ CarvingKnife RazorBlade ButterflyKnife ], { ... }` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `get_item` | Enum/String | `EnchantingPoop, CatnipBig, SeedBombs` |  |
| `get_parasite_from_pool` | Enum/String | `parasites, [ AmoebaHat AmoebaNeck AmoebaFace ], [ CrimsonMask_Cursed RedCap_Cursed PoundOfFlesh_Cursed ]` |  |
| `get_parasite` | Enum/String | `PawShards, CursedHairball, EnchantingPoop_Cursed` |  |
| `global_effect_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal_disorder` | Number | `1` |  |
| `heal_injury` | Number | `1` |  |
| `heal` | Number | `1, 10, 3` |  |
| `increment_legacy_counter` | Enum/String | `WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyCounter_VolcanoSacrifices, WorldEventLegacyToken_StartDigging` |  |
| `injury` | Enum/String | `spd, radiated, str` |  |
| `kill` | Enum/String | `cat` |  |
| `learn_ability_from_pool` | Enum/String | `AnyUnlocked` |  |
| `lose_item` | Enum/String | `inventory, weapon, equipped` |  |
| `lose_specific_item` | Enum/String | `SlagTight` |  |
| `mutation` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Number | `1, 2, -1` |  |
| `next_event_from_set` | Block | `{ ... }` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN", "EVENT_LOCKEDDOOR_PROMPT1", "EVENT_MYSTERIOUSTENT_PROMPT"` |  |
| `party_damage` | Number | `5, [ 1 6 ], 3` |  |
| `party_heal_disorder` | Number | `2` |  |
| `party_heal` | Number | `1, 100%, 3` |  |
| `party_permanent_stats_exclude_self` | Block | `{ ... }` | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. |
| `party_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. |
| `permanent_stats` | Block | `{ ... }` | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| `play_animation` | Enum/String | `resultLeave, [ resultLeave 0 ], resultConfused` |  |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW5", "EVENT_CLOSEDWINDOW_REW1", "EVENT_CLOSEDWINDOW_REW3"` |  |
| `random_mutation_from_set` | Block | `{ ... }` | Event Reward: Applies a random mutation to a character from a specific pool. |
| `random_mutation` | Number | `1, 2, { ... }` | Event Reward: Applies a completely random mutation to a character. |
| `random_pool` | Array | `[ { prompt "EVENT_KNIFEINTHEWALL_REW1" } { prompt "EVENT_..., [ { permanent_stats { str -1 } } { permanent_stats { dex ..., [ { party_heal 5 gain_food [ 2 4 ]` |  |
| `self_damage` | Number | `1, 99%, 50%` | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_heal` | Number | `10` |  |
| `self_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_adventure_token` | Enum/String | `MysteriousStranger_HasLostFinger, AdventureToken_UnmarkedGraveForced, HasPlayedMysteriousStranger` |  |
| `set_frame` | Number | `2, 5, 3` |  |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_HasRunFromDeath` |  |
| `shop_now` | Enum/String | `Event_SmallShop, TreasureEasy` |  |
| `spawn_unit_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| `spin` | Enum/String | `again` |  |
| `upgrade_ability` | Enum/String | `random` |  |

### Context: `communicate`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_COMMUNICATE_ANSW"` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `concheck`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `conditional_reward`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `else` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Else' action. |
| `prompt` | String | `"EVENT_CATSINHEAT_REW8", "EVENT_CATSINHEAT_REW6"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `reward` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |

### Context: `copy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_COPY_ANSW"` |  |

### Context: `counter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW2"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `crack_open`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CRACKOPEN_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `cross`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CROSS_ANSW"` |  |

### Context: `cut_wires`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CUTWIRES_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `cutscene`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cutscene` | String | `"chaos_ending_good", "desert_intro", "time_machine"` | Event Node: Triggers a narrative cutscene. |
| `skip_result_screen` | Boolean | `true` |  |

### Context: `d`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"all (asymmetric)", "set passive pool", "pool disorder"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `damage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DAMAGE_ANSW", "EVENT_BAHPHOMET_HEALTH_ANSW", "QEVENT_STACYMUTANT3_ANSW2"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `damage_1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DEMONICIDOL_1DAMAGE_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `damage_full`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DEMONICIDOL_FULLDAMAGE_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `damage_half`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DEMONICIDOL_HALFDAMAGE_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `desert_cutscene`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"desert"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `destroy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DESTROY_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `dexcheck`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `dig`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DIG_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `str` |  |

### Context: `disarm`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DISARM_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `dive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DIVE_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `donate`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"Donate"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `donate_10`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_ten` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |
| `stat` | Enum/String | `coins` |  |

### Context: `donate_15`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_ten` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat_max` | Number | `15` |  |
| `stat_min` | Number | `15` |  |
| `stat` | Enum/String | `coins` |  |

### Context: `donate_20`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_twentyfive` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat_max` | Number | `20` |  |
| `stat_min` | Number | `20` |  |
| `stat` | Enum/String | `coins` |  |

### Context: `donate_5`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_one` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat_max` | Number | `5` |  |
| `stat_min` | Number | `5` |  |
| `stat` | Enum/String | `coins` |  |

### Context: `double`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW1"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `drink`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_DRINK_ANSW, "EVENT_DRINK_ANSW"` |  |
| `stat` | Enum/String | `lck, con` |  |

### Context: `eat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_EAT_ANSW", EVENT_EAT_ANSW, "EVENT_DRINK_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `eat_meat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_LEAKINGMEAT_EAT_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `else`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `conditional_reward` | Block | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `damage` | Number | `50%` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `event_now_same_cat` | Enum/String | `Needles` |  |
| `event_now` | Enum/String | `Mirage` |  |
| `gain_disorder` | Enum/String | `AcidReflux, Soulless` |  |
| `get_item_from_pool` | Array | `[ LeafyMask LeafyHat LeafyNecklace DinoHat DinoMask DinoN...` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `next_event_bonus` | Number | `1` |  |
| `party_damage` | Number | `1, 5, [ 10 15 ]` |  |
| `prompt` | String | `"QEVENT_STACYMUTANT1_QUES1", "EVENT_MIRAGE_REW3", "EVENT_MIRAGE_REW4"` |  |
| `random_mutation` | Block | `{ ... }` | Event Reward: Applies a completely random mutation to a character. |
| `random_pool` | Array | `[ { get_item Catnip } { gain_food [ 2 5 ], [ { get_item FrozenHat get_item FrozenMask get_item Froze...` |  |
| `self_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_adventure_token` | Enum/String | `AdventureToken_Mirage1` |  |
| `set_frame` | Number | `4, 3` |  |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_HasRunFromDeath` |  |

### Context: `enter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `hint_chapter_exit` | Enum/String | `dimensionx` |  |
| `label` | String | `"EVENT_HOLEINTHEEARTH_ENTER_ANSW", "EVENT_ENTER_ANSW", QEVENT_DIMENSIONXPORTAL_ENTER_ANSW` |  |
| `stat` | Enum/String | `lck, con, none` |  |

### Context: `enter_crater`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSCRATER_ENTER_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `examine`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `copy_results` | Enum/String | `smash, open` |  |
| `gain_coins` | Array | `[ 5 15 ]` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_EXAMINE_ANSW, "EVENT_EXAMINE_ANSW"` |  |
| `stat` | Enum/String | `lck, int` |  |

### Context: `face`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GIFTOFGLORG_FACE_ANSW"` |  |

### Context: `fiddle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_EXAMINE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `fight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_FIGHT_ANSW", EVENT_FIGHT_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `str` |  |

### Context: `fill_jar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_THEHEAD_FILLJAR_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `find`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GOLEMFIND_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `find_another_way`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_AROUND", "EVENT_FINDANOTHERWAY_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `fire`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW1"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `flush_yourself`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_FLUSHYOURSELF_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |

### Context: `follow`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_FOLLOW_ANSW"` |  |
| `stat` | Enum/String | `spd` |  |

### Context: `free`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_FREE_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `future`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `hint_chapter_exit` | Enum/String | `future` |  |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_FUTURE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `gain_clone_familiar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `PlayerCat_MachineClone` |  |

### Context: `gain_familiar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `initial_health` | Number | `10` |  |
| `object` | Enum/String | `CharmedCaveBaby` |  |

### Context: `get_item_from_pool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Enum/String | `chapter_common, chapter, chapter_rare` |  |
| `prompt` | String | `"EVENT_FRANK2_REW4"` |  |
| `restrict` | Array | `[ weapon, trinket, armor ], consumables, trinket` |  |

### Context: `give_parasite`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BODYOFGLORG_PARASITE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |

### Context: `global_effect_next_fight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CharacterTypeGainsStatusAtBattleStart` | Block | `{ ... }` | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. |
| `Fights` | Number | `1, 3` | Applies or references the 'Fights' effect/state. |
| `KillEnemyOfTypeAtBattleStart` | Block | `{ ... }` | Encounter Modifier: Instantly kills one enemy of the specified type at the start of battle. |
| `StatusRandomEnemiesOnBattleStart` | Block | `{ ... }` | Encounter Modifier: Applies a status effect to a random number of enemies at the start of battle. |

### Context: `go_around`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GOAROUND_ANSW", "EVENT_TAKELONGWAY_ANSW"` |  |
| `stat` | Enum/String | `lck, none, spd` |  |

### Context: `good`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `add_weather` | Enum/String | `MeteorShower, GeomagneticStorm, SolarFlare` |  |
| `ally_ambush_next_fights` | Number | `1` |  |
| `begin_chapter` | Enum/String | `iceage.gon, dimensionx.gon, future.gon` |  |
| `clear_surviving_kaiju` | Enum/String | `pyrophina, zaratana` |  |
| `clone_self_to_party` | Number | `1` |  |
| `complete_item_quest` | Enum/String | `GuillotinasHead, ThrobbingGristle, PutridLeech` |  |
| `conditional_reward` | Block | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `copy_items_to_party` | Number | `1` |  |
| `copy_party_items` | Number | `1` |  |
| `cutscene_on_exit` | Enum/String | `king_intro` |  |
| `cutscene` | String | `"chapterintros/bunker", { ... }` | Event Node: Triggers a narrative cutscene. |
| `event_now_same_cat` | Enum/String | `random, BodyOfGlorg_Gift, MysteriousTomb1` |  |
| `event_now` | Enum/String | `StacyMutant2, StacyMutant3, StacyMutant4` |  |
| `full_heal` | Number | `1` |  |
| `gain_clone_familiar` | Block | `{ ... }` | Event Action: Adds a clone of a character to the party as a familiar. |
| `gain_disorder_from_pool` | Enum/String | `all_disorders` |  |
| `gain_disorder` | Enum/String | `Depression, Anxiety, Gargantuan` |  |
| `gain_food` | Array | `[ 10 20 ]` |  |
| `get_full_item_set_from_pool` | Enum/String | `common` |  |
| `get_item_from_pool` | Enum/String | `bloody_items, glitched_items, godly_items` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `get_item` | Enum/String | `MomsKnife, CryogenicTimeChamber_Full, HumanBrain` |  |
| `get_parasite` | Enum/String | `Beepis, Cunch, Feebis` |  |
| `global_effect_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal_disorder` | Number | `1, Anxiety, mental_disorders` |  |
| `heal_injury` | Number | `1, 5` |  |
| `heal` | Number | `50%` |  |
| `increment_legacy_counter` | Enum/String | `WorldEventLegacyCounter_Jack, WorldEventLegacyCounter_SealedCrypt, WorldEventLegacyCounter_TestLegacyFoo` |  |
| `injury` | Enum/String | `random` |  |
| `kill` | Enum/String | `cat` |  |
| `learn_ability_from_pool` | Enum/String | `Necromancer, [ Smack Meow Hiss ]` |  |
| `learn_passive_from_pool` | Array | `[ MiniMe SkillShare ], Necromancer` |  |
| `level_up` | Enum/String | `self, all` |  |
| `lose_item` | Enum/String | `parasite` |  |
| `lose_specific_item` | Enum/String | `PyrophinasCollar, ThrobbingGristle, PutridLeech` |  |
| `mutation` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Number | `1` |  |
| `next_event_from_set` | Block | `{ ... }` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSTOMB1_END", "EVENT_MYSTERIOUSTOMB_END"` |  |
| `party_gain_disorder_from_pool` | Array | `[ Dwarfism ], [ Gigantism ]` |  |
| `play_animation` | Enum/String | `resultVeryGood, [ resultLeave 0 ], resultHole` |  |
| `prompt` | String | `"EVENT_SEALEDCRYPT_LEAVE", "EVENT_TRASHBIN_REW1", "EVENT_CLOSEDWINDOW_REW8"` |  |
| `random_mutation` | Number | `1, 5, 10` | Event Reward: Applies a completely random mutation to a character. |
| `random_pool_consider_luck` | Array | `[ { prompt "EVENT_VENDINGMACHINE_REW4" set_frame 5 gain_d..., [ { prompt "EVENT_TRACY_REW1" weight 1 get_parasite_from_..., [ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo...` |  |
| `random_pool` | Array | `[ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { prompt "EVENT_TRAVERSETHENECROPOLIS_REW1" play_animat..., [ { weight 95 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran...` |  |
| `rare` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `reward` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `scramble_abilities` | Enum/String | `all` |  |
| `scramble_passives` | Enum/String | `all` |  |
| `set_adventure_token` | Enum/String | `StacyMutant_Thorns, StacyMutant_Holy, StacyMutant_Brace` |  |
| `set_frame` | Number | `2, 4, 3` |  |
| `set_legacy_token` | Enum/String | `mapflag_ThrobbingArteryDone, MeatWorldQuest_Leech, WorldEventLegacyToken_StacyMutant` |  |
| `shop_now` | Enum/String | `Event_SmallShop` |  |
| `transform_item` | Array | `[ JarOfRadiation JarOfRadiatedBlood ], [ JarOfRadiatedBlood JarOfChaos ], [ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ]` |  |
| `trigger_adventure_unlock` | Enum/String | `time_machine_quest_finalstep, legacy_event_unlock_momsknife, meat_world_open` |  |
| `trigger_butterfly_effect` | Number | `1` |  |
| `unlock_item_quest` | Enum/String | `CryogenicTimeChamber_Full, JarOfChaos, JarOfRadiatedBlood` |  |
| `upgrade_ability` | Enum/String | `random` |  |
| `upgrade_passive` | Enum/String | `random` |  |

### Context: `hack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_HACK_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `head`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GIFTOFGLORG_HEAD_ANSW"` |  |

### Context: `holy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW3"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `home`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `hint_chapter_exit` | Enum/String | `home` |  |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_HOME_ANSW` |  |
| `stat` | Enum/String | `none` |  |

### Context: `hp`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW1"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `ice`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW2"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `ignore`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `hint_chapter_exit` | Enum/String | `home` |  |
| `label` | String | `"EVENT_LEAVE_ANSW", "EVENT_IGNORE_ANSW", EVENT_IGNORE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `con, none` |  |

### Context: `infinite`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `hint_chapter_exit` | Enum/String | `endoftime` |  |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_THEEND_INFINITE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `inspect`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_INSPECT_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `intcheck`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `intimidation`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_INTIMIDATION_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `intro`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cat_choice` | Enum/String | `random` |  |
| `choose_cat_with_highest_stat` | Enum/String | `int` |  |
| `choose_cat_with_item_slot_equipped` | Enum/String | `weapon` |  |
| `choose_cat_with_item` | Enum/String | `GuillotinasHead, ThrobbingGristle, PutridLeech` |  |
| `choose_cat_with_min_health` | Number | `75%` |  |
| `choose_cat_with_most_injuries` | Boolean | `true` |  |
| `choose_cat_with_parasite` | Boolean | `true` |  |
| `different_from_last_x_cats` | Number | `1, 2, 3` |  |
| `event_clip` | Enum/String | `NonWheelEvent` |  |
| `set_frame` | Number | `1` |  |
| `subject_clip` | Enum/String | `EventSubject` |  |
| `subject_frame_inner` | Number | `2, 4` |  |
| `subject_frame` | Enum/String | `trashcan, mouse_nest, brokenwindow` |  |
| `title` | String | `"EVENT_TRASHBIN_NAME", "EVENT_MOUSENEST_NAME", "EVENT_CLOSEDWINDOW_NAME"` |  |

### Context: `investigate`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_INVESTIGATE_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `itchies`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `label` | String | `"EVENT_ITCHIES_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `join`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_JOININ_ANSW"` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `jump`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |  |
| `stat` | Enum/String | `spd` |  |

### Context: `jump_over`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `keep_going`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_KEEPGOING_ANSW"` |  |

### Context: `kiss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_KISS_ANSW"` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `kiss_meat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_LEAKINGMEAT_KISS_ANSW"` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `knife`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"Get a knife"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `leave`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_IGNORE_ANSW", "EVENT_WALKAWAY_ANSW", "EVENT_LEAVE_ANSW"` |  |
| `stat` | Enum/String | `lck, none, spd` |  |

### Context: `leave_it_in`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW2"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `leave_party_temporarily`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `fights_skipped` | Number | `1, 0` |  |
| `return_as` | Enum/String | `enemy` |  |
| `return_during` | Enum/String | `boss` |  |

### Context: `leg`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_LEGINSIDE_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `lever`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `fixed_chance` | Number | `50%` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_PULLLEVER_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `lick`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_GLOWINGORB_LICK_ANSW, "EVENT_GOLEMLICK_ANSW", "EVENT_LICK_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `cha, con, none` |  |

### Context: `lick_alt`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_LICK_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `con` |  |

### Context: `lightning`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW3"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `listen`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_LISTEN_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `looks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_LOOKS` |  |
| `stat` | Enum/String | `none` |  |

### Context: `loot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc, choice_dex_alt` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_DEADKING_LOOTCORPSE_ANSW, "EVENT_LOOT_ANSW", EVENT_LOOT_ANSW` |  |
| `rare` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `lck, dex` |  |

### Context: `loot_heart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_DEADKING_TAKEHEART_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `main`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `add_weather` | Enum/String | `MeteorShower` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `gain_familiar` | Enum/String | `Snake` | Event Action: Adds a specific familiar to the party. |
| `goto` | Enum/String | `end` |  |
| `leave` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Leave' action. |
| `max_options` | Number | `2, 3` |  |
| `next_event_from_set` | Enum/String | `Tragedy` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `options` | Block | `{ ... }` | Event Block: Lists the available clickable dialog choices for the current story node. |
| `outcome` | Block | `{ ... }` | Event Block: Logic and text executed after selecting a specific dialog option. |
| `party_heal` | Number | `3` |  |
| `party_permanent_stats` | Block | `{ ... }` | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| `play_animation` | Enum/String | `resultVeryGood` |  |
| `prompt` | String | `"EVENT_MOUSENEST_QUES", "EVENT_TRASHBIN_QUES", "EVENT_CLOSEDWINDOW_QUES"` |  |
| `rare` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `requires_flag` | Enum/String | `MeteorShowerUnlocked` | Prerequisite: Must meet this condition. |
| `self_damage` | Array | `[ 4 8 ]` | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_frame` | Number | `15, 16, 3` |  |
| `setup` | Block | `{ ... }` | Event Block: Pre-initialization logic executed before the event UI is drawn. |
| `shop_now` | Enum/String | `Event_RareShop` |  |
| `shuffle_options` | Boolean | `true` |  |
| `weight` | Enum/String | `.25, .5` | Probability weight for this outcome. |

### Context: `makeup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MAKEUP_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `mind`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_CURSEMIND` |  |
| `stat` | Enum/String | `none` |  |

### Context: `move_closer`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_ELEPHANTSFOOT_ANSW", "EVENT_ELEPHANTSFOOTCLOSER_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `mutation`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | `-2` |  |
| `arms` | Number | `900` |  |
| `body` | Number | `900` | Event Node: Story branch or dialog option representing the 'Body' action. |
| `ear1` | Number | `-2` |  |
| `ears` | Number | `-2, 328, 310` |  |
| `eye1` | Number | `-1, -2` |  |
| `eye2` | Number | `-1` |  |
| `eyebrow1` | Number | `-2` |  |
| `eyebrows` | Number | `440, -2, 900` |  |
| `eyes` | Number | `-2, 702, 900` |  |
| `head` | Number | `305, 900` | Event Node: Story branch or dialog option representing the 'Head' action. |
| `leg1` | Number | `-2` |  |
| `legs` | Number | `322, 900` |  |
| `mouth` | Number | `-2, 900, 705` |  |
| `tail` | Number | `900` | Event Node: Story branch or dialog option representing the 'Tail' action. |

### Context: `neck`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GIFTOFGLORG_NECK_ANSW"` |  |

### Context: `next_event_from_set`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `1, 4, 3` | Quantity. |
| `event` | Enum/String | `Tragedy, Death` |  |
| `same_cat` | Boolean | `true` |  |

### Context: `nothanks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_NOTHANKS_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `open`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `copy_results` | Enum/String | `smash` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_OPEN_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `options`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `5coins` | Block | `{ ... }` | Event Action: Grants or consumes 5 coins. |
| `a` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'A' action. |
| `activate_p` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Activate P' action. |
| `activate_z` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Activate Z' action. |
| `altar_sacrifice` | Block | `{ ... }` | Event Action: Triggers the altar sacrifice progression logic. |
| `arm` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Arm' action. |
| `attach_amplifier` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Attach Amplifier' action. |
| `attach_antenna` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Attach Antenna' action. |
| `attach_leech` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Attach Leech' action. |
| `attack` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Attack' action. |
| `b` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'B' action. |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `bash_past_alt` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bash Past Alt' action. |
| `bash` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bash' action. |
| `bite_it_off` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bite It Off' action. |
| `bite` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bite' action. |
| `blue_needle` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Blue Needle' action. |
| `blue` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Blue' action. |
| `body` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Body' action. |
| `boogers` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Boogers' action. |
| `book` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Book' action. |
| `brace` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Brace' action. |
| `break_ice` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Break Ice' action. |
| `break_lock` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Break Lock' action. |
| `bribe` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bribe' action. |
| `button` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Button' action. |
| `buy1` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Buy1' action. |
| `c` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'C' action. |
| `catch` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Catch' action. |
| `challenge_to_game` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Challenge To Game' action. |
| `chaos_ending` | Block | `{ ... }` | Event Node: Triggers the Chaos Boss victory sequence. |
| `chapter_cutscene` | Block | `{ ... }` | Event Node: Triggers an intermission cutscene. |
| `charm_past_alt` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Charm Past Alt' action. |
| `charm` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Charm' action. |
| `climb` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Climb' action. |
| `comfort` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Comfort' action. |
| `communicate` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Communicate' action. |
| `concheck` | Block | `{ ... }` | Event Node: Stat check branch evaluating the 'con' attribute. |
| `copy` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Copy' action. |
| `counter` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Counter' action. |
| `crack_open` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Crack Open' action. |
| `cross` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Cross' action. |
| `cut_wires` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Cut Wires' action. |
| `d` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'D' action. |
| `damage_1` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Damage 1' action. |
| `damage_full` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Damage Full' action. |
| `damage_half` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Damage Half' action. |
| `damage` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `desert_cutscene` | Block | `{ ... }` | Event Node: Triggers the desert transition cutscene. |
| `destroy` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Destroy' action. |
| `dexcheck` | Block | `{ ... }` | Event Node: Stat check branch evaluating the 'dex' attribute. |
| `dig` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Dig' action. |
| `disarm` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Disarm' action. |
| `dive` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Dive' action. |
| `donate_10` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Donate 10' action. |
| `donate_15` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Donate 15' action. |
| `donate_20` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Donate 20' action. |
| `donate_5` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Donate 5' action. |
| `donate` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Donate' action. |
| `double` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Double' action. |
| `drink` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Drink' action. |
| `eat_meat` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Eat Meat' action. |
| `eat` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Eat' action. |
| `enter_crater` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Enter Crater' action. |
| `enter` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Enter' action. |
| `examine` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Examine' action. |
| `face` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Face' action. |
| `fiddle` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Fiddle' action. |
| `fight` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Fight' action. |
| `fill_jar` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Fill Jar' action. |
| `find_another_way` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Find Another Way' action. |
| `find` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Find' action. |
| `fire` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Fire' action. |
| `flush_yourself` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Flush Yourself' action. |
| `follow` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Follow' action. |
| `free` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Free' action. |
| `future` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Future' action. |
| `gain_familiar` | Enum/String | `Squirrel` | Event Action: Adds a specific familiar to the party. |
| `get_item_from_pool` | Enum/String | `flesh_items, any_chapter` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `give_parasite` | Block | `{ ... }` | Event Action: Equips a parasite item to a character. |
| `go_around` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Go Around' action. |
| `hack` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Hack' action. |
| `head` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Head' action. |
| `holy` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Holy' action. |
| `home` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Home' action. |
| `hp` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Hp' action. |
| `ice` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Ice' action. |
| `ignore` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Ignore' action. |
| `infinite` | Block | `{ ... }` | Event Node: A looping or endlessly repeating story branch. |
| `inspect` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Inspect' action. |
| `intcheck` | Block | `{ ... }` | Event Node: Stat check branch evaluating the 'int' attribute. |
| `intimidation` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Intimidation' action. |
| `investigate` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Investigate' action. |
| `itchies` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Itchies' action. |
| `join` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Join' action. |
| `jump_over` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Jump Over' action. |
| `jump` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Jump' action. |
| `keep_going` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Keep Going' action. |
| `kiss_meat` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Kiss Meat' action. |
| `kiss` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Kiss' action. |
| `knife` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Knife' action. |
| `leave_it_in` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Leave It In' action. |
| `leave` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Leave' action. |
| `leg` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Leg' action. |
| `lever` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Lever' action. |
| `lick_alt` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Lick Alt' action. |
| `lick` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Lick' action. |
| `lightning` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Lightning' action. |
| `listen` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Listen' action. |
| `looks` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Looks' action. |
| `loot_heart` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Loot Heart' action. |
| `loot` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Loot' action. |
| `makeup` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Makeup' action. |
| `mind` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Mind' action. |
| `move_closer` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Move Closer' action. |
| `neck` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Neck' action. |
| `nothanks` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Nothanks' action. |
| `open` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Open' action. |
| `outsmart` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Outsmart' action. |
| `past` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Past' action. |
| `patch_up` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Patch Up' action. |
| `pick_lock` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Pick Lock' action. |
| `pilfer` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Pilfer' action. |
| `pirouette` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Pirouette' action. |
| `place_gristle` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Place Gristle' action. |
| `play_animation` | Enum/String | `resultGood` |  |
| `play` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Play' action. |
| `poop` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Poop' action. |
| `power` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Power' action. |
| `print` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Print' action. |
| `prompt` | String | `"EVENT_TRACY_REW5", "EVENT_TRAVERSETHENECROPOLIS_REW6"` |  |
| `protection` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Protection' action. |
| `pull_it_out` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Pull It Out' action. |
| `pull_lever` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Pull Lever' action. |
| `pull` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Pull' action. |
| `purify` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Purify' action. |
| `push_buttons` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Push Buttons' action. |
| `push_through` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Push Through' action. |
| `put_in_coins` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Put In Coins' action. |
| `put_out_of_misery` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Put Out Of Misery' action. |
| `rare` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `reach_inside` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reach Inside' action. |
| `read` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Read' action. |
| `receive` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Receive' action. |
| `red_needle` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Red Needle' action. |
| `red` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Red' action. |
| `reflect` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reflect' action. |
| `remove_the_nail` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Remove The Nail' action. |
| `remove` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Remove' action. |
| `repair_quest` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Repair Quest' action. |
| `repair` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Repair' action. |
| `repell` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Repell' action. |
| `rest` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rest' action. |
| `revive` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Revive' action. |
| `rub` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rub' action. |
| `run_again` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Run Again' action. |
| `run_away` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Run Away' action. |
| `run` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Run' action. |
| `sacrifice_full_favor` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sacrifice Full Favor' action. |
| `sacrifice_normal` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sacrifice Normal' action. |
| `sacrifice_partial_favor` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sacrifice Partial Favor' action. |
| `sacrifice_quest` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sacrifice Quest' action. |
| `sacrifice` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sacrifice' action. |
| `scale` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Scale' action. |
| `scream` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Scream' action. |
| `shake` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Shake' action. |
| `skip` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Skip' action. |
| `slip_through` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Slip Through' action. |
| `smash` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Smash' action. |
| `sneak_by` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sneak By' action. |
| `sneak_past_alt` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sneak Past Alt' action. |
| `sneak` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sneak' action. |
| `soul` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Soul' action. |
| `speed` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Speed' action. |
| `surprise` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Surprise' action. |
| `sweet_talk` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Sweet Talk' action. |
| `swim` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Swim' action. |
| `tail` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Tail' action. |
| `take_blood` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Take Blood' action. |
| `take` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Take' action. |
| `talk_to` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Talk To' action. |
| `talk` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Talk' action. |
| `tappytoes` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Tappytoes' action. |
| `teleport` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Teleport' action. |
| `thorns` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Thorns' action. |
| `throw` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Throw' action. |
| `timemachine` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Timemachine' action. |
| `touch` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Touch' action. |
| `traverse` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Traverse' action. |
| `turnon` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Turnon' action. |
| `upgrade_yourself` | Block | `{ ... }` | Event Reward: Upgrades an existing ability or item. |
| `use_item` | Block | `{ ... }` | Event Requirement: Requires the player to consume a specific item to proceed. |
| `use_toilet_con` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Use Toilet Con' action. |
| `use_toilet_str` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Use Toilet Str' action. |
| `use_weapon` | Block | `{ ... }` | Event Requirement: Uses the properties of the equipped weapon to resolve an outcome. |
| `w1` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'W1' action. |
| `w2` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'W2' action. |
| `w3` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'W3' action. |
| `w4` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'W4' action. |
| `w5` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'W5' action. |
| `w6` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'W6' action. |
| `wealth` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Wealth' action. |
| `weight` | Enum/String | `.5` | Probability weight for this outcome. |
| `wheezies` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Wheezies' action. |
| `wish_genes` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Wish Genes' action. |
| `wish_items` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Wish Items' action. |
| `wish_levelups` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Wish Levelups' action. |
| `wish_strength` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Wish Strength' action. |
| `withstand` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Withstand' action. |
| `yank_it_out` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Yank It Out' action. |
| `yellow_needle` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Yellow Needle' action. |

### Context: `outcome`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `add_weather` | Enum/String | `Birdemic` |  |
| `play_animation` | Array | `[ resultBlessing .5 ], [ resultTragedy .5 ], [ resultWeather .5 ]` |  |
| `random_pool` | Array | `[ { set_frame 12 prompt "EVENT_ACAT_REW1" gain_cat_famili..., [ { set_frame 1 prompt "EVENT_BLESSING_REW1" heal 5 } { s..., [ { set_frame 1 prompt "EVENT_TRAGEDY_REW1" } { set_frame...` |  |
| `weather_roll` | Array | `[ { weight 1 set_frame 2 prompt "EVENT_HAPPENING_FOG_REW"...` |  |

### Context: `outsmart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BUTCHTUTORIAL_OUTSMART_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `party_permanent_stats`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `1` |  |

### Context: `party_permanent_stats_exclude_self`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `1, 2` |  |
| `con` | Number | `1, 2` |  |
| `dex` | Number | `1, 2` |  |
| `int` | Number | `1, 2` |  |
| `lck` | Number | `1, 2` |  |
| `spd` | Number | `1, 2` |  |
| `str` | Number | `1, 2` |  |

### Context: `party_random_mutation_from_set`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `1` | Quantity. |
| `ears` | Number | `-2` |  |
| `eyebrows` | Number | `-2` |  |
| `eyes` | Number | `-2` |  |
| `mouth` | Number | `-2` |  |

### Context: `party_status_next_fight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AbilityOnBattleStart_Immediate` | Enum/String | `RocksFallEvent, SummonBrambles2, GrassEvent` | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| `Bleed` | Number | `3` | Applies or references the 'Bleed' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `HealthRegenUp` | Number | `2` | Applies or references the 'HealthRegenUp' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `NoHealthRegen` | Number | `1` | Applies or references the 'NoHealthRegen' effect/state. |
| `Poison` | Number | `1, 2, 3` | Applies or references the 'Poison' effect/state. |
| `Tangled` | Number | `2` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `Webbed` | Number | `1` | Applies or references the 'Webbed' effect/state. |

### Context: `past`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `hint_chapter_exit` | Enum/String | `iceage, endoftime, jurassic` |  |
| `label` | Enum/String | `QEVENT_TIMEMACHINE_ICEAGE_PAST_ANSW, QEVENT_TIMEMACHINE_PAST_ANSW, QEVENT_TIMEMACHINE_JURASSIC_INFINITE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `patch_up`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_PATCHUP_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `permanent_stats`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Enum/String | `+1, 1, -1` |  |
| `con` | Number | `1, 2, -1` |  |
| `dex` | Number | `1, 2, -1` |  |
| `int` | Number | `-4, 1, -1` |  |
| `lck` | Number | `1, -1, -2` |  |
| `random` | Number | `1, 2, -1` |  |
| `spd` | Number | `1, -1, -2` |  |
| `str` | Number | `1, 2, -1` |  |

### Context: `pick_lock`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_LOCKEDCRATE_PICK_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `pilfer`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_PILFER_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `pirouette`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_PIROUETTE_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `place_gristle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_WALLOFFLESH_PLACE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `play`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSSTRANGER_ANSW"` |  |
| `stat` | Enum/String | `spd` |  |

### Context: `poop`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_FEEBIS_ANSW", "EVENT_POOP_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `power`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_POWER` |  |
| `stat` | Enum/String | `none` |  |

### Context: `print`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_PRINT_ANSW"` |  |

### Context: `protection`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_PROTECTION_ANSW", "EVENT_CUTS_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `pull`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_PULLKNIFE_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `pull_it_out`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW1"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `pull_lever`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_ODDDEVICE_PULLLEVER_ANSW"` |  |

### Context: `purify`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_PURIFY_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `push_buttons`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_ODDDEVICE_PUSHBUTTONS_ANSW"` |  |

### Context: `push_through`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_PUSH"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `put_in_coins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation_fail` | Enum/String | `choice_no_coins` |  |
| `animation` | Enum/String | `choice_coins_ten` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_VENDINGMACHINE_COINS_ANSW"` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |
| `stat` | Enum/String | `coins` |  |

### Context: `put_out_of_misery`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_PUTOUTOFMISERY_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `random_chance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | Probability weight for this outcome. |
| `get_item_from_pool` | Enum/String | `chapter` | Event Action: Rewards the player with an item drawn from a specific loot pool. |

### Context: `random_mutation`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `asymmetric` | Boolean | `false, true` |  |
| `count` | Number | `1, 2, 15` | Quantity. |
| `tag` | Enum/String | `animal, birth_defect, melted` | Specific entity tag required. |

### Context: `random_mutation_from_set`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | `-1, -2` |  |
| `arm2` | Number | `-1, -2` |  |
| `body` | Number | `758, -1` | Event Node: Story branch or dialog option representing the 'Body' action. |
| `count` | Number | `1, 3` | Quantity. |
| `ears` | Number | `-1, 1500, -2` |  |
| `eyebrows` | Number | `-1, -2` |  |
| `eyes` | Number | `-1, -2, 1029` |  |
| `head` | Number | `-1, 759` | Event Node: Story branch or dialog option representing the 'Head' action. |
| `leg1` | Number | `-1` |  |
| `leg2` | Number | `-1` |  |
| `legs` | Number | `-1, 306` |  |
| `mouth` | Number | `1026, -1, 1500` |  |
| `tail` | Number | `-1, 1500, 760` | Event Node: Story branch or dialog option representing the 'Tail' action. |
| `texture` | Number | `-1` |  |

### Context: `rare`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `add_weather` | Enum/String | `RestlessDead, HauntedNight` |  |
| `ally_ambush_next_fights` | Number | `1, 2` |  |
| `ambush_next_basic_fights` | Number | `1` |  |
| `ambush` | String | `"events/chupacabra.lvl"` |  |
| `battle` | String | `"events/crackinthewall.lvl", "events/bigtoe.lvl", "events/chupacabra.lvl"` |  |
| `clear_result_animation` | Number | `1` |  |
| `conditional_reward` | Block | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `damage` | Number | `6, 99%, 10` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `decrement_legacy_counter` | Enum/String | `WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyToken_StartDigging` |  |
| `event_now_same_cat` | Enum/String | `BigToe, SpookieApparation, CatHole` |  |
| `event_now` | Enum/String | `MysteriousMachine_Bad, MysteriousMachine_Good` |  |
| `full_heal` | Number | `1` |  |
| `gain_cat_familiar` | Number | `1` |  |
| `gain_coins` | Array | `[ 10 30 ], [ 10 15 ], [ 20 100 ]` |  |
| `gain_disorder_from_pool` | Enum/String | `diseases, all_disorders, physical_disorders` |  |
| `gain_disorder` | Enum/String | `Dyslexia, Brave, BorrowedTime` |  |
| `gain_familiar` | Enum/String | `CharmedFetus2, CharmedHeadTumor, CharmedLeaper` | Event Action: Adds a specific familiar to the party. |
| `gain_food` | Array | `[ 1 5 ], [ 2 5 ], [ 8 10 ]` |  |
| `gain_immortal_familiar` | Enum/String | `CharmedFleaSpecial` |  |
| `get_and_equip_item` | Enum/String | `FlyLarva` |  |
| `get_item_from_pool` | Enum/String | `treasure_easy, bone_equipment, { ... }` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `get_item` | Enum/String | `BigToe, MomsKnife, MomsToeNail` |  |
| `get_parasite_from_pool` | Enum/String | `parasites, sludge_armor, good_parasites` |  |
| `get_parasite` | Enum/String | `FaceShards, MetalRod, BigToeCursed` |  |
| `global_effect_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal_disorder` | Number | `2` |  |
| `hide_appearance_changes` | Number | `1` |  |
| `increment_legacy_counter` | Enum/String | `WorldEventLegacyCounter_ToiletFlushes, WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyToken_StartDigging` |  |
| `injury` | Enum/String | `radiated, cursed, str` |  |
| `kill` | Enum/String | `cat` |  |
| `learn_ability_from_pool` | Enum/String | `Necromancer` |  |
| `learn_ability` | Enum/String | `BarfBall, FutureSight` |  |
| `learn_passive_from_pool` | Enum/String | `AnyUnlocked` |  |
| `learn_passive` | Enum/String | `DeathProof, PoisonTips, CobraStyle` |  |
| `leave_party_temporarily` | Block | `{ ... }` | Event Action: Removes a character from the active team until the next hub area. |
| `level_up` | Enum/String | `self` |  |
| `lose_all_equipped_items` | Enum/String | `cat` |  |
| `lose_item_from_inventory` | Enum/String | `cat` |  |
| `lose_item` | Enum/String | `inventory, equipped` |  |
| `lose_specific_item` | Enum/String | `SlagTight` |  |
| `make_old` | Enum/String | `self` |  |
| `mutation` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `next_event_bonus` | Number | `1, -1, -2` |  |
| `next_event_from_set` | Enum/String | `WatchingHead2, { ... }` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_MYSTERIOUSTENT_PROMPT", "EVENT_LOCKEDDOOR_PROMPT2"` |  |
| `party_damage` | Number | `2, 5, [ 5 10 ]` |  |
| `party_heal_disorder` | Number | `2` |  |
| `party_heal_injury` | Number | `99` |  |
| `party_heal` | Number | `6, 5, 100%` |  |
| `party_injury` | Enum/String | `random` |  |
| `party_permanent_stats_exclude_self` | Block | `{ ... }` | Event Reward: Permanently modifies stats for all party members except the one who initiated the action. |
| `party_permanent_stats` | Block | `{ ... }` | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| `party_random_mutation_from_set` | Block | `{ ... }` | Event Reward: Applies a random mutation to the entire party from a specific pool. |
| `party_random_mutation` | Number | `1` |  |
| `party_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. |
| `permanent_stats` | Block | `{ ... }` | Event Reward: Permanently increases (or decreases) the core stats of a single character. |
| `play_animation` | Array | `[ resultLeave 0 ], resultHole` |  |
| `play_result_animation` | Enum/String | `resultVeryGood` |  |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW2", "EVENT_CLOSEDWINDOW_REW6", "EVENT_CLOSEDWINDOW_REW4"` |  |
| `random_mutation_from_set` | Block | `{ ... }` | Event Reward: Applies a random mutation to a character from a specific pool. |
| `random_mutation` | Number | `1, 2, { ... }` | Event Reward: Applies a completely random mutation to a character. |
| `random_pool` | Array | `[ { party_heal 100% gain_food [ 10 25 ], [ { event_now_same_cat Crate } { event_now_same_cat Safe ..., [ { permanent_stats { str -1 } } { permanent_stats { dex ...` |  |
| `scramble_abilities` | Enum/String | `all` |  |
| `scramble_basic_attack` | Enum/String | `all` |  |
| `self_damage` | Number | `1, 99%, 50%` | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_status_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `set_adventure_token` | Enum/String | `MysteriousStranger_HasLostFinger, AdventureToken_TrippedOnBigToe, HasPlayedMysteriousStranger` |  |
| `set_age` | Number | `1` |  |
| `set_frame` | Number | `6, 4, 3` |  |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_HeadInTireCompleted, WorldEventLegacyToken_MomsKnife, WorldEventLegacyToken_MonkeyPaw1` |  |
| `shop_now` | Enum/String | `Event_RareShop, Event_SmallShop, TreasureHard` |  |
| `spawn_reflection_next_fight` | Number | `1, { ... }` | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. |
| `spawn_unit_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| `trigger_adventure_unlock` | Enum/String | `legacy_event_unlock_momsknife` |  |
| `upgrade_ability` | Enum/String | `random` |  |
| `upgrade_passive` | Enum/String | `random` |  |

### Context: `reach_inside`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SMALLBLACKHOLE_REACHINSIDE_ANSW"` |  |
| `stat` | Enum/String | `spd` |  |

### Context: `read`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_READ_ANSW"` |  |
| `stat` | Enum/String | `int` |  |

### Context: `receive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"Receive"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `red`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `fixed_chance` | Number | `50%` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_RED_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `red_needle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_NEEDLES_RED_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `lck` |  |

### Context: `reflect`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW3"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `remove`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_REMOVE_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `remove_the_nail`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BIGTOE_NAIL_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `repair`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_REPAIR_ANSW, "EVENT_REPAIR_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `lck, none` |  |

### Context: `repair_quest`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_REPAIR_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `repell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSCAVE3_CLIMB_ANSW", "EVENT_MYSTERIOUSCAVE1_RAPPEL_ANSW", "EVENT_MYSTERIOUSCAVE1_TALKTO_ANSW"` |  |
| `stat` | Enum/String | `cha, dex, str` |  |

### Context: `requirements`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cat_has_injury_count_min` | Number | `2` |  |
| `cat_has_item_equipped` | Enum/String | `GuillotinasHead, ThrobbingGristle, PutridLeech` |  |
| `cat_has_item_slot_equipped` | Enum/String | `weapon` |  |
| `cat_has_parasite` | Boolean | `true` |  |
| `counter_maximum` | Array | `[ WorldEventLegacyCounter_CrackInTheWall 3 ], [ WorldEventLegacyCounter_CrackInTheWall 0 ], [ WorldEventLegacyCounter_SealedCrypt 4 ]` |  |
| `counter_minimum` | Array | `[ WorldEventLegacyToken_StartDigging 4 ], [ WorldEventLegacyCounter_CrackInTheWall 4 ], [ WorldEventLegacyCounter_TestLegacyFoo 3 ]` |  |
| `counter_range` | Array | `[ WorldEventLegacyCounter_SealedCrypt 1 1 ], [ WorldEventLegacyCounter_SealedCrypt 0 0 ], [ WorldEventLegacyCounter_SealedCrypt 2 2 ]` |  |
| `has_token` | Enum/String | `AdventureToken_TrippedOnBigToe, HasPlayedMysteriousStranger, WorldEventLegacyToken_StacyMutant` |  |
| `is_chapter` | Array | `[ future theend ], [ future ], [ theend ]` |  |
| `is_not_chapter` | Array | `[ jurassic iceage ], [ future theend ], [ iceage jurassic ]` |  |
| `minimum_party_size` | Number | `2` |  |
| `not_cat_has_item_equipped` | Enum/String | `GuillotinasHead, CryogenicTimeChamber_Full` |  |
| `not_has_token` | Enum/String | `WorldEventLegacyToken_MomsKnife, AdventureToken_UnmarkedGraveForced, WorldEventLegacyToken_CryptOpened` |  |
| `not_on_quest` | Number | `1` |  |

### Context: `rest`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_REST_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `revive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_REVIVE_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `reward`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `clear_adventure_token` | Enum/String | `AdventureToken_BlueNeedle, AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle` |  |
| `common` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Common' action. |
| `cutscene_on_exit` | Enum/String | `infinite_intro` |  |
| `event_now` | Enum/String | `MeatGolem` |  |
| `gain_coins` | Array | `[ 4 15 ]` |  |
| `gain_disorder_from_pool` | Enum/String | `diseases, Steven_disorders` |  |
| `get_item_from_pool` | Enum/String | `consumables, food, { ... }` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `get_item` | Enum/String | `BrokenWindow` |  |
| `get_parasite_from_pool` | Enum/String | `parasites` |  |
| `injury` | Enum/String | `random, con` |  |
| `next_event_bonus` | Number | `1, -1, -2` |  |
| `party_damage` | Array | `[ 5 10 ]` |  |
| `play_animation` | Enum/String | `resultVeryGood, resultBad` |  |
| `prompt` | String | `"EVENT_SEALEDCRYPT_QUES2", "EVENT_TRASHBIN_REW2", "EVENT_SEALEDCRYPT_QUES1"` |  |
| `random_chance` | Block | `{ ... }` | Event Logic: Executes the nested outcome based on a percentage roll. |
| `random_pool` | Array | `[ { get_item_from_pool uncommon get_item_from_pool uncomm..., [ { get_item_from_pool rare get_item_from_pool rare } { g..., [ { weight 10 gain_disorder_from_pool diseases } { weight...` |  |
| `rare` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `set_adventure_token` | Enum/String | `AdventureToken_Mirage2, HasPlayedMysteriousStranger, AdventureToken_StevenTryAgain3` |  |
| `set_frame` | Number | `1, 2, 3` |  |
| `set_legacy_token` | Enum/String | `WorldEventLegacyToken_CryptOpened` |  |
| `set_subject` | Enum/String | `wall_of_flesh_noartery, dimensionx_head2, throbbing_artery_noflesh` |  |
| `spawn_unit_next_fight` | Block | `{ ... }` | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| `trigger_adventure_unlock` | Enum/String | `end_of_time_unlock, meat_world_unlock` |  |
| `weight` | Number | `3` | Probability weight for this outcome. |

### Context: `rub`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_RUB_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `run`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_RUN_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `spd` |  |

### Context: `run_again`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_leave` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_RUN_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `spd` |  |

### Context: `run_away`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_RUNAWAY_ANSW"` |  |
| `stat` | Enum/String | `spd` |  |

### Context: `sacrifice`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW", "EVENT_BAHPHOMET_SACRIFICE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `sacrifice_full_favor`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `sacrifice_normal`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `lck` |  |

### Context: `sacrifice_partial_favor`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `sacrifice_quest`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `scale`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_SCALE_ANSW"` |  |

### Context: `scream`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GOLEMSCREAM_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `self_status_next_fight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AbilityOnBattleStart_Immediate` | Enum/String | `FlowerEventSleep, BrambleRandomTileEvent, SummonBrambles2` | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| `AbilityOnBattleStart` | Enum/String | `Flush` | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AddInitiative` | Number | `-99` | Applies or references the 'AddInitiative' effect/state. |
| `AddStartingMana` | Number | `5` | Applies or references the 'AddStartingMana' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `AlphaTurns` | Number | `1` | Applies or references the 'AlphaTurns' effect/state. |
| `Bleed` | Number | `1, 2, 3` | Applies or references the 'Bleed' effect/state. |
| `Blind` | Number | `6, 4` | Applies or references the 'Blind' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Burn` | Number | `6, 5, 4` | Applies or references the 'Burn' effect/state. |
| `ChangeTileUnderCharacterAtStart` | Enum/String | `GlassTile` | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. |
| `CharismaUp` | Number | `2, -1, -2` | Applies or references the 'CharismaUp' effect/state. |
| `Confusion` | Number | `2, 4` | Applies or references the 'Confusion' effect/state. |
| `ConstitutionUp` | Number | `1, -1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DexterityUp` | Number | `2, -1` | Applies or references the 'DexterityUp' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `Fear` | Number | `5, 1, 2` | Applies or references the 'Fear' effect/state. |
| `Fights` | Number | `99` | Applies or references the 'Fights' effect/state. |
| `HealthRegenUp` | Number | `1, 2` | Applies or references the 'HealthRegenUp' effect/state. |
| `IntelligenceUp` | Number | `-3, 3` | Applies or references the 'IntelligenceUp' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MissChance` | Number | `10` | Applies or references the 'MissChance' effect/state. |
| `NoHealthRegen` | Number | `1` | Applies or references the 'NoHealthRegen' effect/state. |
| `NoManaRegen` | Number | `1` | Applies or references the 'NoManaRegen' effect/state. |
| `PermanentConfusion` | Number | `1` | Applies or references the 'PermanentConfusion' effect/state. |
| `Poison` | Number | `2, 10, 3` | Applies or references the 'Poison' effect/state. |
| `ProbeCharmed` | Number | `1` | Applies or references the 'ProbeCharmed' effect/state. |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `Rot` | Number | `2` | Applies or references the 'Rot' effect/state. |
| `Sleep` | Number | `1, 2` | Applies or references the 'Sleep' effect/state. |
| `Slow` | Number | `3` | Applies or references the 'Slow' effect/state. |
| `SpeedUp` | Number | `-4, 2, -2` | Applies or references the 'SpeedUp' effect/state. |
| `SpiderInfested` | Number | `1` | Applies or references the 'SpiderInfested' effect/state. |
| `StrengthUp` | Number | `2, -1, -2` | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `TempStrengthUp` | Number | `1` | Applies or references the 'TempStrengthUp' effect/state. |
| `Webbed` | Number | `1, 2` | Applies or references the 'Webbed' effect/state. |

### Context: `setup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `conditional_reward` | Block | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `set_frame` | Number | `4` |  |

### Context: `shake`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_VENDINGMACHINE_SHAKE_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `skip`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW4", "QEVENT_STACYMUTANT3_ANSW4", "QEVENT_STACYMUTANT1_ANSW4"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `slip_through`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SLIPTHROUGH_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `smash`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `copy_results` | Enum/String | `open` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SMASH_ANSW", "EVENT_MYSTERIOUSTOMB_ANSW", "EVENT_GOLEMSMASH_ANSW"` |  |
| `stat` | Enum/String | `none, dex, str` |  |

### Context: `sneak`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SNEAKBY_ANSW", EVENT_SNEAKBY_ANSW, EVENT_RUN_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `dex, spd` |  |

### Context: `sneak_by`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |  |
| `stat` | Enum/String | `dex` |  |

### Context: `sneak_past_alt`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `dex` |  |

### Context: `soul`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_CURSESOUL` |  |
| `stat` | Enum/String | `none` |  |

### Context: `spawn_reflection_next_fight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `mutation` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Mutation' action. |

### Context: `spawn_unit_next_fight`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `8, [ 3 6 ], 3` | Quantity. |
| `object` | Enum/String | `DeadPinky, [ Junk Junk TrashBag ], RandomNonCoinPickup` |  |
| `side` | Enum/String | `enemies` |  |
| `spawn_side` | Enum/String | `cats, anywhere, enemies` |  |

### Context: `speed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW3"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `surprise`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SURPRISE_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `sweet_talk`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_DEATH_SWEETTALK_ANSW"` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `swim`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_SWIM_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `tail`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_TAILINSIDE_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `take`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_dex_alt` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_GOAROUND_ANSW", "EVENT_TAKE_ANSW"` |  |
| `stat` | Enum/String | `lck, con, spd` |  |

### Context: `take_blood`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_DEADKING_DRAINBLOOD_ANSW` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `quest` |  |

### Context: `talk`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_TALKTO_ANSW` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `talk_to`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_TALKTO_ANSW"` |  |
| `stat` | Enum/String | `cha` |  |

### Context: `tappytoes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_TAPPYTOES_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `teleport`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_TELEPORT_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `thorns`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW1"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `throw`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_HOLEINTHEEARTH_THROW_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `timemachine`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"Go to The Past"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `touch`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `QEVENT_OBELISK_MOON_TOUCH_ANSW, "EVENT_MYSTERIOUSOBELISK_TOUCH_ANSW", QEVENT_OBELISK_CORE_TOUCH_ANSW` |  |
| `stat` | Enum/String | `cha, none, lck` |  |

### Context: `traverse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_TRAVERSETHENECROPOLIS_ANSW"` |  |
| `play_animation` | Enum/String | `resultGood` |  |
| `prompt` | String | `"EVENT_TRAVERSETHENECROPOLIS_REW5"` |  |
| `shop_now` | Enum/String | `TreasureHard` |  |

### Context: `turnon`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_TURNONTV_ANSW", "EVENT_MYSTERIOUSMACHINE_TURNITON_ANSW"` |  |
| `stat` | Enum/String | `lck, int` |  |

### Context: `upgrade_yourself`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_UPGRADE_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `use_item`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_USE_ITEM_ANSW"` |  |
| `stat` | Enum/String | `lck` |  |

### Context: `use_toilet_con`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_USETOILET_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `use_toilet_str`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_USETOILET_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `use_weapon`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_USE_WEAPON_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |

### Context: `w1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW1"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `w2`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW2"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `w3`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW3"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `w4`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW4"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `w5`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW5"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `w6`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW6"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `wealth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | Enum/String | `EVENT_GENIE_CHOICE_WEALTH` |  |
| `stat` | Enum/String | `none` |  |

### Context: `wheezies`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | Enum/String | `choice_misc` |  |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `label` | String | `"EVENT_WHEEZIES_ANSW"` |  |
| `stat` | Enum/String | `none` |  |

### Context: `wish_genes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MONKEYPAW_WISH2"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `wish_items`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MONKEYPAW_WISH3"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `wish_levelups`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MONKEYPAW_WISH4"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `wish_strength`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_MONKEYPAW_WISH1"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `none` |  |

### Context: `withstand`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_ELEPHANTSFOOTEVENCLOSER_ANSW"` |  |
| `stat` | Enum/String | `con` |  |

### Context: `yank_it_out`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_BIGTOE_YANK_ANSW"` |  |
| `stat` | Enum/String | `str` |  |

### Context: `yellow_needle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `good` | Block | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `label` | String | `"EVENT_NEEDLES_YELLOW_ANSW"` |  |
| `requirements` | Block | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `stat` | Enum/String | `lck` |  |

---

## Furniture & Metaprogression

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | `1, 5, 2` | Applies or references the 'Appeal' effect/state. |
| `BreedSuppression` | Number | `1` | Applies or references the 'BreedSuppression' effect/state. |
| `Comfort` | Number | `5, -2, -5` | Applies or references the 'Comfort' effect/state. |
| `Evolution` | Number | `1, 5, 2` | Applies or references the 'Evolution' effect/state. |
| `FightBonusRewards` | Number | `1` | Applies or references the 'FightBonusRewards' effect/state. |
| `FightRisk` | Number | `2` | Applies or references the 'FightRisk' effect/state. |
| `FoodStorage` | Number | `40` | Applies or references the 'FoodStorage' effect/state. |
| `Health` | Number | `5, -1, -2` | Applies or references the 'Health' effect/state. |
| `Stimulation` | Number | `1, 5, 2` | Applies or references the 'Stimulation' effect/state. |
| `can_be_rare` | Boolean | `false` |  |
| `desc` | Enum/String | `FURNITURE_DESC_AUTOFEEDER, FURNITURE_DESC_SPECIAL_FOODBOX, FURNITURE_DESC_POOP` |  |
| `name` | Enum/String | `FURNITURE_NAME_SPECIAL_FOODBOX, FURNITURE_NAME_AUTOFEEDER, FURNITURE_NAME_POOP` |  |
| `removed` | Boolean | `true` |  |
| `set` | Enum/String | `sewn, spider, junk` |  |
| `special` | Boolean | `true` |  |

---

## Items & Equipment

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Set` | Enum/String | `Monk` | Applies or references the 'Set' effect/state. |
| `ability` | Enum/String | `wp_PartyDetonator, wp_PersuasionDevice, wp_PartyDetonatorFixed` | ID of the ability to trigger or reference. |
| `attack` | Enum/String | `BasicSpin, BasicTankMelee, IsaacBasicAttack` |  |
| `aux_is_catid` | Boolean | `true` |  |
| `aux` | Number | `12, 24, 10` |  |
| `cant_equip_to_colorless` | Boolean | `true` |  |
| `cha` | Number | `1, 2, -1` |  |
| `con` | Number | `1, 2, 3` |  |
| `consumable` | Boolean | `true` |  |
| `cursed` | Boolean | `true` |  |
| `degrade_after_adventure` | Boolean | `false` |  |
| `desc` | String | `"ARMOR_SCRAPMETALARMOR_DESC", "ARMOR_SCRAPMETALMASK_DESC", "ARMOR_SCRAPMETALHAT_DESC"` | Localization key for the item's desc. |
| `dex` | Number | `1, -1, 3` |  |
| `divine_shield` | Number | `1, 2, 3` |  |
| `dont_destroy_on_0` | Boolean | `true` |  |
| `durability` | Number | `1, 2, 3` | Maximum uses before breaking. |
| `equip_sound` | Enum/String | `SE_CatWeaponPoke_Chainsaw` |  |
| `failable` | Boolean | `true` |  |
| `force_sticky` | Boolean | `true` |  |
| `fragile` | Boolean | `true` |  |
| `frame` | Number | `12, 2, 23` |  |
| `global_passives` | Block | `{ ... }` |  |
| `global_tags` | Array | `[ all_cats_are_jester ], [ fail_all_events ], [ always_ambushed ]` |  |
| `hint_destination` | Enum/String | `meatworld, boneyard, caves` |  |
| `hint_prerequisite_flag` | Enum/String | `mapflag_BothObelisksUnlocked, mapflag_MeatWorldUnlockedFull, mapflag_MeatWorldUnlocked` |  |
| `icon_hint` | Enum/String | `passive_syringe, ability_syringe` |  |
| `indestructible` | Boolean | `true` |  |
| `int` | Number | `1, -1, 7` |  |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear when hovering over the ability. |
| `kind` | Enum/String | `head, face, neck` |  |
| `lck` | Number | `1, 2, -3` |  |
| `legacy_quest` | Boolean | `true` |  |
| `max_durability` | Number | `2, 3, 9` |  |
| `max_health` | Number | `-1` |  |
| `name` | String | `"ARMOR_SCRAPMETALHAT_NAME", "ARMOR_SCRAPMETALMASK_NAME", "ARMOR_SCRAPMETALARMOR_NAME"` | Localization key for the item's name. |
| `on_store` | Enum/String | `become_aux_coins, become_furniture, become_rare_furniture` |  |
| `parasite` | Boolean | `true` |  |
| `passive` | Block | `{ ... }` |  |
| `passives` | Block | `{ ... }` | Passives granted by equipping this. |
| `prevent_level_up` | Boolean | `true` |  |
| `quest_item_alias` | Enum/String | `NuclearKnife, BlackShard` |  |
| `quest_item` | Boolean | `false, true` |  |
| `quest_reward_item` | Enum/String | `PersuasionDevice_Fixed, MagicMirror_Fixed, ChaosDevice_Fixed` |  |
| `randomize_piece_frames` | Boolean | `true` |  |
| `rarity` | Enum/String | `rare, common, uncommon` |  |
| `reset_aux_on_store` | Number | `1` |  |
| `reset_str_aux_on_store` | Enum/String | `ModelingClay_Default` |  |
| `set` | Enum/String | `Rag, Leather, Scrap` |  |
| `shield` | Number | `1, 2, 4` |  |
| `spd` | Number | `-4, -1, 3` |  |
| `speed` | Number | `1` |  |
| `sticky` | Boolean | `true` |  |
| `str_aux_initialize` | Enum/String | `random_stat, random_class_passive, random_seed` |  |
| `str_aux_is_copy_ability` | Block | `{ ... }` |  |
| `str_aux_is_copy_item_active` | Boolean | `true` |  |
| `str_aux_is_copy_item_icon` | Boolean | `true` |  |
| `str_aux_is_copy_item_passive` | Boolean | `true` |  |
| `str_aux_is_copy_passive` | Boolean | `true` |  |
| `str_aux` | Enum/String | `ModelingClay_Default` |  |
| `str` | Number | `1, 2, aux` |  |
| `variant_of` | Enum/String | `PoundOfFlesh, RedCap, CrimsonMask` |  |
| `weightless` | Boolean | `true` |  |

### Context: `AIControlNextTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | `true` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `AbilityHealthThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `cm_HealPercent_Auto` | ID of the ability to trigger or reference. |
| `aux` | Number | `25` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `threshold` | String | `"max(X*.5, 1)"` |  |

### Context: `AbilityOnRoundEndOnce`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `wp_SignalAmplifierSpawnTerminator` | ID of the ability to trigger or reference. |
| `even_of_stunned` | Boolean | `true` |  |

### Context: `AddAdvantageToEvent`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `add` | Number | `5` |  |
| `options` | Array | `[ smash bash open ]` |  |
| `type` | Enum/String | `treasure_box` | Classification type. |

### Context: `AddDamageToElementDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1, 2` | The base damage properties of an attack. |
| `element` | Enum/String | `Ice, Fire, Electric` | Specific element type required or applied. |

### Context: `AddPassivesToCharmed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |

### Context: `AddPassivesToMinions`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `2` | Applies or references the 'AddMaxHealth' effect/state. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `HealthGain` | Number | `2, 4` | Applies or references the 'HealthGain' effect/state. |
| `Shield` | Number | `2` | Applies or references the 'Shield' effect/state. |

### Context: `AddSelfStatusToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `ForceUseAbility` | Enum/String | `DustDash` | Applies or references the 'ForceUseAbility' effect/state. |
| `Quivered` | Array | `[ 1 .10 ]` | Applies or references the 'Quivered' effect/state. |
| `RandomMagicMissile` | Number | `1, 2, 3` | Fires a randomized number of magic missiles. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

### Context: `AddSelfStatusToWeapons`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RepairWeapon` | Array | `[ 1 .25 ]` | Applies or references the 'RepairWeapon' effect/state. |

### Context: `AddStatusToAllDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_HasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Conditional_HasTag` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `KnockbackIfCrit` | Block | `{ ... }` | Applies or references the 'KnockbackIfCrit' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `must_do_damage` | Boolean | `true` |  |

### Context: `AddStatusToBackstabs`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `ChangeTile` | Enum/String | `TallGrassTile, GlassTile, BrambleTile` | Transforms the terrain tile under the target. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `DamageOrHealConditionally` | Number | `1` | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `Fear` | Array | `[ 1 .1 ], [ 1 .15 ], [ 1, .25 ]` | Applies or references the 'Fear' effect/state. |
| `ForceUseAbilityOnTarget` | Block | `{ ... }` | Applies or references the 'ForceUseAbilityOnTarget' effect/state. |
| `Freeze` | Array | `[ 1 .1 ]` | Applies or references the 'Freeze' effect/state. |
| `KnockOutCoin` | Number | `1` | Forces the target to drop coins. |
| `KnockUpAndAway` | Block | `{ ... }` | Displaces the target vertically and horizontally away from the source. |
| `Knockback` | Number | `1, 2` | Applies or references the 'Knockback' effect/state. |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |
| `Leeches` | Number | `1` | Applies or references the 'Leeches' effect/state. |
| `MagicWeakness` | Number | `1` | Applies or references the 'MagicWeakness' effect/state. |
| `ManaLeeches` | Number | `1` | Applies or references the 'ManaLeeches' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `OverrideChainKnockback` | Number | `1` | Applies or references the 'OverrideChainKnockback' effect/state. |
| `Poison` | Number | `1, 2` | Applies or references the 'Poison' effect/state. |
| `PullSourceToTarget` | Number | `1` | Applies or references the 'PullSourceToTarget' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `SoulLink` | Number | `1` | Applies or references the 'SoulLink' effect/state. |
| `SpiderInfested` | Number | `1` | Applies or references the 'SpiderInfested' effect/state. |
| `Stun` | Array | `[ 1, .1 ]` | Applies or references the 'Stun' effect/state. |
| `Tangled` | Array | `[ 1, .05 ], [ 1, .33 ]` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `Weakness` | Number | `1, 3` | Applies or references the 'Weakness' effect/state. |

### Context: `AddStatusToElementDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Stun` | Array | `[ 1 .1 ]` | Applies or references the 'Stun' effect/state. |
| `element` | Enum/String | `Fire, Electric` | Specific element type required or applied. |

### Context: `AddStatusToKnockbackDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Stun` | Array | `[ 1, .1 ]` | Applies or references the 'Stun' effect/state. |

### Context: `AddStatusToSpells`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Enemy` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |

### Context: `AddStatusToWeapons`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |

### Context: `AddTemporaryEffectsToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CastAgainWithStatus` | Block | `{ ... }` | Applies or references the 'CastAgainWithStatus' effect/state. |

### Context: `AlluringDoodieEater`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `damage_instance` | Block | `{ ... }` |  |

### Context: `AllyDodgeChanceAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `range` | Number | `1` | Distance or area of effect in tiles. |

### Context: `ApplyPassives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `StatusOnBattleEnd` | Block | `{ ... }` | Applies the nested status effects when the encounter finishes. |

### Context: `ApplyStatusesToRandomEnemiesEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | `1` | Applies or references the 'Bounty' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `count` | Number | `1` | Quantity. |

### Context: `ApplyToRandomPartyMemberIfPossible`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `GainDisorderFromPool` | Enum/String | `all_disorders` | Applies or references the 'GainDisorderFromPool' effect/state. |

### Context: `ApplyToSource`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Charge` | Number | `1, 3` | Applies or references the 'Charge' effect/state. |
| `HealthGain` | Number | `3` | Applies or references the 'HealthGain' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

### Context: `ArmorBreakOnHit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number | `5%, 10%` |  |
| `durability_loss` | Number | `0` |  |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `face_StevenMask2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

### Context: `BackflipWhenTargeted`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `BackflipDodge` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

### Context: `BoostWeaponDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number | `1, .5` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |

### Context: `BouncyProjectiles`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | `1` |  |
| `max_range` | Number | `2` |  |

### Context: `BuffImmunity`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exclude` | Enum/String | `SpellDamageUp` |  |

### Context: `CastAgainWithStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | `1` | Applies or references the 'OverrideDamage' effect/state. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `CatPartsSizeScale`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `head` | Number | `1.3` |  |

### Context: `CatchProjectiles`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `ally_chance` | Number | `15%` |  |
| `chance` | Number | `15%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

### Context: `ChanceToBackflip`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `BlinkDodge, ShadowstepDodge` | ID of the ability to trigger or reference. |
| `chance` | Number | `33%, 10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

### Context: `ChanceToBlockAndCounter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean | `true` |  |
| `chance` | Number | `100%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

### Context: `ChanceToForceEvent`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `event` | Enum/String | `Blessing` |  |

### Context: `ChanceToRevive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `34%` |  |
| `stacks` | Number | `50` | Number of stacks or intensity to apply. |

### Context: `ClassManaCostReduction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `class` | Enum/String | `Colorless` | Character class identifier. |
| `reduction` | Number | `1, 2` |  |

### Context: `Conditional_Adjacent`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Ally` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `Conditional_PlayerCat` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a player-controlled cat. |

### Context: `Conditional_Ally`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `1` | Applies or references the 'ManaGain' effect/state. |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `odds` | Enum/String | `.1, .3` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

### Context: `Conditional_Boss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1, -2` | Applies or references the 'AllStatsUp' effect/state. |

### Context: `Conditional_Corpse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |

### Context: `Conditional_Enemy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Leeches` | Number | `1` | Applies or references the 'Leeches' effect/state. |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |
| `FindItemFromPool` | Enum/String | `parasites, consumables` | Generates an item drop from the specified loot pool. |
| `ForceUseAbility_NonStack` | Enum/String | `Endeavor_Auto` | Applies or references the 'ForceUseAbility_NonStack' effect/state. |
| `ForceUseAbility` | Enum/String | `tk_WeirdEgg_Spawn, cm_RaptorEggSpawn, tk_Asteroid` | Applies or references the 'ForceUseAbility' effect/state. |
| `Freeze` | Number | `1` | Applies or references the 'Freeze' effect/state. |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |
| `odds` | Number | `15%, 1%, 10%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

### Context: `Conditional_HasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `FlatLeechIfDamaged` | Number | `3` | Applies or references the 'FlatLeechIfDamaged' effect/state. |
| `ImmediateUseAbility_Instant` | Enum/String | `head_CrownOfHorns` | Applies or references the 'ImmediateUseAbility_Instant' effect/state. |
| `RemoveStatusStacks` | Block | `{ ... }` | Removes a specific number of stacks of a status effect. |
| `status` | Enum/String | `Bleed, Thorns` | The specific status ID to check for. |

### Context: `Conditional_HasTag`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusKnockbackDamage` | Number | `5` | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `OverrideChainKnockback` | Number | `0` | Applies or references the 'OverrideChainKnockback' effect/state. |
| `tag` | Enum/String | `rock` | The specific string tag to check for. |

### Context: `Conditional_HealthThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_OncePerBattle` | Block | `{ ... }` | Conditional trigger: Executes nested logic only once per encounter/battle. |
| `threshold_flat` | Number | `3` | A flat numerical health value threshold. |

### Context: `Conditional_ManaThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |
| `threshold_flat` | Number | `0` |  |

### Context: `Conditional_OncePerBattle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ReduceManaCost` | Number | `1` | Applies or references the 'ReduceManaCost' effect/state. |
| `Shield` | Number | `3` | Applies or references the 'Shield' effect/state. |
| `ShowText` | String | `"COMBAT_POPUP_BRAINSTORM"` | Applies or references the 'ShowText' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |
| `key` | Enum/String | `JewelOfDrog` |  |

### Context: `Conditional_PartyMember`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_IsSelf` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is the caster themselves. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |

### Context: `Conditional_PlayerCat`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |

### Context: `Conditional_RandomChance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyPassives` | Block | `{ ... }` | Grants the nested passive abilities dynamically. |
| `odds` | Number | `20%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

### Context: `Conditional_Shielded`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `SetItemAux` | Block | `{ ... }` | Applies or references the 'SetItemAux' effect/state. |

### Context: `ConvertDamageToScaledStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | `1` | Applies or references the 'DelayedPain' effect/state. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

### Context: `CounterAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `attack, neck_TentacleArmorCounter, head_IronJaw` | ID of the ability to trigger or reference. |
| `melee_only` | Boolean | `true` |  |
| `ranged_only` | Boolean | `true` |  |

### Context: `Craft`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Enum/String | `tinkerer_default, bombs` |  |
| `slot` | Enum/String | `weapon` | Equipment slot (weapon, hat, face, chest, etc.). |
| `works_with_tech` | Boolean | `true` |  |

### Context: `CreateGlobalModifiers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Number | `1` | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. |
| `NoCorpses` | Number | `1` | Applies or references the 'NoCorpses' effect/state. |

### Context: `CritsApplyStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |

### Context: `DelayedAutoRevive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `15%, 50%` |  |
| `rounds` | Number | `1, 2` |  |

### Context: `DestroyEquipmentAndAttachParasite`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.75` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `pool` | Array | `[ FaceGrub HeadGrub NeckGrub ]` | The item pool to draw the parasite from. |

### Context: `DoDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage_tiles` | Enum/String | `all` |  |
| `damage` | Number | `0` | The flat damage amount. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `type` | Enum/String | `spell` | The classification of the damage (e.g., spell, melee). |

### Context: `DurabilityTransform`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `eq` | Array | `[ 0 JarOfNothing ], [ 0 WaterBottle_Empty ], [ 1 WaterBottle_Half ]` |  |
| `ge` | Array | `[ 3 EstusFlask_Full ], [ 2 WaterBottle_Full ]` |  |

### Context: `ElementalManaCostReduction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Array | `[ Fire Earth ], [ Holy ]` | Specific element type required or applied. |
| `reduction` | Number | `1` |  |

### Context: `Else`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |

### Context: `Eternal`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | `100%` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `ExtraStatusWhenDealingDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_PartyMember` | Block | `{ ... }` | Conditional constraint. Nested properties only trigger if this is true. |

### Context: `FlyDamageIncrease`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

### Context: `ForceUseAbilityOnTarget`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `head_MiniMoonArmorAsteroid` | ID of the ability to trigger or reference. |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

### Context: `GainCoinsRange`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `25, 30, 60` | Maximum coins granted. |
| `min` | Number | `1, 15, 30` | Minimum coins granted. |

### Context: `GlobalMeleeRevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `5` |  |

### Context: `ImmediateUseAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `wp_NuclearKnifeExplode` | ID of the ability to trigger or reference. |
| `even_if_stunned` | Boolean | `true` |  |

### Context: `ItemAuxTransform`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ge` | Array | `[ 10 NuclearKnife_Glowing ], [ 20 BlackShard_Glowing ]` |  |
| `le` | Array | `[ 50 MoneyBag_Large ], [ 25 MoneyBag_Medium ], [ 10 MoneyBag_Small ]` |  |
| `lt` | Array | `[ 10 NuclearKnife ]` |  |

### Context: `KnockUpAndAway`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `3` | The distance in tiles to knock the target away. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

### Context: `KnockbackIfCrit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `10` |  |
| `override_chain_knockback` | Number | `10` |  |

### Context: `ManaGainRange`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `4` |  |
| `min` | Number | `0` |  |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `knockback` | Number | `1, 2, 10` |  |

### Context: `ModifyAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cost` | Block | `{ ... }` | Currency value in shops/merchants. |
| `meta` | Block | `{ ... }` |  |

### Context: `MovementReaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `wp_Blackjack_Auto, wp_ZodiacsSixshooter_Auto` | ID of the ability to trigger or reference. |
| `create_temp_ability` | Boolean | `true` |  |
| `enemies_only` | Boolean | `true` |  |
| `on_self_move_too` | Boolean | `true` |  |

### Context: `ObjectDetector`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `object` | Enum/String | `CharmedDip` |  |

### Context: `ObjectOnHitCharacter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `CharmedTinySpider, CharmedLeech` | The entity ID of the character to spawn (e.g., CharmedFlea). |
| `stacks` | Number | `1, "floor(lck/4)"` | Number of stacks or intensity to apply. |

### Context: `PassiveAfterXKills`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Passives granted by equipping this. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

### Context: `PassiveAtHealthThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal, equal, greater` |  |
| `passives` | Block | `{ ... }` | Passives granted by equipping this. |
| `threshold` | Number | `1, 5, 10` |  |

### Context: `PassiveAtStatThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal` |  |
| `passives` | Block | `{ ... }` | Passives granted by equipping this. |
| `threshold` | Block | `{ ... }` |  |

### Context: `PassiveIfStrAuxEquals`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Passives granted by equipping this. |
| `value` | Enum/String | `con, dex, str` |  |

### Context: `PassiveIfWeaponIsUsable`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1, 2` | Applies or references the 'Brace' effect/state. |

### Context: `PassiveWhenAffectedByElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `water` | Specific element type required or applied. |
| `passives` | Block | `{ ... }` | Passives granted by equipping this. |

### Context: `PassiveWhenDead`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AutocastEachRound` | Block | `{ ... }` | Forces the character to automatically cast a specific ability at the start of each combat round. |
| `StatusEachRoundEnd` | Block | `{ ... }` | Applies or references the 'StatusEachRoundEnd' effect/state. |
| `StatusEachTurnBegin` | Block | `{ ... }` | Applies or references the 'StatusEachTurnBegin' effect/state. |

### Context: `PassiveWhenOnTile`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` | Passives granted by equipping this. |
| `tile` | Array | `[ TallGrassTile TallFlowerTile ], [ WaterTile ]` |  |

### Context: `PassiveWhileHasDurability`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `MovementReaction` | Block | `{ ... }` | Applies or references the 'MovementReaction' effect/state. |

### Context: `PassiveWhileInMonkMeleeStance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |

### Context: `PassiveWhileShielded`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |

### Context: `PoopWhenHit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `object` | Enum/String | `Poop` |  |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentCharisma` | Number | `1` | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentConstitution` | Number | `1` | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Number | `1` | Applies or references the 'PermanentDexterity' effect/state. |
| `PermanentIntelligence` | Number | `1` | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Number | `1` | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentSpeed` | Number | `1` | Applies or references the 'PermanentSpeed' effect/state. |
| `PermanentStrength` | Number | `1` | Applies or references the 'PermanentStrength' effect/state. |

### Context: `RefreshEquipmentAbilityOnElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Electric` | Specific element type required or applied. |
| `text` | String | `"COMBAT_POPUP_RECHARGED"` |  |

### Context: `RemoveStatusStacks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | The number of stacks to remove. |
| `status` | Enum/String | `Thorns` | The specific status effect ID to remove. |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1, 0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Electric ]` |  |

### Context: `ReviveNextRound`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `2` | Applies or references the 'Shield' effect/state. |
| `revive_health` | Number | `100%` | The flat amount of health to revive with. |

### Context: `ScaldingOrbMoonBossOneShot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | Enum/String | `ScaldingOrb` | Applies or references the 'CompleteItemQuest' effect/state. |
| `RemoveItem` | Enum/String | `ScaldingOrb` | Applies or references the 'RemoveItem' effect/state. |

### Context: `ScaledStatusAlliesOnSpendMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Adjacent` | Block | `{ ... }` | Conditional constraint. Nested properties only trigger if this is true. |

### Context: `ScaledStatusOnHolyShieldBlock`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

### Context: `ScaledStatusOnSpendMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `StatusAfterXStacks` | Block | `{ ... }` | Applies or references the 'StatusAfterXStacks' effect/state. |

### Context: `SetItemAux`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `slot` | Enum/String | `head, face, trinket` | Equipment slot (weapon, hat, face, chest, etc.). |
| `value` | Enum/String | `item_aux+1, item_aux+2, item_aux-1` |  |

### Context: `SpawnEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.2, 5%, 100%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `object` | Enum/String | `CharmedFlea, CharmedAmoeba, [ CharmedFly CharmedMaggot ]` |  |
| `stack_key` | Enum/String | `CATHIDE` |  |

### Context: `SpawnExtraThingsOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `number` | Number | `3, [ 1 2 ]` |  |
| `object` | Enum/String | `RandomPickup` |  |

### Context: `SpawnItemLinkedFamiliar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean | `true` |  |
| `object` | Enum/String | `ZaratanaFamiliar, PyrophinaFamiliar` |  |

### Context: `SpawnObjectOnPopCorpse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `2` | Quantity. |
| `except_tiny` | Boolean | `true` |  |
| `object` | Enum/String | `CharmedTinySpider` |  |

### Context: `SpawnOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `number` | Number | `1, [ 1, 3 ]` |  |
| `object` | Enum/String | `CharmedTinyTumor, Food, CharmedPinky` |  |

### Context: `SpawnOnBattleStartRandomEmptyTile`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `number` | Array | `[ 0 1 ], [ 3 6 ]` |  |
| `object` | Enum/String | `Coin, Bird` |  |

### Context: `SpawnOnDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | Enum/String | `solitary_enemies` |  |
| `obj` | Enum/String | `BeefyCharmedLeech` |  |

### Context: `SpawnRandomPickupsOnTaggedUnitKilled`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Array | `[ 2 3 ]` | Quantity. |
| `tag` | Enum/String | `poop` | Specific entity tag required. |

### Context: `SpawnThingOnDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.25` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `good` | Boolean | `false` |  |
| `number` | Number | `1` |  |
| `object` | Enum/String | `Catnip, CharmedTinySpider, Scrap` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |

### Context: `StackingFlowerTrail`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stack_key` | Enum/String | `FLOWER_SET` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

### Context: `StatDependentPassive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String | `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha...` | Applies or references the 'AddDamageToBasicAttack' effect/state. |

### Context: `StatusAdjacentOnTheirTurnEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Number | `1` | Applies or references the 'ForceMoveAway' effect/state. |

### Context: `StatusAfterCastSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `TempMeleeRangeUp` | Number | `1` | Applies or references the 'TempMeleeRangeUp' effect/state. |
| `TempRangeUp` | Number | `1` | Applies or references the 'TempRangeUp' effect/state. |
| `UseAbility` | Enum/String | `neck_DarkFriend` | Forces the character or target to instantly use a specified ability. |

### Context: `StatusAfterXStacks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `stack_key` | Enum/String | `FANNY_PACK, EMPTY_GENERATOR` |  |
| `threshold` | Number | `12, 3` |  |

### Context: `StatusAfterXTurns`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `tk_MadGhost_Spawn` | Applies or references the 'ForceUseAbility' effect/state. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

### Context: `StatusAllCharactersOnSpawn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Boss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a Boss. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |

### Context: `StatusAlliesEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Adjacent` | Block | `{ ... }` | Conditional constraint. Nested properties only trigger if this is true. |

### Context: `StatusAlliesOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `SpeedUp` | Number | `1, 2` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

### Context: `StatusAlliesOnDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |

### Context: `StatusEachRoundEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DoDamage` | Block | `{ ... }` | Explicitly triggers a secondary damage instance independent of the main attack. |

### Context: `StatusEachTurnBegin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BlessingOfPeace` | Number | `1` | Applies or references the 'BlessingOfPeace' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Conditional_BadRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |
| `DoubleCastSpellThisTurn` | Number | `1` | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |
| `DrinkWater` | Number | `1` | Applies or references the 'DrinkWater' effect/state. |
| `ManaGainRange` | Block | `{ ... }` | Applies or references the 'ManaGainRange' effect/state. |
| `Revive` | Number | `1` | Applies or references the 'Revive' effect/state. |
| `SpeedUp` | Number | `2` | Applies or references the 'SpeedUp' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `UseAbility` | Enum/String | `neck_DarkFriend` | Forces the character or target to instantly use a specified ability. |
| `Wet` | Number | `1` | Applies or references the 'Wet' effect/state. |

### Context: `StatusEachTurnEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddWeaponAux` | Number | `1` | Applies or references the 'AddWeaponAux' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Conditional_ManaThreshold` | Block | `{ ... }` | Conditional constraint. Nested properties only trigger if this is true. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `ForceUseAbility` | Enum/String | `tk_JarOfRadiation, head_HitlersToupe, tk_SuckStone` | Applies or references the 'ForceUseAbility' effect/state. |
| `ImmediateUseAbility` | Enum/String | `head_ThrobbingCrown, { ... }` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `PartialCleanse` | Number | `1` | Applies or references the 'PartialCleanse' effect/state. |
| `PreEmptiveCounterNextAttacks` | Number | `1` | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |
| `SpawnCoinAnywhere` | Number | `1` | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `Stealth` | Array | `[ 1 .1 ]` | Applies or references the 'Stealth' effect/state. |

### Context: `StatusEachTurnEndForEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `face_FartFace` | Applies or references the 'ForceUseAbility' effect/state. |

### Context: `StatusEveryXSpellCasts`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `3` | Applies or references the 'Charge' effect/state. |
| `IntelligenceUp` | Number | `2` | Applies or references the 'IntelligenceUp' effect/state. |
| `ObjectOnHitCharacter` | Block | `{ ... }` | Spawns a specific character or entity upon impact. |
| `stacks` | Number | `4, 3` | Number of stacks or intensity to apply. |

### Context: `StatusIfUnusedActPoints`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BackflipWhenTargeted` | Enum/String | `X` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `Craft` | Block | `{ ... }` | Synthesizes or spawns a new item from a specific pool. |

### Context: `StatusIfUnusedMovePoints`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `3` | Applies or references the 'Charge' effect/state. |
| `HealthGain` | Number | `3` | Applies or references the 'HealthGain' effect/state. |

### Context: `StatusOnAllyCatDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |

### Context: `StatusOnBackstab`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2` | Applies or references the 'HealthGain' effect/state. |
| `SerratedClaws` | Number | `1` | Applies or references the 'SerratedClaws' effect/state. |

### Context: `StatusOnBattleEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Corpse` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Conditional_Shielded` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has a Shield status. |
| `FindItemFromPool` | Enum/String | `pills, chapter_specific_item` | Generates an item drop from the specified loot pool. |
| `GainCoins` | Number | `1, [ 3 5 ]` | Applies or references the 'GainCoins' effect/state. |
| `PermanentConstitution` | Number | `-1` | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentIntelligence` | Number | `-1` | Applies or references the 'PermanentIntelligence' effect/state. |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |
| `RandomPermanentStat` | Number | `1, -1, -3` | Applies or references the 'RandomPermanentStat' effect/state. |
| `RepairAll` | Number | `1` | Applies or references the 'RepairAll' effect/state. |
| `RepairTrinket` | Number | `99` | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Number | `6` | Applies or references the 'RepairWeapon' effect/state. |
| `SetItemAux` | Block | `{ ... }` | Applies or references the 'SetItemAux' effect/state. |
| `TransformWeapon` | Block | `{ ... }` | Transforms the equipped weapon into another specific weapon state. |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |

### Context: `StatusOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Enum/String | `item_aux` | Applies or references the 'Brace' effect/state. |
| `Craft` | Block | `{ ... }` | Synthesizes or spawns a new item from a specific pool. |
| `DestroyEquipmentAndAttachParasite` | Block | `{ ... }` | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `FindItemFromPool` | Enum/String | `common` | Generates an item drop from the specified loot pool. |
| `ForceUseAbility` | Enum/String | `tk_DybbuksRib` | Applies or references the 'ForceUseAbility' effect/state. |
| `ObjectOnHitCharacter` | Block | `{ ... }` | Spawns a specific character or entity upon impact. |
| `RandomMagicMissile` | Number | `4` | Fires a randomized number of magic missiles. |
| `ReviveNextRound` | Block | `{ ... }` | Queues the character to be resurrected at the start of the next combat round. |
| `SafeDie` | Number | `1` | Applies or references the 'SafeDie' effect/state. |
| `SetHealth` | Number | `50%` | Applies or references the 'SetHealth' effect/state. |
| `StealthUntilBasicAttack` | Number | `1` | Applies or references the 'StealthUntilBasicAttack' effect/state. |

### Context: `StatusOnBreak`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyToRandomPartyMemberIfPossible` | Block | `{ ... }` | Redirects the nested effects to apply to a random living member of the player's party. |
| `Bruise` | Number | `3` | Applies or references the 'Bruise' effect/state. |
| `ChangeTilesUnder` | Enum/String | `WaterTile` | Applies or references the 'ChangeTilesUnder' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `FindItemFromPool` | Enum/String | `common` | Generates an item drop from the specified loot pool. |
| `FindItem` | Enum/String | `Pearl` | Applies or references the 'FindItem' effect/state. |
| `GainCoinsRange` | Block | `{ ... }` | Grants the player a randomized amount of coins within a min/max range. |
| `GainDisorder` | Enum/String | `Psychosis` | Applies or references the 'GainDisorder' effect/state. |
| `HealthGain` | Number | `10` | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `ObjectOnHitCharacter` | Enum/String | `BestBud` | Spawns a specific character or entity upon impact. |
| `PermanentConstitution` | Number | `2` | Applies or references the 'PermanentConstitution' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

### Context: `StatusOnBreakItem`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DoDamage` | Block | `{ ... }` | Explicitly triggers a secondary damage instance independent of the main attack. |
| `Shield` | Number | `3` | Applies or references the 'Shield' effect/state. |

### Context: `StatusOnCastSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

### Context: `StatusOnCollectPickup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `StatusAfterXStacks` | Block | `{ ... }` | Applies or references the 'StatusAfterXStacks' effect/state. |

### Context: `StatusOnDie`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_RandomChance` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a flat percentage random roll. |
| `CreateGlobalModifiers` | Block | `{ ... }` | Generates global map or encounter rules/modifiers. |
| `FindItemFromPool` | Enum/String | `chapter_common` | Generates an item drop from the specified loot pool. |
| `GainCoinsRange` | Block | `{ ... }` | Grants the player a randomized amount of coins within a min/max range. |
| `RandomMagicMissile` | Number | `6` | Fires a randomized number of magic missiles. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |

### Context: `StatusOnDodge`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | `2` | Applies or references the 'DodgeChance_Status' effect/state. |

### Context: `StatusOnEatFood`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |
| `TempPassiveUntilSettled` | Block | `{ ... }` | Applies or references the 'TempPassiveUntilSettled' effect/state. |

### Context: `StatusOnEndMove`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies or references the 'Charge' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `ImmediateUseAbility` | Enum/String | `head_MagnetoAttract` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |

### Context: `StatusOnEnemyDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |

### Context: `StatusOnFallAsleep`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `FillMana` | Number | `1` | Applies or references the 'FillMana' effect/state. |
| `HealRandomInjury` | Number | `1` | Applies or references the 'HealRandomInjury' effect/state. |

### Context: `StatusOnFullMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_OncePerBattle` | Block | `{ ... }` | Conditional trigger: Executes nested logic only once per encounter/battle. |

### Context: `StatusOnGainCoins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `2` | Applies or references the 'LuckUp' effect/state. |
| `Shield` | Enum/String | `X` | Applies or references the 'Shield' effect/state. |

### Context: `StatusOnHealed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

### Context: `StatusOnKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BrittleCharismaUp` | Number | `2` | Applies or references the 'BrittleCharismaUp' effect/state. |
| `BrittleConstitutionUp` | Number | `2` | Applies or references the 'BrittleConstitutionUp' effect/state. |
| `BrittleDexterityUp` | Number | `2` | Applies or references the 'BrittleDexterityUp' effect/state. |
| `BrittleIntelligenceUp` | Number | `2` | Applies or references the 'BrittleIntelligenceUp' effect/state. |
| `BrittleLuckUp` | Number | `2` | Applies or references the 'BrittleLuckUp' effect/state. |
| `BrittleSpeedUp` | Number | `2` | Applies or references the 'BrittleSpeedUp' effect/state. |
| `BrittleStrengthUp` | Number | `2` | Applies or references the 'BrittleStrengthUp' effect/state. |
| `CharismaUp` | Number | `1` | Applies or references the 'CharismaUp' effect/state. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `EquipPermanentItem` | Enum/String | `BoneClub` | Applies or references the 'EquipPermanentItem' effect/state. |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

### Context: `StatusOnKillEnemy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `ForceUseAbility` | Enum/String | `head_CatChestPound` | Applies or references the 'ForceUseAbility' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `ManaGain` | Number | `2` | Applies or references the 'ManaGain' effect/state. |

### Context: `StatusOnPickupCoins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `GainCoins` | Number | `1` | Applies or references the 'GainCoins' effect/state. |

### Context: `StatusOnPopCorpse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Number | `1` | Applies or references the 'RepairWeapon' effect/state. |

### Context: `StatusOnTakeHealthOrShieldDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `DivineShield` | Array | `[ 1 .33 ], [ 1 .5 ]` | Applies or references the 'DivineShield' effect/state. |
| `Metronome` | Number | `1` | Executes a random musical or metronome ability. |

### Context: `StatusOnTookDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Charge` | Number | `1, 2` | Applies or references the 'Charge' effect/state. |
| `Conditional_HasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Conditional_HealthThreshold` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `DivineShield` | Array | `[ 1, .33 ]` | Applies or references the 'DivineShield' effect/state. |
| `DodgeChance_Status` | Number | `5` | Applies or references the 'DodgeChance_Status' effect/state. |
| `RemoveStatus` | Enum/String | `AlphaCat` | Applies or references the 'RemoveStatus' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `type` | Enum/String | `move, attack, spell` | Classification type. |

### Context: `StatusOnUseBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `HealthGain` | Number | `1` | Applies or references the 'HealthGain' effect/state. |

### Context: `StatusRandomEnemiesOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `2` | Applies or references the 'Charmed' effect/state. |
| `Confusion` | Number | `2` | Applies or references the 'Confusion' effect/state. |
| `Fear` | Number | `2` | Applies or references the 'Fear' effect/state. |
| `Freeze` | Number | `2` | Applies or references the 'Freeze' effect/state. |
| `count` | Number | `1, 99` | Quantity. |

### Context: `StatusWhenAllySpendsMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies or references the 'Charge' effect/state. |

### Context: `TempPassiveUntilSettled`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `LimitHeal` | Number | `0` | Applies or references the 'LimitHeal' effect/state. |

### Context: `Temporary`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `stacks` | Number | `1, 2, 3` | Number of stacks or intensity to apply. |
| `status` | Enum/String | `SpeedUp, Brace, FreeSpell` | The status effect to apply. |
| `turns` | Number | `1` | Duration in turns. |

### Context: `TintItem`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `add` | Array | `[ 0.05 0.05 0.05 ]` |  |
| `ignore_if_str_aux_equals` | Enum/String | `ModelingClay_Default` |  |
| `mul` | Array | `[ 0.45 0.3 0.25 ]` |  |

### Context: `TransformItemOnElementInfluence`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Fire, Greater_Water` | Specific element type required or applied. |
| `full_repair` | Boolean | `true` |  |
| `item` | Enum/String | `EstusFlask_Full, GallonOfWater, WaterBottle_Full` | Item ID to reference. |

### Context: `TransformWeapon`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `from` | Enum/String | `Necro_SoulDagger_Charged` | The original weapon ID. |
| `to` | Enum/String | `Necro_SoulDagger_Uncharged` | The transformed weapon ID. |

### Context: `TunnelVision`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number | `50%` |  |

### Context: `bonus_passives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ModifyAbility` | Block | `{ ... }` | Applies or references the 'ModifyAbility' effect/state. |

### Context: `cost`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `charge` | Number | `1` |  |
| `mana` | Number | `0` |  |

### Context: `damage_instance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `type` | Enum/String | `status` | Classification type. |

### Context: `effects`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `BounceObject` | Enum/String | `CharmedDip, RandomPickup` | Spawns a physics object that visually bounces off the target. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Confusion` | Number | `2` | Applies or references the 'Confusion' effect/state. |
| `Fear` | Array | `[ 1, .15 ], [ 1, .5 ], [ 1, .25 ]` | Applies or references the 'Fear' effect/state. |
| `Freeze` | Array | `[ 1, .25 ]` | Applies or references the 'Freeze' effect/state. |
| `Grappled` | Array | `[ 1, .75 ], [ 1, .50 ]` | Applies or references the 'Grappled' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Stun` | Array | `[ 1, .25 ], [ 1, .1 ]` | Applies or references the 'Stun' effect/state. |
| `VisualFXTile` | Enum/String | `WaterConduct` | Applies or references the 'VisualFXTile' effect/state. |
| `VisualFX` | Enum/String | `Bolt` | Applies or references the 'VisualFX' effect/state. |

### Context: `global_passives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | `100%, 30%` | Applies or references the 'GlobalEnemyAutoRevive' effect/state. |
| `NoCorpses` | Number | `1` | Applies or references the 'NoCorpses' effect/state. |
| `RealTimePressure` | Number | `5` | Applies or references the 'RealTimePressure' effect/state. |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |

### Context: `meta`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean | `false` |  |
| `is_weapon` | Boolean | `true` |  |

### Context: `passive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | `1` | Applies or references the 'Metal' effect/state. |

### Context: `passives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AIControlNextTurn` | Block | `{ ... }` | Applies or references the 'AIControlNextTurn' effect/state. |
| `AOEBonus` | Number | `1` | Applies or references the 'AOEBonus' effect/state. |
| `AbilityHealthThreshold` | Block | `{ ... }` | Applies or references the 'AbilityHealthThreshold' effect/state. |
| `AbilityOnBattleStart` | Enum/String | `face_FartFaceFixed, face_FartFace, head_SpiderInjector` | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AbilityOnRoundEndOnce` | Block | `{ ... }` | Applies or references the 'AbilityOnRoundEndOnce' effect/state. |
| `AbilityReaction` | Enum/String | `head_EmoSong` | Applies or references the 'AbilityReaction' effect/state. |
| `AddAdvantageToEvent` | Block | `{ ... }` | Applies or references the 'AddAdvantageToEvent' effect/state. |
| `AddBonusMeleeRange` | Number | `1` | Applies or references the 'AddBonusMeleeRange' effect/state. |
| `AddBonusRange` | Number | `1, 2, 10` | Applies or references the 'AddBonusRange' effect/state. |
| `AddCorpseHealth` | Number | `6, -999999` | Applies or references the 'AddCorpseHealth' effect/state. |
| `AddCritMultiplier` | Number | `33%` | Applies or references the 'AddCritMultiplier' effect/state. |
| `AddDamageToElementDamage` | Block | `{ ... }` | Applies or references the 'AddDamageToElementDamage' effect/state. |
| `AddElementsToBasicAttack` | Enum/String | `Holy` | Applies or references the 'AddElementsToBasicAttack' effect/state. |
| `AddEndOfCombatRegen` | Number | `12, 999999` | Applies or references the 'AddEndOfCombatRegen' effect/state. |
| `AddHiddenTag` | Enum/String | `the_nuke_bearer` | Applies or references the 'AddHiddenTag' effect/state. |
| `AddInitiative` | Number | `-20, 100` | Applies or references the 'AddInitiative' effect/state. |
| `AddKnockbackDamage` | Number | `1` | Applies or references the 'AddKnockbackDamage' effect/state. |
| `AddLevelUpRerolls` | Number | `1, 2, 3` | Applies or references the 'AddLevelUpRerolls' effect/state. |
| `AddManaRegen` | Number | `1, 2, 3` | Applies or references the 'AddManaRegen' effect/state. |
| `AddPassivesToCharmed` | Block | `{ ... }` | Applies or references the 'AddPassivesToCharmed' effect/state. |
| `AddPassivesToMinions` | Block | `{ ... }` | Applies or references the 'AddPassivesToMinions' effect/state. |
| `AddSelfStatusToBasicAttack` | Block | `{ ... }` | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. |
| `AddSelfStatusToWeapons` | Block | `{ ... }` | Applies or references the 'AddSelfStatusToWeapons' effect/state. |
| `AddStatusToAllDamage` | Block | `{ ... }` | Modifier: Injects a status effect into a specific action. |
| `AddStatusToBackstabs` | Block | `{ ... }` | Modifier: Injects a status effect into a specific action. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `AddStatusToElementDamage` | Block | `{ ... }` | Modifier: Injects a status effect into a specific action. |
| `AddStatusToKnockbackDamage` | Block | `{ ... }` | Modifier: Injects a status effect into a specific action. |
| `AddStatusToSpells` | Block | `{ ... }` | Modifier: Injects a status effect into a specific action. |
| `AddStatusToWeapons` | Block | `{ ... }` | Modifier: Injects a status effect into a specific action. |
| `AddTag` | Enum/String | `bug, rock` | Applies or references the 'AddTag' effect/state. |
| `AddTemporaryEffectsToBasicAttack` | Block | `{ ... }` | Applies or references the 'AddTemporaryEffectsToBasicAttack' effect/state. |
| `AllSpellsCostCharge` | Number | `1` | Applies or references the 'AllSpellsCostCharge' effect/state. |
| `AllStatsUpPerDisorder` | Number | `1` | Applies or references the 'AllStatsUpPerDisorder' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `AllUnitsExplodeOnDeath` | Number | `5` | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. |
| `AlliesScrambleSpellAfterCast` | Number | `1` | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. |
| `AlluringDoodieEater` | Block | `{ ... }` | Applies or references the 'AlluringDoodieEater' effect/state. |
| `AllyDamageReduction` | Number | `0` | Applies or references the 'AllyDamageReduction' effect/state. |
| `AllyDodgeChanceAura` | Block | `{ ... }` | Applies or references the 'AllyDodgeChanceAura' effect/state. |
| `AlphaAllStatsUp` | Number | `1` | Applies or references the 'AlphaAllStatsUp' effect/state. |
| `AlphaCat` | Number | `1` | Applies or references the 'AlphaCat' effect/state. |
| `AlphaTurns` | Number | `1, -1` | Applies or references the 'AlphaTurns' effect/state. |
| `AlwaysChosenForLevelUp` | Number | `1` | Applies or references the 'AlwaysChosenForLevelUp' effect/state. |
| `AmplifyKnockback` | Number | `2, 10` | Applies or references the 'AmplifyKnockback' effect/state. |
| `AmplifyStatus` | Enum/String | `Poison, Bleed` | Applies or references the 'AmplifyStatus' effect/state. |
| `ApplyStatusesToRandomEnemiesEachTurn` | Block | `{ ... }` | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. |
| `ArmorBreakOnHit` | Block | `{ ... }` | Applies or references the 'ArmorBreakOnHit' effect/state. |
| `ArmorDodgeChance` | Number | `5%, 15%, 10%` | Applies or references the 'ArmorDodgeChance' effect/state. |
| `AutoEquipConsumables` | Number | `1` | Applies or references the 'AutoEquipConsumables' effect/state. |
| `BackflipWhenTargeted` | Block | `{ ... }` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BackstabCritChance` | Enum/String | `.25` | Applies or references the 'BackstabCritChance' effect/state. |
| `BalanceStats` | Number | `1` | Applies or references the 'BalanceStats' effect/state. |
| `BasicAttackCantMiss` | Number | `1` | Applies or references the 'BasicAttackCantMiss' effect/state. |
| `BasicAttackCritChance` | Enum/String | `.1` | Applies or references the 'BasicAttackCritChance' effect/state. |
| `BleedThorns` | Number | `6, 1, 3` | Applies or references the 'BleedThorns' effect/state. |
| `Bleed` | Number | `6, 1, 3` | Applies or references the 'Bleed' effect/state. |
| `Blind` | Number | `-1` | Applies or references the 'Blind' effect/state. |
| `BlockDamageUnderThreshold` | Number | `1` | Applies or references the 'BlockDamageUnderThreshold' effect/state. |
| `BlockNegativeStatus` | Number | `30%` | Applies or references the 'BlockNegativeStatus' effect/state. |
| `BoneArmorPassive` | Number | `1` | Applies or references the 'BoneArmorPassive' effect/state. |
| `BonusAbility` | Enum/String | `WasteTime, neck_NukeBonus` | Applies or references the 'BonusAbility' effect/state. |
| `BoostHeals` | Number | `1, 2` | Applies or references the 'BoostHeals' effect/state. |
| `BoostReceivedHealing` | Number | `2` | Applies or references the 'BoostReceivedHealing' effect/state. |
| `BoostWeaponDamage` | Block | `{ ... }` | Applies or references the 'BoostWeaponDamage' effect/state. |
| `BouncyProjectiles` | Block | `{ ... }` | Applies or references the 'BouncyProjectiles' effect/state. |
| `Brace` | Number | `1, 2, 3` | Applies or references the 'Brace' effect/state. |
| `BreakAtAux` | Number | `0` | Applies or references the 'BreakAtAux' effect/state. |
| `BreakOnElement` | Enum/String | `water` | Applies or references the 'BreakOnElement' effect/state. |
| `BreakWhenNoShield` | Number | `1` | Applies or references the 'BreakWhenNoShield' effect/state. |
| `BrittleDuringElement` | Enum/String | `water` | Applies or references the 'BrittleDuringElement' effect/state. |
| `Brittle` | Number | `1` | Applies or references the 'Brittle' effect/state. |
| `Bruise` | Number | `1, 2` | Applies or references the 'Bruise' effect/state. |
| `BuffImmunity` | Block | `{ ... }` | Applies or references the 'BuffImmunity' effect/state. |
| `Burn` | Number | `2` | Applies or references the 'Burn' effect/state. |
| `CanLevelUpWhenDead` | Number | `1` | Applies or references the 'CanLevelUpWhenDead' effect/state. |
| `CanRemoveCursedItems` | Number | `1` | Applies or references the 'CanRemoveCursedItems' effect/state. |
| `CantCatchDiseases` | Number | `1` | Applies or references the 'CantCatchDiseases' effect/state. |
| `CantSpreadDiseases` | Number | `1` | Applies or references the 'CantSpreadDiseases' effect/state. |
| `CapBasicAttackDamage` | Number | `1` | Applies or references the 'CapBasicAttackDamage' effect/state. |
| `CapMovementAbilityRange` | Number | `1` | Applies or references the 'CapMovementAbilityRange' effect/state. |
| `CatPartsSizeScale` | Block | `{ ... }` | Applies or references the 'CatPartsSizeScale' effect/state. |
| `CatchProjectiles` | Block | `{ ... }` | Applies or references the 'CatchProjectiles' effect/state. |
| `ChanceToAmbush` | Number | `25%` | Applies or references the 'ChanceToAmbush' effect/state. |
| `ChanceToBackflip` | Block | `{ ... }` | Applies or references the 'ChanceToBackflip' effect/state. |
| `ChanceToBlockAndCounter` | Number | `25%, { ... }` | Applies or references the 'ChanceToBlockAndCounter' effect/state. |
| `ChanceToBlock` | Number | `10%` | Applies or references the 'ChanceToBlock' effect/state. |
| `ChanceToForceEvent` | Block | `{ ... }` | Applies or references the 'ChanceToForceEvent' effect/state. |
| `ChanceToRevive` | Number | `25, 100, { ... }` | Applies or references the 'ChanceToRevive' effect/state. |
| `Charge` | Number | `5` | Applies or references the 'Charge' effect/state. |
| `CharismaIsMaxStat` | Number | `1` | Applies or references the 'CharismaIsMaxStat' effect/state. |
| `CharmImmunity` | Number | `1` | Applies or references the 'CharmImmunity' effect/state. |
| `ClassManaCostReduction` | Block | `{ ... }` | Applies or references the 'ClassManaCostReduction' effect/state. |
| `Confusion` | Number | `2, 99, 3` | Applies or references the 'Confusion' effect/state. |
| `ConsumableEffectsMultiplierBonus` | Number | `1` | Applies or references the 'ConsumableEffectsMultiplierBonus' effect/state. |
| `ConvertDamageToScaledStatus` | Block | `{ ... }` | Applies or references the 'ConvertDamageToScaledStatus' effect/state. |
| `CopyPassiveSlot` | Number | `1, 0` | Applies or references the 'CopyPassiveSlot' effect/state. |
| `CounterAttack` | Block | `{ ... }` | Applies or references the 'CounterAttack' effect/state. |
| `CounterNextAttacks` | Number | `2` | Applies or references the 'CounterNextAttacks' effect/state. |
| `CreateGlobalModifiers` | Block | `{ ... }` | Generates global map or encounter rules/modifiers. |
| `CritChanceUp` | Number | `5, 10, 100` | Applies or references the 'CritChanceUp' effect/state. |
| `CritsApplyStatus` | Block | `{ ... }` | Applies or references the 'CritsApplyStatus' effect/state. |
| `DamageUp` | Number | `6, 1, -2` | Applies or references the 'DamageUp' effect/state. |
| `DeathRattleRevive` | Enum/String | `DoNothing, tk_PetrifiedPinky` | Applies or references the 'DeathRattleRevive' effect/state. |
| `DeathRattle` | Enum/String | `neck_NukeExplode` | Applies or references the 'DeathRattle' effect/state. |
| `DebuffImmunity` | Number | `1` | Applies or references the 'DebuffImmunity' effect/state. |
| `DelayedAutoRevive` | Block | `{ ... }` | Applies or references the 'DelayedAutoRevive' effect/state. |
| `DepressionAura` | Number | `1, 2` | Applies or references the 'DepressionAura' effect/state. |
| `DisableAbilities` | Enum/String | `all_items, basic_attack, all_spells` | Applies or references the 'DisableAbilities' effect/state. |
| `DisablePassiveSlot` | Number | `1, 0` | Applies or references the 'DisablePassiveSlot' effect/state. |
| `DodgeChance_Status` | Number | `40, 15, 10` | Applies or references the 'DodgeChance_Status' effect/state. |
| `DodgeChance` | Number | `15%, 25%` | Applies or references the 'DodgeChance' effect/state. |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | `3` | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. |
| `DoubleCastTaggedSpells` | Enum/String | `musical` | Applies or references the 'DoubleCastTaggedSpells' effect/state. |
| `DoubleCastWeapons` | Number | `1` | Applies or references the 'DoubleCastWeapons' effect/state. |
| `DoubleReceivedNegativeStatus` | Number | `1` | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. |
| `DoubleReceivedPositiveStatus` | Number | `1` | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. |
| `DropAsFamiliarOnArmorBreak` | Enum/String | `FaceGrubFamiliar, NeckGrubFamiliar, HeadGrubFamiliar` | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. |
| `DropAsFamiliarOnTookDamage` | Enum/String | `PhantomMaskRock` | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. |
| `DropSoulJarOnDeath` | Enum/String | `SoulJar_Full` | Applies or references the 'DropSoulJarOnDeath' effect/state. |
| `DurabilityTransform` | Block | `{ ... }` | Applies or references the 'DurabilityTransform' effect/state. |
| `ElementImmune` | Enum/String | `Ice, Fire` | Applies or references the 'ElementImmune' effect/state. |
| `ElementalManaCostReduction` | Block | `{ ... }` | Applies or references the 'ElementalManaCostReduction' effect/state. |
| `Eternal` | Block | `{ ... }` | Applies or references the 'Eternal' effect/state. |
| `ExcludeFromEvents` | Enum/String | `Tragedy` | Applies or references the 'ExcludeFromEvents' effect/state. |
| `ExplosionImmunity` | Number | `1` | Applies or references the 'ExplosionImmunity' effect/state. |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraBasicAttacks` | Number | `1, 2` | Applies or references the 'ExtraBasicAttacks' effect/state. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `ExtraMovePoints` | Number | `1` | Applies or references the 'ExtraMovePoints' effect/state. |
| `ExtraStatusWhenDealingDamage` | Block | `{ ... }` | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. |
| `ExtraTrinketUses` | Number | `10` | Applies or references the 'ExtraTrinketUses' effect/state. |
| `ExtraWeaponAttacks` | Number | `1, 2` | Applies or references the 'ExtraWeaponAttacks' effect/state. |
| `FaceArmorPassiveMultiplierBonus` | Number | `1, 2` | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. |
| `FaceShield` | Number | `1` | Applies or references the 'FaceShield' effect/state. |
| `FindExtraItemFromPoolOnBattleEnd` | Enum/String | `combat_reward_easy` | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. |
| `Flammable` | Number | `1, 2` | Applies or references the 'Flammable' effect/state. |
| `FlowersOnEndTurn` | Number | `1` | Applies or references the 'FlowersOnEndTurn' effect/state. |
| `FlyDamageIncrease` | Block | `{ ... }` | Applies or references the 'FlyDamageIncrease' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `FragileDuringElement` | Enum/String | `water` | Applies or references the 'FragileDuringElement' effect/state. |
| `Fragile` | Number | `1` | Applies or references the 'Fragile' effect/state. |
| `FrankBolts` | Number | `1` | Applies or references the 'FrankBolts' effect/state. |
| `FreezePiercing` | Number | `1` | Applies or references the 'FreezePiercing' effect/state. |
| `GainExtraShield` | Number | `4` | Applies or references the 'GainExtraShield' effect/state. |
| `GlobalMeleeRevengeDamage` | Block | `{ ... }` | Applies or references the 'GlobalMeleeRevengeDamage' effect/state. |
| `HPGainBlock` | Number | `1` | Applies or references the 'HPGainBlock' effect/state. |
| `HeadArmorPassiveMultiplierBonus` | Number | `1, 2` | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. |
| `HealthRegenUp` | Number | `1, 2, 3` | Applies or references the 'HealthRegenUp' effect/state. |
| `HideSomeHudStuff` | Number | `1` | Applies or references the 'HideSomeHudStuff' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `IncreaseExplosionDamage` | Number | `1, 2` | Applies or references the 'IncreaseExplosionDamage' effect/state. |
| `IncreaseExplosionSize` | Number | `1, 7` | Applies or references the 'IncreaseExplosionSize' effect/state. |
| `IncreaseSpellRange` | Number | `2` | Applies or references the 'IncreaseSpellRange' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `InnateElement` | Enum/String | `Ice` | Applies or references the 'InnateElement' effect/state. |
| `ItemAuxTransform` | Block | `{ ... }` | Applies or references the 'ItemAuxTransform' effect/state. |
| `JesterLevelUpRerolls` | Number | `1` | Applies or references the 'JesterLevelUpRerolls' effect/state. |
| `KillsToMeat` | Enum/String | `Food` | Applies or references the 'KillsToMeat' effect/state. |
| `KineticSpikes` | Number | `1, 3` | Applies or references the 'KineticSpikes' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `LeaveBehindOnceEachMove` | Enum/String | `Scrap, Poop` | Applies or references the 'LeaveBehindOnceEachMove' effect/state. |
| `LevelUpClassOverride` | Enum/String | `Jester` | Applies or references the 'LevelUpClassOverride' effect/state. |
| `Lifesteal` | Number | `1` | Applies or references the 'Lifesteal' effect/state. |
| `LuckUp` | Number | `222` | Applies or references the 'LuckUp' effect/state. |
| `MakeBasicAttackPull` | Number | `1` | Applies or references the 'MakeBasicAttackPull' effect/state. |
| `MakeSpellsRequireCharge` | Number | `1` | Applies or references the 'MakeSpellsRequireCharge' effect/state. |
| `ManaCostReduction` | Number | `1, 2, -2` | Applies or references the 'ManaCostReduction' effect/state. |
| `MeleeRevengeDamage` | Block | `{ ... }` | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. |
| `Metal` | Number | `1` | Applies or references the 'Metal' effect/state. |
| `MissChance` | Number | `10` | Applies or references the 'MissChance' effect/state. |
| `ModelingClayPassive` | Number | `1` | Applies or references the 'ModelingClayPassive' effect/state. |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | Enum/String | `face_EatNeverstone` | Applies or references the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect/state. |
| `MoveQuivered` | Number | `1, 2` | Applies or references the 'MoveQuivered' effect/state. |
| `MoveSpeedMultiplier` | Enum/String | `.5` | Applies or references the 'MoveSpeedMultiplier' effect/state. |
| `MoveTowardsDamageSource` | Enum/String | `MoveOne` | Applies or references the 'MoveTowardsDamageSource' effect/state. |
| `MovementReaction` | Block | `{ ... }` | Applies or references the 'MovementReaction' effect/state. |
| `MultiplyCoinsOnBattleStart` | Number | `2` | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. |
| `MultiplyReceivedHealing` | Number | `2` | Applies or references the 'MultiplyReceivedHealing' effect/state. |
| `NeckArmorPassiveMultiplierBonus` | Number | `1` | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. |
| `ObjectDetector` | Block | `{ ... }` | Applies or references the 'ObjectDetector' effect/state. |
| `OverrideBasicAttack` | Enum/String | `BasicSpin, BasicTankMelee, IsaacBasicAttack` | Applies or references the 'OverrideBasicAttack' effect/state. |
| `PassiveAfterXKills` | Block | `{ ... }` | Applies or references the 'PassiveAfterXKills' effect/state. |
| `PassiveAtHealthThreshold` | Block | `{ ... }` | Applies or references the 'PassiveAtHealthThreshold' effect/state. |
| `PassiveAtStatThreshold` | Block | `{ ... }` | Applies or references the 'PassiveAtStatThreshold' effect/state. |
| `PassiveIfStrAuxEquals` | Block | `{ ... }` | Applies or references the 'PassiveIfStrAuxEquals' effect/state. |
| `PassiveIfWeaponIsUsable` | Block | `{ ... }` | Applies or references the 'PassiveIfWeaponIsUsable' effect/state. |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` | State Trigger: Grants passives when this condition is met. |
| `PassiveWhenDead` | Block | `{ ... }` | State Trigger: Grants passives when this condition is met. |
| `PassiveWhenOnTile` | Block | `{ ... }` | State Trigger: Grants passives when this condition is met. |
| `PassiveWhileHasDurability` | Block | `{ ... }` | Applies or references the 'PassiveWhileHasDurability' effect/state. |
| `PassiveWhileInMonkMeleeStance` | Block | `{ ... }` | Applies or references the 'PassiveWhileInMonkMeleeStance' effect/state. |
| `PassiveWhileShielded` | Block | `{ ... }` | Applies or references the 'PassiveWhileShielded' effect/state. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `PhysicalAttacksMiss` | Number | `1` | Applies or references the 'PhysicalAttacksMiss' effect/state. |
| `PoisonThorns` | Number | `1` | Applies or references the 'PoisonThorns' effect/state. |
| `Poison` | Number | `1, 2, 3` | Applies or references the 'Poison' effect/state. |
| `PoopWhenHit` | Block | `{ ... }` | Applies or references the 'PoopWhenHit' effect/state. |
| `PreventSpecificInjury` | Enum/String | `int` | Applies or references the 'PreventSpecificInjury' effect/state. |
| `Quivered` | Number | `1, 2` | Applies or references the 'Quivered' effect/state. |
| `RandomSeededStatModifier` | Array | `[ 2 -1 ]` | Applies or references the 'RandomSeededStatModifier' effect/state. |
| `RangedTrueShot` | Number | `1` | Applies or references the 'RangedTrueShot' effect/state. |
| `ReclaimItemOnBreak` | Number | `1` | Applies or references the 'ReclaimItemOnBreak' effect/state. |
| `ReduceManaCost` | Number | `2` | Applies or references the 'ReduceManaCost' effect/state. |
| `ReduceSpellCostsPerDisorder` | Number | `1` | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. |
| `ReduceSpellCostsPerParasite` | Number | `1` | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. |
| `ReflectProjectiles` | Number | `25%, 20%` | Applies or references the 'ReflectProjectiles' effect/state. |
| `RefreshEquipmentAbilityOnElement` | Block | `{ ... }` | Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state. |
| `RemoveLineOfSightRestrictions` | Number | `1` | Applies or references the 'RemoveLineOfSightRestrictions' effect/state. |
| `ReplaceBasicAttack` | Enum/String | `head_Pestilence, BasicPoke` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `ReplaceBasicMove` | Enum/String | `head_HeadBrandJump, BellyFlop_BasicMove, BasicJump` | Applies or references the 'ReplaceBasicMove' effect/state. |
| `ReplaceBlankTilesOnBattleStart` | Enum/String | `GlassTile` | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. |
| `ReplaceSpawnedObjects` | Array | `[ FlamingPoop RandomLivingPoop ], [ Poop RandomLivingPoop ]` | Applies or references the 'ReplaceSpawnedObjects' effect/state. |
| `RerollItemsOnBattleEnd` | Number | `1` | Applies or references the 'RerollItemsOnBattleEnd' effect/state. |
| `RevengeDamage` | Block | `{ ... }` | Reaction trigger: Deals damage to the attacker when hit. |
| `RockyArmorPassive` | Number | `1` | Applies or references the 'RockyArmorPassive' effect/state. |
| `ScaldingOrbMoonBossOneShot` | Block | `{ ... }` | Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. |
| `ScaledStatusAlliesOnSpendMana` | Block | `{ ... }` | Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. |
| `ScaledStatusOnHolyShieldBlock` | Block | `{ ... }` | Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. |
| `ScaledStatusOnSpendMana` | Block | `{ ... }` | Applies or references the 'ScaledStatusOnSpendMana' effect/state. |
| `SetBrittleImmune` | String | `""` | Applies or references the 'SetBrittleImmune' effect/state. |
| `SetDefaultFacePassive` | Enum/String | `euphoric` | Applies or references the 'SetDefaultFacePassive' effect/state. |
| `SetFaction` | Enum/String | `enemies` | Applies or references the 'SetFaction' effect/state. |
| `SetFragileImmune` | String | `""` | Applies or references the 'SetFragileImmune' effect/state. |
| `SetSpellCosts` | Number | `0` | Applies or references the 'SetSpellCosts' effect/state. |
| `SharkySmellsBlood` | Number | `1` | Applies or references the 'SharkySmellsBlood' effect/state. |
| `SpawnCatCloneOnCorpsePopped` | Number | `1` | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. |
| `SpawnEachTurn` | Block | `{ ... }` | Applies or references the 'SpawnEachTurn' effect/state. |
| `SpawnExtraThingsOnBattleStart` | Block | `{ ... }` | Applies or references the 'SpawnExtraThingsOnBattleStart' effect/state. |
| `SpawnItemLinkedFamiliar` | Block | `{ ... }` | Applies or references the 'SpawnItemLinkedFamiliar' effect/state. |
| `SpawnNearEnemies` | Number | `1` | Applies or references the 'SpawnNearEnemies' effect/state. |
| `SpawnObjectOnPopCorpse` | Enum/String | `Coin, Food, { ... }` | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. |
| `SpawnOnBattleStartRandomEmptyTile` | Block | `{ ... }` | Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. |
| `SpawnOnBattleStart` | Enum/String | `CharmedCultist, CharmedGamete, { ... }` | Applies or references the 'SpawnOnBattleStart' effect/state. |
| `SpawnOnDeath` | Block | `{ ... }` | Applies or references the 'SpawnOnDeath' effect/state. |
| `SpawnOnDowned` | Enum/String | `CharmedSpookie` | Applies or references the 'SpawnOnDowned' effect/state. |
| `SpawnRandomPickupsOnTaggedUnitKilled` | Block | `{ ... }` | Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. |
| `SpawnThingOnDamage` | Block | `{ ... }` | Applies or references the 'SpawnThingOnDamage' effect/state. |
| `SpawnThingOnDeath` | Enum/String | `CharmedTinyTumor, TheIntruder, CharmedPooter` | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `SpellDamageUp` | Number | `1, 3` | Applies or references the 'SpellDamageUp' effect/state. |
| `StackingFlowerTrail` | Block | `{ ... }` | Applies or references the 'StackingFlowerTrail' effect/state. |
| `StatDependentPassive` | Block | `{ ... }` | Applies or references the 'StatDependentPassive' effect/state. |
| `StatusAdjacentOnTheirTurnEnd` | Block | `{ ... }` | Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state. |
| `StatusAfterCastSpell` | Block | `{ ... }` | Applies or references the 'StatusAfterCastSpell' effect/state. |
| `StatusAfterXTurns` | Block | `{ ... }` | Applies or references the 'StatusAfterXTurns' effect/state. |
| `StatusAllCharactersOnSpawn` | Block | `{ ... }` | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. |
| `StatusAlliesEachTurn` | Block | `{ ... }` | Applies or references the 'StatusAlliesEachTurn' effect/state. |
| `StatusAlliesOnBattleStart` | Block | `{ ... }` | Applies or references the 'StatusAlliesOnBattleStart' effect/state. |
| `StatusAlliesOnDeath` | Block | `{ ... }` | Applies or references the 'StatusAlliesOnDeath' effect/state. |
| `StatusEachTurnBegin` | Block | `{ ... }` | Applies or references the 'StatusEachTurnBegin' effect/state. |
| `StatusEachTurnEndForEachTurn` | Block | `{ ... }` | Applies or references the 'StatusEachTurnEndForEachTurn' effect/state. |
| `StatusEachTurnEnd` | Block | `{ ... }` | Applies or references the 'StatusEachTurnEnd' effect/state. |
| `StatusEveryXSpellCasts` | Block | `{ ... }` | Applies or references the 'StatusEveryXSpellCasts' effect/state. |
| `StatusIfUnusedActPoints` | Block | `{ ... }` | Applies or references the 'StatusIfUnusedActPoints' effect/state. |
| `StatusIfUnusedMovePoints` | Block | `{ ... }` | Applies or references the 'StatusIfUnusedMovePoints' effect/state. |
| `StatusImmunity` | Enum/String | `Poison, [ Freeze, Slow ], [ Fear Confusion PermanentConfusion ]` | Applies or references the 'StatusImmunity' effect/state. |
| `StatusOnAllyCatDeath` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnBackstab` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnBattleEnd` | Block | `{ ... }` | Applies the nested status effects when the encounter finishes. |
| `StatusOnBattleStart` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnBreakItem` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnBreak` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnCastSpell` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnCollectPickup` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnDie` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnDodge` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnEatFood` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnEndMove` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnEnemyDeath` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnFallAsleep` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnFullMana` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnGainCoins` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnHealed` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnKillEnemy` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnKill` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnPickupCoins` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnPopCorpse` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnTakeHealthOrShieldDamage` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnTookDamage` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnTurnEndIfDidntCastAbilityTypes` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusOnUseBasicAttack` | Block | `{ ... }` | Event Trigger: Applies statuses when this action occurs. |
| `StatusRandomEnemiesOnBattleStart` | Block | `{ ... }` | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. |
| `StatusWhenAllySpendsMana` | Block | `{ ... }` | Applies or references the 'StatusWhenAllySpendsMana' effect/state. |
| `StevenBolts` | Number | `1` | Applies or references the 'StevenBolts' effect/state. |
| `StripKnockback` | Number | `1` | Applies or references the 'StripKnockback' effect/state. |
| `TauntAlways` | Number | `1` | Applies or references the 'TauntAlways' effect/state. |
| `Thorns` | Number | `1, 2, 3` | Applies or references the 'Thorns' effect/state. |
| `TintItem` | Block | `{ ... }` | Applies or references the 'TintItem' effect/state. |
| `Trample` | Number | `3` | Applies or references the 'Trample' effect/state. |
| `TransformItemOnElementInfluence` | Block | `{ ... }` | Applies or references the 'TransformItemOnElementInfluence' effect/state. |
| `TrinketActiveEffectsMultiplierBonus` | Number | `1, 2` | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. |
| `TrinketPassiveMultiplierBonus` | Number | `1, 2` | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. |
| `TrueShot` | Number | `1` | Applies or references the 'TrueShot' effect/state. |
| `TunnelVision` | Block | `{ ... }` | Applies or references the 'TunnelVision' effect/state. |
| `Uncontrollable` | Number | `1` | Applies or references the 'Uncontrollable' effect/state. |
| `Undead` | Number | `1` | Applies or references the 'Undead' effect/state. |
| `WeaponDamageMultiplierBonus` | Number | `1` | Applies or references the 'WeaponDamageMultiplierBonus' effect/state. |

### Context: `str_aux_is_copy_ability`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bonus_passives` | Block | `{ ... }` | Passives granted to the character while this ability is equipped. |

### Context: `threshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `0` |  |
| `int` | Number | `0` |  |

---

## Map Generation & Routing

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `#include` | String | `"standard_nodes.gon"` |  |
| `BoneyardUnlocked` | Block | `{ ... }` | Applies or references the 'BoneyardUnlocked' effect/state. |
| `BothObelisksUnlocked` | Block | `{ ... }` | Applies or references the 'BothObelisksUnlocked' effect/state. |
| `BunkerUnlocked` | Block | `{ ... }` | Applies or references the 'BunkerUnlocked' effect/state. |
| `CavesUnlocked` | Block | `{ ... }` | Applies or references the 'CavesUnlocked' effect/state. |
| `ChaosAntennaAttached` | Block | `{ ... }` | Applies or references the 'ChaosAntennaAttached' effect/state. |
| `CoreObeliskUnlocked` | Block | `{ ... }` | Applies or references the 'CoreObeliskUnlocked' effect/state. |
| `CoreUnlocked` | Block | `{ ... }` | Applies or references the 'CoreUnlocked' effect/state. |
| `CraterUnlocked` | Block | `{ ... }` | Applies or references the 'CraterUnlocked' effect/state. |
| `DimensionXUnlocked` | Block | `{ ... }` | Applies or references the 'DimensionXUnlocked' effect/state. |
| `EndOfTimeUnlocked` | Block | `{ ... }` | Applies or references the 'EndOfTimeUnlocked' effect/state. |
| `FutureUnlocked` | Block | `{ ... }` | Applies or references the 'FutureUnlocked' effect/state. |
| `GenFlag_Boss_Spewer` | Block | `{ ... }` | Applies or references the 'GenFlag_Boss_Spewer' effect/state. |
| `GenFlag_Boss_Stacy` | Block | `{ ... }` | Applies or references the 'GenFlag_Boss_Stacy' effect/state. |
| `HardPathUnlocked` | Block | `{ ... }` | Applies or references the 'HardPathUnlocked' effect/state. |
| `IceAgeUnlocked` | Block | `{ ... }` | Applies or references the 'IceAgeUnlocked' effect/state. |
| `JunkyardUnlocked` | Block | `{ ... }` | Applies or references the 'JunkyardUnlocked' effect/state. |
| `JurassicUnlocked` | Block | `{ ... }` | Applies or references the 'JurassicUnlocked' effect/state. |
| `MeatWorldUnlockedFull` | Block | `{ ... }` | Applies or references the 'MeatWorldUnlockedFull' effect/state. |
| `MeatWorldUnlocked` | Block | `{ ... }` | Applies or references the 'MeatWorldUnlocked' effect/state. |
| `MoonObeliskUnlocked` | Block | `{ ... }` | Applies or references the 'MoonObeliskUnlocked' effect/state. |
| `MoonUnlocked` | Block | `{ ... }` | Applies or references the 'MoonUnlocked' effect/state. |
| `SewersUnlocked` | Block | `{ ... }` | Applies or references the 'SewersUnlocked' effect/state. |
| `TheEndUnlocked` | Block | `{ ... }` | Applies or references the 'TheEndUnlocked' effect/state. |
| `ThrobbingArteryDone` | Block | `{ ... }` | Applies or references the 'ThrobbingArteryDone' effect/state. |
| `VolcanoAntennaAttached` | Block | `{ ... }` | Applies or references the 'VolcanoAntennaAttached' effect/state. |
| `WallOfFleshDone` | Block | `{ ... }` | Applies or references the 'WallOfFleshDone' effect/state. |
| `abandonedones` | Enum/String | `auto` |  |
| `advance` | Number | `1` |  |
| `alley` | Block | `{ ... }` |  |
| `battle` | Block | `{ ... }` |  |
| `boneyard` | Block | `{ ... }` |  |
| `boss` | Block | `{ ... }, [ boss ]` |  |
| `bumblefoot` | Enum/String | `auto` |  |
| `bunker` | Block | `{ ... }` |  |
| `butchercat` | Enum/String | `auto` |  |
| `cancreeper` | Enum/String | `auto` |  |
| `cavecatfamily` | Enum/String | `auto` |  |
| `caves` | Block | `{ ... }` |  |
| `cerberubs` | Enum/String | `auto` |  |
| `chapter_item_pool` | Enum/String | `bunkeritems, boneyarditems, alleyitems` |  |
| `choose_one` | Array | `[ GenFlag_Boss_Stacy, GenFlag_Boss_Spewer ]` |  |
| `clericcat` | Enum/String | `auto` |  |
| `core` | Block | `{ ... }` |  |
| `crater` | Block | `{ ... }` |  |
| `desert` | Block | `{ ... }` |  |
| `dimensionx` | Block | `{ ... }` |  |
| `dinocouple` | Enum/String | `auto` |  |
| `drmangler` | Enum/String | `auto` |  |
| `druidcat` | Enum/String | `auto` |  |
| `easy` | Array | `[ easy ], [ easy bigsharklevels ]` |  |
| `endoftime` | Block | `{ ... }` |  |
| `event` | Block | `{ ... }` |  |
| `exit0` | Block | `{ ... }` |  |
| `exit1` | Block | `{ ... }` |  |
| `exit_desert` | Block | `{ ... }` |  |
| `exit_lab` | Block | `{ ... }` |  |
| `fightercat` | Enum/String | `auto` |  |
| `flushmaster` | Enum/String | `auto` |  |
| `folder` | Enum/String | `bunker, boneyard, alley` |  |
| `future` | Block | `{ ... }` |  |
| `gambit` | Enum/String | `auto` |  |
| `hard_initial` | Block | `{ ... }` |  |
| `hard` | Array | `[ easy ], [ easy bigsharklevels ], [ hard ]` |  |
| `head_start` | Number | `99` |  |
| `home` | Block | `{ ... }` |  |
| `huntercat` | Enum/String | `auto` |  |
| `iceage` | Block | `{ ... }` |  |
| `iceelemental` | Enum/String | `auto` |  |
| `infestedduo` | Enum/String | `auto` |  |
| `jestercat` | Enum/String | `auto` |  |
| `junkyard` | Block | `{ ... }` |  |
| `jurassic` | Block | `{ ... }` |  |
| `lab` | Block | `{ ... }` |  |
| `large` | Array | `[ KillDozer ], [ ], [ Shambler ]` |  |
| `lenny` | Enum/String | `auto` |  |
| `level` | Enum/String | `Treasure_LargeMeteor, TreasureHard, Treasure_SmallMeteor` |  |
| `lightningelemental` | Enum/String | `auto` |  |
| `locked` | Boolean | `true` |  |
| `magecat` | Enum/String | `auto` |  |
| `mamamaggot` | Enum/String | `auto` |  |
| `meatworld` | Block | `{ ... }` |  |
| `medium` | Array | `[ Rat Leaper Pooter Kitten TomTom Mangy CatCaller ], [ AtomicKitten RoboTom CatCultist Cultist CultistZealot C..., [ ZombieCat SkeletonCat TallSkeletonCat WolfCat Tatters S...` |  |
| `miniboss_event` | Block | `{ ... }` |  |
| `miniboss` | Array | `[ miniboss ]` |  |
| `monkcat` | Enum/String | `auto` |  |
| `moon` | Block | `{ ... }` |  |
| `musiclayer` | Enum/String | `boss` |  |
| `mw_altar` | Block | `{ ... }` |  |
| `mw_battle1` | Block | `{ ... }` |  |
| `mw_boss` | Block | `{ ... }` |  |
| `mw_earlyhome` | Block | `{ ... }` |  |
| `mw_event1` | Block | `{ ... }` |  |
| `mw_hard1` | Block | `{ ... }` |  |
| `mw_home` | Block | `{ ... }` |  |
| `mw_quest_event` | Block | `{ ... }` |  |
| `mw_treasure` | Block | `{ ... }` |  |
| `necrocat` | Enum/String | `auto` |  |
| `nemesis` | Array | `[ nemesis ]` |  |
| `normal` | Array | `[ common alley_events.gon ], [ common boneyard_events.gon ], [ common bunker_events.gon ]` |  |
| `override_art` | Enum/String | `MapNode_SmallMeteor, Rare_Treasure, MapNode_LargeMetor` |  |
| `psychiccat` | Enum/String | `auto` |  |
| `queenhippo` | Enum/String | `auto` |  |
| `quest_event` | Block | `{ ... }` |  |
| `radicalrat` | Enum/String | `auto` |  |
| `rare` | Array | `[ rare ]` |  |
| `ratking` | Enum/String | `auto` |  |
| `repeat` | Enum/String | `never` |  |
| `rockybobo` | Enum/String | `auto` |  |
| `sewers` | Block | `{ ... }` |  |
| `shop_cheapwater` | Block | `{ ... }` |  |
| `shop_water` | Block | `{ ... }` |  |
| `slime` | Enum/String | `auto` |  |
| `small` | Array | `[ Maggot Fly Flea Pinky ], [ ], [ Flea Wisp Fly Maggot ]` |  |
| `spawn_node` | Enum/String | `start` |  |
| `special` | Array | `[ special ]` |  |
| `spewer` | Enum/String | `auto` |  |
| `stacy` | Enum/String | `auto` |  |
| `start` | Block | `{ ... }` |  |
| `tankcat` | Enum/String | `auto` |  |
| `thebloat` | Enum/String | `auto` |  |
| `theend` | Block | `{ ... }` |  |
| `thiefcat` | Enum/String | `auto` |  |
| `time_machine` | Block | `{ ... }` |  |
| `tinkerercat` | Enum/String | `auto` |  |
| `trampy` | Enum/String | `auto` |  |
| `treasure` | Block | `{ ... }` |  |
| `type` | Enum/String | `battle, empty, npc` | Classification type. |
| `weather_event` | Block | `{ ... }` |  |
| `zodiac` | Enum/String | `auto` |  |

### Context: `BoneyardUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `BothObelisksUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `BunkerUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `CavesUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `ChaosAntennaAttached`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `CoreObeliskUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `CoreUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `CraterUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit1` | Block | `{ ... }` |  |

### Context: `DimensionXUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `EndOfTimeUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `FutureUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `GenFlag_Boss_Spewer`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `boss` | Block | `{ ... }` |  |

### Context: `GenFlag_Boss_Stacy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `boss` | Block | `{ ... }` |  |
| `miniboss_event` | Block | `{ ... }` |  |

### Context: `HardPathUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hard_initial` | Block | `{ ... }` |  |

### Context: `IceAgeUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `JunkyardUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit1` | Block | `{ ... }` |  |

### Context: `JurassicUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `MeatWorldUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |
| `quest_event` | Block | `{ ... }` |  |

### Context: `MeatWorldUnlockedFull`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `mw_battle1` | Block | `{ ... }` |  |
| `mw_boss` | Block | `{ ... }` |  |
| `mw_earlyhome` | Block | `{ ... }` |  |
| `mw_event1` | Block | `{ ... }` |  |
| `mw_hard1` | Block | `{ ... }` |  |
| `mw_home` | Block | `{ ... }` |  |
| `mw_quest_event` | Block | `{ ... }` |  |
| `mw_treasure` | Block | `{ ... }` |  |

### Context: `MoonObeliskUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `MoonUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `SewersUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `TheEndUnlocked`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exit0` | Block | `{ ... }` |  |

### Context: `ThrobbingArteryDone`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `VolcanoAntennaAttached`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `WallOfFleshDone`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `quest_event` | Block | `{ ... }` |  |

### Context: `battle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `type` | Enum/String | `battle` | Classification type. |

### Context: `boss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `boss_cutscene` | Enum/String | `dybbuk, johnny, spiderkitten` |  |
| `is_final_boss` | Boolean | `true` |  |
| `level` | Enum/String | `stacy, spewer` |  |
| `override_music` | Enum/String | `chaos_boss, finalboss` |  |
| `tileset` | Enum/String | `finalboss` |  |
| `type` | Enum/String | `boss` | Classification type. |
| `unlockcheck_on_complete` | Enum/String | `map_unlock_junkyard` |  |

### Context: `dimensionx`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

### Context: `endoftime`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

### Context: `event`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `Butch_Tutorial` |  |
| `type` | Enum/String | `event` | Classification type. |

### Context: `exit0`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `locked` | Boolean | `false, true` |  |
| `next_map` | Enum/String | `meatworld.gon, core.gon, sewers.gon` |  |
| `override_art` | Enum/String | `MapNodeExit_MeatWorld, MapNodeExit_Core, MapNodeExit_Sewers` |  |
| `type` | Enum/String | `exit` | Classification type. |

### Context: `exit1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `next_map` | Enum/String | `crater.gon, junkyard.gon, future.gon` |  |
| `override_art` | Enum/String | `MapNodeExit_Future, MapNodeExit_Junkyard, MapNodeExit_Crater` |  |
| `type` | Enum/String | `exit` | Classification type. |

### Context: `exit_desert`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `locked` | Boolean | `true` |  |
| `next_map` | Enum/String | `desert.gon` |  |
| `override_art` | Enum/String | `MapNodeExit_Desert` |  |
| `type` | Enum/String | `exit` | Classification type. |

### Context: `exit_lab`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `locked` | Boolean | `true` |  |
| `next_map` | Enum/String | `lab.gon` |  |
| `override_art` | Enum/String | `MapNodeExit_Lab` |  |
| `type` | Enum/String | `exit` | Classification type. |

### Context: `future`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

### Context: `hard_initial`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `type` | Enum/String | `hard` | Classification type. |

### Context: `home`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `type` | Enum/String | `home` | Classification type. |

### Context: `iceage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

### Context: `jurassic`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

### Context: `miniboss_event`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `StacyMutant1` |  |
| `type` | Enum/String | `special_event, empty` | Classification type. |

### Context: `mw_altar`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `Quest_MeatWorldAltar` |  |
| `override_art` | Enum/String | `MapNode_MeatAltar` |  |
| `type` | Enum/String | `special_event` | Classification type. |

### Context: `mw_battle1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | Enum/String | `battle` | Classification type. |

### Context: `mw_boss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `boss_cutscene` | Enum/String | `throbbingking` |  |
| `hidden` | Boolean | `false, true` |  |
| `override_music` | Enum/String | `throbbingking` |  |
| `type` | Enum/String | `boss` | Classification type. |

### Context: `mw_earlyhome`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `type` | Enum/String | `home` | Classification type. |

### Context: `mw_event1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | Enum/String | `event` | Classification type. |

### Context: `mw_hard1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `musiclayer` | Enum/String | `boss` |  |
| `type` | Enum/String | `hard` | Classification type. |

### Context: `mw_home`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | Enum/String | `home` | Classification type. |

### Context: `mw_quest_event`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `level` | Enum/String | `Quest_DeadKing` |  |
| `override_art` | Enum/String | `MapNode_DeadKing` |  |
| `type` | Enum/String | `special_event` | Classification type. |

### Context: `mw_treasure`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | Enum/String | `treasure` | Classification type. |

### Context: `quest_event`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `Quest_ThrobbingArtery2, Quest_ThrobbingArtery, Quest_WallOfFlesh` |  |
| `override_art` | Enum/String | `MapNode_VeinsDrained, MapNode_Veins, MapNode_Empty` |  |
| `type` | Enum/String | `special_event, empty` | Classification type. |

### Context: `shop_cheapwater`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `WaterShopCheap` |  |
| `override_art` | Enum/String | `cheapwatershop` |  |
| `type` | Enum/String | `shop` | Classification type. |

### Context: `shop_water`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `WaterShop` |  |
| `override_art` | Enum/String | `cheapwatershop` |  |
| `type` | Enum/String | `shop` | Classification type. |

### Context: `start`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `type` | Enum/String | `enter` | Classification type. |

### Context: `theend`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

### Context: `time_machine`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `Quest_TimeMachineIceAge, Quest_TimeMachineFuture, Quest_TimeMachineJurassic` |  |
| `override_art` | Enum/String | `MapNode_TimeMachine` |  |
| `type` | Enum/String | `special_event` | Classification type. |

### Context: `treasure`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `TreasureTutorial` |  |
| `type` | Enum/String | `treasure` | Classification type. |

### Context: `weather_event`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `level` | Enum/String | `CraterWeatherEvent` |  |
| `type` | Enum/String | `special_event` | Classification type. |

---

## Passives & Statuses

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `auto_plus_signs_on_name` | Boolean | `false` |  |
| `bonus_items` | Array | `[ Eyeball ]` | Flat addition to a base value. |
| `class` | Enum/String | `Colorless, Butcher, Disorder` | Character class identifier. |
| `desc_multiclass` | String | `"PASSIVE_BARBED_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK_MULTICLASS_DESC", "PASSIVE_HOOKED_MULTICLASS_DESC"` |  |
| `desc` | String | `"PASSIVE_MAINCOURSE_DESC", "PASSIVE_NEVERFULL_DESC", "PASSIVE_PUTREFY_DESCRIPTION"` | Localization key for the passive's display description. |
| `grant_ability` | Enum/String | `Rest` |  |
| `lock_item_slot` | Block | `{ ... }` |  |
| `name_mod` | String | `"CAT_NAME_MOD_GIGANTISM", "CAT_NAME_MOD_DWARF", "CAT_NAME_MOD_VEGAN"` |  |
| `name` | String | `"PASSIVE_NEVERFULL_NAME", "PASSIVE_PUTREFY_NAME", "PASSIVE_MAINCOURSE_NAME"` | Localization key for the passive's display name. |
| `override_basic_attack` | Enum/String | `BasicMelee, GerdShot` |  |
| `passives` | Block | `{ ... }` |  |
| `shield` | Number | `8, 4` |  |
| `stats` | Block | `{ ... }` |  |
| `tags` | Array | `[ noncopyable ]` |  |

### Context: `1`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bonus_items` | Array | `[ SpiderEgg ], [ Stick Stick Stick ], [ Pipe ]` | Flat addition to a base value. |
| `desc` | String | `"DISORDER_DEJAVU_DESC"` | Localization key for the passive's display description. |
| `divine_shield` | Number | `1` |  |
| `empty_armor_scaled_stats` | Block | `{ ... }` |  |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear when hovering over the ability. |
| `override_basic_attack` | Enum/String | `BasicDruidAbilityVersatile, BasicButcherMeleeWideSpin, BasicMagicMissile` |  |
| `passives` | Block | `{ ... }` |  |
| `schadenfreude_scaled_stats` | Block | `{ ... }` |  |
| `shield` | Number | `2, 4` |  |
| `stats` | Block | `{ ... }` |  |

### Context: `10`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"DISORDER_DISTEMPERMAX_DESC"` | Localization key for the passive's display description. |
| `passives` | Block | `{ ... }` |  |

### Context: `2`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `bonus_items` | Array | `[ Stick Stick Stick ], [ FoodBig FoodBig FoodBig FoodBig ], [ SpiderWebber ]` | Flat addition to a base value. |
| `desc_multiclass` | String | `"PASSIVE_BARBED2_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC", "PASSIVE_HOOKED2_MULTICLASS_DESC"` |  |
| `desc` | String | `"PASSIVE_PUTREFY2_DESCRIPTION", "PASSIVE_NEVERFULL2_DESC", "PASSIVE_MAINCOURSE2_DESC"` | Localization key for the passive's display description. |
| `divine_shield` | Number | `1, 3` |  |
| `empty_armor_scaled_stats` | Block | `{ ... }` |  |
| `icon` | Enum/String | `DejaVu2` |  |
| `keyword_tooltips` | Block | `{ ... }` | Forces specific UI tooltips to appear when hovering over the ability. |
| `override_basic_attack` | Enum/String | `BasicDruidAbilityVersatile, BasicButcherMeleeWideDoubleSpin, BasicMagicMissile` |  |
| `passives` | Block | `{ ... }` |  |
| `schadenfreude_scaled_stats` | Block | `{ ... }` |  |
| `shield` | Number | `8, 4` |  |
| `stats` | Block | `{ ... }` |  |

### Context: `3`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"DISORDER_SEVEREDEJAVU_DESC"` | Localization key for the passive's display description. |
| `icon` | Enum/String | `DejaVu3` |  |
| `name` | String | `"DISORDER_SEVEREDEJAVU_NAME"` | Localization key for the passive's display name. |
| `passives` | Block | `{ ... }` |  |

### Context: `4`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |  |

### Context: `5`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |  |

### Context: `6`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |  |

### Context: `7`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |  |

### Context: `8`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |  |

### Context: `9`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |  |

### Context: `AbilityChargeRefundChance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number | `3.5` |  |
| `chance` | Number | `50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

### Context: `AbilityReaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |  |
| `ability` | Enum/String | `SpontaneouslyCombust` | The ID of the ability to trigger or reference. |
| `chance` | Number | `15%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

### Context: `AbilityWhenTaggedCharacterMovesNear`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `move` | The ID of the ability to trigger or reference. |
| `range` | Enum/String | `global, 2` | Distance or area of effect in tiles. |
| `tag` | Enum/String | `food` | The specific entity tag required or applied. |

### Context: `AddDamageToElementDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1, 2` | The base damage properties of an attack. |
| `element` | Enum/String | `Fire, Electric` | The specific element type required or applied. |

### Context: `AddPassiveToSpawnedRocks`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | `7, 3` | Applies the 'AddFilledMaxHealth' effect. |
| `JoinSpawnerFaction` | Number | `1` | Applies the 'JoinSpawnerFaction' effect. |

### Context: `AddPassivesToCharmed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `5, 10` | Applies the 'AddMaxHealth' effect. |
| `AddSpeed` | Number | `4` | Applies the 'AddSpeed' effect. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `DamageUp` | Number | `2, 3` | Combat Trigger: Deals damage to up. |

### Context: `AddPassivesToMinions`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `5, 10` | Applies the 'AddMaxHealth' effect. |
| `AddSpeed` | Number | `4` | Applies the 'AddSpeed' effect. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `AddStatusToExplosions` | Block | `{ ... }` | Applies the 'AddStatusToExplosions' effect. |
| `AddUnfilledMaxHealth` | Number | `10` | Applies the 'AddUnfilledMaxHealth' effect. |
| `DamageUp` | Number | `2, 3` | Combat Trigger: Deals damage to up. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `EMP` | Block | `{ ... }` | Applies the 'EMP' effect. |
| `FamiliarBonusAbility` | Enum/String | `FamiliarSelfDestruct2, FamiliarSelfDestruct` | Applies the 'FamiliarBonusAbility' effect. |
| `ForceAttack` | Number | `1` | Forces the character to execute an immediate attack. |
| `FreePathfindElement` | Enum/String | `Water, Grass` | Applies the 'FreePathfindElement' effect. |
| `GrassTileHealing` | Number | `1` | Applies the 'GrassTileHealing' effect. |
| `HealthGain` | Number | `5, 10` | Applies the 'HealthGain' effect. |
| `HealthRegenUp` | Number | `3` | Applies the 'HealthRegenUp' effect. |
| `HolyShieldTransferToSpawner` | Number | `1` | Applies the 'HolyShieldTransferToSpawner' effect. |
| `IncreaseExplosionDamage` | Number | `2, 4, 3` | Applies the 'IncreaseExplosionDamage' effect. |
| `IncreaseExplosionSize` | Number | `2` | Applies the 'IncreaseExplosionSize' effect. |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` | State Trigger: Grants nested passives when affected by element. |
| `PoisonThorns` | Number | `1, 2` | Applies the 'PoisonThorns' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `SafeExplosions` | Number | `1` | Applies the 'SafeExplosions' effect. |
| `StatusAlliesOnKill` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies on kill. |
| `StatusOnKill` | Block | `{ ... }` | Event Trigger: Applies nested statuses when kill. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `UncappedHP` | Number | `1` | Applies the 'UncappedHP' effect. |
| `WaterWalk` | Number | `1` | Applies the 'WaterWalk' effect. |
| `tag_filter` | Enum/String | `crow` |  |

### Context: `AddPassivesToSummonAbilityMinions`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2, 4` | Combat Trigger: Deals damage to up. |
| `Doomed` | Number | `1` | Applies the 'Doomed' effect. |
| `MovementUp` | Number | `2, 4` | Applies the 'MovementUp' effect. |

### Context: `AddSelfStatusToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

### Context: `AddSelfStatusToWeapons`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ChanceToBreak` | Number | `50, 100` | Applies the 'ChanceToBreak' effect. |

### Context: `AddStatusToAllDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `Conditional_HasTag` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `LeaveBehindRockOnKnockback` | Number | `1` | Applies the 'LeaveBehindRockOnKnockback' effect. |
| `NonLethal` | Number | `1` | Applies the 'NonLethal' effect. |

### Context: `AddStatusToAllDamageAbilities`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Piercing` | Number | `1` | Applies the 'Piercing' effect. |
| `Weakness` | Number | `2` | Applies the 'Weakness' effect. |

### Context: `AddStatusToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyStatusIfCrit` | Block | `{ ... }` | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BigSplashDamage` | Number | `2` | Applies the 'BigSplashDamage' effect. |
| `Bleed` | Number | `1, 2` | Applies the 'Bleed' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `BounceObject` | Enum/String | `BeefyCharmedLeech, CharmedLeech, AllyRotFly` | Spawns a physics object that visually bounces off the target. |
| `Bruise` | Number | `1, 2` | Applies the 'Bruise' effect. |
| `BurgleCoin` | Number | `1` | Applies the 'BurgleCoin' effect. |
| `Burn` | Number | `5, 1, 2` | Applies the 'Burn' effect. |
| `ChangeTile` | Enum/String | `BrambleTile, { ... }` | Transforms the terrain tile under the target. |
| `Charmed` | Array | `[ 1 .25 ]` | Applies the 'Charmed' effect. |
| `Conditional_Adjacent` | Block | `{ ... }` | Conditional block: Executes nested logic only if the target is/has Adjacent. |
| `Conditional_Ally` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `Conditional_Enemy` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `Conditional_HasTag` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Conditional_Shielded` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has a Shield status. |
| `Conditional_SourceHasTag` | Block | `{ ... }` | Conditional block: Executes nested logic only if the target is/has SourceHasTag. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `DamageOrHealConditionally` | Number | `1` | Combat Trigger: Deals damage to or heal conditionally. |
| `DistanceBonusDamage` | Block | `{ ... }` | Applies the 'DistanceBonusDamage' effect. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Fear` | Array | `[ 1 .25 ]` | Applies the 'Fear' effect. |
| `Freeze` | Array | `[ 1 .5 ], [ 1 .20 ]` | Applies the 'Freeze' effect. |
| `KnockOutCoin` | Number | `1, [ 1 .5 ]` | Forces the target to drop coins. |
| `Knockback` | Number | `1, 4, 3` | Applies the 'Knockback' effect. |
| `Leech` | Number | `1` | Applies the 'Leech' effect. |
| `Leeches` | Number | `1` | Applies the 'Leeches' effect. |
| `LuckUp` | Number | `-1` | Applies the 'LuckUp' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `1, 2` | Applies the 'MagicWeakness' effect. |
| `ManaLeeches` | Number | `1` | Applies the 'ManaLeeches' effect. |
| `OverrideChainKnockbackDamage` | Number | `0` | Applies the 'OverrideChainKnockbackDamage' effect. |
| `OverrideChainKnockback` | Number | `0` | Applies the 'OverrideChainKnockback' effect. |
| `Piercing` | Number | `1` | Applies the 'Piercing' effect. |
| `Poison` | Number | `1, 3, [ 1 .5 ]` | Applies the 'Poison' effect. |
| `Rot` | Number | `1, -999999` | Applies the 'Rot' effect. |
| `Slow` | Number | `5, 1, 2` | Applies the 'Slow' effect. |
| `SoulLink` | Number | `1` | Applies the 'SoulLink' effect. |
| `SpawnBearTrapOnMiss` | Number | `1` | Applies the 'SpawnBearTrapOnMiss' effect. |
| `SplashDamage` | Number | `2` | Applies the 'SplashDamage' effect. |
| `SpreadDisease` | Block | `{ ... }` | Provides a chance to transmit a disease status to adjacent targets. |
| `Stun` | Array | `[ 1 .40 ], [ 1 .15 ]` | Applies the 'Stun' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

### Context: `AddStatusToBasicAttackWithCooldown`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | Number | `1` | Applies the 'CharmedForceAttack' effect. |

### Context: `AddStatusToBasicMeleeAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `FaceAway` | Number | `1` | Applies the 'FaceAway' effect. |
| `SpreadDisease` | Block | `{ ... }` | Provides a chance to transmit a disease status to adjacent targets. |
| `Stun` | Array | `[ 1 .15 ], [ 1 .2 ]` | Applies the 'Stun' effect. |

### Context: `AddStatusToElementAbilities`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `ChangeTile` | Enum/String | `FloatingGlassTile` | Transforms the terrain tile under the target. |
| `Conditional_Ally` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `Conditional_Enemy` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `element` | Enum/String | `Gravity` | The specific element type required or applied. |

### Context: `AddStatusToElementDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `1, 3` | Applies the 'Burn' effect. |
| `Conditional_Corpse` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| `element` | Enum/String | `Fire, Electric` | The specific element type required or applied. |

### Context: `AddStatusToExplosions`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddElement` | Enum/String | `Napalm, Fire` | Applies the 'AddElement' effect. |
| `Burn` | Number | `6, 3` | Applies the 'Burn' effect. |

### Context: `AddStatusToFirstBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `5` | Applies the 'Charmed' effect. |

### Context: `AddStatusToKnockbackDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |

### Context: `AddStatusToMeleeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DelayedWindCone` | Block | `{ ... }` | Creates a delayed Area of Effect cone. |
| `DelayedWind` | Block | `{ ... }` | Applies the 'DelayedWind' effect. |

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_DoesDamage` | Block | `{ ... }` | Conditional block: Executes nested logic only if the target is/has DoesDamage. |

### Context: `AddStatusToSpells`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `LeechPercent` | Number | `50` | Applies the 'LeechPercent' effect. |

### Context: `AddStatusToTrampleDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |

### Context: `AddStatusToWeapons`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `LeechPercent` | Number | `50` | Applies the 'LeechPercent' effect. |
| `PullSourceToKnockbackImmuneTarget` | Number | `1` | Applies the 'PullSourceToKnockbackImmuneTarget' effect. |

### Context: `AddStatusesIfPersistentWeatherElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `3` | Applies the 'Burn' effect. |
| `elements` | Array | `[ Heat Fire ]` |  |

### Context: `AddStatusesToReceivedElementalDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `3` | Applies the 'Burn' effect. |
| `elements` | Array | `[ Heat Fire ]` |  |

### Context: `AddTemporaryEffectsToBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | `1, 2` | Applies the 'CastAgain' effect. |
| `Fury` | Number | `75` | Applies the 'Fury' effect. |

### Context: `AddTemporaryEffectsToEquipment`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | `1` | Applies the 'CastAgain' effect. |

### Context: `AllyBonusAbilityAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `Bowl, Bowl2` | The ID of the ability to trigger or reference. |
| `square` | Boolean | `true` |  |

### Context: `AllyHealthRegenAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `range` | Enum/String | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `1, 2` | The number of stacks, duration, or intensity to apply. |

### Context: `AllyManaRegenAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `range` | Enum/String | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `1, 2` | The number of stacks, duration, or intensity to apply. |

### Context: `AlternateCraftingPools`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `tinkerer_0` | Enum/String | `tinkerer_0_bombs` |  |
| `tinkerer_1` | Enum/String | `tinkerer_1_bombs` |  |

### Context: `AmplifyStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number | `2` |  |
| `status` | Enum/String | `Burn, Poison, Bleed` | The ID of the status effect to check or apply. |

### Context: `ApplyStatusIfCrit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Purge` | Number | `0` | Applies the 'Purge' effect. |

### Context: `ApplyStatusesToRandomEnemiesEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | `1, 3` | Applies the 'Bounty' effect. |
| `count` | Number | `2` | The numerical quantity. |

### Context: `ApplyToSource`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `Shield` | Number | `1` | Applies the 'Shield' effect. |

### Context: `Autism`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `innate` | Number | `-2` |  |
| `learned` | Number | `1` |  |

### Context: `AutocastEachRound`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `MedicObey, RaiseTheDead, MedicObey2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |
| `force_display_name` | Boolean | `true` |  |

### Context: `AutocastEachTurnBegin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `PoxScratch` | The ID of the ability to trigger or reference. |
| `advantage_polarity` | Number | `-1` |  |
| `chance` | Number | `10%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

### Context: `BoobyTrapItems`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `on_break` | Block | `{ ... }` |  |
| `on_throw` | Block | `{ ... }` |  |

### Context: `BoostWeaponDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Enum/String | `.25, .5` |  |
| `damage` | Number | `2, 3` | The base damage properties of an attack. |

### Context: `BouncyProjectiles`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | `1, 2` |  |
| `max_range` | Number | `4, 3` |  |

### Context: `CatAPultAnimation`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `CatapultJump2, CatapultJump` | The ID of the ability to trigger or reference. |
| `animation` | Enum/String | `knockupatk` |  |

### Context: `CatchProjectiles`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `ally_chance` | Number | `100%` |  |
| `chance` | Number | `33%, 50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

### Context: `ChanceToBackflip`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `BlinkDodge` | The ID of the ability to trigger or reference. |
| `chance` | Number | `33%, 50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

### Context: `ChanceToRevive`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `33` | The number of stacks, duration, or intensity to apply. |
| `statuses` | Block | `{ ... }` |  |

### Context: `ChangeTile`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | `1` | The area of effect or distance in tiles. |
| `tile` | Enum/String | `BrambleTile` | The specific tile type to change into (e.g., GlassTile). |

### Context: `ClassManaCostReduction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `class` | Enum/String | `Colorless` | Character class identifier. |
| `reduction` | Number | `1, 2` |  |

### Context: `CollectPickupsOnBattleEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean | `true` |  |

### Context: `Conditional_Adjacent`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1, 2` | Applies the 'Bleed' effect. |
| `BonusCritChance` | Number | `25, 50` | Applies the 'BonusCritChance' effect. |
| `BonusDamage` | Number | `2, 3` | Applies the 'BonusDamage' effect. |

### Context: `Conditional_Ally`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, [ 1 .5 ]` | Applies the 'AllStatsUp' effect. |
| `ApplyToSource` | Block | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |
| `ClearNegativeEffects` | Number | `1` | Applies the 'ClearNegativeEffects' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |
| `TempSpeedUp` | Number | `4` | Applies the 'TempSpeedUp' effect. |

### Context: `Conditional_BadRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `odds` | Enum/String | `.1` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

### Context: `Conditional_Boss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `Stun` | Number | `3` | Applies the 'Stun' effect. |

### Context: `Conditional_Corpse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `DamageUp` | Number | `2` | Combat Trigger: Deals damage to up. |
| `OverrideDamage` | Number | `0` | Applies the 'OverrideDamage' effect. |
| `Revive` | Number | `1` | Applies the 'Revive' effect. |
| `SafeDoomed` | Number | `1` | Applies the 'SafeDoomed' effect. |
| `SpeedUp` | Number | `8` | Applies the 'SpeedUp' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |

### Context: `Conditional_DoesDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Array | `[ 1 .1 ]` | Applies the 'Bleed' effect. |

### Context: `Conditional_Enemy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_PartyMember` | Block | `{ ... }` | Conditional block: Executes nested logic only if the target is/has PartyMember. |
| `Confusion` | Number | `2, 3` | Applies the 'Confusion' effect. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `Stun` | Array | `[ 1 .5 ]` | Applies the 'Stun' effect. |

### Context: `Conditional_FirstApplicationThisTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `FillMana` | Number | `1` | Applies the 'FillMana' effect. |
| `ManaGain` | Number | `5` | Applies the 'ManaGain' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |

### Context: `Conditional_GoodRoll`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `UseRandomSpell_Madness` | Number | `1` | Applies the 'UseRandomSpell_Madness' effect. |
| `odds` | Number | `33%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

### Context: `Conditional_HasStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `status` | Enum/String | `Marked, Fear` | The specific status ID to check for. |

### Context: `Conditional_HasTag`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `FlatLeechIfDamaged` | Number | `5` | Applies the 'FlatLeechIfDamaged' effect. |
| `tag` | Enum/String | `poop, rat` | The specific string tag to check for. |

### Context: `Conditional_NotBoss`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Enemy` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is hostile to the caster. |

### Context: `Conditional_PartyMember`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `5` | Applies the 'Charmed' effect. |

### Context: `Conditional_Shielded`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` | Applies the 'BonusCritChance' effect. |

### Context: `Conditional_SourceHasTag`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Ally` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `tag` | Enum/String | `crow` | The specific entity tag required or applied. |

### Context: `Craft`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Enum/String | `tinkerer_default` |  |
| `slot` | Enum/String | `random_empty_armor_or_weapon` |  |

### Context: `CritsApplyStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Conditional_HasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |
| `ObjectOnHitCharacter` | Enum/String | `Coin, RandomPickup` | Spawns a specific character or entity upon impact. |
| `Stun` | Number | `1, [ 1 .33 ], [ 1 .25 ]` | Applies the 'Stun' effect. |
| `Weakness` | Number | `1, 2` | Applies the 'Weakness' effect. |

### Context: `CureDisease`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `can_apply_to_anything` | Boolean | `true` |  |
| `chance` | Number | `5%, 15%, 30%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `disease` | Enum/String | `CommonCold, Pox, Ebola` |  |

### Context: `DamageIfDidntUseSpecificAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `Groom` | The ID of the ability to trigger or reference. |
| `damage` | Number | `2` | The base damage properties of an attack. |

### Context: `DamageNeighborTilesWhenCastSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `fire` | Block | `{ ... }` |  |
| `ice` | Block | `{ ... }` |  |
| `lightning` | Block | `{ ... }` |  |
| `triattack` | Block | `{ ... }` |  |

### Context: `DamageNeighborsAfterMove`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Enum/String | `X` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Electric ]` |  |
| `type` | Enum/String | `spell` | The classification type (e.g., damage type or element). |

### Context: `DamageNeighborsOnEndMove`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `knockback` | Number | `1` |  |
| `type` | Enum/String | `status` | The classification type (e.g., damage type or element). |

### Context: `DamageReductionAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `range` | Enum/String | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `1, 2` | The number of stacks, duration, or intensity to apply. |

### Context: `DeathRattle`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `LastGasp2, LastGasp` | The ID of the ability to trigger or reference. |
| `pop_corpse` | Boolean | `false` |  |

### Context: `DelayedWind`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `2` | The area of effect or distance in tiles. |

### Context: `DelayedWindCone`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `10` | The area of effect or distance in tiles. |

### Context: `Diabetes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1` | Applies the 'AllStatsUp' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |

### Context: `DistanceBonusDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `min_range` | Number | `1, 3` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

### Context: `EMP`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `spell_graphics_override` | Block | `{ ... }` |  |
| `status_explosion_override` | Enum/String | `WaterConduct` |  |

### Context: `Earth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Enum/String | `X` | The base damage properties of an attack. |

### Context: `Electric`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Stun` | Array | `[ 1 .1*X ]` | Applies the 'Stun' effect. |

### Context: `ElementalAttunement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Earth` | Block | `{ ... }` | Applies the 'Earth' effect. |
| `Electric` | Block | `{ ... }` | Applies the 'Electric' effect. |
| `Fire` | Block | `{ ... }` | Applies the 'Fire' effect. |
| `Grass` | Block | `{ ... }` | Applies the 'Grass' effect. |
| `Gravity` | Block | `{ ... }` | Applies the 'Gravity' effect. |
| `Holy` | Block | `{ ... }` | Applies the 'Holy' effect. |
| `Ice` | Block | `{ ... }` | Applies the 'Ice' effect. |
| `Shadow` | Block | `{ ... }` | Applies the 'Shadow' effect. |
| `Water` | Block | `{ ... }` | Applies the 'Water' effect. |
| `Wind` | Block | `{ ... }` | Applies the 'Wind' effect. |

### Context: `ElementalManaCostReduction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Gravity, [ Fire Ice Electric Earth Wind Water Grass Holy Gravity ]` | The specific element type required or applied. |
| `reduction` | Number | `1, 2` |  |

### Context: `Else`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` | Applies the 'CaptureFamiliar' effect. |
| `FactionConversion` | Number | `1` | Applies the 'FactionConversion' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `PermanentCharm` | Number | `1` | Applies the 'PermanentCharm' effect. |
| `TempSpeedUp` | Number | `4` | Applies the 'TempSpeedUp' effect. |

### Context: `EnergyStorm`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | `2` |  |
| `period` | Number | `3` |  |

### Context: `EscapeSequence`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | Number | `20` | Displaces the target by a randomized distance. |
| `SafeExplosionIfHitSomething` | Number | `5, 10` | Applies the 'SafeExplosionIfHitSomething' effect. |

### Context: `Eternal`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `health_percent` | Number | `50%` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

### Context: `ExtraStatusWhenDealingDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Ally` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |

### Context: `FindItemFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Enum/String | `.5` | Probability of finding the item. |
| `pool` | Enum/String | `pills` | The item pool to draw from. |

### Context: `Fire`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Enum/String | `X` | Applies the 'Burn' effect. |

### Context: `ForceMoveAway`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `free` | Boolean | `false` |  |

### Context: `ForceUseAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `DysenteryPoop, CrohnsPoop, TigerForm` | The ID of the ability to trigger or reference. |
| `chance` | Enum/String | `.2, 33%, .5` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

### Context: `FurnitureStats`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | `1` | Applies the 'Appeal' effect. |
| `Comfort` | Number | `1` | Applies the 'Comfort' effect. |
| `Stimulation` | Number | `1` | Applies the 'Stimulation' effect. |

### Context: `Grass`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Enum/String | `X` | Applies the 'Poison' effect. |

### Context: `Gravity`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Weakness` | Enum/String | `X` | Applies the 'Weakness' effect. |

### Context: `GravityWell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `5, 0` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Gravity ]` |  |
| `type` | Enum/String | `status` | The classification type (e.g., damage type or element). |

### Context: `HealAlliesEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean | `false` |  |
| `mana` | Number | `2, 3` |  |
| `stacks` | Number | `2, 3` | The number of stacks, duration, or intensity to apply. |

### Context: `Holy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FlatLeech` | Enum/String | `X` | Applies the 'FlatLeech' effect. |

### Context: `HolyDamageBlessing`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `2, 3` | Applies the 'Burn' effect. |
| `damage_multiplier` | Number | `2, 3` |  |

### Context: `Ice`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Slow` | Enum/String | `X` | Applies the 'Slow' effect. |

### Context: `InfiniteRebirth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `TempSpeedUp` | Number | `10` | Applies the 'TempSpeedUp' effect. |
| `health` | Number | `1, 25%` |  |
| `playercat_health` | Number | `100%` |  |

### Context: `LateBloomer`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |
| `stacks` | Number | `5, 3` | The number of stacks, duration, or intensity to apply. |

### Context: `LightningRod`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |

### Context: `LowHealthAllyDodgeChanceAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `theshold` | Number | `5` |  |

### Context: `ManaCostReductionTagged`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | `1, 3, 50%` |  |
| `tag` | Enum/String | `musical, summon` | The specific entity tag required or applied. |

### Context: `MegaMinions`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | `3` |  |
| `stacks` | Number | `3` | The number of stacks, duration, or intensity to apply. |

### Context: `MeleeRevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `3` | Applies the 'Poison' effect. |
| `SpreadDisease` | Block | `{ ... }` | Provides a chance to transmit a disease status to adjacent targets. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |
| `damage` | Number | `1, 0, 3` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Ice ], [ Fire ]` |  |

### Context: `MoveTowardsDamageSource`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | Enum/String | `move, TrampleMoveOne, TrampleMove` |  |
| `move_far` | Boolean | `false` |  |

### Context: `MoveWhenDamaged`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | Enum/String | `stay_far_always_move` |  |

### Context: `MovementReaction`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `weapon` | The ID of the ability to trigger or reference. |
| `enemies_only` | Boolean | `true` |  |

### Context: `NextBattleStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |

### Context: `ObjectOnHitCharacter`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `CharmedFlea` | The entity ID of the character to spawn (e.g., CharmedFlea). |
| `stacks` | Number | `1, 2` | The number of stacks, duration, or intensity to apply. |

### Context: `PassiveAfterXKills`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | Block | `{ ... }` |  |
| `stacks` | Number | `3` | The number of stacks, duration, or intensity to apply. |

### Context: `PassiveAtFullHealth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ManaCostReduction` | Number | `2` | Applies the 'ManaCostReduction' effect. |
| `TakeExtraDamage` | Number | `200%` | Applies the 'TakeExtraDamage' effect. |

### Context: `PassiveAtHealthThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal, equal` |  |
| `passives` | Block | `{ ... }` |  |
| `threshold` | Number | `1, 5` |  |

### Context: `PassiveAtInjuryThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `injury` | Enum/String | `spd` |  |
| `mode` | Enum/String | `greater_or_equal` |  |
| `passives` | Block | `{ ... }` |  |
| `threshold` | Number | `4` |  |

### Context: `PassiveAtStatThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | Enum/String | `less_or_equal` |  |
| `passives` | Block | `{ ... }` |  |
| `threshold` | Block | `{ ... }` |  |

### Context: `PassiveGroup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-2` | Applies the 'AllStatsUp' effect. |
| `CharismaUp` | Number | `5` | Applies the 'CharismaUp' effect. |
| `IntelligenceUp` | Number | `5` | Applies the 'IntelligenceUp' effect. |
| `SetDefaultFace` | Enum/String | `sad, happy` | Applies the 'SetDefaultFace' effect. |
| `SpeedUp` | Number | `5` | Applies the 'SpeedUp' effect. |

### Context: `PassiveIfAllArmorEmpty`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddSpellDamage` | Number | `1, 2` | Applies the 'AddSpellDamage' effect. |
| `CounterAttack` | Enum/String | `attack` | Applies the 'CounterAttack' effect. |
| `CritsApplyStatus` | Block | `{ ... }` | Applies the 'CritsApplyStatus' effect. |
| `ExtraMovePoints` | Number | `1` | Applies the 'ExtraMovePoints' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |
| `ManaCostReduction` | Number | `1` | Applies the 'ManaCostReduction' effect. |
| `StatusOnStanceSwitch` | Block | `{ ... }` | Event Trigger: Applies nested statuses when stance switch. |

### Context: `PassiveIfEmptyFace`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `40%, 25%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `StatusOnStanceSwitch` | Block | `{ ... }` | Event Trigger: Applies nested statuses when stance switch. |

### Context: `PassiveIfEmptyHead`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `40%, 25%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `StatusOnStanceSwitch` | Block | `{ ... }` | Event Trigger: Applies nested statuses when stance switch. |

### Context: `PassiveIfEmptyNeck`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `40%, 25%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `StatusOnStanceSwitch` | Block | `{ ... }` | Event Trigger: Applies nested statuses when stance switch. |

### Context: `PassiveLevelScaledStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | String | `"2*(X-1)"` | Applies the 'Shield' effect. |
| `SizeScalePercent` | String | `"sqrt(1.0+(.05*(X-1)))*100"` | Applies the 'SizeScalePercent' effect. |
| `Trample` | Array | `[ 3, X-8 ]` | Applies the 'Trample' effect. |

### Context: `PassiveUntilCastSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealAlliesEachTurn` | Block | `{ ... }` | Applies the 'HealAlliesEachTurn' effect. |
| `StatusAlliesEachTurn` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies each turn. |

### Context: `PassiveUntilGetKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HolyDamageBlessing` | Block | `{ ... }` | Applies the 'HolyDamageBlessing' effect. |

### Context: `PassiveWhenAffectedByElement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `water` | The specific element type required or applied. |
| `passives` | Block | `{ ... }` |  |

### Context: `PassiveWhenAtFullMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddMovement` | Number | `20` | Applies the 'AddMovement' effect. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `Brace` | Number | `2, 3` | Applies the 'Brace' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |
| `ReplaceBasicMove` | Enum/String | `Teleport` | Applies the 'ReplaceBasicMove' effect. |

### Context: `PassiveWhenTheAlpha`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | `1` | Applies the 'TogglableRoundEndExtraTurn' effect. |

### Context: `PassiveWhileInMonkMeleeStance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1, 2` | Applies the 'Brace' effect. |
| `HealthRegenUp` | Number | `2` | Applies the 'HealthRegenUp' effect. |

### Context: `PassiveWhileInMonkRangedStance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | `1, 2` | Applies the 'AddBonusRange' effect. |
| `AddSpellDamage` | Number | `2` | Applies the 'AddSpellDamage' effect. |
| `KineticSpikes` | Number | `2` | Applies the 'KineticSpikes' effect. |

### Context: `PassiveWhilePreviewingMonkRangedStance`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | `1, 2` | Applies the 'AddBonusRange' effect. |

### Context: `PassiveWhileWearingMetal`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AddElementsToWeapon` | Enum/String | `Electric` | Applies the 'AddElementsToWeapon' effect. |

### Context: `RandomPassivePool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `PassiveGroup` | Block | `{ ... }` | Applies the 'PassiveGroup' effect. |

### Context: `RandomStatusFromPool`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, -1` | Applies the 'AllStatsUp' effect. |
| `BleedThorns` | Number | `1` | Applies the 'BleedThorns' effect. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `Brace` | Number | `1` | Applies the 'Brace' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `Charge` | Number | `1` | Applies the 'Charge' effect. |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `ConstitutionUp` | Number | `1` | Applies the 'ConstitutionUp' effect. |
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
| `ObjectOnHitCharacter` | Enum/String | `BeefyCharmedLeech, CharmedLeech` | Spawns a specific character or entity upon impact. |
| `Petrify` | Number | `1` | Applies the 'Petrify' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `Reflect` | Number | `1` | Applies the 'Reflect' effect. |
| `Shield` | Number | `1` | Applies the 'Shield' effect. |
| `Sleep` | Number | `1` | Applies the 'Sleep' effect. |
| `Slow` | Number | `1` | Applies the 'Slow' effect. |
| `SpawnCoinAnywhere` | Number | `1` | Applies the 'SpawnCoinAnywhere' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |
| `StatusGroup` | Block | `{ ... }` | Groups multiple status effects together for batch application. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `Stun` | Number | `1` | Applies the 'Stun' effect. |
| `Tarred` | Number | `1` | Applies the 'Tarred' effect. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

### Context: `ReplaceBrain`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | Enum/String | `GenericBrain` |  |
| `decision_weights` | Enum/String | `default` |  |
| `move_weights` | Enum/String | `keep_distance` |  |

### Context: `RepressedMemoriesMetronome`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | Enum/String | `Jester, Psychic` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

### Context: `RevengeDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `knockback` | Number | `10` |  |

### Context: `Robot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | `true` |  |

### Context: `ScaledStatusOnBleedDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies the 'Charge' effect. |

### Context: `ScaledStatusOnLoseShield`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

### Context: `ScaledStatusOnOverHealed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | `1` | Applies the 'SpawnScaledRotFly' effect. |

### Context: `ScaledStatusOnOverMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

### Context: `ScaledStatusOnSpendMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RepressedMemoriesMetronome` | Block | `{ ... }` | Applies the 'RepressedMemoriesMetronome' effect. |

### Context: `SecurityBotProtect`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | Enum/String | `attack` | The ID of the ability to trigger or reference. |
| `move` | Enum/String | `move, MoveThree` |  |

### Context: `SelfDamageWhenDealDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1` | The base damage properties of an attack. |
| `type` | Enum/String | `status` | The classification type (e.g., damage type or element). |

### Context: `Shadow`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Enum/String | `.05*X` |  |

### Context: `SmiteEnemiesWhoKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `10` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Holy ]` |  |
| `type` | Enum/String | `spell` | The classification type (e.g., damage type or element). |

### Context: `SpawnCatCopyOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `object` | Enum/String | `PlayerCat_MiniMe, PlayerCat_MiniMiniMe` |  |
| `prevent_chain_tag` | Enum/String | `minime_clone` |  |

### Context: `SpawnEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `15%, .5, 50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `good` | Boolean | `false` |  |
| `number` | Number | `1` |  |
| `object` | Enum/String | `CharmedFlea, [ CharmedTumorousMaggot CharmedChargeyMaggot CharmedSwapp..., CharmedMaggot` |  |

### Context: `SpawnOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `number` | Number | `1, [ 2 3 ], 3` |  |
| `object` | Enum/String | `SmallRock, CharmedFlea, [ BuffFamiliarMaggot BuffFamiliarPooter BuffFamiliarFlea ...` |  |

### Context: `SpawnOnBattleStartRandomEmptyTile`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `number` | Array | `[ 2 3 ], 10, [ 1 2 ]` |  |
| `object` | Enum/String | `Coin, RandomPickup` |  |

### Context: `SpawnThingOnDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `consider_all_layers` | Boolean | `true` |  |
| `good` | Boolean | `false, true` |  |
| `object` | Enum/String | `Food, PoisonFood, CharmedLeech` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |

### Context: `SpecialFriends`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |

### Context: `SpreadDisease`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `can_apply_to_anything` | Boolean | `true` |  |
| `chance` | Number | `100%, 25%, 50%` | Probability (0.0 to 1.0 or percentage) of transmitting. |
| `disease` | Enum/String | `Pox, CommonCold, Rabies` | The specific status effect ID representing the disease. |

### Context: `StackingDodgeChanceOnTookDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | Number | `10%` | The numerical quantity. |
| `cap` | Number | `50%` |  |

### Context: `StatsAtLowHealth`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `speed` | Number | `6` |  |
| `strength` | Number | `6` |  |
| `threshold` | Number | `5` |  |

### Context: `StatusAdjacentOnTheirTurnBegin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Block | `{ ... }` | Applies the 'ForceMoveAway' effect. |

### Context: `StatusAfterCastSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `TempDamageUp` | Number | `1` | Applies the 'TempDamageUp' effect. |
| `TempSpellDamageUp` | Number | `1` | Applies the 'TempSpellDamageUp' effect. |

### Context: `StatusAlliesEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `3` | Applies the 'RandomStatUp' effect. |
| `exclude_self` | Boolean | `false` |  |

### Context: `StatusAlliesOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `EquipTemporaryItem` | Enum/String | `SleepDart2, SleepDart` | Applies the 'EquipTemporaryItem' effect. |

### Context: `StatusAlliesOnDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `Freeze` | Number | `1` | Applies the 'Freeze' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |
| `HealAndOverhealToShield` | Number | `12, 20` | Applies the 'HealAndOverhealToShield' effect. |
| `Reanimate` | Number | `33%, 100%` | Applies the 'Reanimate' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `triggers_limit` | Number | `1` |  |

### Context: `StatusAlliesOnGainCoins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |
| `scaled` | Boolean | `true` |  |

### Context: `StatusAlliesOnKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |

### Context: `StatusAlliesOnSpendMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `1` | Applies the 'ManaGain' effect. |

### Context: `StatusAlliesScaledByCursedOnDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |

### Context: `StatusAllyWhenAllySpendsMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `threshold` | Number | `7` |  |

### Context: `StatusAnyCatAllyWhoKills`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AlphaCat` | Number | `1` | Applies the 'AlphaCat' effect. |

### Context: `StatusDamagers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Array | `[ 1 .25 ]` | Applies the 'Fear' effect. |
| `LuckUp` | Number | `-1` | Applies the 'LuckUp' effect. |

### Context: `StatusEachTurnBegin`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_BadRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. |
| `Conditional_GoodRoll` | Block | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Fear` | Array | `[ 1 .15 ]` | Applies the 'Fear' effect. |
| `FillMana` | Array | `[ 1 .10 ], [ 1 .25 ]` | Applies the 'FillMana' effect. |
| `ForceUseAbility` | Block | `{ ... }` | Applies the 'ForceUseAbility' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `RandomStatUp` | Number | `2, 3` | Applies the 'RandomStatUp' effect. |

### Context: `StatusEachTurnEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `EmptyMana` | Number | `1` | Applies the 'EmptyMana' effect. |
| `ForceUseAbility` | Enum/String | `MiniFart, Rest, { ... }` | Applies the 'ForceUseAbility' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `NonStackingDivineShield` | Number | `1` | Applies the 'NonStackingDivineShield' effect. |
| `ObjectOnHitCharacter` | Block | `{ ... }` | Spawns a specific character or entity upon impact. |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |
| `RangeUp` | Number | `1` | Applies the 'RangeUp' effect. |
| `SpeedUp` | Number | `1, -2` | Applies the 'SpeedUp' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `UseAbility_Madness` | Enum/String | `weapon` | Applies the 'UseAbility_Madness' effect. |

### Context: `StatusEachTurnEndForEachTurn`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `2, 4` | Fires a randomized number of magic missiles. |

### Context: `StatusEachTurnEndPerEnemyKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitCharacter` | Block | `{ ... }` | Spawns a specific character or entity upon impact. |

### Context: `StatusEnemiesOnDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1, -2` | Applies the 'AllStatsUp' effect. |
| `Freeze` | Number | `2` | Applies the 'Freeze' effect. |

### Context: `StatusEveryXSpellCasts`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `ReduceManaCost` | Number | `1` | Applies the 'ReduceManaCost' effect. |
| `RepairWeaponCondition` | Number | `1` | Applies the 'RepairWeaponCondition' effect. |
| `RepairWeapon` | Number | `1` | Applies the 'RepairWeapon' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `stacks` | Number | `6, 3` | The number of stacks, duration, or intensity to apply. |

### Context: `StatusEveryXTurnBegins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `turns` | Number | `2, 3` | The duration of the effect in turns. |

### Context: `StatusGroup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | `2` | Applies the 'DexterityUp' effect. |
| `LuckUp` | Number | `2` | Applies the 'LuckUp' effect. |
| `SpawnCoinAnywhere` | Number | `1` | Applies the 'SpawnCoinAnywhere' effect. |
| `SpeedUp` | Number | `2` | Applies the 'SpeedUp' effect. |

### Context: `StatusIfBattleAlreadyBegan`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |

### Context: `StatusIfUnusedMovePoints`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1` | Applies the 'Brace' effect. |
| `ConstitutionUp` | Number | `2` | Applies the 'ConstitutionUp' effect. |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |
| `ManaGain` | Number | `5` | Applies the 'ManaGain' effect. |
| `MoveQuivered` | Number | `2` | Applies the 'MoveQuivered' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |

### Context: `StatusKilledCharacters`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number | `100%, 50%` | Applies the 'AutoReanimate' effect. |
| `Conditional_Ally` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |

### Context: `StatusKillers`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_Boss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is a Boss. |
| `Conditional_NotBoss` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target is NOT a Boss. |

### Context: `StatusOnAllyCatDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `FillMana` | Number | `1` | Applies the 'FillMana' effect. |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |
| `PercentHeal` | Number | `50` | Applies the 'PercentHeal' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |

### Context: `StatusOnAnyDeath`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |

### Context: `StatusOnBattleEnd`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CureDisease` | Block | `{ ... }` | Applies the 'CureDisease' effect. |
| `FindItemFromPool` | Enum/String | `consumables, chapter, { ... }` | Generates an item drop from the specified loot pool. |
| `NextBattleStatus` | Block | `{ ... }` | Applies the 'NextBattleStatus' effect. |
| `PermanentConstitution` | Number | `-1` | Applies the 'PermanentConstitution' effect. |
| `PermanentIntelligence` | Number | `-1` | Applies the 'PermanentIntelligence' effect. |
| `PermanentSpeed` | Number | `-1` | Applies the 'PermanentSpeed' effect. |
| `PermanentStrength` | Number | `2` | Applies the 'PermanentStrength' effect. |
| `RandomMutation` | Number | `1` | Applies the 'RandomMutation' effect. |
| `RandomPermanentStat` | Number | `1, -3, 3` | Applies the 'RandomPermanentStat' effect. |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |

### Context: `StatusOnBattleEndIfKillThresholdMet`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `kills` | Number | `3` |  |
| `statuses` | Block | `{ ... }` |  |

### Context: `StatusOnBattleStart`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |
| `Sleep` | Number | `1` | Applies the 'Sleep' effect. |

### Context: `StatusOnBreakItem`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `3` | Applies the 'Shield' effect. |
| `Thorns` | Number | `1, 2` | Applies the 'Thorns' effect. |

### Context: `StatusOnCastSpell`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1, 2` | Applies the 'Charge' effect. |
| `CurrentWeaponDamageUp` | Number | `1` | Applies the 'CurrentWeaponDamageUp' effect. |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |

### Context: `StatusOnCollectPickup`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |

### Context: `StatusOnCrit`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CritChanceUp` | Number | `5` | Applies the 'CritChanceUp' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |

### Context: `StatusOnDealtDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `TempDexterityUp` | Number | `2` | Applies the 'TempDexterityUp' effect. |
| `TempLuckUp` | Number | `2` | Applies the 'TempLuckUp' effect. |
| `TempStrengthUp` | Number | `1, 2` | Applies the 'TempStrengthUp' effect. |

### Context: `StatusOnDealtDamageThreshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |
| `count_overkill` | Boolean | `true` |  |
| `ignore_during_movement` | Boolean | `true` |  |
| `threshold` | Number | `10` |  |

### Context: `StatusOnEatFood`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |

### Context: `StatusOnEatPill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |

### Context: `StatusOnEndMove`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceAttack` | Number | `1` | Forces the character to execute an immediate attack. |

### Context: `StatusOnGainCoins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |

### Context: `StatusOnGainShield`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |

### Context: `StatusOnHeal`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `SpeedUp` | Number | `2, 4` | Applies the 'SpeedUp' effect. |

### Context: `StatusOnHealed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitCharacter` | Enum/String | `CharmedLeech` | Spawns a specific character or entity upon impact. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

### Context: `StatusOnKill`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `Conditional_FirstApplicationThisTurn` | Block | `{ ... }` | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `EquipPermanentItem` | Enum/String | `BoneClub` | Applies the 'EquipPermanentItem' effect. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |
| `LuckUp` | Number | `2` | Applies the 'LuckUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `RefreshActPoints` | Number | `1` | Applies the 'RefreshActPoints' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `SpeedUp` | Number | `2` | Applies the 'SpeedUp' effect. |
| `Stealth` | Number | `1` | Applies the 'Stealth' effect. |
| `StrengthUp` | Number | `2` | Applies the 'StrengthUp' effect. |
| `TakeBonusTurnWithStatus` | Block | `{ ... }` | Grants the character an immediate extra turn while afflicted with specific statuses. |

### Context: `StatusOnKillEnemy`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `HealthGain` | Number | `2` | Applies the 'HealthGain' effect. |
| `ManaGain` | Number | `3` | Applies the 'ManaGain' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |

### Context: `StatusOnLoseShield`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

### Context: `StatusOnOverHealed`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Number | `1` | Applies the 'CurrentWeaponDamageUp' effect. |
| `ForceUseAbility_NonStack` | Enum/String | `Indigestion_Fart, Indigestion_Fart2` | Applies the 'ForceUseAbility_NonStack' effect. |
| `SpawnScaledRotFly` | Number | `0` | Applies the 'SpawnScaledRotFly' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |

### Context: `StatusOnOverMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |

### Context: `StatusOnPickupCoins`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | `1` | Applies the 'DexterityUp' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |

### Context: `StatusOnPopCorpse`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2, 8` | Applies the 'HealthGain' effect. |

### Context: `StatusOnStanceSwitch`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum/String | `RapidFlowSpin, RapidFlowSpin2` | Applies the 'ForceUseAbility' effect. |
| `NextBasicAttackCritsThisTurn` | Number | `1` | Guarantees the next basic attack executed this turn will be a critical hit. |
| `PartialCleanse` | Number | `1` | Applies the 'PartialCleanse' effect. |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |

### Context: `StatusOnTakeHealthDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentConstitution` | Number | `-1` | Applies the 'PermanentConstitution' effect. |

### Context: `StatusOnTookDamage`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_HasStatus` | Block | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `ConstitutionUp` | Number | `1, -1` | Applies the 'ConstitutionUp' effect. |
| `Craft` | Block | `{ ... }` | Synthesizes or spawns a new item from a specific pool. |
| `DamageUp` | Number | `1, 2` | Combat Trigger: Deals damage to up. |
| `DiminishingHealthRegen` | Number | `1` | Applies the 'DiminishingHealthRegen' effect. |
| `Else` | Block | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `IntelligenceUp` | Number | `-1, -2` | Applies the 'IntelligenceUp' effect. |
| `MovementUp` | Number | `1` | Applies the 'MovementUp' effect. |
| `RandomInjury` | Number | `1` | Applies the 'RandomInjury' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `RandomStatusFromPool` | Block | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `Shield` | Number | `1, 2` | Applies the 'Shield' effect. |
| `SpeedUp` | Number | `1, 2` | Applies the 'SpeedUp' effect. |
| `StrengthUp` | Number | `1, -1` | Applies the 'StrengthUp' effect. |
| `TempDamageUp` | Number | `1, 2` | Applies the 'TempDamageUp' effect. |
| `TempMovement` | Number | `1` | Applies the 'TempMovement' effect. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

### Context: `StatusOnTookDamageFromAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DiminishingHealthRegen` | Number | `1, 2` | Applies the 'DiminishingHealthRegen' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |

### Context: `StatusOnTookDamageFromEnemyAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |

### Context: `StatusOnTriggerTrap`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | `2` | Applies the 'DexterityUp' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |

### Context: `StatusOnTurnEndIfCastNSpells`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpell` | Number | `1, 2` | Applies the 'DoubleCastSpell' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `spells` | Number | `1, 2` |  |

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `7` | Applies the 'ManaGain' effect. |
| `type` | Enum/String | `attack` | The classification type (e.g., damage type or element). |

### Context: `StatusOnTurnEndIfManaExact`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FreeSpell` | Number | `1` | Applies the 'FreeSpell' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `mana` | Number | `2, 0` |  |

### Context: `StatusOnTurnEndIfManaOrHealthExact`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `Shield` | Number | `5` | Applies the 'Shield' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `Temporary` | Block | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `mana` | Number | `5, 4` |  |

### Context: `StatusOnUseAbilityWithTag`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_FirstApplicationThisTurn` | Block | `{ ... }` | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `RefreshActPoints` | Number | `1` | Applies the 'RefreshActPoints' effect. |
| `exclude_basicattack` | Boolean | `true` |  |
| `tag` | Enum/String | `shapeshift, musical` | The specific entity tag required or applied. |

### Context: `StatusOnUseBasicAttack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `FlippedFacingForceAttack` | Number | `1` | Applies the 'FlippedFacingForceAttack' effect. |

### Context: `StatusOnUseElementAbility`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `1, 2` | Applies the 'SpeedUp' effect. |
| `element` | Enum/String | `Gravity` | The specific element type required or applied. |

### Context: `StatusPerInjury`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `3` | Applies the 'Shield' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `cap` | Number | `10` |  |
| `injury` | Enum/String | `int` |  |

### Context: `StatusThingsKnockedBack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | `1, 2` | Applies the 'Drag' effect. |

### Context: `StatusWhenAllySpendsMana`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `2` | Applies the 'ManaGain' effect. |
| `OneUseSpellDamageUp` | Number | `2` | Applies the 'OneUseSpellDamageUp' effect. |

### Context: `StrengthInNumbersAura`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean | `true` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

### Context: `Study`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `marked` | Number | `2` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

### Context: `TaggedPickupEffectReplacement`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Enum/String | `2*X, 3*X` | Applies the 'HealthGain' effect. |
| `tag` | Enum/String | `scrap, money` | The specific entity tag required or applied. |

### Context: `TakeBonusTurnWithStatus`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |

### Context: `Temporary`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `stacks` | Number | `5, 1, 2` | The number of stacks, duration, or intensity to apply. |
| `status` | Enum/String | `Uncontrollable, Brace, Thorns` | The status effect to apply. |
| `turns` | Number | `1` | Duration in turns. |

### Context: `TheHunger`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |

### Context: `TileDamageMultiplier`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number | `0` |  |
| `multiplier` | Number | `2` | Multiplicative modifier to a base value. |

### Context: `TourettesMeows`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cooldown` | Array | `[ 8 15 ]` |  |
| `pool` | Array | `[ Hit Hiss Normal ]` |  |

### Context: `TowerDefense`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1, 2` | The base damage properties of an attack. |
| `range` | Number | `1, 2` | Distance or area of effect in tiles. |

### Context: `Water`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AOEPuddle` | Enum/String | `X-1` | Applies the 'AOEPuddle' effect. |

### Context: `Wind`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Enum/String | `X` |  |

### Context: `effects`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `Charmed` | Array | `[ 1, .40 ], [ 1, .25 ]` | Applies the 'Charmed' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `Freeze` | Array | `[ 1, .15 ], [ 1, .05 ]` | Applies the 'Freeze' effect. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |
| `Leeches` | Number | `1` | Applies the 'Leeches' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `Petrify` | Array | `[ 1, .2 ], [ 1, .1 ]` | Applies the 'Petrify' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `Slow` | Number | `2` | Applies the 'Slow' effect. |
| `SpreadDisease` | Block | `{ ... }` | Provides a chance to transmit a disease status to adjacent targets. |
| `Stun` | Number | `1, [ 1, .05*X ], [ 1, .05 ]` | Applies the 'Stun' effect. |
| `VisualFXTile` | Enum/String | `WaterConduct, BurnTrigger, IcePoof` | Applies the 'VisualFXTile' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

### Context: `empty_armor_scaled_stats`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `spd` | Number | `1, 2` |  |

### Context: `fire`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Fire ]` |  |
| `type` | Enum/String | `spell` | The classification type (e.g., damage type or element). |

### Context: `ice`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Ice ]` |  |
| `type` | Enum/String | `spell` | The classification type (e.g., damage type or element). |

### Context: `keyword_tooltips`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `MagicWeakness` | Number | `1` | Applies the 'MagicWeakness' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

### Context: `lightning`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Electric ]` |  |
| `type` | Enum/String | `spell` | The classification type (e.g., damage type or element). |

### Context: `lock_item_slot`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `frame` | Number | `11, 17, 16` |  |
| `slot` | Enum/String | `face, neck, trinket` |  |

### Context: `on_break`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | `5, 10` | Applies the 'SafeExplosionIfHitSomething' effect. |

### Context: `on_throw`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `HitExplosion` | Number | `5, 10` | Applies the 'HitExplosion' effect. |

### Context: `passives`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AbilityChargeRefundChance` | Block | `{ ... }` | Applies the 'AbilityChargeRefundChance' effect. |
| `AbilityOnBattleStart` | Enum/String | `Heathens, neck_ChefsApron, MegaFart` | Applies the 'AbilityOnBattleStart' effect. |
| `AbilityReaction` | Enum/String | `PissYourself, Gassy_AssBlast, Gassy_AssBlast2` | Applies the 'AbilityReaction' effect. |
| `AbilityWhenTaggedCharacterMovesNear` | Block | `{ ... }` | Applies the 'AbilityWhenTaggedCharacterMovesNear' effect. |
| `AbsorbManaAura` | Number | `1` | Applies the 'AbsorbManaAura' effect. |
| `AddAllyNeighborsToAbilityRange` | Number | `1` | Applies the 'AddAllyNeighborsToAbilityRange' effect. |
| `AddAllyNeighborsToAttackRange` | Number | `1` | Applies the 'AddAllyNeighborsToAttackRange' effect. |
| `AddBonusMeleeRange` | Number | `1, 2, 10` | Applies the 'AddBonusMeleeRange' effect. |
| `AddBonusRange` | Number | `1, 2, 10` | Applies the 'AddBonusRange' effect. |
| `AddChaScalingSpellDamage` | Number | `3` | Applies the 'AddChaScalingSpellDamage' effect. |
| `AddCorpseHealth` | Number | `-999999, 96, 3` | Applies the 'AddCorpseHealth' effect. |
| `AddCritMultiplier` | Number | `100%, 25%, 50%` | Applies the 'AddCritMultiplier' effect. |
| `AddDamageToBasicAttack` | Number | `1, 2, 4` | Applies the 'AddDamageToBasicAttack' effect. |
| `AddDamageToElementDamage` | Block | `{ ... }` | Applies the 'AddDamageToElementDamage' effect. |
| `AddElementsToBasicAttack` | Enum/String | `Ice, Fire, Electric` | Applies the 'AddElementsToBasicAttack' effect. |
| `AddHiddenTag` | Enum/String | `bowling_ball` | Applies the 'AddHiddenTag' effect. |
| `AddInitiative` | Number | `999, -100` | Applies the 'AddInitiative' effect. |
| `AddKnockbackDamage` | Number | `1, 2, 3` | Applies the 'AddKnockbackDamage' effect. |
| `AddKnockbackToEverything` | Number | `1` | Applies the 'AddKnockbackToEverything' effect. |
| `AddLevelUpRerolls` | Number | `1, 2, 3` | Applies the 'AddLevelUpRerolls' effect. |
| `AddLevelUpStatMultiplier` | Number | `1` | Applies the 'AddLevelUpStatMultiplier' effect. |
| `AddManaRegen` | Number | `1, 7, 5` | Applies the 'AddManaRegen' effect. |
| `AddMovement` | Number | `1, 2, 4` | Applies the 'AddMovement' effect. |
| `AddPassiveToSpawnedRocks` | Block | `{ ... }` | Applies the 'AddPassiveToSpawnedRocks' effect. |
| `AddPassivesToCharmed` | Block | `{ ... }` | Applies the 'AddPassivesToCharmed' effect. |
| `AddPassivesToMinions` | Block | `{ ... }` | Applies the 'AddPassivesToMinions' effect. |
| `AddPassivesToSummonAbilityMinions` | Block | `{ ... }` | Applies the 'AddPassivesToSummonAbilityMinions' effect. |
| `AddRangedCritChance` | Number | `25%` | Applies the 'AddRangedCritChance' effect. |
| `AddSelfStatusToBasicAttack` | Block | `{ ... }` | Applies the 'AddSelfStatusToBasicAttack' effect. |
| `AddSelfStatusToWeapons` | Block | `{ ... }` | Applies the 'AddSelfStatusToWeapons' effect. |
| `AddSpellDamage` | Number | `1` | Applies the 'AddSpellDamage' effect. |
| `AddStartingMana` | Number | `5, 20` | Applies the 'AddStartingMana' effect. |
| `AddStatusToAllDamageAbilities` | Block | `{ ... }` | Applies the 'AddStatusToAllDamageAbilities' effect. |
| `AddStatusToAllDamage` | Block | `{ ... }` | Applies the 'AddStatusToAllDamage' effect. |
| `AddStatusToBasicAttackWithCooldown` | Block | `{ ... }` | Applies the 'AddStatusToBasicAttackWithCooldown' effect. |
| `AddStatusToBasicAttack` | Block | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `AddStatusToBasicMeleeAttack` | Block | `{ ... }` | Applies the 'AddStatusToBasicMeleeAttack' effect. |
| `AddStatusToElementAbilities` | Block | `{ ... }` | Applies the 'AddStatusToElementAbilities' effect. |
| `AddStatusToElementDamage` | Block | `{ ... }` | Applies the 'AddStatusToElementDamage' effect. |
| `AddStatusToExplosions` | Block | `{ ... }` | Applies the 'AddStatusToExplosions' effect. |
| `AddStatusToFirstBasicAttack` | Block | `{ ... }` | Applies the 'AddStatusToFirstBasicAttack' effect. |
| `AddStatusToKnockbackDamage` | Block | `{ ... }` | Applies the 'AddStatusToKnockbackDamage' effect. |
| `AddStatusToMeleeDamage` | Block | `{ ... }` | Applies the 'AddStatusToMeleeDamage' effect. |
| `AddStatusToReceivedDamage_ExcludeStatuses` | Block | `{ ... }` | Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect. |
| `AddStatusToSpells` | Block | `{ ... }` | Applies the 'AddStatusToSpells' effect. |
| `AddStatusToTrampleDamage` | Block | `{ ... }` | Applies the 'AddStatusToTrampleDamage' effect. |
| `AddStatusToWeapons` | Block | `{ ... }` | Applies the 'AddStatusToWeapons' effect. |
| `AddStatusesIfPersistentWeatherElement` | Block | `{ ... }` | Applies the 'AddStatusesIfPersistentWeatherElement' effect. |
| `AddStatusesToReceivedElementalDamage` | Block | `{ ... }` | Applies the 'AddStatusesToReceivedElementalDamage' effect. |
| `AddTag` | Enum/String | `rock` | Applies the 'AddTag' effect. |
| `AddTemporaryEffectsToBasicAttack` | Block | `{ ... }` | Applies the 'AddTemporaryEffectsToBasicAttack' effect. |
| `AddTemporaryEffectsToEquipment` | Block | `{ ... }` | Applies the 'AddTemporaryEffectsToEquipment' effect. |
| `AddUnfilledMaxHealth` | Number | `50, 20` | Applies the 'AddUnfilledMaxHealth' effect. |
| `AddWeaponScaling` | Number | `1` | Applies the 'AddWeaponScaling' effect. |
| `AfterImage` | Enum/String | `PlayerCat_ThiefShade2, PlayerCat_ThiefShade` | Spawns a visual decoy or shade at the caster's previous location. |
| `AllDamageCrits` | Number | `1` | Applies the 'AllDamageCrits' effect. |
| `AllStatsUp` | Number | `2, -1, -2` | Applies the 'AllStatsUp' effect. |
| `AlliesAvoidTraps` | Number | `1` | Applies the 'AlliesAvoidTraps' effect. |
| `AllowPassTurn` | Number | `1, 0` | Applies the 'AllowPassTurn' effect. |
| `AllyBonusAbilityAura` | Enum/String | `NubbyToss, { ... }` | Applies the 'AllyBonusAbilityAura' effect. |
| `AllyChainKnockback` | Number | `1` | Applies the 'AllyChainKnockback' effect. |
| `AllyDamageReaction` | Enum/String | `attack` | Applies the 'AllyDamageReaction' effect. |
| `AllyDamageReduction` | Number | `0` | Applies the 'AllyDamageReduction' effect. |
| `AllyHealthRegenAura` | Block | `{ ... }` | Applies the 'AllyHealthRegenAura' effect. |
| `AllyManaRegenAura` | Block | `{ ... }` | Applies the 'AllyManaRegenAura' effect. |
| `AllyMoveAbilityAura` | Enum/String | `CatapultJump2, CatapultJump` | Applies the 'AllyMoveAbilityAura' effect. |
| `AllyMultiplyKnockbackDamage` | Number | `2` | Applies the 'AllyMultiplyKnockbackDamage' effect. |
| `AllyMultiplyKnockbackDistance` | Number | `2` | Applies the 'AllyMultiplyKnockbackDistance' effect. |
| `AllyUncappedHPAura` | Number | `1` | Applies the 'AllyUncappedHPAura' effect. |
| `AlphaCat` | Number | `1` | Applies the 'AlphaCat' effect. |
| `AlphaTurns` | Number | `1, -1` | Applies the 'AlphaTurns' effect. |
| `AlternateCraftingPools` | Block | `{ ... }` | Applies the 'AlternateCraftingPools' effect. |
| `AmplifyKnockback` | Number | `2, 10` | Applies the 'AmplifyKnockback' effect. |
| `AmplifyNegativeStatus` | Number | `1` | Applies the 'AmplifyNegativeStatus' effect. |
| `AmplifyPositiveStatus` | Number | `1, 2` | Applies the 'AmplifyPositiveStatus' effect. |
| `AmplifyStatus` | Enum/String | `Burn, { ... }, Rot` | Applies the 'AmplifyStatus' effect. |
| `ApplyStatusesToRandomEnemiesEachTurn` | Block | `{ ... }` | Applies the 'ApplyStatusesToRandomEnemiesEachTurn' effect. |
| `ArmorDodgeChance` | Number | `10%` | Applies the 'ArmorDodgeChance' effect. |
| `Autism` | Block | `{ ... }` | Applies the 'Autism' effect. |
| `AutoCritLowDamage` | Number | `2, 3` | Applies the 'AutoCritLowDamage' effect. |
| `AutoEquipConsumables` | Number | `1` | Applies the 'AutoEquipConsumables' effect. |
| `AutocastEachRound` | Block | `{ ... }` | Forces the character to automatically cast a specific ability at the start of each combat round. |
| `AutocastEachTurnBegin` | Enum/String | `MindCrack_EldritchVisage, MindCrack_EldritchVisage2, { ... }` | Applies the 'AutocastEachTurnBegin' effect. |
| `AutocastEachTurn` | Enum/String | `DarkOneStrike, ViolentOutburst` | Applies the 'AutocastEachTurn' effect. |
| `BackstabCritChance` | Number | `1` | Applies the 'BackstabCritChance' effect. |
| `BackstabImmunity` | Number | `1` | Applies the 'BackstabImmunity' effect. |
| `BackstabWeakness` | Number | `0.75` | Applies the 'BackstabWeakness' effect. |
| `BasicAttackAOEBonus` | Number | `1, 2` | Applies the 'BasicAttackAOEBonus' effect. |
| `BasicAttackCritChance` | Number | `100%` | Applies the 'BasicAttackCritChance' effect. |
| `BasicAttackDamageMultiplier` | Number | `33.333334%, 0, 50%` | Applies the 'BasicAttackDamageMultiplier' effect. |
| `BasicAttackStatusCarefulness` | Number | `1` | Applies the 'BasicAttackStatusCarefulness' effect. |
| `BasicAttackStatusSwap` | Array | `[ TempDamageUp DamageUp ]` | Applies the 'BasicAttackStatusSwap' effect. |
| `BlacklistPickupType` | Enum/String | `food` | Applies the 'BlacklistPickupType' effect. |
| `BlastResistance` | Number | `2, 4, 3` | Applies the 'BlastResistance' effect. |
| `BleedThorns` | Number | `2` | Applies the 'BleedThorns' effect. |
| `Bleed` | Number | `1, 3` | Applies the 'Bleed' effect. |
| `BonusAbility` | Enum/String | `Bloodzerk, FeralMelee, Groom` | Applies the 'BonusAbility' effect. |
| `BonusFoodEachBattle` | Number | `2, 20` | Applies the 'BonusFoodEachBattle' effect. |
| `BonusHealthRegenBasedOnDex` | Number | `5` | Applies the 'BonusHealthRegenBasedOnDex' effect. |
| `BonusRangeBasedOnDex` | Number | `5` | Applies the 'BonusRangeBasedOnDex' effect. |
| `BoobyTrapItems` | Block | `{ ... }` | Applies the 'BoobyTrapItems' effect. |
| `BoostAllyStatsOnDeath` | Number | `1, 2` | Applies the 'BoostAllyStatsOnDeath' effect. |
| `BoostDamageAura` | Number | `1` | Applies the 'BoostDamageAura' effect. |
| `BoostDamageGlobalAura` | Number | `1` | Applies the 'BoostDamageGlobalAura' effect. |
| `BoostHeals` | Number | `1, 2, -2` | Applies the 'BoostHeals' effect. |
| `BoostRangeAura` | Number | `1` | Applies the 'BoostRangeAura' effect. |
| `BoostRangeGlobalAura` | Number | `1` | Applies the 'BoostRangeGlobalAura' effect. |
| `BoostWeaponDamage` | Number | `2, 1, 5` | Applies the 'BoostWeaponDamage' effect. |
| `BouncyProjectiles` | Block | `{ ... }` | Applies the 'BouncyProjectiles' effect. |
| `BraceForEachNeighboringEnemy` | Number | `1, 2` | Applies the 'BraceForEachNeighboringEnemy' effect. |
| `Brace` | Number | `1, 2, 3` | Applies the 'Brace' effect. |
| `Bruise` | Number | `1, 2` | Applies the 'Bruise' effect. |
| `BuffImmunity` | Number | `1` | Applies the 'BuffImmunity' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `CCImmunity` | Number | `1` | Applies the 'CCImmunity' effect. |
| `CanRemoveCursedItems` | Number | `1` | Applies the 'CanRemoveCursedItems' effect. |
| `CantDodge` | Number | `1` | Applies the 'CantDodge' effect. |
| `CapDamageFromAllies` | Number | `1` | Applies the 'CapDamageFromAllies' effect. |
| `CapMovementAbilityRange` | Number | `1` | Applies the 'CapMovementAbilityRange' effect. |
| `CapTechSpent` | Number | `0` | Applies the 'CapTechSpent' effect. |
| `CatAPultAnimation` | Block | `{ ... }` | Applies the 'CatAPultAnimation' effect. |
| `CatchProjectiles` | Block | `{ ... }` | Applies the 'CatchProjectiles' effect. |
| `ChainKnockback` | Number | `1` | Applies the 'ChainKnockback' effect. |
| `ChanceToBackflip` | Block | `{ ... }` | Applies the 'ChanceToBackflip' effect. |
| `ChanceToBlockAndCounter` | Number | `33%, 15%` | Applies the 'ChanceToBlockAndCounter' effect. |
| `ChanceToRevive` | Number | `25, { ... }` | Applies the 'ChanceToRevive' effect. |
| `ChangeTauntPriority` | Number | `-1` | Applies the 'ChangeTauntPriority' effect. |
| `CharmAllFlies` | Number | `1` | Applies the 'CharmAllFlies' effect. |
| `ClassManaCostReduction` | Block | `{ ... }` | Applies the 'ClassManaCostReduction' effect. |
| `CobraReflex` | Enum/String | `BasicMonkMelee` | Applies the 'CobraReflex' effect. |
| `CoinsAddDamage` | Number | `1, 2` | Applies the 'CoinsAddDamage' effect. |
| `CollectPickupsOnBattleEnd` | Number | `1, { ... }` | Applies the 'CollectPickupsOnBattleEnd' effect. |
| `ConductorManaRegen` | Number | `2` | Applies the 'ConductorManaRegen' effect. |
| `Conductor` | Number | `2` | Applies the 'Conductor' effect. |
| `ConfusionEffectOnTaggedAbilities` | Enum/String | `consumable` | Applies the 'ConfusionEffectOnTaggedAbilities' effect. |
| `ConjureCastSpellsForAllies` | Number | `1, 2` | Applies the 'ConjureCastSpellsForAllies' effect. |
| `ConsumableEffectsMultiplierBonus` | Number | `1` | Applies the 'ConsumableEffectsMultiplierBonus' effect. |
| `ConsumablesInfiniteRange` | Number | `1` | Applies the 'ConsumablesInfiniteRange' effect. |
| `ConsumablesMeleeRange` | Number | `1` | Applies the 'ConsumablesMeleeRange' effect. |
| `CounterAttack` | Enum/String | `ReflexPunchJab2, ReflexPunchJab` | Applies the 'CounterAttack' effect. |
| `CritChanceUp` | Number | `25, 5, 10` | Applies the 'CritChanceUp' effect. |
| `CritsApplyStatus` | Block | `{ ... }` | Applies the 'CritsApplyStatus' effect. |
| `DamageEnemiesOnHeal` | Number | `1, 2` | Combat Trigger: Deals damage to enemies on heal. |
| `DamageEnemiesOnKill` | Number | `1, 2` | Combat Trigger: Deals damage to enemies on kill. |
| `DamageIfDidntUseSpecificAbility` | Block | `{ ... }` | Combat Trigger: Deals damage to if didnt use specific ability. |
| `DamageNeighborTilesWhenCastSpell` | Block | `{ ... }` | Combat Trigger: Deals damage to neighbor tiles when cast spell. |
| `DamageNeighborsAfterMove` | Block | `{ ... }` | Combat Trigger: Deals damage to neighbors after move. |
| `DamageNeighborsOnEndMove` | Block | `{ ... }` | Combat Trigger: Deals damage to neighbors on end move. |
| `DamageReductionAura` | Block | `{ ... }` | Combat Trigger: Deals damage to reduction aura. |
| `DamageUp` | Number | `1, 4, 3` | Combat Trigger: Deals damage to up. |
| `DeathChill` | Number | `1` | Applies the 'DeathChill' effect. |
| `DeathRattle` | Block | `{ ... }, BoomerCatExplode` | Applies the 'DeathRattle' effect. |
| `DebuffImmunity` | Number | `1` | Applies the 'DebuffImmunity' effect. |
| `DejaVu` | Number | `10%` | Applies the 'DejaVu' effect. |
| `DepressionAura` | Number | `2` | Applies the 'DepressionAura' effect. |
| `Diabetes` | Block | `{ ... }` | Applies the 'Diabetes' effect. |
| `DirtyClaws` | Number | `1` | Applies the 'DirtyClaws' effect. |
| `DisableAbilitiesWithTag` | Enum/String | `meat` | Applies the 'DisableAbilitiesWithTag' effect. |
| `DisableAbilities` | Enum/String | `all_items` | Applies the 'DisableAbilities' effect. |
| `DodgeChance` | Number | `15%, 25%, 10%` | Applies the 'DodgeChance' effect. |
| `Doomed` | Number | `3` | Applies the 'Doomed' effect. |
| `DoubleCastWeapons` | Number | `1, 2` | Applies the 'DoubleCastWeapons' effect. |
| `DukeOfFlies` | Number | `1` | Applies the 'DukeOfFlies' effect. |
| `Dyslexia` | Array | `[ 6 9 ], [ 3 5 ]` | Applies the 'Dyslexia' effect. |
| `EMP` | Block | `{ ... }` | Applies the 'EMP' effect. |
| `EachSpellFreeAtFullMana` | Number | `1` | Applies the 'EachSpellFreeAtFullMana' effect. |
| `ElementImmune` | Enum/String | `Ice, Fire, Electric` | Applies the 'ElementImmune' effect. |
| `ElementalAttunement` | Block | `{ ... }` | Applies the 'ElementalAttunement' effect. |
| `ElementalManaCostReduction` | Block | `{ ... }` | Applies the 'ElementalManaCostReduction' effect. |
| `Empath` | Number | `100%, 50%` | Applies the 'Empath' effect. |
| `EnemiesGetPickupsKnockedOut` | Number | `1, 2` | Applies the 'EnemiesGetPickupsKnockedOut' effect. |
| `EnergyStorm` | Number | `3, { ... }` | Applies the 'EnergyStorm' effect. |
| `EquipRandomTemporaryItemFromPool` | Enum/String | `weapons` | Applies the 'EquipRandomTemporaryItemFromPool' effect. |
| `EquipTemporaryItem` | Enum/String | `FoodBig, FoodMedium, ButcherHook_Temporary` | Applies the 'EquipTemporaryItem' effect. |
| `EquipmentPassiveMultiplierBonus` | Number | `1` | Applies the 'EquipmentPassiveMultiplierBonus' effect. |
| `EquipmentSetBonusBonus` | Number | `1, 2` | Applies the 'EquipmentSetBonusBonus' effect. |
| `EscapeSequence` | Block | `{ ... }` | Applies the 'EscapeSequence' effect. |
| `Eternal` | Block | `{ ... }` | Applies the 'Eternal' effect. |
| `ExhaustionRoundChange` | Number | `3` | Applies the 'ExhaustionRoundChange' effect. |
| `ExplodeOverkilledEnemies` | Number | `1, 2` | Applies the 'ExplodeOverkilledEnemies' effect. |
| `ExplosionImmunity` | Number | `1` | Applies the 'ExplosionImmunity' effect. |
| `ExtraBasicAttacks` | Number | `1, 2` | Applies the 'ExtraBasicAttacks' effect. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies the 'ExtraBasicMoves_Status' effect. |
| `ExtraInjuryOnDeath` | Number | `1` | Applies the 'ExtraInjuryOnDeath' effect. |
| `ExtraMovePoints` | Number | `1` | Applies the 'ExtraMovePoints' effect. |
| `ExtraStatusWhenDealingDamage` | Block | `{ ... }` | Applies the 'ExtraStatusWhenDealingDamage' effect. |
| `ExtraTrinketUses` | Number | `1` | Applies the 'ExtraTrinketUses' effect. |
| `ExtraWeaponAttacks` | Number | `1, 2` | Applies the 'ExtraWeaponAttacks' effect. |
| `FaceArmorPassiveMultiplierBonus` | Number | `2` | Applies the 'FaceArmorPassiveMultiplierBonus' effect. |
| `FaceShield` | Number | `0` | Applies the 'FaceShield' effect. |
| `FamiliarSecondaryDamageImmunity` | Number | `1` | Applies the 'FamiliarSecondaryDamageImmunity' effect. |
| `FlowerPowerAuraBrace` | Number | `1` | Applies the 'FlowerPowerAuraBrace' effect. |
| `FlowerPowerAuraStrength` | Number | `1` | Applies the 'FlowerPowerAuraStrength' effect. |
| `FlowersOnEndTurn` | Number | `4, 3` | Applies the 'FlowersOnEndTurn' effect. |
| `FlyDamageIncrease` | Number | `1, 4` | Applies the 'FlyDamageIncrease' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |
| `FollowUp` | Enum/String | `FollowUpDash, FollowUpDash2` | Applies the 'FollowUp' effect. |
| `ForceSpecificInjury` | Enum/String | `cha, lck, int` | Applies the 'ForceSpecificInjury' effect. |
| `ForceUseAbility` | Enum/String | `MockingbirdForm` | Applies the 'ForceUseAbility' effect. |
| `FreePathfindElement` | Enum/String | `Water, Grass` | Applies the 'FreePathfindElement' effect. |
| `FreeSpellsAtFullMana` | Number | `1` | Applies the 'FreeSpellsAtFullMana' effect. |
| `FreezePiercing` | Number | `1` | Applies the 'FreezePiercing' effect. |
| `FrontstabBasicAttackCritChance` | Number | `100%` | Applies the 'FrontstabBasicAttackCritChance' effect. |
| `FrontstabCritChance` | Number | `100%` | Applies the 'FrontstabCritChance' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |
| `FullHealthAllStatsUp` | Number | `1` | Applies the 'FullHealthAllStatsUp' effect. |
| `FullHealthCritChance` | Number | `100` | Applies the 'FullHealthCritChance' effect. |
| `FullHealthManaRegen` | Number | `5` | Applies the 'FullHealthManaRegen' effect. |
| `FullPower` | Number | `3` | Applies the 'FullPower' effect. |
| `FurnitureStats` | Block | `{ ... }` | Applies the 'FurnitureStats' effect. |
| `GainExtraShield` | Number | `2` | Applies the 'GainExtraShield' effect. |
| `GrassTileHealing` | Number | `1` | Applies the 'GrassTileHealing' effect. |
| `GravityWell` | Block | `{ ... }` | Applies the 'GravityWell' effect. |
| `HPGainBlock` | Number | `1` | Applies the 'HPGainBlock' effect. |
| `HeadArmorPassiveMultiplierBonus` | Number | `1, 2` | Applies the 'HeadArmorPassiveMultiplierBonus' effect. |
| `HealAtStart` | Number | `100%` | Applies the 'HealAtStart' effect. |
| `HealDamagesEnemies` | Number | `1` | Applies the 'HealDamagesEnemies' effect. |
| `HealingAura` | Number | `1` | Applies the 'HealingAura' effect. |
| `HealsAlsoRegenMana` | Number | `2, 50%` | Applies the 'HealsAlsoRegenMana' effect. |
| `HealsCanRevive` | Number | `1, 3` | Applies the 'HealsCanRevive' effect. |
| `HealthRegenUp` | Number | `1, 2, 3` | Applies the 'HealthRegenUp' effect. |
| `HolyDamageMultiplierBonus` | Number | `1` | Applies the 'HolyDamageMultiplierBonus' effect. |
| `HolyShieldTransferToTaggedMinions` | Enum/String | `any, crow` | Applies the 'HolyShieldTransferToTaggedMinions' effect. |
| `HouseFoodRequirementMultiplier` | Number | `0` | Applies the 'HouseFoodRequirementMultiplier' effect. |
| `Hypomania` | Number | `3` | Applies the 'Hypomania' effect. |
| `IgnoreTiles` | Number | `1` | Applies the 'IgnoreTiles' effect. |
| `ImmortalLeeches` | Number | `1` | Applies the 'ImmortalLeeches' effect. |
| `IncreaseExplosionDamage` | Number | `2, 4, 3` | Applies the 'IncreaseExplosionDamage' effect. |
| `IncreaseExplosionSize` | Number | `2` | Applies the 'IncreaseExplosionSize' effect. |
| `IncreaseHealingSpellRange` | Number | `2` | Applies the 'IncreaseHealingSpellRange' effect. |
| `IncreaseItemUsesOnEquip` | Number | `1` | Applies the 'IncreaseItemUsesOnEquip' effect. |
| `IncreaseSpellRange` | Number | `5, 10` | Applies the 'IncreaseSpellRange' effect. |
| `InfiniteRebirth` | Block | `{ ... }` | Applies the 'InfiniteRebirth' effect. |
| `InjuryImmunity` | Number | `1` | Applies the 'InjuryImmunity' effect. |
| `InnateElement` | Enum/String | `Ice, Fire, Electric` | Applies the 'InnateElement' effect. |
| `InvertBrainFaction` | Number | `1` | Applies the 'InvertBrainFaction' effect. |
| `KillsHeal` | Number | `5, 50%` | Applies the 'KillsHeal' effect. |
| `KillsToMeat` | Enum/String | `Food` | Applies the 'KillsToMeat' effect. |
| `KnockbackImmunity` | Number | `1` | Applies the 'KnockbackImmunity' effect. |
| `LateBloomer` | Block | `{ ... }` | Applies the 'LateBloomer' effect. |
| `LevelUpClassOverride` | Enum/String | `Colorless, Jester` | Applies the 'LevelUpClassOverride' effect. |
| `LightningAspectCharge` | Number | `1, 0` | Applies the 'LightningAspectCharge' effect. |
| `LightningRod` | Block | `{ ... }` | Applies the 'LightningRod' effect. |
| `LimitDamage` | Number | `1` | Applies the 'LimitDamage' effect. |
| `LimitHeal` | Number | `1` | Applies the 'LimitHeal' effect. |
| `LimitSelfKnockbackDamage` | Number | `1` | Applies the 'LimitSelfKnockbackDamage' effect. |
| `LimitedTileTrail` | Enum/String | `FlowerTile` | Applies the 'LimitedTileTrail' effect. |
| `LineOfSightTrueSightAura` | Number | `0, .5` | Applies the 'LineOfSightTrueSightAura' effect. |
| `LobbedHook` | Number | `1, 2` | Applies the 'LobbedHook' effect. |
| `LowHealthAllyDodgeChanceAura` | Block | `{ ... }` | Applies the 'LowHealthAllyDodgeChanceAura' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MakeBasicAttackPassThroughThings` | Number | `1` | Applies the 'MakeBasicAttackPassThroughThings' effect. |
| `MakeSpellsRequireCharge` | Number | `1` | Applies the 'MakeSpellsRequireCharge' effect. |
| `ManaCostReductionTagged` | Block | `{ ... }` | Applies the 'ManaCostReductionTagged' effect. |
| `ManaCostReduction` | Number | `25%` | Applies the 'ManaCostReduction' effect. |
| `ManaRegenMultiplierIfManaEmpty` | Number | `2` | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. |
| `MaxAccuracy` | Number | `1` | Applies the 'MaxAccuracy' effect. |
| `MaxStartingMana` | Number | `1` | Applies the 'MaxStartingMana' effect. |
| `MegaMinions` | Number | `3, { ... }` | Applies the 'MegaMinions' effect. |
| `MeleeRevengeDamage` | Block | `{ ... }` | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. |
| `MetalDetector` | Number | `5, 10` | Applies the 'MetalDetector' effect. |
| `Metal` | Number | `1` | Applies the 'Metal' effect. |
| `MinimumTech` | Number | `1` | Applies the 'MinimumTech' effect. |
| `MissChance` | Number | `5, 15, 10` | Applies the 'MissChance' effect. |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | Enum/String | `EatShit, Cannibalize` | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. |
| `MoveAwayFromDamageSource` | Enum/String | `MoveOne` | Applies the 'MoveAwayFromDamageSource' effect. |
| `MoveQuivered` | Number | `2` | Applies the 'MoveQuivered' effect. |
| `MoveRandomly` | Number | `1` | Applies the 'MoveRandomly' effect. |
| `MoveSpeedMultiplier` | Enum/String | `.5` | Applies the 'MoveSpeedMultiplier' effect. |
| `MoveTowardsDamageSource` | Block | `{ ... }` | Applies the 'MoveTowardsDamageSource' effect. |
| `MoveWhenDamaged` | Block | `{ ... }` | Applies the 'MoveWhenDamaged' effect. |
| `MovementReaction` | Block | `{ ... }` | Applies the 'MovementReaction' effect. |
| `MulticlassLevelUp` | Enum/String | `Hunter, Fighter, Mage` | Applies the 'MulticlassLevelUp' effect. |
| `NeckArmorPassiveMultiplierBonus` | Number | `2` | Applies the 'NeckArmorPassiveMultiplierBonus' effect. |
| `NoManaRegen` | Number | `1` | Applies the 'NoManaRegen' effect. |
| `NoReflection` | Number | `1` | Applies the 'NoReflection' effect. |
| `NubbyTossPriority` | Number | `1` | Applies the 'NubbyTossPriority' effect. |
| `NumbingLeeches` | Number | `3` | Applies the 'NumbingLeeches' effect. |
| `OverhealGainsBothShield` | Number | `1, 2` | Applies the 'OverhealGainsBothShield' effect. |
| `OverrideBasicAttack` | Enum/String | `BasicMelee, GerdShot` | Applies the 'OverrideBasicAttack' effect. |
| `OverrideMaxHealth` | Number | `1` | Applies the 'OverrideMaxHealth' effect. |
| `OverrideMaxMana` | Number | `1` | Applies the 'OverrideMaxMana' effect. |
| `OverridePalette` | Number | `87` | Applies the 'OverridePalette' effect. |
| `Paranoia` | Enum/String | `ParanoiaBasicMelee` | Applies the 'Paranoia' effect. |
| `ParasitesArentCursed` | Number | `1` | Applies the 'ParasitesArentCursed' effect. |
| `PassiveAfterXKills` | Block | `{ ... }` | Applies the 'PassiveAfterXKills' effect. |
| `PassiveAtFullHealth` | Block | `{ ... }` | Applies the 'PassiveAtFullHealth' effect. |
| `PassiveAtHealthThreshold` | Block | `{ ... }` | Applies the 'PassiveAtHealthThreshold' effect. |
| `PassiveAtInjuryThreshold` | Block | `{ ... }` | Applies the 'PassiveAtInjuryThreshold' effect. |
| `PassiveAtStatThreshold` | Block | `{ ... }` | Applies the 'PassiveAtStatThreshold' effect. |
| `PassiveIfAllArmorEmpty` | Block | `{ ... }` | Applies the 'PassiveIfAllArmorEmpty' effect. |
| `PassiveIfEmptyFace` | Block | `{ ... }` | Applies the 'PassiveIfEmptyFace' effect. |
| `PassiveIfEmptyHead` | Block | `{ ... }` | Applies the 'PassiveIfEmptyHead' effect. |
| `PassiveIfEmptyNeck` | Block | `{ ... }` | Applies the 'PassiveIfEmptyNeck' effect. |
| `PassiveLevelScaledStatus` | Block | `{ ... }` | Applies the 'PassiveLevelScaledStatus' effect. |
| `PassiveLevelUpAtCombatEnd` | Number | `1` | Applies the 'PassiveLevelUpAtCombatEnd' effect. |
| `PassiveUntilCastSpell` | Block | `{ ... }` | Applies the 'PassiveUntilCastSpell' effect. |
| `PassiveUntilGetKill` | Block | `{ ... }` | Applies the 'PassiveUntilGetKill' effect. |
| `PassiveWhenAffectedByElement` | Block | `{ ... }` | State Trigger: Grants nested passives when affected by element. |
| `PassiveWhenAtFullMana` | Block | `{ ... }` | State Trigger: Grants nested passives when at full mana. |
| `PassiveWhenTheAlpha` | Block | `{ ... }` | State Trigger: Grants nested passives when the alpha. |
| `PassiveWhileInMonkMeleeStance` | Block | `{ ... }` | Applies the 'PassiveWhileInMonkMeleeStance' effect. |
| `PassiveWhileInMonkRangedStance` | Block | `{ ... }` | Applies the 'PassiveWhileInMonkRangedStance' effect. |
| `PassiveWhilePreviewingMonkRangedStance` | Block | `{ ... }` | Applies the 'PassiveWhilePreviewingMonkRangedStance' effect. |
| `PassiveWhileWearingMetal` | Block | `{ ... }` | Applies the 'PassiveWhileWearingMetal' effect. |
| `PermanentImmobile` | Number | `1` | Applies the 'PermanentImmobile' effect. |
| `PermanentItems` | Number | `1, 2` | Applies the 'PermanentItems' effect. |
| `PermanentKitten` | Number | `1` | Applies the 'PermanentKitten' effect. |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |
| `Phasing` | Number | `1` | Applies the 'Phasing' effect. |
| `PoisonMultiplier` | Number | `2` | Applies the 'PoisonMultiplier' effect. |
| `PoisonThorns` | Number | `1, 2` | Applies the 'PoisonThorns' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `PoopWhenHit` | Enum/String | `Poop` | Applies the 'PoopWhenHit' effect. |
| `ProtectTargetedAllies` | Enum/String | `SwapPositions_WideLoad, SwapPositions_WideLoad2` | Applies the 'ProtectTargetedAllies' effect. |
| `Quiver` | Number | `1, 2` | Applies the 'Quiver' effect. |
| `Quivered` | Number | `5, 1, 2` | Applies the 'Quivered' effect. |
| `RandomPassivePool` | Block | `{ ... }` | Applies the 'RandomPassivePool' effect. |
| `RangedTrueShot` | Number | `1` | Applies the 'RangedTrueShot' effect. |
| `RealTimePressure_OneUnit` | Number | `5` | Applies the 'RealTimePressure_OneUnit' effect. |
| `ReceivedStatusReplacement` | Array | `[ Sleep SleepParalysis ]` | Applies the 'ReceivedStatusReplacement' effect. |
| `RefreshMoveOnWeaponConnect` | Number | `1` | Applies the 'RefreshMoveOnWeaponConnect' effect. |
| `RemoveLineOfSightRestrictions` | Number | `1` | Applies the 'RemoveLineOfSightRestrictions' effect. |
| `RemoveOncePerFightRestriction` | Number | `1` | Applies the 'RemoveOncePerFightRestriction' effect. |
| `ReplaceBasicAttackWhenCastable` | Enum/String | `Shank, BasicSuplex, Shank2` | Applies the 'ReplaceBasicAttackWhenCastable' effect. |
| `ReplaceBasicAttackWhenDead` | Enum/String | `Haunt` | Applies the 'ReplaceBasicAttackWhenDead' effect. |
| `ReplaceBasicAttack` | Enum/String | `BasicDruidAbilityVersatile, BasicButcherMeleeWideSpin, BasicButcherMeleeWideDoubleSpin` | Applies the 'ReplaceBasicAttack' effect. |
| `ReplaceBasicMove` | Enum/String | `ToadJump_BasicMove, BellyFlop_BasicMove, BasicDashAttackMove` | Applies the 'ReplaceBasicMove' effect. |
| `ReplaceBrain` | Block | `{ ... }` | Applies the 'ReplaceBrain' effect. |
| `ReplaceSpawnedObjects` | Array | `[ Crow2 Crow3 ], [ Crow Crow2 ], [ Crow Crow3 ]` | Applies the 'ReplaceSpawnedObjects' effect. |
| `ReplaceSpellsWhenDead` | Enum/String | `Spook` | Applies the 'ReplaceSpellsWhenDead' effect. |
| `RevengeDamage` | Block | `{ ... }` | Reaction trigger: Deals damage to the attacker when hit. |
| `ReviveOnWin` | Number | `100%` | Applies the 'ReviveOnWin' effect. |
| `Robot` | Block | `{ ... }` | Applies the 'Robot' effect. |
| `RobotsInheritArmor` | Number | `1, 2` | Applies the 'RobotsInheritArmor' effect. |
| `RockDetector` | Number | `10` | Applies the 'RockDetector' effect. |
| `SafeExplosions` | Number | `1` | Applies the 'SafeExplosions' effect. |
| `ScaledStatusOnBleedDamage` | Block | `{ ... }` | Applies the 'ScaledStatusOnBleedDamage' effect. |
| `ScaledStatusOnLoseShield` | Block | `{ ... }` | Applies the 'ScaledStatusOnLoseShield' effect. |
| `ScaledStatusOnOverHealed` | Block | `{ ... }` | Applies the 'ScaledStatusOnOverHealed' effect. |
| `ScaledStatusOnOverMana` | Block | `{ ... }` | Applies the 'ScaledStatusOnOverMana' effect. |
| `ScaledStatusOnSpendMana` | Block | `{ ... }` | Applies the 'ScaledStatusOnSpendMana' effect. |
| `SchrodingerDisorder` | Number | `50%` | Applies the 'SchrodingerDisorder' effect. |
| `Scleroderma` | Number | `1` | Applies the 'Scleroderma' effect. |
| `SecurityBotProtect` | Block | `{ ... }` | Applies the 'SecurityBotProtect' effect. |
| `SelfDamageWhenDealDamage` | Block | `{ ... }` | Applies the 'SelfDamageWhenDealDamage' effect. |
| `SetDefaultFacePassive` | Enum/String | `insane` | Applies the 'SetDefaultFacePassive' effect. |
| `SetSpellCosts` | Number | `1, 0, 3` | Applies the 'SetSpellCosts' effect. |
| `ShareHealthRegen` | Number | `1` | Applies the 'ShareHealthRegen' effect. |
| `SharePickups` | Number | `1` | Applies the 'SharePickups' effect. |
| `ShoulderCheck` | Number | `33%, 100%` | Applies the 'ShoulderCheck' effect. |
| `ShovingMatch` | Enum/String | `attack` | Applies the 'ShovingMatch' effect. |
| `ShowHiddenThings` | Number | `1` | Applies the 'ShowHiddenThings' effect. |
| `SizeScale` | Enum/String | `.4, 1.3, .7` | Applies the 'SizeScale' effect. |
| `Slow` | Number | `5` | Applies the 'Slow' effect. |
| `SmallEnemiesIgnoreYou` | Number | `1` | Applies the 'SmallEnemiesIgnoreYou' effect. |
| `SmallRockBehavior` | Number | `5` | Applies the 'SmallRockBehavior' effect. |
| `SmiteEnemiesWhoKill` | Block | `{ ... }` | Applies the 'SmiteEnemiesWhoKill' effect. |
| `SpawnCatCopyOnBattleStart` | Block | `{ ... }` | Applies the 'SpawnCatCopyOnBattleStart' effect. |
| `SpawnCreepOnHit` | Number | `1` | Applies the 'SpawnCreepOnHit' effect. |
| `SpawnEachTurn` | Block | `{ ... }` | Applies the 'SpawnEachTurn' effect. |
| `SpawnMeatOnMove` | Enum/String | `Food` | Applies the 'SpawnMeatOnMove' effect. |
| `SpawnObjectOnPopCorpse` | Enum/String | `Food` | Applies the 'SpawnObjectOnPopCorpse' effect. |
| `SpawnOnBattleStartRandomEmptyTile` | Block | `{ ... }` | Applies the 'SpawnOnBattleStartRandomEmptyTile' effect. |
| `SpawnOnBattleStart` | Enum/String | `BeefyCharmedLeech, CharmedTinySpider, { ... }` | Applies the 'SpawnOnBattleStart' effect. |
| `SpawnThingOnDamage` | Block | `{ ... }` | Applies the 'SpawnThingOnDamage' effect. |
| `SpawnThingOnDeath` | Enum/String | `CharmedDemonKitten, ZombieCatFamiliar` | Applies the 'SpawnThingOnDeath' effect. |
| `SpecialFriends` | Block | `{ ... }` | Applies the 'SpecialFriends' effect. |
| `SpeedUp` | Number | `6` | Applies the 'SpeedUp' effect. |
| `SplittableMove` | Number | `1, 3` | Applies the 'SplittableMove' effect. |
| `SpreadExtraDebuffs` | Number | `1, 2` | Applies the 'SpreadExtraDebuffs' effect. |
| `SpreadPainBonusCrit` | Number | `1` | Applies the 'SpreadPainBonusCrit' effect. |
| `SpreadPainBonus` | Number | `2` | Applies the 'SpreadPainBonus' effect. |
| `StackingDodgeChanceOnTookDamage` | Block | `{ ... }` | Applies the 'StackingDodgeChanceOnTookDamage' effect. |
| `StatMinimum` | Number | `5, 7` | Applies the 'StatMinimum' effect. |
| `StatsAtLowHealth` | Block | `{ ... }` | Applies the 'StatsAtLowHealth' effect. |
| `StatusAdjacentOnTheirTurnBegin` | Block | `{ ... }` | Event Trigger: Applies nested statuses to adjacent on their turn begin. |
| `StatusAfterCastSpell` | Block | `{ ... }` | Event Trigger: Applies nested statuses to after cast spell. |
| `StatusAlliesOnBattleStart` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies on battle start. |
| `StatusAlliesOnDeath` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies on death. |
| `StatusAlliesOnGainCoins` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies on gain coins. |
| `StatusAlliesOnKill` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies on kill. |
| `StatusAlliesOnSpendMana` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies on spend mana. |
| `StatusAlliesScaledByCursedOnDeath` | Block | `{ ... }` | Event Trigger: Applies nested statuses to allies scaled by cursed on death. |
| `StatusAllyWhenAllySpendsMana` | Block | `{ ... }` | Event Trigger: Applies nested statuses to ally when ally spends mana. |
| `StatusAnyCatAllyWhoKills` | Block | `{ ... }` | Event Trigger: Applies nested statuses to any cat ally who kills. |
| `StatusCarefulness` | Number | `1` | Event Trigger: Applies nested statuses to carefulness. |
| `StatusDamagers` | Block | `{ ... }` | Event Trigger: Applies nested statuses to damagers. |
| `StatusEachTurnBegin` | Block | `{ ... }` | Event Trigger: Applies nested statuses to each turn begin. |
| `StatusEachTurnEndForEachTurn` | Block | `{ ... }` | Event Trigger: Applies nested statuses to each turn end for each turn. |
| `StatusEachTurnEndPerEnemyKill` | Block | `{ ... }` | Event Trigger: Applies nested statuses to each turn end per enemy kill. |
| `StatusEachTurnEnd` | Block | `{ ... }` | Event Trigger: Applies nested statuses to each turn end. |
| `StatusEnemiesOnDeath` | Block | `{ ... }` | Event Trigger: Applies nested statuses to enemies on death. |
| `StatusEveryXSpellCasts` | Block | `{ ... }` | Event Trigger: Applies nested statuses to every x spell casts. |
| `StatusEveryXTurnBegins` | Block | `{ ... }` | Event Trigger: Applies nested statuses to every x turn begins. |
| `StatusIfBattleAlreadyBegan` | Block | `{ ... }` | Event Trigger: Applies nested statuses to if battle already began. |
| `StatusIfUnusedMovePoints` | Block | `{ ... }` | Event Trigger: Applies nested statuses to if unused move points. |
| `StatusImmunity` | Array | `[ Sleep SleepParalysis ], Burn, [ Fear Madness PermanentMadness ]` | Event Trigger: Applies nested statuses to immunity. |
| `StatusKilledCharacters` | Block | `{ ... }` | Event Trigger: Applies nested statuses to killed characters. |
| `StatusKillers` | Block | `{ ... }` | Instantly kills the target if they possess the specified status effects. |
| `StatusOnAllyCatDeath` | Block | `{ ... }` | Event Trigger: Applies nested statuses when ally cat death. |
| `StatusOnAnyDeath` | Block | `{ ... }` | Event Trigger: Applies nested statuses when any death. |
| `StatusOnBattleEndIfKillThresholdMet` | Block | `{ ... }` | Event Trigger: Applies nested statuses when battle end if kill threshold met. |
| `StatusOnBattleEnd` | Block | `{ ... }` | Applies the nested status effects when the encounter finishes. |
| `StatusOnBattleStart` | Block | `{ ... }` | Event Trigger: Applies nested statuses when battle start. |
| `StatusOnBreakItem` | Block | `{ ... }` | Event Trigger: Applies nested statuses when break item. |
| `StatusOnCastSpell` | Block | `{ ... }` | Event Trigger: Applies nested statuses when cast spell. |
| `StatusOnCollectPickup` | Block | `{ ... }` | Event Trigger: Applies nested statuses when collect pickup. |
| `StatusOnCrit` | Block | `{ ... }` | Event Trigger: Applies nested statuses when crit. |
| `StatusOnDealtDamageThreshold` | Block | `{ ... }` | Event Trigger: Applies nested statuses when dealt damage threshold. |
| `StatusOnDealtDamage` | Block | `{ ... }` | Event Trigger: Applies nested statuses when dealt damage. |
| `StatusOnEatFood` | Block | `{ ... }` | Event Trigger: Applies nested statuses when eat food. |
| `StatusOnEatPill` | Block | `{ ... }` | Event Trigger: Applies nested statuses when eat pill. |
| `StatusOnEndMove` | Block | `{ ... }` | Event Trigger: Applies nested statuses when end move. |
| `StatusOnGainCoins` | Block | `{ ... }` | Event Trigger: Applies nested statuses when gain coins. |
| `StatusOnGainShield` | Block | `{ ... }` | Event Trigger: Applies nested statuses when gain shield. |
| `StatusOnHeal` | Block | `{ ... }` | Event Trigger: Applies nested statuses when heal. |
| `StatusOnHealed` | Block | `{ ... }` | Event Trigger: Applies nested statuses when healed. |
| `StatusOnKillEnemy` | Block | `{ ... }` | Event Trigger: Applies nested statuses when kill enemy. |
| `StatusOnKill` | Block | `{ ... }` | Event Trigger: Applies nested statuses when kill. |
| `StatusOnLoseShield` | Block | `{ ... }` | Event Trigger: Applies nested statuses when lose shield. |
| `StatusOnOverHealed` | Block | `{ ... }` | Event Trigger: Applies nested statuses when over healed. |
| `StatusOnOverMana` | Block | `{ ... }` | Event Trigger: Applies nested statuses when over mana. |
| `StatusOnPickupCoins` | Block | `{ ... }` | Event Trigger: Applies nested statuses when pickup coins. |
| `StatusOnPopCorpse` | Block | `{ ... }` | Event Trigger: Applies nested statuses when pop corpse. |
| `StatusOnStanceSwitch` | Block | `{ ... }` | Event Trigger: Applies nested statuses when stance switch. |
| `StatusOnTakeHealthDamage` | Block | `{ ... }` | Event Trigger: Applies nested statuses when take health damage. |
| `StatusOnTookDamageFromAbility` | Block | `{ ... }` | Event Trigger: Applies nested statuses when took damage from ability. |
| `StatusOnTookDamageFromEnemyAbility` | Block | `{ ... }` | Event Trigger: Applies nested statuses when took damage from enemy ability. |
| `StatusOnTookDamage` | Block | `{ ... }` | Event Trigger: Applies nested statuses when took damage. |
| `StatusOnTriggerTrap` | Block | `{ ... }` | Event Trigger: Applies nested statuses when trigger trap. |
| `StatusOnTurnEndIfCastNSpells` | Block | `{ ... }` | Event Trigger: Applies nested statuses when turn end if cast n spells. |
| `StatusOnTurnEndIfDidntCastAbilityTypes` | Block | `{ ... }` | Event Trigger: Applies nested statuses when turn end if didnt cast ability types. |
| `StatusOnTurnEndIfManaExact` | Block | `{ ... }` | Event Trigger: Applies nested statuses when turn end if mana exact. |
| `StatusOnTurnEndIfManaOrHealthExact` | Block | `{ ... }` | Event Trigger: Applies nested statuses when turn end if mana or health exact. |
| `StatusOnUseAbilityWithTag` | Block | `{ ... }` | Event Trigger: Applies nested statuses when use ability with tag. |
| `StatusOnUseBasicAttack` | Block | `{ ... }` | Event Trigger: Applies nested statuses when use basic attack. |
| `StatusOnUseElementAbility` | Block | `{ ... }` | Event Trigger: Applies nested statuses when use element ability. |
| `StatusPerInjury` | Block | `{ ... }` | Event Trigger: Applies nested statuses to per injury. |
| `StatusReplacement` | Array | `[ Petrify PetrifyCharmed ]` | Event Trigger: Applies nested statuses to replacement. |
| `StatusThingsKnockedBack` | Block | `{ ... }` | Event Trigger: Applies nested statuses to things knocked back. |
| `StatusWhenAllySpendsMana` | Block | `{ ... }` | Event Trigger: Applies nested statuses to when ally spends mana. |
| `Stealth` | Number | `1` | Applies the 'Stealth' effect. |
| `StrengthForEachNeighboringEnemy` | Number | `2, 3` | Applies the 'StrengthForEachNeighboringEnemy' effect. |
| `StrengthInNumbersAura` | Number | `1, { ... }` | Applies the 'StrengthInNumbersAura' effect. |
| `StrengthUp` | Number | `2` | Applies the 'StrengthUp' effect. |
| `StrictLimitDamage` | Number | `1` | Applies the 'StrictLimitDamage' effect. |
| `Study` | Number | `1, { ... }` | Applies the 'Study' effect. |
| `TaggedPickupEffectReplacement` | Block | `{ ... }` | Applies the 'TaggedPickupEffectReplacement' effect. |
| `TauntAlways` | Number | `1` | Applies the 'TauntAlways' effect. |
| `TauntAtFullHealth` | Number | `1` | Applies the 'TauntAtFullHealth' effect. |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |
| `TempInitiativeChange` | Number | `-999` | Applies the 'TempInitiativeChange' effect. |
| `TheHunger` | Block | `{ ... }` | Applies the 'TheHunger' effect. |
| `Thorns` | Number | `2, 4` | Applies the 'Thorns' effect. |
| `TileDamageMultiplier` | Number | `2, { ... }` | Applies the 'TileDamageMultiplier' effect. |
| `TileTrail` | Enum/String | `FlowerTile, GrassTile` | Applies the 'TileTrail' effect. |
| `TourettesMeows` | Block | `{ ... }` | Applies the 'TourettesMeows' effect. |
| `TowerDefenseReflex` | Enum/String | `attack, BasicRanged_1DMG` | Applies the 'TowerDefenseReflex' effect. |
| `TowerDefense` | Block | `{ ... }` | Applies the 'TowerDefense' effect. |
| `Trample` | Number | `9, 3` | Applies the 'Trample' effect. |
| `TrapEffectsMultiplier` | Number | `2` | Applies the 'TrapEffectsMultiplier' effect. |
| `TrinketActiveEffectsMultiplierBonus` | Number | `1, 2` | Applies the 'TrinketActiveEffectsMultiplierBonus' effect. |
| `TrinketPassiveMultiplierBonus` | Number | `1, 2` | Applies the 'TrinketPassiveMultiplierBonus' effect. |
| `Triskaidekaphobia` | Number | `13` | Applies the 'Triskaidekaphobia' effect. |
| `UncappedHPBonusStr` | Number | `5` | Applies the 'UncappedHPBonusStr' effect. |
| `UncappedHP` | Number | `1` | Applies the 'UncappedHP' effect. |
| `UncappedMana` | Number | `1` | Applies the 'UncappedMana' effect. |
| `UpgradeLevelUpClassActives` | Enum/String | `Colorless` | Applies the 'UpgradeLevelUpClassActives' effect. |
| `UpgradeLevelUpClassPassives` | Enum/String | `Colorless` | Applies the 'UpgradeLevelUpClassPassives' effect. |
| `UpgradeSpawnedPickups` | Number | `1, 2` | Applies the 'UpgradeSpawnedPickups' effect. |
| `Vegan` | Number | `1` | Applies the 'Vegan' effect. |
| `Vengeful` | Number | `1` | Applies the 'Vengeful' effect. |
| `WaterWalk` | Number | `1` | Applies the 'WaterWalk' effect. |
| `Weakness` | Number | `1, 5` | Applies the 'Weakness' effect. |
| `WeaponActiveEffectsMultiplierBonus` | Number | `2` | Applies the 'WeaponActiveEffectsMultiplierBonus' effect. |
| `WeaponCountsAsBasicAttack` | Number | `1` | Applies the 'WeaponCountsAsBasicAttack' effect. |
| `WeaponDamageMultiplierBonus` | Number | `2` | Applies the 'WeaponDamageMultiplierBonus' effect. |
| `WeaponPassiveMultiplierBonus` | Number | `2` | Applies the 'WeaponPassiveMultiplierBonus' effect. |
| `WeaponsDontLoseDurability` | Number | `0` | Applies the 'WeaponsDontLoseDurability' effect. |
| `WobblyCat` | Number | `25%` | Applies the 'WobblyCat' effect. |

### Context: `schadenfreude_scaled_stats`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `con` | Number | `2` |  |
| `dex` | Number | `2` |  |
| `int` | Number | `2` |  |
| `lck` | Number | `2` |  |
| `spd` | Number | `2` |  |
| `str` | Number | `2` |  |

### Context: `spell_graphics_override`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `area_particle` | Enum/String | `WaterConduct` |  |
| `center_particle` | Enum/String | `WaterConduct` |  |
| `palette` | Number | `-1` |  |
| `particle` | Enum/String | `WaterConduct` |  |

### Context: `stats`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2, 4, 3` |  |
| `con` | Number | `2, -1, -2` |  |
| `dex` | Number | `6, -1, 3` |  |
| `int` | Number | `2, -1, -2` |  |
| `lck` | Number | `1, 2, 4` |  |
| `spd` | Number | `1, 2, 3` |  |
| `str` | Number | `2, -1, 4` |  |

### Context: `statuses`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `FindItemFromPool` | Enum/String | `consumables, chapter` | Generates an item drop from the specified loot pool. |
| `HealthGain` | Number | `10` | Applies the 'HealthGain' effect. |
| `PermanentDexterity` | Number | `1` | Applies the 'PermanentDexterity' effect. |

### Context: `threshold`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `0` |  |
| `int` | Number | `-10, 0, 4` |  |
| `spd` | Number | `0` |  |

### Context: `triattack`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `6` | The base damage properties of an attack. |
| `effects` | Block | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `elements` | Array | `[ Fire Ice Electric ]` |  |
| `type` | Enum/String | `spell` | The classification type (e.g., damage type or element). |

---

## Spawns & Enemy Pools

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `#` | Enum/String | `ID` |  |
| `early_spawn` | Boolean | `true` |  |
| `editor` | Block | `{ ... }` |  |
| `empty!` | Enum/String | `editor` |  |
| `forced_placement` | Boolean | `true` |  |
| `image` | String | `"empty.png"` |  |
| `name` | String | `"Empty"` |  |
| `object` | Enum/String | `Rat, Fly, Worm` |  |
| `orientation` | Enum/String | `south, north, east` |  |
| `reserved` | Enum/String | `for` |  |
| `tag_location` | Enum/String | `FinalBossCloneSpot, ChaosValidPosition, HitlerMiniInitial` |  |
| `trap` | Enum/String | `WaterKittenTrap, WebTrap` |  |
| `utility` | Enum/String | `PlayerSpawn` |  |
| `value` | Number | `1, 0, .5` |  |
| `weather_element_alt` | Block | `{ ... }` |  |

### Context: `editor`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `category` | Number | `1, 4, 3` |  |
| `image_tint` | Array | `[ blue ], [ yellow ], [ blue none ]` |  |
| `image` | Array | `[ "rat.png" ], [ "shadow.png" "cat.png" ], [ "fly.png" ]` |  |
| `layer` | Number | `2` |  |
| `name` | String | `"Player Cat Spawn", "Rat", "Fly"` |  |
| `paint` | Boolean | `false, true` |  |
| `subcategory` | Number | `1, 2, 3` |  |

### Context: `weather_element_alt`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `element` | Enum/String | `Ice` | Specific element type required or applied. |
| `object` | Enum/String | `IceElemental` |  |

---

## Status Effect Keywords

### Context: `ROOT`
| Property Key | Inferred Type | Example Values | Definition |
| :--- | :--- | :--- | :--- |
| `alias` | Enum/String | `DodgeChance_Status, Infested, AllStatsUp` |  |
| `icon_frame` | Number | `152, 17, 141` |  |
| `name_reference_applier` | String | `"KEYWORD_MANALEECHES_NAME_APPLIER", "KEYWORD_ATTRACTION_REF", "KEYWORD_LEECHES_NAME_APPLIER"` |  |
| `name_stacks_neg` | String | `"KEYWORD_CONDOWN_NAME", "KEYWORD_ALLSTATSDOWN_NAME", "KEYWORD_CHADOWN_NAME"` |  |
| `name` | String | `"KEYWORD_ALPHA_NAME", "KEYWORD_ADRENALINE_NAME", "KEYWORD_ALLSTATSUP_NAME"` |  |
| `tooltip_reference_applier` | String | `"KEYWORD_MANALEECHES_DESC_APPLIER", "KEYWORD_LEECHES_DESC_APPLIER", "KEYWORD_ATTRACTION_DESC_REF"` |  |
| `tooltip_stackless_neg` | String | `"KEYWORD_TEMPINITDOWN_DESC", "KEYWORD_MOVEMENTDOWN_DESC_STACKLESS", "KEYWORD_DAMAGEDOWN_DESC_STACKLESS"` |  |
| `tooltip_stackless_pos` | String | `"KEYWORD_DAMAGEUP_DESC_STACKLESS", "KEYWORD_MOVEMENTUP_DESC_STACKLESS"` |  |
| `tooltip_stackless` | String | `"KEYWORD_ALPHA_DESC_STACKLESS", none, "KEYWORD_ATTRACTION_DESC_STACKLESS"` |  |
| `tooltip_stacks_neg` | String | `"KEYWORD_CHADOWN_DESC", "KEYWORD_PERMABLIND_DESC", "KEYWORD_ALLSTATSDOWN_DESC"` |  |
| `tooltip_stacks_pos` | String | `"KEYWORD_ALLSTATSUP_DESC", "KEYWORD_CONUP_DESC", "KEYWORD_CHAUP_DESC"` |  |
| `tooltip_stacks_singular` | String | `"KEYWORD_COUNTER_DESC", "KEYWORD_CHARGEFISTS_DESC_SINGULAR", "KEYWORD_BLIND_DESC_STACKLESS"` |  |
| `tooltip_stacks` | String | `"KEYWORD_AMMO_DESC", "KEYWORD_ATTRACTION_DESC", "KEYWORD_BLASTRESISTANCE_DESC"` |  |
| `tooltip` | String | `"KEYWORD_ADRENALINE_DESC", "KEYWORD_BACKFLIP_DESC", "KEYWORD_ALPHA_DESC"` |  |

---
