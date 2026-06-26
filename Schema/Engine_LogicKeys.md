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
| [`Default`](Characters_and_Bosses.md#object-default) | Enum / Object | `release` | 199 ||
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Transforms the character into a different state or form (e.g., Rage, HasCat). | 114 ||
| [`Druid`](#object-druid) | Object | Applies or references the 'Druid' effect/state. | 80 ||
| [`Fighter`](#object-fighter) | Object | Applies or references the 'Fighter' effect/state. | 80 ||
| [`Monk`](#object-monk) | Object | Applies or references the 'Monk' effect/state. | 66 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Transforms the terrain tile under the target. | 62 ||
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 50 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 47 ||
| `rock` | Variable | A reference to a rock object or entity in the game world. | 46 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 42 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 38 ||
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Applies or references the 'VisualFXTile' effect/state. | 36 ||
| [`BounceObject`](Abilities_and_Spells.md#object-bounceobject) | Enum / Object | Spawns a physics object that visually bounces off the target. | 35 ||
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer | Applies or references the 'Freeze' effect/state. | 29 ||
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer | Applies or references the 'Petrify' effect/state. | 28 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 27 ||
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer | Applies or references the 'ConstitutionUp' effect/state. | 26 ||
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Upgrades or transforms an existing ability into a new one from the specified pool. | 26 ||
| [`Normal`](Characters_and_Bosses.md#object-normal) | Integer / Object | Character Form: Behavior and stats for the \'Normal\' state. | 24 ||
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 23 ||
| `IntelligenceUp` | Enum / Integer | Applies or references the 'IntelligenceUp' effect/state. | 21 ||
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer | Applies or references the 'Sleep' effect/state. | 21 ||
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 17 ||
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 17 ||
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | Causes the attack to hit adjacent enemies alongside the primary target. | 15 ||
| `force_contact` | Boolean | If true, enforces physical overlap. | 15 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms specific body parts into different visual variants. | 14 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 14 ||
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 ||
| `instant` | Boolean | Examples: `true` | 12 ||
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | If true, treats the consumption as riding/mounting instead of eating. | 12 ||
| `do_not_pop_corpse` | Boolean | Examples: `true` | 11 ||
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Examples: `false, true, deferred` | 11 ||
| [`Conditional_FormulaIsPositive`](Abilities_and_Spells.md#object-conditional_formulaispositive) | Object | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 10 ||
| `DexterityUp` | Enum / Integer | Applies or references the 'DexterityUp' effect/state. | 10 ||
| `X` | Variable | A variable that can be used in mathematical expressions within the logic system. | 10 ||
| [`Nuke`](Characters_and_Bosses.md#object-nuke) | Object | Character Form: Behavior and stats for the 'Nuke' state. | 10 ||
| `OverrideChainKnockback` | Integer | Applies or references the 'OverrideChainKnockback' effect/state. | 9 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 8 ||
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 ||
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Provides a chance to transmit a disease status to adjacent targets. | 8 ||
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer | Applies or references the 'Tarred' effect/state. | 8 ||
| `wet` | Boolean | Examples: `false, true` | 8 ||
| [`BlackShard`](#object-blackshard) | Object | A loot or collectible object representing a Black Shard. | 8 ||
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 7 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 7 ||
| `Drowsy` | Integer | Applies or references the 'Drowsy' effect/state. | 7 ||
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | Forces the character to execute an immediate attack. | 7 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | The specific form ID to check for. | 7 ||
| `TempDamageUp` | Integer | Applies or references the 'TempDamageUp' effect/state. | 7 ||
| `TempRangeUp` | Integer | Applies or references the 'TempRangeUp' effect/state. | 7 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 6 ||
| [`Conditional_Object`](Abilities_and_Spells.md#object-conditional_object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 ||
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 6 ||
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object | Destroys the target and replaces it with a new spawned entity. | 6 ||
| `RandomInjury` | Integer | Applies or references the 'RandomInjury' effect/state. | 6 ||
| `SpiderInfested` | Integer | Applies or references the 'SpiderInfested' effect/state. | 6 ||
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum / Integer | Applies or references the 'TempSpeedUp' effect/state. | 6 ||
| `threshold_flat` | Integer | A flat numerical health value threshold. | 6 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Forces the character or target to instantly use a specified ability. | 6 ||
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object | Conditional trigger: Executes nested logic if the target is the caster themselves. | 5 ||
| [`DestroyEquipmentAndAttachParasite`](Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 5 ||
| `LavaTile` | Variable | A reference to a tile that is lava on the dungeon floor. | 5 ||
| `MovementUp` | Integer | Applies or references the 'MovementUp' effect/state. | 5 ||
| `SafeDie` | Integer | Applies or references the 'SafeDie' effect/state. | 5 ||
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array / Integer | Applies or references the 'BurgleCoin' effect/state. | 4 ||
| [`Conditional_Familiar`](Abilities_and_Spells.md#object-conditional_familiar) | Object | Conditional trigger: Executes nested logic if the target is a familiar. | 4 ||
| `FreeSpell` | Integer | Applies or references the 'FreeSpell' effect/state. | 4 ||
| `moonhand` | Variable | A reference to the Moon Hand entity or mechanic. | 4 ||
| [`Reanimate`](Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object | Applies or references the 'Reanimate' effect/state. | 4 ||
| `RepairAll` | Integer | Applies or references the 'RepairAll' effect/state. | 4 ||
| [`Thrash`](#object-thrash) | Object | An attack or ability template for a thrashing melee behavior. | 4 ||
| [`ZombieCatFamiliar`](#object-zombiecatfamiliar) | Object | A familiar object representing a Zombie Cat that can be spawned. | 4 ||
| [`BirthSquirrel`](#object-birthsquirrel) | Object | An ability object that spawns a Squirrel unit. | 4 ||
| `WaterTile_Current` | Variable | A tile on the dungeon floor that is water with a current. | 4 ||
| `Attraction` | Integer | Applies or references the 'Attraction' effect/state. | 3 ||
| [`Conditional_AffectedByElement`](Abilities_and_Spells.md#object-conditional_affectedbyelement) | Object | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 3 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 3 ||
| [`Conditional_LastHit`](Abilities_and_Spells.md#object-conditional_lasthit) | Object | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 3 ||
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 3 ||
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 3 ||
| `drop_on_self_death` | Boolean | Examples: `true` | 3 ||
| `ExtraBasicAttacks_Status` | Integer | Applies or references the 'ExtraBasicAttacks_Status' effect/state. | 3 ||
| `Hex` | Integer | Applies or references the 'Hex' effect/state. | 3 ||
| `PullSourceToTarget` | Integer | Applies or references the 'PullSourceToTarget' effect/state. | 3 ||
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object | Queues the character to be resurrected at the start of the next combat round. | 3 ||
| `WaterTile` | Variable | A tile on the dungeon floor that is water. | 3 ||
| [`HeadTumor`](#object-headtumor) | Object | An enemy or object representing a Tumorous Head enemy. | 3 ||
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | Applies or references the 'Leeches' effect/state. | 2 ||
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer | Applies or references the 'MagicWeakness' effect/state. | 2 ||
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Synthesizes or spawns a new item from a specific pool. | 2 ||
| `Tech` | Integer | Applies or references the 'Tech' effect/state. | 2 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 2 ||
| [`Purge`](Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object | Applies or references the 'Purge' effect/state. | 2 ||
| [`SoulLink`](Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object | Applies or references the 'SoulLink' effect/state. | 2 ||
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer | Applies or references the 'Stealth' effect/state. | 2 ||
| [`PoisonLace`](Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String | Applies or references the 'PoisonLace' effect/state. | 2 ||
| [`poop`](Events_and_Encounters.md#object-poop) | Object | Event Object: Story branch or dialog option representing the \'Poop\' action. | 2 ||
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | Redirects the nested effects to apply to a random living member of the player's party. | 2 ||
| `AutoReanimate` | Number | Examples: `50` | 2 ||
| [`Conditional_BossOrBig`](Abilities_and_Spells.md#object-conditional_bossorbig) | Object | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 2 ||
| [`Conditional_Buddy`](Abilities_and_Spells.md#object-conditional_buddy) | Object | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 2 ||
| [`Conditional_DestructibleCorpse`](Abilities_and_Spells.md#object-conditional_destructiblecorpse) | Object | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 2 ||
| [`Conditional_Displaceable`](Abilities_and_Spells.md#object-conditional_displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 ||
| [`Conditional_NotAlly`](Abilities_and_Spells.md#object-conditional_notally) | Object | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 2 ||
| [`Conditional_NotBossOrBig`](Abilities_and_Spells.md#object-conditional_notbossorbig) | Object | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 2 ||
| [`Conditional_NotShielded`](Abilities_and_Spells.md#object-conditional_notshielded) | Object | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 2 ||
| `FireTile` | Variable | A tile on the dungeon floor that is on fire. | 2 ||
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object | Logic: Applies a negative mutation/disorder from a specific pool. | 2 ||
| `gamewin` | Variable | A variable flag indicating the game has been won. | 2 ||
| [`HornCharge`](#object-horncharge) | Object | An ability object for a charge attack using horns. | 2 ||
| `humanoid` | Variable | A reference to a humanoid entity type or tag. | 2 ||
| `ManaLeeches` | Integer | Applies or references the 'ManaLeeches' effect/state. | 2 ||
| [`OffMap`](Characters_and_Bosses.md#object-offmap) | Object | Character Form: Behavior and stats for the 'OffMap' state. | 2 ||
| `OilTile` | Variable | A tile on the dungeon floor that is covered in oil. | 2 ||
| `Ostracized` | Integer | Applies or references the 'Ostracized' effect/state. | 2 ||
| `PartyExplosion` | Variable | A reference to a Party Explosion effect or mechanic. | 2 ||
| `PermanentStrength` | Integer | Applies or references the 'PermanentStrength' effect/state. | 2 ||
| [`Pilfer`](Events_and_Encounters.md#object-pilfer) | Object | An ability object for a pilfering or stealing attack. | 2 ||
| `Possessed` | Integer | Applies or references the 'Possessed' effect/state. | 2 ||
| `PullSourceToKnockbackImmuneTarget` | Integer | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. | 2 ||
| [`Pulp2`](Characters_and_Bosses.md#object-pulp2) | Object | Character Form: Behavior and stats for the 'Pulp2' state. | 2 ||
| [`RandomPickup`](#object-randompickup) | Object | An object that represents a random pickup item. | 2 ||
| `ReduceManaCost` | Integer | Applies or references the 'ReduceManaCost' effect/state. | 2 ||
| `RepairWeaponCondition` | Integer | Applies or references the 'RepairWeaponCondition' effect/state. | 2 ||
| `TallGrassTile` | Number | Examples: `80, 15` | 2 ||
| `TempMovement` | Enum / Integer | Applies or references the 'TempMovement' effect/state. | 2 ||
| `TempSpellDamageUp` | Integer | Applies or references the 'TempSpellDamageUp' effect/state. | 2 ||
| `the_coven` | Variable | A reference to the Coven faction or group in logic. | 2 ||
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 ||
| [`ThrowPoop`](#object-throwpoop) | Object | An ability object for throwing poop as an attack. | 2 ||
| [`AntlerSwipe`](#object-antlerswipe) | Object | An ability object for a swipe attack using antlers. | 2 ||
| [`BerserkDash`](#object-berserkdash) | Object | An ability object for a dash attack used by berserk units. | 2 ||
| `BlankTile` | Number | Examples: `5` | 2 ||
| [`Boulder`](#object-boulder) | Object | Defines a persistent, impassable obstacle tile that blocks movement and line of sight until destroyed. | 2 ||
| [`CharmTrap`](#object-charmtrap) | Object | Defines a deployable hazard that charms the first unit that steps onto it, forcing them to move toward the trapper. | 2 ||
| `flip` | Variable | A variable that toggles a boolean state, typically used to flip a unit's sprite or orientation. | 2 ||
| [`HardenSkin`](#object-hardenskin) | Object | Defines a self-buff ability that grants temporary damage reduction or armor to the unit. | 2 ||
| [`MonkeyThrow`](#object-monkeythrow) | Object | Defines a ranged attack ability where the unit hurls a projectile at a target tile or enemy. | 2 ||
| [`MoonHandDrop`](#object-moonhanddrop) | Object | A variant of MoonHandThrow that drops an object or payload onto a target tile from above, often with bonus passives. | 2 ||
| [`Pounce`](#object-pounce) | Object | Defines a leap ability that moves the unit to an adjacent tile and deals damage to the target upon landing. | 2 ||
| [`Prance`](#object-prance) | Object | Defines a self-buff ability for the Elk Form that enhances mobility or grants a temporary stat boost. | 2 ||
| [`Scavenge`](#object-scavenge) | Object | Defines a move ability that allows the unit to collect items or resources from the environment. | 2 ||
| [`SquirrelForm`](Characters_and_Bosses.md#object-squirrelform) | Object | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 ||
| [`Synthesize`](#object-synthesize) | Object | Defines a self-buff ability that consumes resources to create or upgrade an item on the unit. | 2 ||
| [`TaintedOffering`](#object-taintedoffering) | Object | Defines a sacrificial ability that deals damage to or debuffs the unit in exchange for a powerful benefit. | 2 ||
| [`Tease`](#object-tease) | Object | Defines a targeted status ability for the Mockingbird Form that applies a debuff to an enemy unit. | 2 ||
| [`TheDestroyer`](#object-thedestroyer) | Object | Defines an ultimate or high-damage ability that devastates a large area or single target. | 2 ||
| [`TigerSwipes`](#object-tigerswipes) | Object | Defines a multi-hit melee attack ability that strikes an adjacent target multiple times in rapid succession. | 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 1 ||
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object | Character Form: Behavior and stats for the 'Rain' state. | 1 ||
| [`megadino`](#object-megadino) | Variable | A variable flag indicating the unit is a Mega Dinosaur, granting increased size and stats. | 1 ||
| [`moonhead`](#object-moonhead) | Variable | A variable flag indicating the unit is a Moon Head, associated with alien or lunar abilities. | 1 ||
| `alien` | Variable | A variable flag indicating the unit is an Alien type, granting access to alien-specific abilities or resistances. | 1 ||
| [`AllyInfested`](#object-allyinfested) | Object | Examples: `{ ... }` | 1 ||
| `angeljunk` | Variable | A variable flag indicating the unit is Angel Junk, a celestial or corrupted type with unique properties. | 1 ||
| [`AntlerSwipe2`](#object-antlerswipe2) | Object | A variant of AntlerSwipe that serves as a basic attack for the Elk Form with an alternate description. | 1 ||
| [`BasicDashAttackMove_NoKnockback`](#object-basicdashattackmove_noknockback) | Object | Defines a basic dash attack ability that moves the unit forward but does not knock back the target. | 1 ||
| `berserkIdle` | Variable | A variable flag that triggers a berserk idle animation or behavior when the unit is enraged. | 1 ||
| `bonusbird` | Variable | A variable flag indicating the unit is a Bonus Bird, a special type with extra rewards on defeat. | 1 ||
| [`Boris`](Characters_and_Bosses.md#object-boris) | Enum / Object | `MegaGuppy_TransformBoris` | 1 ||
| `BrambleTile` | Variable | A variable that identifies a tile covered in brambles, damaging units that step onto it. | 1 ||
| `chapter_corpse_medium` | Variable | A variable that references a medium-sized corpse object used as a chapter-specific prop. | 1 ||
| [`Chitter`](#object-chitter) | Object | Defines a spell ability that emits a sonic screech or chittering sound, damaging nearby enemies. | 1 ||
| [`cm_RaptorEggSpawn`](#object-cm_raptoreggspawn) | Object | Defines a spawn ability that creates a raptor egg object at the target location. | 1 ||
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | Conditional constraint. Nested properties only trigger if this is true. | 1 ||
| [`Conditional_ActiveWeather_Any`](Abilities_and_Spells.md#object-conditional_activeweather_any) | Object | Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 1 ||
| [`Conditional_Backstab`](Abilities_and_Spells.md#object-conditional_backstab) | Object | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 1 ||
| [`Conditional_CanBeHealed`](Abilities_and_Spells.md#object-conditional_canbehealed) | Object | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 1 ||
| [`Conditional_DebuffRoll`](Abilities_and_Spells.md#object-conditional_debuffroll) | Object | Conditional trigger: Executes nested logic based on a randomized debuff probability. | 1 ||
| [`Conditional_FinishedSpawning`](Abilities_and_Spells.md#object-conditional_finishedspawning) | Object | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 ||
| [`Conditional_HasCleansableDebuffs`](Abilities_and_Spells.md#object-conditional_hascleansabledebuffs) | Object | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 1 ||
| [`Conditional_HasKnockback`](Characters_and_Bosses.md#object-conditional_hasknockback) | Object | Conditional: Executes logic if the triggering attack deals knockback. | 1 ||
| [`Conditional_IsPhysicalAttack`](Characters_and_Bosses.md#object-conditional_isphysicalattack) | Object | Conditional: Executes logic if the triggering attack is physical. | 1 ||
| [`Conditional_IsTrample`](Abilities_and_Spells.md#object-conditional_istrample) | Object | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 1 ||
| [`Conditional_LivingPlayerCat`](Abilities_and_Spells.md#object-conditional_livingplayercat) | Object | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 1 ||
| [`Conditional_NotBig`](Abilities_and_Spells.md#object-conditional_notbig) | Object | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 1 ||
| [`Conditional_SourceAbilityHasTag`](Abilities_and_Spells.md#object-conditional_sourceabilityhastag) | Object | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 1 ||
| [`Conditional_SourceHasStatus`](Abilities_and_Spells.md#object-conditional_sourcehasstatus) | Object | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 1 ||
| `container` | Variable | A variable flag indicating the object is a container that can be opened for loot. | 1 ||
| [`DeathWormEat`](#object-deathwormeat) | Object | Defines a return ability for the Death Worm that consumes a target tile, dealing damage and recovering health. | 1 ||
| `deferred` | Boolean | `true` | 1 ||
| `DirtTile` | Variable | A variable that identifies a dirt tile, which may be diggable or affect movement costs. | 1 ||
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Examples: `MoonHandDrop` | 1 ||
| [`DualSword`](Characters_and_Bosses.md#object-dualsword) | Object | Character Form: Behavior and stats for the \'DualSword\' state. | 1 ||
| [`DybbukPossessed`](Abilities_and_Spells.md#object-dybbukpossessed) | Object | Defines the abilities and behaviors available when possessing another entity. | 1 ||
| `EggSackTrap` | Variable | A variable that identifies an Egg Sack trap, which explodes into damaging hatchlings when triggered. | 1 ||
| [`EtherSoakedRag`](#object-ethersoakedrag) | Object | Defines a deployable item that applies a flammable or ethereal effect to the target area. | 1 ||
| [`Explosive`](Characters_and_Bosses.md#object-explosive) | Enum / Object | `MegaGuppy_TransformExplosive` | 1 ||
| `GenericBuff` | Integer | Applies or references the 'GenericBuff' effect/state. | 1 ||
| `ghost` | Variable | A variable flag indicating the unit is a Ghost, granting phasing or intangibility. | 1 ||
| `GlassTile` | Variable | A variable that identifies a glass tile, which shatters under pressure, creating a hazard. | 1 ||
| `god` | Variable | A variable flag indicating the unit is a God, granting immense power or special mechanics. | 1 ||
| [`Grown`](Characters_and_Bosses.md#object-grown) | Object | Character Form: Behavior and stats for the \'Grown\' state. | 1 ||
| `grown_hitler_clone` | Variable | A variable flag indicating the unit is a fully grown Hitler Clone, a powerful enemy type. | 1 ||
| [`HalfDead`](Characters_and_Bosses.md#object-halfdead) | Object | Character Form: Behavior and stats for the \'HalfDead\' state. | 1 ||
| [`HardenSkin2`](#object-hardenskin2) | Object | A variant of HardenSkin providing greater or alternate damage reduction. | 1 ||
| [`head_CrownOfHorns`](#object-head_crownofhorns) | Object | Defines a head equipment item that grants thorns damage or a defensive aura. | 1 ||
| `hitler_clone` | Variable | A variable flag indicating the unit is a Hitler Clone, a recurring enemy type. | 1 ||
| `hitler_clone_fetus` | Variable | A variable flag indicating the unit is a fetal Hitler Clone, a weaker or earlier stage. | 1 ||
| [`Infested`](Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object | data/elite_buffs.gon | 1 ||
| `JesterMinusColorless` | Variable | A variable that modifies the Jester trait pool to exclude colorless mutations. | 1 ||
| [`JewelOfDrog`](#object-jewelofdrog) | Object | Defines a powerful artifact item that grants unique stat bonuses or abilities. | 1 ||
| `kill_on_consume` | Boolean | Examples: `true` | 1 ||
| [`MegaGuppy`](#object-megaguppy) | Object | Defines a transformation ability that turns the unit into a Mega Guppy, increasing stats and size. | 1 ||
| [`MockSong`](#object-mocksong) | Object | Defines a spell ability for the Mockingbird Form that mimics or replicates the target's attack. | 1 ||
| [`MockSong2`](#object-mocksong2) | Object | A variant of MockSong for the Mockingbird Form that mimics an advanced or different attack. | 1 ||
| [`MonkeyThrow2`](#object-monkeythrow2) | Object | A variant of MonkeyThrow that throws a different projectile or with altered properties. | 1 ||
| [`MoonHeadFlail`](#object-moonheadflail) | Object | Defines a melee attack ability for Moon Head units that flails in an arc, hitting multiple adjacent tiles. | 1 ||
| `NoDeathrattle` | Variable | A variable flag that prevents the unit from triggering its deathrattle effect upon death. | 1 ||
| `OverrideChainKnockbackDamage` | Equation | Applies or references the 'OverrideChainKnockbackDamage' effect/state. | 1 ||
| `PermanentCharisma` | Integer | Applies or references the 'PermanentCharisma' effect/state. | 1 ||
| `PermanentLuck` | Integer | Applies or references the 'PermanentLuck' effect/state. | 1 ||
| [`Prance2`](#object-prance2) | Object | A variant of Prance with an enhanced or alternative buff effect. | 1 ||
| `ProbeCharmed` | Integer | Applies or references the 'ProbeCharmed' effect/state. | 1 ||
| `rotate_right` | Variable | A variable that triggers a clockwise rotation of the unit or object. | 1 ||
| [`Scavenge2`](#object-scavenge2) | Object | A variant of Scavenge with an improved or alternative resource gathering effect. | 1 ||
| `Scrambled` | Integer | Applies or references the 'Scrambled' effect/state. | 1 ||
| [`Small`](Characters_and_Bosses.md#object-small) | Object | Character Form: Behavior and stats for the \'Small\' state. | 1 ||
| [`SmallHolding`](Characters_and_Bosses.md#object-smallholding) | Object | Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 ||
| [`SmallHoldingCat`](Characters_and_Bosses.md#object-smallholdingcat) | Object | Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 ||
| `spear` | Variable | References the Spear ability or object. | 1 ||
| `SplashDamage` | Integer | Applies or references the 'SplashDamage' effect/state. | 1 ||
| [`Standing`](Characters_and_Bosses.md#object-standing) | Object | Character Form: Behavior and stats for the 'Standing' state. | 1 ||
| [`Synthesize2`](#object-synthesize2) | Object | An upgraded variant of the Synthesize ability. | 1 ||
| [`TaintedOffering2`](#object-taintedoffering2) | Object | A variant of the TaintedOffering ability. | 1 ||
| `TallFlowerTile` | Variable | References the TallFlowerTile object or asset. | 1 ||
| [`Tease2`](#object-tease2) | Object | An upgraded variant of the Tease ability. | 1 ||
| `the_nuke_bearer` | Variable | References the unit or object that carries the Nuke ability. | 1 ||
| `themotherspike` | Variable | References the MotherSpike object or ability. | 1 ||
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | `item_aux` | 1 ||
| [`TigerSwipes2`](#object-tigerswipes2) | Object | An upgraded variant of the TigerSwipes ability. | 1 ||
| [`Timber`](#object-timber) | Object | An alternate basic ability for TreeForm units, using the trample_dash template. | 1 ||
| [`TinaFlail`](#object-tinaflail) | Object | References the TinaFlail ability. | 1 ||
| [`TinaFlailRage`](#object-tinaflailrage) | Object | References the upgraded TinaFlailRage ability. | 1 ||
| [`TransformWeapon`](Abilities_and_Spells.md#object-transformweapon) | Object | Transforms the equipped weapon into another specific weapon state. | 1 ||
| `weapon_throw` | Variable | References the weapon throw mechanic or ability. | 1 ||
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 0 ||
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 0 ||
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 0 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Forces the character or target to instantly use a specified ability. | 0 ||
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
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object | Specifies a pool of disorders or a custom chance to gain a disorder when the condition is met. || `all_disorders` (Enum), `{ ... }` (Object) |

</details>

---

#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 59

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 422 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The amount of flat damage reduction applied to the source. | 20 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of Bruise stacks applied, or an array with duration and chance. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 6 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | If set to 1, removes all status effects from the target; if 0, no cleanse. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `Tech` | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `AddWeaponAux` | Integer / String | Adds to the weapon's auxiliary value, supporting integer or formula input. || `-item_aux` (Enum), `2` (Number), `1` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `EquipPermanentItem` | Enum | Determines which permanent item (e.g., a body part or bone club) is equipped to the source. || `BoneClub` (Enum), `Kidney` (Enum) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Evolves a random ability from the specified pool, optionally flagged as upgraded. || `Necromancer` (Enum), `Thief` (Enum), `{ ... }` (Object) |
| `FindItem` | Enum | Determines which specific item (e.g., Molars, Pearl) is granted to the source. || `BoneClub` (Enum), `Pearl` (Enum) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Determines the item pool name from which a random item is granted to the source. || `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. || `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). || `passive` (Enum), `Default` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer | The number of free spells granted, allowing the source to cast spells without consuming mana or charges. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. || `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `2*X` (Enum), `3*X` (Enum), `3` (Number), `8` (Number) |
| `LuckUp` | Enum / Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. || `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `SpeedUp` | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 0 ||

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Nested conditional. | 1 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `2` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |

</details>

---

#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | Nested conditional. | 1 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type to check for. | 1 ||
| `Burn` | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 36 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 8 | `[1 .5]` (Array), `6` (Number), `3` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | If set to 1, removes all status effects from the target; if 0, no cleanse. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Nested conditional. | 1 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `ManaGain` | Enum / Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `SpeedUp` | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The number of temporary damage increase stacks applied to the target for the current turn. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | Alias for TempSpeedUp; temporarily increases the unit's speed stat. || `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. (Must be float values) | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Instakill` | Integer | If an integer, the percentage chance to instantly kill the target. If an array [stacks, probability], applies that many stacks with the given probability per stack. || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Nested conditional. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer | The number of stacks of the Drowsy status effect to apply, which reduces a unit's action points or turn efficiency. || `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Immobile` | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | The percentage or flat amount of HP restored when reviving a dead ally. | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomMutation` | Integer | The number of random mutations to apply. || `3` (Number), `1` (Number) |
| `SafeDoomed` | Enum / Integer | The number of turns until the target is instantly killed when this counter reaches zero, but unlike standard Doomed, it does not inflict injuries upon death. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of applying the debuff. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `LaunchOffScreen` | String | An expression that calculates the distance (in tiles) to launch the target off-screen, based on damage formula. || `10+bonus_melee_ability_damage` (Enum) |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The number of turns of Confusion applied, or an array with duration and chance. | 6 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Nested conditional. | 3 ||
| [`Conditional_PartyMember`](#conditional_partymember) | Object | Nested conditional. | 2 ||
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | The number of Leech stacks applied, healing the attacker. | 2 | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Conditional_FinishedSpawning`](Abilities_and_Spells.md#object-conditional_finishedspawning) | Object | Nested conditional. | 1 ||
| `Burn` | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Attraction` | Integer | If set to 1, the target is pulled one tile toward the source of the effect. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Doomed` | Integer | The number of turns until the target is instantly killed when this counter reaches zero. || `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Hex` | Integer | The number of Hex stacks applied, which increases the chance of negative status effects landing on the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Marked`](Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The number of temporary damage increase stacks applied to the target for the current turn. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 6 | `[1 .5]` (Array), `6` (Number), `-2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `-2` (Number), `5` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `DivineShield` | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. || `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. || `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `ManaGain` | Enum / Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |

</details>

---

#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 ||
| `Immobile` | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of turns of Slow applied, or an array with duration and chance. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Freeze` | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `ChangeTilesUnder` | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. || `LavaTile` (Enum), `DirtTile` (Enum) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Determines the item pool name from which a random item is granted to the source. || `parasites` (Enum), `chapter_specific_item` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. || `cm_RaptorEggSpawn` (Enum), `tk_WeirdEgg_Spawn` (Enum), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Forces the unit to immediately use the specified ability, even if stunned. || `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `RandomMutation` | Integer | The number of random mutations to apply. || `3` (Number), `1` (Number) |

</details>

---

#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 20 ||
| `Quivered` | Array / Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The number of turns of Confusion applied, or an array with duration and chance. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of turns of Slow applied, or an array with duration and chance. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). || `passive` (Enum), `Bully` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 47

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific string tag to check for. | 981 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Nested conditional. | 6 ||
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Nested conditional. | 4 ||
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `ChangeTilesUnder` | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. || `LavaTile` (Enum), `DirtTile` (Enum) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | Specifies the number of sides on a die roll for a random outcome. || `1` (Number), `6` (Number), `{ ... }` (Object) |
| `EventBounty` | Integer | The number of Event Bounty stacks applied, which increases the chance of encountering special events or loot drops. || `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Forces the unit to immediately use the specified ability, even if stunned. || `HitlerCloneHeil` (Enum), `cm_Lard_Impl` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer | If an integer, the percentage chance to instantly kill the target. If an array [stacks, probability], applies that many stacks with the given probability per stack. || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object | Pops the current object and spawns a new one, optionally cloning cat data and items. || `Sprout` (Enum), `TheDestroyer` (Enum), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Specifies the ability name the unit will use at the end of each round. || `MegaGuppy_SummonTheChild` (Enum), `ManglerThrowRemote` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 5 ||
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 ||
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | Nested conditional. | 1 ||
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | `item_aux` | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | Specifies the number of sides on a die roll for a random outcome. || `1` (Number), `6` (Number), `{ ... }` (Object) |
| `FlatLeech` | Integer | The amount of flat health restored per hit (leech). || `X` (Enum), `5` (Number), `2` (Number) |
| `Instakill` | Integer | If an integer, the percentage chance to instantly kill the target. If an array [stacks, probability], applies that many stacks with the given probability per stack. || `[25 .01]` (Array), `50` (Number), `999` (Number) |

</details>

---

#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance increase, in percentage points. | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| [`form`](./Enums.md#enum-form) | Enum / Integer | The specific form ID to check for. | 7 ||
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The percentage of dodge chance granted by this status effect. | 2 | `[1 .5]` (Array), `15` (Number), `20` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). || `Drunker` (Enum), `BigHolding` (Enum), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Specifies the ability name the unit will use at the end of each round. || `MegaGuppy_SummonTheChild` (Enum), `ManglerThrowRemote` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of Bruise stacks applied, or an array with duration and chance. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `RepairTrinket` | Integer | The amount of durability restored to the trinket item slot. || `1` (Number), `99` (Number) |

</details>

---

#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The number of turns of Confusion applied, or an array with duration and chance. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | Nested conditional. | 2 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Doomed` | Integer | The number of turns until the target is instantly killed when this counter reaches zero. || `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Immobile` | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Knockback` | Integer | The number of tiles the target is knocked back. || `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Nested conditional. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `RepairWeapon` | Array / Integer | The number of stacks of RepairWeapon applied (or an array [stacks, probability] for random application). || `[1 .25]` (Array), `6` (Number), `1` (Number) |

</details>

---

#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `ReduceManaCost` | Integer | The number by which mana cost of abilities is reduced, up to a minimum of zero. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object | Nested conditional. | 3 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer | Applies or references the 'Charmed' effect/state. | 0 ||
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 0 ||

</details>

---

#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | If set to 1, removes all status effects from the target; if 0, no cleanse. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Charge` | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. || `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Scrambled` | Integer | The number of stacks of the Scrambled status effect applied to the target. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | If an integer, the number of cleave hits; if an object, may contain a chance for cleave. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`SetItemAux`](Engine_StatusAndPassiveKeys.md#object-setitemaux) | Object | Sets the auxiliary value of a specific item slot (e.g., face, trinket, head) to a calculated value. || `{ ... }` (Object) |
| `Stun` | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 981 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins scattered, or an object with stacks and stacking behavior. || `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of Bruise stacks applied, or an array with duration and chance. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 981 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||

</details>

---

#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Nested conditional. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Knockback` | Integer | The number of tiles the target is knocked back. || `3` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 85

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance increase, in percentage points. | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of Bruise stacks applied, or an array with duration and chance. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The number of turns of Confusion applied, or an array with duration and chance. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of turns of Slow applied, or an array with duration and chance. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Nested conditional. | 2 ||
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | If set to 1, removes all status effects from the target; if 0, no cleanse. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The percentage of dodge chance granted by this status effect. | 2 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | The number of Leech stacks applied, healing the attacker. | 2 | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| [`Revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | The percentage or flat amount of HP restored when reviving a dead ally. | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| [`Conditional_Displaceable`](Abilities_and_Spells.md#object-conditional_displaceable) | Object | Nested conditional. | 1 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 1 ||
| [`Conditional_HasKnockback`](Characters_and_Bosses.md#object-conditional_hasknockback) | Object | Nested conditional. | 1 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Nested conditional. | 1 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Nested conditional. | 1 ||
| [`Conditional_Object`](Abilities_and_Spells.md#object-conditional_object) | Object | Nested conditional. | 1 ||
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | Nested conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`AllyInfested`](#object-allyinfested) | Array / Number / Object | Spawns an allied infested unit (e.g., CharmedMaggot) on the target's side. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | If an integer, the number of cleave hits; if an object, may contain a chance for cleave. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`DybbukPossessed`](Abilities_and_Spells.md#object-dybbukpossessed) | Object | An object configuring the Dybbuk possession effect, including exit and punch-self abilities. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). || `passive` (Enum), `Holy` (Enum), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. || `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Forces the unit to immediately use the specified ability, even if stunned. || `MoonHandMegaSqueeze` (Enum), `tk_ButterBean_Normal` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer | If an integer, the percentage chance to instantly kill the target. If an array [stacks, probability], applies that many stacks with the given probability per stack. || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| [`Marked`](Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. || `Maggot` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `PartialCleanse` | Integer | The number of status effects removed from the target (partial cleanse). || `1` (Number), `9999` (Number) |
| `PermanentCharm` | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String | The number of stacks or chance to decrease a random stat; can be an array `[stacks, probability]` or a formula. || `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins scattered, or an object with stacks and stacking behavior. || `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | Alias for TempSpeedUp; temporarily increases the unit's speed stat. || `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `Webbed` | Integer | The number of Webbed stacks applied, which immobilizes the target and prevents movement; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2166

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Nested conditional. | 38 ||
| `CritChanceUp` | Integer | The amount of critical hit chance increase, in percentage points. | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 36 | `[1 .5]` (Array), `3` (Number), `5` (Number), `{ ... }` (Object) |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | Nested conditional. | 35 ||
| `HealthRegenUp` | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Nested conditional. | 25 ||
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The amount of flat damage reduction applied to the source. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 14 ||
| `Trample` | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 14 | `[3 X-8]` (Array), `[1 .5]` (Array), `9` (Number), `6` (Number), `{ ... }` (Object) |
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Nested conditional. | 13 ||
| [`Conditional_FormulaIsPositive`](Abilities_and_Spells.md#object-conditional_formulaispositive) | Object | Nested conditional. | 10 ||
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | Nested conditional. | 10 ||
| `Bleed` | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | `[1 .1]` (Array), `[3 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of Bruise stacks applied, or an array with duration and chance. | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `5` (Number), `{ ... }` (Object) |
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Nested conditional. | 6 ||
| `Blind` | Array / Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 6 | `[1 .25]` (Array), `[1 .10]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The number of turns of Confusion applied, or an array with duration and chance. | 6 | `[1 .2]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 6 | `[1 .5]` (Array), `3` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 6 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Leech` | Integer | The amount of health stolen per hit as a percentage of damage dealt. | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Nested conditional. | 5 ||
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Nested conditional. | 5 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Nested conditional. | 5 ||
| [`Conditional_Object`](Abilities_and_Spells.md#object-conditional_object) | Object | Nested conditional. | 5 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Nested conditional. | 5 ||
| [`Conditional_Familiar`](Abilities_and_Spells.md#object-conditional_familiar) | Object | Nested conditional. | 4 ||
| `Immobile` | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Reanimate`](Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object | The percentage chance (e.g., 50%) to revive upon death. | 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `SizeScale` | Number | A multiplier for the unit's visual size. Values above 1 increase size, values below 1 decrease size. | 4 | `1.1` (Number), `1.3` (Number), `.6` (String), `.8` (String) |
| [`Conditional_AffectedByElement`](Abilities_and_Spells.md#object-conditional_affectedbyelement) | Object | Nested conditional. | 3 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Nested conditional. | 3 ||
| [`Conditional_LastHit`](Abilities_and_Spells.md#object-conditional_lasthit) | Object | Nested conditional. | 3 ||
| `AlphaCat` | Integer | The number of stacks of the AlphaCat status effect. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The percentage of dodge chance granted by this status effect. | 2 | `[1 .5]` (Array), `15` (Number), `50` (Number), `{ ... }` (Object) |
| `DrinkWater` | Integer | The number of stacks of the Drink Water status effect applied, which may trigger water-related behaviors or effects. | 2 | `1` (Number) |
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | The number of Leech stacks applied, healing the attacker. | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | Nested conditional. | 2 ||
| [`Conditional_BossOrBig`](Abilities_and_Spells.md#object-conditional_bossorbig) | Object | Nested conditional. | 2 ||
| [`Conditional_Buddy`](Abilities_and_Spells.md#object-conditional_buddy) | Object | Nested conditional. | 2 ||
| [`Conditional_DestructibleCorpse`](Abilities_and_Spells.md#object-conditional_destructiblecorpse) | Object | Nested conditional. | 2 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Nested conditional. | 2 ||
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object | Nested conditional. | 2 ||
| [`Conditional_NotAlly`](Abilities_and_Spells.md#object-conditional_notally) | Object | Nested conditional. | 2 ||
| [`Conditional_NotBossOrBig`](Abilities_and_Spells.md#object-conditional_notbossorbig) | Object | Nested conditional. | 2 ||
| [`Conditional_NotShielded`](Abilities_and_Spells.md#object-conditional_notshielded) | Object | Nested conditional. | 2 ||
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | Nested conditional. | 2 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | Nested conditional. | 2 ||
| `MagicWeakness` | Array / Integer | The number of stacks of MagicWeakness, increasing incoming magic damage; can be an array `[stacks, probability]`. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`PoisonLace`](Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String | The amount or formula for PoisonLace damage applied per turn; can be a fixed integer or a formula like `X/3`. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Purge`](Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object | The number of stacks of Purge to apply, removing beneficial statuses. | 2 | `3` (Number), `0` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `3` (Number), `-3` (Number) |
| [`Reflect`](Engine_StatusAndPassiveKeys.md#object-reflect) | Integer / Object | The number of stacks of Reflect, causing a percentage of incoming damage to be reflected back to the attacker. | 2 | `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| [`Revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | The percentage or flat amount of HP restored when reviving a dead ally. | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| [`SoulLink`](Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object | The number of turns the linked status lasts, sharing damage between linked units. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Infested`](Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object | The number of stacks of Infested, causing the unit to spawn a friendly fly or swarm upon death. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | Nested conditional. | 1 ||
| [`Conditional_ActiveWeather_Any`](Abilities_and_Spells.md#object-conditional_activeweather_any) | Object | Nested conditional. | 1 ||
| [`Conditional_Backstab`](Abilities_and_Spells.md#object-conditional_backstab) | Object | Nested conditional. | 1 ||
| [`Conditional_CanBeHealed`](Abilities_and_Spells.md#object-conditional_canbehealed) | Object | Nested conditional. | 1 ||
| [`Conditional_DebuffRoll`](Abilities_and_Spells.md#object-conditional_debuffroll) | Object | Nested conditional. | 1 ||
| [`Conditional_Displaceable`](Abilities_and_Spells.md#object-conditional_displaceable) | Object | Nested conditional. | 1 ||
| [`Conditional_HasCleansableDebuffs`](Abilities_and_Spells.md#object-conditional_hascleansabledebuffs) | Object | Nested conditional. | 1 ||
| [`Conditional_IsTrample`](Abilities_and_Spells.md#object-conditional_istrample) | Object | Nested conditional. | 1 ||
| [`Conditional_LivingPlayerCat`](Abilities_and_Spells.md#object-conditional_livingplayercat) | Object | Nested conditional. | 1 ||
| [`Conditional_NotBig`](Abilities_and_Spells.md#object-conditional_notbig) | Object | Nested conditional. | 1 ||
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | Nested conditional. | 1 ||
| [`Conditional_SourceAbilityHasTag`](Abilities_and_Spells.md#object-conditional_sourceabilityhastag) | Object | Nested conditional. | 1 ||
| [`Conditional_SourceHasStatus`](Abilities_and_Spells.md#object-conditional_sourcehasstatus) | Object | Nested conditional. | 1 ||
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object | Configures a rain weather effect, including particle system and AI brain. | 1 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. |||
| `Attraction` | Integer | If set to 1, the target is pulled one tile toward the source of the effect. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BounceObject`](Abilities_and_Spells.md#object-bounceobject) | Enum / Object | Spawns and bounces the specified object onto a random tile, with an optional chance. || `CharmedFlea_Champion` (Enum), `CharmedDip` (Enum), `{ ... }` (Object) |
| `BurgleCoin` | Array / Integer | The number of coins stolen, or an array of [stacks, probability]. || `[1 .5]` (Array), `3` (Number), `1` (Number) |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change the target's tile into (e.g., BrambleTile, LavaTile). || `FireTile` (Enum), `GrassTile` (Enum), `{ ... }` (Object) |
| `ChangeTilesUnder` | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. || `LavaTile` (Enum), `DirtTile` (Enum) |
| `Charge` | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. || `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer | The amount of Charisma stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. || `[1 .25]` (Array), `[1 .15]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | If an integer, the number of cleave hits; if an object, may contain a chance for cleave. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | An object containing global modifier effects to apply after the time delay. || `{ ... }` (Object) |
| `DamageOrHealConditionally` | Integer | If set to 1, the status group effect conditionally deals damage or heals based on target. || `1` (Number) |
| `DexterityUp` | Enum / Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer | The number of stacks of DiminishingHealthRegen, providing health regeneration each turn that decreases with each stack. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `Doomed` | Integer | The number of turns until the target is instantly killed when this counter reaches zero. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer | The number of stacks of the Drowsy status effect to apply, which reduces a unit's action points or turn efficiency. || `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Evolves a random ability from the specified pool, optionally flagged as upgraded. || `Tinkerer` (Enum), `Fighter` (Enum), `{ ... }` (Object) |
| `ExtraBasicAttacks_Status` | Integer | The number of extra basic attacks the unit can perform each turn. Stacks for additional attacks. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves the unit can perform each turn. Stacks for additional moves. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .25]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. || `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `FindExtraItemFromPoolOnBattleEnd` | Enum | The loot pool from which to grant an extra item at battle end. || `combat_reward_easy` (Enum), `pills` (Enum) |
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | Forces the unit to perform a basic attack immediately. || `1` (Number), `{ ... }` (Object) |
| `ForceMoveAway` | Integer | The number of tiles the unit is forced to move away from its attacker. || `1` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. || `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer | The number of free spells granted, allowing the source to cast spells without consuming mana or charges. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. || `[1 .25]` (Array), `[1 .15]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. || `{ ... }` (Object) |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `Hex` | Integer | The number of Hex stacks applied, which increases the chance of negative status effects landing on the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Forces the unit to immediately use the specified ability, even if stunned. || `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer | If an integer, the percentage chance to instantly kill the target. If an array [stacks, probability], applies that many stacks with the given probability per stack. || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `IntelligenceUp` | Enum / Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Knockback` | Integer | The number of tiles the target is knocked back. || `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`KnockOutCoin`](Abilities_and_Spells.md#object-knockoutcoin) | Integer / Object | Either an integer for guaranteed stacks or an object with `stacks` and `chance` for a probability-based knock-out effect. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Lifesteal` | Integer | The number of stacks of Lifesteal, converting a percentage of damage dealt into healing for the attacker. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. || `[1 .5]` (Array), `3` (Number), `-4` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). || `item_aux` (Enum), `X-1` (Enum), `2` (Number), `6` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `ManaLeeches` | Integer | The number of mana leech stacks that drain mana on hit. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `MovementUp` | Integer | The number of points of additional movement gained for a number of turns. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `NonStackingDivineShield` | Integer | A non-stacking shield that blocks the next instance of damage; applied as an integer for the number of shields. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. || `SkeletonCatFamiliar` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `Ostracized` | Integer | The number of stacks of Ostracized, making the unit unable to be targeted by ally abilities or receive allied benefits. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `OverrideChainKnockbackDamage` | String | A formula or value that overrides the damage dealt by chain knockback effects. || `3+bonus_melee_ability_damage` (Enum), `0` (Number) |
| `PartialCleanse` | Integer | The number of status effects removed from the target (partial cleanse). || `1` (Number), `9999` (Number) |
| `PermanentConstitution` | Integer | The amount of permanent Constitution (max HP) added. || `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer | The amount of permanent dexterity added to the unit. || `1` (Number), `2` (Number) |
| `PermanentIntelligence` | Integer | The number of permanent intelligence stat points added or subtracted. || `1` (Number), `2` (Number) |
| `PermanentSpeed` | Integer | The number of permanent speed stat points added or subtracted. || `1` (Number), `2` (Number) |
| `Petrify` | Array / Integer | The number of stacks of Petrify, turning the unit to stone and immobilizing it; can be an array `[stacks, probability]`. || `[1 .15]` (Array), `[1 .2]` (Array), `1` (Number), `{ ... }` (Object) |
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object | Pops the current object and spawns a new one, optionally cloning cat data and items. || `TheDestroyer` (Enum), `StemCat_HalfHealth` (Enum), `{ ... }` (Object) |
| `Possessed` | Integer | The number of stacks of the Possessed status effect applied, which causes the unit to be controlled by an external force. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ProbeCharmed` | Integer | The number of stacks of ProbeCharmed status, which charms the target when probed. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomInjury` | Integer | The number of random injuries applied to the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. || `[1 .5]` (Array), `5` (Number), `6` (Number), `{ ... }` (Object) |
| `RandomPermanentStat` | Integer | The amount of random permanent stat change applied, positive or negative. || `-1` (Number), `-2` (Number) |
| `RandomStatDown` | Array / Integer / String | The number of stacks or chance to decrease a random stat; can be an array `[stacks, probability]` or a formula. || `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `RangeUp` | Integer | The amount of bonus range added to the unit's attacks. Each stack adds one tile of range. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ReduceManaCost` | Integer | The number by which mana cost of abilities is reduced, up to a minimum of zero. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `RepairWeapon` | Array / Integer | The number of stacks of RepairWeapon applied (or an array [stacks, probability] for random application). || `[1 .25]` (Array), `6` (Number), `1` (Number) |
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object | The number of stacks of ReviveNextRound or an object defining revival properties; causes the unit to revive with specified health, shields, or buffs at the start of the next round. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Rot` | Array / Integer | The number of stacks of Rot, causing damage over time and potentially spawning a fly on death; can be an array `[stacks, probability]`. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SetDefaultFace` | Enum | Specifies the default face expression for the unit (e.g., sad, happy, insane). || `insane` (Enum), `happy` (Enum) |
| `Sleep` | Array / Integer | The number of stacks of Sleep, putting the unit to sleep for that many turns; can be an array `[stacks, probability]`. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer | If integer, the number of coins spawned; if array, [stacks, probability] of spawning a coin anywhere on the map. || `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer | The number of turns the target is infested with spiders, taking damage over time. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`StatusAllCharactersOnSpawn`](House_and_Environment.md#object-statusallcharactersonspawn) | Object | Applies the nested status effects to all characters when this object spawns. || `{ ... }` (Object) |
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | A collection of status effects applied together as a group, each with its own stack count. || `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of turns the target is unable to move, with optional [stacks, probability] format. || `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer | The number of stacks of Tarred, making the unit more vulnerable to fire damage; can be an array `[stacks, probability]`. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempCounterAttack` | Integer | The number of stacks (turns) for TempCounterAttack, causing the unit to counterattack after being hit. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The number of temporary damage increase stacks applied to the target for the current turn. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempDexterityUp` | Enum | A temporary increase to the dexterity stat, specified as an alias or integer. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempMovement` | Enum / Integer | Specifies the temporary movement range granted to the unit, either as an integer or via an alias. Stacks determine duration in turns. || `[1 .5]` (Array), `20` (Number), `1` (Number), `{ ... }` (Object) |
| `TempRangeUp` | Integer | The number of turns this unit gains increased attack range. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | Alias for TempSpeedUp; temporarily increases the unit's speed stat. || `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpellDamageUp` | Integer | A temporary increase to spell damage output. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempStrengthUp` | Enum | Alias for TempStrengthUp; temporarily increases the unit's strength stat. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Specifies the ability name the unit will use at the end of each round. || `MegaGuppy_SummonTheChild` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `Webbed` | Integer | The number of Webbed stacks applied, which immobilizes the target and prevents movement; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `Alert`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Alert` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `AllAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 | `{ ... }` (Object) |

</details>

### Object: `AllyInfested`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `faction` | Enum | Determines which faction the spawned entity belongs to, controlling its team allegiance and targeting behavior. | 1 | `allies` (Enum) |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 | `CharmedMaggot` (Enum) |
| `alias` | Enum | Specifies an alias keyword for referencing this status effect in tooltips or logic. || `Infested` (Enum) |

</details>

### Object: `Angry`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Angry"` (Enum) |

</details>

### Object: `Antidote`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_Antidote` (Enum) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_ANTIDOTE_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `2` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `103` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_ANTIDOTE_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_common` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `Appeal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_APPEAL_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_APPEAL_DESC"` (String) |

</details>

### Object: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Flying` | Integer | The number of stacks of the Flying status effect applied to the unit. | 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `YOffset` | Number | A vertical offset multiplier used to adjust the unit's visual position on the tile. | 4 | `-.18` (String), `.35` (String) |

</details>

### Object: `Attacker`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |

</details>

### Object: `Attraction`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_ATTRACTION_NAME"` (String) |
| `name_reference_applier` | String | The localized string key for the name of the unit that applied this status effect. || `"KEYWORD_ATTRACTION_REF"` (String) |
| `tooltip_reference_applier` | String | The localized string key for the tooltip description of the unit that applied this status effect. || `"KEYWORD_ATTRACTION_DESC_REF"` (String) |
| `tooltip_stackless` | String | The localized string key for the stackless version of the status effect's tooltip. || `"KEYWORD_ATTRACTION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | The localized string key for the stackable version of the status effect's tooltip. || `"KEYWORD_ATTRACTION_DESC"` (String) |

</details>

### Object: `BagOfSeeds`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `tk_BagOfSeeds` (Enum) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_BAGOFSEEDS_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `182` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_BAGOFSEEDS_NAME"` (String) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `rare` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Druid` (Enum) |

</details>

### Object: `Basement0`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundBasement0` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `33` (Number) |

</details>

### Object: `Basement1`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundBasement1` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `33` (Number) |

</details>

### Object: `Basement2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundBasement2` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `33` (Number) |

</details>

### Object: `Basement3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundBasement3` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `33` (Number) |

</details>

### Object: `Basement4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundBasement4` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `33` (Number) |

</details>

### Object: `BasementUpgrade`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Basement0` (Enum) |

</details>

### Object: `BasementUpgrade2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `BasementUpgrade` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Basement1` (Enum) |

</details>

### Object: `BasementUpgrade3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `BasementUpgrade2` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Basement2` (Enum) |

</details>

### Object: `BasementUpgrade4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `BasementUpgrade3` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Basement3` (Enum) |

</details>

### Object: `BasementUpgrade5`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `BasementUpgrade4` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Basement4` (Enum) |

</details>

### Object: `Bear`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `BellyFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Belly"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Big`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `Big` (Enum), `"Big"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `GameteSpawn` (Enum) |
| `follow_character_tag` | Enum | The character tag this visual effect follows. | 2 | `zaratana` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `position` | Array | The 2D position (x, y) or single-coordinate value for placement. || `[4.5 4.5]` (Array) |

</details>

### Object: `BigCatnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `BigFood`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `FoodBase` (Enum) |

</details>

### Object: `BigHolding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"BigHolding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `BigHoldingCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"BigHoldingCat"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `BigScrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `BiggestFood`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `FoodBase` (Enum) |

</details>

### Object: `BirdFeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_BIRDFEED_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `191` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_BIRDFEED_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |

</details>

### Object: `BirdPoopHat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Enum / Integer | Specifies the charisma stat value as an integer or 'aux' for auxiliary stat assignment. || `-1` (Number) |
| `cursed` | Boolean | If true, the item is cursed and cannot be unequipped. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ARMOR_BIRDPOOPHAT_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `30` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `head` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ARMOR_BIRDPOOPHAT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Fecal` (Enum) |

</details>

### Object: `Bishop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Bishop"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BBXLightning` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CULTISTBISHOP_NAME"` (String), `"ITEM_BISHOP_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CULTISTBISHOP_DESC"` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `2.5` (Number) |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `tk_Bishop` (Enum) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_BISHOP_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `6` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `201` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |

</details>

### Object: `BlackBird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdSmall` (Enum) |

</details>

### Object: `BlackHole`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"BlackHole"` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"OBJECT_BLACKHOLE_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"OBJECT_BLACKHOLE_DESC"` (String) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `NeutronStar` (Enum) |

</details>

### Object: `Blessing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`intro`](Events_and_Encounters.md#object-intro) | Object | Defines the introductory sequence or dialog for an event or quest. || `{ ... }` (Object) |
| [`main`](Events_and_Encounters.md#object-main) | Object | Defines the main interaction prompt and options for an event. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `Bomb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Button` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `wp_Bomb` (Enum) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_BOMB_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `1` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `11` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `weapon` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_BOMB_NAME"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |

</details>

### Object: `BoneyardUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `Boris`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"2"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `BothObelisksUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 4 | `{ ... }` (Object) |

</details>

### Object: `Bully`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `BunkerUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `Butcher`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate SkullBash Shred Chomp Succ...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_BUTCHER0" "TEAMNAME_ADJECTIVE_BUTCHER1" "TEAMNAME_ADJECTIVE_BUTCHER2" "TEAMNAME_ADJECTIVE_BUTCHER3" "TEAMNAME_ADJECTIVE_BUTCHER4" "TEAMNAME_ADJECTIVE_BUTCHER5" "TEAMNAME_ADJECTIVE_BUTCHER6" "TEAMNAME_ADJECTIVE_BUTCHER7" "TEAMNAME_ADJECTIVE_BUTCHER8" "TEAMNAME_ADJECTIVE_BUTCHER9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicButcherMelee]` (Array) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_BUTCHER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`innate_items`](Cat_Classes.md#object-innate_items) | Object | Specifies items equipped by default on a unit, such as weapon or trinket. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[con str lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_BUTCHER_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_BUTCHER0" "TEAMNAME_NOUN_BUTCHER1" "TEAMNAME_NOUN_BUTCHER2" "TEAMNAME_NOUN_BUTCHER3" "TEAMNAME_NOUN_BUTCHER4" "TEAMNAME_NOUN_BUTCHER5" "TEAMNAME_NOUN_BUTCHER6" "TEAMNAME_NOUN_BUTCHER7" "TEAMNAME_NOUN_BUTCHER8" "TEAMNAME_NOUN_BUTCHER9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[Putrefy NeverFull MainCourse FreshMeat Masochist Glutton Hooked Stompy Barbed GrapplingHook...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[Succ HogRush Chomp BodySlam Vurp Tromp Spoil Grill Sharpen SliceAndDice]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `spell` (Enum) |

</details>

### Object: `Cat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `formchange` | Enum | Specifies the formchange name to apply when the cat is captured or present. | 6 | `SmallHoldingCat` (Enum), `BigHoldingCat` (Enum) |
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the revival or aura triggers. | 4 | `{ ... }` (Object) |
| `animation` | Enum | Specifies the animation clip to use for the ability’s meta representation. | 2 | `spawnHoldingCat` (Enum) |

</details>

### Object: `Catepillar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `Catnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_Catnip` (Enum) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. || `7` (Number) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_SMALLCATNIPBAGGY_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `1` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `22` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_SMALLCATNIPBAGGY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_common` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `CatnipBig`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_Catnip` (Enum) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. || `12` (Number) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_LARGECATNIPBAGGY_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `1` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `3` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_LARGECATNIPBAGGY_NAME"` (String) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_common` (Enum) |

</details>

### Object: `CaveBaby`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"CaveBaby"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `CaveBabyMelee` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CAVEBABY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CAVEBABY_DESC"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `CavePerson` (Enum) |

</details>

### Object: `CaveMan`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"CaveMan"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 4 | `CaveMan3HitCombo` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 | `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CAVEMANMAN_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CAVEMANMAN_DESC"` (String) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `CavePerson` (Enum) |

</details>

### Object: `CaveManSpear`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"SpearCaveMan"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 4 | `CaveManThrowSpear` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 | `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_SPEARCAVEMAN_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_SPEARCAVEMAN_DESC"` (String) |

</details>

### Object: `CaveWoman`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"CaveWoman"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `CaveWomanKick` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CAVEMANWOMAN_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CAVEMANWOMAN_DESC"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `CavePerson` (Enum) |

</details>

### Object: `CaveWomanHasCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"CatCaveWoman"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `CaveWomanCatSlap` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CAVEMANWOMAN2_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CAVEMANWOMAN2_DESC"` (String) |

</details>

### Object: `CavesUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `CerberubsJumpBlind`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 2 | `nubs_fakeblind` (Enum) |

</details>

### Object: `CerberubsJumpNormal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 2 | `default` (Enum) |

</details>

### Object: `ChaosAntennaAttached`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 | `{ ... }` (Object) |

</details>

### Object: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fear` | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 | `{ ... }` (Object) |
| `Stealth` | Array / Integer | The number of turns the unit is invisible, or [stacks, probability] of gaining stealth. | 1 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

### Object: `Charging`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `MoonHead_Blow` (Enum) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Charging"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `CharmedDip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `Dip` (Enum) |

</details>

### Object: `CharmedFloater`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `Floater` (Enum) |

</details>

### Object: `CharmedPile`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `Pile` (Enum) |

</details>

### Object: `Cherub`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdSmall` (Enum) |

</details>

### Object: `Chicken`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_Heal` (Enum) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. || `15` (Number) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_ROTISSERIECHICKEN_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `3` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `59` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_ROTISSERIECHICKEN_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_rare` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdLarge` (Enum) |

</details>

### Object: `Close`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `CloseConvert`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `MarshmallowConvert` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_close` (Enum) |

</details>

### Object: `Cockroach`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. || `[0 20]` (Array), `[10 20]` (Array) |

</details>

### Object: `Coin`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `Coin10`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `Coin` (Enum) |

</details>

### Object: `Coin2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `Coin` (Enum) |

</details>

### Object: `Coin3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `Coin` (Enum) |

</details>

### Object: `Coin4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `Coin` (Enum) |

</details>

### Object: `Colorless`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[Block Rest Brace Roll SharpenClaws Reach ManaDrain SoothingGlow Ponder Brainstorm...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_COLORLESS0" "TEAMNAME_ADJECTIVE_COLORLESS1" "TEAMNAME_ADJECTIVE_COLORLESS2"]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicMelee BasicMelee BasicShortRanged BasicShortLobbed]` (Array) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[str dex con int spd cha lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `move_pool` | Array | The list of move ability names available for random selection during level-up or generation. || `[DefaultMove]` (Array) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_COLORLESS0" "TEAMNAME_NOUN_COLORLESS1" "TEAMNAME_NOUN_COLORLESS2"]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[SelfAssured LuckDrain Infested Worms Amped Furious MetalDetector DeathProof Leader Mange...]` (Array) |
| `tutorial_levelup_active_pool` | Array | The list of active ability names shown during tutorial level-ups. || `[Block LickHeal Dump]` (Array) |
| `tutorial_levelup_active_pool_2` | Array | The secondary list of active ability names shown during tutorial level-ups. || `[GainThorns ButtScoot Burst HireHitman]` (Array) |
| `tutorial_levelup_passive_pool` | Array | The list of passive ability names shown during tutorial level-ups. || `[Furious PressurePoints LateBloomer ZenkaiBoost]` (Array) |

</details>

### Object: `Comfort`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_COMFORT_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_COMFORT_DESC"` (String) |

</details>

### Object: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

</details>

### Object: `Conditional_FinishedSpawning`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Imprison` | Enum | Specifies the unit name to be imprisoned by the status effect. | 2 | `Fly` (Enum), `BeefyCharmedLeech` (Enum) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

</details>

### Object: `CoreObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 | `{ ... }` (Object) |

</details>

### Object: `CoreUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `CraterUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](Map_Generation_and_Routing.md#object-exit1) | Object | Defines the properties of the second exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `Cultist`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Cultist"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BasicMelee` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CULTISTLACKEY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CULTISTLACKEY_DESC"` (String) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `Damaged`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |

</details>

### Object: `DashRandomly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 4 | `ShamblerDash` (Enum) |
| `decision_weights` | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 4 | `blind` (Enum) |

</details>

### Object: `DeadHummingbird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_EatHummingbird` (Enum) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. || `20` (Number) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_DEADHUMMINGBIRD_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `2` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `245` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_DEADHUMMINGBIRD_NAME"` (String) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_very_rare` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Feathered` (Enum) |

</details>

### Object: `Default`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 54 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 20 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 4 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `LennyShove` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `LennyTrampleMove` (Enum) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `""` (String) |
| `set_house` | Enum | Specifies which house type to set for the upgrade. | 2 | `House1` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Floor1_Large` (Enum) |

</details>

### Object: `Default_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Default_Ground`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `DemonicGlyph_Bite`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_TOR_BITE_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_TOR_BITE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Bounce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_TOR_BOUNCE_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_TOR_BOUNCE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Fire`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_TOR_FIRE_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_TOR_FIRE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Movement`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_TOR_MOVE_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_TOR_MOVE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Summon`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_TOR_SUMMON_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_TOR_SUMMON_DESC"` (String) |

</details>

### Object: `DesireMech`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |

</details>

### Object: `Die`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Maps keyword identifiers to their tooltip override values for display. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `DimensionXUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 4 | `{ ... }` (Object) |

</details>

### Object: `Dove`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdSmall` (Enum) |

</details>

### Object: `Down`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"Down"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `ButtFart` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `TeleportFlipUp` (Enum) |

</details>

### Object: `Druid`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[ManaBomb SongOfSpring GrantLife SquirrelSquad SummonSquirrel DruidSwap BattleCry SummonSnake SummonTurtle SummonToad...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_DRUID0" "TEAMNAME_ADJECTIVE_DRUID1" "TEAMNAME_ADJECTIVE_DRUID2" "TEAMNAME_ADJECTIVE_DRUID3" "TEAMNAME_ADJECTIVE_DRUID4" "TEAMNAME_ADJECTIVE_DRUID5" "TEAMNAME_ADJECTIVE_DRUID6" "TEAMNAME_ADJECTIVE_DRUID7" "TEAMNAME_ADJECTIVE_DRUID8" "TEAMNAME_ADJECTIVE_DRUID9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicDruidAbility]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_DRUID_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | Specifies passive abilities that are permanently granted to the unit. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[cha int str]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_DRUID_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_DRUID0" "TEAMNAME_NOUN_DRUID1" "TEAMNAME_NOUN_DRUID2" "TEAMNAME_NOUN_DRUID3" "TEAMNAME_NOUN_DRUID4" "TEAMNAME_NOUN_DRUID5" "TEAMNAME_NOUN_DRUID6" "TEAMNAME_NOUN_DRUID7" "TEAMNAME_NOUN_DRUID8" "TEAMNAME_NOUN_DRUID9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[SuperCrow NaturesGuidance PoisonIvy Pathfinder EmptyVessels WildAnimals BarkSkin SoothingSong Teamwork Bouquet...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[SummonSquirrel SummonToad Encourage Protection SongOfSpring BattleCry SafetyDance TigerForm RhinoForm InspirationalSong]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Drunker`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Drunk` (Enum) |

</details>

### Object: `DualSword`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"2"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 2 | `1.5` (Number) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |

</details>

### Object: `DualSword_Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Holy2"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 2 | `1.5` (Number) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |

</details>

### Object: `Dumb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Maps keyword identifiers to their tooltip override values for display. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `DybbukPossessed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit_ability` | Enum | Specifies the ability used to exit the possession state. | 2 | `DybbukReturn` (Enum) |
| `punch_self_ability` | Enum | Specifies the ability that makes the possessed unit attack itself. | 2 | `Dybbuk_StopHittingYourself` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_DYBBUKED_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_DYBBUKED_DESC"` (String) |

</details>

### Object: `Eagle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdLarge` (Enum) |

</details>

### Object: `Earth`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | The damage dealt, which can be a numeric value, a formula string, or a defined damage object. | 4 | `X` (Equation) |

</details>

### Object: `Electric`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. || `[1 .1]` (Array), `[1 .1*X]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

### Object: `Empty`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `""` (String) |

</details>

### Object: `EndOfTimeUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 4 | `{ ... }` (Object) |

</details>

### Object: `Escape`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 4 | `DybbukEscape` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 | `keep_distance_always_move` (Enum) |

</details>

### Object: `EventBounty`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_EVENTBOUNTY_NAME"` (String) |
| `tooltip_stacks` | String | The localized string key for the stackable version of the status effect's tooltip. || `"KEYWORD_EVENTBOUNTY_DESC"` (String) |

</details>

### Object: `Evolution`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_EVOLUTION_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_EVOLUTION_DESC"` (String) |

</details>

### Object: `EvolveAbilityFromPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 26 | `Fighter` (Enum), `Thief` (Enum) |
| `upgraded` | Boolean | If true, the ability evolution uses an upgraded version or state instead of the base one. | 26 | `true` (Boolean) |

</details>

### Object: `Explody`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Expl` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `ToxExplode` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Explosive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"3"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `FightPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `T3Shoot` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `FloatMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Fighter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[Spin Dash FirePunch IcePunch ThunderPunch FurySwipes SideSlash FighterLeap Uppercut Counter...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_FIGHTER0" "TEAMNAME_ADJECTIVE_FIGHTER1" "TEAMNAME_ADJECTIVE_FIGHTER2" "TEAMNAME_ADJECTIVE_FIGHTER3" "TEAMNAME_ADJECTIVE_FIGHTER4" "TEAMNAME_ADJECTIVE_FIGHTER5" "TEAMNAME_ADJECTIVE_FIGHTER6" "TEAMNAME_ADJECTIVE_FIGHTER7" "TEAMNAME_ADJECTIVE_FIGHTER8" "TEAMNAME_ADJECTIVE_FIGHTER9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicMelee_Fighter]` (Array) |
| `complicated_abilities` | Array | The list of ability names that have complex logic and may be hidden from simplified views. || `[FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooHard Zoomzerk Bloodzerk ExhaustingBlow ChaosRampage...]` (Array) |
| `complicated_passives` | Array | The list of passive names that have complex logic and may be hidden from simplified views. || `[ShoulderCheck DumbMuscle ThickSkull MostValuableCat HitMe]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_FIGHTER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[str con spd]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_FIGHTER_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_FIGHTER0" "TEAMNAME_NOUN_FIGHTER1" "TEAMNAME_NOUN_FIGHTER2" "TEAMNAME_NOUN_FIGHTER3" "TEAMNAME_NOUN_FIGHTER4" "TEAMNAME_NOUN_FIGHTER5" "TEAMNAME_NOUN_FIGHTER6" "TEAMNAME_NOUN_FIGHTER7" "TEAMNAME_NOUN_FIGHTER8" "TEAMNAME_NOUN_FIGHTER9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[BloodLust Avenger Scars FasterWhenHit KillsHeal Vengeful HamsterStyle WeaponMaster ShoulderCheck SkullSmash...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `shield` | Enum / Integer | The unit's shield value, specified as an integer or a formula. || `[1 .5]` (Array), `4` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[FurySwipes Dash Spin Confront FirePunch SideSlash Exert Berserk Stick Counter]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Fire`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `SpewerLobbed_Lava` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `FireFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Full` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `SpewerSpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `combo` | Array | Defines a sequence of visual effect names to play in order for a particle or animation combo. || `[FireSmoke FirePlumes FireWaves FireBase FireWhites]` (Array) |

</details>

### Object: `Firefly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. || `[0 2]` (Array) |

</details>

### Object: `FloatingDebris`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. | 1 | `20` (Number) |

</details>

### Object: `Floor1_Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame name used for interstitial room transition screens. | 2 | `room1` (Enum) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. | 2 | `RoomBackgroundLargeF1` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. | 2 | `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. | 2 | `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. | 2 | `16` (Number) |

</details>

### Object: `Floor1_Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame name used for interstitial room transition screens. | 2 | `room2` (Enum) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. | 2 | `RoomBackgroundSmallF1` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. | 2 | `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. | 2 | `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. | 2 | `16` (Number) |

</details>

### Object: `Floor2_Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame name used for interstitial room transition screens. || `room3` (Enum) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundLargeF2` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `16` (Number) |

</details>

### Object: `Floor2_Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame name used for interstitial room transition screens. || `room4` (Enum) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundSmallF2` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `16` (Number) |

</details>

### Object: `Flop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Down"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Flop2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Down"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Flush`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `spell` (Enum) |

</details>

### Object: `FlushBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `FlushHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Host` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `FlushNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Fly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. || `[0 20]` (Array), `[10 20]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_FLY_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_FLY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `Food`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | If true, duplicate items can appear in selection or generation pools. | 4 | `true` (Boolean) |
| `amount` | Array | A scalar value for the strength or intensity of an ambient effect, or a percentage range. | 4 | `10` (Number) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. | 4 | `5` (Number) |
| `weight` | Number | A multiplier or probability weight for selection, relative to other options. | 2 | `5` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `FoodBase` (Enum) |

</details>

### Object: `FoodBig`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_Heal` (Enum) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. || `24` (Number) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_CATFOOD_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `1` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `2` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_CATFOOD_NAME"` (String) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_common` (Enum) |

</details>

### Object: `FoodMedium`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_Heal` (Enum) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. || `12` (Number) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_ASNACK_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `1` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `21` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_ASNACK_NAME"` (String) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_common` (Enum) |

</details>

### Object: `FoodMove`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `CaveBabyFoodMove` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_close_move_if_possible` (Enum) |

</details>

### Object: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean | If true, the option has no cost and can be chosen freely; or specifies an object for free options. | 2 | `false` (Boolean) |

</details>

### Object: `ForceTrample`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `BirthwortTrample` (Enum) |
| `decision_weights` | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 2 | `always_cast_careless` (Enum) |

</details>

### Object: `FreeSpell`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_FREESPELL_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_FREESPELL_DESC"` (String) |

</details>

### Object: `Full`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"Full"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 4 | `KirbySpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 | `{ ... }` (Object) |
| [`statuses_on_enter_form`](Characters_and_Bosses.md#object-statuses_on_enter_form) | Object | Defines status effects or abilities to apply upon entering this form. | 4 | `{ ... }` (Object) |

</details>

### Object: `FutureUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 | `{ ... }` (Object) |

</details>

### Object: `GenFlag_Boss_Spewer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](Combat_Rewards.md#object-boss) | Object | Configures boss encounter properties, including type, rewards, and cutscene. | 2 | `{ ... }` (Object) |

</details>

### Object: `GenFlag_Boss_Stacy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](Combat_Rewards.md#object-boss) | Object | Configures boss encounter properties, including type, rewards, and cutscene. | 2 | `{ ... }` (Object) |
| [`miniboss_event`](Map_Generation_and_Routing.md#object-miniboss_event) | Object | Defines a miniboss event node, specifying its type and level. | 2 | `{ ... }` (Object) |

</details>

### Object: `GlowingSeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_GLOWINGSEED_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `71` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_GLOWINGSEED_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |

</details>

### Object: `GoldenEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_GOLDENEGG_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `190` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_GOLDENEGG_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |

</details>

### Object: `Grass`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |

</details>

### Object: `Gravity`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `Grown`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Grown` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `HitlerCloneSwipes` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_HITLERCLONE_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `1.5` (Number) |
| `weak_threshold` | Integer | The health threshold below which the unit is considered 'weak' for mechanics. | 2 | `15` (Number) |

</details>

### Object: `GuaranteedJackpot`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Guarding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Guarding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `HalfDead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"2"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `RatKingDash` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `HardPathUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](Map_Generation_and_Routing.md#object-hard_initial) | Object | Defines initial properties for the hard path node, such as type and locked state. | 4 | `{ ... }` (Object) |

</details>

### Object: `Harpy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdLarge` (Enum) |

</details>

### Object: `HarpysClaw`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `wp_HarpyClaw` (Enum) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_HARPYSCLAW_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `199` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `weapon` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_HARPYSCLAW_NAME"` (String) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `very_rare` (Enum) |

</details>

### Object: `HasCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 10 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 10 | `LennyCatSlap` (Enum), `MoonHandSqueeze` (Enum) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 8 | `"Grabbing"` (Enum), `"Cat"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 8 | `{ ... }` (Object) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Swallowed"` (Enum) |

</details>

### Object: `HasDeadCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"CatDead"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `LennyCatSlap` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `HasRock`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"rock"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `AmoebaRockBash` (Enum) |

</details>

### Object: `Headless`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Headless"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `HealRandomInjury`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the elite buff's icon. || `158` (Number) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_HEALRANDOMINJURY_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_HEALRANDOMINJURY_DESC"` (String) |

</details>

### Object: `Health`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_HEALTH_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_HEALTH_DESC"` (String) |

</details>

### Object: `Hint_CrackedVisuals`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Cracked"` (Enum) |

</details>

### Object: `Hint_CrackedVisuals2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"ChargingCracked"` (Enum) |

</details>

### Object: `Hint_CrackedVisuals3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"SwallowedCracked"` (Enum) |

</details>

### Object: `Holding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Holding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Holy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatLeech` | Integer | The amount of flat health restored per hit (leech). | 4 | `X` (Enum), `10` (Number), `1` (Number) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"1"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `House1`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](House_and_Environment.md#object-aux_positions) | Object | Maps auxiliary object names to their [x, y] coordinates in the house scene. | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum | Specifies which placement frame to use for background decorations in the house. | 2 | `small` (Enum) |
| `movieclip_bg` | Enum | Specifies the movieclip identifier for the house background layer. | 2 | `HouseBackground1` (Enum) |
| `movieclip_fg` | Enum | Specifies the movieclip identifier for the house foreground layer. | 2 | `HouseForeground1` (Enum) |
| [`room_positions`](House_and_Environment.md#object-room_positions) | Object | Maps room names to their [x, y] grid positions within the house layout. | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String | The volume level for cat sounds when the camera is zoomed out, as a float. | 2 | `.8` (String) |

</details>

### Object: `House2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](House_and_Environment.md#object-aux_positions) | Object | Maps auxiliary object names to their [x, y] coordinates in the house scene. | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum | Specifies which placement frame to use for background decorations in the house. | 2 | `large` (Enum) |
| `movieclip_bg` | Enum | Specifies the movieclip identifier for the house background layer. | 2 | `HouseBackground2` (Enum) |
| `movieclip_fg` | Enum | Specifies the movieclip identifier for the house foreground layer. | 2 | `HouseForeground2` (Enum) |
| [`room_positions`](House_and_Environment.md#object-room_positions) | Object | Maps room names to their [x, y] grid positions within the house layout. | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String | The volume level for cat sounds when the camera is zoomed out, as a float. | 2 | `.7` (String) |

</details>

### Object: `House3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](House_and_Environment.md#object-aux_positions) | Object | Maps auxiliary object names to their [x, y] coordinates in the house scene. | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum | Specifies which placement frame to use for background decorations in the house. | 2 | `large` (Enum) |
| `movieclip_bg` | Enum | Specifies the movieclip identifier for the house background layer. | 2 | `HouseBackground3` (Enum) |
| `movieclip_fg` | Enum | Specifies the movieclip identifier for the house foreground layer. | 2 | `HouseForeground3` (Enum) |
| [`room_positions`](House_and_Environment.md#object-room_positions) | Object | Maps room names to their [x, y] grid positions within the house layout. | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String | The volume level for cat sounds when the camera is zoomed out, as a float. | 2 | `.6` (String) |

</details>

### Object: `HumanDead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `DH` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `HCSpin` (Enum) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_HUMANCAT2_DESC"` (String) |

</details>

### Object: `HummingBird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdSmall` (Enum) |

</details>

### Object: `Hunter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[LineShot SpawnMaggotFriend SpawnPooterFriend Marked HailOfNails ScatterShot BrambleShot BearTrap TwinShot CrossShot...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_HUNTER0" "TEAMNAME_ADJECTIVE_HUNTER1" "TEAMNAME_ADJECTIVE_HUNTER2" "TEAMNAME_ADJECTIVE_HUNTER3" "TEAMNAME_ADJECTIVE_HUNTER4" "TEAMNAME_ADJECTIVE_HUNTER5" "TEAMNAME_ADJECTIVE_HUNTER6" "TEAMNAME_ADJECTIVE_HUNTER7" "TEAMNAME_ADJECTIVE_HUNTER8" "TEAMNAME_ADJECTIVE_HUNTER9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicRanged_Hunter]` (Array) |
| `complicated_abilities` | Array | The list of ability names that have complex logic and may be hidden from simplified views. || `[Extend LastHit StakeOut Diversion ScoutMe CraftArrow BounceShot Vivisect SlopThePigs SpiderInjector...]` (Array) |
| `complicated_passives` | Array | The list of passive names that have complex logic and may be hidden from simplified views. || `[Hazardous Traps CatchProjectiles Host SleepDarts Survivalist]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_HUNTER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[dex spd int]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_HUNTER_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_HUNTER0" "TEAMNAME_NOUN_HUNTER1" "TEAMNAME_NOUN_HUNTER2" "TEAMNAME_NOUN_HUNTER3" "TEAMNAME_NOUN_HUNTER4" "TEAMNAME_NOUN_HUNTER5" "TEAMNAME_NOUN_HUNTER6" "TEAMNAME_NOUN_HUNTER7" "TEAMNAME_NOUN_HUNTER8" "TEAMNAME_NOUN_HUNTER9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[TakeAim HuntersBoon BroodMother TaintedMother Quiver SplitShot Hazardous ThornArrows Traps CatchProjectiles...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[SpawnPooterFriend BrambleShot SpawnBaitTrap BearTrap TerrainWalk NeedleShot ScatterShot Marked FleaShot HeavyShot]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Ice`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of turns of Slow applied, or an array with duration and chance. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `IceAgeUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 | `{ ... }` (Object) |

</details>

### Object: `InitialPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `T3Shoot` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `FloatMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Insane_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Insane"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Insane_Ground`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Insane"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Item`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. | 21 | `15` (Number), `5` (Number) |
| `pool` | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 18 | `[TutorialStick]` (Array), `[WaterBottle_Half]` (Array), `treasure_easy` (Enum), `rare` (Enum) |
| `mandatory` | Boolean | If true, the item or reward is guaranteed and cannot be skipped. | 14 | `true` (Boolean) |
| `weight` | Number | A multiplier or probability weight for selection, relative to other options. | 2 | `1` (Number) |

</details>

### Object: `Jack_Gainaltfurniture`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | String | The dialog string identifier to display for this sequence step. | 16 | `NPC_JACK_JACK_GAINALTFURNITURE_4` (String), `NPC_JACK_JACK_GAINALTFURNITURE_2` (String) |
| `set_state` | Enum | Specifies the state or pose to set for a character in the sequence. | 8 | `closeup` (Enum), `blocking` (Enum) |
| `lock_controls` | Number | Specifies the duration in seconds to lock player controls during a sequence. | 2 | `1` (Number) |
| `unlock_controls` | Number | A flag (1 to enable) that unlocks player controls at this point in a sequence. | 2 | `1` (Number) |

</details>

### Object: `Jester`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[SmartMetronome RNGCannon Bump PowerUp]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_JESTER0" "TEAMNAME_ADJECTIVE_JESTER1" "TEAMNAME_ADJECTIVE_JESTER2" "TEAMNAME_ADJECTIVE_JESTER3" "TEAMNAME_ADJECTIVE_JESTER4" "TEAMNAME_ADJECTIVE_JESTER5" "TEAMNAME_ADJECTIVE_JESTER6" "TEAMNAME_ADJECTIVE_JESTER7" "TEAMNAME_ADJECTIVE_JESTER8" "TEAMNAME_ADJECTIVE_JESTER9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicMelee_Fighter BasicRanged_Hunter BasicMagicShortRanged BasicTankMelee BasicStraightShot_Thief BasicMedicMelee BasicButcherMelee BasicPsychicPull BasicNecroRanged]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_JESTER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[str dex con int spd cha lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_JESTER_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_JESTER0" "TEAMNAME_NOUN_JESTER1" "TEAMNAME_NOUN_JESTER2" "TEAMNAME_NOUN_JESTER3" "TEAMNAME_NOUN_JESTER4" "TEAMNAME_NOUN_JESTER5" "TEAMNAME_NOUN_JESTER6" "TEAMNAME_NOUN_JESTER7" "TEAMNAME_NOUN_JESTER8" "TEAMNAME_NOUN_JESTER9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[SuperLuck Goofball]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Johnny`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `JohnnyBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `JohnnyHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Host` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `JohnnyNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Joystick`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Joystick"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `JunkyardUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](Map_Generation_and_Routing.md#object-exit1) | Object | Defines the properties of the second exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `JurassicUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `LargeAttic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `built_in_collision` | Array | An array defining the collision geometry for the room, typically as a list of vertices or shapes. || `[[ 6 6 6 6 6 6 6 6 6...]` (Array) |
| `extra_bound_planes` | Array | An array defining additional collision planes that bound the room's playable area. || `[{ p [ 0 0 ] n [ 1 -2...]` (Array) |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). || `9` (Number) |
| `id` | Enum | Specifies the unique identifier for the object or room, used for referencing or categorization. || `Attic` (Enum) |
| `interstitial_bg_frame` | Enum | Specifies the background frame name used for interstitial room transition screens. || `attic` (Enum) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RoomBackgroundAttic` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| `width` | Number | The width of the room in grid tiles. || `35` (Number) |

</details>

### Object: `LargeBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `LargeHouse`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `MediumHouse` (Enum) |
| `set_house` | Enum | Specifies which house type to set for the upgrade. | 2 | `House3` (Enum) |

</details>

### Object: `LargeHouse_Floor2Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Floor2_Large` (Enum) |

</details>

### Object: `LargeHouse_Floor2Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Floor2_Small` (Enum) |

</details>

### Object: `LastHit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `lobbed_attack` (Enum) |

</details>

### Object: `LeapClose`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `GKLeap` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `towards_aggro` (Enum) |

</details>

### Object: `Leave`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `leave` (Enum) |

</details>

### Object: `LevelUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. | 3 | `10` (Number) |

</details>

### Object: `Lifted`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Lift"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Lighting`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient` | String | The ambient light intensity multiplier for the lighting setup, typically between 0 and 1. | 10 | `.6` (String), `.8` (String) |
| `smallray_clip` | Enum | Determines which light clip or mask texture to use for small ray lighting effects. | 2 | `labligtht` (Enum), `Bunkerlight` (Enum) |
| `bigrays` | Array | An array controlling big ray lighting, typically [intensity, count] or similar. || `[0 0]` (Array), `[1 1]` (Array) |
| `smallrays` | Array | An array controlling small ray lighting, typically [intensity, count] or similar. || `[0 0]` (Array), `[4 8]` (Array) |

</details>

### Object: `Lit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Lit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `LostSoul`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ARMOR_LOSTSOUL_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `180` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `neck` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ARMOR_LOSTSOUL_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `very_rare` (Enum) |

</details>

### Object: `Mage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[Surf Bolt Fireball FreezeRay MagicMissile Blast WallOfFire HyperBeam MeteorStorm MegaBlast...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_MAGE0" "TEAMNAME_ADJECTIVE_MAGE1" "TEAMNAME_ADJECTIVE_MAGE2" "TEAMNAME_ADJECTIVE_MAGE3" "TEAMNAME_ADJECTIVE_MAGE4" "TEAMNAME_ADJECTIVE_MAGE5" "TEAMNAME_ADJECTIVE_MAGE6" "TEAMNAME_ADJECTIVE_MAGE7" "TEAMNAME_ADJECTIVE_MAGE8" "TEAMNAME_ADJECTIVE_MAGE9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicMagicShortRanged]` (Array) |
| `complicated_abilities` | Array | The list of ability names that have complex logic and may be hidden from simplified views. || `[DealWithTheDevil ForbiddenFlame ForbiddenFlood ForbiddenFulmination Corrupt FireSurge IceSurge LightningSurge Creshendo Divide...]` (Array) |
| `complicated_passives` | Array | The list of passive names that have complex logic and may be hidden from simplified views. || `[ElementalAttunement LatentEnergy MagicGuru One Two Four Five]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_MAGE_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[int cha dex]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_MAGE_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_MAGE0" "TEAMNAME_NOUN_MAGE1" "TEAMNAME_NOUN_MAGE2" "TEAMNAME_NOUN_MAGE3" "TEAMNAME_NOUN_MAGE4" "TEAMNAME_NOUN_MAGE5" "TEAMNAME_NOUN_MAGE6" "TEAMNAME_NOUN_MAGE7" "TEAMNAME_NOUN_MAGE8"]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[Micronaps HolyMantel Shrapnel BurningPaws LightningPaws IcePaws PawMissile Overload ChargeUp Recharged...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[MagicMissile Fireball FreezeRay Warp Surf WindSlash Absorb Bolt Inspire MegaBlast]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `MagicSeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_MAGICSEED_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `113` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_MAGICSEED_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |

</details>

### Object: `MeatWorldUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 4 | `{ ... }` (Object) |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 4 | `{ ... }` (Object) |

</details>

### Object: `MeatWorldUnlockedFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](Map_Generation_and_Routing.md#object-mw_battle1) | Object | Defines a battle node on the Meat World map, with properties like type, hidden status, and music override. | 2 | `{ ... }` (Object) |
| [`mw_boss`](Map_Generation_and_Routing.md#object-mw_boss) | Object | Defines a boss encounter node on the Meat World map, with properties for cutscene and music. | 2 | `{ ... }` (Object) |
| [`mw_earlyhome`](Map_Generation_and_Routing.md#object-mw_earlyhome) | Object | Defines an early home node on the Meat World map, typically hidden or used for early access. | 2 | `{ ... }` (Object) |
| [`mw_event1`](Map_Generation_and_Routing.md#object-mw_event1) | Object | Defines an event node on the Meat World map, with properties like type and hidden status. | 2 | `{ ... }` (Object) |
| [`mw_hard1`](Map_Generation_and_Routing.md#object-mw_hard1) | Object | Defines a hard difficulty battle node on the Meat World map, with optional music layer override. | 2 | `{ ... }` (Object) |
| [`mw_home`](Map_Generation_and_Routing.md#object-mw_home) | Object | Defines a home node on the Meat World map, with properties for type and visibility. | 2 | `{ ... }` (Object) |
| [`mw_quest_event`](Map_Generation_and_Routing.md#object-mw_quest_event) | Object | Defines a quest event node on the Meat World map, with overrides for level and art. | 2 | `{ ... }` (Object) |
| [`mw_treasure`](Map_Generation_and_Routing.md#object-mw_treasure) | Object | Defines a treasure node on the Meat World map, with type and hidden status. | 2 | `{ ... }` (Object) |

</details>

### Object: `MedBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `MedCatnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `MedScrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `Medic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[RangedHeal MeleeHeal Malaise OpenWounds Prayer Convert Cleanse HereticMark Zealot Haste...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_MEDIC0" "TEAMNAME_ADJECTIVE_MEDIC1" "TEAMNAME_ADJECTIVE_MEDIC2" "TEAMNAME_ADJECTIVE_MEDIC3" "TEAMNAME_ADJECTIVE_MEDIC4" "TEAMNAME_ADJECTIVE_MEDIC5" "TEAMNAME_ADJECTIVE_MEDIC6" "TEAMNAME_ADJECTIVE_MEDIC7" "TEAMNAME_ADJECTIVE_MEDIC8" "TEAMNAME_ADJECTIVE_MEDIC9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicMedicMelee]` (Array) |
| `complicated_abilities` | Array | The list of ability names that have complex logic and may be hidden from simplified views. || `[OpenWounds WitchHunt Adoubement DivineProtection ChosenWarrior SwiftSanctify DivineGift HolyWeapon GetDown Rebuke...]` (Array) |
| `complicated_passives` | Array | The list of passive names that have complex logic and may be hidden from simplified views. || `[RangedMedic ThouShaltNotKill BlessingOfHolyFire BlessingOfSpirit]` (Array) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[cha int con]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_MEDIC0" "TEAMNAME_NOUN_MEDIC1" "TEAMNAME_NOUN_MEDIC2" "TEAMNAME_NOUN_MEDIC3" "TEAMNAME_NOUN_MEDIC4" "TEAMNAME_NOUN_MEDIC5" "TEAMNAME_NOUN_MEDIC6" "TEAMNAME_NOUN_MEDIC7" "TEAMNAME_NOUN_MEDIC8" "TEAMNAME_NOUN_MEDIC9"]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[HealingAura NaturalHealer Eternal Blessed EvilPatron AngelicInspiration TopOff SharingIsCaring Caretaker MoraleBoost...]` (Array) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[RangedHeal Rally Prayer FriendOrFoe HolyWeapon Zealot OpenWounds RallyCharge HallowedGround Cleanse]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `MediumHouse`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `Default` (Enum) |
| `set_house` | Enum | Specifies which house type to set for the upgrade. | 2 | `House2` (Enum) |

</details>

### Object: `MediumHouse_SmallRoom`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Floor1_Small` (Enum) |

</details>

### Object: `Monk`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[Propell Hadouken Cartwheel StoneFists Transcend HipToss Bruise Slapback Finisher Reverberate...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_MONK0" "TEAMNAME_ADJECTIVE_MONK1" "TEAMNAME_ADJECTIVE_MONK2" "TEAMNAME_ADJECTIVE_MONK3" "TEAMNAME_ADJECTIVE_MONK4" "TEAMNAME_ADJECTIVE_MONK5" "TEAMNAME_ADJECTIVE_MONK6" "TEAMNAME_ADJECTIVE_MONK7" "TEAMNAME_ADJECTIVE_MONK8" "TEAMNAME_ADJECTIVE_MONK9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicMonkMelee]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_MONK_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`innate_items`](Cat_Classes.md#object-innate_items) | Object | Specifies items equipped by default on a unit, such as weapon or trinket. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | Specifies passive abilities that are permanently granted to the unit. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[int str lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_MONK_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_MONK0" "TEAMNAME_NOUN_MONK1" "TEAMNAME_NOUN_MONK2" "TEAMNAME_NOUN_MONK3" "TEAMNAME_NOUN_MONK4" "TEAMNAME_NOUN_MONK5" "TEAMNAME_NOUN_MONK6" "TEAMNAME_NOUN_MONK7" "TEAMNAME_NOUN_MONK8" "TEAMNAME_NOUN_MONK9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[SafeSwitching Mixup Turnabout MonkeyStyle BrickSkin JaggedEdges MindBreaker CobraStyle Tenderize LongArms...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[Propell Pogo ComboThrow ComboPull Bruise Anneal Hadouken ReallyFastRun Finisher UnbridledHits]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `MoonObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 | `{ ... }` (Object) |

</details>

### Object: `MoonUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `Mounted`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Cat"` (Enum) |

</details>

### Object: `MouthFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"MouthFull"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `MoveAway`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 8 | `ExtraMove` (Enum), `MoveTwoCantrip` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 8 | `stay_far` (Enum), `keep_distance_always_move` (Enum) |

</details>

### Object: `MoveCenter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 4 | `move` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 | `stay_near_map_center` (Enum) |

</details>

### Object: `MoveClose`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 8 | `move` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 8 | `stay_close_avoid_allies` (Enum), `stay_close_always_move` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 6 | `Spin_Enemy` (Enum), `attack` (Enum) |

</details>

### Object: `MoveForBarrage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `ZaratanaVSBombardment` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_far` (Enum) |

</details>

### Object: `MoveForDash`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `attack` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveForGrass`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `StegoGrassStomp` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `StegoEatGrass` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `minimum_move` (Enum) |

</details>

### Object: `MoveForPounce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `attack` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveForSpin`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `PyrophinaVSRun` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `PyrophinaVSSpinThrow` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_close` (Enum) |

</details>

### Object: `MoveForThrow`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 4 | `move` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 4 | `PyrophinaVSCatThrow` (Enum), `PyrophinaSoloCatThrow` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 | `util_minmove` (Enum) |

</details>

### Object: `MoveOneForPuke`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `AlienBeastMoveOne` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `AlienBeastPuke` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveSpaced`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `move` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `terminator_keep_distance_always_move` (Enum) |

</details>

### Object: `MoveToHead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `G3RunToHead` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `G3GrabHead` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `minimum_move` (Enum) |

</details>

### Object: `MoveTowards`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `attack` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_close` (Enum) |

</details>

### Object: `Mutant`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Mutant"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BBMutantSwipe` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 2 | `.5` (String) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CULTISTMUTANT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CULTISTMUTANT_DESC"` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdMed` (Enum) |

</details>

### Object: `NCGravecrawlFAR`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `NCGravecrawl` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_far` (Enum) |

</details>

### Object: `Necromancer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[MaggotArmy Reanimate Rebirth Pestilence Weakness SoulSuck EvilIncarnate SoulLink WeAreOne BloodRain...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_NECROMANCER0" "TEAMNAME_ADJECTIVE_NECROMANCER1" "TEAMNAME_ADJECTIVE_NECROMANCER2" "TEAMNAME_ADJECTIVE_NECROMANCER3" "TEAMNAME_ADJECTIVE_NECROMANCER4" "TEAMNAME_ADJECTIVE_NECROMANCER5" "TEAMNAME_ADJECTIVE_NECROMANCER6" "TEAMNAME_ADJECTIVE_NECROMANCER7" "TEAMNAME_ADJECTIVE_NECROMANCER8" "TEAMNAME_ADJECTIVE_NECROMANCER9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicNecroRanged]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_NECROMANCER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[dex cha con]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_NECROMANCER_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_NECROMANCER0" "TEAMNAME_NOUN_NECROMANCER1" "TEAMNAME_NOUN_NECROMANCER2" "TEAMNAME_NOUN_NECROMANCER3" "TEAMNAME_NOUN_NECROMANCER4" "TEAMNAME_NOUN_NECROMANCER5" "TEAMNAME_NOUN_NECROMANCER6" "TEAMNAME_NOUN_NECROMANCER7" "TEAMNAME_NOUN_NECROMANCER8" "TEAMNAME_NOUN_NECROMANCER9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[Vampirism OneWithNothing BedBugs WormLord InfiniteRebirth SacrificialLamb DeathIncarnate OffloadPain CambionConception Leechmother...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[SoulLink Reanimate Rebirth CarrionShot Pestilence BloodGeyser MaggotArmy Gravecrawl FullMoon CoffinFlop]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `NeutronStar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `NoEyes`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"0"` (Enum) |

</details>

### Object: `NoStick`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `ManglerJab` (Enum) |

</details>

### Object: `NonCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `formchange` | Enum | Specifies the formchange name to apply when the cat is captured or present. | 6 | `SmallHolding` (Enum), `BigHolding` (Enum) |
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the revival or aura triggers. | 4 | `{ ... }` (Object) |
| `animation` | Enum | Specifies the animation clip to use for the ability’s meta representation. | 2 | `spawnHolding` (Enum) |

</details>

### Object: `Normal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 20 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 10 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 4 | `TinaBasicBigMeleeA` (Enum), `SpewerLobbed_Normal` (Enum) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Up"` (Enum) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `NormalFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Full` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `SpewerSpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `NotPriming`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 4 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Nothing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum | Specifies the animation clip to use for the ability’s meta representation. | 2 | `spawn` (Enum) |

</details>

### Object: `Nuke`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Nuke` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ARMOR_NUKE_DESC"` (String) |
| `failable` | Boolean | If true, the nuclear device's effect can fail to trigger. || `true` (Boolean) |
| `frame` | Integer | The sprite frame index used for this arm. || `77` (Number) |
| `hint_destination` | Enum | Specifies the destination key or name that the item gives a hint towards. || `endoftime` (Enum) |
| `indestructible` | Boolean | If true, the object cannot be destroyed by any means. || `true` (Boolean) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `neck` (Enum) |
| `legacy_quest` | Boolean | If true, this item is tied to a legacy quest system. || `true` (Boolean) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ARMOR_NUKE_NAME"` (String) |
| `quest_item` | Boolean | If true, the item is a critical quest item that cannot be discarded or destroyed. || `true` (Boolean) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `quest` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Radioactive` (Enum) |
| `shield` | Enum / Integer | The unit's shield value, specified as an integer or a formula. || `[1 .5]` (Array), `10` (Number) |
| `spd` | Enum / Integer | The speed stat value or modifier for the unit. || `-2` (Number) |

</details>

### Object: `Obey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Maps keyword identifiers to their tooltip override values for display. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Off`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Off` (Enum) |

</details>

### Object: `OffMap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 6 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `OffScreen`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `OneAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 6 | `{ ... }` (Object) |

</details>

### Object: `OneEye`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"1"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Open`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Open` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `GSOpenAttack` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `OpenCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `OpenCat` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Out`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Parousworm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer | The constitution stat value or modifier for the unit. || `-1` (Number) |
| `cursed` | Boolean | If true, the item is cursed and cannot be unequipped. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_PAROUSWORM_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `271` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_PAROUSWORM_NAME"` (String) |
| `parasite` | Boolean | If true, this creature behaves as a parasite (e.g., attaches to or inhabits another unit). || `true` (Boolean) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |

</details>

### Object: `ParticleAttractor`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force_end` | Number | The force vector (or scalar magnitude) applied to particles at the end of their lifespan. | 6 | `200` (Number), `500` (Number) |
| `force_start` | Number | The force vector (or scalar magnitude) applied to particles at the start of their lifespan. | 6 | `0` (Number) |
| `force` | Number | A force vector [x, y, z] applied to particles, or a scalar magnitude applied downward. | 1 | `100` (Number) |
| `towards` | Array | An array defining the direction vector particles are attracted towards. || `[5 0 5]` (Array), `[0 .5 0]` (Array) |

</details>

### Object: `ParticleBouncePlane`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String | The velocity dampening factor (0 to 1) applied when particles bounce off the plane. | 74 | `1` (Number), `0` (Number), `.1` (String), `.75` (String) |
| `friction` | Number / String | An array of friction coefficients [x y z] applied to particle velocity on the bounce plane. | 70 | `5` (Number), `2` (Number), `.1` (String), `.2` (String) |
| `plane` | Enum | Specifies the orientation of the bounce plane (e.g., 'right', 'back'). | 32 | `right` (Enum), `back` (Enum) |
| `position` | Number | The 2D position (x, y) or single-coordinate value for placement. | 32 | `10.5` (Number) |
| `rotation_dampening` | Number | The dampening factor applied to particle rotation upon bouncing. | 1 | `1` (Number) |

</details>

### Object: `ParticleCharacterCollision`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_sphere_offset` | Number | The offset distance from the character's collision sphere used for particle character collision. | 1 | `0` (Number) |
| `inherit_velocity` | String | The fraction (0 to 1) of the character's velocity inherited by particles upon collision. | 1 | `.5` (String) |
| `pushforce` | Number | The force magnitude applied to push characters away upon particle collision. | 1 | `2` (Number) |

</details>

### Object: `ParticleGlobalForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Array | A scalar value for the strength or intensity of an ambient effect, or a percentage range. | 27 | `3` (Number), `1` (Number), `.1` (String), `.5` (String) |
| `id` | Enum | Specifies the unique identifier for the object or room, used for referencing or categorization. | 27 | `Wind` (Enum) |

</details>

### Object: `ParticleLineCollisions`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String | The velocity dampening factor (0 to 1) applied when particles bounce off the plane. | 6 | `1` (Number), `.5` (String) |
| `friction` | Number | An array of friction coefficients [x y z] applied to particle velocity on the bounce plane. | 6 | `1` (Number), `0` (Number) |
| `end_on_collision` | Boolean | If true, the particle system ends immediately upon any collision with a line. | 2 | `true` (Boolean) |

</details>

### Object: `ParticleRandomForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `begin` | Array | The starting force vector (or range) applied by the random force, often with random values per axis. || `[0 -20 0]` (Array), `[0 -10 0]` (Array) |
| `end` | Enum | The ending force vector (or range), or an enum string referencing a predefined force pattern. || `[0 -450 0]` (Array), `[0 [ 40 120 ] 0]` (Array) |

</details>

### Object: `ParticleTornadoForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force` | Number | A force vector [x, y, z] applied to particles, or a scalar magnitude applied downward. | 19 | `8` (Number), `5` (Number) |
| `axis` | Array | The axis vector around which the tornado force rotates. || `[0 -0.5 0]` (Array), `[0 1 0]` (Array) |
| `point` | Array | The center point of the tornado force effect. || `[1 1 1]` (Array), `[0 0 0]` (Array) |

</details>

### Object: `PeaceSymbol`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ARMOR_PEACESYMBOL_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `91` (Number) |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Maps keyword identifiers to their tooltip override values for display. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `neck` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ARMOR_PEACESYMBOL_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `[Hippie Twine]` (Array) |

</details>

### Object: `PeaceSymbolFacePaint`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ARMOR_PEACESYMBOLFACEPAINT_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `194` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `face` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ARMOR_PEACESYMBOLFACEPAINT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `rare` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Hippie` (Enum) |

</details>

### Object: `PermanentCharm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies an alias keyword for referencing this status effect in tooltips or logic. || `Charmed` (Enum) |

</details>

### Object: `Pigeon`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdMed` (Enum) |

</details>

### Object: `PopAndSpawn`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 4 | `BoyShade` (Enum), `PlayerCat_ClotClone` (Enum) |
| `clone_items` | Boolean | If true, items from the source unit are cloned onto the spawned unit. | 2 | `false` (Boolean) |
| `clone_referenced_catdata` | Boolean | If true, any referenced cat data (e.g., unique stats) is also cloned to the spawned unit. | 2 | `true` (Boolean) |
| `no_splatter` | Boolean | If true, prevents blood splatter visual effect when the object pops and spawns. | 2 | `false` (Boolean) |

</details>

### Object: `Possessing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Possessing"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `GA_Telekinesis_Big` (Enum) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `primed` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Priming`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 4 | `{ ... }` (Object) |

</details>

### Object: `Psychic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[Telekinesis Suggestion MindControl MegaGrav PsyFlutter MagnetPull MindBlast PsychicChoke SkyShatter Supernova...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_PSYCHIC0" "TEAMNAME_ADJECTIVE_PSYCHIC1" "TEAMNAME_ADJECTIVE_PSYCHIC2" "TEAMNAME_ADJECTIVE_PSYCHIC3" "TEAMNAME_ADJECTIVE_PSYCHIC4" "TEAMNAME_ADJECTIVE_PSYCHIC5" "TEAMNAME_ADJECTIVE_PSYCHIC6" "TEAMNAME_ADJECTIVE_PSYCHIC7" "TEAMNAME_ADJECTIVE_PSYCHIC8" "TEAMNAME_ADJECTIVE_PSYCHIC9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicPsychicPull]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_PSYCHIC_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | Specifies passive abilities that are permanently granted to the unit. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[int cha spd]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_PSYCHIC_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_PSYCHIC0" "TEAMNAME_NOUN_PSYCHIC1" "TEAMNAME_NOUN_PSYCHIC2" "TEAMNAME_NOUN_PSYCHIC3" "TEAMNAME_NOUN_PSYCHIC4" "TEAMNAME_NOUN_PSYCHIC5" "TEAMNAME_NOUN_PSYCHIC6" "TEAMNAME_NOUN_PSYCHIC7" "TEAMNAME_NOUN_PSYCHIC8" "TEAMNAME_NOUN_PSYCHIC9"]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[Flying SoulShatter Glow Blink FullPower RealityShatter MentalStorm Wither Flourish PsySmack...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[Ping Telekinesis Suggestion SkyShatter MindMeld Glare MindCrack FlashForward CumulativeBlast IncreaseGravity]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Pulp2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `2` (Number) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `3` (Number) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `4` (Number) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp5`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `5` (Number) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp6`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `6` (Number) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp7`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `7` (Number) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 2 | `1` (Number) |

</details>

### Object: `Rage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 16 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 12 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 12 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 8 | `"Rage"` (Enum) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"Rage"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `ChubsSpinRage` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 2 | `2` (Number) |

</details>

### Object: `Rain`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `adventure_weather` | Enum | Specifies the weather type for the adventure map (e.g., Snow, Rain, Windy, Thunderstorm). | 1 | `Rain` (Enum) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather event. | 1 | `amb_rain.ogg` (String) |
| `prewarm` | Number | The number of seconds to prewarm the particle system before displaying. | 1 | `5` (Number) |
| `skybox_frame` | Enum | Specifies the skybox visual frame to use for this weather. | 1 | `day_rain` (Enum) |
| `alpha` | String | The transparency or opacity level of the particle or visual effect. || `.5` (String) |
| `chain` | Boolean | Specifies the chain effect type (e.g., 'splashM') or 'true' to enable chaining. || `splash` (Enum) |
| `combo` | Array | Defines a sequence of visual effect names to play in order for a particle or animation combo. || `[RainB RainM RainF]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"WEATHER_RAIN_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Defines the effects (e.g., statuses, damage) applied by the revenge damage. || `{ ... }` (Object) |
| `emit_amount` | Number | The number of particles emitted per burst, or a range [min, max] of possible amounts. || `1` (Number) |
| `emit_box` | Array | A bounding box [xMin xMax yMin yMax zMin zMax] defining the area in which particles are spawned. || `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array | A vector [x, y, z] defining the initial direction of emitted particles. || `[0 -1 0]` (Array) |
| `emit_rate` | Number | The number of particles emitted per second. || `200` (Number) |
| `emit_spread` | Number | The angular spread in degrees over which particles are emitted. || `0` (Number) |
| `face_moving_direction` | Boolean | If true, particles rotate to face their direction of movement. || `true` (Boolean) |
| `force` | Array | A force vector [x, y, z] applied to particles, or a scalar magnitude applied downward. || `[0 -10 0]` (Array) |
| `hint_persistent_elements` | Array | An array of element types that persist as hints during this weather (e.g., [Ice Wind]). || `[Water]` (Array) |
| `live_bounds` | Array | A bounding box [xMin xMax yMin yMax zMin zMax] outside which particles are deactivated or destroyed. || `[-999 999 0 999 -999 999]` (Array) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. || `RainParticle` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"WEATHER_RAIN_NAME"` (String) |
| `particle_lifetime` | Number | The duration in seconds a particle lives, or a range [min, max] of possible lifetimes. || `5` (Number) |
| `particles` | Array | An array of particle system names to be used for this weather effect. || `[Rain]` (Array) |
| `projection_matrix` | Enum | Specifies the projection mode for the particle system, e.g., default or perspective-based. || `default` (Enum) |
| `render_mode` | Enum | Determines how the particle system renders, e.g., default or separate render passes. || `separate` (Enum) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Defines scripted behaviors on particles, such as bounce planes or wind effects. || `{ ... }` (Object) |
| `simulation_space` | Enum | Determines if particle simulation is in local or global space. || `global` (Enum) |
| `size_start` | String | The initial size of particles, or a range [min, max] of possible sizes. || `.5` (String) |
| `speed_scale` | String | A multiplier applied to the overall speed of the particle system animation. || `.1` (String) |
| `speed_start` | Number | The initial speed of particles, or a range [min, max] of possible speeds. || `10` (Number) |

</details>

### Object: `RandomArmorPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `RandomBiggerArmorPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `RandomBiggerCatnipPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `RandomBiggerFoodPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `RandomCatnipPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `RandomFoodPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `RaptorEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_RaptorEgg` (Enum) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_RAPTOREGG_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `1` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `263` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_RAPTOREGG_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |

</details>

### Object: `Raven`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdMed` (Enum) |

</details>

### Object: `RavenFeather`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ARMOR_RAVENFEATHER_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `179` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `neck` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ARMOR_RAVENFEATHER_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `rare` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Feathered` (Enum) |

</details>

### Object: `Return`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `return` (Enum) |

</details>

### Object: `ReturnA`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `HangerBotReturn` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_close` (Enum) |

</details>

### Object: `RunFar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `PyrophinaVSRun` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `run_far` (Enum) |

</details>

### Object: `Scrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_SCRAP_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_SCRAP_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `shield` | Enum / Integer | The unit's shield value, specified as an integer or a formula. || `[1 .5]` (Array), `3` (Number) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `PickupBase` (Enum) |

</details>

### Object: `Seagull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdMed` (Enum) |

</details>

### Object: `SewersUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `Shadow`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Number | The chance for the damage instance to critically hit, expressed as a percentage (e.g., 50%) or a decimal fraction (e.g., .5). | 4 | `.05*X` (String) |
| `class` | Enum | Specifies the class name or ability class associated with this object. || `Thief` (Enum) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"PASSIVE_STEALTHED_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"PASSIVE_STEALTHED_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `teleport` (Enum) |

</details>

### Object: `ShowFakeDamage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks or formula for the status effect applied. | 2 | `999` (Number) |
| `style` | Array | An array of style tags applied to the fake damage display (e.g., ['crit']). || `[crit]` (Array) |

</details>

### Object: `Sitting`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Chair` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `DoNothing` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `DoNothing` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `SlotResult_Explode`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | A damage instance object that applies damage and effects to the source unit itself. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `spell` (Enum) |

</details>

### Object: `SlotResult_Jackpot_Coins`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | A damage instance object that applies damage and effects to the source unit itself. || `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Specifies the unit or object to spawn, along with its properties (e.g. object, ai_base_score, faction, layer). || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `spawn` (Enum) |

</details>

### Object: `SlotResult_Nothing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `self_buff` (Enum) |

</details>

### Object: `SlotResult_RandomPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Specifies the unit or object to spawn, along with its properties (e.g. object, ai_base_score, faction, layer). || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `spawn` (Enum) |

</details>

### Object: `Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `""` (String) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `GameteInflate` (Enum) |

</details>

### Object: `SmallAttic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 2 | `5` (Number) |
| `id` | Enum | Specifies the unique identifier for the object or room, used for referencing or categorization. | 2 | `Attic` (Enum) |
| `interstitial_bg_frame` | Enum | Specifies the background frame name used for interstitial room transition screens. | 2 | `attic` (Enum) |
| `movieclip` | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. | 2 | `RoomBackgroundSmallAttic` (Enum) |
| `width` | Number | The width of the room in grid tiles. | 2 | `18` (Number) |
| `built_in_collision` | Array | An array defining the collision geometry for the room, typically as a list of vertices or shapes. || `[[ 6 6 6 6 6 6 6 6 6...]` (Array) |
| `extra_bound_planes` | Array | An array defining additional collision planes that bound the room's playable area. || `[{ p [ 0 0 ] n [ 1 -2...]` (Array) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |

</details>

### Object: `SmallBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Defines an alternative spawning pool with item names and weights, replacing the default pool under certain conditions. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |

</details>

### Object: `SmallHolding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Holding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `SmallHoldingCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"HoldingCat"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `SmallHouse_Attic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 2 | `Default` (Enum) |
| `unlock_room` | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 2 | `Attic` (Enum) |

</details>

### Object: `Snake`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `SpawningPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `SpearRun`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 4 | `CaveManSpearRun` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 4 | `CaveManPickupSpear` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 | `util_minmove` (Enum) |

</details>

### Object: `Squirrel`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `SquirrelForm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 4 | `BasicMelee` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `ENEMY_DRAVENSQUIRRELFORM_DESC` (String) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | A damage instance object that applies damage and effects to the source unit itself. || `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Specifies the unit or object to spawn, along with its properties (e.g. object, ai_base_score, faction, layer). || `{ ... }` (Object) |
| `tags` | Array / Enum | Array of gameplay-relevant tags for item or unit categorization (e.g., 'consumable', 'cat'). || `[shapeshift summon]` (Array) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters for an ability, such as range, aoe, or target mode. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `spawn` (Enum) |

</details>

### Object: `Standing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BungaSmash` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `DefaultMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Standing2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BungaSmash` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 2 | `BungaJumpMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 2 | `{ ... }` (Object) |

</details>

### Object: `Start_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Stimulation`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"KEYWORD_STIMULATION_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"KEYWORD_STIMULATION_DESC"` (String) |

</details>

### Object: `Stop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Maps keyword identifiers to their tooltip override values for display. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `SuckMF`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `TormentorSuck` (Enum) |
| `decision_weights` | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 2 | `careless` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `keep_distance` (Enum) |

</details>

### Object: `SwordAndShield`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `DestroyerAttack` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `SwordAndShield_Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Holy"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `DestroyerAttack` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `TF_TargetAllies`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 2 | `util_target_allies` (Enum) |

</details>

### Object: `TF_TargetEnemies`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 2 | `util_target_enemies` (Enum) |

</details>

### Object: `TVBotDie`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the elite buff's icon. || `155` (Number) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ENEMY_TVBOT_DIE_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"ENEMY_TVBOT_DIE_DESC"` (String) |

</details>

### Object: `TVBotDumb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the elite buff's icon. || `155` (Number) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ENEMY_TVBOT_DUMB_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"ENEMY_TVBOT_DUMB_DESC"` (String) |

</details>

### Object: `TVBotObey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the elite buff's icon. || `155` (Number) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ENEMY_TVBOT_OBEY_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"ENEMY_TVBOT_OBEY_DESC"` (String) |

</details>

### Object: `TVBotStop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the elite buff's icon. || `155` (Number) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ENEMY_TVBOT_STOP_NAME"` (String) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. || `"ENEMY_TVBOT_STOP_DESC"` (String) |

</details>

### Object: `Tank`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[HeadButt ThrowShield ChewCud AssBlast Chew BatterUp BackBreaker Suplex Intimidate Toss...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_TANK0" "TEAMNAME_ADJECTIVE_TANK1" "TEAMNAME_ADJECTIVE_TANK2" "TEAMNAME_ADJECTIVE_TANK3" "TEAMNAME_ADJECTIVE_TANK4" "TEAMNAME_ADJECTIVE_TANK5" "TEAMNAME_ADJECTIVE_TANK6" "TEAMNAME_ADJECTIVE_TANK7" "TEAMNAME_ADJECTIVE_TANK8" "TEAMNAME_ADJECTIVE_TANK9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicTankMelee]` (Array) |
| `complicated_abilities` | Array | The list of ability names that have complex logic and may be hidden from simplified views. || `[TankRockSong FlipFlop Lunge PlantFeet IronHead Aftershock Demolish FullForce Thicken Spur]` (Array) |
| `complicated_passives` | Array | The list of passive names that have complex logic and may be hidden from simplified views. || `[Plow ChainKnockback Wrestlemaniac MyLeg SlowAndSteady ShovingMatch]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_TANK_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[con str spd]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_TANK_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_TANK0" "TEAMNAME_NOUN_TANK1" "TEAMNAME_NOUN_TANK2" "TEAMNAME_NOUN_TANK3" "TEAMNAME_NOUN_TANK4" "TEAMNAME_NOUN_TANK5" "TEAMNAME_NOUN_TANK6" "TEAMNAME_NOUN_TANK7" "TEAMNAME_NOUN_TANK8" "TEAMNAME_NOUN_TANK9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[Thorns HeavyHanded SlackOff Scabs ThunderThighs Plow PetRocks ToadStyle ChainKnockback ProtectiveAura...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[TankSwap Toss BellyFlop BatterUp Chew ThrowShield DrawAttention BodyGuard Earthquake Spur]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Tar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `SpewerLobbed_Tar` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `TarFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `Full` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `SpewerSpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `TempDexterityUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies an alias keyword for referencing this status effect in tooltips or logic. || `DexterityUp` (Enum) |

</details>

### Object: `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `TempSpeedUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies an alias keyword for referencing this status effect in tooltips or logic. || `SpeedUp` (Enum) |

</details>

### Object: `TheEndUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 | `{ ... }` (Object) |

</details>

### Object: `Thief`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[MoveAgain Assassinate BoostBackstab PoisonGas PoisonNail WeakeningNail SharpNail CoinToss Shadow TimeWalk...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_THIEF0" "TEAMNAME_ADJECTIVE_THIEF1" "TEAMNAME_ADJECTIVE_THIEF2" "TEAMNAME_ADJECTIVE_THIEF3" "TEAMNAME_ADJECTIVE_THIEF4" "TEAMNAME_ADJECTIVE_THIEF5" "TEAMNAME_ADJECTIVE_THIEF6" "TEAMNAME_ADJECTIVE_THIEF7" "TEAMNAME_ADJECTIVE_THIEF8" "TEAMNAME_ADJECTIVE_THIEF9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[BasicStraightShot_Thief]` (Array) |
| `complicated_abilities` | Array | The list of ability names that have complex logic and may be hidden from simplified views. || `[QuickRoll Shadowshift SlingShade ThiefSwap Pierce TripleNails SkinDisguise PoisonDip]` (Array) |
| `complicated_passives` | Array | The list of passive names that have complex logic and may be hidden from simplified views. || `[BountyHunter AfterImage Agile FlipACoin]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_THIEF_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[spd dex lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_THIEF_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_THIEF0" "TEAMNAME_NOUN_THIEF1" "TEAMNAME_NOUN_THIEF2" "TEAMNAME_NOUN_THIEF3" "TEAMNAME_NOUN_THIEF4" "TEAMNAME_NOUN_THIEF5" "TEAMNAME_NOUN_THIEF6" "TEAMNAME_NOUN_THIEF7" "TEAMNAME_NOUN_THIEF8" "TEAMNAME_NOUN_THIEF9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[Backstabber GoldenClaws Shadow PoisonTips Burgle SwiftKiller DoubleThrow BountyHunter RazorClaws Looter...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[Shadow PoisonNail MoveAgain Backflip Distract Rebound Stalk Assassinate CutPurse SeverArtery]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Throb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Host` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobbingArteryDone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 | `{ ... }` (Object) |

</details>

### Object: `Thunderstorm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum | Specifies the weather type for the adventure map (e.g., Snow, Rain, Windy, Thunderstorm). | 1 | `Thunderstorm` (Enum) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather event. | 1 | `amb_thunderstorm.ogg` (String), `amb_heavyrain.ogg` (String) |
| `lightning_fx` | Boolean | If true, enables lightning visual effects during the thunderstorm. | 1 | `true` (Boolean) |
| `prewarm` | Number | The number of seconds to prewarm the particle system before displaying. | 1 | `5` (Number) |
| `skybox_frame` | Enum | Specifies the skybox visual frame to use for this weather. | 1 | `day_thunderstorm` (Enum) |
| `combo` | Array | Defines a sequence of visual effect names to play in order for a particle or animation combo. || `[TRainB TRainM TRainF WindDust]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"WEATHER_THUNDERSTORM_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Defines the effects (e.g., statuses, damage) applied by the revenge damage. || `{ ... }` (Object) |
| `hint_persistent_elements` | Array | An array of element types that persist as hints during this weather (e.g., [Ice Wind]). || `[Water Wind]` (Array) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"WEATHER_THUNDERSTORM_NAME"` (String) |
| `particles` | Array | An array of particle system names to be used for this weather effect. || `[Thunderstorm]` (Array) |

</details>

### Object: `TieDyeBandana`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ARMOR_TIEDYEBANDANA_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `209` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `head` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ARMOR_TIEDYEBANDANA_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `rare` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Hippie` (Enum) |

</details>

### Object: `Tinkerer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | Groups abilities into named categories for organized selection or assignment. || `{ ... }` (Object) |
| `ability_pool` | Array | The list of ability names available for random selection during level-up or generation. || `[Research Discharge Repair ShoddyJetpack SpawnDecoy SpringShoes AutoPilot Recycle BuildTurret RocketSkates...]` (Array) |
| `adjectives` | Array | The list of adjective strings used for procedural naming of units. || `["TEAMNAME_ADJECTIVE_TINKERER0" "TEAMNAME_ADJECTIVE_TINKERER1" "TEAMNAME_ADJECTIVE_TINKERER2" "TEAMNAME_ADJECTIVE_TINKERER3" "TEAMNAME_ADJECTIVE_TINKERER4" "TEAMNAME_ADJECTIVE_TINKERER5" "TEAMNAME_ADJECTIVE_TINKERER6" "TEAMNAME_ADJECTIVE_TINKERER7" "TEAMNAME_ADJECTIVE_TINKERER8" "TEAMNAME_ADJECTIVE_TINKERER9"...]` (Array) |
| `attack_pool` | Array | The list of attack ability names available for random selection during level-up or generation. || `[TinkererCraft]` (Array) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"SETBONUS_TINKERER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | Specifies passive abilities that are permanently granted to the unit. || `{ ... }` (Object) |
| `levelup_stats` | Array | The three stat names that randomly improve when the unit levels up. || `[dex cha int]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"SETBONUS_TINKERER_NAME"` (String) |
| `nouns` | Array | The list of noun strings used for procedural naming of units. || `["TEAMNAME_NOUN_TINKERER0" "TEAMNAME_NOUN_TINKERER1" "TEAMNAME_NOUN_TINKERER2" "TEAMNAME_NOUN_TINKERER3" "TEAMNAME_NOUN_TINKERER4" "TEAMNAME_NOUN_TINKERER5" "TEAMNAME_NOUN_TINKERER6" "TEAMNAME_NOUN_TINKERER7" "TEAMNAME_NOUN_TINKERER8" "TEAMNAME_NOUN_TINKERER9"...]` (Array) |
| `passive_pool` | Array | The list of passive ability names available for random selection during level-up or generation. || `[VersionTwo WeaponProficiency LivingBattery FuzzyFeet ArmorSpecialist EMP MrMega EscapeSequence ItemProxy LightningRod...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of material pieces needed to craft or combine into a full item. || `3` (Number) |
| `starter_abilities` | Array | The list of ability names granted to the unit at the start of the game. || `[Research ArmorUp ShoddyJetpack BuildTurret RocketSkates Discharge Craft Catbot Electrolyze InstantBarrier]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | A dictionary of stat name keys to integer modifiers applied to the unit's base stats. || `{ ... }` (Object) |

</details>

### Object: `Toad`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `Transformed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Turkey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_Heal` (Enum) |
| `aux` | Integer | An integer modifier for the auxiliary stat, often used for scaling or effect values. || `15` (Number) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_TURKEY_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `7` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `244` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_TURKEY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_rare` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Configures the object's sound effects, including alternative sounds for actions. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `BirdLarge` (Enum) |

</details>

### Object: `Turtle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Defines the unit's move, attack, and spell abilities (as an array). || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Defines the unit's base stats (strength, dexterity, constitution, intelligence, speed). || `{ ... }` (Object) |

</details>

### Object: `Turtled`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `Turtle` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 4 | `None` (Enum) |
| `move` | Enum | Determines which movement ability the unit uses. | 4 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 | `{ ... }` (Object) |

</details>

### Object: `TwoAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Configures turn-taking behavior for the status effect, including whether the unit takes turns and bonus turns. | 6 | `{ ... }` (Object) |

</details>

### Object: `TwoEyes`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Unflip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | `TeleportFlipUp` (Enum) |
| `move_for_ability` | Enum | Determines which animation or movement ability is used to close distance. | 2 | `Spin_Enemy` (Enum) |
| `move_weights` | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 | `stay_close_always_move` (Enum) |

</details>

### Object: `Unlit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Unlit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Unwashed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `Unwashed` (Enum) |

</details>

### Object: `Up`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 | `"Up"` (Enum) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"OBJECT_TIREUP_DESC"` (String) |

</details>

### Object: `VolcanoAntennaAttached`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 4 | `{ ... }` (Object) |

</details>

### Object: `WallOfFleshDone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 | `{ ... }` (Object) |

</details>

### Object: `Washed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `Washer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BasicMelee` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CULTISTWASHER_NAME"` (String) |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Cultist"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CULTISTWASHER_DESC"` (String) |

</details>

### Object: `Water`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 | `"Water"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |

</details>

### Object: `WeirdEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_WEIRDEGG_DESC"` (String) |
| `frame` | Integer | The sprite frame index used for this arm. || `73` (Number) |
| [`intro`](Events_and_Encounters.md#object-intro) | Object | Defines the introductory sequence or dialog for an event or quest. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| [`main`](Events_and_Encounters.md#object-main) | Object | Defines the main interaction prompt and options for an event. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_WEIRDEGG_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `uncommon` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Baby` (Enum) |

</details>

### Object: `WereMan`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"WereMan"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `WereManFurySwipes` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_WEREMAN_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_WEREMAN_DESC"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Defines the unit's core properties such as tag, health, movement, faction, type, and crit chance. || `{ ... }` (Object) |
| `variant_of` | Enum | Specifies the base character that this entry is a variant of. || `CavePerson` (Enum) |

</details>

### Object: `Wind`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 4 | `X` (Enum) |

</details>

### Object: `WishBone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). || `cm_WishBone` (Enum) |
| `consumable` | Boolean | If true, marks the item as consumable; can also specify a sub-object defining its item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localization key or literal description text for the ability. || `"ITEM_WISHBONE_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. || `1` (Number) |
| `frame` | Integer | The sprite frame index used for this arm. || `193` (Number) |
| `kind` | Enum | Specifies the equipment slot type (e.g., head, face, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. || `"ITEM_WISHBONE_NAME"` (String) |
| `rarity` | Enum | Determines the loot rarity tier of the item (e.g., very_rare, consumable_common). || `consumable_very_rare` (Enum) |
| `set` | Array / Enum | The visual set or furniture style tag (e.g., elegant, guts, Tentacle, wooden, Druid). || `Bone` (Enum) |

</details>

### Object: `Zealot`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"Zealot"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BBStabby` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_CULTISTZEALOT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_CULTISTZEALOT_DESC"` (String) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource or action cost to use an ability, such as mana or a cantrip slot. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Contains visual properties for an entity or effect, such as animation, particle, or name. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for an ability such as name, description, class, and icon type. || `{ ... }` (Object) |
| `template` | Enum | Specifies the ability template or behavior type, such as throw_attack or self_buff. || `self_buff` (Enum) |

</details>

### Object: `ZealotBomb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Defines the AI brain, decision/move weights, and pattern for controlling a unit's behavior. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 | `"BombZealot"` (Enum) |
| `attack` | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 | `BBExplode` (Enum) |
| `name` | Enum | Specifies the localization key or literal name for the ability. | 2 | `"ENEMY_BOMBZEALOT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 2 | `"ENEMY_BOMBZEALOT_DESC"` (String) |

</details>


---

## Auto-Discovered Objects


### Object: `AntlerSwipe`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `throw_attack` |

</details>

### Object: `AntlerSwipe2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `AntlerSwipe` |

</details>

### Object: `BasicDashAttackMove_NoKnockback`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `dash_attack` |

</details>

### Object: `BerserkDash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `dash_attack` |

</details>

### Object: `BirthSquirrel`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `summon` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spawn` |

</details>

### Object: `BlackShard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_BlackShard` |
| `aux` | Number | Undocumented. | 1 | `1` |
| `desc` | String | Undocumented. | 1 | `"ITEM_BLACKSHARD_DESC"` |
| `frame` | Number | Undocumented. | 1 | `164` |
| `hint_destination` | String | Undocumented. | 1 | `core` |
| `indestructible` | Boolean | Undocumented. | 1 | `true` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `legacy_quest` | Boolean | Undocumented. | 1 | `true` |
| `name` | String | Undocumented. | 1 | `"ITEM_BLACKSHARD_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `quest_item` | Boolean | Undocumented. | 1 | `true` |
| `rarity` | String | Undocumented. | 1 | `quest` |
| `set` | String | Undocumented. | 1 | `Obelisk` |

</details>

### Object: `Boulder`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | Undocumented. | 1 ||

</details>

### Object: `CharmTrap`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `lobbed_attack` |

</details>

### Object: `Chitter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `DeathWormEat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `return` |
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Undocumented. | 1 ||

</details>

### Object: `EtherSoakedRag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_EtherSoakedRag` |
| `desc` | String | Undocumented. | 1 | `"ITEM_ETHERSOAKEDRAG_DESC"` |
| `frame` | Number | Undocumented. | 1 | `121` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_ETHERSOAKEDRAG_NAME"` |
| `rarity` | String | Undocumented. | 1 | `uncommon` |
| `set` | String | Undocumented. | 1 | `Rag` |

</details>

### Object: `HardenSkin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `HardenSkin2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `HardenSkin` |

</details>

### Object: `HeadTumor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `HornCharge`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `dash_attack` |

</details>

### Object: `JewelOfDrog`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"ARMOR_JEWELOFDROG_DESC"` |
| `frame` | Number | Undocumented. | 1 | `137` |
| `kind` | String | Undocumented. | 1 | `head` |
| `name` | String | Undocumented. | 1 | `"ARMOR_JEWELOFDROG_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `rarity` | String | Undocumented. | 1 | `rare` |
| `set` | String | Undocumented. | 1 | `Gemstone` |

</details>

### Object: `MegaGuppy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `MockSong`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `MockSong2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `MonkeyThrow`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `throw_attack` |

</details>

### Object: `MonkeyThrow2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `MonkeyThrow` |

</details>

### Object: `MoonHandDrop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `MoonHandThrow` |

</details>

### Object: `MoonHeadFlail`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `FlailBase` |

</details>

### Object: `Pounce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `jump_attack` |

</details>

### Object: `Prance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `Prance2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Prance` |

</details>

### Object: `RandomPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||

</details>

### Object: `Scavenge`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `move` |

</details>

### Object: `Scavenge2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Scavenge` |

</details>

### Object: `Synthesize`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `Synthesize2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Synthesize` |

</details>

### Object: `TaintedOffering`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `jump_attack` |

</details>

### Object: `TaintedOffering2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `TaintedOffering` |

</details>

### Object: `Tease`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `targeted_status` |

</details>

### Object: `Tease2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Tease` |

</details>

### Object: `TheDestroyer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `Thrash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `ThrowPoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `lobbed_attack` |

</details>

### Object: `TigerSwipes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `TigerSwipes2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `TigerSwipes` |

</details>

### Object: `Timber`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `trample_dash` |
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Undocumented. | 1 ||

</details>

### Object: `TinaFlail`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `FlailBase` |

</details>

### Object: `TinaFlailRage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `FlailBase` |

</details>

### Object: `ZombieCatFamiliar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `cm_RaptorEggSpawn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `summon` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spawn` |

</details>

### Object: `head_CrownOfHorns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `straightshot_attack` |

</details>

### Object: `megadino`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_MEGADINO_QUOTE_1` | String | Undocumented. | 1 ||
| `frame_label` | String | Undocumented. | 1 | `MegaDino` |
| `name` | String | Undocumented. | 1 | `BOSS_MEGADINO_NAME` |
| `quotes` | Array | Undocumented. | 1 ||

</details>

### Object: `moonhead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_MOONHEAD_QUOTE_1` | String | Undocumented. | 1 ||
| `BOSS_MOONHEAD_QUOTE_2` | String | Undocumented. | 1 ||
| `BOSS_MOONHEAD_QUOTE_3` | String | Undocumented. | 1 ||
| `BOSS_MOONHEAD_QUOTE_4` | String | Undocumented. | 1 ||
| `frame_label` | String | Undocumented. | 1 | `MoonHead` |
| `name` | String | Undocumented. | 1 | `BOSS_MOONHEAD_NAME` |
| `quotes` | Array | Undocumented. | 1 ||

</details>
