# Mewgenics Mod Developer Documentation: Engine: Logic Keys

## Engine: Logic Keys

This document is the authoritative reference for Logic Blocks. All of the contexts below can appear as dynamic keys inside an `effects {}` block, or directly inside abilities. Many of these are conditional wrappers that evaluate a condition before executing their nested block, while others redirect execution flow (e.g. `ApplyToSource`).

> **Note:** Because many of these contexts accept arbitrary nested Logic Blocks, any entry marked `{Logic Keys}` recursively refers back to this same document.

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-root), [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`temporary_effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temporary_effects), [`Else` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-else), [`ApplyToSource` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_ally), [`Consumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-consumed), [`Conditional_Boss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_speculative), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`Conditional_Corpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_playercat), [`ApplyToConsumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytoconsumed), [`TimeDelayStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-post_spawn_statuses), [`Conditional_AffectedByElement` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_lasthit), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`ApplyToTile` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytotile), [`Conditional_BadRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_DestructibleCorpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_destructiblecorpse), [`Conditional_Displaceable` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_displaceable), [`Conditional_IsSelf` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_isself), [`Conditional_OncePerBattle` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_shielded), [`ApplyToRandomClosestAlly` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandomclosestally), [`Conditional_Backstab` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_backstab), [`Conditional_FinishedSpawning` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_finishedspawning), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Conditional_IsTrample` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_istrample), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_NotBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notbig), [`Conditional_RandomChance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_randomchance), [`NextBattleStatusStacks` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-nextbattlestatusstacks), [`ROOT` (Boss_Cutscene_Info)](./Boss_Cutscene_Info.md#context-root), [`ROOT` (Cat_Classes)](./Cat_Classes.md#context-root), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`Conditional_RandomChance` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_randomchance), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_goodroll), [`ROOT` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-root), [`FormChanger` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-formchanger), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`Consumed` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-consumed), [`Conditional_GoodRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_goodroll), [`Conditional_BadRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-else), [`FinalBossBecomeTheChild` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbossbecomethechild), [`InfiniteRebirth` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-infiniterebirth), [`TVBotScreen` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-tvbotscreen), [`ROOT` (Custom_Cats)](./Custom_Cats.md#context-root), [`ROOT` (Damage_Text_Styles)](./Damage_Text_Styles.md#context-root), [`ROOT` (Difficulties)](./Difficulties.md#context-root), [`ROOT` (Elite_Buffs)](./Elite_Buffs.md#context-root), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`ROOT` (Enemy_AI)](./Enemy_AI.md#context-root), [`ROOT` (Events_and_Encounters)](./Events_and_Encounters.md#context-root), [`global_effect_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-global_effect_next_fight), [`ROOT` (Furniture_and_Metaprogression)](./Furniture_and_Metaprogression.md#context-root), [`ROOT` (House_and_Environment)](./House_and_Environment.md#context-root), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`Else` (House_and_Environment)](./House_and_Environment.md#context-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundend), [`Conditional_GoodRoll` (House_and_Environment)](./House_and_Environment.md#context-conditional_goodroll), [`Conditional_Corpse` (House_and_Environment)](./House_and_Environment.md#context-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](./House_and_Environment.md#context-conditional_partymember), [`ROOT` (Injuries)](./Injuries.md#context-root), [`ROOT` (Items_and_Equipment)](./Items_and_Equipment.md#context-root), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`Conditional_GoodRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_goodroll), [`ApplyToSource` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytosource), [`Conditional_HasStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else` (Items_and_Equipment)](./Items_and_Equipment.md#context-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`Conditional_PartyMember` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_partymember), [`Conditional_Adjacent` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_onceperbattle), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytorandompartymemberifpossible), [`CastAgainWithStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-castagainwithstatus), [`Conditional_Ally` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_enemy), [`Conditional_HasCleansableDebuffs` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`Conditional_HealthThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_healththreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_shielded), [`CyborgTurns` (Items_and_Equipment)](./Items_and_Equipment.md#context-cyborgturns), [`ScaldingOrbMoonBossOneShot` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot), [`StatusAdjacentOnTheirTurnEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusadjacentontheirturnend), [`StatusOnFallAsleep` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonfallasleep), [`StatusOnTurnEndIfCastNSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifcastnspells), [`ROOT` (Item_Pools)](./Item_Pools.md#context-root), [`ROOT` (Map_Generation_and_Routing)](./Map_Generation_and_Routing.md#context-root), [`ROOT` (Miscellaneous)](./Miscellaneous.md#context-root), [`ROOT` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-root), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects), [`StatusOnStanceSwitch` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonstanceswitch), [`Conditional_Ally` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_enemy), [`Else` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-else), [`StatusOnOverHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonoverhealed), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaexact), [`Conditional_BadRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hasstatus), [`AddStatusToBasicAttackWithCooldown` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicattackwithcooldown), [`AddStatusToMeleeDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustomeleedamage), [`ApplyToSource` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applytosource), [`Conditional_Adjacent` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_shielded), [`EscapeSequence` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-escapesequence), [`InfiniteRebirth` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-infiniterebirth), [`StatusOnDealtDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamage), [`on_throw` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-on_throw), [`Conditional_GoodRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_goodroll), [`StatusAdjacentOnTheirTurnBegin` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin), [`ROOT` (Progression_Unlocks)](./Progression_Unlocks.md#context-root), [`ROOT` (Shops)](./Shops.md#context-root), [`ROOT` (Spawns_and_Enemy_Pools)](./Spawns_and_Enemy_Pools.md#context-root), [`ROOT` (Status_Effect_Keywords)](./Status_Effect_Keywords.md#context-root)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#effects) | Block |  | 2166 |
| `FormChange` | Variable |  | 114 |
| `Burn` | Variable |  | 88 |
| `Bruise` | Variable |  | 79 |
| [`Else`](#else) | Block |  | 76 |
| `IgnoreSelf` | Integer | Applies or references the 'IgnoreSelf' effect/state. | 75 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 65 |
| `ChangeTile` | Variable |  | 62 |
| `Shield` | Variable |  | 59 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 58 |
| `Cleanse` | Variable |  | 52 |
| `odds` | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 50 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 48 |
| `AllStatsUp` | Variable |  | 48 |
| [`ApplyToSource`](#applytosource) | Block |  | 47 |
| `Temporary` | Variable |  | 46 |
| `Confusion` | Variable |  | 44 |
| [`Conditional_HasTag`](#conditionalhastag) | Block |  | 42 |
| `Stun` | Variable |  | 41 |
| `SpeedUp` | Variable |  | 40 |
| [`Conditional_Enemy`](#conditionalenemy) | Block |  | 38 |
| `VisualFXTile` | Variable |  | 36 |
| `BounceObject` | Variable |  | 35 |
| `ManaGain` | Variable |  | 31 |
| `Slow` | Variable |  | 30 |
| `StrengthUp` | Variable |  | 29 |
| `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. | 29 |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Applies or references the 'TransformAbility' effect/state. | 28 |
| `SpawnExtraThingsOnBattleStart` | Variable |  | 28 |
| [`Conditional_Ally`](#conditionalally) | Block |  | 27 |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum | Upgrades or transforms an existing ability into a new one from the specified pool. | 26 |
| `Charmed` | Variable |  | 25 |
| `ConstitutionUp` | Variable |  | 25 |
| `Immobile` | Variable |  | 24 |
| `BonusDamage` | Variable |  | 23 |
| `KnockUpAndAway` | Variable |  | 23 |
| `Leech` | Variable |  | 22 |
| `Madness` | Variable |  | 22 |
| `RandomStatusFromPool` | Variable |  | 22 |
| `TakeExtraTurn` | Variable |  | 22 |
| `Weakness` | Variable |  | 22 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 21 |
| `Freeze` | Variable |  | 21 |
| `IntelligenceUp` | Variable |  | 21 |
| `Blind` | Variable |  | 20 |
| `Sleep` | Variable |  | 19 |
| [`Consumed`](#consumed) | Block |  | 18 |
| `Petrify` | Variable |  | 18 |
| `VaporizeCorpse` | Integer | Applies or references the 'VaporizeCorpse' effect/state. | 18 |
| [`Conditional_Boss`](#conditionalboss) | Block |  | 17 |
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum | Applies or references the 'OverrideKnockbackDamage' effect/state. | 17 |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 17 |
| `CollectsPickups` | Integer | Applies or references the 'CollectsPickups' effect/state. | 17 |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 16 |
| `FullHeal` | Variable |  | 16 |
| `Leeches` | Variable |  | 16 |
| `OverrideDamage` | Integer | Applies or references the 'OverrideDamage' effect/state. | 16 |
| `Revive` | Variable |  | 16 |
| [`ApplyToSourceOnKill`](#applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 15 |
| [`CanApplyToInanimate`](#canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 15 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block |  | 15 |
| `Cleave` | Variable |  | 15 |
| `FaceAway` | Variable |  | 15 |
| `GenericDebuff` | Integer | Applies or references the 'GenericDebuff' effect/state. | 15 |
| `RefreshMovePoints` | Variable |  | 15 |
| `RemoveStatus` | Variable |  | 15 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 15 |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Applies or references the 'ChangeCatClass' effect/state. | 14 |
| [`Conditional_NotBoss`](#conditionalnotboss) | Block |  | 14 |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Applies or references the 'TransformBasicAttack' effect/state. | 14 |
| `CatPartsTransform` | Variable |  | 14 |
| `EndTurn` | Integer | Applies or references the 'EndTurn' effect/state. | 14 |
| `RefreshActPoints` | Variable |  | 14 |
| [`ApplyPassives`](#applypassives) | Block | Grants the nested passive abilities dynamically. | 13 |
| [`Conditional_HasStatus`](#conditionalhasstatus) | Block |  | 13 |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | Applies or references the 'VisualFX' effect/state. | 13 |
| [`Conditional_Speculative`](#conditional_speculative) | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 12 |
| `AlphaCat` | Variable |  | 12 |
| `Displace` | Integer | Applies or references the 'Displace' effect/state. | 12 |
| `instant` | Boolean |  | 12 |
| `mount_mode` | Boolean | If true, treats the consumption as riding/mounting instead of eating. | 12 |
| `rock` | Variable |  | 12 |
| [`ChanceToBreakFree`](#chancetobreakfree) | Block | Provides a probability to escape a grapple or restraining effect. | 11 |
| [`DoScreenShake`](#doscreenshake) | Block | Triggers a camera screen shake effect. | 11 |
| `Instakill` | Variable |  | 11 |
| `Marked` | Variable |  | 11 |
| `PurgeAll` | Integer | Applies or references the 'PurgeAll' effect/state. | 11 |
| `do_not_pop_corpse` | Boolean |  | 11 |
| `drop_on_death` | Boolean |  | 11 |
| [`Conditional_FormulaIsPositive`](#conditional_formulaispositive) | Block | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 10 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | Applies or references the 'SpawnThingIfHitKills' effect/state. | 10 |
| `DexterityUp` | Variable |  | 10 |
| `KnockbackDamageImmuneUntilSettled` | Integer | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 10 |
| `PartialPurge` | Integer | Applies or references the 'PartialPurge' effect/state. | 10 |
| `X` | Variable |  | 10 |
| `Ammo` | Variable |  | 9 |
| `ChanceToBreak` | Variable |  | 9 |
| `Craft` | Variable |  | 9 |
| `DeferVaporize` | Integer | Applies or references the 'DeferVaporize' effect/state. | 9 |
| `IgnoreDamage` | Integer | Applies or references the 'IgnoreDamage' effect/state. | 9 |
| `OverrideChainKnockback` | Variable |  | 9 |
| `SpawnCreep` | Integer | Applies or references the 'SpawnCreep' effect/state. | 9 |
| [`Conditional_Corpse`](#conditionalcorpse) | Block |  | 8 |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 |
| `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 8 |
| `MagicWeakness` | Variable |  | 8 |
| `SpreadDisease` | Variable |  | 8 |
| `Tech` | Variable |  | 8 |
| `wet` | Boolean |  | 8 |
| [`Conditional_InForm`](#conditional_inform) | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 7 |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 7 |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. | 7 |
| `ApplyStatusIfCrit` | Variable |  | 7 |
| `BramblesOnHit` | Integer | Applies or references the 'BramblesOnHit' effect/state. | 7 |
| `ContextualHeal` | Integer | Applies or references the 'ContextualHeal' effect/state. | 7 |
| `Drowsy` | Variable |  | 7 |
| `ForceAttack` | Variable |  | 7 |
| `ImmediateUseAbility` | Variable |  | 7 |
| `ManaSteal` | Integer | Applies or references the 'ManaSteal' effect/state. | 7 |
| `SetHealth` | Variable |  | 7 |
| `TempDamageUp` | Variable |  | 7 |
| `TempRangeUp` | Variable |  | 7 |
| `VaporizeInanimate` | Variable |  | 7 |
| [`Conditional_HealthThreshold`](#conditionalhealththreshold) | Block |  | 6 |
| [`Conditional_Object`](#conditional_object) | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 |
| [`DoDistortionRing`](#dodistortionring) | Block | Creates a visual distortion ring effect on the screen. | 6 |
| [`PopAndSpawn`](./Enums.md#enum-popandspawn) | Enum | Destroys the target and replaces it with a new spawned entity. | 6 |
| [`TeamCastAbility`](./Enums.md#enum-teamcastability) | Enum | Requires or involves multiple characters to execute the ability. | 6 |
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum | Applies or references the 'TempSpeedUp' effect/state. | 6 |
| [`TwisterDisplaceWithDamage`](#twisterdisplacewithdamage) | Block | A whirlwind effect that randomly displaces targets and deals damage. | 6 |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 6 |
| `BackflipWhenTargeted` | Variable |  | 6 |
| `CaptureFamiliar` | Variable |  | 6 |
| `ClearStarving` | Integer | Applies or references the 'ClearStarving' effect/state. | 6 |
| `ConjureBonusAbility` | Variable |  | 6 |
| `Die` | Integer | Applies or references the 'Die' effect/state. | 6 |
| `Doomed` | Variable |  | 6 |
| `FactionConversion` | Integer | Applies or references the 'FactionConversion' effect/state. | 6 |
| `FillMana` | Variable |  | 6 |
| `FlatLeech` | Variable |  | 6 |
| `FloatingRockTrap` | Integer | Applies or references the 'FloatingRockTrap' effect/state. | 6 |
| `ForceMoveTowards` | Integer | Applies or references the 'ForceMoveTowards' effect/state. | 6 |
| `Metronome` | Integer | Executes a random musical or metronome ability. | 6 |
| `RandomInjury` | Variable |  | 6 |
| `SetDistanceDisplace` | Integer | Applies or references the 'SetDistanceDisplace' effect/state. | 6 |
| `SpiderInfested` | Variable |  | 6 |
| `UseAbility` | Variable |  | 6 |
| `Webbed` | Variable |  | 6 |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 6 |
| [`CollectsPickupsWithAltEffects`](#collectspickupswithalteffects) | Block | Triggers alternative nested effects when collecting items or pickups. | 5 |
| [`Conditional_IsSelf`](#conditional_isself) | Block | Conditional trigger: Executes nested logic if the target is the caster themselves. | 5 |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Applies or references the 'Imprison' effect/state. | 5 |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Applies or references the 'ObjectOnHitEmpty' effect/state. | 5 |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum | Spawns a specific physics/item object upon impact. | 5 |
| [`SpecificInjury`](./Enums.md#enum-specificinjury) | Enum | Applies or references the 'SpecificInjury' effect/state. | 5 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| `DestroyEquipmentAndAttachParasite` | Variable |  | 5 |
| `DisplaceTowardsSource` | Integer | Applies or references the 'DisplaceTowardsSource' effect/state. | 5 |
| `FaceCamera` | Integer | Applies or references the 'FaceCamera' effect/state. | 5 |
| `ForceMoveAway` | Integer | Applies or references the 'ForceMoveAway' effect/state. | 5 |
| `HitExplosion` | Integer | Applies or references the 'HitExplosion' effect/state. | 5 |
| `KnockbackDirectionIsFacingDirection` | Integer | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. | 5 |
| `LavaTile` | Variable |  | 5 |
| `MonkStanceSwitch` | Integer | Applies or references the 'MonkStanceSwitch' effect/state. | 5 |
| `MovementUp` | Variable |  | 5 |
| `PermanentCharm` | Integer | Applies the 'PermanentCharm' effect. | 5 |
| `Purge` | Variable |  | 5 |
| `RefreshMovePointsIfHit` | Integer | Applies or references the 'RefreshMovePointsIfHit' effect/state. | 5 |
| `SafeDie` | Variable |  | 5 |
| `SoulLink` | Variable |  | 5 |
| `SpawnBearTrap` | Integer | Applies or references the 'SpawnBearTrap' effect/state. | 5 |
| `Stealth` | Variable |  | 5 |
| `UpgradeRandomAbility` | Integer | Applies or references the 'UpgradeRandomAbility' effect/state. | 5 |
| [`ApplyToConsumed`](#applytoconsumed) | Block | Redirects the nested effects to apply to the entity that just consumed this object. | 4 |
| [`ArcLightning`](#arclightning) | Block | Executes a chain-lightning logic block that bounces between targets. | 4 |
| [`BounceRock`](./Enums.md#enum-bouncerock) | Enum | Applies or references the 'BounceRock' effect/state. | 4 |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Applies or references the 'CompleteItemQuest' effect/state. | 4 |
| [`Conditional_Adjacent`](#conditional_adjacent) | Block |  | 4 |
| [`Conditional_Familiar`](#conditional_familiar) | Block | Conditional trigger: Executes nested logic if the target is a familiar. | 4 |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Applies or references the 'EnableWeather' effect/state. | 4 |
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum |  | 4 |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 4 |
| [`LateStatusApplication`](#latestatusapplication) | Block | Applies a status effect after all primary damage and effects have fully resolved. | 4 |
| [`SwitchMusic`](#switchmusic) | Block | Changes the background music track or layer during combat. | 4 |
| [`TempPassiveWhileHasStatus`](#temppassivewhilehasstatus) | Block | Grants nested passives only while the character possesses the specified status. | 4 |
| [`TimeDelayStatusApplication`](#timedelaystatusapplication) | Block | Delays the nested effects by a specified amount of real-time seconds. | 4 |
| `Default` | Variable |  | 4 |
| `DeleteObject` | Integer | Applies or references the 'DeleteObject' effect/state. | 4 |
| `DestroyTrinket` | Variable |  | 4 |
| `DieViolently` | Integer | Applies or references the 'DieViolently' effect/state. | 4 |
| `ExplosionIfHitSomething` | Integer | Applies or references the 'ExplosionIfHitSomething' effect/state. | 4 |
| `FreeSpell` | Integer | Applies or references the 'FreeSpell' effect/state. | 4 |
| `Grappled` | Integer | Applies or references the 'Grappled' effect/state. | 4 |
| `LowerAmbientLight` | Variable |  | 4 |
| `Rain` | Integer |  | 4 |
| `Reanimate` | Variable |  | 4 |
| `RefreshWeaponAbility` | Integer | Applies or references the 'RefreshWeaponAbility' effect/state. | 4 |
| `RemoveActPoints` | Integer | Applies or references the 'RemoveActPoints' effect/state. | 4 |
| `RepairAll` | Variable |  | 4 |
| `SendRock` | Integer | Applies or references the 'SendRock' effect/state. | 4 |
| `TakeBonusTurnWithStatus` | Variable |  | 4 |
| `Thrash` | Variable |  | 4 |
| `Windy` | Integer |  | 4 |
| `moonhand` | Variable |  | 4 |
| [`ApplyMultipleTimes`](#applymultipletimes) | Block | A loop block that executes its nested logic multiple times. | 3 |
| [`CatPartsSizeScaleStatus`](#catpartssizescalestatus) | Block | Visually scales specific body parts of a character. | 3 |
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | Applies or references the 'CollideWithConsumed' effect/state. | 3 |
| [`Conditional_AffectedByElement`](#conditional_affectedbyelement) | Block | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 3 |
| [`Conditional_FirstApplicationThisTurn`](#conditionalfirstapplicationthisturn) | Block |  | 3 |
| [`Conditional_LastHit`](#conditional_lasthit) | Block | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 3 |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Block | Conditional trigger: Executes nested logic only once per encounter/battle. | 3 |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | Applies or references the 'DoubleStatus' effect/state. | 3 |
| [`DustOnHit`](#dustonhit) | Block | Spawns a specific particle or cloud object upon impact. | 3 |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Applies or references the 'RemoveItem' effect/state. | 3 |
| [`SetCrazyEyeBackgroundWeights`](#setcrazyeyebackgroundweights) | Block | Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 3 |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Applies or references the 'SpawnCustomTrap' effect/state. | 3 |
| [`SpawnVolcanoOnBattleStart`](#spawnvolcanoonbattlestart) | Block |  | 3 |
| [`StatusCharactersOnRoundEnd`](#statuscharactersonroundend) | Block |  | 3 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 3 |
| [`extra_statuses`](#extra_statuses) | Block | Additional generic status applications. | 3 |
| `AddWeaponAux` | Variable |  | 3 |
| `Attraction` | Integer | Applies or references the 'Attraction' effect/state. | 3 |
| `BlackShard` | Variable |  | 3 |
| `BonusKnockbackDamage` | Variable |  | 3 |
| `CorpseVaporizer` | Integer | Applies or references the 'CorpseVaporizer' effect/state. | 3 |
| `CurrentWeaponDamageUp` | Variable |  | 3 |
| `DestroyWeaponThrow` | Integer | Applies or references the 'DestroyWeaponThrow' effect/state. | 3 |
| `DestroyWeapon` | Integer | Applies or references the 'DestroyWeapon' effect/state. | 3 |
| `DisplaceToAbilityTarget` | Integer | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 3 |
| `DoDamage` | Variable |  | 3 |
| `ExtraBasicAttacks_Status` | Variable |  | 3 |
| `FlatAIBonus` | Integer | Applies or references the 'FlatAIBonus' effect/state. | 3 |
| `ForceDisplace` | Integer | Applies or references the 'ForceDisplace' effect/state. | 3 |
| `ForceMoveTowardsEnemies` | Integer | Applies or references the 'ForceMoveTowardsEnemies' effect/state. | 3 |
| `Hex` | Variable |  | 3 |
| `InstantMaxHealthUp` | Integer | Applies or references the 'InstantMaxHealthUp' effect/state. | 3 |
| `Meteornado` | Integer |  | 3 |
| `NextAttackBonusRange` | Integer | Applies or references the 'NextAttackBonusRange' effect/state. | 3 |
| `PlayBackground` | Integer | Applies or references the 'PlayBackground' effect/state. | 3 |
| `PoisonLace` | Variable |  | 3 |
| `PullSourceToTarget` | Variable |  | 3 |
| `RemoveMovePoints` | Integer | Applies or references the 'RemoveMovePoints' effect/state. | 3 |
| `RepairOnKill` | Integer | Applies or references the 'RepairOnKill' effect/state. | 3 |
| `RepairWeapon` | Variable |  | 3 |
| `ReviveNextRound` | Variable |  | 3 |
| `SetShield` | Integer | Applies or references the 'SetShield' effect/state. | 3 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 3 |
| `SpawnNeutralWebTrapOnMiss` | Integer | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. | 3 |
| `SpawnRock` | Integer | Applies or references the 'SpawnRock' effect/state. | 3 |
| `SpeculativeMoveSelfCorpseOffMap` | Integer | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 3 |
| `StanceSwitchToMelee` | Integer | Applies or references the 'StanceSwitchToMelee' effect/state. | 3 |
| `Tangled` | Variable |  | 3 |
| `TempInitiativeChange` | Variable |  | 3 |
| `TempStrengthUp` | Variable |  | 3 |
| `TempTrampleUntilSettled` | Integer | Applies or references the 'TempTrampleUntilSettled' effect/state. | 3 |
| `TriggerGameEnding` | Integer | Applies or references the 'TriggerGameEnding' effect/state. | 3 |
| `VaporizeTarget` | Integer | Applies or references the 'VaporizeTarget' effect/state. | 3 |
| `WaterTile` | Variable |  | 3 |
| `ZombieCatFamiliar` | Variable |  | 3 |
| `drop_on_self_death` | Boolean |  | 3 |
| `poop` | Variable |  | 3 |
| [`ApplyToRandomPartyMemberIfPossible`](#applytorandompartymemberifpossible) | Block |  | 2 |
| [`ApplyToTile`](#applytotile) | Block | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 2 |
| [`BodyGuard`](#bodyguard) | Block | Protects an ally by intercepting attacks directed at them. | 2 |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Applies or references the 'ChangeFaction' effect/state. | 2 |
| [`CharacterTypeGainsStatusAtBattleStart`](#charactertypegainsstatusatbattlestart) | Block |  | 2 |
| [`Conditional_BadRoll`](#conditional_badroll) | Block |  | 2 |
| [`Conditional_BossOrBig`](#conditional_bossorbig) | Block | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 2 |
| [`Conditional_Buddy`](#conditional_buddy) | Block | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 2 |
| [`Conditional_DestructibleCorpse`](#conditional_destructiblecorpse) | Block | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 2 |
| [`Conditional_Displaceable`](#conditional_displaceable) | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| [`Conditional_NotAlly`](#conditional_notally) | Block | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 2 |
| [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Block | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 2 |
| [`Conditional_NotShielded`](#conditional_notshielded) | Block | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 2 |
| [`Conditional_PartyMember`](#conditional_partymember) | Block |  | 2 |
| [`Conditional_Shielded`](#conditional_shielded) | Block |  | 2 |
| [`DelayCastAbility`](./Enums.md#enum-delaycastability) | Enum | Queues an ability to be cast automatically after a certain delay or trigger. | 2 |
| [`ForceMoveTowardsTaggedObject`](#forcemovetowardstaggedobject) | Block | Forces the character to move towards the nearest object with a specific tag. | 2 |
| [`GlobalSpawnOnRoundEnd`](#globalspawnonroundend) | Block |  | 2 |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. | 2 |
| [`Math`](#math) | Block | Triggers the Tinkerer's Math ability sequence. | 2 |
| [`OverHealToStatuses`](#overhealtostatuses) | Block | Converts excessive healing beyond maximum health into specific status effects. | 2 |
| [`QuakeAreaChance`](#quakeareachance) | Block | Provides a probability to trigger an earthquake Area of Effect. | 2 |
| [`RandomKnockback`](#randomknockback) | Block | Applies a randomized amount of knockback force. | 2 |
| [`SpecialGodRays`](#specialgodrays) | Block |  | 2 |
| [`StatusCharactersOnRoundStart`](#statuscharactersonroundstart) | Block |  | 2 |
| [`TakeBonusTurnWithAIControl`](#takebonusturnwithaicontrol) | Block | Grants the character an immediate extra turn, but forces the AI to control them during it. | 2 |
| [`TempDexterityUp`](./Enums.md#enum-tempdexterityup) | Enum | Applies or references the 'TempDexterityUp' effect/state. | 2 |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array | Applies or references the 'TriggerWerewolfTransform' effect/state. | 2 |
| [`XIsTargetHealth`](#xistargethealth) | Block | Math variable assignment: Evaluates X as the target's current health. | 2 |
| `AddLeechesStatus` | Integer | Applies or references the 'AddLeechesStatus' effect/state. | 2 |
| `AddSpiritBombCharges` | Integer | Applies or references the 'AddSpiritBombCharges' effect/state. | 2 |
| `AutoReanimate` | Variable |  | 2 |
| `BonusDamageBasedOnDistance` | Integer | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 2 |
| `Bound` | Integer | Applies or references the 'Bound' effect/state. | 2 |
| `BurgleCoin` | Variable |  | 2 |
| `CancelPrimedAbilities` | Integer | Applies or references the 'CancelPrimedAbilities' effect/state. | 2 |
| `CharmedForceAttack` | Integer | Applies or references the 'CharmedForceAttack' effect/state. | 2 |
| `ClearNegativeEffects` | Integer | Applies the 'ClearNegativeEffects' effect. | 2 |
| `CollideWithThrowTarget` | Integer | Applies or references the 'CollideWithThrowTarget' effect/state. | 2 |
| `ConjureRandomAbilityFromCat` | Integer | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 2 |
| `CopySpells` | Integer | Duplicates existing spells currently in the character's hand. | 2 |
| `Counterspell` | Integer | Applies or references the 'Counterspell' effect/state. | 2 |
| `DamageBasedOnMissingHealth` | Integer | Applies or references the 'DamageBasedOnMissingHealth' effect/state. | 2 |
| `DamageDistanceAOEFalloff` | Integer | Applies or references the 'DamageDistanceAOEFalloff' effect/state. | 2 |
| `DamageTrinket` | Integer | Applies or references the 'DamageTrinket' effect/state. | 2 |
| `DelayedFury` | Integer | Applies or references the 'DelayedFury' effect/state. | 2 |
| `DieViaAbilityInternally` | Integer | Applies or references the 'DieViaAbilityInternally' effect/state. | 2 |
| `DisplaceToOriginalPosition` | Integer | Applies or references the 'DisplaceToOriginalPosition' effect/state. | 2 |
| `DoubleCastSpell` | Integer | Applies or references the 'DoubleCastSpell' effect/state. | 2 |
| `DoubleLoot` | Integer | Applies or references the 'DoubleLoot' effect/state. | 2 |
| `ExplodeCharacter_NoDie` | Integer | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 2 |
| `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 2 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 2 |
| `ExplodeCharacter_RockCrusher` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 2 |
| `ExplodeCharacter` | Integer | Applies or references the 'ExplodeCharacter' effect/state. | 2 |
| `FireStorm` | Integer |  | 2 |
| `FireTile` | Variable |  | 2 |
| `FlatLeechIfDamaged` | Integer | Applies or references the 'FlatLeechIfDamaged' effect/state. | 2 |
| `FlowersOnHit` | Integer | Applies or references the 'FlowersOnHit' effect/state. | 2 |
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. | 2 |
| `GainDisorderFromPool` | Variable |  | 2 |
| `HealRandomInjury` | Integer | Applies or references the 'HealRandomInjury' effect/state. | 2 |
| `HornCharge` | Variable |  | 2 |
| `JohnnyCriesForWashers` | Integer | Applies or references the 'JohnnyCriesForWashers' effect/state. | 2 |
| `KnockOutCoin` | Variable |  | 2 |
| `LeaveBehindRockOnKnockback` | Variable |  | 2 |
| `ManaLeeches` | Variable |  | 2 |
| `MaxHPUp` | Integer | Applies or references the 'MaxHPUp' effect/state. | 2 |
| `NextAttackSpecialCrit` | Integer | Modifies the character's next attack to have special critical properties. | 2 |
| `OffMap` | Variable |  | 2 |
| `OilTile` | Variable |  | 2 |
| `Ostracized` | Variable |  | 2 |
| `PartyExplosion` | Variable |  | 2 |
| `PermanentStrength` | Variable |  | 2 |
| `PermanentUpgradeRandomActive` | Integer | Applies or references the 'PermanentUpgradeRandomActive' effect/state. | 2 |
| `Pilfer` | Variable |  | 2 |
| `Possessed` | Variable |  | 2 |
| `PullSourceToKnockbackImmuneTarget` | Variable |  | 2 |
| `Pulp2` | Variable |  | 2 |
| `RandomDistanceDisplace` | Integer | Displaces the target by a randomized distance. | 2 |
| `RandomLightning` | Integer |  | 2 |
| `RandomPickup` | Variable |  | 2 |
| `RebukeDamage` | Integer | Applies or references the 'RebukeDamage' effect/state. | 2 |
| `ReduceManaCost` | Variable |  | 2 |
| `RemoveKnockback` | Integer | Applies or references the 'RemoveKnockback' effect/state. | 2 |
| `RemoveStatusStacks` | Variable |  | 2 |
| `RepairArmorCondition` | Integer | Applies or references the 'RepairArmorCondition' effect/state. | 2 |
| `RepairWeaponCondition` | Variable |  | 2 |
| `ResetArmorShield` | Integer | Applies or references the 'ResetArmorShield' effect/state. | 2 |
| `ScatterCoins` | Variable |  | 2 |
| `ScatterHeldCoin` | Integer | Applies or references the 'ScatterHeldCoin' effect/state. | 2 |
| `ScatterRandomPickups` | Integer | Applies or references the 'ScatterRandomPickups' effect/state. | 2 |
| `ScrambleEverything` | Integer | Applies or references the 'ScrambleEverything' effect/state. | 2 |
| `SetKnockback` | Integer | Applies or references the 'SetKnockback' effect/state. | 2 |
| `Shatter` | Integer | Applies or references the 'Shatter' effect/state. | 2 |
| `SignalFinalBossShieldBroke` | Integer | Applies or references the 'SignalFinalBossShieldBroke' effect/state. | 2 |
| `SmartMetronome` | Integer | Executes a 'smart' random ability that aims to be beneficial based on context. | 2 |
| `Snow` | Integer |  | 2 |
| `SpawnBearTrapIfHitKills` | Integer | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 2 |
| `SwallowSmallCharacter` | Integer | Applies or references the 'SwallowSmallCharacter' effect/state. | 2 |
| `TallGrassTile` | Variable |  | 2 |
| `TempCritChanceUp` | Integer | Applies or references the 'TempCritChanceUp' effect/state. | 2 |
| `TempMovement` | Variable |  | 2 |
| `TempPassiveUntilSettled` | Variable |  | 2 |
| `TempSpellDamageUp` | Variable |  | 2 |
| `ThornsDamageImmuneUntilSettled` | Integer | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 2 |
| `ThrowPoop` | Variable |  | 2 |
| `TileDamageImmuneUntilSettled` | Integer | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 2 |
| `TradeLife` | Integer | Applies or references the 'TradeLife' effect/state. | 2 |
| `TrailBlazer` | Integer | Applies or references the 'TrailBlazer' effect/state. | 2 |
| `TriggerDOTStatuses` | Integer | Applies or references the 'TriggerDOTStatuses' effect/state. | 2 |
| `VisualFlySwarm` | Integer |  | 2 |
| `gamewin` | Variable |  | 2 |
| `humanoid` | Variable |  | 2 |
| `megadino` | Variable |  | 2 |
| `moonhead` | Variable |  | 2 |
| `the_coven` | Variable |  | 2 |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 |
| [`AddPostProcessEffect`](#addpostprocesseffect) | Block |  | 1 |
| [`AddTilesetObjects`](#addtilesetobjects) | Block |  | 1 |
| [`AllyInfested`](#allyinfested) | Block |  | 1 |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Applies or references the 'AlternateIdleAnimation' effect/state. | 1 |
| [`ApplyStatusesNextTurnBegin`](#applystatusesnextturnbegin) | Block | Delays the application of the nested status effects until the start of the target's next turn. | 1 |
| [`ApplyToOthersWithSharedTagAndFaction`](#applytootherswithsharedtagandfaction) | Block | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 1 |
| [`ApplyToRandomClosestAlly`](#applytorandomclosestally) | Block | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 1 |
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum | Applies or references the 'CoinTossBounce' effect/state. | 1 |
| [`Conditional_AbilityTargetIsSelf`](#conditional_abilitytargetisself) | Block | Conditional constraint. Nested properties only trigger if this is true. | 1 |
| [`Conditional_ActiveWeather_Any`](#conditional_activeweather_any) | Block | Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 1 |
| [`Conditional_Backstab`](#conditional_backstab) | Block | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 1 |
| [`Conditional_CanBeHealed`](#conditional_canbehealed) | Block | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 1 |
| [`Conditional_DebuffRoll`](#conditional_debuffroll) | Block | Conditional trigger: Executes nested logic based on a randomized debuff probability. | 1 |
| [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |
| [`Conditional_HasKnockback`](#conditional_hasknockback) | Block | Conditional: Executes logic if the triggering attack deals knockback. | 1 |
| [`Conditional_IsPhysicalAttack`](#conditional_isphysicalattack) | Block |  | 1 |
| [`Conditional_IsTrample`](#conditional_istrample) | Block | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 1 |
| [`Conditional_LivingPlayerCat`](#conditional_livingplayercat) | Block | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 1 |
| [`Conditional_ManaThreshold`](#conditional_manathreshold) | Block |  | 1 |
| [`Conditional_NotBig`](#conditional_notbig) | Block | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 1 |
| [`Conditional_RandomChance`](#conditional_randomchance) | Block |  | 1 |
| [`Conditional_SourceAbilityHasTag`](#conditional_sourceabilityhastag) | Block | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 1 |
| [`Conditional_SourceHasStatus`](#conditional_sourcehasstatus) | Block | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 1 |
| [`Conditional_SourceHasTag`](#conditional_sourcehastag) | Block |  | 1 |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. | 1 |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Applies or references the 'DeathwormUnderground' effect/state. | 1 |
| [`DelayedWindCone`](#delayedwindcone) | Block | Creates a delayed Area of Effect cone. | 1 |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Applies or references the 'DinoLegAnimation' effect/state. | 1 |
| [`DybbukPossessed`](#dybbukpossessed) | Block | Defines the abilities and behaviors available when possessing another entity. | 1 |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Applies or references the 'EnterMount' effect/state. | 1 |
| [`ForceImmediateMoveAndAttack`](#forceimmediatemoveandattack) | Block | Forces the character to immediately move to a target and use a specified ability. | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. | 1 |
| [`IncAuxCounterCycle`](#incauxcountercycle) | Block | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 1 |
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | Applies or references the 'KnockOutClone' effect/state. | 1 |
| [`LaunchOffScreen`](./Math_Equations.md) | Equation | Applies or references the 'LaunchOffScreen' effect/state. | 1 |
| [`MergeDamageInstance`](#mergedamageinstance) | Block | Combines damage numbers or visual hit effects. | 1 |
| [`NextBasicAttackCritsThisTurn`](#nextbasicattackcritsthisturn) | Block | Guarantees the next basic attack executed this turn will be a critical hit. | 1 |
| [`NextBattleStatusStacks`](#nextbattlestatusstacks) | Block | Carries over the specified status effects into the next encounter/battle. | 1 |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. | 1 |
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum |  | 1 |
| [`PoolMetronome`](#poolmetronome) | Block | Executes a random ability drawn from a specific pool. | 1 |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Applies or references the 'QueueUseAbility' effect/state. | 1 |
| [`ScrambleLastUsedSpell`](#scramblelastusedspell) | Block | Randomizes or scrambles the properties of the last spell cast. | 1 |
| [`SetAnimationAlts`](#setanimationalts) | Block | Overrides specific animation states with alternative animations. | 1 |
| [`ShowFakeDamage`](#showfakedamage) | Block | Displays a visual damage number without actually modifying health. | 1 |
| [`SolarFlare`](#solarflare) | Block |  | 1 |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Applies or references the 'SoundEventOnHit' effect/state. | 1 |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. | 1 |
| [`SpawnTilePuddleOnBattleStart`](#spawntilepuddleonbattlestart) | Block |  | 1 |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Applies or references the 'SpecialBossMultipartInstakill' effect/state. | 1 |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Applies or references the 'StealEquipment' effect/state. | 1 |
| [`SwapWeapon`](#swapweapon) | Block | Replaces the character's currently equipped weapon with one from a specified pool. | 1 |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Applies or references the 'TagMetronome' effect/state. | 1 |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Applies or references the 'TeamBonusAbility' effect/state. | 1 |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Applies or references the 'TeleportBackAtTurnEnd' effect/state. | 1 |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Applies or references the 'TickDownStatus' effect/state. | 1 |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Applies or references the 'TilesMovedToNeighborHeal' effect/state. | 1 |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Applies or references the 'TransformBasicMove' effect/state. | 1 |
| [`TransformEquipment`](#transformequipment) | Block | Upgrades or transforms a specific equipped item into another. | 1 |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Applies or references the 'TransformNow' effect/state. | 1 |
| [`UseMoveAbilityWithAI`](#usemoveabilitywithai) | Block | Forces the character to execute a movement ability using specific AI weights. | 1 |
| [`VisualCountDownThenApplyStatus`](#visualcountdownthenapplystatus) | Block | Displays a visual countdown above the target before applying the nested effects. | 1 |
| [`WaggleClone`](#waggleclone) | Block | Spawns visual clones or alternative hitbox variants of the projectile. | 1 |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum |  | 1 |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum |  | 1 |
| `AIFavorLowHealth` | Integer | Applies or references the 'AIFavorLowHealth' effect/state. | 1 |
| `AcidRain` | Integer |  | 1 |
| `AddExtraTurnsBeforeRun` | Integer |  | 1 |
| `Adrenaline` | Integer | Applies or references the 'Adrenaline' effect/state. | 1 |
| `AlliesTakeExtraTurn` | Integer | Applies or references the 'AlliesTakeExtraTurn' effect/state. | 1 |
| `AntlerSwipe2` | Variable |  | 1 |
| `AntlerSwipe` | Variable |  | 1 |
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. | 1 |
| `BasicDashAttackMove_NoKnockback` | Variable |  | 1 |
| `BerserkDash` | Variable |  | 1 |
| `BirthSquirrel` | Variable |  | 1 |
| `BlackHoleSuck` | Integer | Applies or references the 'BlackHoleSuck' effect/state. | 1 |
| `BlankTile` | Variable |  | 1 |
| `Bloodzerked` | Integer | Applies or references the 'Bloodzerked' effect/state. | 1 |
| `BombRatTurtle` | Integer | Applies or references the 'BombRatTurtle' effect/state. | 1 |
| `BonusDamageBasedOnMana` | Integer | Applies or references the 'BonusDamageBasedOnMana' effect/state. | 1 |
| `Boris` | Variable |  | 1 |
| `Boulder` | Variable |  | 1 |
| `BrambleTile` | Variable |  | 1 |
| `ButterflySwarm` | Integer |  | 1 |
| `BypassRockKnockback` | Integer | Applies or references the 'BypassRockKnockback' effect/state. | 1 |
| `CanceledQueuedInput` | Integer | Applies or references the 'CanceledQueuedInput' effect/state. | 1 |
| `CapDamage` | Integer | Applies or references the 'CapDamage' effect/state. | 1 |
| `ChampionUpgradeNextMinion` | Integer | Applies or references the 'ChampionUpgradeNextMinion' effect/state. | 1 |
| `ChaosBossFlipMidTeleport` | Integer | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. | 1 |
| `ChaosBossFormChange` | Integer | Applies or references the 'ChaosBossFormChange' effect/state. | 1 |
| `ChargeFists` | Integer | Applies or references the 'ChargeFists' effect/state. | 1 |
| `CharmTrap` | Variable |  | 1 |
| `CharmedFacingForceAttack` | Integer | Applies or references the 'CharmedFacingForceAttack' effect/state. | 1 |
| `Chitter` | Variable |  | 1 |
| `ClearDefaultDebris` | Integer |  | 1 |
| `ClearFinalBossBattlefield` | Integer | Applies or references the 'ClearFinalBossBattlefield' effect/state. | 1 |
| `CloneWeaponTemp` | Integer | Applies or references the 'CloneWeaponTemp' effect/state. | 1 |
| `CockroachSwarm` | Integer |  | 1 |
| `Conditional_HasCleansableDebuffs` | Variable |  | 1 |
| `CrackMoonHead` | Integer | Applies or references the 'CrackMoonHead' effect/state. | 1 |
| `CurrentWeaponAddElectricElement` | Integer | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. | 1 |
| `DamageWeapon` | Integer | Applies or references the 'DamageWeapon' effect/state. | 1 |
| `DeathWormEat` | Variable |  | 1 |
| `DecoySwapper` | Integer | Applies or references the 'DecoySwapper' effect/state. | 1 |
| `DeleteInanimateObjectsChance` | Integer |  | 1 |
| `DeleteTraps` | Integer | Applies or references the 'DeleteTraps' effect/state. | 1 |
| `DestroyNeckArmor` | Integer | Applies or references the 'DestroyNeckArmor' effect/state. | 1 |
| `DirtTile` | Variable |  | 1 |
| `DisableWeapon` | Integer | Applies or references the 'DisableWeapon' effect/state. | 1 |
| `Disguised` | Variable |  | 1 |
| `DissolveRandomArmorPiece` | Integer | Applies or references the 'DissolveRandomArmorPiece' effect/state. | 1 |
| `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. | 1 |
| `DoubleCastSpellsEachTurn_Status` | Variable |  | 1 |
| `DoubleCast` | Integer | Applies or references the 'DoubleCast' effect/state. | 1 |
| `DrainAllyCatsForFleshGolem` | Integer | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. | 1 |
| `Druid` | Variable |  | 1 |
| `DualSword` | Variable |  | 1 |
| `DuplicateRandomEquippedItem` | Integer | Applies or references the 'DuplicateRandomEquippedItem' effect/state. | 1 |
| `DybbukManualExitTag` | Variable |  | 1 |
| `EggSackTrap` | Variable |  | 1 |
| `EliteUpgradeNextMinion` | Integer | Applies or references the 'EliteUpgradeNextMinion' effect/state. | 1 |
| `EmptyMind` | Integer | Applies or references the 'EmptyMind' effect/state. | 1 |
| `Enlarge` | Integer | Applies or references the 'Enlarge' effect/state. | 1 |
| `EtherSoakedRag` | Variable |  | 1 |
| `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. | 1 |
| `ExistUntilIdleUpkeep` | Integer | Applies or references the 'ExistUntilIdleUpkeep' effect/state. | 1 |
| `ExplodeCharacter_DeathBloom2` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. | 1 |
| `ExplodeCharacter_DeathBloom` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. | 1 |
| `ExplodeCharacter_Party` | Integer | Applies or references the 'ExplodeCharacter_Party' effect/state. | 1 |
| `Explosive` | Variable |  | 1 |
| `FactionDisguiseSource` | Integer | Applies or references the 'FactionDisguiseSource' effect/state. | 1 |
| `FastKnockback` | Integer | Applies or references the 'FastKnockback' effect/state. | 1 |
| `Fighter` | Variable |  | 1 |
| `FinalBossQueueBeam` | Integer | Applies or references the 'FinalBossQueueBeam' effect/state. | 1 |
| `FireArmor2` | Integer | Applies or references the 'FireArmor2' effect/state. | 1 |
| `FireArmor` | Integer | Applies or references the 'FireArmor' effect/state. | 1 |
| `FireflySwarm` | Integer |  | 1 |
| `FlySwarm` | Integer |  | 1 |
| `Fog` | Integer |  | 1 |
| `ForceCollectsPickups` | Integer | Applies or references the 'ForceCollectsPickups' effect/state. | 1 |
| `ForceImmediateMove` | Integer | Applies or references the 'ForceImmediateMove' effect/state. | 1 |
| `ForceMoveAndAttack` | Integer | Applies or references the 'ForceMoveAndAttack' effect/state. | 1 |
| `ForceTransferWeapon` | Integer | Applies or references the 'ForceTransferWeapon' effect/state. | 1 |
| `GainDisorder` | Variable |  | 1 |
| `GenericBuff` | Integer | Applies or references the 'GenericBuff' effect/state. | 1 |
| `GiveBoundItemToTarget` | Integer | Applies or references the 'GiveBoundItemToTarget' effect/state. | 1 |
| `GlassTile` | Variable |  | 1 |
| `GlobalHealthRegenAura` | Integer |  | 1 |
| `Grown` | Variable |  | 1 |
| `HalfDead` | Variable |  | 1 |
| `HardenSkin2` | Variable |  | 1 |
| `HardenSkin` | Variable |  | 1 |
| `HeadTumor` | Variable |  | 1 |
| `HealPercentMaxHP` | Integer | Applies or references the 'HealPercentMaxHP' effect/state. | 1 |
| `HealTo` | Integer | Applies or references the 'HealTo' effect/state. | 1 |
| `HeatWave` | Integer |  | 1 |
| `HeavyHits` | Integer | Applies or references the 'HeavyHits' effect/state. | 1 |
| `IceArmor` | Integer | Applies or references the 'IceArmor' effect/state. | 1 |
| `IgnoreDebuffs` | Integer | Applies or references the 'IgnoreDebuffs' effect/state. | 1 |
| `IncreaseCumulativeBlastDamage` | Integer | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. | 1 |
| `IncreaseItemAuxOnKill` | Integer | Applies or references the 'IncreaseItemAuxOnKill' effect/state. | 1 |
| `Infested` | Variable |  | 1 |
| `InterchangeMoveActPoints` | Integer | Applies or references the 'InterchangeMoveActPoints' effect/state. | 1 |
| `Invulnerable` | Integer | Applies or references the 'Invulnerable' effect/state. | 1 |
| `JesterMinusColorless` | Variable |  | 1 |
| `JewelOfDrog` | Variable |  | 1 |
| `JudgementDay` | Integer |  | 1 |
| `LaunchOffScreenInstakill` | Integer | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 1 |
| `LowGravityKnockbackBoost` | Integer |  | 1 |
| `LowGravityRangeBoost` | Integer |  | 1 |
| `MadnessChanceOnTurnBegin` | Integer | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 |
| `MakeWeaponUnbreakable` | Integer | Applies or references the 'MakeWeaponUnbreakable' effect/state. | 1 |
| `ManaStealToHealth` | Integer | Applies or references the 'ManaStealToHealth' effect/state. | 1 |
| `ManglerAttack` | Integer | Applies or references the 'ManglerAttack' effect/state. | 1 |
| `ManglerShuffle` | Boolean | Applies or references the 'ManglerShuffle' effect/state. | 1 |
| `MassAttackThis` | Integer | Applies or references the 'MassAttackThis' effect/state. | 1 |
| `Meaty` | Integer | Applies or references the 'Meaty' effect/state. | 1 |
| `MegaGuppy` | Variable |  | 1 |
| `MeteorShower` | Integer |  | 1 |
| `MimicMetronome` | Integer | Applies or references the 'MimicMetronome' effect/state. | 1 |
| `MockSong2` | Variable |  | 1 |
| `MockSong` | Variable |  | 1 |
| `Monk` | Variable |  | 1 |
| `MonkeyThrow2` | Variable |  | 1 |
| `MonkeyThrow` | Variable |  | 1 |
| `MoonHandDrop` | Variable |  | 1 |
| `MoonHeadFlail` | Variable |  | 1 |
| `MotherTumorDebugForcePass` | Integer | Applies or references the 'MotherTumorDebugForcePass' effect/state. | 1 |
| `Muted` | Integer | Applies or references the 'Muted' effect/state. | 1 |
| `NextAbilityHeals` | Integer | Applies or references the 'NextAbilityHeals' effect/state. | 1 |
| `NextActionLuckUp` | Integer | Applies or references the 'NextActionLuckUp' effect/state. | 1 |
| `NextDamageReduceAndHealAllies` | Integer | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. | 1 |
| `NextTurnDoubleRangedDamage` | Integer | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. | 1 |
| `NoDeathrattle` | Variable |  | 1 |
| `Normal` | Variable |  | 1 |
| `Nuke` | Variable |  | 1 |
| `OverHealToShield` | Integer | Applies or references the 'OverHealToShield' effect/state. | 1 |
| `OverrideChainKnockbackDamage` | Variable |  | 1 |
| `PermanentCharisma` | Variable |  | 1 |
| `PermanentImmobile` | Variable |  | 1 |
| `PermanentLuck` | Variable |  | 1 |
| `PermanentUpgradeRandomActiveOrPassive` | Integer | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. | 1 |
| `Pounce` | Variable |  | 1 |
| `Prance2` | Variable |  | 1 |
| `Prance` | Variable |  | 1 |
| `ProbeCharmed` | Variable |  | 1 |
| `RNGCannonRandomDamage` | Integer | Applies or references the 'RNGCannonRandomDamage' effect/state. | 1 |
| `RandomBonusDamage` | Integer | Applies or references the 'RandomBonusDamage' effect/state. | 1 |
| `RandomKnockbackDirection` | Integer | Applies or references the 'RandomKnockbackDirection' effect/state. | 1 |
| `ReduceManaCostExcludeBrainstorm` | Integer | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. | 1 |
| `ReformMoonHead` | Integer | Applies or references the 'ReformMoonHead' effect/state. | 1 |
| `RefreshItemAbilities` | Integer | Applies or references the 'RefreshItemAbilities' effect/state. | 1 |
| `RefreshNonManaItemAbilities` | Integer | Applies or references the 'RefreshNonManaItemAbilities' effect/state. | 1 |
| `RefreshOncePerFightAbilities` | Integer | Applies or references the 'RefreshOncePerFightAbilities' effect/state. | 1 |
| `Regurge` | Integer | Applies or references the 'Regurge' effect/state. | 1 |
| `RemoveTurnsThisRound` | Integer | Applies or references the 'RemoveTurnsThisRound' effect/state. | 1 |
| `RepairAllCondition` | Integer | Applies or references the 'RepairAllCondition' effect/state. | 1 |
| `RerollEnemy` | Integer | Applies or references the 'RerollEnemy' effect/state. | 1 |
| `ReturnDinoLegs` | Integer | Applies or references the 'ReturnDinoLegs' effect/state. | 1 |
| `Sandstorm` | Integer |  | 1 |
| `Scavenge2` | Variable |  | 1 |
| `Scavenge` | Variable |  | 1 |
| `Scrambled` | Variable |  | 1 |
| `SelfStun` | Integer | Applies or references the 'SelfStun' effect/state. | 1 |
| `ShadowCrit` | Integer | Applies or references the 'ShadowCrit' effect/state. | 1 |
| `ShootHereCommand` | Integer | Applies or references the 'ShootHereCommand' effect/state. | 1 |
| `ShootHereReceiver` | Integer | Applies or references the 'ShootHereReceiver' effect/state. | 1 |
| `ShortCircuit` | Integer | Applies or references the 'ShortCircuit' effect/state. | 1 |
| `SleepParalysis` | Variable |  | 1 |
| `SmallHitExplosion` | Integer | Applies or references the 'SmallHitExplosion' effect/state. | 1 |
| `SmallHoldingCat` | Variable |  | 1 |
| `SmallHolding` | Variable |  | 1 |
| `Small` | Variable |  | 1 |
| `SmellBlood` | Integer | Applies or references the 'SmellBlood' effect/state. | 1 |
| `SpawnWebTrap` | Integer | Applies or references the 'SpawnWebTrap' effect/state. | 1 |
| `SpellShield` | Integer | Applies or references the 'SpellShield' effect/state. | 1 |
| `SpitConsumed` | Integer | Applies or references the 'SpitConsumed' effect/state. | 1 |
| `SplashDamage` | Variable |  | 1 |
| `SquirrelForm` | Variable |  | 1 |
| `StackingSandstorm` | Variable |  | 1 |
| `StanceSwitchToRanged` | Integer | Applies or references the 'StanceSwitchToRanged' effect/state. | 1 |
| `Standing` | Variable |  | 1 |
| `StatBounty` | Integer | Applies or references the 'StatBounty' effect/state. | 1 |
| `StealDemonicGlyph` | Integer | Applies or references the 'StealDemonicGlyph' effect/state. | 1 |
| `StealTurn` | Integer | Applies or references the 'StealTurn' effect/state. | 1 |
| `StealthCritChance` | Integer | Applies or references the 'StealthCritChance' effect/state. | 1 |
| `SwapHighestAndLowestStat` | Variable |  | 1 |
| `Switcheroo` | Integer | Applies or references the 'Switcheroo' effect/state. | 1 |
| `Synthesize2` | Variable |  | 1 |
| `Synthesize` | Variable |  | 1 |
| `T2CopyCatInternal` | Variable |  | 1 |
| `T2CopyCat` | Integer | Applies or references the 'T2CopyCat' effect/state. | 1 |
| `T3HitlerTriggerInitialSpawns` | Integer | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. | 1 |
| `TaintedOffering2` | Variable |  | 1 |
| `TaintedOffering` | Variable |  | 1 |
| `TakeExtraTurnEndOfRound` | Integer | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. | 1 |
| `TallFlowerTile` | Variable |  | 1 |
| `TargetedMetronome` | Integer | Applies or references the 'TargetedMetronome' effect/state. | 1 |
| `Taunting` | Integer | Applies or references the 'Taunting' effect/state. | 1 |
| `Tease2` | Variable |  | 1 |
| `Tease` | Variable |  | 1 |
| `TempBackstabBleed` | Integer | Applies or references the 'TempBackstabBleed' effect/state. | 1 |
| `TempBackstabPiercing` | Integer | Applies or references the 'TempBackstabPiercing' effect/state. | 1 |
| `TempBackstabPoison` | Integer | Applies or references the 'TempBackstabPoison' effect/state. | 1 |
| `TempBackstab` | Integer | Applies or references the 'TempBackstab' effect/state. | 1 |
| `TempBasicAttackBonusAOE` | Integer | Applies or references the 'TempBasicAttackBonusAOE' effect/state. | 1 |
| `TempBonusKnockbackDamage` | Integer | Applies or references the 'TempBonusKnockbackDamage' effect/state. | 1 |
| `TempBonusKnockback` | Integer | Applies or references the 'TempBonusKnockback' effect/state. | 1 |
| `TempInjuryImmunity` | Integer | Applies or references the 'TempInjuryImmunity' effect/state. | 1 |
| `TempLuckUp` | Integer | Applies or references the 'TempLuckUp' effect/state. | 1 |
| `TempManaCostReduction` | Integer | Applies or references the 'TempManaCostReduction' effect/state. | 1 |
| `TempPenetrate` | Integer | Applies or references the 'TempPenetrate' effect/state. | 1 |
| `TempPreEmptiveCounterAttack` | Integer | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. | 1 |
| `TheDestroyer` | Variable |  | 1 |
| `TigerSwipes2` | Variable |  | 1 |
| `TigerSwipes` | Variable |  | 1 |
| `TilesMovedToCritChance` | Integer | Applies or references the 'TilesMovedToCritChance' effect/state. | 1 |
| `TilesMovedToMana` | Integer | Applies or references the 'TilesMovedToMana' effect/state. | 1 |
| `TilesMovedToStrength` | Integer | Applies or references the 'TilesMovedToStrength' effect/state. | 1 |
| `Timber` | Variable |  | 1 |
| `TinaFlailRage` | Variable |  | 1 |
| `TinaFlail` | Variable |  | 1 |
| `TowerDefenseStatus2` | Integer | Applies or references the 'TowerDefenseStatus2' effect/state. | 1 |
| `TowerDefenseStatus` | Integer | Applies or references the 'TowerDefenseStatus' effect/state. | 1 |
| `TransformWeapon` | Variable |  | 1 |
| `Trapper_Status` | Integer | Applies or references the 'Trapper_Status' effect/state. | 1 |
| `TriggerMotherConsume` | Integer | Applies or references the 'TriggerMotherConsume' effect/state. | 1 |
| `TriggerMotherGrow` | Integer | Applies or references the 'TriggerMotherGrow' effect/state. | 1 |
| `TurnAround` | Integer | Applies or references the 'TurnAround' effect/state. | 1 |
| `TurnControlDelay` | Float | Applies or references the 'TurnControlDelay' effect/state. | 1 |
| `TurnRight` | Integer | Applies or references the 'TurnRight' effect/state. | 1 |
| `UndoDamage` | Integer | Applies or references the 'UndoDamage' effect/state. | 1 |
| `UseRandomSpell_Madness` | Integer | Applies the 'UseRandomSpell_Madness' effect. | 1 |
| `VaporizeDice` | Integer | Applies or references the 'VaporizeDice' effect/state. | 1 |
| `WaterTile_Current` | Variable |  | 1 |
| `WeaponAuxMultiplier` | Float | Applies or references the 'WeaponAuxMultiplier' effect/state. | 1 |
| `alien` | Variable |  | 1 |
| `angeljunk` | Variable |  | 1 |
| `berserkIdle` | Variable |  | 1 |
| `bonusbird` | Variable |  | 1 |
| `chapter_corpse_medium` | Variable |  | 1 |
| `cm_RaptorEggSpawn` | Variable |  | 1 |
| `container` | Variable |  | 1 |
| `deferred` | Variable |  | 1 |
| `flip` | Variable |  | 1 |
| `ghost` | Variable |  | 1 |
| `god` | Variable |  | 1 |
| `grown_hitler_clone` | Variable |  | 1 |
| `head_CrownOfHorns` | Variable |  | 1 |
| `hitler_clone_fetus` | Variable |  | 1 |
| `hitler_clone` | Variable |  | 1 |
| `kill_on_consume` | Boolean |  | 1 |
| `rotate_right` | Variable |  | 1 |
| `spear` | Variable |  | 1 |
| `the_nuke_bearer` | Variable |  | 1 |
| `themotherspike` | Variable |  | 1 |
| `weapon_throw` | Variable |  | 1 |

</details>

### Valid Nested Blocks

The following blocks all behave as `{Logic Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 59

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. | 1 |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 3 |
| [`Conditional_Speculative`](#conditional_speculative) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. | 1 |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`odds`](./Math_Equations.md) | Equation | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. (Must be float values) | 8 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. | 6 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](#conditional_inform) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Float | The probability (0.0 to 1.0) of applying the debuff. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Nested conditional. | 3 |
| [`Conditional_PartyMember`](#conditional_partymember) | Block | Nested conditional. | 2 |
| [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 20 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 47

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 46 |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Nested conditional. | 6 |
| [`Conditional_Boss`](#conditional_boss) | Block | Nested conditional. | 4 |
| [`Conditional_InForm`](#conditional_inform) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 5 |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Block | Nested conditional. | 1 |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum |  | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. | 7 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer |  | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. | 2 |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum |  | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](#conditional_isself) | Block | Nested conditional. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Float |  | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 17 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 15 |
| `instant` | Boolean |  | 12 |
| `mount_mode` | Boolean | If true, treats the consumption as riding/mounting instead of eating. | 12 |
| `do_not_pop_corpse` | Boolean |  | 11 |
| `drop_on_death` | Boolean |  | 11 |
| `wet` | Boolean |  | 8 |
| [`extra_statuses`](#extra_statuses) | Block | Additional generic status applications. | 3 |
| `drop_on_self_death` | Boolean |  | 3 |
| `use_placeholder` | Boolean |  | 3 |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum |  | 1 |
| `kill_on_consume` | Boolean |  | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 85

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. | 2 |
| [`Conditional_Displaceable`](#conditional_displaceable) | Block | Nested conditional. | 1 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. | 1 |
| [`Conditional_HasKnockback`](#conditional_hasknockback) | Block | Nested conditional. | 1 |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. | 1 |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. | 1 |
| [`Conditional_Object`](#conditional_object) | Block | Nested conditional. | 1 |
| [`Conditional_Speculative`](#conditional_speculative) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

#### `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2166

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. | 38 |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. | 35 |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. | 25 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. | 14 |
| [`Conditional_Boss`](#conditional_boss) | Block | Nested conditional. | 13 |
| [`Conditional_FormulaIsPositive`](#conditional_formulaispositive) | Block | Nested conditional. | 10 |
| [`Conditional_Speculative`](#conditional_speculative) | Block | Nested conditional. | 10 |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. | 6 |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. | 5 |
| [`Conditional_InForm`](#conditional_inform) | Block | Nested conditional. | 5 |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Nested conditional. | 5 |
| [`Conditional_Object`](#conditional_object) | Block | Nested conditional. | 5 |
| [`Conditional_PlayerCat`](#conditional_playercat) | Block | Nested conditional. | 5 |
| [`Conditional_Familiar`](#conditional_familiar) | Block | Nested conditional. | 4 |
| `LowerAmbientLight` | Number |  | 4 |
| [`Conditional_AffectedByElement`](#conditional_affectedbyelement) | Block | Nested conditional. | 3 |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Block | Nested conditional. | 3 |
| [`Conditional_LastHit`](#conditional_lasthit) | Block | Nested conditional. | 3 |
| [`Conditional_BadRoll`](#conditional_badroll) | Block | Nested conditional. | 2 |
| [`Conditional_BossOrBig`](#conditional_bossorbig) | Block | Nested conditional. | 2 |
| [`Conditional_Buddy`](#conditional_buddy) | Block | Nested conditional. | 2 |
| [`Conditional_DestructibleCorpse`](#conditional_destructiblecorpse) | Block | Nested conditional. | 2 |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. | 2 |
| [`Conditional_IsSelf`](#conditional_isself) | Block | Nested conditional. | 2 |
| [`Conditional_NotAlly`](#conditional_notally) | Block | Nested conditional. | 2 |
| [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Block | Nested conditional. | 2 |
| [`Conditional_NotShielded`](#conditional_notshielded) | Block | Nested conditional. | 2 |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Block | Nested conditional. | 2 |
| [`Conditional_Shielded`](#conditional_shielded) | Block | Nested conditional. | 2 |
| [`Conditional_AbilityTargetIsSelf`](#conditional_abilitytargetisself) | Block | Nested conditional. | 1 |
| [`Conditional_ActiveWeather_Any`](#conditional_activeweather_any) | Block | Nested conditional. | 1 |
| [`Conditional_Backstab`](#conditional_backstab) | Block | Nested conditional. | 1 |
| [`Conditional_CanBeHealed`](#conditional_canbehealed) | Block | Nested conditional. | 1 |
| [`Conditional_DebuffRoll`](#conditional_debuffroll) | Block | Nested conditional. | 1 |
| [`Conditional_Displaceable`](#conditional_displaceable) | Block | Nested conditional. | 1 |
| [`Conditional_HasCleansableDebuffs`](#conditional_hascleansabledebuffs) | Block | Nested conditional. | 1 |
| [`Conditional_IsTrample`](#conditional_istrample) | Block | Nested conditional. | 1 |
| [`Conditional_LivingPlayerCat`](#conditional_livingplayercat) | Block | Nested conditional. | 1 |
| [`Conditional_NotBig`](#conditional_notbig) | Block | Nested conditional. | 1 |
| [`Conditional_RandomChance`](#conditional_randomchance) | Block | Nested conditional. | 1 |
| [`Conditional_SourceAbilityHasTag`](#conditional_sourceabilityhastag) | Block | Nested conditional. | 1 |
| [`Conditional_SourceHasStatus`](#conditional_sourcehasstatus) | Block | Nested conditional. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

