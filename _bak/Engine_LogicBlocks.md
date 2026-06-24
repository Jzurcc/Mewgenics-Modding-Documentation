# Mewgenics Mod Developer Documentation: Engine: Logic Blocks

## Engine: Logic Blocks

This document is the authoritative reference for Logic Blocks. All of the contexts below can appear as dynamic keys inside an `effects {}` block, or directly inside abilities. Many of these are conditional wrappers that evaluate a condition before executing their nested block, while others redirect execution flow (e.g. `ApplyToSource`).

> **Note:** Because many of these contexts accept arbitrary nested Logic Blocks, any entry marked `{Logic Blocks}` recursively refers back to this same document.

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-root), [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`temporary_effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temporary_effects), [`Else` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-else), [`ApplyToSource` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_ally), [`Consumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-consumed), [`Conditional_Boss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_speculative), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`Conditional_Corpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_playercat), [`ApplyToConsumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytoconsumed), [`TimeDelayStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-post_spawn_statuses), [`Conditional_AffectedByElement` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_lasthit), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`ApplyToTile` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytotile), [`Conditional_BadRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_DestructibleCorpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_destructiblecorpse), [`Conditional_Displaceable` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_displaceable), [`Conditional_IsSelf` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_isself), [`Conditional_OncePerBattle` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_shielded), [`ApplyToRandomClosestAlly` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandomclosestally), [`Conditional_Backstab` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_backstab), [`Conditional_FinishedSpawning` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_finishedspawning), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Conditional_IsTrample` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_istrample), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_NotBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notbig), [`Conditional_RandomChance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_randomchance), [`NextBattleStatusStacks` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-nextbattlestatusstacks), [`ROOT` (Boss_Cutscene_Info)](./Boss_Cutscene_Info.md#context-root), [`ROOT` (Cat_Classes)](./Cat_Classes.md#context-root), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`Conditional_RandomChance` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_randomchance), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_goodroll), [`ROOT` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-root), [`FormChanger` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-formchanger), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`Consumed` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-consumed), [`Conditional_GoodRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_goodroll), [`Conditional_BadRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-else), [`FinalBossBecomeTheChild` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbossbecomethechild), [`InfiniteRebirth` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-infiniterebirth), [`TVBotScreen` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-tvbotscreen), [`ROOT` (Custom_Cats)](./Custom_Cats.md#context-root), [`ROOT` (Damage_Text_Styles)](./Damage_Text_Styles.md#context-root), [`ROOT` (Difficulties)](./Difficulties.md#context-root), [`ROOT` (Elite_Buffs)](./Elite_Buffs.md#context-root), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`ROOT` (Enemy_AI)](./Enemy_AI.md#context-root), [`ROOT` (Events_and_Encounters)](./Events_and_Encounters.md#context-root), [`global_effect_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-global_effect_next_fight), [`ROOT` (Furniture_and_Metaprogression)](./Furniture_and_Metaprogression.md#context-root), [`ROOT` (House_and_Environment)](./House_and_Environment.md#context-root), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`Else` (House_and_Environment)](./House_and_Environment.md#context-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundend), [`Conditional_GoodRoll` (House_and_Environment)](./House_and_Environment.md#context-conditional_goodroll), [`Conditional_Corpse` (House_and_Environment)](./House_and_Environment.md#context-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](./House_and_Environment.md#context-conditional_partymember), [`ROOT` (Injuries)](./Injuries.md#context-root), [`ROOT` (Items_and_Equipment)](./Items_and_Equipment.md#context-root), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`Conditional_GoodRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_goodroll), [`ApplyToSource` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytosource), [`Conditional_HasStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else` (Items_and_Equipment)](./Items_and_Equipment.md#context-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`Conditional_PartyMember` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_partymember), [`Conditional_Adjacent` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_onceperbattle), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytorandompartymemberifpossible), [`CastAgainWithStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-castagainwithstatus), [`Conditional_Ally` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_enemy), [`Conditional_HasCleansableDebuffs` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`Conditional_HealthThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_healththreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_shielded), [`CyborgTurns` (Items_and_Equipment)](./Items_and_Equipment.md#context-cyborgturns), [`ScaldingOrbMoonBossOneShot` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot), [`StatusAdjacentOnTheirTurnEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusadjacentontheirturnend), [`StatusOnFallAsleep` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonfallasleep), [`StatusOnTurnEndIfCastNSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifcastnspells), [`ROOT` (Item_Pools)](./Item_Pools.md#context-root), [`ROOT` (Map_Generation_and_Routing)](./Map_Generation_and_Routing.md#context-root), [`ROOT` (Miscellaneous)](./Miscellaneous.md#context-root), [`ROOT` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-root), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects), [`StatusOnStanceSwitch` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonstanceswitch), [`Conditional_Ally` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_enemy), [`Else` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-else), [`StatusOnOverHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonoverhealed), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaexact), [`Conditional_BadRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hasstatus), [`AddStatusToBasicAttackWithCooldown` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicattackwithcooldown), [`AddStatusToMeleeDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustomeleedamage), [`ApplyToSource` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applytosource), [`Conditional_Adjacent` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_shielded), [`EscapeSequence` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-escapesequence), [`InfiniteRebirth` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-infiniterebirth), [`StatusOnDealtDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamage), [`on_throw` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-on_throw), [`Conditional_GoodRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_goodroll), [`StatusAdjacentOnTheirTurnBegin` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin), [`ROOT` (Progression_Unlocks)](./Progression_Unlocks.md#context-root), [`ROOT` (Shops)](./Shops.md#context-root), [`ROOT` (Spawns_and_Enemy_Pools)](./Spawns_and_Enemy_Pools.md#context-root), [`ROOT` (Status_Effect_Keywords)](./Status_Effect_Keywords.md#context-root)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| `AIFavorLowHealth` | Number | Applies or references the 'AIFavorLowHealth' effect/state. |
| `AcidRain` | Number |  |
| `AddExtraTurnsBeforeRun` | Number |  |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. |
| [`AddPostProcessEffect`](#addpostprocesseffect) | Block |  |
| `AddSpiritBombCharges` | Number | Applies or references the 'AddSpiritBombCharges' effect/state. |
| [`AddTilesetObjects`](#addtilesetobjects) | Block |  |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. |
| `Adrenaline` | Number | Applies or references the 'Adrenaline' effect/state. |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. |
| `AlliesTakeExtraTurn` | Number | Applies or references the 'AlliesTakeExtraTurn' effect/state. |
| [`AllyInfested`](#allyinfested) | Block |  |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Applies or references the 'AlternateIdleAnimation' effect/state. |
| `Ammo` | Number | Applies or references the 'Ammo' effect/state. |
| [`ApplyMultipleTimes`](#applymultipletimes) | Block | A loop block that executes its nested logic multiple times. |
| [`ApplyPassives`](#applypassives) | Block | Grants the nested passive abilities dynamically. |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. |
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
| `Attraction` | Number | Applies or references the 'Attraction' effect/state. |
| `AutoReanimate` | Number |  |
| `BackflipWhenTargeted` | Number | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BlackHoleSuck` | Number | Applies or references the 'BlackHoleSuck' effect/state. |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. |
| `Blind` | Number | Applies or references the 'Blind' effect/state. |
| `Bloodzerked` | Number | Applies or references the 'Bloodzerked' effect/state. |
| [`BodyGuard`](#bodyguard) | Block | Protects an ally by intercepting attacks directed at them. |
| `BombRatTurtle` | Number | Applies or references the 'BombRatTurtle' effect/state. |
| `BonusCritChance` | Number | Applies or references the 'BonusCritChance' effect/state. |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. |
| `BonusDamageBasedOnDistance` | Number | Applies or references the 'BonusDamageBasedOnDistance' effect/state. |
| `BonusDamageBasedOnMana` | Number | Applies or references the 'BonusDamageBasedOnMana' effect/state. |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | Spawns a physics object that visually bounces off the target. |
| [`BounceRock`](./Enums.md#enum-bouncerock) | Enum | Applies or references the 'BounceRock' effect/state. |
| `Bound` | Number | Applies or references the 'Bound' effect/state. |
| `Brace` | Number | Applies or references the 'Brace' effect/state. |
| `BramblesOnHit` | Number | Applies or references the 'BramblesOnHit' effect/state. |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. |
| `BurgleCoin` | Number | Applies or references the 'BurgleCoin' effect/state. |
| `Burn` | Number | Applies or references the 'Burn' effect/state. |
| `ButterflySwarm` | Number |  |
| `BypassRockKnockback` | Number | Applies or references the 'BypassRockKnockback' effect/state. |
| [`CanApplyToInanimate`](#canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `CancelPrimedAbilities` | Number | Applies or references the 'CancelPrimedAbilities' effect/state. |
| `CanceledQueuedInput` | Number | Applies or references the 'CanceledQueuedInput' effect/state. |
| `CapDamage` | Number | Applies or references the 'CapDamage' effect/state. |
| `CaptureFamiliar` | Number | Applies the 'CaptureFamiliar' effect. |
| [`CatPartsSizeScaleStatus`](#catpartssizescalestatus) | Block | Visually scales specific body parts of a character. |
| [`CatPartsTransform`](#catpartstransform) | Block | Transforms specific body parts into different visual variants. |
| `ChampionUpgradeNextMinion` | Number | Applies or references the 'ChampionUpgradeNextMinion' effect/state. |
| `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. |
| [`ChanceToBreakFree`](#chancetobreakfree) | Block | Provides a probability to escape a grapple or restraining effect. |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Applies or references the 'ChangeCatClass' effect/state. |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Applies or references the 'ChangeFaction' effect/state. |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | Transforms the terrain tile under the target. |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Applies or references the 'ChangeTilesUnder' effect/state. |
| `ChaosBossFlipMidTeleport` | Number | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. |
| `ChaosBossFormChange` | Number | Applies or references the 'ChaosBossFormChange' effect/state. |
| [`CharacterTypeGainsStatusAtBattleStart`](#charactertypegainsstatusatbattlestart) | Block |  |
| `Charge` | Number | Applies or references the 'Charge' effect/state. |
| `ChargeFists` | Number | Applies or references the 'ChargeFists' effect/state. |
| `CharismaUp` | Number | Applies or references the 'CharismaUp' effect/state. |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. |
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
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum | Applies or references the 'CoinTossBounce' effect/state. |
| `CollectsPickups` | Number | Applies or references the 'CollectsPickups' effect/state. |
| [`CollectsPickupsWithAltEffects`](#collectspickupswithalteffects) | Block | Triggers alternative nested effects when collecting items or pickups. |
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | Applies or references the 'CollideWithConsumed' effect/state. |
| `CollideWithThrowTarget` | Number | Applies or references the 'CollideWithThrowTarget' effect/state. |
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
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum | Adds a temporary bonus ability to the character's hand/deck. |
| `ConjureRandomAbilityFromCat` | Number | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. |
| [`Consumed`](#consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. |
| `ContextualHeal` | Number | Applies or references the 'ContextualHeal' effect/state. |
| `CopySpells` | Number | Duplicates existing spells currently in the character's hand. |
| `CorpseVaporizer` | Number | Applies or references the 'CorpseVaporizer' effect/state. |
| `Counterspell` | Number | Applies or references the 'Counterspell' effect/state. |
| `CrackMoonHead` | Number | Applies or references the 'CrackMoonHead' effect/state. |
| [`Craft`](#craft) | Block | Synthesizes or spawns a new item from a specific pool. |
| [`CreateGlobalModifiers`](#createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. |
| `CurrentWeaponAddElectricElement` | Number | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. |
| `DamageBasedOnMissingHealth` | Number | Applies or references the 'DamageBasedOnMissingHealth' effect/state. |
| `DamageDistanceAOEFalloff` | Number | Applies or references the 'DamageDistanceAOEFalloff' effect/state. |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `DamageTrinket` | Number | Applies or references the 'DamageTrinket' effect/state. |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. |
| `DamageWeapon` | Number | Applies or references the 'DamageWeapon' effect/state. |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Applies or references the 'DeathwormUnderground' effect/state. |
| `DecoySwapper` | Number | Applies or references the 'DecoySwapper' effect/state. |
| `DeferVaporize` | Number | Applies or references the 'DeferVaporize' effect/state. |
| [`DelayCastAbility`](#delaycastability) | Block | Queues an ability to be cast automatically after a certain delay or trigger. |
| `DelayedFury` | Number | Applies or references the 'DelayedFury' effect/state. |
| [`DelayedWindCone`](#delayedwindcone) | Block | Creates a delayed Area of Effect cone. |
| `DeleteInanimateObjectsChance` | Number |  |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. |
| `DeleteTraps` | Number | Applies or references the 'DeleteTraps' effect/state. |
| [`DestroyEquipmentAndAttachParasite`](#destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DestroyNeckArmor` | Number | Applies or references the 'DestroyNeckArmor' effect/state. |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. |
| `DestroyWeapon` | Number | Applies or references the 'DestroyWeapon' effect/state. |
| `DestroyWeaponThrow` | Number | Applies or references the 'DestroyWeaponThrow' effect/state. |
| `DexterityUp` | Number | Applies or references the 'DexterityUp' effect/state. |
| `Die` | Number | Applies or references the 'Die' effect/state. |
| `DieViaAbilityInternally` | Number | Applies or references the 'DieViaAbilityInternally' effect/state. |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. |
| `DiminishingHealthRegen` | Number | Applies or references the 'DiminishingHealthRegen' effect/state. |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Applies or references the 'DinoLegAnimation' effect/state. |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. |
| `Disguised` | Number | Applies or references the 'Disguised' effect/state. |
| `Displace` | Number | Applies or references the 'Displace' effect/state. |
| `DisplaceToAbilityTarget` | Number | Applies or references the 'DisplaceToAbilityTarget' effect/state. |
| `DisplaceToOriginalPosition` | Number | Applies or references the 'DisplaceToOriginalPosition' effect/state. |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. |
| `DissolveRandomArmorPiece` | Number | Applies or references the 'DissolveRandomArmorPiece' effect/state. |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. |
| [`DoDamage`](#dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. |
| [`DoDistortionRing`](#dodistortionring) | Block | Creates a visual distortion ring effect on the screen. |
| [`DoScreenShake`](#doscreenshake) | Block | Triggers a camera screen shake effect. |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. |
| `DontHealEnemies` | Number | Applies or references the 'DontHealEnemies' effect/state. |
| `Doomed` | Number | Applies or references the 'Doomed' effect/state. |
| `DoubleCast` | Number | Applies or references the 'DoubleCast' effect/state. |
| `DoubleCastSpell` | Number | Applies or references the 'DoubleCastSpell' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. |
| `DoubleLoot` | Number | Applies or references the 'DoubleLoot' effect/state. |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | Applies or references the 'DoubleStatus' effect/state. |
| `DrainAllyCatsForFleshGolem` | Number | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. |
| `DrinkWater` | Number | Applies or references the 'DrinkWater' effect/state. |
| `Drowsy` | Number | Applies or references the 'Drowsy' effect/state. |
| `DuplicateRandomEquippedItem` | Number | Applies or references the 'DuplicateRandomEquippedItem' effect/state. |
| [`DustOnHit`](#dustonhit) | Block | Spawns a specific particle or cloud object upon impact. |
| [`DybbukPossessed`](#dybbukpossessed) | Block | Defines the abilities and behaviors available when possessing another entity. |
| `EliteUpgradeNextMinion` | Number | Applies or references the 'EliteUpgradeNextMinion' effect/state. |
| [`Else`](#else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `EmptyMind` | Number | Applies or references the 'EmptyMind' effect/state. |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Applies or references the 'EnableWeather' effect/state. |
| `EndTurn` | Number | Applies or references the 'EndTurn' effect/state. |
| `Enlarge` | Number | Applies or references the 'Enlarge' effect/state. |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Applies or references the 'EnterMount' effect/state. |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | Applies or references the 'EquipPermanentItem' effect/state. |
| `EventBounty` | Number | Applies or references the 'EventBounty' effect/state. |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum | Upgrades or transforms an existing ability into a new one from the specified pool. |
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
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum |  |
| `FastKnockback` | Number | Applies or references the 'FastKnockback' effect/state. |
| `Fear` | Number | Applies or references the 'Fear' effect/state. |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. |
| `FinalBossQueueBeam` | Number | Applies or references the 'FinalBossQueueBeam' effect/state. |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum |  |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | Applies or references the 'FindItem' effect/state. |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | Generates an item drop from the specified loot pool. |
| `FireArmor` | Number | Applies or references the 'FireArmor' effect/state. |
| `FireArmor2` | Number | Applies or references the 'FireArmor2' effect/state. |
| `FireStorm` | Number |  |
| `FireflySwarm` | Number |  |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. |
| `FlatLeechIfDamaged` | Number | Applies the 'FlatLeechIfDamaged' effect. |
| `FloatingRockTrap` | Number | Applies or references the 'FloatingRockTrap' effect/state. |
| `FlowersOnHit` | Number | Applies or references the 'FlowersOnHit' effect/state. |
| `FlySwarm` | Number |  |
| `Fog` | Number |  |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. |
| `ForceCollectsPickups` | Number | Applies or references the 'ForceCollectsPickups' effect/state. |
| `ForceDisplace` | Number | Applies or references the 'ForceDisplace' effect/state. |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. |
| [`ForceImmediateMoveAndAttack`](#forceimmediatemoveandattack) | Block | Forces the character to immediately move to a target and use a specified ability. |
| `ForceMoveAndAttack` | Number | Applies or references the 'ForceMoveAndAttack' effect/state. |
| `ForceMoveAway` | Number | Applies or references the 'ForceMoveAway' effect/state. |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. |
| `ForceMoveTowardsEnemies` | Number | Applies or references the 'ForceMoveTowardsEnemies' effect/state. |
| [`ForceMoveTowardsTaggedObject`](#forcemovetowardstaggedobject) | Block | Forces the character to move towards the nearest object with a specific tag. |
| `ForceTransferWeapon` | Number | Applies or references the 'ForceTransferWeapon' effect/state. |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies or references the 'ForceUseAbility' effect/state. |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | Applies or references the 'ForceUseAbility_NonStack' effect/state. |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FreeSpell` | Number | Applies or references the 'FreeSpell' effect/state. |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. |
| [`GainCoinsRange`](#gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Applies or references the 'GainDisorder' effect/state. |
| [`GainDisorderFromPool`](./Enums.md#enum-gaindisorderfrompool) | Enum | Applies or references the 'GainDisorderFromPool' effect/state. |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |
| `GenericBuff` | Number | Applies or references the 'GenericBuff' effect/state. |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. |
| `GiveBoundItemToTarget` | Number | Applies or references the 'GiveBoundItemToTarget' effect/state. |
| `GlobalHealthRegenAura` | Number |  |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| [`GlobalSpawnOnRoundEnd`](#globalspawnonroundend) | Block |  |
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
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Applies or references the 'Imprison' effect/state. |
| [`IncAuxCounterCycle`](#incauxcountercycle) | Block | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. |
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
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | Applies or references the 'KnockOutClone' effect/state. |
| `KnockOutCoin` | Number | Forces the target to drop coins. |
| [`KnockUpAndAway`](#knockupandaway) | Block | Displaces the target vertically and horizontally away from the source. |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. |
| `KnockbackDamageImmuneUntilSettled` | Number | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. |
| `KnockbackDirectionIsFacingDirection` | Number | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. |
| [`LateStatusApplication`](#latestatusapplication) | Block | Applies a status effect after all primary damage and effects have fully resolved. |
| [`LaunchOffScreen`](./Math_Equations.md) | Equation | Applies or references the 'LaunchOffScreen' effect/state. |
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
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. |
| `ManaLeeches` | Number | Applies or references the 'ManaLeeches' effect/state. |
| `ManaSteal` | Number | Applies or references the 'ManaSteal' effect/state. |
| `ManaStealToHealth` | Number | Applies or references the 'ManaStealToHealth' effect/state. |
| `ManglerAttack` | Number | Applies or references the 'ManglerAttack' effect/state. |
| `ManglerShuffle` | Boolean | Applies or references the 'ManglerShuffle' effect/state. |
| `Marked` | Number | Applies or references the 'Marked' effect/state. |
| `MassAttackThis` | Number | Applies or references the 'MassAttackThis' effect/state. |
| [`Math`](#math) | Block | Triggers the Tinkerer's Math ability sequence. |
| `MaxHPUp` | Number | Applies or references the 'MaxHPUp' effect/state. |
| `Meaty` | Number | Applies or references the 'Meaty' effect/state. |
| [`MergeDamageInstance`](#mergedamageinstance) | Block | Combines damage numbers or visual hit effects. |
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
| [`NextBasicAttackCritsThisTurn`](#nextbasicattackcritsthisturn) | Block | Guarantees the next basic attack executed this turn will be a critical hit. |
| [`NextBattleStatusStacks`](#nextbattlestatusstacks) | Block | Carries over the specified status effects into the next encounter/battle. |
| `NextDamageReduceAndHealAllies` | Number | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. |
| `NextTurnDoubleRangedDamage` | Number | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. |
| `NonStackingDivineShield` | Number | Applies or references the 'NonStackingDivineShield' effect/state. |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum | Spawns a specific physics/item object upon impact. |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | Spawns a specific character or entity upon impact. |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Applies or references the 'ObjectOnHitEmpty' effect/state. |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. |
| `Ostracized` | Number | Applies or references the 'Ostracized' effect/state. |
| `OverHealToShield` | Number | Applies or references the 'OverHealToShield' effect/state. |
| [`OverHealToStatuses`](#overhealtostatuses) | Block | Converts excessive healing beyond maximum health into specific status effects. |
| `OverrideChainKnockback` | Number | Applies or references the 'OverrideChainKnockback' effect/state. |
| [`OverrideChainKnockbackDamage`](./Math_Equations.md) | Equation | Applies or references the 'OverrideChainKnockbackDamage' effect/state. |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. |
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum | Applies or references the 'OverrideKnockbackDamage' effect/state. |
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
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum |  |
| `Petrify` | Number | Applies or references the 'Petrify' effect/state. |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. |
| `Poison` | Number | Applies or references the 'Poison' effect/state. |
| `PoisonLace` | Number | Applies or references the 'PoisonLace' effect/state. |
| [`PoolMetronome`](#poolmetronome) | Block | Executes a random ability drawn from a specific pool. |
| [`PopAndSpawn`](./Enums.md#enum-popandspawn) | Enum | Destroys the target and replaces it with a new spawned entity. |
| `Possessed` | Number | Applies or references the 'Possessed' effect/state. |
| `ProbeCharmed` | Number | Applies or references the 'ProbeCharmed' effect/state. |
| `PullSourceToKnockbackImmuneTarget` | Number | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. |
| `PullSourceToTarget` | Number | Applies or references the 'PullSourceToTarget' effect/state. |
| `Purge` | Number | Applies or references the 'Purge' effect/state. |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. |
| [`QuakeAreaChance`](#quakeareachance) | Block | Provides a probability to trigger an earthquake Area of Effect. |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Applies or references the 'QueueUseAbility' effect/state. |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. |
| `RNGCannonRandomDamage` | Number | Applies or references the 'RNGCannonRandomDamage' effect/state. |
| `Rain` | Number |  |
| `RandomBonusDamage` | Number | Applies or references the 'RandomBonusDamage' effect/state. |
| `RandomDistanceDisplace` | Number | Displaces the target by a randomized distance. |
| `RandomInjury` | Number | Applies or references the 'RandomInjury' effect/state. |
| [`RandomKnockback`](#randomknockback) | Block | Applies a randomized amount of knockback force. |
| `RandomKnockbackDirection` | Number | Applies or references the 'RandomKnockbackDirection' effect/state. |
| `RandomLightning` | Number |  |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. |
| `RandomPermanentStat` | Number | Applies or references the 'RandomPermanentStat' effect/state. |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. |
| [`RandomStatusFromPool`](#randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. |
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array |  |
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
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Applies or references the 'RemoveItem' effect/state. |
| `RemoveKnockback` | Number | Applies or references the 'RemoveKnockback' effect/state. |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | Applies or references the 'RemoveStatus' effect/state. |
| [`RemoveStatusStacks`](#removestatusstacks) | Block | Removes a specific number of stacks of a status effect. |
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
| [`ScatterCoins`](#scattercoins) | Block | Throws coins out into the level randomly. |
| `ScatterHeldCoin` | Number | Applies or references the 'ScatterHeldCoin' effect/state. |
| `ScatterRandomPickups` | Number | Applies or references the 'ScatterRandomPickups' effect/state. |
| `ScrambleEverything` | Number | Applies or references the 'ScrambleEverything' effect/state. |
| [`ScrambleLastUsedSpell`](#scramblelastusedspell) | Block | Randomizes or scrambles the properties of the last spell cast. |
| `Scrambled` | Number | Applies or references the 'Scrambled' effect/state. |
| `SelfStun` | Number | Applies or references the 'SelfStun' effect/state. |
| `SendRock` | Number | Applies or references the 'SendRock' effect/state. |
| [`SetAnimationAlts`](#setanimationalts) | Block | Overrides specific animation states with alternative animations. |
| [`SetCrazyEyeBackgroundWeights`](#setcrazyeyebackgroundweights) | Block | Adjusts visual rendering weights for the 'Crazy Eye' background effect. |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Applies or references the 'SetDefaultFace' effect/state. |
| `SetDistanceDisplace` | Number | Applies or references the 'SetDistanceDisplace' effect/state. |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. |
| [`SetItemAux`](#setitemaux) | Block | Applies or references the 'SetItemAux' effect/state. |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. |
| `ShadowCrit` | Number | Applies or references the 'ShadowCrit' effect/state. |
| `Shatter` | Number | Applies or references the 'Shatter' effect/state. |
| `Shield` | Number | Applies or references the 'Shield' effect/state. |
| `ShootHereCommand` | Number | Applies or references the 'ShootHereCommand' effect/state. |
| `ShootHereReceiver` | Number | Applies or references the 'ShootHereReceiver' effect/state. |
| `ShortCircuit` | Number | Applies or references the 'ShortCircuit' effect/state. |
| [`ShowFakeDamage`](#showfakedamage) | Block | Displays a visual damage number without actually modifying health. |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. |
| `SignalFinalBossShieldBroke` | Number | Applies or references the 'SignalFinalBossShieldBroke' effect/state. |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum | Applies or references the 'SizeScale' effect/state. |
| `Sleep` | Number | Applies or references the 'Sleep' effect/state. |
| `Slow` | Number | Applies or references the 'Slow' effect/state. |
| `SmallHitExplosion` | Number | Applies or references the 'SmallHitExplosion' effect/state. |
| `SmartMetronome` | Number | Executes a 'smart' random ability that aims to be beneficial based on context. |
| `SmellBlood` | Number | Applies or references the 'SmellBlood' effect/state. |
| `Snow` | Number |  |
| [`SolarFlare`](#solarflare) | Block |  |
| `SoulLink` | Number | Applies or references the 'SoulLink' effect/state. |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Applies or references the 'SoundEventOnHit' effect/state. |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. |
| `SpawnBearTrap` | Number | Applies or references the 'SpawnBearTrap' effect/state. |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. |
| `SpawnCoinAnywhere` | Number | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `SpawnCreep` | Number | Applies or references the 'SpawnCreep' effect/state. |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Applies or references the 'SpawnCustomTrap' effect/state. |
| [`SpawnExtraThingsOnBattleStart`](#spawnextrathingsonbattlestart) | Block |  |
| [`SpawnFlames`](./Arrays.md#array-spawnflames) | Array | Applies or references the 'SpawnFlames' effect/state. |
| `SpawnNeutralWebTrapOnMiss` | Number | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. |
| `SpawnRock` | Number | Applies or references the 'SpawnRock' effect/state. |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| [`SpawnTilePuddleOnBattleStart`](#spawntilepuddleonbattlestart) | Block |  |
| [`SpawnVolcanoOnBattleStart`](#spawnvolcanoonbattlestart) | Block |  |
| `SpawnWebTrap` | Number | Applies or references the 'SpawnWebTrap' effect/state. |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Applies or references the 'SpecialBossMultipartInstakill' effect/state. |
| [`SpecialGodRays`](#specialgodrays) | Block |  |
| [`SpecificInjury`](./Enums.md#enum-specificinjury) | Enum | Applies or references the 'SpecificInjury' effect/state. |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. |
| `SpellShield` | Number | Applies or references the 'SpellShield' effect/state. |
| `SpiderInfested` | Number | Applies or references the 'SpiderInfested' effect/state. |
| `SpitConsumed` | Number | Applies or references the 'SpitConsumed' effect/state. |
| `SplashDamage` | Number | Applies or references the 'SplashDamage' effect/state. |
| [`SpreadDisease`](#spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. |
| `StackingSandstorm` | Number | Applies or references the 'StackingSandstorm' effect/state. |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. |
| `StatBounty` | Number | Applies or references the 'StatBounty' effect/state. |
| [`StatusAllCharactersOnSpawn`](#statusallcharactersonspawn) | Block |  |
| [`StatusCharactersOnRoundEnd`](#statuscharactersonroundend) | Block |  |
| [`StatusCharactersOnRoundStart`](#statuscharactersonroundstart) | Block |  |
| [`StatusGroup`](#statusgroup) | Block | Groups multiple status effects together for batch application. |
| `StealDemonicGlyph` | Number | Applies or references the 'StealDemonicGlyph' effect/state. |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Applies or references the 'StealEquipment' effect/state. |
| `StealTurn` | Number | Applies or references the 'StealTurn' effect/state. |
| `Stealth` | Number | Applies or references the 'Stealth' effect/state. |
| `StealthCritChance` | Number | Applies or references the 'StealthCritChance' effect/state. |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Number | Applies or references the 'Stun' effect/state. |
| `SwallowSmallCharacter` | Number | Applies or references the 'SwallowSmallCharacter' effect/state. |
| `SwapHighestAndLowestStat` | Number | Applies or references the 'SwapHighestAndLowestStat' effect/state. |
| [`SwapWeapon`](#swapweapon) | Block | Replaces the character's currently equipped weapon with one from a specified pool. |
| [`SwitchMusic`](#switchmusic) | Block | Changes the background music track or layer during combat. |
| `Switcheroo` | Number | Applies or references the 'Switcheroo' effect/state. |
| `T2CopyCat` | Number | Applies or references the 'T2CopyCat' effect/state. |
| `T3HitlerTriggerInitialSpawns` | Number | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Applies or references the 'TagMetronome' effect/state. |
| [`TakeBonusTurnWithAIControl`](#takebonusturnwithaicontrol) | Block | Grants the character an immediate extra turn, but forces the AI to control them during it. |
| [`TakeBonusTurnWithStatus`](#takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. |
| `TakeExtraTurnEndOfRound` | Number | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. |
| `Tangled` | Number | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `TargetedMetronome` | Number | Applies or references the 'TargetedMetronome' effect/state. |
| `Tarred` | Number | Applies or references the 'Tarred' effect/state. |
| `Taunting` | Number | Applies or references the 'Taunting' effect/state. |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Applies or references the 'TeamBonusAbility' effect/state. |
| [`TeamCastAbility`](./Enums.md#enum-teamcastability) | Enum | Requires or involves multiple characters to execute the ability. |
| `Tech` | Number | Applies or references the 'Tech' effect/state. |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Applies or references the 'TeleportBackAtTurnEnd' effect/state. |
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
| [`TempDexterityUp`](./Enums.md#enum-tempdexterityup) | Enum | Applies or references the 'TempDexterityUp' effect/state. |
| `TempInitiativeChange` | Number | Applies or references the 'TempInitiativeChange' effect/state. |
| `TempInjuryImmunity` | Number | Applies or references the 'TempInjuryImmunity' effect/state. |
| `TempLuckUp` | Number | Applies or references the 'TempLuckUp' effect/state. |
| `TempManaCostReduction` | Number | Applies or references the 'TempManaCostReduction' effect/state. |
| `TempMovement` | Number | Applies or references the 'TempMovement' effect/state. |
| [`TempPassiveUntilSettled`](#temppassiveuntilsettled) | Block | Passive: Active only until the physics engine stops moving the character. |
| [`TempPassiveWhileHasStatus`](#temppassivewhilehasstatus) | Block | Grants nested passives only while the character possesses the specified status. |
| `TempPenetrate` | Number | Applies or references the 'TempPenetrate' effect/state. |
| `TempPreEmptiveCounterAttack` | Number | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. |
| `TempRangeUp` | Number | Applies or references the 'TempRangeUp' effect/state. |
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum | Applies or references the 'TempSpeedUp' effect/state. |
| `TempSpellDamageUp` | Number | Applies or references the 'TempSpellDamageUp' effect/state. |
| [`TempStrengthUp`](./Enums.md#enum-tempstrengthup) | Enum | Applies or references the 'TempStrengthUp' effect/state. |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. |
| [`Temporary`](#temporary) | Block | A wrapper block for applying status effects that automatically expire. |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. |
| `ThornsDamageImmuneUntilSettled` | Number | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Applies or references the 'TickDownStatus' effect/state. |
| `TileDamageImmuneUntilSettled` | Number | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. |
| `TilesMovedToCritChance` | Number | Applies or references the 'TilesMovedToCritChance' effect/state. |
| `TilesMovedToMana` | Number | Applies or references the 'TilesMovedToMana' effect/state. |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Applies or references the 'TilesMovedToNeighborHeal' effect/state. |
| `TilesMovedToStrength` | Number | Applies or references the 'TilesMovedToStrength' effect/state. |
| [`TimeDelayStatusApplication`](#timedelaystatusapplication) | Block | Delays the nested effects by a specified amount of real-time seconds. |
| `TowerDefenseStatus` | Number | Applies or references the 'TowerDefenseStatus' effect/state. |
| `TowerDefenseStatus2` | Number | Applies or references the 'TowerDefenseStatus2' effect/state. |
| `TradeLife` | Number | Applies or references the 'TradeLife' effect/state. |
| `TrailBlazer` | Number | Applies or references the 'TrailBlazer' effect/state. |
| `Trample` | Number | Applies or references the 'Trample' effect/state. |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Applies or references the 'TransformAbility' effect/state. |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Applies or references the 'TransformBasicAttack' effect/state. |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Applies or references the 'TransformBasicMove' effect/state. |
| [`TransformEquipment`](#transformequipment) | Block | Upgrades or transforms a specific equipped item into another. |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Applies or references the 'TransformNow' effect/state. |
| [`TransformWeapon`](#transformweapon) | Block | Transforms the equipped weapon into another specific weapon state. |
| `Trapper_Status` | Number | Applies or references the 'Trapper_Status' effect/state. |
| `TriggerDOTStatuses` | Number | Applies or references the 'TriggerDOTStatuses' effect/state. |
| `TriggerGameEnding` | Number | Applies or references the 'TriggerGameEnding' effect/state. |
| `TriggerMotherConsume` | Number | Applies or references the 'TriggerMotherConsume' effect/state. |
| `TriggerMotherGrow` | Number | Applies or references the 'TriggerMotherGrow' effect/state. |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array | Applies or references the 'TriggerWerewolfTransform' effect/state. |
| `TurnAround` | Number | Applies or references the 'TurnAround' effect/state. |
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Enum | Applies or references the 'TurnControlDelay' effect/state. |
| `TurnRight` | Number | Applies or references the 'TurnRight' effect/state. |
| [`TwisterDisplaceWithDamage`](#twisterdisplacewithdamage) | Block | A whirlwind effect that randomly displaces targets and deals damage. |
| `UndoDamage` | Number | Applies or references the 'UndoDamage' effect/state. |
| `UpgradeRandomAbility` | Number | Applies or references the 'UpgradeRandomAbility' effect/state. |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Forces the character or target to instantly use a specified ability. |
| [`UseMoveAbilityWithAI`](#usemoveabilitywithai) | Block | Forces the character to execute a movement ability using specific AI weights. |
| `UseRandomSpell_Madness` | Number | Applies the 'UseRandomSpell_Madness' effect. |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. |
| [`VaporizeCorpseFlipAdvantage`](./Arrays.md#array-vaporizecorpseflipadvantage) | Array | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. |
| `VaporizeDice` | Number | Applies or references the 'VaporizeDice' effect/state. |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. |
| `VaporizeTarget` | Number | Applies or references the 'VaporizeTarget' effect/state. |
| [`VisualCountDownThenApplyStatus`](#visualcountdownthenapplystatus) | Block | Displays a visual countdown above the target before applying the nested effects. |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | Applies or references the 'VisualFX' effect/state. |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Applies or references the 'VisualFXTile' effect/state. |
| `VisualFlySwarm` | Number |  |
| [`WaggleClone`](#waggleclone) | Block | Spawns visual clones or alternative hitbox variants of the projectile. |
| `Weakness` | Number | Applies or references the 'Weakness' effect/state. |
| [`WeaponAuxMultiplier`](./Enums.md#enum-weaponauxmultiplier) | Enum | Applies or references the 'WeaponAuxMultiplier' effect/state. |
| `Webbed` | Number | Applies or references the 'Webbed' effect/state. |
| `Windy` | Number |  |
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
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum |  |
| `threshold_flat` | Number | A flat numerical health value threshold. |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). |
| `use_placeholder` | Boolean |  |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. |
| `wet` | Boolean |  |
| `{Global Modifiers}` | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |
| [`{Logic Blocks}`](#{logic blocks}) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |
| `{Statuses / Passives}` | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |

</details>

### Valid Nested Blocks

The following blocks all behave as `[logic_block]` containers. Each has its own unique parameters listed below its entry.

---

#### `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. |

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. |

</details>

---

#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. |
| [`Conditional_Speculative`](#conditional_speculative) | Block | Nested conditional. |

</details>

---

#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. |

</details>

---

#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. |

</details>

---

#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_InForm`](#conditional_inform) | Block | Nested conditional. |

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. |

</details>

---

#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `odds` | Number | The probability (0.0 to 1.0) of applying the debuff. |

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
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
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. |

</details>

---

#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. |

</details>

---

#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. |

</details>

---

#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. |

</details>

---

#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
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
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum |  |
| `threshold_flat` | Number | A flat numerical health value threshold. |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Block | Nested conditional. |

</details>

---

#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. |

</details>

---

#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `threshold_flat` | Number |  |

</details>

---

#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. |

</details>

---

#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. |

</details>

---

#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`key`](./Enums.md#enum-key) | Enum |  |

</details>

---

#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_IsSelf`](#conditional_isself) | Block | Nested conditional. |

</details>

---

#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `odds` | Number |  |

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. |

</details>

---

#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. |

</details>

---

#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |

</details>

---

#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. |

</details>

---

#### `Consumed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
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
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
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
| [`[logic_block]`](./Engine_LogicBlocks.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
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

