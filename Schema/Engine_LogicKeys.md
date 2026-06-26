# Mewgenics Mod Developer Documentation: Engine: Logic Keys

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

## Engine: Logic Keys

This document is the authoritative reference for Logic Blocks. All of the contexts below can appear as dynamic keys inside an `effects {}` block, or directly inside abilities. Many of these are conditional wrappers that evaluate a condition before executing their nested object, while others redirect execution flow (e.g. `ApplyToSource`).

> **Note:** Because many of these contexts accept arbitrary nested Logic Blocks, any entry marked `{Logic Keys}` recursively refers back to this same document.

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-root), [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`temporary_effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temporary_effects), [`Else` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-else), [`ApplyToSource` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_ally), [`Consumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-consumed), [`Conditional_Boss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_speculative), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`Conditional_Corpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_playercat), [`ApplyToConsumed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytoconsumed), [`TimeDelayStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-post_spawn_statuses), [`Conditional_AffectedByElement` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_lasthit), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`ApplyToTile` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytotile), [`Conditional_BadRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_DestructibleCorpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_destructiblecorpse), [`Conditional_Displaceable` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_displaceable), [`Conditional_IsSelf` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_isself), [`Conditional_OncePerBattle` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_shielded), [`ApplyToRandomClosestAlly` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandomclosestally), [`Conditional_Backstab` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_backstab), [`Conditional_FinishedSpawning` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_finishedspawning), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Conditional_IsTrample` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_istrample), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_NotBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notbig), [`Conditional_RandomChance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_randomchance), [`NextBattleStatusStacks` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-nextbattlestatusstacks), [`ROOT` (Boss_Cutscene_Info)](./Boss_Cutscene_Info.md#context-root), [`ROOT` (Cat_Classes)](./Cat_Classes.md#context-root), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`Conditional_RandomChance` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_randomchance), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_goodroll), [`ROOT` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-root), [`FormChanger` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-formchanger), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`Consumed` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-consumed), [`Conditional_GoodRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_goodroll), [`Conditional_BadRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-else), [`FinalBossBecomeTheChild` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbossbecomethechild), [`InfiniteRebirth` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-infiniterebirth), [`TVBotScreen` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-tvbotscreen), [`ROOT` (Custom_Cats)](./Custom_Cats.md#context-root), [`ROOT` (Damage_Text_Styles)](./Damage_Text_Styles.md#context-root), [`ROOT` (Difficulties)](./Difficulties.md#context-root), [`ROOT` (Elite_Buffs)](./Elite_Buffs.md#context-root), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`ROOT` (Enemy_AI)](./Enemy_AI.md#context-root), [`ROOT` (Events_and_Encounters)](./Events_and_Encounters.md#context-root), [`global_effect_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-global_effect_next_fight), [`ROOT` (Furniture_and_Metaprogression)](./Furniture_and_Metaprogression.md#context-root), [`ROOT` (House_and_Environment)](./House_and_Environment.md#context-root), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`Else` (House_and_Environment)](./House_and_Environment.md#context-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundend), [`Conditional_GoodRoll` (House_and_Environment)](./House_and_Environment.md#context-conditional_goodroll), [`Conditional_Corpse` (House_and_Environment)](./House_and_Environment.md#context-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](./House_and_Environment.md#context-conditional_partymember), [`ROOT` (Injuries)](./Injuries.md#context-root), [`ROOT` (Items_and_Equipment)](./Items_and_Equipment.md#context-root), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`Conditional_GoodRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_goodroll), [`ApplyToSource` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytosource), [`Conditional_HasStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else` (Items_and_Equipment)](./Items_and_Equipment.md#context-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`Conditional_PartyMember` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_partymember), [`Conditional_Adjacent` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_onceperbattle), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytorandompartymemberifpossible), [`CastAgainWithStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-castagainwithstatus), [`Conditional_Ally` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_enemy), [`Conditional_HasCleansableDebuffs` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`Conditional_HealthThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_healththreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_shielded), [`CyborgTurns` (Items_and_Equipment)](./Items_and_Equipment.md#context-cyborgturns), [`ScaldingOrbMoonBossOneShot` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot), [`StatusAdjacentOnTheirTurnEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusadjacentontheirturnend), [`StatusOnFallAsleep` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonfallasleep), [`StatusOnTurnEndIfCastNSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifcastnspells), [`ROOT` (Item_Pools)](./Item_Pools.md#context-root), [`ROOT` (Map_Generation_and_Routing)](./Map_Generation_and_Routing.md#context-root), [`ROOT` (Miscellaneous)](./Miscellaneous.md#context-root), [`ROOT` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-root), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects), [`StatusOnStanceSwitch` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonstanceswitch), [`Conditional_Ally` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_enemy), [`Else` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-else), [`StatusOnOverHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonoverhealed), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaexact), [`Conditional_BadRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hasstatus), [`AddStatusToBasicAttackWithCooldown` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicattackwithcooldown), [`AddStatusToMeleeDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustomeleedamage), [`ApplyToSource` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applytosource), [`Conditional_Adjacent` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_shielded), [`EscapeSequence` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-escapesequence), [`InfiniteRebirth` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-infiniterebirth), [`StatusOnDealtDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamage), [`on_throw` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-on_throw), [`Conditional_GoodRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_goodroll), [`StatusAdjacentOnTheirTurnBegin` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin), [`ROOT` (Progression_Unlocks)](./Progression_Unlocks.md#context-root), [`ROOT` (Shops)](./Shops.md#context-root), [`ROOT` (Spawns_and_Enemy_Pools)](./Spawns_and_Enemy_Pools.md#context-root), [`ROOT` (Status_Effect_Keywords)](./Status_Effect_Keywords.md#context-root)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 |  |
| [`FormChange`](./Enums.md#enum-formchange) | Enum / Object | Transforms the character into a different state or form (e.g., Rage, HasCat). | 114 |  |
| [`Else`](#else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 1 |  |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum / Object | Transforms the terrain tile under the target. | 62 |  |
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 50 |  |
| [`ApplyToSource`](#applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 47 |  |
| [`Conditional_HasTag`](#conditionalhastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 42 |  |
| [`Conditional_Enemy`](#conditionalenemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 38 |  |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Applies or references the 'VisualFXTile' effect/state. | 36 |  |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum / Object | Spawns a physics object that visually bounces off the target. | 35 |  |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer | Applies or references the 'Freeze' effect/state. | 29 |  |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer | Applies or references the 'Petrify' effect/state. | 28 |  |
| [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 27 |  |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer | Applies or references the 'ConstitutionUp' effect/state. | 26 |  |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum / Object | Upgrades or transforms an existing ability into a new one from the specified pool. | 26 |  |
| `KnockUpAndAway` | Object | Displaces the target vertically and horizontally away from the source. | 23 |  |
| `IntelligenceUp` | Enum / Integer | Applies or references the 'IntelligenceUp' effect/state. | 21 |  |
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer | Applies or references the 'Sleep' effect/state. | 21 |  |
| [`Conditional_Boss`](#conditionalboss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 17 |  |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 17 |  |
| `Leeches` | Integer / Object | Applies or references the 'Leeches' effect/state. | 2 |  |
| `Cleave` | Integer / Object | Causes the attack to hit adjacent enemies alongside the primary target. | 15 |  |
| `force_contact` | Boolean | If true, enforces physical overlap. | 15 |  |
| `CatPartsTransform` | Object | Transforms specific body parts into different visual variants. | 14 |  |
| [`Conditional_NotBoss`](#conditionalnotboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 14 |  |
| [`Conditional_Speculative`](#conditional_speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 |  |
| `instant` | Boolean | Examples: `true` | 12 |  |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | If true, treats the consumption as riding/mounting instead of eating. | 12 |  |
| `rock` | Variable |  | 46 |  |
| `do_not_pop_corpse` | Boolean | Examples: `true` | 11 |  |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Examples: `false, true, deferred` | 11 |  |
| [`Conditional_FormulaIsPositive`](#conditional_formulaispositive) | Object | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 10 |  |
| `DexterityUp` | Enum / Integer | Applies or references the 'DexterityUp' effect/state. | 10 |  |
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer | Applies or references the 'MagicWeakness' effect/state. | 2 |  |
| `X` | Variable |  | 10 |  |
| `Craft` | Object | Synthesizes or spawns a new item from a specific pool. | 2 |  |
| `OverrideChainKnockback` | Integer | Applies or references the 'OverrideChainKnockback' effect/state. | 9 |  |
| [`Conditional_Corpse`](#conditionalcorpse) | Object | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 8 |  |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 |  |
| `SpreadDisease` | Object | Provides a chance to transmit a disease status to adjacent targets. | 8 |  |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer | Applies or references the 'Tarred' effect/state. | 8 |  |
| `Tech` | Integer | Applies or references the 'Tech' effect/state. | 2 |  |
| `wet` | Boolean | Examples: `false, true` | 8 |  |
| [`Conditional_InForm`](#conditional_inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 7 |  |
| [`Conditional_PlayerCat`](#conditional_playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 7 |  |
| `Drowsy` | Integer | Applies or references the 'Drowsy' effect/state. | 7 |  |
| `ForceAttack` | Integer / Object | Forces the character to execute an immediate attack. | 7 |  |
| [`form`](./Enums.md#enum-form) | Enum / Integer | The specific form ID to check for. | 7 |  |
| `TempDamageUp` | Integer | Applies or references the 'TempDamageUp' effect/state. | 7 |  |
| `TempRangeUp` | Integer | Applies or references the 'TempRangeUp' effect/state. | 7 |  |
| `BackflipWhenTargeted` | Enum / Integer / Object | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 2 |  |
| [`Conditional_HealthThreshold`](#conditionalhealththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 6 |  |
| [`Conditional_Object`](#conditional_object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 |  |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 6 |  |
| [`PopAndSpawn`](./Enums.md#enum-popandspawn) | Enum / Object | Destroys the target and replaces it with a new spawned entity. | 6 |  |
| `RandomInjury` | Integer | Applies or references the 'RandomInjury' effect/state. | 6 |  |
| `SpiderInfested` | Integer | Applies or references the 'SpiderInfested' effect/state. | 6 |  |
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum / Integer | Applies or references the 'TempSpeedUp' effect/state. | 6 |  |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 6 |  |
| [`UseAbility`](./Enums.md#enum-useability) | Enum / Object | Forces the character or target to instantly use a specified ability. | 6 |  |
| [`Conditional_IsSelf`](#conditional_isself) | Object | Conditional trigger: Executes nested logic if the target is the caster themselves. | 5 |  |
| `DestroyEquipmentAndAttachParasite` | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 5 |  |
| `LavaTile` | Variable |  | 5 |  |
| `MovementUp` | Integer | Applies or references the 'MovementUp' effect/state. | 5 |  |
| `Purge` | Integer / Object | Applies or references the 'Purge' effect/state. | 2 |  |
| `SafeDie` | Integer | Applies or references the 'SafeDie' effect/state. | 5 |  |
| `SoulLink` | Integer / Object | Applies or references the 'SoulLink' effect/state. | 2 |  |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer | Applies or references the 'Stealth' effect/state. | 2 |  |
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array / Integer | Applies or references the 'BurgleCoin' effect/state. | 4 |  |
| [`Conditional_Familiar`](#conditional_familiar) | Object | Conditional trigger: Executes nested logic if the target is a familiar. | 4 |  |
| [`Default`](./Enums.md#enum-default) | Enum / Object | `release` | 199 |  |
| `FreeSpell` | Integer | Applies or references the 'FreeSpell' effect/state. | 4 |  |
| `moonhand` | Variable |  | 4 |  |
| `Rain` | Object | Character Form: Behavior and stats for the 'Rain' state. | 1 |  |
| `Reanimate` | Integer / Object | Applies or references the 'Reanimate' effect/state. | 4 |  |
| `RepairAll` | Integer | Applies or references the 'RepairAll' effect/state. | 4 |  |
| `Thrash` | Object |  | 4 |  |
| `Attraction` | Integer | Applies or references the 'Attraction' effect/state. | 3 |  |
| `BlackShard` | Object |  | 8 |  |
| [`Conditional_AffectedByElement`](#conditional_affectedbyelement) | Object | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 3 |  |
| [`Conditional_FirstApplicationThisTurn`](#conditionalfirstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 3 |  |
| [`Conditional_LastHit`](#conditional_lasthit) | Object | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 3 |  |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 3 |  |
| `DoDamage` | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 3 |  |
| `drop_on_self_death` | Boolean | Examples: `true` | 3 |  |
| `ExtraBasicAttacks_Status` | Integer | Applies or references the 'ExtraBasicAttacks_Status' effect/state. | 3 |  |
| `Hex` | Integer | Applies or references the 'Hex' effect/state. | 3 |  |
| `PoisonLace` | Integer / Object / String | Applies or references the 'PoisonLace' effect/state. | 2 |  |
| `poop` | Object | Event Object: Story branch or dialog option representing the \'Poop\' action. | 2 |  |
| `PullSourceToTarget` | Integer | Applies or references the 'PullSourceToTarget' effect/state. | 3 |  |
| `ReviveNextRound` | Integer / Object | Queues the character to be resurrected at the start of the next combat round. | 3 |  |
| `WaterTile` | Variable |  | 3 |  |
| `ZombieCatFamiliar` | Object |  | 4 |  |
| [`ApplyToRandomPartyMemberIfPossible`](#applytorandompartymemberifpossible) | Object | Redirects the nested effects to apply to a random living member of the player's party. | 2 |  |
| `AutoReanimate` | Number | Examples: `50` | 2 |  |
| [`Conditional_BossOrBig`](#conditional_bossorbig) | Object | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 2 |  |
| [`Conditional_Buddy`](#conditional_buddy) | Object | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 2 |  |
| [`Conditional_DestructibleCorpse`](#conditional_destructiblecorpse) | Object | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 2 |  |
| [`Conditional_Displaceable`](#conditional_displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |  |
| [`Conditional_NotAlly`](#conditional_notally) | Object | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 2 |  |
| [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Object | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 2 |  |
| [`Conditional_NotShielded`](#conditional_notshielded) | Object | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 2 |  |
| `FireTile` | Variable |  | 2 |  |
| [`GainDisorderFromPool`](./Enums.md#enum-gaindisorderfrompool) | Enum / Object | Logic: Applies a negative mutation/disorder from a specific pool. | 2 |  |
| `gamewin` | Variable |  | 2 |  |
| `HornCharge` | Object |  | 2 |  |
| `humanoid` | Variable |  | 2 |  |
| `ManaLeeches` | Integer | Applies or references the 'ManaLeeches' effect/state. | 2 |  |
| `megadino` | Variable |  | 1 |  |
| `moonhead` | Variable |  | 1 |  |
| `OffMap` | Object | Character Form: Behavior and stats for the 'OffMap' state. | 2 |  |
| `OilTile` | Variable |  | 2 |  |
| `Ostracized` | Integer | Applies or references the 'Ostracized' effect/state. | 2 |  |
| `PartyExplosion` | Variable |  | 2 |  |
| `PermanentStrength` | Integer | Applies or references the 'PermanentStrength' effect/state. | 2 |  |
| `Pilfer` | Object |  | 2 |  |
| `Possessed` | Integer | Applies or references the 'Possessed' effect/state. | 2 |  |
| `PullSourceToKnockbackImmuneTarget` | Integer | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. | 2 |  |
| `Pulp2` | Object | Character Form: Behavior and stats for the 'Pulp2' state. | 2 |  |
| `RandomPickup` | Object |  | 2 |  |
| `ReduceManaCost` | Integer | Applies or references the 'ReduceManaCost' effect/state. | 2 |  |
| `RepairWeaponCondition` | Integer | Applies or references the 'RepairWeaponCondition' effect/state. | 2 |  |
| `TallGrassTile` | Number | Examples: `80, 15` | 2 |  |
| `TempMovement` | Enum / Integer | Applies or references the 'TempMovement' effect/state. | 2 |  |
| `TempSpellDamageUp` | Integer | Applies or references the 'TempSpellDamageUp' effect/state. | 2 |  |
| `the_coven` | Variable |  | 2 |  |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 |  |
| `ThrowPoop` | Object |  | 2 |  |
| `alien` | Variable |  | 1 |  |
| [`AllyInfested`](#allyinfested) | Object | Examples: `{ ... }` | 1 |  |
| `angeljunk` | Variable |  | 1 |  |
| `AntlerSwipe` | Object |  | 2 |  |
| `AntlerSwipe2` | Object |  | 1 |  |
| `BasicDashAttackMove_NoKnockback` | Object |  | 1 |  |
| `BerserkDash` | Object |  | 2 |  |
| `berserkIdle` | Variable |  | 1 |  |
| `BirthSquirrel` | Object |  | 4 |  |
| `BlankTile` | Number | Examples: `5` | 2 |  |
| `bonusbird` | Variable |  | 1 |  |
| [`Boris`](./Enums.md#enum-boris) | Enum / Object | `MegaGuppy_TransformBoris` | 1 |  |
| `Boulder` | Object |  | 2 |  |
| `BrambleTile` | Variable |  | 1 |  |
| `chapter_corpse_medium` | Variable |  | 1 |  |
| `CharmTrap` | Object |  | 2 |  |
| `Chitter` | Object |  | 1 |  |
| `cm_RaptorEggSpawn` | Object |  | 1 |  |
| [`Conditional_AbilityTargetIsSelf`](#conditional_abilitytargetisself) | Object | Conditional constraint. Nested properties only trigger if this is true. | 1 |  |
| [`Conditional_ActiveWeather_Any`](#conditional_activeweather_any) | Object | Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 1 |  |
| [`Conditional_Backstab`](#conditional_backstab) | Object | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 1 |  |
| [`Conditional_CanBeHealed`](#conditional_canbehealed) | Object | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 1 |  |
| [`Conditional_DebuffRoll`](#conditional_debuffroll) | Object | Conditional trigger: Executes nested logic based on a randomized debuff probability. | 1 |  |
| [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Object | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |  |
| `Conditional_HasCleansableDebuffs` | Object | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 1 |  |
| [`Conditional_HasKnockback`](#conditional_hasknockback) | Object | Conditional: Executes logic if the triggering attack deals knockback. | 1 |  |
| [`Conditional_IsPhysicalAttack`](#conditional_isphysicalattack) | Object | Conditional: Executes logic if the triggering attack is physical. | 1 |  |
| [`Conditional_IsTrample`](#conditional_istrample) | Object | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 1 |  |
| [`Conditional_LivingPlayerCat`](#conditional_livingplayercat) | Object | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 1 |  |
| [`Conditional_NotBig`](#conditional_notbig) | Object | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 1 |  |
| [`Conditional_SourceAbilityHasTag`](#conditional_sourceabilityhastag) | Object | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 1 |  |
| [`Conditional_SourceHasStatus`](#conditional_sourcehasstatus) | Object | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 1 |  |
| `container` | Variable |  | 1 |  |
| `DeathWormEat` | Object |  | 1 |  |
| `deferred` | Boolean | `true` | 1 |  |
| `DirtTile` | Variable |  | 1 |  |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Examples: `MoonHandDrop` | 1 |  |
| [`Druid`](./Arrays.md#array-druid) | Object | Applies or references the 'Druid' effect/state. | 80 |  |
| `DualSword` | Object | Character Form: Behavior and stats for the \'DualSword\' state. | 1 |  |
| [`DybbukPossessed`](#dybbukpossessed) | Object | Defines the abilities and behaviors available when possessing another entity. | 1 |  |
| `EggSackTrap` | Variable |  | 1 |  |
| `EtherSoakedRag` | Object |  | 1 |  |
| [`Explosive`](./Enums.md#enum-explosive) | Enum / Object | `MegaGuppy_TransformExplosive` | 1 |  |
| [`Fighter`](./Arrays.md#array-fighter) | Object | Applies or references the 'Fighter' effect/state. | 80 |  |
| `flip` | Variable |  | 2 |  |
| `GenericBuff` | Integer | Applies or references the 'GenericBuff' effect/state. | 1 |  |
| `ghost` | Variable |  | 1 |  |
| `GlassTile` | Variable |  | 1 |  |
| `god` | Variable |  | 1 |  |
| `Grown` | Object | Character Form: Behavior and stats for the \'Grown\' state. | 1 |  |
| `grown_hitler_clone` | Variable |  | 1 |  |
| `HalfDead` | Object | Character Form: Behavior and stats for the \'HalfDead\' state. | 1 |  |
| `HardenSkin` | Object |  | 2 |  |
| `HardenSkin2` | Object |  | 1 |  |
| `head_CrownOfHorns` | Object |  | 1 |  |
| `HeadTumor` | Object |  | 3 |  |
| `hitler_clone` | Variable |  | 1 |  |
| `hitler_clone_fetus` | Variable |  | 1 |  |
| `Infested` | Integer / Object | data/elite_buffs.gon | 1 |  |
| `JesterMinusColorless` | Variable |  | 1 |  |
| `JewelOfDrog` | Object |  | 1 |  |
| `kill_on_consume` | Boolean | Examples: `true` | 1 |  |
| `MegaGuppy` | Object |  | 1 |  |
| `MockSong` | Object |  | 1 |  |
| `MockSong2` | Object |  | 1 |  |
| [`Monk`](./Arrays.md#array-monk) | Object | Applies or references the 'Monk' effect/state. | 66 |  |
| `MonkeyThrow` | Object |  | 2 |  |
| `MonkeyThrow2` | Object |  | 1 |  |
| `MoonHandDrop` | Object |  | 2 |  |
| `MoonHeadFlail` | Object |  | 1 |  |
| `NoDeathrattle` | Variable |  | 1 |  |
| `Normal` | Integer / Object | Character Form: Behavior and stats for the \'Normal\' state. | 24 |  |
| `Nuke` | Object | Character Form: Behavior and stats for the 'Nuke' state. | 10 |  |
| `OverrideChainKnockbackDamage` | Equation | Applies or references the 'OverrideChainKnockbackDamage' effect/state. | 1 |  |
| `PermanentCharisma` | Integer | Applies or references the 'PermanentCharisma' effect/state. | 1 |  |
| `PermanentLuck` | Integer | Applies or references the 'PermanentLuck' effect/state. | 1 |  |
| `Pounce` | Object |  | 2 |  |
| `Prance` | Object |  | 2 |  |
| `Prance2` | Object |  | 1 |  |
| `ProbeCharmed` | Integer | Applies or references the 'ProbeCharmed' effect/state. | 1 |  |
| `rotate_right` | Variable |  | 1 |  |
| `Scavenge` | Object |  | 2 |  |
| `Scavenge2` | Object |  | 1 |  |
| `Scrambled` | Integer | Applies or references the 'Scrambled' effect/state. | 1 |  |
| `Small` | Object | Character Form: Behavior and stats for the \'Small\' state. | 1 |  |
| `SmallHolding` | Object | Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 |  |
| `SmallHoldingCat` | Object | Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 |  |
| `spear` | Variable |  | 1 |  |
| `SplashDamage` | Integer | Applies or references the 'SplashDamage' effect/state. | 1 |  |
| `SquirrelForm` | Object | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 |  |
| `Standing` | Object | Character Form: Behavior and stats for the 'Standing' state. | 1 |  |
| `Synthesize` | Object |  | 2 |  |
| `Synthesize2` | Object |  | 1 |  |
| `TaintedOffering` | Object |  | 2 |  |
| `TaintedOffering2` | Object |  | 1 |  |
| `TallFlowerTile` | Variable |  | 1 |  |
| `Tease` | Object |  | 2 |  |
| `Tease2` | Object |  | 1 |  |
| `the_nuke_bearer` | Variable |  | 1 |  |
| `TheDestroyer` | Object |  | 2 |  |
| `themotherspike` | Variable |  | 1 |  |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | `item_aux` | 1 |  |
| `TigerSwipes` | Object |  | 2 |  |
| `TigerSwipes2` | Object |  | 1 |  |
| `Timber` | Object |  | 1 |  |
| `TinaFlail` | Object |  | 1 |  |
| `TinaFlailRage` | Object |  | 1 |  |
| `TransformWeapon` | Object | Transforms the equipped weapon into another specific weapon state. | 1 |  |
| `WaterTile_Current` | Variable |  | 4 |  |
| `weapon_throw` | Variable |  | 1 |  |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 |  |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 0 |  |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 0 |  |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 0 |  |
| `UseAbility` | Enum / Object | Forces the character or target to instantly use a specified ability. | 0 |  |
</details>

### Valid Nested Objects

The following objects all behave as `{Logic Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GainDisorderFromPool` | Enum / Object |  |  | `all_disorders` (Enum), `{ ... }` (Object) |

</details>

---

#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 59

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddWeaponAux` | Integer / String |  |  | `-item_aux` (Enum), `2` (Number), `1` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Brace` | Enum / Integer / Object |  | 20 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| `Bruise` | Array / Integer / Object |  | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Cleanse` | Integer / Object |  | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `EquipPermanentItem` | Enum |  |  | `BoneClub` (Enum), `Kidney` (Enum) |
| `EvolveAbilityFromPool` | Enum / Object |  |  | `Necromancer` (Enum), `Thief` (Enum), `{ ... }` (Object) |
| `FindItem` | Enum |  |  | `BoneClub` (Enum), `Pearl` (Enum) |
| `FindItemFromPool` | Enum / Object |  |  | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `ForceUseAbility` | Enum / Object |  |  | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `FormChange` | Enum / Object |  |  | `passive` (Enum), `Default` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `GainCoinsRange` | Object |  |  | `{ ... }` (Object) |
| `HealthGain` | Integer |  |  | `2*X` (Enum), `3*X` (Enum), `3` (Number), `8` (Number) |
| `KineticSpikes` | Integer |  | 6 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer |  |  | `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `MoveQuivered` | Integer |  | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Shield` | Enum / Integer |  | 422 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Tech` | Integer |  | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 0 |  |

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_Ally`](#conditional_ally) | Object | Nested conditional. | 1 |  |
| [`Conditional_PlayerCat`](#conditional_playercat) | Object | Nested conditional. | 1 |  |
| `Bleed` | Array / Integer |  | 9 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `2` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |

</details>

---

#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_Speculative`](#conditional_speculative) | Object | Nested conditional. | 1 |  |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type to check for. | 1 |  |
| `Burn` | Array / Enum / Integer |  | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_Corpse`](#conditional_corpse) | Object | Nested conditional. | 1 |  |
| [`Conditional_PlayerCat`](#conditional_playercat) | Object | Nested conditional. | 1 |  |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer |  | 8 | `[1 .5]` (Array), `6` (Number), `3` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Cleanse` | Integer / Object |  | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer |  |  | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `ManaGain` | Enum / Integer |  |  | `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `RandomStatUp` | Integer / String |  | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `Shield` | Enum / Integer |  | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `Thorns` | Integer |  | 36 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `Fear` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. (Must be float values) | 8 |  |
| `Instakill` | Integer |  |  | `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `Madness` | Array / Enum / Integer / Object |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Object | Nested conditional. | 6 |  |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer |  |  | `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `Immobile` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_InForm`](#conditional_inform) | Object | Nested conditional. | 1 |  |

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_Enemy`](#conditional_enemy) | Object | Nested conditional. | 1 |  |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealRandomInjury` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Madness` | Array / Enum / Integer / Object |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomMutation` | Integer |  |  | `3` (Number), `1` (Number) |
| `Revive` | Integer / Object |  | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| `SafeDoomed` | Enum / Integer |  |  | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of applying the debuff. | 1 |  |

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `LaunchOffScreen` | String |  |  | `10+bonus_melee_ability_damage` (Enum) |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_NotBoss`](#conditional_notboss) | Object | Nested conditional. | 3 |  |
| [`Conditional_PartyMember`](#conditional_partymember) | Object | Nested conditional. | 2 |  |
| [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Object | Nested conditional. | 1 |  |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Attraction` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Burn` | Array / Enum / Integer |  | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Confusion` | Array / Integer / Object |  | 6 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Doomed` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Hex` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Leeches` | Integer / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Madness` | Array / Enum / Integer / Object |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Marked` | Array / Integer / Object |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer |  | 8 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Weakness` | Array / Integer / Object |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `-2` (Number), `5` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `6` (Number), `-2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 |  |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `FillMana` | Integer |  |  | `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `ManaGain` | Enum / Integer |  |  | `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |

</details>

---

#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 |  |
| `Burn` | Array / Enum / Integer |  | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `Shield` | Enum / Integer |  | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Slow` | Array / Enum / Integer / Object |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 |  |
| [`Conditional_Corpse`](#conditional_corpse) | Object | Nested conditional. | 1 |  |
| `ChangeTilesUnder` | Enum |  |  | `LavaTile` (Enum), `DirtTile` (Enum) |
| `FindItemFromPool` | Enum / Object |  |  | `parasites` (Enum), `chapter_specific_item` (Enum), `{ ... }` (Object) |
| `ForceUseAbility` | Enum / Object |  |  | `cm_RaptorEggSpawn` (Enum), `tk_WeirdEgg_Spawn` (Enum), `{ ... }` (Object) |
| `Freeze` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ImmediateUseAbility` | Enum / Object |  |  | `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `RandomMutation` | Integer |  |  | `3` (Number), `1` (Number) |

</details>

---

#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 20 |  |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Burn` | Array / Enum / Integer |  | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Confusion` | Array / Integer / Object |  | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `FormChange` | Enum / Object |  |  | `passive` (Enum), `Bully` (Enum), `{ ... }` (Object) |
| `Quivered` | Array / Integer |  | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `Slow` | Array / Enum / Integer / Object |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 47

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific string tag to check for. | 981 |  |
| [`Conditional_NotBoss`](#conditional_notboss) | Object | Nested conditional. | 6 |  |
| [`Conditional_Boss`](#conditional_boss) | Object | Nested conditional. | 4 |  |
| [`Conditional_InForm`](#conditional_inform) | Object | Nested conditional. | 1 |  |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `ChangeTilesUnder` | Enum |  |  | `LavaTile` (Enum), `DirtTile` (Enum) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `Die` | Integer / Object |  |  | `1` (Number), `6` (Number), `{ ... }` (Object) |
| `EventBounty` | Integer |  |  | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `ImmediateUseAbility` | Enum / Object |  |  | `HitlerCloneHeil` (Enum), `cm_Lard_Impl` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer |  |  | `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `PopAndSpawn` | Enum / Object |  |  | `Sprout` (Enum), `TheDestroyer` (Enum), `{ ... }` (Object) |
| `UseAbility` | Enum / Object |  |  | `MegaGuppy_SummonTheChild` (Enum), `ManglerThrowRemote` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Die` | Integer / Object |  |  | `1` (Number), `6` (Number), `{ ... }` (Object) |
| `FlatLeech` | Integer |  |  | `X` (Enum), `5` (Number), `2` (Number) |
| `Instakill` | Integer |  |  | `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 5 |  |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 |  |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Object | Nested conditional. | 1 |  |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | `item_aux` | 1 |  |

</details>

---

#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`form`](./Enums.md#enum-form) | Enum / Integer | The specific form ID to check for. | 7 |  |
| `CritChanceUp` | Integer |  | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer |  | 2 | `[1 .5]` (Array), `15` (Number), `20` (Number), `{ ... }` (Object) |
| `FormChange` | Enum / Object |  |  | `Drunker` (Enum), `BigHolding` (Enum), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `UseAbility` | Enum / Object |  |  | `MegaGuppy_SummonTheChild` (Enum), `ManglerThrowRemote` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Bruise` | Array / Integer / Object |  | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `RepairTrinket` | Integer |  |  | `1` (Number), `99` (Number) |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 1 |  |

</details>

---

#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `Confusion` | Array / Integer / Object |  | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_Enemy`](#conditional_enemy) | Object | Nested conditional. | 2 |  |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Object | Nested conditional. | 1 |  |
| `Doomed` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `Immobile` | Array / Integer |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `Knockback` | Integer |  |  | `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_HasTag`](#conditional_hastag) | Object | Nested conditional. | 3 |  |
| `RepairWeapon` | Array / Integer |  |  | `[1 .25]` (Array), `6` (Number), `1` (Number) |

</details>

---

#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 |  |
| `ReduceManaCost` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Shield` | Enum / Integer |  | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_IsSelf`](#conditional_isself) | Object | Nested conditional. | 3 |  |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Else`](#else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 1 |  |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer | Applies or references the 'Charmed' effect/state. | 0 |  |
| [`ApplyPassives`](#applypassives) | Object | Grants the nested passive abilities dynamically. | 0 |  |

</details>

---

#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `Charge` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Cleanse` | Integer / Object |  | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `Scrambled` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 4 |  |

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Cleave` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SetItemAux` | Object |  |  | `{ ... }` (Object) |
| `Stun` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 981 |  |
| `ScatterCoins` | Object |  |  | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |  |
| `Bruise` | Array / Integer / Object |  | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 981 |  |
| [`Conditional_Ally`](#conditional_ally) | Object | Nested conditional. | 1 |  |

</details>

---

#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Object | Nested conditional. | 2 |  |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Knockback` | Integer |  |  | `3` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 85

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Object | Nested conditional. | 2 |  |
| [`Conditional_Displaceable`](#conditional_displaceable) | Object | Nested conditional. | 1 |  |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 1 |  |
| [`Conditional_HasKnockback`](#conditional_hasknockback) | Object | Nested conditional. | 1 |  |
| [`Conditional_HasTag`](#conditional_hastag) | Object | Nested conditional. | 1 |  |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Object | Nested conditional. | 1 |  |
| [`Conditional_Object`](#conditional_object) | Object | Nested conditional. | 1 |  |
| [`Conditional_Speculative`](#conditional_speculative) | Object | Nested conditional. | 1 |  |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AllyInfested` | Array / Number / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Bruise` | Array / Integer / Object |  | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Cleanse` | Integer / Object |  | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `Cleave` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Confusion` | Array / Integer / Object |  | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `CritChanceUp` | Integer |  | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer |  | 2 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |
| `DybbukPossessed` | Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `FormChange` | Enum / Object |  |  | `passive` (Enum), `Holy` (Enum), `{ ... }` (Object) |
| `GainCoinsRange` | Object |  |  | `{ ... }` (Object) |
| `ImmediateUseAbility` | Enum / Object |  |  | `MoonHandMegaSqueeze` (Enum), `tk_ButterBean_Normal` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `Instakill` | Integer |  |  | `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `Leeches` | Integer / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Marked` | Array / Integer / Object |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| `ObjectOnHitCharacter` | Enum / Object |  |  | `Maggot` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `PartialCleanse` | Integer |  |  | `1` (Number), `9999` (Number) |
| `PermanentCharm` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer |  | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String |  |  | `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `RandomStatUp` | Integer / String |  | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `Revive` | Integer / Object |  | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| `ScatterCoins` | Object |  |  | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |
| `Slow` | Array / Enum / Integer / Object |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `Webbed` | Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2166

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | | |
| [`Conditional_HasTag`](#conditional_hastag) | Object | Nested conditional. | 38 |  |
| [`Conditional_Enemy`](#conditional_enemy) | Object | Nested conditional. | 35 |  |
| [`Conditional_Ally`](#conditional_ally) | Object | Nested conditional. | 25 |  |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 14 |  |
| [`Conditional_Boss`](#conditional_boss) | Object | Nested conditional. | 13 |  |
| [`Conditional_FormulaIsPositive`](#conditional_formulaispositive) | Object | Nested conditional. | 10 |  |
| [`Conditional_Speculative`](#conditional_speculative) | Object | Nested conditional. | 10 |  |
| [`Conditional_Corpse`](#conditional_corpse) | Object | Nested conditional. | 6 |  |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Object | Nested conditional. | 5 |  |
| [`Conditional_InForm`](#conditional_inform) | Object | Nested conditional. | 5 |  |
| [`Conditional_NotBoss`](#conditional_notboss) | Object | Nested conditional. | 5 |  |
| [`Conditional_Object`](#conditional_object) | Object | Nested conditional. | 5 |  |
| [`Conditional_PlayerCat`](#conditional_playercat) | Object | Nested conditional. | 5 |  |
| [`Conditional_Familiar`](#conditional_familiar) | Object | Nested conditional. | 4 |  |
| `AlphaCat` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Attraction` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BackflipWhenTargeted` | Enum / Integer / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer |  | 9 | `[1 .1]` (Array), `[3 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer |  | 6 | `[1 .25]` (Array), `[1 .10]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `BounceObject` | Enum / Object |  |  | `CharmedFlea_Champion` (Enum), `CharmedDip` (Enum), `{ ... }` (Object) |
| `Brace` | Enum / Integer / Object |  | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bruise` | Array / Integer / Object |  | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `BurgleCoin` | Array / Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number) |
| `ChangeTile` | Enum / Object |  |  | `FireTile` (Enum), `GrassTile` (Enum), `{ ... }` (Object) |
| `ChangeTilesUnder` | Enum |  |  | `LavaTile` (Enum), `DirtTile` (Enum) |
| `Charge` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer |  |  | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .25]` (Array), `[1 .15]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Cleave` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Confusion` | Array / Integer / Object |  | 6 | `[1 .2]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `CreateGlobalModifiers` | Object |  |  | `{ ... }` (Object) |
| `CritChanceUp` | Integer |  | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `DamageOrHealConditionally` | Integer |  |  | `1` (Number) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `3` (Number), `2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer |  | 2 | `[1 .5]` (Array), `15` (Number), `50` (Number), `{ ... }` (Object) |
| `Doomed` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DrinkWater` | Integer |  | 2 | `1` (Number) |
| `Drowsy` | Integer |  |  | `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `EvolveAbilityFromPool` | Enum / Object |  |  | `Tinkerer` (Enum), `Fighter` (Enum), `{ ... }` (Object) |
| `ExtraBasicAttacks_Status` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ExtraBasicMoves_Status` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer |  |  | `[1 .25]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `FillMana` | Integer |  |  | `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `FindExtraItemFromPoolOnBattleEnd` | Enum |  |  | `combat_reward_easy` (Enum), `pills` (Enum) |
| `ForceAttack` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `ForceMoveAway` | Integer |  |  | `1` (Number), `{ ... }` (Object) |
| `ForceUseAbility` | Enum / Object |  |  | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer |  |  | `[1 .25]` (Array), `[1 .15]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `GainCoinsRange` | Object |  |  | `{ ... }` (Object) |
| `HealRandomInjury` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer |  |  | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `HealthRegenUp` | Integer |  | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Hex` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ImmediateUseAbility` | Enum / Object |  |  | `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Infested` | Integer / Object |  | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Instakill` | Integer |  |  | `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `IntelligenceUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer |  | 6 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Knockback` | Integer |  |  | `3` (Number), `4` (Number), `{ ... }` (Object) |
| `KnockOutCoin` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Leech` | Integer |  | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Leeches` | Integer / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Lifesteal` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_AffectedByElement`](#conditional_affectedbyelement) | Object | Nested conditional. | 3 |  |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Object | Nested conditional. | 3 |  |
| [`Conditional_LastHit`](#conditional_lasthit) | Object | Nested conditional. | 3 |  |
| [`Conditional_BadRoll`](#conditional_badroll) | Object | Nested conditional. | 2 |  |
| [`Conditional_BossOrBig`](#conditional_bossorbig) | Object | Nested conditional. | 2 |  |
| [`Conditional_Buddy`](#conditional_buddy) | Object | Nested conditional. | 2 |  |
| [`Conditional_DestructibleCorpse`](#conditional_destructiblecorpse) | Object | Nested conditional. | 2 |  |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Object | Nested conditional. | 2 |  |
| [`Conditional_IsSelf`](#conditional_isself) | Object | Nested conditional. | 2 |  |
| [`Conditional_NotAlly`](#conditional_notally) | Object | Nested conditional. | 2 |  |
| [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Object | Nested conditional. | 2 |  |
| [`Conditional_NotShielded`](#conditional_notshielded) | Object | Nested conditional. | 2 |  |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Object | Nested conditional. | 2 |  |
| [`Conditional_Shielded`](#conditional_shielded) | Object | Nested conditional. | 2 |  |
| [`Conditional_AbilityTargetIsSelf`](#conditional_abilitytargetisself) | Object | Nested conditional. | 1 |  |
| [`Conditional_ActiveWeather_Any`](#conditional_activeweather_any) | Object | Nested conditional. | 1 |  |
| [`Conditional_Backstab`](#conditional_backstab) | Object | Nested conditional. | 1 |  |
| [`Conditional_CanBeHealed`](#conditional_canbehealed) | Object | Nested conditional. | 1 |  |
| [`Conditional_DebuffRoll`](#conditional_debuffroll) | Object | Nested conditional. | 1 |  |
| [`Conditional_Displaceable`](#conditional_displaceable) | Object | Nested conditional. | 1 |  |
| [`Conditional_HasCleansableDebuffs`](#conditional_hascleansabledebuffs) | Object | Nested conditional. | 1 |  |
| [`Conditional_IsTrample`](#conditional_istrample) | Object | Nested conditional. | 1 |  |
| [`Conditional_LivingPlayerCat`](#conditional_livingplayercat) | Object | Nested conditional. | 1 |  |
| [`Conditional_NotBig`](#conditional_notbig) | Object | Nested conditional. | 1 |  |
| [`Conditional_RandomChance`](#conditional_randomchance) | Object | Nested conditional. | 1 |  |
| [`Conditional_SourceAbilityHasTag`](#conditional_sourceabilityhastag) | Object | Nested conditional. | 1 |  |
| [`Conditional_SourceHasStatus`](#conditional_sourcehasstatus) | Object | Nested conditional. | 1 |  |
| `LuckUp` | Enum / Integer |  |  | `[1 .5]` (Array), `3` (Number), `-4` (Number), `{ ... }` (Object) |
| `MagicWeakness` | Array / Integer |  | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer |  |  | `item_aux` (Enum), `X-1` (Enum), `2` (Number), `6` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `ManaLeeches` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `MovementUp` | Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer |  | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `NonStackingDivineShield` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ObjectOnHitCharacter` | Enum / Object |  |  | `SkeletonCatFamiliar` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `Ostracized` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `OverrideChainKnockbackDamage` | String |  |  | `3+bonus_melee_ability_damage` (Enum), `0` (Number) |
| `PartialCleanse` | Integer |  |  | `1` (Number), `9999` (Number) |
| `PermanentConstitution` | Integer |  |  | `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer |  |  | `1` (Number), `2` (Number) |
| `PermanentIntelligence` | Integer |  |  | `1` (Number), `2` (Number) |
| `PermanentSpeed` | Integer |  |  | `1` (Number), `2` (Number) |
| `Petrify` | Array / Integer |  |  | `[1 .15]` (Array), `[1 .2]` (Array), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer |  | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `5` (Number), `{ ... }` (Object) |
| `PoisonLace` | Integer / Object / String |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PopAndSpawn` | Enum / Object |  |  | `TheDestroyer` (Enum), `StemCat_HalfHealth` (Enum), `{ ... }` (Object) |
| `Possessed` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ProbeCharmed` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Purge` | Integer / Object |  | 2 | `3` (Number), `0` (Number), `{ ... }` (Object) |
| `Rain` | Object |  | 1 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomInjury` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomMagicMissile` | Integer / Object |  |  | `[1 .5]` (Array), `5` (Number), `6` (Number), `{ ... }` (Object) |
| `RandomPermanentStat` | Integer |  |  | `-1` (Number), `-2` (Number) |
| `RandomStatDown` | Array / Integer / String |  |  | `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `RandomStatUp` | Integer / String |  | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `3` (Number), `-3` (Number) |
| `RangeUp` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Reanimate` | Integer / Object |  | 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `ReduceManaCost` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Reflect` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `RepairWeapon` | Array / Integer |  |  | `[1 .25]` (Array), `6` (Number), `1` (Number) |
| `Revive` | Integer / Object |  | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| `ReviveNextRound` | Integer / Object |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Rot` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SetDefaultFace` | Enum |  |  | `insane` (Enum), `happy` (Enum) |
| `SizeScale` | Number |  | 4 | `1.1` (Number), `1.3` (Number), `.6` (String), `.8` (String) |
| `Sleep` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SoulLink` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer |  |  | `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `StatusAllCharactersOnSpawn` | Object |  |  | `{ ... }` (Object) |
| `StatusGroup` | Object |  |  | `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Tangled` | Array / Integer / Object |  |  | `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempCounterAttack` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempDexterityUp` | Enum |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempMovement` | Enum / Integer |  |  | `[1 .5]` (Array), `20` (Number), `1` (Number), `{ ... }` (Object) |
| `TempRangeUp` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpellDamageUp` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempStrengthUp` | Enum |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Thorns` | Integer |  | 36 | `[1 .5]` (Array), `3` (Number), `5` (Number), `{ ... }` (Object) |
| `Trample` | Integer |  | 14 | `[3 X-8]` (Array), `[1 .5]` (Array), `9` (Number), `6` (Number), `{ ... }` (Object) |
| `UseAbility` | Enum / Object |  |  | `MegaGuppy_SummonTheChild` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `Webbed` | Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `Alert`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Alert` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `AllAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 6 | `{ ... }` (Object) |

</details>

### Object: `AllyInfested`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Infested` (Enum) |
| `faction` | Enum |  | 1 | `allies` (Enum) |
| `object` | Array / Enum |  | 1 | `CharmedMaggot` (Enum) |

</details>

### Object: `Angry`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Angry"` (Enum) |

</details>

### Object: `Antidote`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_Antidote` (Enum) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_ANTIDOTE_DESC"` (String) |
| `durability` | Array / Integer |  |  | `2` (Number) |
| `frame` | Integer |  |  | `103` (Number) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_ANTIDOTE_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `consumable_common` (Enum) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `Appeal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_APPEAL_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_APPEAL_DESC"` (String) |

</details>

### Object: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Flying` | Integer |  | 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `YOffset` | Number |  | 4 | `-.18` (String), `.35` (String) |

</details>

### Object: `Attacker`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Attraction`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_ATTRACTION_NAME"` (String) |
| `name_reference_applier` | String |  |  | `"KEYWORD_ATTRACTION_REF"` (String) |
| `tooltip_reference_applier` | String |  |  | `"KEYWORD_ATTRACTION_DESC_REF"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_ATTRACTION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_ATTRACTION_DESC"` (String) |

</details>

### Object: `BagOfSeeds`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `tk_BagOfSeeds` (Enum) |
| `desc` | Enum |  |  | `"ITEM_BAGOFSEEDS_DESC"` (String) |
| `frame` | Integer |  |  | `182` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_BAGOFSEEDS_NAME"` (String) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Druid` (Enum) |

</details>

### Object: `Basement0`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement0` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |

</details>

### Object: `Basement1`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement1` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |

</details>

### Object: `Basement2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement2` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |

</details>

### Object: `Basement3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement3` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |

</details>

### Object: `Basement4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement4` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |

</details>

### Object: `BasementUpgrade`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement0` (Enum) |

</details>

### Object: `BasementUpgrade2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement1` (Enum) |

</details>

### Object: `BasementUpgrade3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade2` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement2` (Enum) |

</details>

### Object: `BasementUpgrade4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade3` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement3` (Enum) |

</details>

### Object: `BasementUpgrade5`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade4` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement4` (Enum) |

</details>

### Object: `Bear`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `BellyFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Belly"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Big`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `Big` (Enum), `"Big"` (Enum) |
| `attack` | Enum |  | 2 | `GameteSpawn` (Enum) |
| `follow_character_tag` | Enum |  | 2 | `zaratana` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `position` | Array |  |  | `[4.5 4.5]` (Array) |

</details>

### Object: `BigCatnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `BigFood`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `FoodBase` (Enum) |

</details>

### Object: `BigHolding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"BigHolding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `BigHoldingCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"BigHoldingCat"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `BigScrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `BiggestFood`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `FoodBase` (Enum) |

</details>

### Object: `BirdFeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_BIRDFEED_DESC"` (String) |
| `frame` | Integer |  |  | `191` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_BIRDFEED_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |

</details>

### Object: `BirdPoopHat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Enum / Integer |  |  | `-1` (Number) |
| `cursed` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ARMOR_BIRDPOOPHAT_DESC"` (String) |
| `frame` | Integer |  |  | `30` (Number) |
| `kind` | Enum |  |  | `head` (Enum) |
| `name` | Enum |  |  | `"ARMOR_BIRDPOOPHAT_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `set` | Array / Enum |  |  | `Fecal` (Enum) |

</details>

### Object: `Bishop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `tk_Bishop` (Enum) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Bishop"` (Enum) |
| `attack` | Enum |  | 2 | `BBXLightning` (Enum) |
| `desc` | Enum |  |  | `"ITEM_BISHOP_DESC"` (String) |
| `durability` | Array / Integer |  |  | `6` (Number) |
| `frame` | Integer |  |  | `201` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CULTISTBISHOP_NAME"` (String), `"ITEM_BISHOP_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CULTISTBISHOP_DESC"` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `2.5` (Number) |

</details>

### Object: `BlackBird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |

</details>

### Object: `BlackHole`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"BlackHole"` (Enum) |
| `name` | Enum |  | 2 | `"OBJECT_BLACKHOLE_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"OBJECT_BLACKHOLE_DESC"` (String) |
| `variant_of` | Enum |  |  | `NeutronStar` (Enum) |

</details>

### Object: `Blessing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `intro` | Object |  |  | `{ ... }` (Object) |
| `main` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `Bomb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ability` | Enum |  |  | `wp_Bomb` (Enum) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `desc` | Enum |  |  | `"ITEM_BOMB_DESC"` (String) |
| `durability` | Array / Integer |  |  | `1` (Number) |
| `frame` | Integer |  |  | `11` (Number) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `weapon` (Enum) |
| `name` | Enum |  |  | `"ITEM_BOMB_NAME"` (String) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Button` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |
| `sound` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `BoneyardUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Boris`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `"2"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `BothObelisksUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Bully`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `BunkerUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Butcher`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate SkullBash Shred Chomp Succ...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_BUTCHER0" "TEAMNAME_ADJECTIVE_BUTCHER1" "TEAMNAME_ADJECTIVE_BUTCHER2" "TEAMNAME_ADJECTIVE_BUTCHER3" "TEAMNAME_ADJECTIVE_BUTCHER4" "TEAMNAME_ADJECTIVE_BUTCHER5" "TEAMNAME_ADJECTIVE_BUTCHER6" "TEAMNAME_ADJECTIVE_BUTCHER7" "TEAMNAME_ADJECTIVE_BUTCHER8" "TEAMNAME_ADJECTIVE_BUTCHER9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicButcherMelee]` (Array) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `desc` | Enum |  |  | `"SETBONUS_BUTCHER_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `innate_items` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[con str lck]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_BUTCHER_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_BUTCHER0" "TEAMNAME_NOUN_BUTCHER1" "TEAMNAME_NOUN_BUTCHER2" "TEAMNAME_NOUN_BUTCHER3" "TEAMNAME_NOUN_BUTCHER4" "TEAMNAME_NOUN_BUTCHER5" "TEAMNAME_NOUN_BUTCHER6" "TEAMNAME_NOUN_BUTCHER7" "TEAMNAME_NOUN_BUTCHER8" "TEAMNAME_NOUN_BUTCHER9"...]` (Array) |
| `passive_pool` | Array |  |  | `[Putrefy NeverFull MainCourse FreshMeat Masochist Glutton Hooked Stompy Barbed GrapplingHook...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[Succ HogRush Chomp BodySlam Vurp Tromp Spoil Grill Sharpen SliceAndDice]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |

</details>

### Object: `Cat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum |  | 2 | `spawnHoldingCat` (Enum) |
| `formchange` | Enum |  | 6 | `SmallHoldingCat` (Enum), `BigHoldingCat` (Enum) |
| `statuses` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Catepillar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Catnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_Catnip` (Enum) |
| `aux` | Integer |  |  | `7` (Number) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_SMALLCATNIPBAGGY_DESC"` (String) |
| `durability` | Array / Integer |  |  | `1` (Number) |
| `frame` | Integer |  |  | `22` (Number) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_SMALLCATNIPBAGGY_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `consumable_common` (Enum) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `CatnipBig`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_Catnip` (Enum) |
| `aux` | Integer |  |  | `12` (Number) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_LARGECATNIPBAGGY_DESC"` (String) |
| `durability` | Array / Integer |  |  | `1` (Number) |
| `frame` | Integer |  |  | `3` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_LARGECATNIPBAGGY_NAME"` (String) |
| `rarity` | Enum |  |  | `consumable_common` (Enum) |

</details>

### Object: `CaveBaby`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"CaveBaby"` (Enum) |
| `attack` | Enum |  | 2 | `CaveBabyMelee` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CAVEBABY_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CAVEBABY_DESC"` (String) |
| `variant_of` | Enum |  |  | `CavePerson` (Enum) |

</details>

### Object: `CaveMan`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"CaveMan"` (Enum) |
| `attack` | Enum |  | 4 | `CaveMan3HitCombo` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CAVEMANMAN_NAME"` (String) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CAVEMANMAN_DESC"` (String) |
| `variant_of` | Enum |  |  | `CavePerson` (Enum) |

</details>

### Object: `CaveManSpear`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"SpearCaveMan"` (Enum) |
| `attack` | Enum |  | 4 | `CaveManThrowSpear` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_SPEARCAVEMAN_NAME"` (String) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_SPEARCAVEMAN_DESC"` (String) |

</details>

### Object: `CaveWoman`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"CaveWoman"` (Enum) |
| `attack` | Enum |  | 2 | `CaveWomanKick` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CAVEMANWOMAN_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CAVEMANWOMAN_DESC"` (String) |
| `variant_of` | Enum |  |  | `CavePerson` (Enum) |

</details>

### Object: `CaveWomanHasCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"CatCaveWoman"` (Enum) |
| `attack` | Enum |  | 2 | `CaveWomanCatSlap` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CAVEMANWOMAN2_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CAVEMANWOMAN2_DESC"` (String) |

</details>

### Object: `CavesUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `CerberubsJumpBlind`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum |  | 2 | `nubs_fakeblind` (Enum) |

</details>

### Object: `CerberubsJumpNormal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum |  | 2 | `default` (Enum) |

</details>

### Object: `ChaosAntennaAttached`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer |  | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Else` | Object |  | 1 | `{ ... }` (Object) |
| `Fear` | Array / Integer |  | 3 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Stealth` | Array / Integer |  | 1 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer |  | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

### Object: `Charging`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `MoonHead_Blow` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Charging"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `CharmedDip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Dip` (Enum) |

</details>

### Object: `CharmedFloater`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Floater` (Enum) |

</details>

### Object: `CharmedPile`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Pile` (Enum) |

</details>

### Object: `Cherub`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |

</details>

### Object: `Chicken`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_Heal` (Enum) |
| `aux` | Integer |  |  | `15` (Number) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_ROTISSERIECHICKEN_DESC"` (String) |
| `durability` | Array / Integer |  |  | `3` (Number) |
| `frame` | Integer |  |  | `59` (Number) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_ROTISSERIECHICKEN_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `consumable_rare` (Enum) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdLarge` (Enum) |

</details>

### Object: `Close`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `CloseConvert`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `MarshmallowConvert` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |

</details>

### Object: `Cockroach`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  |  | `[0 20]` (Array), `[10 20]` (Array) |

</details>

### Object: `Coin`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `Coin10`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |

</details>

### Object: `Coin2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |

</details>

### Object: `Coin3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |

</details>

### Object: `Coin4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |

</details>

### Object: `Colorless`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_pool` | Array |  |  | `[Block Rest Brace Roll SharpenClaws Reach ManaDrain SoothingGlow Ponder Brainstorm...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_COLORLESS0" "TEAMNAME_ADJECTIVE_COLORLESS1" "TEAMNAME_ADJECTIVE_COLORLESS2"]` (Array) |
| `attack_pool` | Array |  |  | `[BasicMelee BasicMelee BasicShortRanged BasicShortLobbed]` (Array) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[str dex con int spd cha lck]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `move_pool` | Array |  |  | `[DefaultMove]` (Array) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_COLORLESS0" "TEAMNAME_NOUN_COLORLESS1" "TEAMNAME_NOUN_COLORLESS2"]` (Array) |
| `passive_pool` | Array |  |  | `[SelfAssured LuckDrain Infested Worms Amped Furious MetalDetector DeathProof Leader Mange...]` (Array) |
| `tutorial_levelup_active_pool` | Array |  |  | `[Block LickHeal Dump]` (Array) |
| `tutorial_levelup_active_pool_2` | Array |  |  | `[GainThorns ButtScoot Burst HireHitman]` (Array) |
| `tutorial_levelup_passive_pool` | Array |  |  | `[Furious PressurePoints LateBloomer ZenkaiBoost]` (Array) |

</details>

### Object: `Comfort`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_COMFORT_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_COMFORT_DESC"` (String) |

</details>

### Object: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer |  |  | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |

</details>

### Object: `Conditional_FinishedSpawning`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Imprison` | Enum |  | 2 | `Fly` (Enum), `BeefyCharmedLeech` (Enum) |

</details>

### Object: `CoreObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `CoreUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `CraterUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit1` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Cultist`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Cultist"` (Enum) |
| `attack` | Enum |  | 2 | `BasicMelee` (Enum) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  | 2 | `"ENEMY_CULTISTLACKEY_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CULTISTLACKEY_DESC"` (String) |

</details>

### Object: `Damaged`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `DashRandomly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `ShamblerDash` (Enum) |
| `decision_weights` | Enum |  | 4 | `blind` (Enum) |

</details>

### Object: `DeadHummingbird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_EatHummingbird` (Enum) |
| `aux` | Integer |  |  | `20` (Number) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_DEADHUMMINGBIRD_DESC"` (String) |
| `durability` | Array / Integer |  |  | `2` (Number) |
| `frame` | Integer |  |  | `245` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_DEADHUMMINGBIRD_NAME"` (String) |
| `rarity` | Enum |  |  | `consumable_very_rare` (Enum) |
| `set` | Array / Enum |  |  | `Feathered` (Enum) |

</details>

### Object: `Default`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 20 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `LennyShove` (Enum) |
| `move` | Enum |  | 2 | `LennyTrampleMove` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `""` (String) |
| `passives` | Object |  | 54 | `{ ... }` (Object) |
| `set_house` | Enum |  | 2 | `House1` (Enum) |
| `turns` | Array / Integer / Object |  | 4 | `{ ... }` (Object) |
| `unlock_room` | Enum |  | 2 | `Floor1_Large` (Enum) |

</details>

### Object: `Default_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Default_Ground`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `DemonicGlyph_Bite`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_BITE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_BITE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Bounce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_BOUNCE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_BOUNCE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Fire`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_FIRE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_FIRE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Movement`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_MOVE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_MOVE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Summon`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_SUMMON_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_SUMMON_DESC"` (String) |

</details>

### Object: `DesireMech`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Die`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `DimensionXUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Dove`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |

</details>

### Object: `Down`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Down"` (Enum) |
| `attack` | Enum |  | 2 | `ButtFart` (Enum) |
| `move` | Enum |  | 2 | `TeleportFlipUp` (Enum) |
| `passives` | Object |  | 6 | `{ ... }` (Object) |

</details>

### Object: `Druid`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[ManaBomb SongOfSpring GrantLife SquirrelSquad SummonSquirrel DruidSwap BattleCry SummonSnake SummonTurtle SummonToad...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_DRUID0" "TEAMNAME_ADJECTIVE_DRUID1" "TEAMNAME_ADJECTIVE_DRUID2" "TEAMNAME_ADJECTIVE_DRUID3" "TEAMNAME_ADJECTIVE_DRUID4" "TEAMNAME_ADJECTIVE_DRUID5" "TEAMNAME_ADJECTIVE_DRUID6" "TEAMNAME_ADJECTIVE_DRUID7" "TEAMNAME_ADJECTIVE_DRUID8" "TEAMNAME_ADJECTIVE_DRUID9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicDruidAbility]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_DRUID_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `innate_passives` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[cha int str]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_DRUID_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_DRUID0" "TEAMNAME_NOUN_DRUID1" "TEAMNAME_NOUN_DRUID2" "TEAMNAME_NOUN_DRUID3" "TEAMNAME_NOUN_DRUID4" "TEAMNAME_NOUN_DRUID5" "TEAMNAME_NOUN_DRUID6" "TEAMNAME_NOUN_DRUID7" "TEAMNAME_NOUN_DRUID8" "TEAMNAME_NOUN_DRUID9"...]` (Array) |
| `passive_pool` | Array |  |  | `[SuperCrow NaturesGuidance PoisonIvy Pathfinder EmptyVessels WildAnimals BarkSkin SoothingSong Teamwork Bouquet...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[SummonSquirrel SummonToad Encourage Protection SongOfSpring BattleCry SafetyDance TigerForm RhinoForm InspirationalSong]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Drunker`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Drunk` (Enum) |

</details>

### Object: `DualSword`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"2"` (Enum) |
| `attack` | Enum |  | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number |  | 2 | `1.5` (Number) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |

</details>

### Object: `DualSword_Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Holy2"` (Enum) |
| `attack` | Enum |  | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number |  | 2 | `1.5` (Number) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |

</details>

### Object: `Dumb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `DybbukPossessed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit_ability` | Enum |  | 2 | `DybbukReturn` (Enum) |
| `name` | Enum |  |  | `"KEYWORD_DYBBUKED_NAME"` (String) |
| `punch_self_ability` | Enum |  | 2 | `Dybbuk_StopHittingYourself` (Enum) |
| `tooltip` | Enum |  |  | `"KEYWORD_DYBBUKED_DESC"` (String) |

</details>

### Object: `Eagle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdLarge` (Enum) |

</details>

### Object: `Earth`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation |  | 4 | `X` (Equation) |

</details>

### Object: `Electric`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .1*X]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

### Object: `Empty`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `""` (String) |

</details>

### Object: `EndOfTimeUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Escape`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `DybbukEscape` (Enum) |
| `move_weights` | Enum |  | 4 | `keep_distance_always_move` (Enum) |

</details>

### Object: `EventBounty`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_EVENTBOUNTY_NAME"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_EVENTBOUNTY_DESC"` (String) |

</details>

### Object: `Evolution`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_EVOLUTION_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_EVOLUTION_DESC"` (String) |

</details>

### Object: `EvolveAbilityFromPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum |  | 26 | `Fighter` (Enum), `Thief` (Enum) |
| `upgraded` | Boolean |  | 26 | `true` (Boolean) |

</details>

### Object: `Explody`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Expl` (Enum) |
| `attack` | Enum |  | 2 | `ToxExplode` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Explosive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `"3"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `FightPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `T3Shoot` (Enum) |
| `move` | Enum |  | 2 | `FloatMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Fighter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[Spin Dash FirePunch IcePunch ThunderPunch FurySwipes SideSlash FighterLeap Uppercut Counter...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_FIGHTER0" "TEAMNAME_ADJECTIVE_FIGHTER1" "TEAMNAME_ADJECTIVE_FIGHTER2" "TEAMNAME_ADJECTIVE_FIGHTER3" "TEAMNAME_ADJECTIVE_FIGHTER4" "TEAMNAME_ADJECTIVE_FIGHTER5" "TEAMNAME_ADJECTIVE_FIGHTER6" "TEAMNAME_ADJECTIVE_FIGHTER7" "TEAMNAME_ADJECTIVE_FIGHTER8" "TEAMNAME_ADJECTIVE_FIGHTER9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicMelee_Fighter]` (Array) |
| `complicated_abilities` | Array |  |  | `[FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooHard Zoomzerk Bloodzerk ExhaustingBlow ChaosRampage...]` (Array) |
| `complicated_passives` | Array |  |  | `[ShoulderCheck DumbMuscle ThickSkull MostValuableCat HitMe]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_FIGHTER_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[str con spd]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_FIGHTER_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_FIGHTER0" "TEAMNAME_NOUN_FIGHTER1" "TEAMNAME_NOUN_FIGHTER2" "TEAMNAME_NOUN_FIGHTER3" "TEAMNAME_NOUN_FIGHTER4" "TEAMNAME_NOUN_FIGHTER5" "TEAMNAME_NOUN_FIGHTER6" "TEAMNAME_NOUN_FIGHTER7" "TEAMNAME_NOUN_FIGHTER8" "TEAMNAME_NOUN_FIGHTER9"...]` (Array) |
| `passive_pool` | Array |  |  | `[BloodLust Avenger Scars FasterWhenHit KillsHeal Vengeful HamsterStyle WeaponMaster ShoulderCheck SkullSmash...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `shield` | Enum / Integer |  |  | `[1 .5]` (Array), `4` (Number) |
| `starter_abilities` | Array |  |  | `[FurySwipes Dash Spin Confront FirePunch SideSlash Exert Berserk Stick Counter]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Fire`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Array / Enum / Integer |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `SpewerLobbed_Lava` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `FireFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Full` (Enum) |
| `attack` | Enum |  | 2 | `SpewerSpit` (Enum) |
| `combo` | Array |  |  | `[FireSmoke FirePlumes FireWaves FireBase FireWhites]` (Array) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Firefly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  |  | `[0 2]` (Array) |

</details>

### Object: `FloatingDebris`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  | 1 | `20` (Number) |

</details>

### Object: `Floor1_Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum |  | 2 | `room1` (Enum) |
| `movieclip` | Array / Enum |  | 2 | `RoomBackgroundLargeF1` (Enum) |
| `reverb_empty` | Object |  | 2 | `{ ... }` (Object) |
| `reverb_full` | Object |  | 2 | `{ ... }` (Object) |
| `width` | Number |  | 2 | `16` (Number) |

</details>

### Object: `Floor1_Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum |  | 2 | `room2` (Enum) |
| `movieclip` | Array / Enum |  | 2 | `RoomBackgroundSmallF1` (Enum) |
| `reverb_empty` | Object |  | 2 | `{ ... }` (Object) |
| `reverb_full` | Object |  | 2 | `{ ... }` (Object) |
| `width` | Number |  | 2 | `16` (Number) |

</details>

### Object: `Floor2_Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `7` (Number) |
| `interstitial_bg_frame` | Enum |  |  | `room3` (Enum) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundLargeF2` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `16` (Number) |

</details>

### Object: `Floor2_Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `7` (Number) |
| `interstitial_bg_frame` | Enum |  |  | `room4` (Enum) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundSmallF2` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `16` (Number) |

</details>

### Object: `Flop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Down"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Flop2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Down"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Flush`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |

</details>

### Object: `FlushBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `FlushHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Host` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `FlushNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Fly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `count` | Array / Integer |  |  | `[0 20]` (Array), `[10 20]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_FLY_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_FLY_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Food`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean |  | 4 | `true` (Boolean) |
| `amount` | Array |  | 4 | `10` (Number) |
| `cost` | Object |  | 4 | `5` (Number) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `FoodBase` (Enum) |
| `weight` | Number |  | 2 | `5` (Number) |

</details>

### Object: `FoodBig`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_Heal` (Enum) |
| `aux` | Integer |  |  | `24` (Number) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_CATFOOD_DESC"` (String) |
| `durability` | Array / Integer |  |  | `1` (Number) |
| `frame` | Integer |  |  | `2` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_CATFOOD_NAME"` (String) |
| `rarity` | Enum |  |  | `consumable_common` (Enum) |

</details>

### Object: `FoodMedium`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_Heal` (Enum) |
| `aux` | Integer |  |  | `12` (Number) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_ASNACK_DESC"` (String) |
| `durability` | Array / Integer |  |  | `1` (Number) |
| `frame` | Integer |  |  | `21` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_ASNACK_NAME"` (String) |
| `rarity` | Enum |  |  | `consumable_common` (Enum) |

</details>

### Object: `FoodMove`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `CaveBabyFoodMove` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close_move_if_possible` (Enum) |

</details>

### Object: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 2 | `false` (Boolean) |

</details>

### Object: `ForceTrample`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `BirthwortTrample` (Enum) |
| `decision_weights` | Enum |  | 2 | `always_cast_careless` (Enum) |

</details>

### Object: `FreeSpell`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_FREESPELL_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_FREESPELL_DESC"` (String) |

</details>

### Object: `Full`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Full"` (Enum) |
| `attack` | Enum |  | 4 | `KirbySpit` (Enum) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `statuses_on_enter_form` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `FutureUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `GenFlag_Boss_Spewer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boss` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `GenFlag_Boss_Stacy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boss` | Object |  | 2 | `{ ... }` (Object) |
| `miniboss_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `GlowingSeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_GLOWINGSEED_DESC"` (String) |
| `frame` | Integer |  |  | `71` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_GLOWINGSEED_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |

</details>

### Object: `GoldenEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_GOLDENEGG_DESC"` (String) |
| `frame` | Integer |  |  | `190` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_GOLDENEGG_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |

</details>

### Object: `Grass`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |

</details>

### Object: `Gravity`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Weakness` | Array / Integer / Object |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `Grown`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Grown` (Enum) |
| `attack` | Enum |  | 2 | `HitlerCloneSwipes` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_HITLERCLONE_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1.5` (Number) |
| `weak_threshold` | Integer |  | 2 | `15` (Number) |

</details>

### Object: `GuaranteedJackpot`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Guarding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Guarding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `HalfDead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"2"` (Enum) |
| `attack` | Enum |  | 2 | `RatKingDash` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `HardPathUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hard_initial` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Harpy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdLarge` (Enum) |

</details>

### Object: `HarpysClaw`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `wp_HarpyClaw` (Enum) |
| `desc` | Enum |  |  | `"ITEM_HARPYSCLAW_DESC"` (String) |
| `frame` | Integer |  |  | `199` (Number) |
| `kind` | Enum |  |  | `weapon` (Enum) |
| `name` | Enum |  |  | `"ITEM_HARPYSCLAW_NAME"` (String) |
| `rarity` | Enum |  |  | `very_rare` (Enum) |

</details>

### Object: `HasCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 10 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 8 | `"Grabbing"` (Enum), `"Cat"` (Enum) |
| `attack` | Enum |  | 10 | `LennyCatSlap` (Enum), `MoonHandSqueeze` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Swallowed"` (Enum) |
| `passives` | Object |  | 8 | `{ ... }` (Object) |

</details>

### Object: `HasDeadCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"CatDead"` (Enum) |
| `attack` | Enum |  | 2 | `LennyCatSlap` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `HasRock`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"rock"` (Enum) |
| `attack` | Enum |  | 2 | `AmoebaRockBash` (Enum) |

</details>

### Object: `Headless`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Headless"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `HealRandomInjury`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `158` (Number) |
| `name` | Enum |  |  | `"KEYWORD_HEALRANDOMINJURY_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_HEALRANDOMINJURY_DESC"` (String) |

</details>

### Object: `Health`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_HEALTH_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_HEALTH_DESC"` (String) |

</details>

### Object: `Hint_CrackedVisuals`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Cracked"` (Enum) |

</details>

### Object: `Hint_CrackedVisuals2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"ChargingCracked"` (Enum) |

</details>

### Object: `Hint_CrackedVisuals3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"SwallowedCracked"` (Enum) |

</details>

### Object: `Holding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Holding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Holy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatLeech` | Integer |  | 4 | `X` (Enum), `10` (Number), `1` (Number) |
| `animation_suffix` | Enum / Integer |  | 4 | `"1"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `House1`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aux_positions` | Object |  | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum |  | 2 | `small` (Enum) |
| `movieclip_bg` | Enum |  | 2 | `HouseBackground1` (Enum) |
| `movieclip_fg` | Enum |  | 2 | `HouseForeground1` (Enum) |
| `room_positions` | Object |  | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String |  | 2 | `.8` (String) |

</details>

### Object: `House2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aux_positions` | Object |  | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum |  | 2 | `large` (Enum) |
| `movieclip_bg` | Enum |  | 2 | `HouseBackground2` (Enum) |
| `movieclip_fg` | Enum |  | 2 | `HouseForeground2` (Enum) |
| `room_positions` | Object |  | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String |  | 2 | `.7` (String) |

</details>

### Object: `House3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aux_positions` | Object |  | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum |  | 2 | `large` (Enum) |
| `movieclip_bg` | Enum |  | 2 | `HouseBackground3` (Enum) |
| `movieclip_fg` | Enum |  | 2 | `HouseForeground3` (Enum) |
| `room_positions` | Object |  | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String |  | 2 | `.6` (String) |

</details>

### Object: `HumanDead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `DH` (Enum) |
| `attack` | Enum |  | 2 | `HCSpin` (Enum) |
| `tooltip` | Enum |  | 2 | `"ENEMY_HUMANCAT2_DESC"` (String) |

</details>

### Object: `HummingBird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |

</details>

### Object: `Hunter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[LineShot SpawnMaggotFriend SpawnPooterFriend Marked HailOfNails ScatterShot BrambleShot BearTrap TwinShot CrossShot...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_HUNTER0" "TEAMNAME_ADJECTIVE_HUNTER1" "TEAMNAME_ADJECTIVE_HUNTER2" "TEAMNAME_ADJECTIVE_HUNTER3" "TEAMNAME_ADJECTIVE_HUNTER4" "TEAMNAME_ADJECTIVE_HUNTER5" "TEAMNAME_ADJECTIVE_HUNTER6" "TEAMNAME_ADJECTIVE_HUNTER7" "TEAMNAME_ADJECTIVE_HUNTER8" "TEAMNAME_ADJECTIVE_HUNTER9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicRanged_Hunter]` (Array) |
| `complicated_abilities` | Array |  |  | `[Extend LastHit StakeOut Diversion ScoutMe CraftArrow BounceShot Vivisect SlopThePigs SpiderInjector...]` (Array) |
| `complicated_passives` | Array |  |  | `[Hazardous Traps CatchProjectiles Host SleepDarts Survivalist]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_HUNTER_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[dex spd int]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_HUNTER_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_HUNTER0" "TEAMNAME_NOUN_HUNTER1" "TEAMNAME_NOUN_HUNTER2" "TEAMNAME_NOUN_HUNTER3" "TEAMNAME_NOUN_HUNTER4" "TEAMNAME_NOUN_HUNTER5" "TEAMNAME_NOUN_HUNTER6" "TEAMNAME_NOUN_HUNTER7" "TEAMNAME_NOUN_HUNTER8" "TEAMNAME_NOUN_HUNTER9"...]` (Array) |
| `passive_pool` | Array |  |  | `[TakeAim HuntersBoon BroodMother TaintedMother Quiver SplitShot Hazardous ThornArrows Traps CatchProjectiles...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[SpawnPooterFriend BrambleShot SpawnBaitTrap BearTrap TerrainWalk NeedleShot ScatterShot Marked FleaShot HeavyShot]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Ice`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Slow` | Array / Enum / Integer / Object |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `IceAgeUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `InitialPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `T3Shoot` (Enum) |
| `move` | Enum |  | 2 | `FloatMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Insane_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Insane"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Insane_Ground`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Insane"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Item`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  | 21 | `15` (Number), `5` (Number) |
| `mandatory` | Boolean |  | 14 | `true` (Boolean) |
| `pool` | Array / Enum |  | 18 | `[TutorialStick]` (Array), `[WaterBottle_Half]` (Array), `treasure_easy` (Enum), `rare` (Enum) |
| `weight` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Jack_Gainaltfurniture`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | String |  | 16 | `NPC_JACK_JACK_GAINALTFURNITURE_4` (String), `NPC_JACK_JACK_GAINALTFURNITURE_2` (String) |
| `lock_controls` | Number |  | 2 | `1` (Number) |
| `set_state` | Enum |  | 8 | `closeup` (Enum), `blocking` (Enum) |
| `unlock_controls` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Jester`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_pool` | Array |  |  | `[SmartMetronome RNGCannon Bump PowerUp]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_JESTER0" "TEAMNAME_ADJECTIVE_JESTER1" "TEAMNAME_ADJECTIVE_JESTER2" "TEAMNAME_ADJECTIVE_JESTER3" "TEAMNAME_ADJECTIVE_JESTER4" "TEAMNAME_ADJECTIVE_JESTER5" "TEAMNAME_ADJECTIVE_JESTER6" "TEAMNAME_ADJECTIVE_JESTER7" "TEAMNAME_ADJECTIVE_JESTER8" "TEAMNAME_ADJECTIVE_JESTER9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicMelee_Fighter BasicRanged_Hunter BasicMagicShortRanged BasicTankMelee BasicStraightShot_Thief BasicMedicMelee BasicButcherMelee BasicPsychicPull BasicNecroRanged]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_JESTER_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[str dex con int spd cha lck]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_JESTER_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_JESTER0" "TEAMNAME_NOUN_JESTER1" "TEAMNAME_NOUN_JESTER2" "TEAMNAME_NOUN_JESTER3" "TEAMNAME_NOUN_JESTER4" "TEAMNAME_NOUN_JESTER5" "TEAMNAME_NOUN_JESTER6" "TEAMNAME_NOUN_JESTER7" "TEAMNAME_NOUN_JESTER8" "TEAMNAME_NOUN_JESTER9"...]` (Array) |
| `passive_pool` | Array |  |  | `[SuperLuck Goofball]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Johnny`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `JohnnyBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `JohnnyHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Host` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `JohnnyNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Joystick`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Joystick"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `JunkyardUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit1` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `JurassicUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `LargeAttic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `built_in_collision` | Array |  |  | `[[ 6 6 6 6 6 6 6 6 6...]` (Array) |
| `extra_bound_planes` | Array |  |  | `[{ p [ 0 0 ] n [ 1 -2...]` (Array) |
| `height` | Integer |  |  | `9` (Number) |
| `id` | Enum |  |  | `Attic` (Enum) |
| `interstitial_bg_frame` | Enum |  |  | `attic` (Enum) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundAttic` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `35` (Number) |

</details>

### Object: `LargeBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `LargeHouse`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `MediumHouse` (Enum) |
| `set_house` | Enum |  | 2 | `House3` (Enum) |

</details>

### Object: `LargeHouse_Floor2Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Floor2_Large` (Enum) |

</details>

### Object: `LargeHouse_Floor2Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Floor2_Small` (Enum) |

</details>

### Object: `LastHit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `lobbed_attack` (Enum) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `LeapClose`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `GKLeap` (Enum) |
| `move_weights` | Enum |  | 2 | `towards_aggro` (Enum) |

</details>

### Object: `Leave`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `leave` (Enum) |

</details>

### Object: `LevelUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  | 3 | `10` (Number) |

</details>

### Object: `Lifted`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Lift"` (Enum) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Lighting`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient` | String |  | 10 | `.6` (String), `.8` (String) |
| `bigrays` | Array |  |  | `[0 0]` (Array), `[1 1]` (Array) |
| `smallray_clip` | Enum |  | 2 | `labligtht` (Enum), `Bunkerlight` (Enum) |
| `smallrays` | Array |  |  | `[0 0]` (Array), `[4 8]` (Array) |

</details>

### Object: `Lit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Lit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `LostSoul`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_LOSTSOUL_DESC"` (String) |
| `frame` | Integer |  |  | `180` (Number) |
| `kind` | Enum |  |  | `neck` (Enum) |
| `name` | Enum |  |  | `"ARMOR_LOSTSOUL_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `very_rare` (Enum) |

</details>

### Object: `Mage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[Surf Bolt Fireball FreezeRay MagicMissile Blast WallOfFire HyperBeam MeteorStorm MegaBlast...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_MAGE0" "TEAMNAME_ADJECTIVE_MAGE1" "TEAMNAME_ADJECTIVE_MAGE2" "TEAMNAME_ADJECTIVE_MAGE3" "TEAMNAME_ADJECTIVE_MAGE4" "TEAMNAME_ADJECTIVE_MAGE5" "TEAMNAME_ADJECTIVE_MAGE6" "TEAMNAME_ADJECTIVE_MAGE7" "TEAMNAME_ADJECTIVE_MAGE8" "TEAMNAME_ADJECTIVE_MAGE9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicMagicShortRanged]` (Array) |
| `complicated_abilities` | Array |  |  | `[DealWithTheDevil ForbiddenFlame ForbiddenFlood ForbiddenFulmination Corrupt FireSurge IceSurge LightningSurge Creshendo Divide...]` (Array) |
| `complicated_passives` | Array |  |  | `[ElementalAttunement LatentEnergy MagicGuru One Two Four Five]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_MAGE_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[int cha dex]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_MAGE_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_MAGE0" "TEAMNAME_NOUN_MAGE1" "TEAMNAME_NOUN_MAGE2" "TEAMNAME_NOUN_MAGE3" "TEAMNAME_NOUN_MAGE4" "TEAMNAME_NOUN_MAGE5" "TEAMNAME_NOUN_MAGE6" "TEAMNAME_NOUN_MAGE7" "TEAMNAME_NOUN_MAGE8"]` (Array) |
| `passive_pool` | Array |  |  | `[Micronaps HolyMantel Shrapnel BurningPaws LightningPaws IcePaws PawMissile Overload ChargeUp Recharged...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[MagicMissile Fireball FreezeRay Warp Surf WindSlash Absorb Bolt Inspire MegaBlast]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `MagicSeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_MAGICSEED_DESC"` (String) |
| `frame` | Integer |  |  | `113` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_MAGICSEED_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |

</details>

### Object: `MeatWorldUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 4 | `{ ... }` (Object) |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `MeatWorldUnlockedFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mw_battle1` | Object |  | 2 | `{ ... }` (Object) |
| `mw_boss` | Object |  | 2 | `{ ... }` (Object) |
| `mw_earlyhome` | Object |  | 2 | `{ ... }` (Object) |
| `mw_event1` | Object |  | 2 | `{ ... }` (Object) |
| `mw_hard1` | Object |  | 2 | `{ ... }` (Object) |
| `mw_home` | Object |  | 2 | `{ ... }` (Object) |
| `mw_quest_event` | Object |  | 2 | `{ ... }` (Object) |
| `mw_treasure` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `MedBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `MedCatnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `MedScrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `Medic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[RangedHeal MeleeHeal Malaise OpenWounds Prayer Convert Cleanse HereticMark Zealot Haste...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_MEDIC0" "TEAMNAME_ADJECTIVE_MEDIC1" "TEAMNAME_ADJECTIVE_MEDIC2" "TEAMNAME_ADJECTIVE_MEDIC3" "TEAMNAME_ADJECTIVE_MEDIC4" "TEAMNAME_ADJECTIVE_MEDIC5" "TEAMNAME_ADJECTIVE_MEDIC6" "TEAMNAME_ADJECTIVE_MEDIC7" "TEAMNAME_ADJECTIVE_MEDIC8" "TEAMNAME_ADJECTIVE_MEDIC9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicMedicMelee]` (Array) |
| `complicated_abilities` | Array |  |  | `[OpenWounds WitchHunt Adoubement DivineProtection ChosenWarrior SwiftSanctify DivineGift HolyWeapon GetDown Rebuke...]` (Array) |
| `complicated_passives` | Array |  |  | `[RangedMedic ThouShaltNotKill BlessingOfHolyFire BlessingOfSpirit]` (Array) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[cha int con]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_MEDIC0" "TEAMNAME_NOUN_MEDIC1" "TEAMNAME_NOUN_MEDIC2" "TEAMNAME_NOUN_MEDIC3" "TEAMNAME_NOUN_MEDIC4" "TEAMNAME_NOUN_MEDIC5" "TEAMNAME_NOUN_MEDIC6" "TEAMNAME_NOUN_MEDIC7" "TEAMNAME_NOUN_MEDIC8" "TEAMNAME_NOUN_MEDIC9"]` (Array) |
| `passive_pool` | Array |  |  | `[HealingAura NaturalHealer Eternal Blessed EvilPatron AngelicInspiration TopOff SharingIsCaring Caretaker MoraleBoost...]` (Array) |
| `starter_abilities` | Array |  |  | `[RangedHeal Rally Prayer FriendOrFoe HolyWeapon Zealot OpenWounds RallyCharge HallowedGround Cleanse]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `MediumHouse`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `Default` (Enum) |
| `set_house` | Enum |  | 2 | `House2` (Enum) |

</details>

### Object: `MediumHouse_SmallRoom`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Floor1_Small` (Enum) |

</details>

### Object: `Monk`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[Propell Hadouken Cartwheel StoneFists Transcend HipToss Bruise Slapback Finisher Reverberate...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_MONK0" "TEAMNAME_ADJECTIVE_MONK1" "TEAMNAME_ADJECTIVE_MONK2" "TEAMNAME_ADJECTIVE_MONK3" "TEAMNAME_ADJECTIVE_MONK4" "TEAMNAME_ADJECTIVE_MONK5" "TEAMNAME_ADJECTIVE_MONK6" "TEAMNAME_ADJECTIVE_MONK7" "TEAMNAME_ADJECTIVE_MONK8" "TEAMNAME_ADJECTIVE_MONK9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicMonkMelee]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_MONK_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `innate_items` | Object |  |  | `{ ... }` (Object) |
| `innate_passives` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[int str lck]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_MONK_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_MONK0" "TEAMNAME_NOUN_MONK1" "TEAMNAME_NOUN_MONK2" "TEAMNAME_NOUN_MONK3" "TEAMNAME_NOUN_MONK4" "TEAMNAME_NOUN_MONK5" "TEAMNAME_NOUN_MONK6" "TEAMNAME_NOUN_MONK7" "TEAMNAME_NOUN_MONK8" "TEAMNAME_NOUN_MONK9"...]` (Array) |
| `passive_pool` | Array |  |  | `[SafeSwitching Mixup Turnabout MonkeyStyle BrickSkin JaggedEdges MindBreaker CobraStyle Tenderize LongArms...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[Propell Pogo ComboThrow ComboPull Bruise Anneal Hadouken ReallyFastRun Finisher UnbridledHits]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `MoonObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `MoonUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Mounted`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Cat"` (Enum) |

</details>

### Object: `MouthFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"MouthFull"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `MoveAway`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 8 | `ExtraMove` (Enum), `MoveTwoCantrip` (Enum) |
| `move_weights` | Enum |  | 8 | `stay_far` (Enum), `keep_distance_always_move` (Enum) |

</details>

### Object: `MoveCenter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `move` (Enum) |
| `move_weights` | Enum |  | 4 | `stay_near_map_center` (Enum) |

</details>

### Object: `MoveClose`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 8 | `move` (Enum) |
| `move_for_ability` | Enum |  | 6 | `Spin_Enemy` (Enum), `attack` (Enum) |
| `move_weights` | Enum |  | 8 | `stay_close_avoid_allies` (Enum), `stay_close_always_move` (Enum) |

</details>

### Object: `MoveForBarrage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `ZaratanaVSBombardment` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_far` (Enum) |

</details>

### Object: `MoveForDash`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `attack` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveForGrass`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `StegoGrassStomp` (Enum) |
| `move_for_ability` | Enum |  | 2 | `StegoEatGrass` (Enum) |
| `move_weights` | Enum |  | 2 | `minimum_move` (Enum) |

</details>

### Object: `MoveForPounce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `attack` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveForSpin`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `PyrophinaVSRun` (Enum) |
| `move_for_ability` | Enum |  | 2 | `PyrophinaVSSpinThrow` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |

</details>

### Object: `MoveForThrow`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `move` (Enum) |
| `move_for_ability` | Enum |  | 4 | `PyrophinaVSCatThrow` (Enum), `PyrophinaSoloCatThrow` (Enum) |
| `move_weights` | Enum |  | 4 | `util_minmove` (Enum) |

</details>

### Object: `MoveOneForPuke`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `AlienBeastMoveOne` (Enum) |
| `move_for_ability` | Enum |  | 2 | `AlienBeastPuke` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveSpaced`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_weights` | Enum |  | 2 | `terminator_keep_distance_always_move` (Enum) |

</details>

### Object: `MoveToHead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `G3RunToHead` (Enum) |
| `move_for_ability` | Enum |  | 2 | `G3GrabHead` (Enum) |
| `move_weights` | Enum |  | 2 | `minimum_move` (Enum) |

</details>

### Object: `MoveTowards`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `attack` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |

</details>

### Object: `Mutant`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Mutant"` (Enum) |
| `attack` | Enum |  | 2 | `BBMutantSwipe` (Enum) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `move_speed_multiplier` | Number |  | 2 | `.5` (String) |
| `name` | Enum |  | 2 | `"ENEMY_CULTISTMUTANT_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CULTISTMUTANT_DESC"` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdMed` (Enum) |

</details>

### Object: `NCGravecrawlFAR`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `NCGravecrawl` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_far` (Enum) |

</details>

### Object: `Necromancer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[MaggotArmy Reanimate Rebirth Pestilence Weakness SoulSuck EvilIncarnate SoulLink WeAreOne BloodRain...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_NECROMANCER0" "TEAMNAME_ADJECTIVE_NECROMANCER1" "TEAMNAME_ADJECTIVE_NECROMANCER2" "TEAMNAME_ADJECTIVE_NECROMANCER3" "TEAMNAME_ADJECTIVE_NECROMANCER4" "TEAMNAME_ADJECTIVE_NECROMANCER5" "TEAMNAME_ADJECTIVE_NECROMANCER6" "TEAMNAME_ADJECTIVE_NECROMANCER7" "TEAMNAME_ADJECTIVE_NECROMANCER8" "TEAMNAME_ADJECTIVE_NECROMANCER9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicNecroRanged]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_NECROMANCER_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[dex cha con]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_NECROMANCER_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_NECROMANCER0" "TEAMNAME_NOUN_NECROMANCER1" "TEAMNAME_NOUN_NECROMANCER2" "TEAMNAME_NOUN_NECROMANCER3" "TEAMNAME_NOUN_NECROMANCER4" "TEAMNAME_NOUN_NECROMANCER5" "TEAMNAME_NOUN_NECROMANCER6" "TEAMNAME_NOUN_NECROMANCER7" "TEAMNAME_NOUN_NECROMANCER8" "TEAMNAME_NOUN_NECROMANCER9"...]` (Array) |
| `passive_pool` | Array |  |  | `[Vampirism OneWithNothing BedBugs WormLord InfiniteRebirth SacrificialLamb DeathIncarnate OffloadPain CambionConception Leechmother...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[SoulLink Reanimate Rebirth CarrionShot Pestilence BloodGeyser MaggotArmy Gravecrawl FullMoon CoffinFlop]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `NeutronStar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `NoEyes`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"0"` (Enum) |

</details>

### Object: `NoStick`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `ManglerJab` (Enum) |

</details>

### Object: `NonCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum |  | 2 | `spawnHolding` (Enum) |
| `formchange` | Enum |  | 6 | `SmallHolding` (Enum), `BigHolding` (Enum) |
| `statuses` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Normal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 10 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Up"` (Enum) |
| `attack` | Enum |  | 4 | `TinaBasicBigMeleeA` (Enum), `SpewerLobbed_Normal` (Enum) |
| `passives` | Object |  | 20 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `NormalFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Full` (Enum) |
| `attack` | Enum |  | 2 | `SpewerSpit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `NotPriming`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Nothing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum |  | 2 | `spawn` (Enum) |

</details>

### Object: `Nuke`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Nuke` (Enum) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `desc` | Enum |  |  | `"ARMOR_NUKE_DESC"` (String) |
| `failable` | Boolean |  |  | `true` (Boolean) |
| `frame` | Integer |  |  | `77` (Number) |
| `hint_destination` | Enum |  |  | `endoftime` (Enum) |
| `indestructible` | Boolean |  |  | `true` (Boolean) |
| `kind` | Enum |  |  | `neck` (Enum) |
| `legacy_quest` | Boolean |  |  | `true` (Boolean) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `name` | Enum |  |  | `"ARMOR_NUKE_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `quest_item` | Boolean |  |  | `true` (Boolean) |
| `rarity` | Enum |  |  | `quest` (Enum) |
| `set` | Array / Enum |  |  | `Radioactive` (Enum) |
| `shield` | Enum / Integer |  |  | `[1 .5]` (Array), `10` (Number) |
| `spd` | Enum / Integer |  |  | `-2` (Number) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Obey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Off`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `Off` (Enum) |

</details>

### Object: `OffMap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 6 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `OffScreen`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `OneAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 6 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 6 | `{ ... }` (Object) |

</details>

### Object: `OneEye`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"1"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Open`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Open` (Enum) |
| `attack` | Enum |  | 2 | `GSOpenAttack` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `OpenCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `OpenCat` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Out`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Parousworm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer |  |  | `-1` (Number) |
| `cursed` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_PAROUSWORM_DESC"` (String) |
| `frame` | Integer |  |  | `271` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_PAROUSWORM_NAME"` (String) |
| `parasite` | Boolean |  |  | `true` (Boolean) |
| `passives` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `ParticleAttractor`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force` | Number |  | 1 | `100` (Number) |
| `force_end` | Number |  | 6 | `200` (Number), `500` (Number) |
| `force_start` | Number |  | 6 | `0` (Number) |
| `towards` | Array |  |  | `[5 0 5]` (Array), `[0 .5 0]` (Array) |

</details>

### Object: `ParticleBouncePlane`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String |  | 74 | `1` (Number), `0` (Number), `.1` (String), `.75` (String) |
| `friction` | Number / String |  | 70 | `5` (Number), `2` (Number), `.1` (String), `.2` (String) |
| `plane` | Enum |  | 32 | `right` (Enum), `back` (Enum) |
| `position` | Number |  | 32 | `10.5` (Number) |
| `rotation_dampening` | Number |  | 1 | `1` (Number) |

</details>

### Object: `ParticleCharacterCollision`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_sphere_offset` | Number |  | 1 | `0` (Number) |
| `inherit_velocity` | String |  | 1 | `.5` (String) |
| `pushforce` | Number |  | 1 | `2` (Number) |

</details>

### Object: `ParticleGlobalForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Array |  | 27 | `3` (Number), `1` (Number), `.1` (String), `.5` (String) |
| `id` | Enum |  | 27 | `Wind` (Enum) |

</details>

### Object: `ParticleLineCollisions`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String |  | 6 | `1` (Number), `.5` (String) |
| `end_on_collision` | Boolean |  | 2 | `true` (Boolean) |
| `friction` | Number |  | 6 | `1` (Number), `0` (Number) |

</details>

### Object: `ParticleRandomForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `begin` | Array |  |  | `[0 -20 0]` (Array), `[0 -10 0]` (Array) |
| `end` | Enum |  |  | `[0 -450 0]` (Array), `[0 [ 40 120 ] 0]` (Array) |

</details>

### Object: `ParticleTornadoForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `axis` | Array |  |  | `[0 -0.5 0]` (Array), `[0 1 0]` (Array) |
| `force` | Number |  | 19 | `8` (Number), `5` (Number) |
| `point` | Array |  |  | `[1 1 1]` (Array), `[0 0 0]` (Array) |

</details>

### Object: `PeaceSymbol`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_PEACESYMBOL_DESC"` (String) |
| `frame` | Integer |  |  | `91` (Number) |
| `keyword_tooltips` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `neck` (Enum) |
| `name` | Enum |  |  | `"ARMOR_PEACESYMBOL_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |
| `set` | Array / Enum |  |  | `[Hippie Twine]` (Array) |

</details>

### Object: `PeaceSymbolFacePaint`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_PEACESYMBOLFACEPAINT_DESC"` (String) |
| `frame` | Integer |  |  | `194` (Number) |
| `kind` | Enum |  |  | `face` (Enum) |
| `name` | Enum |  |  | `"ARMOR_PEACESYMBOLFACEPAINT_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Hippie` (Enum) |

</details>

### Object: `PermanentCharm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Charmed` (Enum) |

</details>

### Object: `Pigeon`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdMed` (Enum) |

</details>

### Object: `PopAndSpawn`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `clone_items` | Boolean |  | 2 | `false` (Boolean) |
| `clone_referenced_catdata` | Boolean |  | 2 | `true` (Boolean) |
| `no_splatter` | Boolean |  | 2 | `false` (Boolean) |
| `object` | Array / Enum |  | 4 | `BoyShade` (Enum), `PlayerCat_ClotClone` (Enum) |

</details>

### Object: `Possessing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Possessing"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `GA_Telekinesis_Big` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `primed` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Priming`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `Psychic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[Telekinesis Suggestion MindControl MegaGrav PsyFlutter MagnetPull MindBlast PsychicChoke SkyShatter Supernova...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_PSYCHIC0" "TEAMNAME_ADJECTIVE_PSYCHIC1" "TEAMNAME_ADJECTIVE_PSYCHIC2" "TEAMNAME_ADJECTIVE_PSYCHIC3" "TEAMNAME_ADJECTIVE_PSYCHIC4" "TEAMNAME_ADJECTIVE_PSYCHIC5" "TEAMNAME_ADJECTIVE_PSYCHIC6" "TEAMNAME_ADJECTIVE_PSYCHIC7" "TEAMNAME_ADJECTIVE_PSYCHIC8" "TEAMNAME_ADJECTIVE_PSYCHIC9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicPsychicPull]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_PSYCHIC_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `innate_passives` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[int cha spd]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_PSYCHIC_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_PSYCHIC0" "TEAMNAME_NOUN_PSYCHIC1" "TEAMNAME_NOUN_PSYCHIC2" "TEAMNAME_NOUN_PSYCHIC3" "TEAMNAME_NOUN_PSYCHIC4" "TEAMNAME_NOUN_PSYCHIC5" "TEAMNAME_NOUN_PSYCHIC6" "TEAMNAME_NOUN_PSYCHIC7" "TEAMNAME_NOUN_PSYCHIC8" "TEAMNAME_NOUN_PSYCHIC9"]` (Array) |
| `passive_pool` | Array |  |  | `[Flying SoulShatter Glow Blink FullPower RealityShatter MentalStorm Wither Flourish PsySmack...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[Ping Telekinesis Suggestion SkyShatter MindMeld Glare MindCrack FlashForward CumulativeBlast IncreaseGravity]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Pulp2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `2` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Pulp3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `3` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Pulp4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `4` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Pulp5`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `5` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Pulp6`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `6` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Pulp7`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `7` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |

</details>

### Object: `Rage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 16 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Rage"` (Enum) |
| `attack` | Enum |  | 2 | `ChubsSpinRage` (Enum) |
| `move_speed_multiplier` | Number |  | 2 | `2` (Number) |
| `partial_animation_suffix` | Enum / Integer |  | 8 | `"Rage"` (Enum) |
| `passives` | Object |  | 12 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 12 | `{ ... }` (Object) |

</details>

### Object: `Rain`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum |  | 1 | `Rain` (Enum) |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `alpha` | String |  |  | `.5` (String) |
| `ambient_sound` | String |  | 1 | `amb_rain.ogg` (String) |
| `chain` | Boolean |  |  | `splash` (Enum) |
| `combo` | Array |  |  | `[RainB RainM RainF]` (Array) |
| `desc` | Enum |  |  | `"WEATHER_RAIN_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `emit_amount` | Number |  |  | `1` (Number) |
| `emit_box` | Array |  |  | `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array |  |  | `[0 -1 0]` (Array) |
| `emit_rate` | Number |  |  | `200` (Number) |
| `emit_spread` | Number |  |  | `0` (Number) |
| `face_moving_direction` | Boolean |  |  | `true` (Boolean) |
| `force` | Array |  |  | `[0 -10 0]` (Array) |
| `hint_persistent_elements` | Array |  |  | `[Water]` (Array) |
| `live_bounds` | Array |  |  | `[-999 999 0 999 -999 999]` (Array) |
| `movieclip` | Array / Enum |  |  | `RainParticle` (Enum) |
| `name` | Enum |  |  | `"WEATHER_RAIN_NAME"` (String) |
| `particle_lifetime` | Number |  |  | `5` (Number) |
| `particles` | Array |  |  | `[Rain]` (Array) |
| `prewarm` | Number |  | 1 | `5` (Number) |
| `projection_matrix` | Enum |  |  | `default` (Enum) |
| `render_mode` | Enum |  |  | `separate` (Enum) |
| `scripts` | Object |  |  | `{ ... }` (Object) |
| `simulation_space` | Enum |  |  | `global` (Enum) |
| `size_start` | String |  |  | `.5` (String) |
| `skybox_frame` | Enum |  | 1 | `day_rain` (Enum) |
| `speed_scale` | String |  |  | `.1` (String) |
| `speed_start` | Number |  |  | `10` (Number) |

</details>

### Object: `RandomArmorPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `RandomBiggerArmorPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `RandomBiggerCatnipPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `RandomBiggerFoodPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `RandomCatnipPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `RandomFoodPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `RaptorEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_RaptorEgg` (Enum) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_RAPTOREGG_DESC"` (String) |
| `durability` | Array / Integer |  |  | `1` (Number) |
| `frame` | Integer |  |  | `263` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_RAPTOREGG_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Raven`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdMed` (Enum) |

</details>

### Object: `RavenFeather`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_RAVENFEATHER_DESC"` (String) |
| `frame` | Integer |  |  | `179` (Number) |
| `kind` | Enum |  |  | `neck` (Enum) |
| `name` | Enum |  |  | `"ARMOR_RAVENFEATHER_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Feathered` (Enum) |

</details>

### Object: `Return`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `return` (Enum) |

</details>

### Object: `ReturnA`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `HangerBotReturn` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |

</details>

### Object: `RunFar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `PyrophinaVSRun` (Enum) |
| `move_weights` | Enum |  | 2 | `run_far` (Enum) |

</details>

### Object: `Scrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"SETBONUS_SCRAP_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_SCRAP_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `shield` | Enum / Integer |  |  | `[1 .5]` (Array), `3` (Number) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |

</details>

### Object: `Seagull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdMed` (Enum) |

</details>

### Object: `SewersUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Shadow`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Thief` (Enum) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `crit_chance` | Number |  | 4 | `.05*X` (String) |
| `desc` | Enum |  |  | `"PASSIVE_STEALTHED_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"PASSIVE_STEALTHED_NAME"` (String) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `teleport` (Enum) |

</details>

### Object: `ShowFakeDamage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer |  | 2 | `999` (Number) |
| `style` | Array |  |  | `[crit]` (Array) |

</details>

### Object: `Sitting`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Chair` (Enum) |
| `attack` | Enum |  | 2 | `DoNothing` (Enum) |
| `move` | Enum |  | 2 | `DoNothing` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `SlotResult_Explode`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |

</details>

### Object: `SlotResult_Jackpot_Coins`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `spawn` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spawn` (Enum) |

</details>

### Object: `SlotResult_Nothing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `self_buff` (Enum) |

</details>

### Object: `SlotResult_RandomPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `spawn` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spawn` (Enum) |

</details>

### Object: `Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `""` (String) |
| `attack` | Enum |  | 2 | `GameteInflate` (Enum) |

</details>

### Object: `SmallAttic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `built_in_collision` | Array |  |  | `[[ 6 6 6 6 6 6 6 6 6...]` (Array) |
| `extra_bound_planes` | Array |  |  | `[{ p [ 0 0 ] n [ 1 -2...]` (Array) |
| `height` | Integer |  | 2 | `5` (Number) |
| `id` | Enum |  | 2 | `Attic` (Enum) |
| `interstitial_bg_frame` | Enum |  | 2 | `attic` (Enum) |
| `movieclip` | Array / Enum |  | 2 | `RoomBackgroundSmallAttic` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  | 2 | `18` (Number) |

</details>

### Object: `SmallBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `SmallHolding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Holding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `SmallHoldingCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"HoldingCat"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `SmallHouse_Attic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `Default` (Enum) |
| `unlock_room` | Enum |  | 2 | `Attic` (Enum) |

</details>

### Object: `Snake`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `SpawningPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `SpearRun`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `CaveManSpearRun` (Enum) |
| `move_for_ability` | Enum |  | 4 | `CaveManPickupSpear` (Enum) |
| `move_weights` | Enum |  | 4 | `util_minmove` (Enum) |

</details>

### Object: `Squirrel`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `SquirrelForm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `attack` | Enum |  | 4 | `BasicMelee` (Enum) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `spawn` | Object |  |  | `{ ... }` (Object) |
| `tags` | Array / Enum |  |  | `[shapeshift summon]` (Array) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spawn` (Enum) |
| `tooltip` | Enum |  | 2 | `ENEMY_DRAVENSQUIRRELFORM_DESC` (String) |

</details>

### Object: `Standing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `BungaSmash` (Enum) |
| `move` | Enum |  | 2 | `DefaultMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Standing2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `BungaSmash` (Enum) |
| `move` | Enum |  | 2 | `BungaJumpMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Start_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Stimulation`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_STIMULATION_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_STIMULATION_DESC"` (String) |

</details>

### Object: `Stop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `SuckMF`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TormentorSuck` (Enum) |
| `decision_weights` | Enum |  | 2 | `careless` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |

</details>

### Object: `SwordAndShield`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `DestroyerAttack` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `SwordAndShield_Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Holy"` (Enum) |
| `attack` | Enum |  | 2 | `DestroyerAttack` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `TF_TargetAllies`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum |  | 2 | `util_target_allies` (Enum) |

</details>

### Object: `TF_TargetEnemies`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum |  | 2 | `util_target_enemies` (Enum) |

</details>

### Object: `TVBotDie`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_DIE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_DIE_DESC"` (String) |

</details>

### Object: `TVBotDumb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_DUMB_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_DUMB_DESC"` (String) |

</details>

### Object: `TVBotObey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_OBEY_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_OBEY_DESC"` (String) |

</details>

### Object: `TVBotStop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_STOP_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_STOP_DESC"` (String) |

</details>

### Object: `Tank`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[HeadButt ThrowShield ChewCud AssBlast Chew BatterUp BackBreaker Suplex Intimidate Toss...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_TANK0" "TEAMNAME_ADJECTIVE_TANK1" "TEAMNAME_ADJECTIVE_TANK2" "TEAMNAME_ADJECTIVE_TANK3" "TEAMNAME_ADJECTIVE_TANK4" "TEAMNAME_ADJECTIVE_TANK5" "TEAMNAME_ADJECTIVE_TANK6" "TEAMNAME_ADJECTIVE_TANK7" "TEAMNAME_ADJECTIVE_TANK8" "TEAMNAME_ADJECTIVE_TANK9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicTankMelee]` (Array) |
| `complicated_abilities` | Array |  |  | `[TankRockSong FlipFlop Lunge PlantFeet IronHead Aftershock Demolish FullForce Thicken Spur]` (Array) |
| `complicated_passives` | Array |  |  | `[Plow ChainKnockback Wrestlemaniac MyLeg SlowAndSteady ShovingMatch]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_TANK_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[con str spd]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_TANK_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_TANK0" "TEAMNAME_NOUN_TANK1" "TEAMNAME_NOUN_TANK2" "TEAMNAME_NOUN_TANK3" "TEAMNAME_NOUN_TANK4" "TEAMNAME_NOUN_TANK5" "TEAMNAME_NOUN_TANK6" "TEAMNAME_NOUN_TANK7" "TEAMNAME_NOUN_TANK8" "TEAMNAME_NOUN_TANK9"...]` (Array) |
| `passive_pool` | Array |  |  | `[Thorns HeavyHanded SlackOff Scabs ThunderThighs Plow PetRocks ToadStyle ChainKnockback ProtectiveAura...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[TankSwap Toss BellyFlop BatterUp Chew ThrowShield DrawAttention BodyGuard Earthquake Spur]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Tar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `SpewerLobbed_Tar` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `TarFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Full` (Enum) |
| `attack` | Enum |  | 2 | `SpewerSpit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `TempDexterityUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DexterityUp` (Enum) |

</details>

### Object: `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer |  | 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `TempSpeedUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `SpeedUp` (Enum) |

</details>

### Object: `TheEndUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Thief`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[MoveAgain Assassinate BoostBackstab PoisonGas PoisonNail WeakeningNail SharpNail CoinToss Shadow TimeWalk...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_THIEF0" "TEAMNAME_ADJECTIVE_THIEF1" "TEAMNAME_ADJECTIVE_THIEF2" "TEAMNAME_ADJECTIVE_THIEF3" "TEAMNAME_ADJECTIVE_THIEF4" "TEAMNAME_ADJECTIVE_THIEF5" "TEAMNAME_ADJECTIVE_THIEF6" "TEAMNAME_ADJECTIVE_THIEF7" "TEAMNAME_ADJECTIVE_THIEF8" "TEAMNAME_ADJECTIVE_THIEF9"...]` (Array) |
| `attack_pool` | Array |  |  | `[BasicStraightShot_Thief]` (Array) |
| `complicated_abilities` | Array |  |  | `[QuickRoll Shadowshift SlingShade ThiefSwap Pierce TripleNails SkinDisguise PoisonDip]` (Array) |
| `complicated_passives` | Array |  |  | `[BountyHunter AfterImage Agile FlipACoin]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_THIEF_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[spd dex lck]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_THIEF_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_THIEF0" "TEAMNAME_NOUN_THIEF1" "TEAMNAME_NOUN_THIEF2" "TEAMNAME_NOUN_THIEF3" "TEAMNAME_NOUN_THIEF4" "TEAMNAME_NOUN_THIEF5" "TEAMNAME_NOUN_THIEF6" "TEAMNAME_NOUN_THIEF7" "TEAMNAME_NOUN_THIEF8" "TEAMNAME_NOUN_THIEF9"...]` (Array) |
| `passive_pool` | Array |  |  | `[Backstabber GoldenClaws Shadow PoisonTips Burgle SwiftKiller DoubleThrow BountyHunter RazorClaws Looter...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[Shadow PoisonNail MoveAgain Backflip Distract Rebound Stalk Assassinate CutPurse SeverArtery]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Throb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Host` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobbingArteryDone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Thunderstorm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum |  | 1 | `Thunderstorm` (Enum) |
| `ambient_sound` | String |  | 1 | `amb_thunderstorm.ogg` (String), `amb_heavyrain.ogg` (String) |
| `combo` | Array |  |  | `[TRainB TRainM TRainF WindDust]` (Array) |
| `desc` | Enum |  |  | `"WEATHER_THUNDERSTORM_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `hint_persistent_elements` | Array |  |  | `[Water Wind]` (Array) |
| `lightning_fx` | Boolean |  | 1 | `true` (Boolean) |
| `name` | Enum |  |  | `"WEATHER_THUNDERSTORM_NAME"` (String) |
| `particles` | Array |  |  | `[Thunderstorm]` (Array) |
| `prewarm` | Number |  | 1 | `5` (Number) |
| `skybox_frame` | Enum |  | 1 | `day_thunderstorm` (Enum) |

</details>

### Object: `TieDyeBandana`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_TIEDYEBANDANA_DESC"` (String) |
| `frame` | Integer |  |  | `209` (Number) |
| `kind` | Enum |  |  | `head` (Enum) |
| `name` | Enum |  |  | `"ARMOR_TIEDYEBANDANA_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Hippie` (Enum) |

</details>

### Object: `Tinkerer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_groups` | Object |  |  | `{ ... }` (Object) |
| `ability_pool` | Array |  |  | `[Research Discharge Repair ShoddyJetpack SpawnDecoy SpringShoes AutoPilot Recycle BuildTurret RocketSkates...]` (Array) |
| `adjectives` | Array |  |  | `["TEAMNAME_ADJECTIVE_TINKERER0" "TEAMNAME_ADJECTIVE_TINKERER1" "TEAMNAME_ADJECTIVE_TINKERER2" "TEAMNAME_ADJECTIVE_TINKERER3" "TEAMNAME_ADJECTIVE_TINKERER4" "TEAMNAME_ADJECTIVE_TINKERER5" "TEAMNAME_ADJECTIVE_TINKERER6" "TEAMNAME_ADJECTIVE_TINKERER7" "TEAMNAME_ADJECTIVE_TINKERER8" "TEAMNAME_ADJECTIVE_TINKERER9"...]` (Array) |
| `attack_pool` | Array |  |  | `[TinkererCraft]` (Array) |
| `desc` | Enum |  |  | `"SETBONUS_TINKERER_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `innate_passives` | Object |  |  | `{ ... }` (Object) |
| `levelup_stats` | Array |  |  | `[dex cha int]` (Array) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"SETBONUS_TINKERER_NAME"` (String) |
| `nouns` | Array |  |  | `["TEAMNAME_NOUN_TINKERER0" "TEAMNAME_NOUN_TINKERER1" "TEAMNAME_NOUN_TINKERER2" "TEAMNAME_NOUN_TINKERER3" "TEAMNAME_NOUN_TINKERER4" "TEAMNAME_NOUN_TINKERER5" "TEAMNAME_NOUN_TINKERER6" "TEAMNAME_NOUN_TINKERER7" "TEAMNAME_NOUN_TINKERER8" "TEAMNAME_NOUN_TINKERER9"...]` (Array) |
| `passive_pool` | Array |  |  | `[VersionTwo WeaponProficiency LivingBattery FuzzyFeet ArmorSpecialist EMP MrMega EscapeSequence ItemProxy LightningRod...]` (Array) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `pieces_required` | Number |  |  | `3` (Number) |
| `starter_abilities` | Array |  |  | `[Research ArmorUp ShoddyJetpack BuildTurret RocketSkates Discharge Craft Catbot Electrolyze InstantBarrier]` (Array) |
| `stat_mods` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Toad`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Transformed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Turkey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_Heal` (Enum) |
| `aux` | Integer |  |  | `15` (Number) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_TURKEY_DESC"` (String) |
| `durability` | Array / Integer |  |  | `7` (Number) |
| `frame` | Integer |  |  | `244` (Number) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_TURKEY_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `consumable_rare` (Enum) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdLarge` (Enum) |

</details>

### Object: `Turtle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |

</details>

### Object: `Turtled`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `Turtle` (Enum) |
| `attack` | Enum |  | 4 | `None` (Enum) |
| `move` | Enum |  | 4 | `None` (Enum) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `TwoAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 6 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 6 | `{ ... }` (Object) |

</details>

### Object: `TwoEyes`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Unflip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TeleportFlipUp` (Enum) |
| `move_for_ability` | Enum |  | 2 | `Spin_Enemy` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close_always_move` (Enum) |

</details>

### Object: `Unlit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Unlit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Unwashed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Unwashed` (Enum) |

</details>

### Object: `Up`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Up"` (Enum) |
| `passives` | Object |  | 6 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"OBJECT_TIREUP_DESC"` (String) |

</details>

### Object: `VolcanoAntennaAttached`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |

</details>

### Object: `WallOfFleshDone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Washed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `Washer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `BasicMelee` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CULTISTWASHER_NAME"` (String) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Cultist"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CULTISTWASHER_DESC"` (String) |

</details>

### Object: `Water`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Water"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |

</details>

### Object: `WeirdEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_WEIRDEGG_DESC"` (String) |
| `frame` | Integer |  |  | `73` (Number) |
| `intro` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `main` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"ITEM_WEIRDEGG_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |
| `set` | Array / Enum |  |  | `Baby` (Enum) |

</details>

### Object: `WereMan`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"WereMan"` (Enum) |
| `attack` | Enum |  | 2 | `WereManFurySwipes` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_WEREMAN_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_WEREMAN_DESC"` (String) |
| `variant_of` | Enum |  |  | `CavePerson` (Enum) |

</details>

### Object: `Wind`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer |  | 4 | `X` (Enum) |

</details>

### Object: `WishBone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `cm_WishBone` (Enum) |
| `consumable` | Boolean |  |  | `true` (Boolean) |
| `desc` | Enum |  |  | `"ITEM_WISHBONE_DESC"` (String) |
| `durability` | Array / Integer |  |  | `1` (Number) |
| `frame` | Integer |  |  | `193` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_WISHBONE_NAME"` (String) |
| `rarity` | Enum |  |  | `consumable_very_rare` (Enum) |
| `set` | Array / Enum |  |  | `Bone` (Enum) |

</details>

### Object: `Zealot`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Zealot"` (Enum) |
| `attack` | Enum |  | 2 | `BBStabby` (Enum) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  | 2 | `"ENEMY_CULTISTZEALOT_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CULTISTZEALOT_DESC"` (String) |

</details>

### Object: `ZealotBomb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"BombZealot"` (Enum) |
| `attack` | Enum |  | 2 | `BBExplode` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_BOMBZEALOT_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_BOMBZEALOT_DESC"` (String) |

</details>
