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
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 |  |
| [`FormChange`](./Enums.md#enum-formchange) | Enum / Object | Transforms the character into a different state or form (e.g., Rage, HasCat). | 114 |  |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer | Applies or references the 'Stun' effect/state. | 106 |  |
| `Burn` | Array / Enum / Integer | Applies or references the 'Burn' effect/state. | 1 |  |
| `Bruise` | Array / Integer / Object | Applies or references the 'Bruise' effect/state. | 8 |  |
| [`Else`](#else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 1 |  |
| `IgnoreSelf` | Boolean / Integer | Applies or references the 'IgnoreSelf' effect/state. | 75 |  |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum / Object | Transforms the terrain tile under the target. | 62 |  |
| `Shield` | Enum / Integer | Applies or references the 'Shield' effect/state. | 422 |  |
| [`Confusion`](./Arrays.md#array-confusion) | Array / Integer / Object | Applies or references the 'Confusion' effect/state. | 6 |  |
| `Cleanse` | Integer / Object | Applies or references the 'Cleanse' effect/state. | 2 |  |
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 50 |  |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | Applies or references the 'AllStatsUp' effect/state. | 49 |  |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific string tag to check for. | 981 |  |
| [`ApplyToSource`](#applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 47 |  |
| `Temporary` | Object | A wrapper object for applying status effects that automatically expire. | 46 |  |
| [`Conditional_HasTag`](#conditionalhastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 42 |  |
| `SpeedUp` | Enum / Integer | Applies or references the 'SpeedUp' effect/state. | 40 |  |
| [`Conditional_Enemy`](#conditionalenemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 38 |  |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Applies or references the 'VisualFXTile' effect/state. | 36 |  |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum / Object | Spawns a physics object that visually bounces off the target. | 35 |  |
| [`Slow`](./Arrays.md#array-slow) | Array / Enum / Integer / Object | Applies or references the 'Slow' effect/state. | 4 |  |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer | Applies or references the 'Charmed' effect/state. | 33 |  |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer | Applies or references the 'Immobile' effect/state. | 4 |  |
| `ManaGain` | Enum / Integer | Applies or references the 'ManaGain' effect/state. | 31 |  |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer | Applies or references the 'Freeze' effect/state. | 29 |  |
| `StrengthUp` | Enum / Integer | Applies or references the 'StrengthUp' effect/state. | 29 |  |
| `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. | 29 |  |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer | Applies or references the 'Petrify' effect/state. | 28 |  |
| `SpawnExtraThingsOnBattleStart` | Object | Examples: `{ ... }` | 2 |  |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Applies or references the 'TransformAbility' effect/state. | 28 |  |
| [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 27 |  |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer | Applies or references the 'ConstitutionUp' effect/state. | 26 |  |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum / Object | Upgrades or transforms an existing ability into a new one from the specified pool. | 26 |  |
| [`Weakness`](./Arrays.md#array-weakness) | Array / Integer / Object | Applies or references the 'Weakness' effect/state. | 4 |  |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer | Applies or references the 'Blind' effect/state. | 6 |  |
| [`Madness`](./Arrays.md#array-madness) | Array / Enum / Integer / Object | Applies the Madness debuff/status effect. | 24 |  |
| `BonusDamage` | Enum / Integer | Applies or references the 'BonusDamage' effect/state. | 23 |  |
| `KnockUpAndAway` | Object | Displaces the target vertically and horizontally away from the source. | 23 |  |
| `Leech` | Integer | Applies or references the 'Leech' effect/state. | 6 |  |
| `RandomStatusFromPool` | Object | Selects and applies a random status effect from the provided nested object. | 22 |  |
| `TakeExtraTurn` | Integer | Applies or references the 'TakeExtraTurn' effect/state. | 22 |  |
| `IntelligenceUp` | Enum / Integer | Applies or references the 'IntelligenceUp' effect/state. | 21 |  |
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer | Applies or references the 'Sleep' effect/state. | 21 |  |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 21 |  |
| [`Consumed`](#consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 18 |  |
| `VaporizeCorpse` | Integer | Applies or references the 'VaporizeCorpse' effect/state. | 18 |  |
| `CollectsPickups` | Integer | Applies or references the 'CollectsPickups' effect/state. | 17 |  |
| [`Conditional_Boss`](#conditionalboss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 17 |  |
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum / Integer | Applies or references the 'OverrideKnockbackDamage' effect/state. | 17 |  |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 17 |  |
| `FullHeal` | Integer | Applies or references the 'FullHeal' effect/state. | 16 |  |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 16 |  |
| `Leeches` | Integer / Object | Applies or references the 'Leeches' effect/state. | 2 |  |
| `OverrideDamage` | Integer | Applies or references the 'OverrideDamage' effect/state. | 16 |  |
| `Revive` | Integer / Object | Applies or references the 'Revive' effect/state. | 2 |  |
| [`ApplyToSourceOnKill`](#applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 15 |  |
| [`CanApplyToInanimate`](#canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 15 |  |
| `Cleave` | Integer / Object | Causes the attack to hit adjacent enemies alongside the primary target. | 15 |  |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 15 |  |
| `FaceAway` | Integer | Applies or references the 'FaceAway' effect/state. | 15 |  |
| `force_contact` | Boolean | If true, enforces physical overlap. | 15 |  |
| `GenericDebuff` | Integer | Applies or references the 'GenericDebuff' effect/state. | 15 |  |
| `RefreshMovePoints` | Integer | Applies or references the 'RefreshMovePoints' effect/state. | 15 |  |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | Applies or references the 'RemoveStatus' effect/state. | 15 |  |
| `CatPartsTransform` | Object | Transforms specific body parts into different visual variants. | 14 |  |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Applies or references the 'ChangeCatClass' effect/state. | 14 |  |
| [`Conditional_NotBoss`](#conditionalnotboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 14 |  |
| `EndTurn` | Integer | Applies or references the 'EndTurn' effect/state. | 14 |  |
| `RefreshActPoints` | Integer | Applies or references the 'RefreshActPoints' effect/state. | 14 |  |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Applies or references the 'TransformBasicAttack' effect/state. | 14 |  |
| [`ApplyPassives`](#applypassives) | Object | Grants the nested passive abilities dynamically. | 13 |  |
| [`Conditional_HasStatus`](#conditionalhasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 13 |  |
| [`Marked`](./Arrays.md#array-marked) | Array / Integer / Object | Applies or references the 'Marked' effect/state. | 13 |  |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | Applies or references the 'VisualFX' effect/state. | 13 |  |
| `AlphaCat` | Integer | Applies or references the 'AlphaCat' effect/state. | 2 |  |
| [`Conditional_Speculative`](#conditional_speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 |  |
| `Displace` | Integer | Applies or references the 'Displace' effect/state. | 12 |  |
| `instant` | Boolean | Examples: `true` | 12 |  |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | If true, treats the consumption as riding/mounting instead of eating. | 12 |  |
| `rock` | Variable |  | 46 |  |
| [`ChanceToBreakFree`](#chancetobreakfree) | Object | Provides a probability to escape a grapple or restraining effect. | 11 |  |
| `do_not_pop_corpse` | Boolean | Examples: `true` | 11 |  |
| [`DoScreenShake`](#doscreenshake) | Integer / Object | Triggers a camera screen shake effect. | 11 |  |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Examples: `false, true, deferred` | 11 |  |
| [`Instakill`](./Arrays.md#array-instakill) | Integer | Applies or references the 'Instakill' effect/state. | 11 |  |
| `PurgeAll` | Integer | Applies or references the 'PurgeAll' effect/state. | 11 |  |
| [`Conditional_FormulaIsPositive`](#conditional_formulaispositive) | Object | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 10 |  |
| `DexterityUp` | Enum / Integer | Applies or references the 'DexterityUp' effect/state. | 10 |  |
| `KnockbackDamageImmuneUntilSettled` | Integer | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 10 |  |
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer | Applies or references the 'MagicWeakness' effect/state. | 2 |  |
| `PartialPurge` | Integer | Applies or references the 'PartialPurge' effect/state. | 10 |  |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | Applies or references the 'SpawnThingIfHitKills' effect/state. | 10 |  |
| `X` | Variable |  | 10 |  |
| `Ammo` | Integer | Applies or references the 'Ammo' effect/state. | 9 |  |
| `ChanceToBreak` | Integer | Applies or references the 'ChanceToBreak' effect/state. | 9 |  |
| `Craft` | Object | Synthesizes or spawns a new item from a specific pool. | 2 |  |
| `DeferVaporize` | Integer | Applies or references the 'DeferVaporize' effect/state. | 9 |  |
| `IgnoreDamage` | Integer | Applies or references the 'IgnoreDamage' effect/state. | 9 |  |
| `OverrideChainKnockback` | Integer | Applies or references the 'OverrideChainKnockback' effect/state. | 9 |  |
| `SpawnCreep` | Integer | Applies or references the 'SpawnCreep' effect/state. | 9 |  |
| `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 8 |  |
| [`Conditional_Corpse`](#conditionalcorpse) | Object | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 8 |  |
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 |  |
| [`Grappled`](./Arrays.md#array-grappled) | Array / Integer | Applies or references the 'Grappled' effect/state. | 8 |  |
| `SpreadDisease` | Object | Provides a chance to transmit a disease status to adjacent targets. | 8 |  |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer | Applies or references the 'Tarred' effect/state. | 8 |  |
| `Tech` | Integer | Applies or references the 'Tech' effect/state. | 2 |  |
| `wet` | Boolean | Examples: `false, true` | 8 |  |
| `ApplyStatusIfCrit` | Object | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 7 |  |
| `BramblesOnHit` | Integer | Applies or references the 'BramblesOnHit' effect/state. | 7 |  |
| [`Conditional_InForm`](#conditional_inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 7 |  |
| [`Conditional_PlayerCat`](#conditional_playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 7 |  |
| `ContextualHeal` | Integer | Applies or references the 'ContextualHeal' effect/state. | 7 |  |
| `Drowsy` | Integer | Applies or references the 'Drowsy' effect/state. | 7 |  |
| `ForceAttack` | Integer / Object | Forces the character to execute an immediate attack. | 7 |  |
| [`form`](./Enums.md#enum-form) | Enum / Integer | The specific form ID to check for. | 7 |  |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum / Object | Applies or references the 'ImmediateUseAbility' effect/state. | 7 |  |
| `ManaSteal` | Integer | Applies or references the 'ManaSteal' effect/state. | 7 |  |
| `SetHealth` | Integer | Applies or references the 'SetHealth' effect/state. | 7 |  |
| `TempDamageUp` | Integer | Applies or references the 'TempDamageUp' effect/state. | 7 |  |
| `TempRangeUp` | Integer | Applies or references the 'TempRangeUp' effect/state. | 7 |  |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array / Number | Applies or references the 'TriggerWerewolfTransform' effect/state. | 7 |  |
| `VaporizeInanimate` | Integer | Applies or references the 'VaporizeInanimate' effect/state. | 7 |  |
| `BackflipWhenTargeted` | Enum / Integer / Object | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 2 |  |
| [`BounceRock`](./Enums.md#enum-bouncerock) | Array / Enum | Applies or references the 'BounceRock' effect/state. | 6 |  |
| `CaptureFamiliar` | Integer | Applies or references the 'CaptureFamiliar' effect/state. | 6 |  |
| `ClearStarving` | Integer | Applies or references the 'ClearStarving' effect/state. | 6 |  |
| [`Conditional_HealthThreshold`](#conditionalhealththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 6 |  |
| [`Conditional_Object`](#conditional_object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 |  |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum / Object | Adds a temporary bonus ability to the character's hand/deck. | 2 |  |
| `Die` | Integer / Object | Applies or references the 'Die' effect/state. | 6 |  |
| [`DoDistortionRing`](#dodistortionring) | Object | Creates a visual distortion ring effect on the screen. | 6 |  |
| `Doomed` | Integer | Applies or references the 'Doomed' effect/state. | 6 |  |
| `FactionConversion` | Integer | Applies or references the 'FactionConversion' effect/state. | 6 |  |
| [`FillMana`](./Arrays.md#array-fillmana) | Integer | Applies or references the 'FillMana' effect/state. | 6 |  |
| `FlatLeech` | Integer | Applies or references the 'FlatLeech' effect/state. | 6 |  |
| `FloatingRockTrap` | Integer | Applies or references the 'FloatingRockTrap' effect/state. | 6 |  |
| `ForceMoveTowards` | Integer | Applies or references the 'ForceMoveTowards' effect/state. | 6 |  |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 6 |  |
| `Metronome` | Integer / Object | Executes a random musical or metronome ability. | 4 |  |
| [`PopAndSpawn`](./Enums.md#enum-popandspawn) | Enum / Object | Destroys the target and replaces it with a new spawned entity. | 6 |  |
| `RandomInjury` | Integer | Applies or references the 'RandomInjury' effect/state. | 6 |  |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array / Integer / String | Applies or references the 'RandomStatDown' effect/state. | 6 |  |
| [`ScatterHeldCoin`](./Arrays.md#array-scatterheldcoin) | Array / Integer | Applies or references the 'ScatterHeldCoin' effect/state. | 6 |  |
| `SetDistanceDisplace` | Integer | Applies or references the 'SetDistanceDisplace' effect/state. | 6 |  |
| `SpiderInfested` | Integer | Applies or references the 'SpiderInfested' effect/state. | 6 |  |
| [`TeamCastAbility`](./Enums.md#enum-teamcastability) | Enum / Object | Requires or involves multiple characters to execute the ability. | 6 |  |
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum / Integer | Applies or references the 'TempSpeedUp' effect/state. | 6 |  |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 6 |  |
| [`TwisterDisplaceWithDamage`](#twisterdisplacewithdamage) | Object | A whirlwind effect that randomly displaces targets and deals damage. | 6 |  |
| [`UseAbility`](./Enums.md#enum-useability) | Enum / Object | Forces the character or target to instantly use a specified ability. | 6 |  |
| [`CollectsPickupsWithAltEffects`](#collectspickupswithalteffects) | Object | Triggers alternative nested effects when collecting items or pickups. | 5 |  |
| [`Conditional_IsSelf`](#conditional_isself) | Object | Conditional trigger: Executes nested logic if the target is the caster themselves. | 5 |  |
| `DestroyEquipmentAndAttachParasite` | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 5 |  |
| `DisplaceTowardsSource` | Integer | Applies or references the 'DisplaceTowardsSource' effect/state. | 5 |  |
| `FaceCamera` | Integer | Applies or references the 'FaceCamera' effect/state. | 5 |  |
| `ForceMoveAway` | Integer | Applies or references the 'ForceMoveAway' effect/state. | 5 |  |
| `HitExplosion` | Integer | Applies or references the 'HitExplosion' effect/state. | 5 |  |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Applies or references the 'Imprison' effect/state. | 5 |  |
| `KnockbackDirectionIsFacingDirection` | Enum / Integer | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. | 5 |  |
| `LavaTile` | Variable |  | 5 |  |
| `MonkStanceSwitch` | Integer | Applies or references the 'MonkStanceSwitch' effect/state. | 5 |  |
| `MovementUp` | Integer | Applies or references the 'MovementUp' effect/state. | 5 |  |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum / Object | Spawns a specific physics/item object upon impact. | 5 |  |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Applies or references the 'ObjectOnHitEmpty' effect/state. | 5 |  |
| `PermanentCharm` | Integer | Applies the 'PermanentCharm' effect. | 5 |  |
| `Purge` | Integer / Object | Applies or references the 'Purge' effect/state. | 2 |  |
| `RefreshMovePointsIfHit` | Integer | Applies or references the 'RefreshMovePointsIfHit' effect/state. | 5 |  |
| `SafeDie` | Integer | Applies or references the 'SafeDie' effect/state. | 5 |  |
| `SoulLink` | Integer / Object | Applies or references the 'SoulLink' effect/state. | 2 |  |
| `SpawnBearTrap` | Integer | Applies or references the 'SpawnBearTrap' effect/state. | 5 |  |
| [`SpawnRock`](./Arrays.md#array-spawnrock) | Array / Integer | Applies or references the 'SpawnRock' effect/state. | 5 |  |
| [`SpecificInjury`](./Enums.md#enum-specificinjury) | Enum | Applies or references the 'SpecificInjury' effect/state. | 5 |  |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer | Applies or references the 'Stealth' effect/state. | 2 |  |
| `UpgradeRandomAbility` | Integer | Applies or references the 'UpgradeRandomAbility' effect/state. | 5 |  |
| [`ApplyToConsumed`](#applytoconsumed) | Object | Redirects the nested effects to apply to the entity that just consumed this object. | 4 |  |
| [`ArcLightning`](#arclightning) | Object | Executes a chain-lightning logic block that bounces between targets. | 4 |  |
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array / Integer | Applies or references the 'BurgleCoin' effect/state. | 4 |  |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Applies or references the 'CompleteItemQuest' effect/state. | 4 |  |
| [`Conditional_Adjacent`](#conditional_adjacent) | Object | Conditional constraint. Nested properties only trigger if this is true. | 4 |  |
| [`Conditional_Familiar`](#conditional_familiar) | Object | Conditional trigger: Executes nested logic if the target is a familiar. | 4 |  |
| [`Default`](./Enums.md#enum-default) | Enum / Object | `release` | 199 |  |
| `DeleteObject` | Integer | Applies or references the 'DeleteObject' effect/state. | 4 |  |
| `DestroyTrinket` | Integer | Applies or references the 'DestroyTrinket' effect/state. | 4 |  |
| `DieViolently` | Integer | Applies or references the 'DieViolently' effect/state. | 4 |  |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Applies or references the 'EnableWeather' effect/state. | 4 |  |
| `ExplosionIfHitSomething` | Integer | Applies or references the 'ExplosionIfHitSomething' effect/state. | 4 |  |
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum | Examples: `alien, robot, ghost` | 4 |  |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 4 |  |
| `FreeSpell` | Integer | Applies or references the 'FreeSpell' effect/state. | 4 |  |
| [`LateStatusApplication`](#latestatusapplication) | Object | Applies a status effect after all primary damage and effects have fully resolved. | 4 |  |
| `LowerAmbientLight` | Object | A visual effect that dims the map's lighting. | 4 |  |
| `moonhand` | Variable |  | 4 |  |
| `Rain` | Object | Character Form: Behavior and stats for the 'Rain' state. | 1 |  |
| `Reanimate` | Integer / Object | Applies or references the 'Reanimate' effect/state. | 4 |  |
| `RefreshWeaponAbility` | Integer | Applies or references the 'RefreshWeaponAbility' effect/state. | 4 |  |
| `RemoveActPoints` | Integer | Applies or references the 'RemoveActPoints' effect/state. | 4 |  |
| `RepairAll` | Integer | Applies or references the 'RepairAll' effect/state. | 4 |  |
| `SendRock` | Integer | Applies or references the 'SendRock' effect/state. | 4 |  |
| [`SwitchMusic`](#switchmusic) | Object | Changes the background music track or layer during combat. | 4 |  |
| `TakeBonusTurnWithStatus` | Object | Grants the character an immediate extra turn while afflicted with specific statuses. | 4 |  |
| [`TempPassiveWhileHasStatus`](#temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 4 |  |
| `Thrash` | Object |  | 4 |  |
| [`TimeDelayStatusApplication`](#timedelaystatusapplication) | Object | Delays the nested effects by a specified amount of real-time seconds. | 4 |  |
| `Windy` | Integer | Examples: `{ ... }` | 1 |  |
| `AddWeaponAux` | Integer / String | Applies or references the 'AddWeaponAux' effect/state. | 3 |  |
| [`ApplyMultipleTimes`](#applymultipletimes) | Object | A loop object that executes its nested logic multiple times. | 3 |  |
| `Attraction` | Integer | Applies or references the 'Attraction' effect/state. | 3 |  |
| `BlackShard` | Object |  | 8 |  |
| `BonusKnockbackDamage` | Integer | Applies or references the 'BonusKnockbackDamage' effect/state. | 3 |  |
| [`CatPartsSizeScaleStatus`](#catpartssizescalestatus) | Object | Visually scales specific body parts of a character. | 3 |  |
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | Applies or references the 'CollideWithConsumed' effect/state. | 3 |  |
| [`Conditional_AffectedByElement`](#conditional_affectedbyelement) | Object | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 3 |  |
| [`Conditional_FirstApplicationThisTurn`](#conditionalfirstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 3 |  |
| [`Conditional_LastHit`](#conditional_lasthit) | Object | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 3 |  |
| [`Conditional_OncePerBattle`](#conditional_onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 3 |  |
| `CorpseVaporizer` | Integer | Applies or references the 'CorpseVaporizer' effect/state. | 3 |  |
| `CurrentWeaponDamageUp` | Integer | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 3 |  |
| `DestroyWeapon` | Integer | Applies or references the 'DestroyWeapon' effect/state. | 3 |  |
| `DestroyWeaponThrow` | Integer | Applies or references the 'DestroyWeaponThrow' effect/state. | 3 |  |
| `DisplaceToAbilityTarget` | Integer | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 3 |  |
| `DoDamage` | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 3 |  |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | Applies or references the 'DoubleStatus' effect/state. | 3 |  |
| `drop_on_self_death` | Boolean | Examples: `true` | 3 |  |
| [`DustOnHit`](#dustonhit) | Object | Spawns a specific particle or cloud object upon impact. | 3 |  |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type to check for. | 1 |  |
| [`extra_statuses`](#extra_statuses) | Object | Additional generic status applications. | 3 |  |
| `ExtraBasicAttacks_Status` | Integer | Applies or references the 'ExtraBasicAttacks_Status' effect/state. | 3 |  |
| `FlatAIBonus` | Integer | Applies or references the 'FlatAIBonus' effect/state. | 3 |  |
| `ForceDisplace` | Integer | Applies or references the 'ForceDisplace' effect/state. | 3 |  |
| `ForceMoveTowardsEnemies` | Enum / Integer | Applies or references the 'ForceMoveTowardsEnemies' effect/state. | 3 |  |
| `Hex` | Integer | Applies or references the 'Hex' effect/state. | 3 |  |
| `InstantMaxHealthUp` | Integer | Applies or references the 'InstantMaxHealthUp' effect/state. | 3 |  |
| `Meteornado` | Integer | Examples: `1` | 3 |  |
| `NextAttackBonusRange` | Integer | Applies or references the 'NextAttackBonusRange' effect/state. | 3 |  |
| `PlayBackground` | Integer | Applies or references the 'PlayBackground' effect/state. | 3 |  |
| `PoisonLace` | Integer / Object / String | Applies or references the 'PoisonLace' effect/state. | 2 |  |
| `poop` | Object | Event Object: Story branch or dialog option representing the \'Poop\' action. | 2 |  |
| `PullSourceToTarget` | Integer | Applies or references the 'PullSourceToTarget' effect/state. | 3 |  |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Applies or references the 'RemoveItem' effect/state. | 3 |  |
| `RemoveMovePoints` | Integer | Applies or references the 'RemoveMovePoints' effect/state. | 3 |  |
| `RepairOnKill` | Integer | Applies or references the 'RepairOnKill' effect/state. | 3 |  |
| `ReviveNextRound` | Integer / Object | Queues the character to be resurrected at the start of the next combat round. | 3 |  |
| [`SetCrazyEyeBackgroundWeights`](#setcrazyeyebackgroundweights) | Object | Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 3 |  |
| `SetShield` | Integer | Applies or references the 'SetShield' effect/state. | 3 |  |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 3 |  |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Applies or references the 'SpawnCustomTrap' effect/state. | 3 |  |
| `SpawnNeutralWebTrapOnMiss` | Integer | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. | 3 |  |
| [`SpawnVolcanoOnBattleStart`](#spawnvolcanoonbattlestart) | Object | Examples: `{ ... }` | 3 |  |
| `SpeculativeMoveSelfCorpseOffMap` | Integer | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 3 |  |
| `StanceSwitchToMelee` | Integer | Applies or references the 'StanceSwitchToMelee' effect/state. | 3 |  |
| [`StatusCharactersOnRoundEnd`](#statuscharactersonroundend) | Object | Examples: `{ ... }` | 3 |  |
| `TempInitiativeChange` | Integer | Applies or references the 'TempInitiativeChange' effect/state. | 3 |  |
| `TempStrengthUp` | Equation | Applies or references the 'TempStrengthUp' effect/state. | 3 |  |
| `TempTrampleUntilSettled` | Integer | Applies or references the 'TempTrampleUntilSettled' effect/state. | 3 |  |
| `TriggerGameEnding` | Integer | Applies or references the 'TriggerGameEnding' effect/state. | 3 |  |
| `VaporizeTarget` | Integer | Applies or references the 'VaporizeTarget' effect/state. | 3 |  |
| `WaterTile` | Variable |  | 3 |  |
| `ZombieCatFamiliar` | Object |  | 4 |  |
| `AddLeechesStatus` | Integer | Applies or references the 'AddLeechesStatus' effect/state. | 2 |  |
| `AddSpiritBombCharges` | Integer | Applies or references the 'AddSpiritBombCharges' effect/state. | 2 |  |
| [`ApplyToRandomPartyMemberIfPossible`](#applytorandompartymemberifpossible) | Object | Redirects the nested effects to apply to a random living member of the player's party. | 2 |  |
| [`ApplyToTile`](#applytotile) | Object | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 2 |  |
| `AutoReanimate` | Number | Examples: `50` | 2 |  |
| [`BodyGuard`](#bodyguard) | Object | Protects an ally by intercepting attacks directed at them. | 2 |  |
| `BonusDamageBasedOnDistance` | Integer | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 2 |  |
| `Bound` | Integer | Applies or references the 'Bound' effect/state. | 2 |  |
| `CancelPrimedAbilities` | Integer | Applies or references the 'CancelPrimedAbilities' effect/state. | 2 |  |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Applies or references the 'ChangeFaction' effect/state. | 2 |  |
| [`CharacterTypeGainsStatusAtBattleStart`](#charactertypegainsstatusatbattlestart) | Object | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. | 1 |  |
| `CharmedForceAttack` | Integer | Applies or references the 'CharmedForceAttack' effect/state. | 2 |  |
| `ClearNegativeEffects` | Integer | Applies the 'ClearNegativeEffects' effect. | 2 |  |
| `CollideWithThrowTarget` | Integer | Applies or references the 'CollideWithThrowTarget' effect/state. | 2 |  |
| [`Conditional_BadRoll`](#conditional_badroll) | Object | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 2 |  |
| [`Conditional_BossOrBig`](#conditional_bossorbig) | Object | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 2 |  |
| [`Conditional_Buddy`](#conditional_buddy) | Object | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 2 |  |
| [`Conditional_DestructibleCorpse`](#conditional_destructiblecorpse) | Object | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 2 |  |
| [`Conditional_Displaceable`](#conditional_displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |  |
| [`Conditional_NotAlly`](#conditional_notally) | Object | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 2 |  |
| [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Object | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 2 |  |
| [`Conditional_NotShielded`](#conditional_notshielded) | Object | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 2 |  |
| [`Conditional_PartyMember`](#conditional_partymember) | Object | Conditional constraint. Nested properties only trigger if this is true. | 2 |  |
| [`Conditional_Shielded`](#conditional_shielded) | Object | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 2 |  |
| `ConjureRandomAbilityFromCat` | Integer | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 2 |  |
| `CopySpells` | Integer / Object | Duplicates existing spells currently in the character's hand. | 2 |  |
| `Counterspell` | Integer / Object | Applies or references the 'Counterspell' effect/state. | 2 |  |
| `DamageBasedOnMissingHealth` | Integer | Applies or references the 'DamageBasedOnMissingHealth' effect/state. | 2 |  |
| `DamageDistanceAOEFalloff` | Integer | Applies or references the 'DamageDistanceAOEFalloff' effect/state. | 2 |  |
| `DamageTrinket` | Integer | Applies or references the 'DamageTrinket' effect/state. | 2 |  |
| [`DelayCastAbility`](./Enums.md#enum-delaycastability) | Enum / Object | Queues an ability to be cast automatically after a certain delay or trigger. | 2 |  |
| `DelayedFury` | Integer | Applies or references the 'DelayedFury' effect/state. | 2 |  |
| `DieViaAbilityInternally` | Integer | Applies or references the 'DieViaAbilityInternally' effect/state. | 2 |  |
| `DisplaceToOriginalPosition` | Integer | Applies or references the 'DisplaceToOriginalPosition' effect/state. | 2 |  |
| `DoubleCastSpell` | Integer | Applies or references the 'DoubleCastSpell' effect/state. | 2 |  |
| `DoubleLoot` | Integer / Object | Applies or references the 'DoubleLoot' effect/state. | 2 |  |
| `ExplodeCharacter` | Integer | Applies or references the 'ExplodeCharacter' effect/state. | 2 |  |
| `ExplodeCharacter_NoDie` | Integer | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 2 |  |
| `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 2 |  |
| `ExplodeCharacter_RockCrusher` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 2 |  |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 2 |  |
| `FireStorm` | Integer | Examples: `33, 0` | 2 |  |
| `FireTile` | Variable |  | 2 |  |
| `FlatLeechIfDamaged` | Integer | Applies or references the 'FlatLeechIfDamaged' effect/state. | 2 |  |
| `FlowersOnHit` | Integer | Applies or references the 'FlowersOnHit' effect/state. | 2 |  |
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. | 2 |  |
| [`ForceMoveTowardsTaggedObject`](#forcemovetowardstaggedobject) | Object | Forces the character to move towards the nearest object with a specific tag. | 2 |  |
| [`GainDisorderFromPool`](./Enums.md#enum-gaindisorderfrompool) | Enum / Object | Logic: Applies a negative mutation/disorder from a specific pool. | 2 |  |
| `gamewin` | Variable |  | 2 |  |
| [`GlobalSpawnOnRoundEnd`](#globalspawnonroundend) | Object | Examples: `{ ... }` | 2 |  |
| `HealRandomInjury` | Integer | Applies or references the 'HealRandomInjury' effect/state. | 2 |  |
| `HornCharge` | Object |  | 2 |  |
| `humanoid` | Variable |  | 2 |  |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. | 2 |  |
| `JohnnyCriesForWashers` | Integer | Applies or references the 'JohnnyCriesForWashers' effect/state. | 2 |  |
| `LeaveBehindRockOnKnockback` | Integer | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 2 |  |
| `ManaLeeches` | Integer | Applies or references the 'ManaLeeches' effect/state. | 2 |  |
| [`Math`](#math) | Object | Triggers the Tinkerer's Math ability sequence. | 2 |  |
| `MaxHPUp` | Integer | Applies or references the 'MaxHPUp' effect/state. | 2 |  |
| `megadino` | Variable |  | 1 |  |
| `moonhead` | Variable |  | 1 |  |
| `NextAttackSpecialCrit` | Integer / Object | Modifies the character's next attack to have special critical properties. | 2 |  |
| `OffMap` | Object | Character Form: Behavior and stats for the 'OffMap' state. | 2 |  |
| `OilTile` | Variable |  | 2 |  |
| `Ostracized` | Integer | Applies or references the 'Ostracized' effect/state. | 2 |  |
| [`OverHealToStatuses`](#overhealtostatuses) | Object | Converts excessive healing beyond maximum health into specific status effects. | 2 |  |
| `PartyExplosion` | Variable |  | 2 |  |
| `PermanentStrength` | Integer | Applies or references the 'PermanentStrength' effect/state. | 2 |  |
| `PermanentUpgradeRandomActive` | Integer | Applies or references the 'PermanentUpgradeRandomActive' effect/state. | 2 |  |
| `Pilfer` | Object |  | 2 |  |
| `Possessed` | Integer | Applies or references the 'Possessed' effect/state. | 2 |  |
| `PullSourceToKnockbackImmuneTarget` | Integer | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. | 2 |  |
| `Pulp2` | Object | Character Form: Behavior and stats for the 'Pulp2' state. | 2 |  |
| [`QuakeAreaChance`](#quakeareachance) | Object | Provides a probability to trigger an earthquake Area of Effect. | 2 |  |
| `RandomDistanceDisplace` | Integer / Object | Displaces the target by a randomized distance. | 2 |  |
| [`RandomKnockback`](#randomknockback) | Object | Applies a randomized amount of knockback force. | 2 |  |
| `RandomLightning` | Integer | Examples: `50` | 2 |  |
| `RandomPickup` | Object |  | 2 |  |
| `RebukeDamage` | Integer | Applies or references the 'RebukeDamage' effect/state. | 2 |  |
| `ReduceManaCost` | Integer | Applies or references the 'ReduceManaCost' effect/state. | 2 |  |
| `RemoveKnockback` | Integer | Applies or references the 'RemoveKnockback' effect/state. | 2 |  |
| `RemoveStatusStacks` | Object | Removes a specific number of stacks of a status effect. | 2 |  |
| `RepairArmorCondition` | Integer | Applies or references the 'RepairArmorCondition' effect/state. | 2 |  |
| `RepairWeaponCondition` | Integer | Applies or references the 'RepairWeaponCondition' effect/state. | 2 |  |
| `ResetArmorShield` | Integer | Applies or references the 'ResetArmorShield' effect/state. | 2 |  |
| `ScatterRandomPickups` | Integer | Applies or references the 'ScatterRandomPickups' effect/state. | 2 |  |
| `ScrambleEverything` | Integer | Applies or references the 'ScrambleEverything' effect/state. | 2 |  |
| [`SelfStun`](./Arrays.md#array-selfstun) | Array / Integer | Applies or references the 'SelfStun' effect/state. | 2 |  |
| `SetKnockback` | Integer | Applies or references the 'SetKnockback' effect/state. | 2 |  |
| `Shatter` | Integer / Object | Applies or references the 'Shatter' effect/state. | 2 |  |
| `SignalFinalBossShieldBroke` | Integer | Applies or references the 'SignalFinalBossShieldBroke' effect/state. | 2 |  |
| `SmartMetronome` | Integer / Object | Executes a 'smart' random ability that aims to be beneficial based on context. | 4 |  |
| `Snow` | Integer | Examples: `{ ... }` | 1 |  |
| `SpawnBearTrapIfHitKills` | Integer | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 2 |  |
| [`SpawnFlames`](./Arrays.md#array-spawnflames) | Array | Applies or references the 'SpawnFlames' effect/state. | 2 |  |
| [`SpecialGodRays`](#specialgodrays) | Object | Examples: `{ ... }` | 2 |  |
| [`StatusCharactersOnRoundStart`](#statuscharactersonroundstart) | Object | Examples: `{ ... }` | 2 |  |
| `SwallowSmallCharacter` | Integer | Applies or references the 'SwallowSmallCharacter' effect/state. | 2 |  |
| [`TakeBonusTurnWithAIControl`](#takebonusturnwithaicontrol) | Object | Grants the character an immediate extra turn, but forces the AI to control them during it. | 2 |  |
| `TallGrassTile` | Number | Examples: `80, 15` | 2 |  |
| `TempCritChanceUp` | Integer | Applies or references the 'TempCritChanceUp' effect/state. | 2 |  |
| [`TempDexterityUp`](./Enums.md#enum-tempdexterityup) | Enum | Applies or references the 'TempDexterityUp' effect/state. | 2 |  |
| `TempMovement` | Enum / Integer | Applies or references the 'TempMovement' effect/state. | 2 |  |
| `TempPassiveUntilSettled` | Object | Passive: Active only until the physics engine stops moving the character. | 2 |  |
| `TempSpellDamageUp` | Integer | Applies or references the 'TempSpellDamageUp' effect/state. | 2 |  |
| `the_coven` | Variable |  | 2 |  |
| `ThornsDamageImmuneUntilSettled` | Integer | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 2 |  |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 |  |
| `ThrowPoop` | Object |  | 2 |  |
| `TileDamageImmuneUntilSettled` | Integer | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 2 |  |
| `TradeLife` | Integer / Object | Applies or references the 'TradeLife' effect/state. | 2 |  |
| `TrailBlazer` | Enum / Integer / Object | Applies or references the 'TrailBlazer' effect/state. | 2 |  |
| `TriggerDOTStatuses` | Integer | Applies or references the 'TriggerDOTStatuses' effect/state. | 2 |  |
| `VisualFlySwarm` | Integer | Examples: `1` | 2 |  |
| [`XIsTargetHealth`](#xistargethealth) | Object | Math variable assignment: Evaluates X as the target's current health. | 2 |  |
| `AcidRain` | Integer | Examples: `2` | 1 |  |
| `AddExtraTurnsBeforeRun` | Integer | Examples: `2` | 1 |  |
| [`AddPostProcessEffect`](#addpostprocesseffect) | Object | Examples: `{ ... }` | 1 |  |
| [`AddTilesetObjects`](#addtilesetobjects) | Object | Examples: `{ ... }` | 1 |  |
| `Adrenaline` | Integer | Applies or references the 'Adrenaline' effect/state. | 1 |  |
| `AIFavorLowHealth` | Integer | Applies or references the 'AIFavorLowHealth' effect/state. | 1 |  |
| `alien` | Variable |  | 1 |  |
| `AlliesTakeExtraTurn` | Integer | Applies or references the 'AlliesTakeExtraTurn' effect/state. | 1 |  |
| [`AllyInfested`](#allyinfested) | Object | Examples: `{ ... }` | 1 |  |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Applies or references the 'AlternateIdleAnimation' effect/state. | 1 |  |
| `angeljunk` | Variable |  | 1 |  |
| `AntlerSwipe` | Object |  | 2 |  |
| `AntlerSwipe2` | Object |  | 1 |  |
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. | 1 |  |
| [`ApplyStatusesNextTurnBegin`](#applystatusesnextturnbegin) | Object | Delays the application of the nested status effects until the start of the target's next turn. | 1 |  |
| [`ApplyToOthersWithSharedTagAndFaction`](#applytootherswithsharedtagandfaction) | Object | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 1 |  |
| [`ApplyToRandomClosestAlly`](#applytorandomclosestally) | Object | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 1 |  |
| `BasicDashAttackMove_NoKnockback` | Object |  | 1 |  |
| `BerserkDash` | Object |  | 2 |  |
| `berserkIdle` | Variable |  | 1 |  |
| `BirthSquirrel` | Object |  | 4 |  |
| `BlackHoleSuck` | Integer | Applies or references the 'BlackHoleSuck' effect/state. | 1 |  |
| `BlankTile` | Number | Examples: `5` | 2 |  |
| `Bloodzerked` | Integer | Applies or references the 'Bloodzerked' effect/state. | 1 |  |
| `BombRatTurtle` | Integer / Object | Applies or references the 'BombRatTurtle' effect/state. | 1 |  |
| `bonusbird` | Variable |  | 1 |  |
| `BonusDamageBasedOnMana` | Integer | Applies or references the 'BonusDamageBasedOnMana' effect/state. | 1 |  |
| [`Boris`](./Enums.md#enum-boris) | Enum / Object | `MegaGuppy_TransformBoris` | 1 |  |
| `Boulder` | Object |  | 2 |  |
| `BrambleTile` | Variable |  | 1 |  |
| `ButterflySwarm` | Integer | Examples: `2` | 1 |  |
| `BypassRockKnockback` | Integer | Applies or references the 'BypassRockKnockback' effect/state. | 1 |  |
| `CanceledQueuedInput` | Integer | Applies or references the 'CanceledQueuedInput' effect/state. | 1 |  |
| `CapDamage` | Integer | Applies or references the 'CapDamage' effect/state. | 1 |  |
| `ChampionUpgradeNextMinion` | Integer | Applies or references the 'ChampionUpgradeNextMinion' effect/state. | 1 |  |
| `ChaosBossFlipMidTeleport` | Integer | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. | 1 |  |
| `ChaosBossFormChange` | Integer | Applies or references the 'ChaosBossFormChange' effect/state. | 1 |  |
| `chapter_corpse_medium` | Variable |  | 1 |  |
| `ChargeFists` | Integer / Object | Applies or references the 'ChargeFists' effect/state. | 2 |  |
| `CharmedFacingForceAttack` | Integer | Applies or references the 'CharmedFacingForceAttack' effect/state. | 1 |  |
| `CharmTrap` | Object |  | 2 |  |
| `Chitter` | Object |  | 1 |  |
| `ClearDefaultDebris` | Integer | Examples: `1` | 1 |  |
| `ClearFinalBossBattlefield` | Integer | Applies or references the 'ClearFinalBossBattlefield' effect/state. | 1 |  |
| `CloneWeaponTemp` | Integer | Applies or references the 'CloneWeaponTemp' effect/state. | 1 |  |
| `cm_RaptorEggSpawn` | Object |  | 1 |  |
| `CockroachSwarm` | Integer | Examples: `1` | 1 |  |
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum | Applies or references the 'CoinTossBounce' effect/state. | 1 |  |
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
| [`Conditional_ManaThreshold`](#conditional_manathreshold) | Object | Conditional constraint. Nested properties only trigger if this is true. | 1 |  |
| [`Conditional_NotBig`](#conditional_notbig) | Object | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 1 |  |
| [`Conditional_RandomChance`](#conditional_randomchance) | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 1 |  |
| [`Conditional_SourceAbilityHasTag`](#conditional_sourceabilityhastag) | Object | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 1 |  |
| [`Conditional_SourceHasStatus`](#conditional_sourcehasstatus) | Object | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 1 |  |
| [`Conditional_SourceHasTag`](#conditional_sourcehastag) | Object | Examples: `{ ... }` | 1 |  |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. | 1 |  |
| `container` | Variable |  | 1 |  |
| `CrackMoonHead` | Integer | Applies or references the 'CrackMoonHead' effect/state. | 1 |  |
| `CurrentWeaponAddElectricElement` | Integer | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. | 1 |  |
| `DamageWeapon` | Integer | Applies or references the 'DamageWeapon' effect/state. | 1 |  |
| `DeathWormEat` | Object |  | 1 |  |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Applies or references the 'DeathwormUnderground' effect/state. | 1 |  |
| `DecoySwapper` | Integer | Applies or references the 'DecoySwapper' effect/state. | 1 |  |
| `deferred` | Boolean | `true` | 1 |  |
| [`DelayedWindCone`](#delayedwindcone) | Object | Creates a delayed Area of Effect cone. | 1 |  |
| `DeleteInanimateObjectsChance` | Integer | Examples: `25` | 1 |  |
| `DeleteTraps` | Integer | Applies or references the 'DeleteTraps' effect/state. | 1 |  |
| `DestroyNeckArmor` | Integer | Applies or references the 'DestroyNeckArmor' effect/state. | 1 |  |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Applies or references the 'DinoLegAnimation' effect/state. | 1 |  |
| `DirtTile` | Variable |  | 1 |  |
| `DisableWeapon` | Integer | Applies or references the 'DisableWeapon' effect/state. | 1 |  |
| `Disguised` | Integer | Applies or references the 'Disguised' effect/state. | 1 |  |
| `DissolveRandomArmorPiece` | Integer | Applies or references the 'DissolveRandomArmorPiece' effect/state. | 1 |  |
| `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. | 1 |  |
| `DoubleCast` | Integer | Applies or references the 'DoubleCast' effect/state. | 1 |  |
| `DoubleCastSpellsEachTurn_Status` | Integer | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. | 1 |  |
| `DrainAllyCatsForFleshGolem` | Integer | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. | 1 |  |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Examples: `MoonHandDrop` | 1 |  |
| [`Druid`](./Arrays.md#array-druid) | Object | Applies or references the 'Druid' effect/state. | 80 |  |
| `DualSword` | Object | Character Form: Behavior and stats for the \'DualSword\' state. | 1 |  |
| `DuplicateRandomEquippedItem` | Integer | Applies or references the 'DuplicateRandomEquippedItem' effect/state. | 1 |  |
| `DybbukManualExitTag` | Variable |  | 1 |  |
| [`DybbukPossessed`](#dybbukpossessed) | Object | Defines the abilities and behaviors available when possessing another entity. | 1 |  |
| `EggSackTrap` | Variable |  | 1 |  |
| `EliteUpgradeNextMinion` | Integer | Applies or references the 'EliteUpgradeNextMinion' effect/state. | 1 |  |
| `EmptyMind` | Integer / Object | Applies or references the 'EmptyMind' effect/state. | 2 |  |
| `Enlarge` | Integer / Object | Applies or references the 'Enlarge' effect/state. | 2 |  |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Applies or references the 'EnterMount' effect/state. | 1 |  |
| `EtherSoakedRag` | Object |  | 1 |  |
| `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. | 1 |  |
| `ExistUntilIdleUpkeep` | Integer | Applies or references the 'ExistUntilIdleUpkeep' effect/state. | 1 |  |
| `ExplodeCharacter_DeathBloom` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. | 1 |  |
| `ExplodeCharacter_DeathBloom2` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. | 1 |  |
| `ExplodeCharacter_Party` | Integer | Applies or references the 'ExplodeCharacter_Party' effect/state. | 1 |  |
| [`Explosive`](./Enums.md#enum-explosive) | Enum / Object | `MegaGuppy_TransformExplosive` | 1 |  |
| `FactionDisguiseSource` | Integer | Applies or references the 'FactionDisguiseSource' effect/state. | 1 |  |
| `FastKnockback` | Integer | Applies or references the 'FastKnockback' effect/state. | 1 |  |
| [`Fighter`](./Arrays.md#array-fighter) | Object | Applies or references the 'Fighter' effect/state. | 80 |  |
| `FinalBossQueueBeam` | Integer | Applies or references the 'FinalBossQueueBeam' effect/state. | 1 |  |
| `FireArmor` | Integer / Object | Applies or references the 'FireArmor' effect/state. | 1 |  |
| `FireArmor2` | Integer / Object | Applies or references the 'FireArmor2' effect/state. | 1 |  |
| `FireflySwarm` | Integer | Examples: `2` | 1 |  |
| `flip` | Variable |  | 2 |  |
| `FlySwarm` | Object | Examples: `50` | 5 |  |
| `Fog` | Integer | Examples: `1` | 1 |  |
| `ForceCollectsPickups` | Integer | Applies or references the 'ForceCollectsPickups' effect/state. | 1 |  |
| `ForceImmediateMove` | Integer | Applies or references the 'ForceImmediateMove' effect/state. | 1 |  |
| [`ForceImmediateMoveAndAttack`](#forceimmediatemoveandattack) | Object | Forces the character to immediately move to a target and use a specified ability. | 1 |  |
| `ForceMoveAndAttack` | Integer | Applies or references the 'ForceMoveAndAttack' effect/state. | 1 |  |
| `ForceTransferWeapon` | Integer | Applies or references the 'ForceTransferWeapon' effect/state. | 1 |  |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Applies or references the 'GainDisorder' effect/state. | 1 |  |
| `GenericBuff` | Integer | Applies or references the 'GenericBuff' effect/state. | 1 |  |
| `ghost` | Variable |  | 1 |  |
| `GiveBoundItemToTarget` | Integer | Applies or references the 'GiveBoundItemToTarget' effect/state. | 1 |  |
| `GlassTile` | Variable |  | 1 |  |
| `GlobalHealthRegenAura` | Integer | Examples: `3` | 1 |  |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |  |
| `god` | Variable |  | 1 |  |
| `Grown` | Object | Character Form: Behavior and stats for the \'Grown\' state. | 1 |  |
| `grown_hitler_clone` | Variable |  | 1 |  |
| `HalfDead` | Object | Character Form: Behavior and stats for the \'HalfDead\' state. | 1 |  |
| `HardenSkin` | Object |  | 2 |  |
| `HardenSkin2` | Object |  | 1 |  |
| `head_CrownOfHorns` | Object |  | 1 |  |
| `HeadTumor` | Object |  | 3 |  |
| `HealPercentMaxHP` | Integer | Applies or references the 'HealPercentMaxHP' effect/state. | 1 |  |
| `HealTo` | Integer | Applies or references the 'HealTo' effect/state. | 1 |  |
| `HeatWave` | Integer | Examples: `1` | 1 |  |
| `HeavyHits` | Integer | Applies or references the 'HeavyHits' effect/state. | 1 |  |
| `hitler_clone` | Variable |  | 1 |  |
| `hitler_clone_fetus` | Variable |  | 1 |  |
| `IceArmor` | Integer / Object | Applies or references the 'IceArmor' effect/state. | 2 |  |
| `IgnoreDebuffs` | Integer | Applies or references the 'IgnoreDebuffs' effect/state. | 1 |  |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. | 1 |  |
| [`IncAuxCounterCycle`](#incauxcountercycle) | Object | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 1 |  |
| `IncreaseCumulativeBlastDamage` | Integer | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. | 1 |  |
| `IncreaseItemAuxOnKill` | Integer | Applies or references the 'IncreaseItemAuxOnKill' effect/state. | 1 |  |
| `Infested` | Integer / Object | data/elite_buffs.gon | 1 |  |
| `InterchangeMoveActPoints` | Integer | Applies or references the 'InterchangeMoveActPoints' effect/state. | 1 |  |
| `Invulnerable` | Integer | Applies or references the 'Invulnerable' effect/state. | 1 |  |
| `JesterMinusColorless` | Variable |  | 1 |  |
| `JewelOfDrog` | Object |  | 1 |  |
| `JudgementDay` | Integer | Examples: `25` | 1 |  |
| `kill_on_consume` | Boolean | Examples: `true` | 1 |  |
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | Applies or references the 'KnockOutClone' effect/state. | 1 |  |
| [`LaunchOffScreen`](./Math_Equations.md) | Equation | Applies or references the 'LaunchOffScreen' effect/state. | 1 |  |
| `LaunchOffScreenInstakill` | Integer | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 1 |  |
| `LowGravityKnockbackBoost` | Integer | Examples: `1` | 1 |  |
| `LowGravityRangeBoost` | Integer | Examples: `2` | 1 |  |
| `MadnessChanceOnTurnBegin` | Integer | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 |  |
| `MakeWeaponUnbreakable` | Integer | Applies or references the 'MakeWeaponUnbreakable' effect/state. | 1 |  |
| `ManaStealToHealth` | Integer | Applies or references the 'ManaStealToHealth' effect/state. | 1 |  |
| `ManglerAttack` | Integer | Applies or references the 'ManglerAttack' effect/state. | 1 |  |
| `ManglerShuffle` | Boolean | Applies or references the 'ManglerShuffle' effect/state. | 1 |  |
| `MassAttackThis` | Integer | Applies or references the 'MassAttackThis' effect/state. | 1 |  |
| `Meaty` | Integer | Applies or references the 'Meaty' effect/state. | 1 |  |
| `MegaGuppy` | Object |  | 1 |  |
| [`MergeDamageInstance`](#mergedamageinstance) | Object | Combines damage numbers or visual hit effects. | 1 |  |
| `MeteorShower` | Integer | Examples: `25` | 1 |  |
| `MimicMetronome` | Integer | Applies or references the 'MimicMetronome' effect/state. | 1 |  |
| `MockSong` | Object |  | 1 |  |
| `MockSong2` | Object |  | 1 |  |
| [`Monk`](./Arrays.md#array-monk) | Object | Applies or references the 'Monk' effect/state. | 66 |  |
| `MonkeyThrow` | Object |  | 2 |  |
| `MonkeyThrow2` | Object |  | 1 |  |
| `MoonHandDrop` | Object |  | 2 |  |
| `MoonHeadFlail` | Object |  | 1 |  |
| `MotherTumorDebugForcePass` | Integer | Applies or references the 'MotherTumorDebugForcePass' effect/state. | 1 |  |
| `Muted` | Integer | Applies or references the 'Muted' effect/state. | 1 |  |
| `NextAbilityHeals` | Integer | Applies or references the 'NextAbilityHeals' effect/state. | 1 |  |
| `NextActionLuckUp` | Integer | Applies or references the 'NextActionLuckUp' effect/state. | 1 |  |
| [`NextBasicAttackCritsThisTurn`](#nextbasicattackcritsthisturn) | Object | Guarantees the next basic attack executed this turn will be a critical hit. | 1 |  |
| [`NextBattleStatusStacks`](#nextbattlestatusstacks) | Object | Carries over the specified status effects into the next encounter/battle. | 1 |  |
| `NextDamageReduceAndHealAllies` | Integer | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. | 1 |  |
| `NextTurnDoubleRangedDamage` | Integer | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. | 1 |  |
| `NoDeathrattle` | Variable |  | 1 |  |
| `Normal` | Integer / Object | Character Form: Behavior and stats for the \'Normal\' state. | 24 |  |
| `Nuke` | Object | Character Form: Behavior and stats for the 'Nuke' state. | 10 |  |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. | 1 |  |
| `OverHealToShield` | Integer | Applies or references the 'OverHealToShield' effect/state. | 1 |  |
| `OverrideChainKnockbackDamage` | Equation | Applies or references the 'OverrideChainKnockbackDamage' effect/state. | 1 |  |
| `PermanentCharisma` | Integer | Applies or references the 'PermanentCharisma' effect/state. | 1 |  |
| `PermanentImmobile` | Integer | Applies or references the 'PermanentImmobile' effect/state. | 1 |  |
| `PermanentLuck` | Integer | Applies or references the 'PermanentLuck' effect/state. | 1 |  |
| `PermanentUpgradeRandomActiveOrPassive` | Integer | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. | 1 |  |
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum | Examples: `Holy` | 1 |  |
| [`PoolMetronome`](#poolmetronome) | Object | Executes a random ability drawn from a specific pool. | 1 |  |
| `Pounce` | Object |  | 2 |  |
| `Prance` | Object |  | 2 |  |
| `Prance2` | Object |  | 1 |  |
| `ProbeCharmed` | Integer | Applies or references the 'ProbeCharmed' effect/state. | 1 |  |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Applies or references the 'QueueUseAbility' effect/state. | 1 |  |
| `RandomBonusDamage` | Integer | Applies or references the 'RandomBonusDamage' effect/state. | 1 |  |
| `RandomKnockbackDirection` | Integer | Applies or references the 'RandomKnockbackDirection' effect/state. | 1 |  |
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array | Examples: `[ Fog Rain Windy Sandstorm HeatWave Snow Thunderstorm Bli...` | 1 |  |
| `ReduceManaCostExcludeBrainstorm` | Integer | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. | 1 |  |
| `ReformMoonHead` | Integer | Applies or references the 'ReformMoonHead' effect/state. | 1 |  |
| `RefreshItemAbilities` | Integer | Applies or references the 'RefreshItemAbilities' effect/state. | 1 |  |
| `RefreshNonManaItemAbilities` | Integer | Applies or references the 'RefreshNonManaItemAbilities' effect/state. | 1 |  |
| `RefreshOncePerFightAbilities` | Integer | Applies or references the 'RefreshOncePerFightAbilities' effect/state. | 1 |  |
| `Regurge` | Integer / Object | Applies or references the 'Regurge' effect/state. | 2 |  |
| `RemoveTurnsThisRound` | Integer | Applies or references the 'RemoveTurnsThisRound' effect/state. | 1 |  |
| `RepairAllCondition` | Integer | Applies or references the 'RepairAllCondition' effect/state. | 1 |  |
| `RerollEnemy` | Integer | Applies or references the 'RerollEnemy' effect/state. | 1 |  |
| `ReturnDinoLegs` | Integer | Applies or references the 'ReturnDinoLegs' effect/state. | 1 |  |
| `RNGCannonRandomDamage` | Integer | Applies or references the 'RNGCannonRandomDamage' effect/state. | 1 |  |
| `rotate_right` | Variable |  | 1 |  |
| `Sandstorm` | Object | Examples: `1` | 2 |  |
| `Scavenge` | Object |  | 2 |  |
| `Scavenge2` | Object |  | 1 |  |
| `Scrambled` | Integer | Applies or references the 'Scrambled' effect/state. | 1 |  |
| [`ScrambleLastUsedSpell`](#scramblelastusedspell) | Object | Randomizes or scrambles the properties of the last spell cast. | 1 |  |
| [`SetAnimationAlts`](#setanimationalts) | Object | Overrides specific animation states with alternative animations. | 1 |  |
| `ShadowCrit` | Integer | Applies or references the 'ShadowCrit' effect/state. | 1 |  |
| `ShootHereCommand` | Integer | Applies or references the 'ShootHereCommand' effect/state. | 1 |  |
| `ShootHereReceiver` | Integer | Applies or references the 'ShootHereReceiver' effect/state. | 1 |  |
| `ShortCircuit` | Integer / Object | Applies or references the 'ShortCircuit' effect/state. | 2 |  |
| [`ShowFakeDamage`](#showfakedamage) | Object | Displays a visual damage number without actually modifying health. | 1 |  |
| `SleepParalysis` | Variable |  | 1 |  |
| `Small` | Object | Character Form: Behavior and stats for the \'Small\' state. | 1 |  |
| `SmallHitExplosion` | Integer | Applies or references the 'SmallHitExplosion' effect/state. | 1 |  |
| `SmallHolding` | Object | Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 |  |
| `SmallHoldingCat` | Object | Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 |  |
| `SmellBlood` | Integer / Object | Applies or references the 'SmellBlood' effect/state. | 2 |  |
| [`SolarFlare`](#solarflare) | Object | Examples: `{ ... }` | 1 |  |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Applies or references the 'SoundEventOnHit' effect/state. | 1 |  |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. | 1 |  |
| [`SpawnTilePuddleOnBattleStart`](#spawntilepuddleonbattlestart) | Object | Examples: `{ ... }` | 1 |  |
| `SpawnWebTrap` | Integer | Applies or references the 'SpawnWebTrap' effect/state. | 1 |  |
| `spear` | Variable |  | 1 |  |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Applies or references the 'SpecialBossMultipartInstakill' effect/state. | 1 |  |
| `SpellShield` | Integer | Applies or references the 'SpellShield' effect/state. | 1 |  |
| `SpitConsumed` | Integer | Applies or references the 'SpitConsumed' effect/state. | 1 |  |
| `SplashDamage` | Integer | Applies or references the 'SplashDamage' effect/state. | 1 |  |
| `SquirrelForm` | Object | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 |  |
| `StackingSandstorm` | Integer | Applies or references the 'StackingSandstorm' effect/state. | 1 |  |
| `StanceSwitchToRanged` | Integer | Applies or references the 'StanceSwitchToRanged' effect/state. | 1 |  |
| `Standing` | Object | Character Form: Behavior and stats for the 'Standing' state. | 1 |  |
| `StatBounty` | Integer | Applies or references the 'StatBounty' effect/state. | 1 |  |
| `StealDemonicGlyph` | Integer | Applies or references the 'StealDemonicGlyph' effect/state. | 1 |  |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Applies or references the 'StealEquipment' effect/state. | 1 |  |
| `StealthCritChance` | Integer | Applies or references the 'StealthCritChance' effect/state. | 1 |  |
| `StealTurn` | Integer | Applies or references the 'StealTurn' effect/state. | 1 |  |
| `SwapHighestAndLowestStat` | Integer | Applies or references the 'SwapHighestAndLowestStat' effect/state. | 2 |  |
| [`SwapWeapon`](#swapweapon) | Object | Replaces the character's currently equipped weapon with one from a specified pool. | 1 |  |
| `Switcheroo` | Integer / Object | Applies or references the 'Switcheroo' effect/state. | 2 |  |
| `Synthesize` | Object |  | 2 |  |
| `Synthesize2` | Object |  | 1 |  |
| `T2CopyCat` | Integer | Applies or references the 'T2CopyCat' effect/state. | 1 |  |
| `T2CopyCatInternal` | Variable |  | 1 |  |
| `T3HitlerTriggerInitialSpawns` | Integer | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. | 1 |  |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Applies or references the 'TagMetronome' effect/state. | 1 |  |
| `TaintedOffering` | Object |  | 2 |  |
| `TaintedOffering2` | Object |  | 1 |  |
| `TakeExtraTurnEndOfRound` | Integer | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. | 1 |  |
| `TallFlowerTile` | Variable |  | 1 |  |
| `TargetedMetronome` | Integer | Applies or references the 'TargetedMetronome' effect/state. | 1 |  |
| `Taunting` | Integer | Applies or references the 'Taunting' effect/state. | 1 |  |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Applies or references the 'TeamBonusAbility' effect/state. | 1 |  |
| `Tease` | Object |  | 2 |  |
| `Tease2` | Object |  | 1 |  |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Applies or references the 'TeleportBackAtTurnEnd' effect/state. | 1 |  |
| `TempBackstab` | Integer | Applies or references the 'TempBackstab' effect/state. | 1 |  |
| `TempBackstabBleed` | Integer | Applies or references the 'TempBackstabBleed' effect/state. | 1 |  |
| `TempBackstabPiercing` | Integer | Applies or references the 'TempBackstabPiercing' effect/state. | 1 |  |
| `TempBackstabPoison` | Integer | Applies or references the 'TempBackstabPoison' effect/state. | 1 |  |
| `TempBasicAttackBonusAOE` | Integer | Applies or references the 'TempBasicAttackBonusAOE' effect/state. | 1 |  |
| `TempBonusKnockback` | Integer | Applies or references the 'TempBonusKnockback' effect/state. | 1 |  |
| `TempBonusKnockbackDamage` | Integer | Applies or references the 'TempBonusKnockbackDamage' effect/state. | 1 |  |
| `TempInjuryImmunity` | Integer | Applies or references the 'TempInjuryImmunity' effect/state. | 1 |  |
| `TempLuckUp` | Integer | Applies or references the 'TempLuckUp' effect/state. | 1 |  |
| `TempManaCostReduction` | Integer | Applies or references the 'TempManaCostReduction' effect/state. | 1 |  |
| `TempPenetrate` | Integer | Applies or references the 'TempPenetrate' effect/state. | 1 |  |
| `TempPreEmptiveCounterAttack` | Integer | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. | 1 |  |
| `the_nuke_bearer` | Variable |  | 1 |  |
| `TheDestroyer` | Object |  | 2 |  |
| `themotherspike` | Variable |  | 1 |  |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | `item_aux` | 1 |  |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Applies or references the 'TickDownStatus' effect/state. | 1 |  |
| `TigerSwipes` | Object |  | 2 |  |
| `TigerSwipes2` | Object |  | 1 |  |
| `TilesMovedToCritChance` | Integer | Applies or references the 'TilesMovedToCritChance' effect/state. | 1 |  |
| `TilesMovedToMana` | Integer | Applies or references the 'TilesMovedToMana' effect/state. | 1 |  |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Applies or references the 'TilesMovedToNeighborHeal' effect/state. | 1 |  |
| `TilesMovedToStrength` | Integer | Applies or references the 'TilesMovedToStrength' effect/state. | 1 |  |
| `Timber` | Object |  | 1 |  |
| `TinaFlail` | Object |  | 1 |  |
| `TinaFlailRage` | Object |  | 1 |  |
| `TowerDefenseStatus` | Integer | Applies or references the 'TowerDefenseStatus' effect/state. | 1 |  |
| `TowerDefenseStatus2` | Integer | Applies or references the 'TowerDefenseStatus2' effect/state. | 1 |  |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Applies or references the 'TransformBasicMove' effect/state. | 1 |  |
| [`TransformEquipment`](#transformequipment) | Object | Upgrades or transforms a specific equipped item into another. | 1 |  |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Applies or references the 'TransformNow' effect/state. | 1 |  |
| `TransformWeapon` | Object | Transforms the equipped weapon into another specific weapon state. | 1 |  |
| `Trapper_Status` | Integer | Applies or references the 'Trapper_Status' effect/state. | 1 |  |
| `TriggerMotherConsume` | Integer | Applies or references the 'TriggerMotherConsume' effect/state. | 1 |  |
| `TriggerMotherGrow` | Integer | Applies or references the 'TriggerMotherGrow' effect/state. | 1 |  |
| `TurnAround` | Integer | Applies or references the 'TurnAround' effect/state. | 1 |  |
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Float | Applies or references the 'TurnControlDelay' effect/state. | 1 |  |
| `TurnRight` | Integer | Applies or references the 'TurnRight' effect/state. | 1 |  |
| `UndoDamage` | Integer | Applies or references the 'UndoDamage' effect/state. | 1 |  |
| [`UseMoveAbilityWithAI`](#usemoveabilitywithai) | Object | Forces the character to execute a movement ability using specific AI weights. | 1 |  |
| `UseRandomSpell_Madness` | Integer | Applies the 'UseRandomSpell_Madness' effect. | 1 |  |
| [`VaporizeCorpseFlipAdvantage`](./Arrays.md#array-vaporizecorpseflipadvantage) | Array | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. | 1 |  |
| `VaporizeDice` | Integer | Applies or references the 'VaporizeDice' effect/state. | 1 |  |
| [`VisualCountDownThenApplyStatus`](#visualcountdownthenapplystatus) | Object | Displays a visual countdown above the target before applying the nested effects. | 1 |  |
| [`WaggleClone`](#waggleclone) | Object | Spawns visual clones or alternative hitbox variants of the projectile. | 1 |  |
| `WaterTile_Current` | Variable |  | 4 |  |
| `weapon_throw` | Variable |  | 1 |  |
| [`WeaponAuxMultiplier`](./Enums.md#enum-weaponauxmultiplier) | Float | Applies or references the 'WeaponAuxMultiplier' effect/state. | 1 |  |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 |  |
| `AutocastEachRound` | Enum / Object | Forces the character to automatically cast a specific ability at the start of each combat round. | 4 |  |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 0 |  |
| `MovementReaction` | Object | Reaction: Triggers an effect or ability when forced to move. | 2 |  |
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

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AlphaCat` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `EvolveAbilityFromPool` | Enum / Object |  |  | `Hunter` (Enum), `Fighter` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer |  |  | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `ManaGain` | Enum / Integer |  |  | `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `Revive` | Integer / Object |  | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `WeaponAuxMultiplier` | Number |  |  | `.5` (String) |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 0 |  |

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| `Fear` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| `Immobile` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](#conditional_inform) | Object | Nested conditional. | 1 |  |

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of applying the debuff. | 1 |  |

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LaunchOffScreen` | String |  |  | `10+bonus_melee_ability_damage` (Enum) |
| `TempInitiativeChange` | Integer |  |  | `[1 .5]` (Array), `9999` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| [`formula`](./Enums.md#enum-formula) | Enum | The math expression to evaluate. | 8 |  |
| `Burn` | Array / Enum / Integer |  | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `OverrideKnockbackDamage` | Enum / Integer |  |  | `str` (Enum), `X*10` (Enum), `5` (Number), `2` (Number), `"max(5+bonus_melee_ability_damage, 1)"` (String) |
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

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Bruise` | Array / Integer / Object |  | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DelayCastAbility` | Enum / Object |  |  | `HitlerNuke` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| `Confusion` | Array / Integer / Object |  | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| `Immobile` | Array / Integer |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Knockback` | Integer |  |  | `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| `Adrenaline` | Integer |  |  | `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
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
| [`odds`](./Enums.md#enum-odds) | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 4 |  |

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Object | Nested conditional. | 2 |  |
| `BonusDamage` | Enum / Integer |  |  | `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Knockback` | Integer |  |  | `3` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 17 |  |
| `force_contact` | Boolean | If true, enforces physical overlap. | 15 |  |
| `instant` | Boolean | Examples: `true` | 12 |  |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | If true, treats the consumption as riding/mounting instead of eating. | 12 |  |
| `do_not_pop_corpse` | Boolean | Examples: `true` | 11 |  |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Examples: `false, true, deferred` | 11 |  |
| `wet` | Boolean | Examples: `false, true` | 8 |  |
| `drop_on_self_death` | Boolean | Examples: `true` | 3 |  |
| [`extra_statuses`](#extra_statuses) | Object | Additional generic status applications. | 3 |  |
| `use_placeholder` | Boolean | Examples: `true` | 3 |  |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Examples: `MoonHandDrop` | 1 |  |
| `kill_on_consume` | Boolean | Examples: `true` | 1 |  |

</details>

---

#### `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 85

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
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
| `AcidRain` | Number / Object |  |  | `2` (Number), `{ ... }` (Object) |
| `AlphaCat` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Ammo` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `6` (Number), `{ ... }` (Object) |
| `Attraction` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BackflipWhenTargeted` | Enum / Integer / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer |  | 9 | `[1 .1]` (Array), `[3 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer |  | 6 | `[1 .25]` (Array), `[1 .10]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Bloodzerked` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BodyGuard` | Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BombRatTurtle` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `BounceObject` | Enum / Object |  |  | `CharmedFlea_Champion` (Enum), `CharmedDip` (Enum), `{ ... }` (Object) |
| `BounceRock` | Array / Enum |  |  | `[1 .2]` (Array), `LavaBoulder` (Enum), `SmallRock` (Enum) |
| `Brace` | Enum / Integer / Object |  | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bruise` | Array / Integer / Object |  | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `BurgleCoin` | Array / Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number) |
| `ButterflySwarm` | Number / Object |  |  | `2` (Number), `{ ... }` (Object) |
| `ChampionUpgradeNextMinion` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ChangeTile` | Enum / Object |  |  | `FireTile` (Enum), `GrassTile` (Enum), `{ ... }` (Object) |
| `ChangeTilesUnder` | Enum |  |  | `LavaTile` (Enum), `DirtTile` (Enum) |
| `Charge` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `ChargeFists` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer |  |  | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer |  |  | `[1 .25]` (Array), `[1 .15]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Cleave` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `CockroachSwarm` | Number / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `CollideWithConsumed` | String |  |  | `5+bonus_melee_damage` (Enum), `4+bonus_melee_damage` (Enum) |
| `Confusion` | Array / Integer / Object |  | 6 | `[1 .2]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ConjureBonusAbility` | Enum / Object |  | 2 | `random` (Enum), `Mage` (Enum), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `CopySpells` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `Counterspell` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `CreateGlobalModifiers` | Object |  |  | `{ ... }` (Object) |
| `CritChanceUp` | Integer |  | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `DamageOrHealConditionally` | Integer |  |  | `1` (Number) |
| `DamageUp` | Integer / String |  | 6 | `[1 .5]` (Array), `3` (Number), `2` (Number), `{ ... }` (Object) |
| `DelayCastAbility` | Enum / Object |  |  | `HitlerNuke` (Enum), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer |  | 2 | `[1 .5]` (Array), `15` (Number), `50` (Number), `{ ... }` (Object) |
| `Doomed` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DoubleCast` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DoubleCastSpell` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DoubleLoot` | Integer / Object |  | 2 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DrinkWater` | Integer |  | 2 | `1` (Number) |
| `Drowsy` | Integer |  |  | `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `EliteUpgradeNextMinion` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `EmptyMind` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Enlarge` | Integer / Object |  | 2 | `3` (Number), `{ ... }` (Object) |
| `EvolveAbilityFromPool` | Enum / Object |  |  | `Tinkerer` (Enum), `Fighter` (Enum), `{ ... }` (Object) |
| `ExtraBasicAttacks_Status` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ExtraBasicMoves_Status` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FactionUprising` | Enum / Object |  |  | `robot` (Enum), `ghost` (Enum), `{ ... }` (Object) |
| `Fear` | Array / Integer |  |  | `[1 .25]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `FillMana` | Integer |  |  | `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `FindExtraItemFromPoolOnBattleEnd` | Enum |  |  | `combat_reward_easy` (Enum), `pills` (Enum) |
| `FireArmor` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FireArmor2` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FireflySwarm` | Number / Object |  |  | `2` (Number), `{ ... }` (Object) |
| `FireStorm` | Number / Object |  |  | `33` (Number), `0` (Number), `{ ... }` (Object) |
| `FlySwarm` | Object |  | 5 | `50` (Number), `{ ... }` (Object) |
| `Fog` | Number / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `ForceAttack` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `ForceMoveAway` | Integer |  |  | `1` (Number), `{ ... }` (Object) |
| `ForceMoveTowardsEnemies` | Enum / Integer |  |  | `MoveOne` (Enum), `DumbMove_Impl` (Enum), `1` (Number) |
| `ForceUseAbility` | Enum / Object |  |  | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer |  |  | `[1 .25]` (Array), `[1 .15]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `GainCoinsRange` | Object |  |  | `{ ... }` (Object) |
| `Grappled` | Array / Integer |  |  | `[1 .5]` (Array), `[1 .75]` (Array), `1` (Number), `{ ... }` (Object) |
| `HealRandomInjury` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer |  |  | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `HealthRegenUp` | Integer |  | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HeatWave` | Array / Number / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HeavyHits` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Hex` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `IceArmor` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `IgnoreSelf` | Boolean / Integer |  |  | `true` (Boolean), `1` (Number) |
| `ImmediateUseAbility` | Enum / Object |  |  | `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Infested` | Integer / Object |  | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Instakill` | Integer |  |  | `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `IntelligenceUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Invulnerable` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `JudgementDay` | Number / Object |  |  | `25` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer |  | 6 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Knockback` | Integer |  |  | `3` (Number), `4` (Number), `{ ... }` (Object) |
| `KnockbackDirectionIsFacingDirection` | Enum / Integer |  |  | `flip` (Enum), `rotate_right` (Enum), `1` (Number) |
| `KnockOutCoin` | Integer / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Leech` | Integer |  | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Leeches` | Integer / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Lifesteal` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `LowerAmbientLight` | Object | A visual effect that dims the map's lighting. | 4 |  |
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
| `Meaty` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Meteornado` | Number / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `MeteorShower` | Number / Object |  |  | `25` (Number), `{ ... }` (Object) |
| `Metronome` | Boolean (Flag) / Number / Object |  | 4 | `(Flag)` (Boolean (Flag)), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `MovementUp` | Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer |  | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Muted` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextAbilityHeals` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextActionLuckUp` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `99` (Number), `{ ... }` (Object) |
| `NextAttackBonusRange` | Integer |  |  | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `NextAttackSpecialCrit` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `NextBasicAttackCritsThisTurn` | Object |  |  | `1` (Number), `{ ... }` (Object) |
| `NextDamageReduceAndHealAllies` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextTurnDoubleRangedDamage` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NonStackingDivineShield` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ObjectOnHitCharacter` | Enum / Object |  |  | `SkeletonCatFamiliar` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `Ostracized` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `OverrideChainKnockbackDamage` | String |  |  | `3+bonus_melee_ability_damage` (Enum), `0` (Number) |
| `OverrideKnockbackDamage` | Enum / Integer |  |  | `str` (Enum), `3+bonus_melee_ability_damage` (Enum), `2` (Number), `3` (Number), `"max(5+bonus_melee_ability_damage, 1)"` (String) |
| `PartialCleanse` | Integer |  |  | `1` (Number), `9999` (Number) |
| `PermanentConstitution` | Integer |  |  | `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer |  |  | `1` (Number), `2` (Number) |
| `PermanentImmobile` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
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
| `RandomDistanceDisplace` | Integer / Object |  |  | `20` (Number), `{ ... }` (Object) |
| `RandomInjury` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomMagicMissile` | Integer / Object |  |  | `[1 .5]` (Array), `5` (Number), `6` (Number), `{ ... }` (Object) |
| `RandomPermanentStat` | Integer |  |  | `-1` (Number), `-2` (Number) |
| `RandomStatDown` | Array / Integer / String |  |  | `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `RandomStatUp` | Integer / String |  | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `3` (Number), `-3` (Number) |
| `RangeUp` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Reanimate` | Integer / Object |  | 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `ReduceManaCost` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ReduceManaCostExcludeBrainstorm` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Reflect` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `Regurge` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `RepairWeapon` | Array / Integer |  |  | `[1 .25]` (Array), `6` (Number), `1` (Number) |
| `Revive` | Integer / Object |  | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| `ReviveNextRound` | Integer / Object |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Rot` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Sandstorm` | Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `ScatterHeldCoin` | Array / Integer |  |  | `[1 .3]` (Array), `[1 .5]` (Array), `1` (Number) |
| `SelfStun` | Array / Integer |  |  | `[1 .5]` (Array), `1` (Number) |
| `SetDefaultFace` | Enum |  |  | `insane` (Enum), `happy` (Enum) |
| `Shatter` | Integer / Object |  |  | `15` (Number), `{ ... }` (Object) |
| `ShortCircuit` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SizeScale` | Number |  | 4 | `1.1` (Number), `1.3` (Number), `.6` (String), `.8` (String) |
| `Sleep` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SmartMetronome` | Integer / Object |  | 4 | `20` (Number), `{ ... }` (Object) |
| `SmellBlood` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Snow` | Number / Object |  | 1 | `1` (Number), `{ ... }` (Object) |
| `SoulLink` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer |  |  | `[1 .5]` (Array), `1` (Number) |
| `SpawnRock` | Array / Integer |  |  | `[1 .20]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `SpellShield` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `StatBounty` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `StatusAllCharactersOnSpawn` | Object |  |  | `{ ... }` (Object) |
| `StatusGroup` | Object |  |  | `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Switcheroo` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Tangled` | Array / Integer / Object |  |  | `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Taunting` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TeamCastAbility` | Enum / Object |  |  | `TeamFlex_Impl2` (Enum), `TeamFlex_Impl` (Enum), `{ ... }` (Object) |
| `TempBackstab` | Integer |  |  | `[1 .5]` (Array), `75` (Number), `1` (Number), `{ ... }` (Object) |
| `TempBonusKnockback` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempBonusKnockbackDamage` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempCounterAttack` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempCritChanceUp` | Integer |  |  | `[1 .5]` (Array), `30` (Number), `1` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempDexterityUp` | Enum |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInitiativeChange` | Integer |  |  | `[1 .5]` (Array), `9999` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInjuryImmunity` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempManaCostReduction` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempMovement` | Enum / Integer |  |  | `[1 .5]` (Array), `20` (Number), `1` (Number), `{ ... }` (Object) |
| `TempPreEmptiveCounterAttack` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempRangeUp` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpellDamageUp` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempStrengthUp` | Enum |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Thorns` | Integer |  | 36 | `[1 .5]` (Array), `3` (Number), `5` (Number), `{ ... }` (Object) |
| `TilesMovedToCritChance` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToMana` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToNeighborHeal` | Enum |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToStrength` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TowerDefenseStatus` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TowerDefenseStatus2` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TradeLife` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `TrailBlazer` | Enum / Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Trample` | Integer |  | 14 | `[3 X-8]` (Array), `[1 .5]` (Array), `9` (Number), `6` (Number), `{ ... }` (Object) |
| `TriggerWerewolfTransform` | Array / Number |  |  | `[1 .5]` (Array), `[1 .20]` (Array), `.5` (String) |
| `TurnControlDelay` | Number |  |  | `.25` (String) |
| `UseAbility` | Enum / Object |  |  | `MegaGuppy_SummonTheChild` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `VisualFlySwarm` | Number / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `Webbed` | Integer |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Windy` | Number / Object |  | 1 | `10` (Number), `1` (Number), `{ ... }` (Object) |

</details>



## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.

### Object: `AcidRain`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | String |  |  | `.5` (String) |
| `ambient_sound` | String |  |  | `amb_acidrain.ogg` (String) |
| `chain` | Boolean |  |  | `AcidSplash` (Enum) |
| `desc` | Enum |  |  | `"WEATHER_ACIDRAIN_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `emit_amount` | Number |  |  | `1` (Number) |
| `emit_box` | Array |  |  | `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array |  |  | `[0 -1 0]` (Array) |
| `emit_rate` | Number |  |  | `100` (Number) |
| `emit_spread` | Number |  |  | `0` (Number) |
| `face_moving_direction` | Boolean |  |  | `true` (Boolean) |
| `force` | Array |  |  | `[0 -10 0]` (Array) |
| `live_bounds` | Array |  |  | `[-999 999 0 999 -999 999]` (Array) |
| `movieclip` | Array / Enum |  |  | `AcidRainParticle` (Enum) |
| `name` | Enum |  |  | `"WEATHER_ACIDRAIN_NAME"` (String) |
| `particle_lifetime` | Number |  |  | `5` (Number) |
| `projection_matrix` | Enum |  |  | `default` (Enum) |
| `render_mode` | Enum |  |  | `separate` (Enum) |
| `scripts` | Object |  |  | `{ ... }` (Object) |
| `simulation_space` | Enum |  |  | `global` (Enum) |
| `size_start` | String |  |  | `.5` (String) |
| `speed_scale` | String |  |  | `.1` (String) |
| `speed_start` | Number |  |  | `10` (Number) |


### Object: `AddPostProcessEffect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean |  | 1 | `false` (Boolean) |
| `shader` | Enum |  | 1 | `shimmervignette` (Enum) |


### Object: `AddTilesetObjects`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FloatingDebris` | Object |  | 1 | `{ ... }` (Object) |


### Object: `Adrenaline`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_ADRENALINE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_ADRENALINE_DESC"` (String) |


### Object: `Alert`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Alert` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `AllAlive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 6 | `{ ... }` (Object) |


### Object: `AllyInfested`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Infested` (Enum) |
| `faction` | Enum |  | 1 | `allies` (Enum) |
| `object` | Array / Enum |  | 1 | `CharmedMaggot` (Enum) |


### Object: `Angry`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Angry"` (Enum) |


### Object: `Antidote`

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


### Object: `Appeal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_APPEAL_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_APPEAL_DESC"` (String) |


### Object: `ApplyMultipleTimes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatusFromPool` | Object |  | 6 | `{ ... }` (Object) |
| `stacks` | Enum / Integer |  | 6 | `X` (Enum), `4` (Number), `8` (Number) |


### Object: `ApplyPassives`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Flying` | Integer |  | 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `YOffset` | Number |  | 4 | `-.18` (String), `.35` (String) |


### Object: `ApplyStatusesNextTurnBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Quivered` | Array / Integer |  | 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |


### Object: `ApplyToConsumed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | Integer |  | 6 | `1` (Number) |
| `Die` | Integer / Object |  | 2 | `6` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `ApplyToOthersWithSharedTagAndFaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Marked` | Array / Integer / Object |  | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `ApplyToRandomClosestAlly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Integer |  | 2 | `1` (Number) |


### Object: `ApplyToTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ObjectOnHit` | Enum / Object |  | 4 | `BiggestFood` (Enum), `Bait` (Enum), `{ ... }` (Object) |
| `SpawnBearTrap` | Integer |  | 4 | `1` (Number) |


### Object: `ArcLightning`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number |  | 2 | `.5` (String) |
| `enemies_only` | Boolean |  | 8 | `false` (Boolean), `true` (Boolean) |
| `ignore_self` | Boolean |  | 2 | `true` (Boolean) |
| `max_distance` | Integer |  | 8 | `3` (Number), `1` (Number) |
| `stacks` | Enum / Integer |  | 8 | `100` (Number) |


### Object: `Attacker`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Attraction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_ATTRACTION_NAME"` (String) |
| `name_reference_applier` | String |  |  | `"KEYWORD_ATTRACTION_REF"` (String) |
| `tooltip_reference_applier` | String |  |  | `"KEYWORD_ATTRACTION_DESC_REF"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_ATTRACTION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_ATTRACTION_DESC"` (String) |


### Object: `BagOfSeeds`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `tk_BagOfSeeds` (Enum) |
| `desc` | Enum |  |  | `"ITEM_BAGOFSEEDS_DESC"` (String) |
| `frame` | Integer |  |  | `182` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_BAGOFSEEDS_NAME"` (String) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Druid` (Enum) |


### Object: `Basement0`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement0` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |


### Object: `Basement1`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement1` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |


### Object: `Basement2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement2` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |


### Object: `Basement3`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement3` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |


### Object: `Basement4`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `5` (Number) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundBasement4` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `33` (Number) |


### Object: `BasementUpgrade`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement0` (Enum) |


### Object: `BasementUpgrade2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement1` (Enum) |


### Object: `BasementUpgrade3`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade2` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement2` (Enum) |


### Object: `BasementUpgrade4`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade3` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement3` (Enum) |


### Object: `BasementUpgrade5`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `BasementUpgrade4` (Enum) |
| `unlock_room` | Enum |  | 2 | `Basement4` (Enum) |


### Object: `Bear`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `BellyFull`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Belly"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Big`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `Big` (Enum), `"Big"` (Enum) |
| `attack` | Enum |  | 2 | `GameteSpawn` (Enum) |
| `follow_character_tag` | Enum |  | 2 | `zaratana` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `position` | Array |  |  | `[4.5 4.5]` (Array) |


### Object: `BigCatnip`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |


### Object: `BigFood`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `FoodBase` (Enum) |


### Object: `BigHolding`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"BigHolding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `BigHoldingCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"BigHoldingCat"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `BigScrap`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |


### Object: `BiggestFood`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `FoodBase` (Enum) |


### Object: `BirdFeed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_BIRDFEED_DESC"` (String) |
| `frame` | Integer |  |  | `191` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_BIRDFEED_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |


### Object: `BirdPoopHat`

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


### Object: `Bishop`

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


### Object: `BlackBird`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |


### Object: `BlackHole`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"BlackHole"` (Enum) |
| `name` | Enum |  | 2 | `"OBJECT_BLACKHOLE_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"OBJECT_BLACKHOLE_DESC"` (String) |
| `variant_of` | Enum |  |  | `NeutronStar` (Enum) |


### Object: `Blessing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `intro` | Object |  |  | `{ ... }` (Object) |
| `main` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |


### Object: `Bloodzerked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BLOODZERK_NAME"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BLOODZERK_DESC"` (String) |


### Object: `BodyGuard`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `BodyGuardSwap2` (Enum), `BodyGuardSwap` (Enum) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_BODYGUARD_NAME"` (String) |
| `stacks` | Enum / Integer |  | 4 | `1` (Number) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  |  | `"KEYWORD_BODYGUARD_DESC"` (String) |


### Object: `Bomb`

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


### Object: `BombRatTurtle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `self_buff` (Enum) |


### Object: `BoneyardUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Boris`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `"2"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `BothObelisksUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |


### Object: `Bully`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `BunkerUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Butcher`

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


### Object: `ButterflySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String |  |  | `amb_butterflyswarm.ogg` (String) |
| `desc` | Enum |  |  | `"WEATHER_BUTTERFLY_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_BUTTERFLY_NAME"` (String) |


### Object: `CanApplyToInanimate`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ApplyToSource` | Object |  | 6 | `{ ... }` (Object) |
| `BreakIntoRocks` | Enum |  | 8 | `Coin` (Enum), `SmallRock` (Enum) |
| `GetAggroTarget` | Integer |  | 4 | `1` (Number) |
| `ObjectOnHitCharacter` | Enum / Object |  | 20 | `AllyRotFly` (Enum), `CharmedLeech` (Enum), `{ ... }` (Object) |
| `PreventDeathTransforms` | Integer |  | 2 | `1` (Number) |
| `Temporary` | Object |  | 2 | `{ ... }` (Object) |
| `Vaporize` | Integer |  | 6 | `1` (Number), `20` (Number) |


### Object: `CastAgainWithStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | Integer |  | 2 | `25` (Number), `10` (Number) |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |


### Object: `Cat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum |  | 2 | `spawnHoldingCat` (Enum) |
| `formchange` | Enum |  | 6 | `SmallHoldingCat` (Enum), `BigHoldingCat` (Enum) |
| `statuses` | Object |  | 4 | `{ ... }` (Object) |


### Object: `CatPartsSizeScaleStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `arm1` | Number |  | 2 | `1.1` (Number) |
| `arm2` | Number |  | 2 | `1.1` (Number) |
| `body` | Number |  | 2 | `1.1` (Number) |
| `mouth` | Number |  | 2 | `1.1` (Number) |


### Object: `Catepillar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `Catnip`

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


### Object: `CatnipBig`

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


### Object: `CaveBaby`

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


### Object: `CaveMan`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"CaveMan"` (Enum) |
| `attack` | Enum |  | 4 | `CaveMan3HitCombo` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CAVEMANMAN_NAME"` (String) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CAVEMANMAN_DESC"` (String) |
| `variant_of` | Enum |  |  | `CavePerson` (Enum) |


### Object: `CaveManSpear`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"SpearCaveMan"` (Enum) |
| `attack` | Enum |  | 4 | `CaveManThrowSpear` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_SPEARCAVEMAN_NAME"` (String) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_SPEARCAVEMAN_DESC"` (String) |


### Object: `CaveWoman`

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


### Object: `CaveWomanHasCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"CatCaveWoman"` (Enum) |
| `attack` | Enum |  | 2 | `CaveWomanCatSlap` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CAVEMANWOMAN2_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CAVEMANWOMAN2_DESC"` (String) |


### Object: `CavesUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `CerberubsJumpBlind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum |  | 2 | `nubs_fakeblind` (Enum) |


### Object: `CerberubsJumpNormal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum |  | 2 | `default` (Enum) |


### Object: `ChampionUpgradeNextMinion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_PROMOTE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_PROMOTE_DESC"` (String) |


### Object: `ChanceToBreakFree`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 22 | `CHuskDrop` (Enum), `LennyDrop` (Enum) |
| `fail_ability` | Enum |  | 6 | `CHuskDropFail` (Enum), `XXX` (Enum) |
| `stacks` | Enum / Integer |  | 6 | `25` (Number) |


### Object: `ChaosAntennaAttached`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `CharacterTypeGainsStatusAtBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer |  | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Else` | Object |  | 1 | `{ ... }` (Object) |
| `Fear` | Array / Integer |  | 3 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Stealth` | Array / Integer |  | 1 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer |  | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `ChargeFists`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `keyword_tooltips` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_CHARGEFISTS_NAME"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_CHARGEFISTS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_CHARGEFISTS_DESC"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_CHARGEFISTS_DESC_SINGULAR"` (String) |


### Object: `Charging`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `MoonHead_Blow` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Charging"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `CharmedDip`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Dip` (Enum) |


### Object: `CharmedFloater`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Floater` (Enum) |


### Object: `CharmedPile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Pile` (Enum) |


### Object: `Cherub`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |


### Object: `Chicken`

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


### Object: `Close`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `CloseConvert`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `MarshmallowConvert` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |


### Object: `Cockroach`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  |  | `[0 20]` (Array), `[10 20]` (Array) |


### Object: `CockroachSwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"WEATHER_COCKROACHES_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_COCKROACHES_NAME"` (String) |


### Object: `Coin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |


### Object: `Coin10`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |


### Object: `Coin2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |


### Object: `Coin3`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |


### Object: `Coin4`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `Coin` (Enum) |


### Object: `CollectsPickupsWithAltEffects`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponAddPoison` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer |  | 2 | `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer |  | 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String |  | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `Shield` | Enum / Integer |  | 2 | `[1 .5]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Tech` | Integer |  | 4 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `Colorless`

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


### Object: `Comfort`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_COMFORT_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_COMFORT_DESC"` (String) |


### Object: `Conditional_DoesDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer |  |  | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `Conditional_FinishedSpawning`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Imprison` | Enum |  | 2 | `Fly` (Enum), `BeefyCharmedLeech` (Enum) |


### Object: `CopySpells`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |
| `upgraded` | Boolean |  | 2 | `true` (Boolean) |


### Object: `CoreObeliskUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `CoreUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Counterspell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `self_buff` (Enum) |


### Object: `CraterUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit1` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Cultist`

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


### Object: `CurrentWeaponAddPoison`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_WPOISONLACE_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_WPOISONLACE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_WPOISONLACE_DESC"` (String) |


### Object: `Damaged`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |


### Object: `DashRandomly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `ShamblerDash` (Enum) |
| `decision_weights` | Enum |  | 4 | `blind` (Enum) |


### Object: `DeadHummingbird`

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


### Object: `Default`

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


### Object: `Default_Ceiling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Default_Ground`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `DelayCastAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `FetusAirstrike` (Enum) |
| `lingering` | Boolean |  | 2 | `true` (Boolean) |
| `relative` | Boolean |  | 2 | `false` (Boolean) |


### Object: `DelayedWind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer |  | 2 | `2` (Number) |


### Object: `DelayedWindCone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation |  | 2 | `5` (Equation) |
| `distance` | Integer |  | 4 | `10` (Number) |


### Object: `DemonicGlyph_Bite`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_BITE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_BITE_DESC"` (String) |


### Object: `DemonicGlyph_Bounce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_BOUNCE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_BOUNCE_DESC"` (String) |


### Object: `DemonicGlyph_Fire`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_FIRE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_FIRE_DESC"` (String) |


### Object: `DemonicGlyph_Movement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_MOVE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_MOVE_DESC"` (String) |


### Object: `DemonicGlyph_Summon`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TOR_SUMMON_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TOR_SUMMON_DESC"` (String) |


### Object: `DesireMech`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Die`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `DimensionXUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |


### Object: `DoDistortionRing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer |  | 12 | `-2` (Number), `1` (Number) |
| `radius` | Array / Integer |  | 12 | `4` (Number), `5` (Number) |
| `speed` | Array / Number |  | 12 | `30` (Number), `-30` (Number) |


### Object: `DoScreenShake`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer |  | 20 | `10` (Number), `3` (Number) |
| `time` | Number |  | 20 | `1` (Number), `2` (Number), `.75` (String), `.5` (String) |


### Object: `DoubleCast`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_DOUBLECAST_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_DOUBLECAST_DESC"` (String) |


### Object: `DoubleCastSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_DOUBLECASTSPELL_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_DOUBLECASTSPELL_DESC"` (String) |


### Object: `DoubleLoot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `self_buff` (Enum) |


### Object: `Dove`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |


### Object: `Down`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Down"` (Enum) |
| `attack` | Enum |  | 2 | `ButtFart` (Enum) |
| `move` | Enum |  | 2 | `TeleportFlipUp` (Enum) |
| `passives` | Object |  | 6 | `{ ... }` (Object) |


### Object: `Drag`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Psychic` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_DRAG_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_DRAG_NAME"` (String) |


### Object: `Druid`

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


### Object: `Drunker`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Drunk` (Enum) |


### Object: `DualSword`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"2"` (Enum) |
| `attack` | Enum |  | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number |  | 2 | `1.5` (Number) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |


### Object: `DualSword_Primed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Holy2"` (Enum) |
| `attack` | Enum |  | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number |  | 2 | `1.5` (Number) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |


### Object: `Dumb`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `DustOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum |  | 6 | `GasCloud` (Enum) |


### Object: `DybbukPossessed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit_ability` | Enum |  | 2 | `DybbukReturn` (Enum) |
| `name` | Enum |  |  | `"KEYWORD_DYBBUKED_NAME"` (String) |
| `punch_self_ability` | Enum |  | 2 | `Dybbuk_StopHittingYourself` (Enum) |
| `tooltip` | Enum |  |  | `"KEYWORD_DYBBUKED_DESC"` (String) |


### Object: `Eagle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdLarge` (Enum) |


### Object: `Earth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation |  | 4 | `X` (Equation) |


### Object: `Electric`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer |  |  | `[1 .1]` (Array), `[1 .1*X]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `EliteUpgradeNextMinion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_PROMOTE2_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_PROMOTE2_DESC"` (String) |


### Object: `Empty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `""` (String) |


### Object: `EmptyMind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_EMPTYMIND_NAME"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  |  | `"KEYWORD_EMPTYMIND_DESC"` (String) |


### Object: `EndOfTimeUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 4 | `{ ... }` (Object) |


### Object: `Enlarge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |


### Object: `Escape`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `DybbukEscape` (Enum) |
| `move_weights` | Enum |  | 4 | `keep_distance_always_move` (Enum) |


### Object: `EventBounty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_EVENTBOUNTY_NAME"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_EVENTBOUNTY_DESC"` (String) |


### Object: `Evolution`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_EVOLUTION_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_EVOLUTION_DESC"` (String) |


### Object: `EvolveAbilityFromPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum |  | 26 | `Fighter` (Enum), `Thief` (Enum) |
| `upgraded` | Boolean |  | 26 | `true` (Boolean) |


### Object: `Explody`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Expl` (Enum) |
| `attack` | Enum |  | 2 | `ToxExplode` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Explosive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 4 | `"3"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `FactionUprising`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `extra_statuses` | Object |  | 1 | `{ ... }` (Object) |
| `tag` | Array / Enum |  | 1 | `bird` (Enum) |


### Object: `FightPhase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `T3Shoot` (Enum) |
| `move` | Enum |  | 2 | `FloatMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Fighter`

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


### Object: `Fire`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Array / Enum / Integer |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `SpewerLobbed_Lava` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `FireArmor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Mage` (Enum) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `desc` | Enum |  |  | `"PASSIVE_FIREASPECT_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"FireArmor"` (Enum), `"PASSIVE_FIREASPECT_NAME"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `FireArmor2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"FireArmor2"` (Enum) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `FireFull`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Full` (Enum) |
| `attack` | Enum |  | 2 | `SpewerSpit` (Enum) |
| `combo` | Array |  |  | `[FireSmoke FirePlumes FireWaves FireBase FireWhites]` (Array) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `FireStorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combo` | Array |  |  | `[Firestorm_Fire Firestorm_Embers Firestorm_Distortion]` (Array) |


### Object: `Firefly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  |  | `[0 2]` (Array) |


### Object: `FireflySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"WEATHER_FIREFLY_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_FIREFLY_NAME"` (String) |


### Object: `FloatingDebris`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  | 1 | `20` (Number) |


### Object: `Floor1_Large`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum |  | 2 | `room1` (Enum) |
| `movieclip` | Array / Enum |  | 2 | `RoomBackgroundLargeF1` (Enum) |
| `reverb_empty` | Object |  | 2 | `{ ... }` (Object) |
| `reverb_full` | Object |  | 2 | `{ ... }` (Object) |
| `width` | Number |  | 2 | `16` (Number) |


### Object: `Floor1_Small`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum |  | 2 | `room2` (Enum) |
| `movieclip` | Array / Enum |  | 2 | `RoomBackgroundSmallF1` (Enum) |
| `reverb_empty` | Object |  | 2 | `{ ... }` (Object) |
| `reverb_full` | Object |  | 2 | `{ ... }` (Object) |
| `width` | Number |  | 2 | `16` (Number) |


### Object: `Floor2_Large`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `7` (Number) |
| `interstitial_bg_frame` | Enum |  |  | `room3` (Enum) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundLargeF2` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `16` (Number) |


### Object: `Floor2_Small`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer |  |  | `7` (Number) |
| `interstitial_bg_frame` | Enum |  |  | `room4` (Enum) |
| `movieclip` | Array / Enum |  |  | `RoomBackgroundSmallF2` (Enum) |
| `reverb_empty` | Object |  |  | `{ ... }` (Object) |
| `reverb_full` | Object |  |  | `{ ... }` (Object) |
| `width` | Number |  |  | `16` (Number) |


### Object: `Flop`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Down"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Flop2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Down"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Flush`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |


### Object: `FlushBubs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `FlushHost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Host` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `FlushNettle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Fly`

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


### Object: `FlySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `ambient_sound` | String |  |  | `amb_flyswarm.ogg` (String) |
| `desc` | Enum |  |  | `"WEATHER_FLYSWARM_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_FLYSWARM_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `Fog`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number |  |  | `0` (Number) |
| `alpha_start` | Number |  |  | `2` (Number) |
| `desc` | Enum |  |  | `"WEATHER_FOG_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `emit_amount` | Number |  |  | `1` (Number) |
| `emit_box` | Array |  |  | `[-5 10 0 2 -5 10]` (Array) |
| `emit_direction` | Array |  |  | `[0 1 0]` (Array) |
| `emit_rate` | Number |  |  | `100` (Number) |
| `emit_spread` | Number |  |  | `360` (Number) |
| `friction` | Array |  |  | `[0 1 0]` (Array) |
| `live_bounds` | Array |  |  | `[-999 999 -999 999 -999 999]` (Array) |
| `movieclip` | Array / Enum |  |  | `FogParticle` (Enum) |
| `name` | Enum |  |  | `"WEATHER_FOG_NAME"` (String) |
| `particle_lifetime` | Array |  |  | `[3 5]` (Array) |
| `projection_matrix` | Enum |  |  | `default` (Enum) |
| `render_mode` | Enum |  |  | `separate` (Enum) |
| `scripts` | Object |  |  | `{ ... }` (Object) |
| `simulation_space` | Enum |  |  | `global` (Enum) |
| `size_start` | Array |  |  | `[.2 1]` (Array) |
| `speed_start` | String |  |  | `.1` (String) |


### Object: `Food`

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


### Object: `FoodBig`

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


### Object: `FoodMedium`

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


### Object: `FoodMove`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `CaveBabyFoodMove` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close_move_if_possible` (Enum) |


### Object: `ForceImmediateMoveAndAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `G3GrabHead` (Enum) |
| `even_if_cant_reach` | Boolean |  | 2 | `true` (Boolean) |


### Object: `ForceMoveAway`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 2 | `false` (Boolean) |


### Object: `ForceMoveTowardsTaggedObject`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `MoveOneTrample` (Enum), `MoveTwoTrample` (Enum) |
| `tag` | Array / Enum |  | 2 | `food` (Enum) |


### Object: `ForceTrample`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `BirthwortTrample` (Enum) |
| `decision_weights` | Enum |  | 2 | `always_cast_careless` (Enum) |


### Object: `FreeSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_FREESPELL_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_FREESPELL_DESC"` (String) |


### Object: `Full`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Full"` (Enum) |
| `attack` | Enum |  | 4 | `KirbySpit` (Enum) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `statuses_on_enter_form` | Object |  | 4 | `{ ... }` (Object) |


### Object: `FutureUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `GenFlag_Boss_Spewer`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boss` | Object |  | 2 | `{ ... }` (Object) |


### Object: `GenFlag_Boss_Stacy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boss` | Object |  | 2 | `{ ... }` (Object) |
| `miniboss_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `GlobalSpawnOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `number` | Array / Integer |  |  | `[1 2]` (Array) |
| `object` | Array / Enum |  | 2 | `NeutralZombieKitten` (Enum), `NeutralTwister` (Enum) |


### Object: `GlowingSeed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_GLOWINGSEED_DESC"` (String) |
| `frame` | Integer |  |  | `71` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_GLOWINGSEED_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |


### Object: `GoldenEgg`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_GOLDENEGG_DESC"` (String) |
| `frame` | Integer |  |  | `190` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_GOLDENEGG_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |


### Object: `Grappled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_GRAPPLED_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_GRAPPLED_DESC"` (String) |


### Object: `Grappling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit_animations` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Grapple` (Enum) |


### Object: `Grass`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `Gravity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Weakness` | Array / Integer / Object |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `Grown`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Grown` (Enum) |
| `attack` | Enum |  | 2 | `HitlerCloneSwipes` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_HITLERCLONE_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1.5` (Number) |
| `weak_threshold` | Integer |  | 2 | `15` (Number) |


### Object: `GuaranteedJackpot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Guarding`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Guarding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `HalfDead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"2"` (Enum) |
| `attack` | Enum |  | 2 | `RatKingDash` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `HardPathUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hard_initial` | Object |  | 4 | `{ ... }` (Object) |


### Object: `Harpy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdLarge` (Enum) |


### Object: `HarpysClaw`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `wp_HarpyClaw` (Enum) |
| `desc` | Enum |  |  | `"ITEM_HARPYSCLAW_DESC"` (String) |
| `frame` | Integer |  |  | `199` (Number) |
| `kind` | Enum |  |  | `weapon` (Enum) |
| `name` | Enum |  |  | `"ITEM_HARPYSCLAW_NAME"` (String) |
| `rarity` | Enum |  |  | `very_rare` (Enum) |


### Object: `HasCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 10 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 8 | `"Grabbing"` (Enum), `"Cat"` (Enum) |
| `attack` | Enum |  | 10 | `LennyCatSlap` (Enum), `MoonHandSqueeze` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Swallowed"` (Enum) |
| `passives` | Object |  | 8 | `{ ... }` (Object) |


### Object: `HasDeadCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"CatDead"` (Enum) |
| `attack` | Enum |  | 2 | `LennyCatSlap` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `HasRock`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"rock"` (Enum) |
| `attack` | Enum |  | 2 | `AmoebaRockBash` (Enum) |


### Object: `Headless`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Headless"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `HealAlliesEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 4 | `false` (Boolean) |
| `mana` | Enum / Integer |  | 4 | `3` (Number), `2` (Number) |
| `stacks` | Enum / Integer |  | 4 | `3` (Number), `2` (Number) |


### Object: `HealRandomInjury`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `158` (Number) |
| `name` | Enum |  |  | `"KEYWORD_HEALRANDOMINJURY_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_HEALRANDOMINJURY_DESC"` (String) |


### Object: `Health`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_HEALTH_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_HEALTH_DESC"` (String) |


### Object: `HeatWave`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combo` | Array |  |  | `[HeatWave_Particles HeatWave_Distortion]` (Array) |
| `desc` | Enum |  |  | `"WEATHER_HEATWAVE_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `hint_persistent_elements` | Array |  |  | `[Heat]` (Array) |
| `name` | Enum |  |  | `"WEATHER_HEATWAVE_NAME"` (String), `"KEYWORD_DEHYDRATED_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_DEHYDRATED_DESC"` (String) |


### Object: `HeavyHits`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_HEAVYHITS_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_HEAVYHITS_DESC_STACKS"` (String) |


### Object: `Hint_CrackedVisuals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Cracked"` (Enum) |


### Object: `Hint_CrackedVisuals2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"ChargingCracked"` (Enum) |


### Object: `Hint_CrackedVisuals3`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"SwallowedCracked"` (Enum) |


### Object: `Holding`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Holding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Holy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatLeech` | Integer |  | 4 | `X` (Enum), `10` (Number), `1` (Number) |
| `animation_suffix` | Enum / Integer |  | 4 | `"1"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `HolyDamageBlessing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Array / Enum / Integer |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `damage_multiplier` | Number |  | 4 | `3` (Number), `2` (Number) |


### Object: `House1`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aux_positions` | Object |  | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum |  | 2 | `small` (Enum) |
| `movieclip_bg` | Enum |  | 2 | `HouseBackground1` (Enum) |
| `movieclip_fg` | Enum |  | 2 | `HouseForeground1` (Enum) |
| `room_positions` | Object |  | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String |  | 2 | `.8` (String) |


### Object: `House2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aux_positions` | Object |  | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum |  | 2 | `large` (Enum) |
| `movieclip_bg` | Enum |  | 2 | `HouseBackground2` (Enum) |
| `movieclip_fg` | Enum |  | 2 | `HouseForeground2` (Enum) |
| `room_positions` | Object |  | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String |  | 2 | `.7` (String) |


### Object: `House3`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aux_positions` | Object |  | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum |  | 2 | `large` (Enum) |
| `movieclip_bg` | Enum |  | 2 | `HouseBackground3` (Enum) |
| `movieclip_fg` | Enum |  | 2 | `HouseForeground3` (Enum) |
| `room_positions` | Object |  | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String |  | 2 | `.6` (String) |


### Object: `HumanDead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `DH` (Enum) |
| `attack` | Enum |  | 2 | `HCSpin` (Enum) |
| `tooltip` | Enum |  | 2 | `"ENEMY_HUMANCAT2_DESC"` (String) |


### Object: `HummingBird`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdSmall` (Enum) |


### Object: `Hunter`

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


### Object: `Ice`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Slow` | Array / Enum / Integer / Object |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `IceAgeUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `IceArmor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Mage` (Enum) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `desc` | Enum |  |  | `"PASSIVE_ICEASPECT_DESC"` (String) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"IceArmor"` (Enum), `"PASSIVE_ICEASPECT_NAME"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `IncAuxCounterCycle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer |  | 2 | `1` (Number) |
| `max` | Integer |  | 2 | `3` (Number) |


### Object: `InitialPhase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `T3Shoot` (Enum) |
| `move` | Enum |  | 2 | `FloatMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Insane_Ceiling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Insane"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Insane_Ground`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Insane"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Invulnerable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_INVULNERABLE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_INVULNERABLE_DESC"` (String) |


### Object: `Item`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  | 21 | `15` (Number), `5` (Number) |
| `mandatory` | Boolean |  | 14 | `true` (Boolean) |
| `pool` | Array / Enum |  | 18 | `[TutorialStick]` (Array), `[WaterBottle_Half]` (Array), `treasure_easy` (Enum), `rare` (Enum) |
| `weight` | Number |  | 2 | `1` (Number) |


### Object: `Jack_Gainaltfurniture`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | String |  | 16 | `NPC_JACK_JACK_GAINALTFURNITURE_4` (String), `NPC_JACK_JACK_GAINALTFURNITURE_2` (String) |
| `lock_controls` | Number |  | 2 | `1` (Number) |
| `set_state` | Enum |  | 8 | `closeup` (Enum), `blocking` (Enum) |
| `unlock_controls` | Number |  | 2 | `1` (Number) |


### Object: `Jester`

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


### Object: `Johnny`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `JohnnyBubs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `JohnnyHost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Host` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `JohnnyNettle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Joystick`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Joystick"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `JudgementDay`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"WEATHER_JUDGEMENT_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_JUDGEMENT_NAME"` (String) |


### Object: `JunkyardUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit1` | Object |  | 2 | `{ ... }` (Object) |


### Object: `JurassicUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `KillEnemyOfTypeAtBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemy_type` | Enum |  | 2 | `cat` (Enum), `any` (Enum) |
| `fallback_spawn` | Array |  |  | `[TomTom Kitten CatCaller Mangy]` (Array) |


### Object: `LargeAttic`

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


### Object: `LargeBirdPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `LargeHouse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `MediumHouse` (Enum) |
| `set_house` | Enum |  | 2 | `House3` (Enum) |


### Object: `LargeHouse_Floor2Large`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Floor2_Large` (Enum) |


### Object: `LargeHouse_Floor2Small`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Floor2_Small` (Enum) |


### Object: `LastHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `lobbed_attack` (Enum) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `LateStatusApplication`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddWeaponAux` | Integer / String |  | 2 | `-item_aux` (Enum), `1` (Number), `2` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `CurrentWeaponDamageUp` | Integer |  | 6 | `3` (Number), `1` (Number) |


### Object: `LeapClose`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `GKLeap` (Enum) |
| `move_weights` | Enum |  | 2 | `towards_aggro` (Enum) |


### Object: `Leave`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `leave` (Enum) |


### Object: `LeaveBehind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum |  | 8 | `CharmedMaggot` (Enum), `Twister` (Enum) |


### Object: `LevelUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  | 3 | `10` (Number) |


### Object: `Lifted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Lift"` (Enum) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Lighting`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient` | String |  | 10 | `.6` (String), `.8` (String) |
| `bigrays` | Array |  |  | `[0 0]` (Array), `[1 1]` (Array) |
| `smallray_clip` | Enum |  | 2 | `labligtht` (Enum), `Bunkerlight` (Enum) |
| `smallrays` | Array |  |  | `[0 0]` (Array), `[4 8]` (Array) |


### Object: `Lit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Lit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `LostSoul`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_LOSTSOUL_DESC"` (String) |
| `frame` | Integer |  |  | `180` (Number) |
| `kind` | Enum |  |  | `neck` (Enum) |
| `name` | Enum |  |  | `"ARMOR_LOSTSOUL_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `very_rare` (Enum) |


### Object: `Mage`

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


### Object: `MagicSeed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ITEM_MAGICSEED_DESC"` (String) |
| `frame` | Integer |  |  | `113` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_MAGICSEED_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |


### Object: `Math`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ApplyToSource` | Object |  | 2 | `{ ... }` (Object) |
| `Stun` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `stacks` | Enum / Integer |  | 4 | `1` (Number) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |


### Object: `MeatWorldUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 4 | `{ ... }` (Object) |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |


### Object: `MeatWorldUnlockedFull`

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


### Object: `Meaty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_MEATY_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_MEATY_DESC"` (String) |


### Object: `MedBirdPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `MedCatnip`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |


### Object: `MedScrap`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `PickupBase` (Enum) |


### Object: `Medic`

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


### Object: `MediumHouse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `Default` (Enum) |
| `set_house` | Enum |  | 2 | `House2` (Enum) |


### Object: `MediumHouse_SmallRoom`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum |  | 2 | `Floor1_Small` (Enum) |


### Object: `MergeDamageInstance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean |  | 2 | `false` (Boolean) |
| `force_no_hit_animation` | Boolean |  | 2 | `true` (Boolean) |


### Object: `MeteorShower`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"WEATHER_METEORS_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_METEORS_NAME"` (String) |


### Object: `Meteornado`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_in` | String |  |  | `.2` (String) |
| `alpha_out` | String |  |  | `.2` (String) |
| `desc` | Enum |  |  | `"WEATHER_METEORNADO_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `emit_amount` | Number |  |  | `1` (Number) |
| `emit_box` | Array |  |  | `[0 10 0 5 0 10]` (Array) |
| `emit_direction` | Array |  |  | `[0 1 0]` (Array) |
| `emit_rate` | Number |  |  | `200` (Number) |
| `emit_spread` | Number |  |  | `360` (Number) |
| `live_bounds` | Array |  |  | `[-999 999 -999 999 -999 999]` (Array) |
| `movieclip` | Array / Enum |  |  | `FX_MoonRock` (Enum) |
| `name` | Enum |  |  | `"WEATHER_METEORNADO_NAME"` (String) |
| `particle_lifetime` | Array |  |  | `[.1 3]` (Array) |
| `projection_matrix` | Enum |  |  | `default` (Enum) |
| `render_mode` | Enum |  |  | `separate` (Enum) |
| `rotation` | Array |  |  | `[0 360]` (Array) |
| `rotation_speed` | Array |  |  | `[-1000 1000]` (Array) |
| `scripts` | Object |  |  | `{ ... }` (Object) |
| `simulation_space` | Enum |  |  | `global` (Enum) |
| `size_start` | Array |  |  | `[.5 1.5]` (Array) |
| `speed_start` | Number |  |  | `5` (Number) |


### Object: `Metronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  |  | `tk_Metronome` (Enum) |
| `banned_abilities` | Array |  |  | `[BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine]` (Array) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `desc` | Enum |  |  | `"ITEM_METRONOME_DESC"` (String) |
| `frame` | Integer |  |  | `17` (Number) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"ITEM_METRONOME_NAME"` (String) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Jester` (Enum) |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |
| `tags` | Array / Enum |  |  | `[musical]` (Array) |
| `template` | Enum |  |  | `self_buff` (Enum) |


### Object: `Monk`

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


### Object: `MoonObeliskUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `MoonUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Mounted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Cat"` (Enum) |


### Object: `MouthFull`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"MouthFull"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `MoveAway`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 8 | `ExtraMove` (Enum), `MoveTwoCantrip` (Enum) |
| `move_weights` | Enum |  | 8 | `stay_far` (Enum), `keep_distance_always_move` (Enum) |


### Object: `MoveCenter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `move` (Enum) |
| `move_weights` | Enum |  | 4 | `stay_near_map_center` (Enum) |


### Object: `MoveClose`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 8 | `move` (Enum) |
| `move_for_ability` | Enum |  | 6 | `Spin_Enemy` (Enum), `attack` (Enum) |
| `move_weights` | Enum |  | 8 | `stay_close_avoid_allies` (Enum), `stay_close_always_move` (Enum) |


### Object: `MoveForBarrage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `ZaratanaVSBombardment` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_far` (Enum) |


### Object: `MoveForDash`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `attack` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |


### Object: `MoveForGrass`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `StegoGrassStomp` (Enum) |
| `move_for_ability` | Enum |  | 2 | `StegoEatGrass` (Enum) |
| `move_weights` | Enum |  | 2 | `minimum_move` (Enum) |


### Object: `MoveForPounce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `attack` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |


### Object: `MoveForSpin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `PyrophinaVSRun` (Enum) |
| `move_for_ability` | Enum |  | 2 | `PyrophinaVSSpinThrow` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |


### Object: `MoveForThrow`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `move` (Enum) |
| `move_for_ability` | Enum |  | 4 | `PyrophinaVSCatThrow` (Enum), `PyrophinaSoloCatThrow` (Enum) |
| `move_weights` | Enum |  | 4 | `util_minmove` (Enum) |


### Object: `MoveOneForPuke`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `AlienBeastMoveOne` (Enum) |
| `move_for_ability` | Enum |  | 2 | `AlienBeastPuke` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |


### Object: `MoveSpaced`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_weights` | Enum |  | 2 | `terminator_keep_distance_always_move` (Enum) |


### Object: `MoveToHead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `G3RunToHead` (Enum) |
| `move_for_ability` | Enum |  | 2 | `G3GrabHead` (Enum) |
| `move_weights` | Enum |  | 2 | `minimum_move` (Enum) |


### Object: `MoveTowards`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `move` (Enum) |
| `move_for_ability` | Enum |  | 2 | `attack` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |


### Object: `Mutant`

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


### Object: `Muted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_MUTED_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_MUTED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_MUTED_DESC"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_MUTED_DESC_SINGULAR"` (String) |


### Object: `NCGravecrawlFAR`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `NCGravecrawl` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_far` (Enum) |


### Object: `Necromancer`

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


### Object: `NeutronStar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `NextAbilityHeals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"NextAbilityHeals"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `NextActionLuckUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `LuckUp` (Enum) |


### Object: `NextAttackBonusRange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BONUSRANGE_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_BONUSRANGE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BONUSRANGE_DESC"` (String) |


### Object: `NextAttackSpecialCrit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer |  | 2 | `2` (Number) |
| `extra_coins_per_stack` | Integer |  | 2 | `2` (Number) |
| `luck_increase` | Integer |  | 2 | `1` (Number) |


### Object: `NextBasicAttackCritsThisTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean |  | 2 | `true` (Boolean) |
| `piercing` | Boolean |  | 2 | `true` (Boolean) |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |


### Object: `NextBattleStatusStacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Integer |  | 2 | `2` (Number) |
| `fights` | Integer |  | 2 | `9999` (Number) |


### Object: `NextDamageReduceAndHealAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"NextDamageReduceAndHealAllies"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `NextTurnDoubleRangedDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_DOUBLERANGEDDMG_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_DOUBLERANGEDDMG_DESC"` (String) |


### Object: `NoEyes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"0"` (Enum) |


### Object: `NoStick`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `ManglerJab` (Enum) |


### Object: `NonCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum |  | 2 | `spawnHolding` (Enum) |
| `formchange` | Enum |  | 6 | `SmallHolding` (Enum), `BigHolding` (Enum) |
| `statuses` | Object |  | 4 | `{ ... }` (Object) |


### Object: `Normal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 10 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Up"` (Enum) |
| `attack` | Enum |  | 4 | `TinaBasicBigMeleeA` (Enum), `SpewerLobbed_Normal` (Enum) |
| `passives` | Object |  | 20 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `NormalFull`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Full` (Enum) |
| `attack` | Enum |  | 2 | `SpewerSpit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `NotPriming`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 4 | `{ ... }` (Object) |


### Object: `Nothing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum |  | 2 | `spawn` (Enum) |


### Object: `Nuke`

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


### Object: `Obey`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `ObjectOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum |  | 4 | `Poop` (Enum) |


### Object: `Off`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `Off` (Enum) |


### Object: `OffMap`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 6 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `OffScreen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `OneAlive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 6 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 6 | `{ ... }` (Object) |


### Object: `OneEye`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"1"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Open`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Open` (Enum) |
| `attack` | Enum |  | 2 | `GSOpenAttack` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `OpenCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `OpenCat` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Out`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `OverHealToStatuses`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String |  | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `TakeExtraTurn` | Integer |  | 2 | `1` (Number) |
| `stack_scale` | Integer |  | 2 | `0` (Number) |


### Object: `Parousworm`

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


### Object: `ParticleAttractor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force` | Number |  | 1 | `100` (Number) |
| `force_end` | Number |  | 6 | `200` (Number), `500` (Number) |
| `force_start` | Number |  | 6 | `0` (Number) |
| `towards` | Array |  |  | `[5 0 5]` (Array), `[0 .5 0]` (Array) |


### Object: `ParticleBouncePlane`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String |  | 74 | `1` (Number), `0` (Number), `.1` (String), `.75` (String) |
| `friction` | Number / String |  | 70 | `5` (Number), `2` (Number), `.1` (String), `.2` (String) |
| `plane` | Enum |  | 32 | `right` (Enum), `back` (Enum) |
| `position` | Number |  | 32 | `10.5` (Number) |
| `rotation_dampening` | Number |  | 1 | `1` (Number) |


### Object: `ParticleCharacterCollision`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_sphere_offset` | Number |  | 1 | `0` (Number) |
| `inherit_velocity` | String |  | 1 | `.5` (String) |
| `pushforce` | Number |  | 1 | `2` (Number) |


### Object: `ParticleGlobalForce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Array |  | 27 | `3` (Number), `1` (Number), `.1` (String), `.5` (String) |
| `id` | Enum |  | 27 | `Wind` (Enum) |


### Object: `ParticleLineCollisions`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String |  | 6 | `1` (Number), `.5` (String) |
| `end_on_collision` | Boolean |  | 2 | `true` (Boolean) |
| `friction` | Number |  | 6 | `1` (Number), `0` (Number) |


### Object: `ParticleRandomForce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `begin` | Array |  |  | `[0 -20 0]` (Array), `[0 -10 0]` (Array) |
| `end` | Enum |  |  | `[0 -450 0]` (Array), `[0 [ 40 120 ] 0]` (Array) |


### Object: `ParticleTornadoForce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `axis` | Array |  |  | `[0 -0.5 0]` (Array), `[0 1 0]` (Array) |
| `force` | Number |  | 19 | `8` (Number), `5` (Number) |
| `point` | Array |  |  | `[1 1 1]` (Array), `[0 0 0]` (Array) |


### Object: `PeaceSymbol`

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


### Object: `PeaceSymbolFacePaint`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_PEACESYMBOLFACEPAINT_DESC"` (String) |
| `frame` | Integer |  |  | `194` (Number) |
| `kind` | Enum |  |  | `face` (Enum) |
| `name` | Enum |  |  | `"ARMOR_PEACESYMBOLFACEPAINT_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Hippie` (Enum) |


### Object: `PermanentCharm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Charmed` (Enum) |


### Object: `Pigeon`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdMed` (Enum) |


### Object: `PoolMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum |  |  | `[Shockwave Ping Telefrag Stasis Reduce Zealot]` (Array) |


### Object: `PopAndSpawn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `clone_items` | Boolean |  | 2 | `false` (Boolean) |
| `clone_referenced_catdata` | Boolean |  | 2 | `true` (Boolean) |
| `no_splatter` | Boolean |  | 2 | `false` (Boolean) |
| `object` | Array / Enum |  | 4 | `BoyShade` (Enum), `PlayerCat_ClotClone` (Enum) |


### Object: `Possessing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Possessing"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Primed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `GA_Telekinesis_Big` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `primed` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Priming`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 4 | `{ ... }` (Object) |


### Object: `Psychic`

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


### Object: `Pulp2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `2` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |


### Object: `Pulp3`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `3` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |


### Object: `Pulp4`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `4` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |


### Object: `Pulp5`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `5` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |


### Object: `Pulp6`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `6` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |


### Object: `Pulp7`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `7` (Number) |
| `attack` | Enum |  | 2 | `None` (Enum) |
| `move` | Enum |  | 2 | `None` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number |  | 2 | `1` (Number) |


### Object: `QuakeAreaChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number |  | 4 | `50` (Number) |
| `radius` | Array / Integer |  | 4 | `1` (Number), `0` (Number) |


### Object: `Rage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 16 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Rage"` (Enum) |
| `attack` | Enum |  | 2 | `ChubsSpinRage` (Enum) |
| `move_speed_multiplier` | Number |  | 2 | `2` (Number) |
| `partial_animation_suffix` | Enum / Integer |  | 8 | `"Rage"` (Enum) |
| `passives` | Object |  | 12 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 12 | `{ ... }` (Object) |


### Object: `Rain`

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


### Object: `RandomArmorPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `RandomBiggerArmorPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `RandomBiggerCatnipPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `RandomBiggerFoodPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `RandomCatnipPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `RandomDistanceDisplace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_dist` | Integer |  | 2 | `4` (Number) |
| `stacks` | Enum / Integer |  | 2 | `20` (Number) |


### Object: `RandomFoodPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `RandomKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer |  | 4 | `10` (Number), `3` (Number) |
| `min` | Integer |  | 4 | `1` (Number) |


### Object: `RaptorEgg`

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


### Object: `Raven`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdMed` (Enum) |


### Object: `RavenFeather`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_RAVENFEATHER_DESC"` (String) |
| `frame` | Integer |  |  | `179` (Number) |
| `kind` | Enum |  |  | `neck` (Enum) |
| `name` | Enum |  |  | `"ARMOR_RAVENFEATHER_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Feathered` (Enum) |


### Object: `ReduceManaCostExcludeBrainstorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_INSIGHT_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_INSIGHT_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_INSIGHT_DESC"` (String) |


### Object: `Regurge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `spawn` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spawn` (Enum) |


### Object: `RepressedMemoriesMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum |  | 4 | `Psychic` (Enum), `Jester` (Enum) |
| `stacks` | Enum / Integer |  | 4 | `1` (Number) |


### Object: `Return`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `return` (Enum) |


### Object: `ReturnA`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `HangerBotReturn` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close` (Enum) |


### Object: `RunFar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `PyrophinaVSRun` (Enum) |
| `move_weights` | Enum |  | 2 | `run_far` (Enum) |


### Object: `Sandstorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String |  |  | `amb_sandstorm.ogg` (String) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `desc` | Enum |  |  | `"WEATHER_SANDSTORM_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_SANDSTORM_NAME"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |


### Object: `ScrambleLastUsedSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean |  | 2 | `true` (Boolean) |


### Object: `Scrap`

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


### Object: `Seagull`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `sound` | Object |  |  | `{ ... }` (Object) |
| `variant_of` | Enum |  |  | `BirdMed` (Enum) |


### Object: `SerratedClaws`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_SERRATED_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_SERRATED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_SERRATED_DESC"` (String) |


### Object: `SetAnimationAlts`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dead` | Enum |  | 2 | `deadShot` (Enum) |
| `dying` | Enum |  | 2 | `shot` (Enum) |


### Object: `SetCrazyEyeBackgroundWeights`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `weights` | Array / Enum |  |  | `[0 0 1]` (Array), `[0 1 0]` (Array) |


### Object: `SewersUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Shadow`

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


### Object: `Shatter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `melee_attack` (Enum) |


### Object: `ShortCircuit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_SHORTCIRCUIT_NAME"` (String) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |
| `tooltip` | Enum |  |  | `"KEYWORD_SHORTCIRCUIT_DESC"` (String) |


### Object: `ShowFakeDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer |  | 2 | `999` (Number) |
| `style` | Array |  |  | `[crit]` (Array) |


### Object: `Sitting`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Chair` (Enum) |
| `attack` | Enum |  | 2 | `DoNothing` (Enum) |
| `move` | Enum |  | 2 | `DoNothing` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `SlotResult_Explode`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |


### Object: `SlotResult_Jackpot_Coins`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `spawn` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spawn` (Enum) |


### Object: `SlotResult_Nothing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `self_buff` (Enum) |


### Object: `SlotResult_RandomPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `spawn` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spawn` (Enum) |


### Object: `Small`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `""` (String) |
| `attack` | Enum |  | 2 | `GameteInflate` (Enum) |


### Object: `SmallAttic`

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


### Object: `SmallBirdPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `SmallHolding`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"Holding"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `SmallHoldingCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer |  | 2 | `"HoldingCat"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `SmallHouse_Attic`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum |  | 2 | `Default` (Enum) |
| `unlock_room` | Enum |  | 2 | `Attic` (Enum) |


### Object: `SmartMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `stacks` | Enum / Integer |  | 2 | `20` (Number) |
| `tags` | Array / Enum |  |  | `[musical]` (Array) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `upgraded` | Boolean |  | 2 | `true` (Boolean) |


### Object: `SmellBlood`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `self_buff` (Enum) |


### Object: `Snake`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `Snow`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum |  | 1 | `Snow` (Enum) |
| `alpha` | String |  |  | `.5` (String) |
| `ambient_sound` | String |  | 1 | `amb_snow.ogg` (String) |
| `combo` | Array |  |  | `[SnowB SnowM SnowF]` (Array) |
| `desc` | Enum |  |  | `"WEATHER_SNOW_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `emit_amount` | Number |  |  | `1` (Number) |
| `emit_box` | Array |  |  | `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array |  |  | `[0 -1 0]` (Array) |
| `emit_rate` | Number |  |  | `200` (Number) |
| `emit_spread` | Number |  |  | `10` (Number) |
| `hint_persistent_elements` | Array |  |  | `[Ice]` (Array) |
| `live_bounds` | Array |  |  | `[-0.5 999 -999 999 -0.5 999]` (Array) |
| `movieclip` | Array / Enum |  |  | `ParticleTestNoRandom` (Enum) |
| `name` | Enum |  |  | `"WEATHER_SNOW_NAME"` (String) |
| `particle_lifetime` | Number |  |  | `7` (Number) |
| `particles` | Array |  |  | `[Snow]` (Array) |
| `prewarm` | Number |  | 1 | `20` (Number) |
| `projection_matrix` | Enum |  |  | `default` (Enum) |
| `render_mode` | Enum |  |  | `separate` (Enum) |
| `rotation` | Array |  |  | `[0 360]` (Array) |
| `rotation_speed` | Array |  |  | `[-100 100]` (Array) |
| `rotation_speed_end` | Number |  |  | `0` (Number) |
| `scripts` | Object |  |  | `{ ... }` (Object) |
| `simulation_space` | Enum |  |  | `global` (Enum) |
| `size_end` | Number |  |  | `0` (Number) |
| `size_start` | Array |  |  | `[.3 .8]` (Array) |
| `skybox_frame` | Enum |  | 1 | `day_snow` (Enum) |
| `speed_start` | Array |  |  | `[2 4]` (Array) |


### Object: `SolarFlare`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation |  | 1 | `5` (Equation) |
| `desc` | Enum |  |  | `"WEATHER_SOLARFLARE_DESC"` (String) |
| `effects` | Object |  | 1 | `{ ... }` (Object) |
| `elements` | Array |  |  | `[Fire]` (Array) |
| `name` | Enum |  |  | `"WEATHER_SOLARFLARE_NAME"` (String) |


### Object: `SpawnTilePuddleOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_radius` | Number |  | 1 | `3.5` (Number) |
| `min_radius` | Number |  | 1 | `1.5` (Number) |
| `tile` | Array / Enum |  | 1 | `OilTile` (Enum) |


### Object: `SpawnVolcanoOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_radius` | Number |  | 2 | `2.2` (Number) |
| `min_radius` | Number / String |  | 2 | `1` (Number), `.2` (String) |
| `number` | Array / Integer |  |  | `[3 5]` (Array) |
| `object` | Array / Enum |  | 3 | `Sprout` (Enum), `MiniVolcano` (Enum) |
| `puddle_tile` | Array / Enum |  | 1 | `[BrambleTile TallBrambleTile]` (Array), `LavaTile` (Enum) |


### Object: `SpawningPhase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `SpearRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `CaveManSpearRun` (Enum) |
| `move_for_ability` | Enum |  | 4 | `CaveManPickupSpear` (Enum) |
| `move_weights` | Enum |  | 4 | `util_minmove` (Enum) |


### Object: `SpecialGodRays`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Big` | Object |  | 2 | `{ ... }` (Object) |


### Object: `SpellShield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"SpellShield"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `Squirrel`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `SquirrelForm`

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


### Object: `Standing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `BungaSmash` (Enum) |
| `move` | Enum |  | 2 | `DefaultMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Standing2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `BungaSmash` (Enum) |
| `move` | Enum |  | 2 | `BungaJumpMove` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 2 | `{ ... }` (Object) |


### Object: `Start_Ceiling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `StatBounty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_STATBOUNTY_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_STATBOUNTY_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_STATBOUNTY_DESC"` (String) |


### Object: `StatusCharactersOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | Object |  | 1 | `{ ... }` (Object) |
| `FloatingRockTrap` | Integer |  | 1 | `1` (Number) |
| `Thorns` | Integer |  | 1 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `tag_filter` | Enum |  | 1 | `rock` (Enum) |


### Object: `StatusCharactersOnRoundStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | Object |  | 1 | `{ ... }` (Object) |
| `Else` | Object |  | 1 | `{ ... }` (Object) |
| `Madness` | Array / Enum / Integer / Object |  |  | `[1 .1]` (Array), `[1 .25]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `Stimulation`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_STIMULATION_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_STIMULATION_DESC"` (String) |


### Object: `Stop`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `keyword_tooltips` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `SuckMF`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TormentorSuck` (Enum) |
| `decision_weights` | Enum |  | 2 | `careless` (Enum) |
| `move_weights` | Enum |  | 2 | `keep_distance` (Enum) |


### Object: `SwapWeapon`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum |  |  | `[TerminatorShotgun TerminatorSniper TerminatorUzi]` (Array) |


### Object: `SwitchMusic`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crossfade_speed` | Integer |  | 2 | `1` (Number) |
| `new_layer` | Enum |  | 14 | `battle` (Enum), `map` (Enum) |
| `new_song` | Enum |  | 12 | `same` (Enum) |


### Object: `Switcheroo`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"Switcheroo"` (Enum) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `SwordAndShield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `DestroyerAttack` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `SwordAndShield_Primed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"Holy"` (Enum) |
| `attack` | Enum |  | 2 | `DestroyerAttack` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `TF_TargetAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum |  | 2 | `util_target_allies` (Enum) |


### Object: `TF_TargetEnemies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum |  | 2 | `util_target_enemies` (Enum) |


### Object: `TVBotDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_DIE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_DIE_DESC"` (String) |


### Object: `TVBotDumb`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_DUMB_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_DUMB_DESC"` (String) |


### Object: `TVBotObey`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_OBEY_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_OBEY_DESC"` (String) |


### Object: `TVBotStop`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `155` (Number) |
| `name` | Enum |  |  | `"ENEMY_TVBOT_STOP_NAME"` (String) |
| `tooltip` | Enum |  |  | `"ENEMY_TVBOT_STOP_DESC"` (String) |


### Object: `Tank`

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


### Object: `Tar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `SpewerLobbed_Tar` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `TarFull`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `Full` (Enum) |
| `attack` | Enum |  | 2 | `SpewerSpit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Taunting`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"Taunting"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `TeamCastAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `CollectiveSpinImpl` (Enum), `CollectiveCounterImpl` (Enum) |
| `same_orientation` | Boolean |  | 2 | `true` (Boolean) |
| `tag_restriction` | Enum |  | 4 | `collective` (Enum) |


### Object: `TempBackstab`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TEMPBACKSTAB_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_TEMPBACKSTAB_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_TEMPBACKSTAB_DESC"` (String) |


### Object: `TempBonusKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BONUSKNOCKBACK_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `None` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BONUSKNOCKBACK_DESC"` (String) |


### Object: `TempBonusKnockbackDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BONUSKNOCKBACKDAMAGE_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `None` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BONUSKNOCKBACKDAMAGE_DESC"` (String) |


### Object: `TempCritChanceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `CritChanceUp` (Enum) |


### Object: `TempDexterityUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DexterityUp` (Enum) |


### Object: `TempInjuryImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TEMPIMMUNE_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_TEMPIMMUNE_DESC"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_TEMPIMMUNE_DESC_SINGULAR"` (String) |


### Object: `TempManaCostReduction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TEMPMANAREDUCTION_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_TEMPMANAREDUCTION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_TEMPMANAREDUCTION_DESC"` (String) |


### Object: `TempPassiveWhileHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer |  | 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `TempPreEmptiveCounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_PRECOUNTER_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_PRECOUNTER_DESC"` (String) |


### Object: `TempSpeedUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `SpeedUp` (Enum) |


### Object: `TemporaryItem`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `164` (Number) |
| `name` | Enum |  |  | `"KEYWORD_TEMPITEM_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TEMPITEM_DESC"` (String) |


### Object: `TheEndUnlocked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit0` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Thief`

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


### Object: `Throb`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |


### Object: `ThrobBubs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `ThrobHost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Host` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `ThrobNettle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `ThrobbingArteryDone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Thunderstorm`

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


### Object: `TieDyeBandana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_TIEDYEBANDANA_DESC"` (String) |
| `frame` | Integer |  |  | `209` (Number) |
| `kind` | Enum |  |  | `head` (Enum) |
| `name` | Enum |  |  | `"ARMOR_TIEDYEBANDANA_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `rare` (Enum) |
| `set` | Array / Enum |  |  | `Hippie` (Enum) |


### Object: `TilesMovedToCritChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"TilesMovedToCritChance"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `TilesMovedToMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"TilesMovedToMana"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `TilesMovedToNeighborHeal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"TilesMovedToNeighborHeal"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `TilesMovedToStrength`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"TilesMovedToStrength"` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `TimeDelayStatusApplication`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Cleanse` | Integer / Object |  | 2 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `CreateGlobalModifiers` | Object |  | 2 | `{ ... }` (Object) |
| `DoScreenShake` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `FormChange` | Enum / Object |  | 2 | `passive` (Enum), `Boris` (Enum), `{ ... }` (Object) |
| `FullHeal` | Integer |  | 2 | `1` (Number), `0` (Number) |
| `GlobalSpawnCharacter` | Enum |  | 2 | `MegaGuppy` (Enum) |
| `PlayBackground` | Integer |  | 2 | `1` (Number), `0` (Number) |
| `RemoveAmbientLightEffects` | Number |  | 2 | `4` (Number), `.5` (String) |
| `SwitchMusic` | Object |  | 4 | `{ ... }` (Object) |
| `Vaporize` | Integer |  | 2 | `1` (Number), `20` (Number) |
| `delay` | Number |  | 8 | `1.13333` (Number), `3` (Number), `.1` (String), `.25` (String) |


### Object: `Tinkerer`

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


### Object: `Toad`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `TowerDefenseStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_SENTRY_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_SENTRY_DESC"` (String) |


### Object: `TowerDefenseStatus2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_SENTRYPLUS_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_SENTRYPLUS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_SENTRYPLUS_DESC"` (String) |


### Object: `TradeLife`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `bonus_passives` | Object |  |  | `{ ... }` (Object) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |


### Object: `TrailBlazer`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"Trail Blazer"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip` | Enum |  |  | `None` (Enum) |


### Object: `TransformEquipment`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `from` | Enum |  | 2 | `JarOfChaos` (Enum) |
| `to` | Enum |  | 2 | `JarOfNothing` (Enum) |


### Object: `Transformed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Turkey`

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


### Object: `Turtle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `abilities` | Object |  |  | `{ ... }` (Object) |
| `ai` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |


### Object: `Turtled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `Turtle` (Enum) |
| `attack` | Enum |  | 4 | `None` (Enum) |
| `move` | Enum |  | 4 | `None` (Enum) |
| `passives` | Object |  | 4 | `{ ... }` (Object) |


### Object: `TwisterDisplaceWithDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation |  | 12 | `inherit` (Equation), `1` (Equation) |
| `exclude_prefix` | Enum |  | 2 | `Twister` (Enum) |
| `max_dist` | Integer |  | 12 | `3` (Number), `20` (Number) |
| `min_dist` | Integer |  | 4 | `3` (Number), `2` (Number) |


### Object: `TwoAlive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 6 | `{ ... }` (Object) |
| `turns` | Array / Integer / Object |  | 6 | `{ ... }` (Object) |


### Object: `TwoEyes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Unflip`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `TeleportFlipUp` (Enum) |
| `move_for_ability` | Enum |  | 2 | `Spin_Enemy` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_close_always_move` (Enum) |


### Object: `Unlit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Unlit` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Unwashed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `Unwashed` (Enum) |


### Object: `Up`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 4 | `"Up"` (Enum) |
| `passives` | Object |  | 6 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"OBJECT_TIREUP_DESC"` (String) |


### Object: `UseMoveAbilityWithAI`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `LEPortFar` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_far_move_far` (Enum) |


### Object: `VisualCountDownThenApplyStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum / Object |  | 2 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |


### Object: `VisualFlySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String |  |  | `amb_flyswarm.ogg` (String) |
| `desc` | Enum |  |  | `"WEATHER_TORFLIES_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"WEATHER_TORFLIES_NAME"` (String) |


### Object: `VolcanoAntennaAttached`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 4 | `{ ... }` (Object) |


### Object: `WaggleClone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cWaggle` | Boolean (Flag) / Object |  | 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| `cWaggle2x2` | Boolean (Flag) / Object |  | 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| `cWaggle3x3` | Boolean (Flag) / Object |  |  | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `stacks` | Enum / Integer |  | 2 | `5` (Number) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `lobbed_attack` (Enum) |


### Object: `WallOfFleshDone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `quest_event` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Washed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Washer`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `attack` | Enum |  | 2 | `BasicMelee` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_CULTISTWASHER_NAME"` (String) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Cultist"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_CULTISTWASHER_DESC"` (String) |


### Object: `Water`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AOEPuddle` | Enum |  | 4 | `X-1` (Enum) |
| `partial_animation_suffix` | Enum / Integer |  | 2 | `"Water"` (Enum) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |


### Object: `WeirdEgg`

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


### Object: `WereMan`

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


### Object: `Wind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer |  | 4 | `X` (Enum) |


### Object: `Windy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum |  | 1 | `Windy` (Enum) |
| `ambient_sound` | String |  | 1 | `amb_windy.ogg` (String) |
| `desc` | Enum |  |  | `"WEATHER_WINDY_DESC"` (String) |
| `effects` | Object |  |  | `{ ... }` (Object) |
| `hint_persistent_elements` | Array |  |  | `[Wind]` (Array) |
| `name` | Enum |  |  | `"WEATHER_WINDY_NAME"` (String) |
| `particles` | Array |  |  | `[WindFull]` (Array) |
| `prewarm` | Number |  | 1 | `5` (Number) |
| `skybox_frame` | Enum |  | 1 | `day_windy` (Enum) |


### Object: `WishBone`

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


### Object: `XIsTargetHealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer |  | 4 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |


### Object: `Zealot`

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


### Object: `ZealotBomb`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai` | Object |  | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer |  | 2 | `"BombZealot"` (Enum) |
| `attack` | Enum |  | 2 | `BBExplode` (Enum) |
| `name` | Enum |  | 2 | `"ENEMY_BOMBZEALOT_NAME"` (String) |
| `passives` | Object |  | 2 | `{ ... }` (Object) |
| `tooltip` | Enum |  | 2 | `"ENEMY_BOMBZEALOT_DESC"` (String) |

