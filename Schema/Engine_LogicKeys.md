# Mewgenics Mod Developer Documentation: Engine: Logic Keys

## Engine: Logic Keys

This document is the authoritative reference for Logic Blocks. All of the contexts below can appear as dynamic keys inside an `effects {}` block, or directly inside abilities. Many of these are conditional wrappers that evaluate a condition before executing their nested block, while others redirect execution flow (e.g. `ApplyToSource`).

> **Note:** Because many of these contexts accept arbitrary nested Logic Blocks, any entry marked `{Logic Keys}` recursively refers back to this same document.

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-root), [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`temporary_effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temporary_effects), [`Else` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-else), [`ApplyToSource` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_ally), [`Consumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-consumed), [`Conditional_Boss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_speculative), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`Conditional_Corpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_playercat), [`ApplyToConsumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytoconsumed), [`TimeDelayStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-post_spawn_statuses), [`Conditional_AffectedByElement` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_lasthit), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`ApplyToTile` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytotile), [`Conditional_BadRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_DestructibleCorpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_destructiblecorpse), [`Conditional_Displaceable` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_displaceable), [`Conditional_IsSelf` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_isself), [`Conditional_OncePerBattle` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_shielded), [`ApplyToRandomClosestAlly` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandomclosestally), [`Conditional_Backstab` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_backstab), [`Conditional_FinishedSpawning` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_finishedspawning), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Conditional_IsTrample` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_istrample), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_NotBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notbig), [`Conditional_RandomChance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_randomchance), [`NextBattleStatusStacks` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-nextbattlestatusstacks), [`ROOT` (Boss_Cutscene_Info)](./Boss_Cutscene_Info.md#context-root), [`ROOT` (Cat_Classes)](./Cat_Classes.md#context-root), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`Conditional_RandomChance` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_randomchance), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_goodroll), [`ROOT` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-root), [`FormChanger` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-formchanger), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`Consumed` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-consumed), [`Conditional_GoodRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_goodroll), [`Conditional_BadRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-else), [`FinalBossBecomeTheChild` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbossbecomethechild), [`InfiniteRebirth` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-infiniterebirth), [`TVBotScreen` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-tvbotscreen), [`ROOT` (Custom_Cats)](./Custom_Cats.md#context-root), [`ROOT` (Damage_Text_Styles)](./Damage_Text_Styles.md#context-root), [`ROOT` (Difficulties)](./Difficulties.md#context-root), [`ROOT` (Elite_Buffs)](./Elite_Buffs.md#context-root), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`ROOT` (Enemy_AI)](./Enemy_AI.md#context-root), [`ROOT` (Events_and_Encounters)](./Events_and_Encounters.md#context-root), [`global_effect_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-global_effect_next_fight), [`ROOT` (Furniture_and_Metaprogression)](./Furniture_and_Metaprogression.md#context-root), [`ROOT` (House_and_Environment)](./House_and_Environment.md#context-root), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`Else` (House_and_Environment)](./House_and_Environment.md#context-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundend), [`Conditional_GoodRoll` (House_and_Environment)](./House_and_Environment.md#context-conditional_goodroll), [`Conditional_Corpse` (House_and_Environment)](./House_and_Environment.md#context-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](./House_and_Environment.md#context-conditional_partymember), [`ROOT` (Injuries)](./Injuries.md#context-root), [`ROOT` (Items_and_Equipment)](./Items_and_Equipment.md#context-root), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`Conditional_GoodRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_goodroll), [`ApplyToSource` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytosource), [`Conditional_HasStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else` (Items_and_Equipment)](./Items_and_Equipment.md#context-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`Conditional_PartyMember` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_partymember), [`Conditional_Adjacent` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_onceperbattle), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytorandompartymemberifpossible), [`CastAgainWithStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-castagainwithstatus), [`Conditional_Ally` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_enemy), [`Conditional_HasCleansableDebuffs` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`Conditional_HealthThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_healththreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_shielded), [`CyborgTurns` (Items_and_Equipment)](./Items_and_Equipment.md#context-cyborgturns), [`ScaldingOrbMoonBossOneShot` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot), [`StatusAdjacentOnTheirTurnEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusadjacentontheirturnend), [`StatusOnFallAsleep` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonfallasleep), [`StatusOnTurnEndIfCastNSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifcastnspells), [`ROOT` (Item_Pools)](./Item_Pools.md#context-root), [`ROOT` (Map_Generation_and_Routing)](./Map_Generation_and_Routing.md#context-root), [`ROOT` (Miscellaneous)](./Miscellaneous.md#context-root), [`ROOT` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-root), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects), [`StatusOnStanceSwitch` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonstanceswitch), [`Conditional_Ally` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_enemy), [`Else` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-else), [`StatusOnOverHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonoverhealed), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaexact), [`Conditional_BadRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hasstatus), [`AddStatusToBasicAttackWithCooldown` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicattackwithcooldown), [`AddStatusToMeleeDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustomeleedamage), [`ApplyToSource` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applytosource), [`Conditional_Adjacent` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_shielded), [`EscapeSequence` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-escapesequence), [`InfiniteRebirth` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-infiniterebirth), [`StatusOnDealtDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamage), [`on_throw` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-on_throw), [`Conditional_GoodRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_goodroll), [`StatusAdjacentOnTheirTurnBegin` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin), [`ROOT` (Progression_Unlocks)](./Progression_Unlocks.md#context-root), [`ROOT` (Shops)](./Shops.md#context-root), [`ROOT` (Spawns_and_Enemy_Pools)](./Spawns_and_Enemy_Pools.md#context-root), [`ROOT` (Status_Effect_Keywords)](./Status_Effect_Keywords.md#context-root)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| `AIFavorLowHealth` | Integer | Applies or references the 'AIFavorLowHealth' effect/state. |
| `AcidRain` | Integer |  |
| `AddExtraTurnsBeforeRun` | Integer |  |
| `AddLeechesStatus` | Integer | Applies or references the 'AddLeechesStatus' effect/state. |
| [`AddPostProcessEffect`](#addpostprocesseffect) | Block |  |
| `AddSpiritBombCharges` | Integer | Applies or references the 'AddSpiritBombCharges' effect/state. |
| [`AddTilesetObjects`](#addtilesetobjects) | Block |  |
| `AddWeaponAux` | Integer | Applies or references the 'AddWeaponAux' effect/state. |
| `Adrenaline` | Integer | Applies or references the 'Adrenaline' effect/state. |
| `AllStatsUp` | Integer | Applies or references the 'AllStatsUp' effect/state. |
| `AlliesTakeExtraTurn` | Integer | Applies or references the 'AlliesTakeExtraTurn' effect/state. |
| [`AllyInfested`](#allyinfested) | Block |  |
| `AlphaCat` | Integer | Applies or references the 'AlphaCat' effect/state. |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Applies or references the 'AlternateIdleAnimation' effect/state. |
| `Ammo` | Integer | Applies or references the 'Ammo' effect/state. |
| [`ApplyMultipleTimes`](#applymultipletimes) | Block | A loop block that executes its nested logic multiple times. |
| [`ApplyPassives`](#applypassives) | Block | Grants the nested passive abilities dynamically. |
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. |
| [`ApplyStatusIfCrit`](#applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. |
| [`ApplyStatusesNextTurnBegin`](#applystatusesnextturnbegin) | Block | Delays the application of the nested status effects until the start of the target's next turn. |
| [`ApplyToConsumed`](#applytoconsumed) | Block | Redirects the nested effects to apply to the entity that just consumed this object. |
| [`ApplyToOthersWithSharedTagAndFaction`](#applytootherswithsharedtagandfaction) | Block | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. |
| [`ApplyToRandomClosestAlly`](#applytorandomclosestally) | Block | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. |
| [`ApplyToRandomPartyMemberIfPossible`](#applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. |
| [`ApplyToSource`](#applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| [`ApplyToSourceOnKill`](#applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. |
| [`ApplyToTile`](#applytotile) | Block | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. |
| [`ArcLightning`](#arclightning) | Block | Executes a chain-lightning logic block that bounces between targets. |
| `Attraction` | Integer | Applies or references the 'Attraction' effect/state. |
| `AutoReanimate` | Integer |  |
| `BackflipWhenTargeted` | Integer | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BlackHoleSuck` | Integer | Applies or references the 'BlackHoleSuck' effect/state. |
| `Bleed` | Integer | Applies or references the 'Bleed' effect/state. |
| `BleedThorns` | Integer | Applies or references the 'BleedThorns' effect/state. |
| `Blind` | Integer | Applies or references the 'Blind' effect/state. |
| `Bloodzerked` | Integer | Applies or references the 'Bloodzerked' effect/state. |
| [`BodyGuard`](#bodyguard) | Block | Protects an ally by intercepting attacks directed at them. |
| `BombRatTurtle` | Integer | Applies or references the 'BombRatTurtle' effect/state. |
| `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. |
| `BonusDamage` | Integer | Applies or references the 'BonusDamage' effect/state. |
| `BonusDamageBasedOnDistance` | Integer | Applies or references the 'BonusDamageBasedOnDistance' effect/state. |
| `BonusDamageBasedOnMana` | Integer | Applies or references the 'BonusDamageBasedOnMana' effect/state. |
| `BonusKnockbackDamage` | Integer | Applies or references the 'BonusKnockbackDamage' effect/state. |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | Spawns a physics object that visually bounces off the target. |
| [`BounceRock`](./Enums.md#enum-bouncerock) | Enum | Applies or references the 'BounceRock' effect/state. |
| `Bound` | Integer | Applies or references the 'Bound' effect/state. |
| `Brace` | Integer | Applies or references the 'Brace' effect/state. |
| `BramblesOnHit` | Integer | Applies or references the 'BramblesOnHit' effect/state. |
| `Bruise` | Integer | Applies or references the 'Bruise' effect/state. |
| `BurgleCoin` | Integer | Applies or references the 'BurgleCoin' effect/state. |
| `Burn` | Integer | Applies or references the 'Burn' effect/state. |
| `ButterflySwarm` | Integer |  |
| `BypassRockKnockback` | Integer | Applies or references the 'BypassRockKnockback' effect/state. |
| [`CanApplyToInanimate`](#canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `CancelPrimedAbilities` | Integer | Applies or references the 'CancelPrimedAbilities' effect/state. |
| `CanceledQueuedInput` | Integer | Applies or references the 'CanceledQueuedInput' effect/state. |
| `CapDamage` | Integer | Applies or references the 'CapDamage' effect/state. |
| `CaptureFamiliar` | Integer | Applies or references the 'CaptureFamiliar' effect/state. |
| [`CatPartsSizeScaleStatus`](#catpartssizescalestatus) | Block | Visually scales specific body parts of a character. |
| [`CatPartsTransform`](#catpartstransform) | Block | Transforms specific body parts into different visual variants. |
| `ChampionUpgradeNextMinion` | Integer | Applies or references the 'ChampionUpgradeNextMinion' effect/state. |
| `ChanceToBreak` | Integer | Applies or references the 'ChanceToBreak' effect/state. |
| [`ChanceToBreakFree`](#chancetobreakfree) | Block | Provides a probability to escape a grapple or restraining effect. |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Applies or references the 'ChangeCatClass' effect/state. |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Applies or references the 'ChangeFaction' effect/state. |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | Transforms the terrain tile under the target. |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Applies or references the 'ChangeTilesUnder' effect/state. |
| `ChaosBossFlipMidTeleport` | Integer | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. |
| `ChaosBossFormChange` | Integer | Applies or references the 'ChaosBossFormChange' effect/state. |
| [`CharacterTypeGainsStatusAtBattleStart`](#charactertypegainsstatusatbattlestart) | Block |  |
| `Charge` | Integer | Applies or references the 'Charge' effect/state. |
| `ChargeFists` | Integer | Applies or references the 'ChargeFists' effect/state. |
| `CharismaUp` | Integer | Applies or references the 'CharismaUp' effect/state. |
| `Charmed` | Integer | Applies or references the 'Charmed' effect/state. |
| `CharmedFacingForceAttack` | Integer | Applies or references the 'CharmedFacingForceAttack' effect/state. |
| `CharmedForceAttack` | Integer | Applies or references the 'CharmedForceAttack' effect/state. |
| `Cleanse` | Integer | Applies or references the 'Cleanse' effect/state. |
| `ClearDefaultDebris` | Integer |  |
| `ClearFinalBossBattlefield` | Integer | Applies or references the 'ClearFinalBossBattlefield' effect/state. |
| `ClearNegativeEffects` | Integer | Applies the 'ClearNegativeEffects' effect. |
| `ClearStarving` | Integer | Applies or references the 'ClearStarving' effect/state. |
| `Cleave` | Integer | Causes the attack to hit adjacent enemies alongside the primary target. |
| `CloneWeaponTemp` | Integer | Applies or references the 'CloneWeaponTemp' effect/state. |
| `CockroachSwarm` | Integer |  |
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum | Applies or references the 'CoinTossBounce' effect/state. |
| `CollectsPickups` | Integer | Applies or references the 'CollectsPickups' effect/state. |
| [`CollectsPickupsWithAltEffects`](#collectspickupswithalteffects) | Block | Triggers alternative nested effects when collecting items or pickups. |
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | Applies or references the 'CollideWithConsumed' effect/state. |
| `CollideWithThrowTarget` | Integer | Applies or references the 'CollideWithThrowTarget' effect/state. |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Applies or references the 'CompleteItemQuest' effect/state. |
| [`Conditional_AbilityTargetIsSelf`](#conditional_abilitytargetisself) | Block | Conditional constraint. Nested properties only trigger if this is true. |
| [`Conditional_ActiveWeather_Any`](#conditional_activeweather_any) | Block | Conditional trigger: Executes nested logic if the current map weather matches any in the list. |
| [`Conditional_AffectedByElement`](#conditional_affectedbyelement) | Block | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. |
| [`Conditional_Ally`](#conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| [`Conditional_Backstab`](#conditional_backstab) | Block | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. |
| [`Conditional_BadRoll`](#conditional_badroll) | Block | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. |
| [`Conditional_Boss`](#conditional_boss) | Block | Conditional trigger: Executes nested logic if the target is a Boss. |
| [`Conditional_BossOrBig`](#conditional_bossorbig) | Block | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. |
| [`Conditional_Buddy`](#conditional_buddy) | Block | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. |
| [`Conditional_CanBeHealed`](#conditional_canbehealed) | Block | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| [`Conditional_DebuffRoll`](#conditional_debuffroll) | Block | Conditional trigger: Executes nested logic based on a randomized debuff probability. |
| [`Conditional_DestructibleCorpse`](#conditional_destructiblecorpse) | Block | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. |
| [`Conditional_Displaceable`](#conditional_displaceable) | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| [`Conditional_Familiar`](#conditional_familiar) | Block | Conditional trigger: Executes nested logic if the target is a familiar. |
| [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. |
| [`Conditional_FormulaIsPositive`](#conditional_formulaispositive) | Block | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| [`Conditional_HasCleansableDebuffs`](#conditional_hascleansabledebuffs) | Block | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. |
| [`Conditional_HasKnockback`](#conditional_hasknockback) | Block | Conditional: Executes logic if the triggering attack deals knockback. |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| [`Conditional_InForm`](#conditional_inform) | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. |
| [`Conditional_IsSelf`](#conditional_isself) | Block | Conditional trigger: Executes nested logic if the target is the caster themselves. |
| [`Conditional_IsTrample`](#conditional_istrample) | Block | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. |
| [`Conditional_LastHit`](#conditional_lasthit) | Block | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. |
| [`Conditional_LivingPlayerCat`](#conditional_livingplayercat) | Block | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. |
| [`Conditional_NotAlly`](#conditional_notally) | Block | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. |
| [`Conditional_NotBig`](#conditional_notbig) | Block | Conditional trigger: Executes nested logic if the target is NOT classified as large. |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Block | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. |
| [`Conditional_NotShielded`](#conditional_notshielded) | Block | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. |
| [`Conditional_Object`](#conditional_object) | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Block | Conditional trigger: Executes nested logic only once per encounter/battle. |
| [`Conditional_PartyMember`](#conditional_partymember) | Block | Conditional block: Executes nested logic only if the target is/has PartyMember. |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Conditional trigger: Executes nested logic if the target is a player-controlled cat. |
| [`Conditional_RandomChance`](#conditional_randomchance) | Block | Conditional trigger: Executes nested logic based on a flat percentage random roll. |
| [`Conditional_Shielded`](#conditional_shielded) | Block | Conditional trigger: Executes nested logic if the target currently has a Shield status. |
| [`Conditional_SourceAbilityHasTag`](#conditional_sourceabilityhastag) | Block | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. |
| [`Conditional_SourceHasStatus`](#conditional_sourcehasstatus) | Block | Conditional trigger: Executes nested logic if the caster currently has the specified status. |
| [`Conditional_Speculative`](#conditional_speculative) | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. |
| `Confusion` | Integer | Applies or references the 'Confusion' effect/state. |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum | Adds a temporary bonus ability to the character's hand/deck. |
| `ConjureRandomAbilityFromCat` | Integer | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. |
| `ConstitutionUp` | Integer | Applies or references the 'ConstitutionUp' effect/state. |
| [`Consumed`](#consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. |
| `ContextualHeal` | Integer | Applies or references the 'ContextualHeal' effect/state. |
| `CopySpells` | Integer | Duplicates existing spells currently in the character's hand. |
| `CorpseVaporizer` | Integer | Applies or references the 'CorpseVaporizer' effect/state. |
| `Counterspell` | Integer | Applies or references the 'Counterspell' effect/state. |
| `CrackMoonHead` | Integer | Applies or references the 'CrackMoonHead' effect/state. |
| [`Craft`](#craft) | Block | Synthesizes or spawns a new item from a specific pool. |
| [`CreateGlobalModifiers`](#createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. |
| `CritChanceUp` | Integer | Applies or references the 'CritChanceUp' effect/state. |
| `CurrentWeaponAddElectricElement` | Integer | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. |
| `CurrentWeaponDamageUp` | Integer | Applies or references the 'CurrentWeaponDamageUp' effect/state. |
| `DamageBasedOnMissingHealth` | Integer | Applies or references the 'DamageBasedOnMissingHealth' effect/state. |
| `DamageDistanceAOEFalloff` | Integer | Applies or references the 'DamageDistanceAOEFalloff' effect/state. |
| `DamageOrHealConditionally` | Integer | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `DamageTrinket` | Integer | Applies or references the 'DamageTrinket' effect/state. |
| `DamageUp` | Integer | Applies or references the 'DamageUp' effect/state. |
| `DamageWeapon` | Integer | Applies or references the 'DamageWeapon' effect/state. |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Applies or references the 'DeathwormUnderground' effect/state. |
| `DecoySwapper` | Integer | Applies or references the 'DecoySwapper' effect/state. |
| `DeferVaporize` | Integer | Applies or references the 'DeferVaporize' effect/state. |
| [`DelayCastAbility`](./Enums.md#enum-delaycastability) | Enum | Queues an ability to be cast automatically after a certain delay or trigger. |
| `DelayedFury` | Integer | Applies or references the 'DelayedFury' effect/state. |
| [`DelayedWindCone`](#delayedwindcone) | Block | Creates a delayed Area of Effect cone. |
| `DeleteInanimateObjectsChance` | Integer |  |
| `DeleteObject` | Integer | Applies or references the 'DeleteObject' effect/state. |
| `DeleteTraps` | Integer | Applies or references the 'DeleteTraps' effect/state. |
| [`DestroyEquipmentAndAttachParasite`](#destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DestroyNeckArmor` | Integer | Applies or references the 'DestroyNeckArmor' effect/state. |
| `DestroyTrinket` | Integer | Applies or references the 'DestroyTrinket' effect/state. |
| `DestroyWeapon` | Integer | Applies or references the 'DestroyWeapon' effect/state. |
| `DestroyWeaponThrow` | Integer | Applies or references the 'DestroyWeaponThrow' effect/state. |
| `DexterityUp` | Integer | Applies or references the 'DexterityUp' effect/state. |
| `Die` | Integer | Applies or references the 'Die' effect/state. |
| `DieViaAbilityInternally` | Integer | Applies or references the 'DieViaAbilityInternally' effect/state. |
| `DieViolently` | Integer | Applies or references the 'DieViolently' effect/state. |
| `DiminishingHealthRegen` | Integer | Applies or references the 'DiminishingHealthRegen' effect/state. |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Applies or references the 'DinoLegAnimation' effect/state. |
| `DisableWeapon` | Integer | Applies or references the 'DisableWeapon' effect/state. |
| `Disguised` | Integer | Applies or references the 'Disguised' effect/state. |
| `Displace` | Integer | Applies or references the 'Displace' effect/state. |
| `DisplaceToAbilityTarget` | Integer | Applies or references the 'DisplaceToAbilityTarget' effect/state. |
| `DisplaceToOriginalPosition` | Integer | Applies or references the 'DisplaceToOriginalPosition' effect/state. |
| `DisplaceTowardsSource` | Integer | Applies or references the 'DisplaceTowardsSource' effect/state. |
| `DissolveRandomArmorPiece` | Integer | Applies or references the 'DissolveRandomArmorPiece' effect/state. |
| `DivineShield` | Integer | Applies or references the 'DivineShield' effect/state. |
| [`DoDamage`](#dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. |
| [`DoDistortionRing`](#dodistortionring) | Block | Creates a visual distortion ring effect on the screen. |
| [`DoScreenShake`](#doscreenshake) | Block | Triggers a camera screen shake effect. |
| `DodgeChance_Status` | Integer | Applies or references the 'DodgeChance_Status' effect/state. |
| `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. |
| `Doomed` | Integer | Applies or references the 'Doomed' effect/state. |
| `DoubleCast` | Integer | Applies or references the 'DoubleCast' effect/state. |
| `DoubleCastSpell` | Integer | Applies or references the 'DoubleCastSpell' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Integer | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. |
| `DoubleLoot` | Integer | Applies or references the 'DoubleLoot' effect/state. |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | Applies or references the 'DoubleStatus' effect/state. |
| `DrainAllyCatsForFleshGolem` | Integer | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. |
| `DrinkWater` | Integer | Applies or references the 'DrinkWater' effect/state. |
| `Drowsy` | Integer | Applies or references the 'Drowsy' effect/state. |
| `DuplicateRandomEquippedItem` | Integer | Applies or references the 'DuplicateRandomEquippedItem' effect/state. |
| [`DustOnHit`](#dustonhit) | Block | Spawns a specific particle or cloud object upon impact. |
| [`DybbukPossessed`](#dybbukpossessed) | Block | Defines the abilities and behaviors available when possessing another entity. |
| `EliteUpgradeNextMinion` | Integer | Applies or references the 'EliteUpgradeNextMinion' effect/state. |
| [`Else`](#else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `EmptyMind` | Integer | Applies or references the 'EmptyMind' effect/state. |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Applies or references the 'EnableWeather' effect/state. |
| `EndTurn` | Integer | Applies or references the 'EndTurn' effect/state. |
| `Enlarge` | Integer | Applies or references the 'Enlarge' effect/state. |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Applies or references the 'EnterMount' effect/state. |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | Applies or references the 'EquipPermanentItem' effect/state. |
| `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `ExistUntilIdleUpkeep` | Integer | Applies or references the 'ExistUntilIdleUpkeep' effect/state. |
| `ExplodeCharacter` | Integer | Applies or references the 'ExplodeCharacter' effect/state. |
| `ExplodeCharacter_DeathBloom` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. |
| `ExplodeCharacter_DeathBloom2` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. |
| `ExplodeCharacter_NoDie` | Integer | Applies or references the 'ExplodeCharacter_NoDie' effect/state. |
| `ExplodeCharacter_Party` | Integer | Applies or references the 'ExplodeCharacter_Party' effect/state. |
| `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. |
| `ExplodeCharacter_RockCrusher` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. |
| `ExplosionIfHitSomething` | Integer | Applies or references the 'ExplosionIfHitSomething' effect/state. |
| `ExtraBasicAttacks_Status` | Integer | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraBasicMoves_Status` | Integer | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `FaceAway` | Integer | Applies or references the 'FaceAway' effect/state. |
| `FaceCamera` | Integer | Applies or references the 'FaceCamera' effect/state. |
| `FactionConversion` | Integer | Applies or references the 'FactionConversion' effect/state. |
| `FactionDisguiseSource` | Integer | Applies or references the 'FactionDisguiseSource' effect/state. |
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum |  |
| `FastKnockback` | Integer | Applies or references the 'FastKnockback' effect/state. |
| `Fear` | Integer | Applies or references the 'Fear' effect/state. |
| `FillMana` | Integer | Applies or references the 'FillMana' effect/state. |
| `FinalBossQueueBeam` | Integer | Applies or references the 'FinalBossQueueBeam' effect/state. |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum |  |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | Applies or references the 'FindItem' effect/state. |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | Generates an item drop from the specified loot pool. |
| `FireArmor` | Integer | Applies or references the 'FireArmor' effect/state. |
| `FireArmor2` | Integer | Applies or references the 'FireArmor2' effect/state. |
| `FireStorm` | Integer |  |
| `FireflySwarm` | Integer |  |
| `FlatAIBonus` | Integer | Applies or references the 'FlatAIBonus' effect/state. |
| `FlatLeech` | Integer | Applies or references the 'FlatLeech' effect/state. |
| `FlatLeechIfDamaged` | Integer | Applies or references the 'FlatLeechIfDamaged' effect/state. |
| `FloatingRockTrap` | Integer | Applies or references the 'FloatingRockTrap' effect/state. |
| `FlowersOnHit` | Integer | Applies or references the 'FlowersOnHit' effect/state. |
| `FlySwarm` | Integer |  |
| `Fog` | Integer |  |
| `ForceAttack` | Integer | Forces the character to execute an immediate attack. |
| `ForceCollectsPickups` | Integer | Applies or references the 'ForceCollectsPickups' effect/state. |
| `ForceDisplace` | Integer | Applies or references the 'ForceDisplace' effect/state. |
| `ForceImmediateMove` | Integer | Applies or references the 'ForceImmediateMove' effect/state. |
| [`ForceImmediateMoveAndAttack`](#forceimmediatemoveandattack) | Block | Forces the character to immediately move to a target and use a specified ability. |
| `ForceMoveAndAttack` | Integer | Applies or references the 'ForceMoveAndAttack' effect/state. |
| `ForceMoveAway` | Integer | Applies or references the 'ForceMoveAway' effect/state. |
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. |
| `ForceMoveTowards` | Integer | Applies or references the 'ForceMoveTowards' effect/state. |
| `ForceMoveTowardsEnemies` | Integer | Applies or references the 'ForceMoveTowardsEnemies' effect/state. |
| [`ForceMoveTowardsTaggedObject`](#forcemovetowardstaggedobject) | Block | Forces the character to move towards the nearest object with a specific tag. |
| `ForceTransferWeapon` | Integer | Applies or references the 'ForceTransferWeapon' effect/state. |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies or references the 'ForceUseAbility' effect/state. |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | Applies or references the 'ForceUseAbility_NonStack' effect/state. |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FreeSpell` | Integer | Applies or references the 'FreeSpell' effect/state. |
| `Freeze` | Integer | Applies or references the 'Freeze' effect/state. |
| `FullHeal` | Integer | Applies or references the 'FullHeal' effect/state. |
| [`GainCoinsRange`](#gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Applies or references the 'GainDisorder' effect/state. |
| [`GainDisorderFromPool`](./Enums.md#enum-gaindisorderfrompool) | Enum | Applies or references the 'GainDisorderFromPool' effect/state. |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |
| `GenericBuff` | Integer | Applies or references the 'GenericBuff' effect/state. |
| `GenericDebuff` | Integer | Applies or references the 'GenericDebuff' effect/state. |
| `GiveBoundItemToTarget` | Integer | Applies or references the 'GiveBoundItemToTarget' effect/state. |
| `GlobalHealthRegenAura` | Integer |  |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| [`GlobalSpawnOnRoundEnd`](#globalspawnonroundend) | Block |  |
| `Grappled` | Integer | Applies or references the 'Grappled' effect/state. |
| `HealPercentMaxHP` | Integer | Applies or references the 'HealPercentMaxHP' effect/state. |
| `HealRandomInjury` | Integer | Applies or references the 'HealRandomInjury' effect/state. |
| `HealTo` | Integer | Applies or references the 'HealTo' effect/state. |
| `HealthGain` | Integer | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Integer | Applies or references the 'HealthRegenUp' effect/state. |
| `HeatWave` | Integer |  |
| `HeavyHits` | Integer | Applies or references the 'HeavyHits' effect/state. |
| `Hex` | Integer | Applies or references the 'Hex' effect/state. |
| `HitExplosion` | Integer | Applies or references the 'HitExplosion' effect/state. |
| `IceArmor` | Integer | Applies or references the 'IceArmor' effect/state. |
| `IgnoreDamage` | Integer | Applies or references the 'IgnoreDamage' effect/state. |
| `IgnoreDebuffs` | Integer | Applies or references the 'IgnoreDebuffs' effect/state. |
| `IgnoreSelf` | Integer | Applies or references the 'IgnoreSelf' effect/state. |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. |
| `Immobile` | Integer | Applies or references the 'Immobile' effect/state. |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Applies or references the 'Imprison' effect/state. |
| [`IncAuxCounterCycle`](#incauxcountercycle) | Block | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. |
| `IncreaseCumulativeBlastDamage` | Integer | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. |
| `IncreaseItemAuxOnKill` | Integer | Applies or references the 'IncreaseItemAuxOnKill' effect/state. |
| `Infested` | Integer | Applies or references the 'Infested' effect/state. |
| `Instakill` | Integer | Applies or references the 'Instakill' effect/state. |
| `InstantMaxHealthUp` | Integer | Applies or references the 'InstantMaxHealthUp' effect/state. |
| `IntelligenceUp` | Integer | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeMoveActPoints` | Integer | Applies or references the 'InterchangeMoveActPoints' effect/state. |
| `Invulnerable` | Integer | Applies or references the 'Invulnerable' effect/state. |
| `JohnnyCriesForWashers` | Integer | Applies or references the 'JohnnyCriesForWashers' effect/state. |
| `JudgementDay` | Integer |  |
| `KineticSpikes` | Integer | Applies or references the 'KineticSpikes' effect/state. |
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | Applies or references the 'KnockOutClone' effect/state. |
| `KnockOutCoin` | Integer | Forces the target to drop coins. |
| [`KnockUpAndAway`](#knockupandaway) | Block | Displaces the target vertically and horizontally away from the source. |
| `Knockback` | Integer | Applies or references the 'Knockback' effect/state. |
| `KnockbackDamageImmuneUntilSettled` | Integer | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. |
| `KnockbackDirectionIsFacingDirection` | Integer | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. |
| [`LateStatusApplication`](#latestatusapplication) | Block | Applies a status effect after all primary damage and effects have fully resolved. |
| [`LaunchOffScreen`](./Math_Equations.md) | Equation | Applies or references the 'LaunchOffScreen' effect/state. |
| `LaunchOffScreenInstakill` | Integer | Applies or references the 'LaunchOffScreenInstakill' effect/state. |
| `LeaveBehindRockOnKnockback` | Integer | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. |
| `Leech` | Integer | Applies or references the 'Leech' effect/state. |
| `Leeches` | Integer | Applies or references the 'Leeches' effect/state. |
| `Lifesteal` | Integer | Applies or references the 'Lifesteal' effect/state. |
| `LowGravityKnockbackBoost` | Integer |  |
| `LowGravityRangeBoost` | Integer |  |
| `LowerAmbientLight` | Number |  |
| `LuckUp` | Integer | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Integer | Applies the Madness debuff/status effect. |
| `MadnessChanceOnTurnBegin` | Integer | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. |
| `MagicWeakness` | Integer | Applies or references the 'MagicWeakness' effect/state. |
| `MakeWeaponUnbreakable` | Integer | Applies or references the 'MakeWeaponUnbreakable' effect/state. |
| `ManaGain` | Integer | Applies or references the 'ManaGain' effect/state. |
| `ManaLeeches` | Integer | Applies or references the 'ManaLeeches' effect/state. |
| `ManaSteal` | Integer | Applies or references the 'ManaSteal' effect/state. |
| `ManaStealToHealth` | Integer | Applies or references the 'ManaStealToHealth' effect/state. |
| `ManglerAttack` | Integer | Applies or references the 'ManglerAttack' effect/state. |
| `ManglerShuffle` | Boolean | Applies or references the 'ManglerShuffle' effect/state. |
| `Marked` | Integer | Applies or references the 'Marked' effect/state. |
| `MassAttackThis` | Integer | Applies or references the 'MassAttackThis' effect/state. |
| [`Math`](#math) | Block | Triggers the Tinkerer's Math ability sequence. |
| `MaxHPUp` | Integer | Applies or references the 'MaxHPUp' effect/state. |
| `Meaty` | Integer | Applies or references the 'Meaty' effect/state. |
| [`MergeDamageInstance`](#mergedamageinstance) | Block | Combines damage numbers or visual hit effects. |
| `MeteorShower` | Integer |  |
| `Meteornado` | Integer |  |
| `Metronome` | Integer | Executes a random musical or metronome ability. |
| `MimicMetronome` | Integer | Applies or references the 'MimicMetronome' effect/state. |
| `MonkStanceSwitch` | Integer | Applies or references the 'MonkStanceSwitch' effect/state. |
| `MotherTumorDebugForcePass` | Integer | Applies or references the 'MotherTumorDebugForcePass' effect/state. |
| `MoveQuivered` | Integer | Applies or references the 'MoveQuivered' effect/state. |
| `MovementUp` | Integer | Applies or references the 'MovementUp' effect/state. |
| `Muted` | Integer | Applies or references the 'Muted' effect/state. |
| `NextAbilityHeals` | Integer | Applies or references the 'NextAbilityHeals' effect/state. |
| `NextActionLuckUp` | Integer | Applies or references the 'NextActionLuckUp' effect/state. |
| `NextAttackBonusRange` | Integer | Applies or references the 'NextAttackBonusRange' effect/state. |
| `NextAttackSpecialCrit` | Integer | Modifies the character's next attack to have special critical properties. |
| [`NextBasicAttackCritsThisTurn`](#nextbasicattackcritsthisturn) | Block | Guarantees the next basic attack executed this turn will be a critical hit. |
| [`NextBattleStatusStacks`](#nextbattlestatusstacks) | Block | Carries over the specified status effects into the next encounter/battle. |
| `NextDamageReduceAndHealAllies` | Integer | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. |
| `NextTurnDoubleRangedDamage` | Integer | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. |
| `NonStackingDivineShield` | Integer | Applies or references the 'NonStackingDivineShield' effect/state. |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum | Spawns a specific physics/item object upon impact. |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | Spawns a specific character or entity upon impact. |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Applies or references the 'ObjectOnHitEmpty' effect/state. |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. |
| `Ostracized` | Integer | Applies or references the 'Ostracized' effect/state. |
| `OverHealToShield` | Integer | Applies or references the 'OverHealToShield' effect/state. |
| [`OverHealToStatuses`](#overhealtostatuses) | Block | Converts excessive healing beyond maximum health into specific status effects. |
| `OverrideChainKnockback` | Integer | Applies or references the 'OverrideChainKnockback' effect/state. |
| [`OverrideChainKnockbackDamage`](./Math_Equations.md) | Equation | Applies or references the 'OverrideChainKnockbackDamage' effect/state. |
| `OverrideDamage` | Integer | Applies or references the 'OverrideDamage' effect/state. |
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum | Applies or references the 'OverrideKnockbackDamage' effect/state. |
| `PartialCleanse` | Integer | Applies or references the 'PartialCleanse' effect/state. |
| `PartialPurge` | Integer | Applies or references the 'PartialPurge' effect/state. |
| `PermanentCharisma` | Integer | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentCharm` | Integer | Applies the 'PermanentCharm' effect. |
| `PermanentConstitution` | Integer | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Integer | Applies or references the 'PermanentDexterity' effect/state. |
| `PermanentImmobile` | Integer | Applies or references the 'PermanentImmobile' effect/state. |
| `PermanentIntelligence` | Integer | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Integer | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentSpeed` | Integer | Applies or references the 'PermanentSpeed' effect/state. |
| `PermanentStrength` | Integer | Applies or references the 'PermanentStrength' effect/state. |
| `PermanentUpgradeRandomActive` | Integer | Applies or references the 'PermanentUpgradeRandomActive' effect/state. |
| `PermanentUpgradeRandomActiveOrPassive` | Integer | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. |
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum |  |
| `Petrify` | Integer | Applies or references the 'Petrify' effect/state. |
| `PlayBackground` | Integer | Applies or references the 'PlayBackground' effect/state. |
| `Poison` | Integer | Applies or references the 'Poison' effect/state. |
| `PoisonLace` | Integer | Applies or references the 'PoisonLace' effect/state. |
| [`PoolMetronome`](#poolmetronome) | Block | Executes a random ability drawn from a specific pool. |
| [`PopAndSpawn`](./Enums.md#enum-popandspawn) | Enum | Destroys the target and replaces it with a new spawned entity. |
| `Possessed` | Integer | Applies or references the 'Possessed' effect/state. |
| `ProbeCharmed` | Integer | Applies or references the 'ProbeCharmed' effect/state. |
| `PullSourceToKnockbackImmuneTarget` | Integer | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. |
| `PullSourceToTarget` | Integer | Applies or references the 'PullSourceToTarget' effect/state. |
| `Purge` | Integer | Applies or references the 'Purge' effect/state. |
| `PurgeAll` | Integer | Applies or references the 'PurgeAll' effect/state. |
| [`QuakeAreaChance`](#quakeareachance) | Block | Provides a probability to trigger an earthquake Area of Effect. |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Applies or references the 'QueueUseAbility' effect/state. |
| `Quivered` | Integer | Applies or references the 'Quivered' effect/state. |
| `RNGCannonRandomDamage` | Integer | Applies or references the 'RNGCannonRandomDamage' effect/state. |
| `Rain` | Integer |  |
| `RandomBonusDamage` | Integer | Applies or references the 'RandomBonusDamage' effect/state. |
| `RandomDistanceDisplace` | Integer | Displaces the target by a randomized distance. |
| `RandomInjury` | Integer | Applies or references the 'RandomInjury' effect/state. |
| [`RandomKnockback`](#randomknockback) | Block | Applies a randomized amount of knockback force. |
| `RandomKnockbackDirection` | Integer | Applies or references the 'RandomKnockbackDirection' effect/state. |
| `RandomLightning` | Integer |  |
| `RandomMagicMissile` | Integer | Fires a randomized number of magic missiles. |
| `RandomMutation` | Integer | Applies or references the 'RandomMutation' effect/state. |
| `RandomPermanentStat` | Integer | Applies or references the 'RandomPermanentStat' effect/state. |
| `RandomStatDown` | Integer | Applies or references the 'RandomStatDown' effect/state. |
| `RandomStatUp` | Integer | Applies or references the 'RandomStatUp' effect/state. |
| [`RandomStatusFromPool`](#randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. |
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array |  |
| `RangeUp` | Integer | Applies or references the 'RangeUp' effect/state. |
| `Reanimate` | Integer | Applies or references the 'Reanimate' effect/state. |
| `RebukeDamage` | Integer | Applies or references the 'RebukeDamage' effect/state. |
| `ReduceManaCost` | Integer | Applies or references the 'ReduceManaCost' effect/state. |
| `ReduceManaCostExcludeBrainstorm` | Integer | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. |
| `Reflect` | Integer | Applies or references the 'Reflect' effect/state. |
| `ReformMoonHead` | Integer | Applies or references the 'ReformMoonHead' effect/state. |
| `RefreshActPoints` | Integer | Applies or references the 'RefreshActPoints' effect/state. |
| `RefreshItemAbilities` | Integer | Applies or references the 'RefreshItemAbilities' effect/state. |
| `RefreshMovePoints` | Integer | Applies or references the 'RefreshMovePoints' effect/state. |
| `RefreshMovePointsIfHit` | Integer | Applies or references the 'RefreshMovePointsIfHit' effect/state. |
| `RefreshNonManaItemAbilities` | Integer | Applies or references the 'RefreshNonManaItemAbilities' effect/state. |
| `RefreshOncePerFightAbilities` | Integer | Applies or references the 'RefreshOncePerFightAbilities' effect/state. |
| `RefreshWeaponAbility` | Integer | Applies or references the 'RefreshWeaponAbility' effect/state. |
| `Regurge` | Integer | Applies or references the 'Regurge' effect/state. |
| `RemoveActPoints` | Integer | Applies or references the 'RemoveActPoints' effect/state. |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Applies or references the 'RemoveItem' effect/state. |
| `RemoveKnockback` | Integer | Applies or references the 'RemoveKnockback' effect/state. |
| `RemoveMovePoints` | Integer | Applies or references the 'RemoveMovePoints' effect/state. |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | Applies or references the 'RemoveStatus' effect/state. |
| [`RemoveStatusStacks`](#removestatusstacks) | Block | Removes a specific number of stacks of a status effect. |
| `RemoveTurnsThisRound` | Integer | Applies or references the 'RemoveTurnsThisRound' effect/state. |
| `RepairAll` | Integer | Applies or references the 'RepairAll' effect/state. |
| `RepairAllCondition` | Integer | Applies or references the 'RepairAllCondition' effect/state. |
| `RepairArmorCondition` | Integer | Applies or references the 'RepairArmorCondition' effect/state. |
| `RepairOnKill` | Integer | Applies or references the 'RepairOnKill' effect/state. |
| `RepairTrinket` | Integer | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Integer | Applies or references the 'RepairWeapon' effect/state. |
| `RepairWeaponCondition` | Integer | Applies or references the 'RepairWeaponCondition' effect/state. |
| `RerollEnemy` | Integer | Applies or references the 'RerollEnemy' effect/state. |
| `ResetArmorShield` | Integer | Applies or references the 'ResetArmorShield' effect/state. |
| `ReturnDinoLegs` | Integer | Applies or references the 'ReturnDinoLegs' effect/state. |
| `Revive` | Integer | Applies or references the 'Revive' effect/state. |
| `ReviveNextRound` | Integer | Queues the character to be resurrected at the start of the next combat round. |
| `Rot` | Integer | Applies or references the 'Rot' effect/state. |
| `SafeDie` | Integer | Applies or references the 'SafeDie' effect/state. |
| `SafeDoomed` | Integer | Applies the 'SafeDoomed' effect. |
| `Sandstorm` | Integer |  |
| [`ScatterCoins`](#scattercoins) | Block | Throws coins out into the level randomly. |
| `ScatterHeldCoin` | Integer | Applies or references the 'ScatterHeldCoin' effect/state. |
| `ScatterRandomPickups` | Integer | Applies or references the 'ScatterRandomPickups' effect/state. |
| `ScrambleEverything` | Integer | Applies or references the 'ScrambleEverything' effect/state. |
| [`ScrambleLastUsedSpell`](#scramblelastusedspell) | Block | Randomizes or scrambles the properties of the last spell cast. |
| `Scrambled` | Integer | Applies or references the 'Scrambled' effect/state. |
| `SelfStun` | Integer | Applies or references the 'SelfStun' effect/state. |
| `SendRock` | Integer | Applies or references the 'SendRock' effect/state. |
| [`SetAnimationAlts`](#setanimationalts) | Block | Overrides specific animation states with alternative animations. |
| [`SetCrazyEyeBackgroundWeights`](#setcrazyeyebackgroundweights) | Block | Adjusts visual rendering weights for the 'Crazy Eye' background effect. |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Applies or references the 'SetDefaultFace' effect/state. |
| `SetDistanceDisplace` | Integer | Applies or references the 'SetDistanceDisplace' effect/state. |
| `SetHealth` | Integer | Applies or references the 'SetHealth' effect/state. |
| [`SetItemAux`](#setitemaux) | Block | Applies or references the 'SetItemAux' effect/state. |
| `SetKnockback` | Integer | Applies or references the 'SetKnockback' effect/state. |
| `SetShield` | Integer | Applies or references the 'SetShield' effect/state. |
| `ShadowCrit` | Integer | Applies or references the 'ShadowCrit' effect/state. |
| `Shatter` | Integer | Applies or references the 'Shatter' effect/state. |
| `Shield` | Integer | Applies or references the 'Shield' effect/state. |
| `ShootHereCommand` | Integer | Applies or references the 'ShootHereCommand' effect/state. |
| `ShootHereReceiver` | Integer | Applies or references the 'ShootHereReceiver' effect/state. |
| `ShortCircuit` | Integer | Applies or references the 'ShortCircuit' effect/state. |
| [`ShowFakeDamage`](#showfakedamage) | Block | Displays a visual damage number without actually modifying health. |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. |
| `SignalFinalBossShieldBroke` | Integer | Applies or references the 'SignalFinalBossShieldBroke' effect/state. |
| `SizeScale` | Float | Applies or references the 'SizeScale' effect/state. |
| `Sleep` | Integer | Applies or references the 'Sleep' effect/state. |
| `Slow` | Integer | Applies or references the 'Slow' effect/state. |
| `SmallHitExplosion` | Integer | Applies or references the 'SmallHitExplosion' effect/state. |
| `SmartMetronome` | Integer | Executes a 'smart' random ability that aims to be beneficial based on context. |
| `SmellBlood` | Integer | Applies or references the 'SmellBlood' effect/state. |
| `Snow` | Integer |  |
| [`SolarFlare`](#solarflare) | Block |  |
| `SoulLink` | Integer | Applies or references the 'SoulLink' effect/state. |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Applies or references the 'SoundEventOnHit' effect/state. |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. |
| `SpawnBearTrap` | Integer | Applies or references the 'SpawnBearTrap' effect/state. |
| `SpawnBearTrapIfHitKills` | Integer | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. |
| `SpawnCoinAnywhere` | Integer | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `SpawnCreep` | Integer | Applies or references the 'SpawnCreep' effect/state. |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Applies or references the 'SpawnCustomTrap' effect/state. |
| [`SpawnExtraThingsOnBattleStart`](#spawnextrathingsonbattlestart) | Block |  |
| [`SpawnFlames`](./Arrays.md#array-spawnflames) | Array | Applies or references the 'SpawnFlames' effect/state. |
| `SpawnNeutralWebTrapOnMiss` | Integer | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. |
| `SpawnRock` | Integer | Applies or references the 'SpawnRock' effect/state. |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| [`SpawnTilePuddleOnBattleStart`](#spawntilepuddleonbattlestart) | Block |  |
| [`SpawnVolcanoOnBattleStart`](#spawnvolcanoonbattlestart) | Block |  |
| `SpawnWebTrap` | Integer | Applies or references the 'SpawnWebTrap' effect/state. |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Applies or references the 'SpecialBossMultipartInstakill' effect/state. |
| [`SpecialGodRays`](#specialgodrays) | Block |  |
| [`SpecificInjury`](./Enums.md#enum-specificinjury) | Enum | Applies or references the 'SpecificInjury' effect/state. |
| `SpeculativeMoveSelfCorpseOffMap` | Integer | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. |
| `SpeedUp` | Integer | Applies or references the 'SpeedUp' effect/state. |
| `SpellDamageUp` | Integer | Applies or references the 'SpellDamageUp' effect/state. |
| `SpellShield` | Integer | Applies or references the 'SpellShield' effect/state. |
| `SpiderInfested` | Integer | Applies or references the 'SpiderInfested' effect/state. |
| `SpitConsumed` | Integer | Applies or references the 'SpitConsumed' effect/state. |
| `SplashDamage` | Integer | Applies or references the 'SplashDamage' effect/state. |
| [`SpreadDisease`](#spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. |
| `StackingSandstorm` | Integer | Applies or references the 'StackingSandstorm' effect/state. |
| `StanceSwitchToMelee` | Integer | Applies or references the 'StanceSwitchToMelee' effect/state. |
| `StanceSwitchToRanged` | Integer | Applies or references the 'StanceSwitchToRanged' effect/state. |
| `StatBounty` | Integer | Applies or references the 'StatBounty' effect/state. |
| [`StatusAllCharactersOnSpawn`](#statusallcharactersonspawn) | Block |  |
| [`StatusCharactersOnRoundEnd`](#statuscharactersonroundend) | Block |  |
| [`StatusCharactersOnRoundStart`](#statuscharactersonroundstart) | Block |  |
| [`StatusGroup`](#statusgroup) | Block | Groups multiple status effects together for batch application. |
| `StealDemonicGlyph` | Integer | Applies or references the 'StealDemonicGlyph' effect/state. |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Applies or references the 'StealEquipment' effect/state. |
| `StealTurn` | Integer | Applies or references the 'StealTurn' effect/state. |
| `Stealth` | Integer | Applies or references the 'Stealth' effect/state. |
| `StealthCritChance` | Integer | Applies or references the 'StealthCritChance' effect/state. |
| `StrengthUp` | Integer | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Integer | Applies or references the 'Stun' effect/state. |
| `SwallowSmallCharacter` | Integer | Applies or references the 'SwallowSmallCharacter' effect/state. |
| `SwapHighestAndLowestStat` | Integer | Applies or references the 'SwapHighestAndLowestStat' effect/state. |
| [`SwapWeapon`](#swapweapon) | Block | Replaces the character's currently equipped weapon with one from a specified pool. |
| [`SwitchMusic`](#switchmusic) | Block | Changes the background music track or layer during combat. |
| `Switcheroo` | Integer | Applies or references the 'Switcheroo' effect/state. |
| `T2CopyCat` | Integer | Applies or references the 'T2CopyCat' effect/state. |
| `T3HitlerTriggerInitialSpawns` | Integer | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Applies or references the 'TagMetronome' effect/state. |
| [`TakeBonusTurnWithAIControl`](#takebonusturnwithaicontrol) | Block | Grants the character an immediate extra turn, but forces the AI to control them during it. |
| [`TakeBonusTurnWithStatus`](#takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. |
| `TakeExtraTurn` | Integer | Applies or references the 'TakeExtraTurn' effect/state. |
| `TakeExtraTurnEndOfRound` | Integer | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. |
| `Tangled` | Integer | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `TargetedMetronome` | Integer | Applies or references the 'TargetedMetronome' effect/state. |
| `Tarred` | Integer | Applies or references the 'Tarred' effect/state. |
| `Taunting` | Integer | Applies or references the 'Taunting' effect/state. |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Applies or references the 'TeamBonusAbility' effect/state. |
| [`TeamCastAbility`](./Enums.md#enum-teamcastability) | Enum | Requires or involves multiple characters to execute the ability. |
| `Tech` | Integer | Applies or references the 'Tech' effect/state. |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Applies or references the 'TeleportBackAtTurnEnd' effect/state. |
| `TempBackstab` | Integer | Applies or references the 'TempBackstab' effect/state. |
| `TempBackstabBleed` | Integer | Applies or references the 'TempBackstabBleed' effect/state. |
| `TempBackstabPiercing` | Integer | Applies or references the 'TempBackstabPiercing' effect/state. |
| `TempBackstabPoison` | Integer | Applies or references the 'TempBackstabPoison' effect/state. |
| `TempBasicAttackBonusAOE` | Integer | Applies or references the 'TempBasicAttackBonusAOE' effect/state. |
| `TempBonusKnockback` | Integer | Applies or references the 'TempBonusKnockback' effect/state. |
| `TempBonusKnockbackDamage` | Integer | Applies or references the 'TempBonusKnockbackDamage' effect/state. |
| `TempCounterAttack` | Integer | Applies or references the 'TempCounterAttack' effect/state. |
| `TempCritChanceUp` | Integer | Applies or references the 'TempCritChanceUp' effect/state. |
| `TempDamageUp` | Integer | Applies or references the 'TempDamageUp' effect/state. |
| [`TempDexterityUp`](./Enums.md#enum-tempdexterityup) | Enum | Applies or references the 'TempDexterityUp' effect/state. |
| `TempInitiativeChange` | Integer | Applies or references the 'TempInitiativeChange' effect/state. |
| `TempInjuryImmunity` | Integer | Applies or references the 'TempInjuryImmunity' effect/state. |
| `TempLuckUp` | Integer | Applies or references the 'TempLuckUp' effect/state. |
| `TempManaCostReduction` | Integer | Applies or references the 'TempManaCostReduction' effect/state. |
| `TempMovement` | Integer | Applies or references the 'TempMovement' effect/state. |
| [`TempPassiveUntilSettled`](#temppassiveuntilsettled) | Block | Passive: Active only until the physics engine stops moving the character. |
| [`TempPassiveWhileHasStatus`](#temppassivewhilehasstatus) | Block | Grants nested passives only while the character possesses the specified status. |
| `TempPenetrate` | Integer | Applies or references the 'TempPenetrate' effect/state. |
| `TempPreEmptiveCounterAttack` | Integer | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. |
| `TempRangeUp` | Integer | Applies or references the 'TempRangeUp' effect/state. |
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum | Applies or references the 'TempSpeedUp' effect/state. |
| `TempSpellDamageUp` | Integer | Applies or references the 'TempSpellDamageUp' effect/state. |
| [`TempStrengthUp`](./Enums.md#enum-tempstrengthup) | Enum | Applies or references the 'TempStrengthUp' effect/state. |
| `TempTrampleUntilSettled` | Integer | Applies or references the 'TempTrampleUntilSettled' effect/state. |
| [`Temporary`](#temporary) | Block | A wrapper block for applying status effects that automatically expire. |
| `Thorns` | Integer | Applies or references the 'Thorns' effect/state. |
| `ThornsDamageImmuneUntilSettled` | Integer | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Applies or references the 'TickDownStatus' effect/state. |
| `TileDamageImmuneUntilSettled` | Integer | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. |
| `TilesMovedToCritChance` | Integer | Applies or references the 'TilesMovedToCritChance' effect/state. |
| `TilesMovedToMana` | Integer | Applies or references the 'TilesMovedToMana' effect/state. |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Applies or references the 'TilesMovedToNeighborHeal' effect/state. |
| `TilesMovedToStrength` | Integer | Applies or references the 'TilesMovedToStrength' effect/state. |
| [`TimeDelayStatusApplication`](#timedelaystatusapplication) | Block | Delays the nested effects by a specified amount of real-time seconds. |
| `TowerDefenseStatus` | Integer | Applies or references the 'TowerDefenseStatus' effect/state. |
| `TowerDefenseStatus2` | Integer | Applies or references the 'TowerDefenseStatus2' effect/state. |
| `TradeLife` | Integer | Applies or references the 'TradeLife' effect/state. |
| `TrailBlazer` | Integer | Applies or references the 'TrailBlazer' effect/state. |
| `Trample` | Integer | Applies or references the 'Trample' effect/state. |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Applies or references the 'TransformAbility' effect/state. |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Applies or references the 'TransformBasicAttack' effect/state. |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Applies or references the 'TransformBasicMove' effect/state. |
| [`TransformEquipment`](#transformequipment) | Block | Upgrades or transforms a specific equipped item into another. |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Applies or references the 'TransformNow' effect/state. |
| [`TransformWeapon`](#transformweapon) | Block | Transforms the equipped weapon into another specific weapon state. |
| `Trapper_Status` | Integer | Applies or references the 'Trapper_Status' effect/state. |
| `TriggerDOTStatuses` | Integer | Applies or references the 'TriggerDOTStatuses' effect/state. |
| `TriggerGameEnding` | Integer | Applies or references the 'TriggerGameEnding' effect/state. |
| `TriggerMotherConsume` | Integer | Applies or references the 'TriggerMotherConsume' effect/state. |
| `TriggerMotherGrow` | Integer | Applies or references the 'TriggerMotherGrow' effect/state. |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array | Applies or references the 'TriggerWerewolfTransform' effect/state. |
| `TurnAround` | Integer | Applies or references the 'TurnAround' effect/state. |
| `TurnControlDelay` | Float | Applies or references the 'TurnControlDelay' effect/state. |
| `TurnRight` | Integer | Applies or references the 'TurnRight' effect/state. |
| [`TwisterDisplaceWithDamage`](#twisterdisplacewithdamage) | Block | A whirlwind effect that randomly displaces targets and deals damage. |
| `UndoDamage` | Integer | Applies or references the 'UndoDamage' effect/state. |
| `UpgradeRandomAbility` | Integer | Applies or references the 'UpgradeRandomAbility' effect/state. |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Forces the character or target to instantly use a specified ability. |
| [`UseMoveAbilityWithAI`](#usemoveabilitywithai) | Block | Forces the character to execute a movement ability using specific AI weights. |
| `UseRandomSpell_Madness` | Integer | Applies the 'UseRandomSpell_Madness' effect. |
| `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. |
| `VaporizeCorpse` | Integer | Applies or references the 'VaporizeCorpse' effect/state. |
| [`VaporizeCorpseFlipAdvantage`](./Arrays.md#array-vaporizecorpseflipadvantage) | Array | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. |
| `VaporizeDice` | Integer | Applies or references the 'VaporizeDice' effect/state. |
| `VaporizeInanimate` | Integer | Applies or references the 'VaporizeInanimate' effect/state. |
| `VaporizeTarget` | Integer | Applies or references the 'VaporizeTarget' effect/state. |
| [`VisualCountDownThenApplyStatus`](#visualcountdownthenapplystatus) | Block | Displays a visual countdown above the target before applying the nested effects. |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | Applies or references the 'VisualFX' effect/state. |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Applies or references the 'VisualFXTile' effect/state. |
| `VisualFlySwarm` | Integer |  |
| [`WaggleClone`](#waggleclone) | Block | Spawns visual clones or alternative hitbox variants of the projectile. |
| `Weakness` | Integer | Applies or references the 'Weakness' effect/state. |
| `WeaponAuxMultiplier` | Float | Applies or references the 'WeaponAuxMultiplier' effect/state. |
| `Webbed` | Integer | Applies or references the 'Webbed' effect/state. |
| `Windy` | Integer |  |
| [`XIsTargetHealth`](#xistargethealth) | Block | Math variable assignment: Evaluates X as the target's current health. |
| `do_not_pop_corpse` | Boolean |  |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum |  |
| `drop_on_death` | Boolean |  |
| `drop_on_self_death` | Boolean |  |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. |
| [`extra_statuses`](#extra_statuses) | Block | Additional generic status applications. |
| `force_contact` | Boolean | If true, enforces physical overlap. |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. |
| `instant` | Boolean |  |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. |
| `kill_on_consume` | Boolean |  |
| `mount_mode` | Boolean | If true, treats the consumption as riding/mounting instead of eating. |
| `odds` | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum |  |
| `threshold_flat` | Integer | A flat numerical health value threshold. |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). |
| `use_placeholder` | Boolean |  |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. |
| `wet` | Boolean |  |
| [`{Logic Keys}`](#{logic blocks}) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `{Status and Passive Keys}` | Variable | All valid keys from the specified engine key are applicable to this context/block. |

</details>

### Valid Nested Blocks

The following blocks all behave as `{Logic Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. |

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. |

</details>

---

#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. |
| [`Conditional_Speculative`](#conditional_speculative) | Block | Nested conditional. |

</details>

---

#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. |

</details>

---

#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`odds`](./Math_Equations.md) | Equation | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. (Must be float values) |

</details>

---

#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. |

</details>

---

#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_InForm`](#conditional_inform) | Block | Nested conditional. |

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. |

</details>

---

#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `odds` | Float | The probability (0.0 to 1.0) of applying the debuff. |

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Block | Nested conditional. |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Nested conditional. |
| [`Conditional_PartyMember`](#conditional_partymember) | Block | Nested conditional. |

</details>

---

#### `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. |

</details>

---

#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. |

</details>

---

#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `odds` | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. |

</details>

---

#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. |

</details>

---

#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. |
| [`Conditional_Boss`](#conditional_boss) | Block | Nested conditional. |
| [`Conditional_InForm`](#conditional_inform) | Block | Nested conditional. |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Nested conditional. |

</details>

---

#### `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum |  |
| `threshold_flat` | Integer | A flat numerical health value threshold. |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Block | Nested conditional. |

</details>

---

#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. |

</details>

---

#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `threshold_flat` | Integer |  |

</details>

---

#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. |

</details>

---

#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. |

</details>

---

#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`key`](./Enums.md#enum-key) | Enum |  |

</details>

---

#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_IsSelf`](#conditional_isself) | Block | Nested conditional. |

</details>

---

#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `odds` | Float |  |

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |

</details>

---

#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. |

</details>

---

#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. |

</details>

---

#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |

</details>

---

#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. |

</details>

---

#### `Consumed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `do_not_pop_corpse` | Boolean |  |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum |  |
| `drop_on_death` | Boolean |  |
| `drop_on_self_death` | Boolean |  |
| [`extra_statuses`](#extra_statuses) | Block | Additional generic status applications. |
| `force_contact` | Boolean | If true, enforces physical overlap. |
| `instant` | Boolean |  |
| `kill_on_consume` | Boolean |  |
| `mount_mode` | Boolean | If true, treats the consumption as riding/mounting instead of eating. |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. |
| `use_placeholder` | Boolean |  |
| `wet` | Boolean |  |

</details>

---

#### `Else`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| [`Conditional_Displaceable`](#conditional_displaceable) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |
| [`Conditional_HasKnockback`](#conditional_hasknockback) | Block | Nested conditional. |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. |
| [`Conditional_Object`](#conditional_object) | Block | Nested conditional. |
| [`Conditional_Speculative`](#conditional_speculative) | Block | Nested conditional. |

</details>

---

#### `effects`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. |
| `LowerAmbientLight` | Number |  |
| [`Conditional_AbilityTargetIsSelf`](#conditional_abilitytargetisself) | Block | Nested conditional. |
| [`Conditional_ActiveWeather_Any`](#conditional_activeweather_any) | Block | Nested conditional. |
| [`Conditional_AffectedByElement`](#conditional_affectedbyelement) | Block | Nested conditional. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |
| [`Conditional_Backstab`](#conditional_backstab) | Block | Nested conditional. |
| [`Conditional_BadRoll`](#conditional_badroll) | Block | Nested conditional. |
| [`Conditional_Boss`](#conditional_boss) | Block | Nested conditional. |
| [`Conditional_BossOrBig`](#conditional_bossorbig) | Block | Nested conditional. |
| [`Conditional_Buddy`](#conditional_buddy) | Block | Nested conditional. |
| [`Conditional_CanBeHealed`](#conditional_canbehealed) | Block | Nested conditional. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. |
| [`Conditional_DebuffRoll`](#conditional_debuffroll) | Block | Nested conditional. |
| [`Conditional_DestructibleCorpse`](#conditional_destructiblecorpse) | Block | Nested conditional. |
| [`Conditional_Displaceable`](#conditional_displaceable) | Block | Nested conditional. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. |
| [`Conditional_Familiar`](#conditional_familiar) | Block | Nested conditional. |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Block | Nested conditional. |
| [`Conditional_FormulaIsPositive`](#conditional_formulaispositive) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |
| [`Conditional_HasCleansableDebuffs`](#conditional_hascleansabledebuffs) | Block | Nested conditional. |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. |
| [`Conditional_InForm`](#conditional_inform) | Block | Nested conditional. |
| [`Conditional_IsSelf`](#conditional_isself) | Block | Nested conditional. |
| [`Conditional_IsTrample`](#conditional_istrample) | Block | Nested conditional. |
| [`Conditional_LastHit`](#conditional_lasthit) | Block | Nested conditional. |
| [`Conditional_LivingPlayerCat`](#conditional_livingplayercat) | Block | Nested conditional. |
| [`Conditional_NotAlly`](#conditional_notally) | Block | Nested conditional. |
| [`Conditional_NotBig`](#conditional_notbig) | Block | Nested conditional. |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Nested conditional. |
| [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Block | Nested conditional. |
| [`Conditional_NotShielded`](#conditional_notshielded) | Block | Nested conditional. |
| [`Conditional_Object`](#conditional_object) | Block | Nested conditional. |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. |
| [`Conditional_RandomChance`](#conditional_randomchance) | Block | Nested conditional. |
| [`Conditional_Shielded`](#conditional_shielded) | Block | Nested conditional. |
| [`Conditional_SourceAbilityHasTag`](#conditional_sourceabilityhastag) | Block | Nested conditional. |
| [`Conditional_SourceHasStatus`](#conditional_sourcehasstatus) | Block | Nested conditional. |
| [`Conditional_Speculative`](#conditional_speculative) | Block | Nested conditional. |

</details>

