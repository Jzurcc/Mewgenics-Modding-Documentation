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
| [`Default`](Characters_and_Bosses.md#object-default) | Enum / Object | The default form configuration for a unit, containing its standard stats and abilities. | 199 ||
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 114 ||
| [`Druid`](#object-druid) | Object | Specifies the 'Druid' form within FormChanger, used for boss dialogue. | 80 ||
| [`Fighter`](#object-fighter) | Object | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 80 ||
| [`Monk`](#object-monk) | Object | Defines a list of quotes for the Monk class. | 66 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 62 ||
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 62 ||
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 47 ||
| `rock` | Variable | A variable used in logic contexts. | 46 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 42 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 38 ||
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Specifies the name of the visual effect to play on the target tile. | 36 ||
| [`BounceObject`](Abilities_and_Spells.md#object-bounceobject) | Enum / Object | Specifies the object or projectile to spawn and bounce from the target. | 35 ||
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 29 ||
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. | 28 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 27 ||
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 26 ||
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 26 ||
| [`Normal`](Characters_and_Bosses.md#object-normal) | Integer / Object | The normal form configuration, used as a baseline state for shape-shifting units. | 24 ||
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 23 ||
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. | 21 ||
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 21 ||
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Contains effects that apply only if the target is a boss enemy. | 17 ||
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 ||
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 15 ||
| `force_contact` | Boolean | If true, the consumed unit is forced into contact with the consumer. | 15 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 14 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 14 ||
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 12 ||
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 12 ||
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 12 ||
| `do_not_pop_corpse` | Boolean | If true, the consumed unit's corpse is not popped upon consumption. | 11 ||
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 ||
| [`Conditional_FormulaIsPositive`](Abilities_and_Spells.md#object-conditional_formulaispositive) | Object | Defines effects that apply only if a given formula evaluates to a positive value. | 10 ||
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 10 ||
| `X` | Variable | A generic variable placeholder often used for coordinates or unknown values. | 10 ||
| [`Nuke`](Characters_and_Bosses.md#object-nuke) | Object | Defines a nuke form with no attack or movement options. | 10 ||
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. | 9 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 8 ||
| [`formula`](./Enums.md#enum-formula) | Enum | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 8 ||
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 8 ||
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 8 ||
| `wet` | Boolean | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 ||
| [`BlackShard`](#object-blackshard) | Object | Defines the BlackShard object, likely a collectible item or a specific entity in the game. | 8 ||
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Contains effects that apply only if the target is in the specified form. | 7 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 7 ||
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 7 ||
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | If set to 1, forces the target to perform an attack against a random or specified target. | 7 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 7 ||
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 7 ||
| `TempRangeUp` | Integer | The amount of temporary range increase applied. | 7 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 6 ||
| [`Conditional_Object`](Abilities_and_Spells.md#object-conditional_object) | Object | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 6 ||
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 6 ||
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 6 ||
| `RandomInjury` | Integer | The number of random injuries applied. | 6 ||
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 6 ||
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 6 ||
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 6 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 6 ||
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object | An object containing effects that are only applied if the target is the source unit itself. | 5 ||
| [`DestroyEquipmentAndAttachParasite`](Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 5 ||
| `LavaTile` | Variable | Represents a tile of lava on the map, which deals damage to units standing on it. | 5 ||
| `MovementUp` | Integer | The amount of movement increase or decrease applied. | 5 ||
| `SafeDie` | Integer | The number of times the unit can survive a fatal hit. | 5 ||
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array / Integer | The number of coins stolen from the target, or an array of `[number, probability]`. | 4 ||
| [`Conditional_Familiar`](Abilities_and_Spells.md#object-conditional_familiar) | Object | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 ||
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 4 ||
| `moonhand` | Variable | A variable representing the Moon Hand, likely a limb or entity type associated with lunar or cosmic themes. | 4 ||
| [`Reanimate`](Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object | The percentage chance to reanimate the target. | 4 ||
| `RepairAll` | Integer | The amount of durability restored to all equipped items. | 4 ||
| [`Thrash`](#object-thrash) | Object | Defines the Thrash ability, likely a close-range, multi-hit attack. | 4 ||
| [`ZombieCatFamiliar`](#object-zombiecatfamiliar) | Object | Defines the ZombieCat familiar, a companion entity that follows the unit in combat. | 4 ||
| [`BirthSquirrel`](#object-birthsquirrel) | Object | Defines the Birth Squirrel ability, which spawns a squirrel ally when used. | 4 ||
| `WaterTile_Current` | Variable | Represents a water tile with a current, pushing units in a specific direction. | 4 ||
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 3 ||
| [`Conditional_AffectedByElement`](Abilities_and_Spells.md#object-conditional_affectedbyelement) | Object | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Container for effects applied only on the first application of this ability during the turn. | 3 ||
| [`Conditional_LastHit`](Abilities_and_Spells.md#object-conditional_lasthit) | Object | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 ||
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | An object containing effects that can only trigger once per battle, preventing double-activation. | 3 ||
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 3 ||
| `drop_on_self_death` | Boolean | If true, the consumed unit is dropped when the consumer dies. | 3 ||
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. | 3 ||
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 3 ||
| `PullSourceToTarget` | Integer | The amount of tiles the source is pulled towards the target after the attack. | 3 ||
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object | The number of revives granted, or an object defining revive properties. | 3 ||
| `WaterTile` | Variable | Represents a standard water tile on the map, which may slow or hinder movement. | 3 ||
| [`HeadTumor`](#object-headtumor) | Object | Defines the HeadTumor enemy, likely a swollen-headed unit with unique abilities. | 3 ||
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 ||
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 ||
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 2 ||
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 2 ||
| [`Purge`](Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object | The number of status effects to purge from the target. | 2 ||
| [`SoulLink`](Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object | The number of soul link stacks applied. | 2 ||
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer | The number of stealth stacks applied. | 2 ||
| [`PoisonLace`](Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 ||
| [`poop`](Events_and_Encounters.md#object-poop) | Object | Defines a poop event or interaction, often part of a random encounter or response in dialogue. | 2 ||
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | Contains an inner effect block that is applied to a random living party member if one exists. | 2 ||
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. | 2 ||
| [`Conditional_BossOrBig`](Abilities_and_Spells.md#object-conditional_bossorbig) | Object | An object containing effects that are only applied if the target is a boss or large unit. | 2 ||
| [`Conditional_Buddy`](Abilities_and_Spells.md#object-conditional_buddy) | Object | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 ||
| [`Conditional_DestructibleCorpse`](Abilities_and_Spells.md#object-conditional_destructiblecorpse) | Object | An object containing effects that are only applied if the corpse is destructible. | 2 ||
| [`Conditional_Displaceable`](Abilities_and_Spells.md#object-conditional_displaceable) | Object | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 2 ||
| [`Conditional_NotAlly`](Abilities_and_Spells.md#object-conditional_notally) | Object | An object containing effects that are only applied if the target is not an ally of the source. | 2 ||
| [`Conditional_NotBossOrBig`](Abilities_and_Spells.md#object-conditional_notbossorbig) | Object | An object containing effects that are only applied if the target is not a boss or large unit. | 2 ||
| [`Conditional_NotShielded`](Abilities_and_Spells.md#object-conditional_notshielded) | Object | An object containing effects that are only applied if the target does not have a shield active. | 2 ||
| `FireTile` | Variable | Represents a tile of fire on the map, which deals damage to units on it over time. | 2 ||
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 2 ||
| `gamewin` | Variable | A variable that triggers the end of the game, typically set to true when victory conditions are met. | 2 ||
| [`HornCharge`](#object-horncharge) | Object | Defines the Horn Charge ability, a dash attack that uses the character's horns to impale enemies. | 2 ||
| `humanoid` | Variable | A variable indicating whether the unit has a humanoid body type, affecting appearances and interactions. | 2 ||
| `ManaLeeches` | Integer | The number of mana leech stacks applied. | 2 ||
| [`OffMap`](Characters_and_Bosses.md#object-offmap) | Object | The form configuration applied when the unit is off the battlefield map. | 2 ||
| `OilTile` | Variable | Represents a tile covered in oil on the map, which can ignite and explode when exposed to fire. | 2 ||
| `Ostracized` | Integer | The number of stacks of Ostracized applied. | 2 ||
| `PartyExplosion` | Variable | A variable that triggers a large explosive effect, often an event-based mechanic. | 2 ||
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 2 ||
| [`Pilfer`](Events_and_Encounters.md#object-pilfer) | Object | Defines the Pilfer ability, which steals an item or resource from the target. | 2 ||
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. | 2 ||
| `PullSourceToKnockbackImmuneTarget` | Integer | The amount of pull force applied to the source toward a knockback-immune target. | 2 ||
| [`Pulp2`](Characters_and_Bosses.md#object-pulp2) | Object | Form state for the second stage of pulping, with no attacks or movement. | 2 ||
| [`RandomPickup`](#object-randompickup) | Object | Defines the RandomPickup object, likely a lootable item with random contents. | 2 ||
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. | 2 ||
| `RepairWeaponCondition` | Integer | The amount of weapon condition restored. | 2 ||
| `TallGrassTile` | Number | The percentage chance of this tile being tall grass, which provides cover or concealment. | 2 ||
| `TempMovement` | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. | 2 ||
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. | 2 ||
| `the_coven` | Variable | A variable representing a group of characters called The Coven, likely a faction or story element. | 2 ||
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 ||
| [`ThrowPoop`](#object-throwpoop) | Object | Defines the Throw Poop ability, which hurls a projectile of feces at the target. | 2 ||
| [`AntlerSwipe`](#object-antlerswipe) | Object | Defines the Antler Swipe ability, a basic melee attack that uses the character's antlers. | 2 ||
| [`BerserkDash`](#object-berserkdash) | Object | Defines the Berserk Dash ability, a close-range charge that damages and knocks back enemies. | 2 ||
| `BlankTile` | Number | The number of blank tiles in a map segment, which are empty spaces with no special properties. | 2 ||
| [`Boulder`](#object-boulder) | Object | Defines the Boulder object, a large rock that blocks movement and can be destroyed or pushed. | 2 ||
| [`CharmTrap`](#object-charmtrap) | Object | Defines the Charm Trap, a hazard that charms units entering its area, turning them against allies. | 2 ||
| `flip` | Variable | A variable that triggers a flip animation or reverses the state of something. | 2 ||
| [`HardenSkin`](#object-hardenskin) | Object | Defines the Harden Skin ability, which increases the unit's defense by making its skin tougher. | 2 ||
| [`MonkeyThrow`](#object-monkeythrow) | Object | Defines the Monkey Throw ability, which hurls a projectile in a manner similar to a monkey. | 2 ||
| [`MoonHandDrop`](#object-moonhanddrop) | Object | A variant of MoonHandThrow that includes bonus passives to enable a finisher. | 2 ||
| [`Pounce`](#object-pounce) | Object | Defines the Pounce ability, a jumping attack that lunges at the target. | 2 ||
| [`Prance`](#object-prance) | Object | Defines the Prance ability, a self-targeted buff that increases evasion or mobility. | 2 ||
| [`Scavenge`](#object-scavenge) | Object | Defines the Scavenge ability, a movement skill that allows the unit to search for items. | 2 ||
| [`SquirrelForm`](Characters_and_Bosses.md#object-squirrelform) | Object | Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses. | 2 ||
| [`Synthesize`](#object-synthesize) | Object | Defines the Synthesize ability, a self-buff that creates or enhances items. | 2 ||
| [`TaintedOffering`](#object-taintedoffering) | Object | Defines the Tainted Offering ability, a harmful or corrupted gift bestowed upon a target. | 2 ||
| [`Tease`](#object-tease) | Object | Defines the Tease ability, a targeted status effect that provokes or irritates the target. | 2 ||
| [`TheDestroyer`](#object-thedestroyer) | Object | Defines The Destroyer object, likely a powerful boss or destructive entity. | 2 ||
| [`TigerSwipes`](#object-tigerswipes) | Object | Defines the Tiger Swipes ability, a rapid series of claw attacks. | 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object | Defines the rain weather effect with associated particle, sound, and rendering settings. | 1 ||
| [`megadino`](#object-megadino) | Variable | A variable representing a Mega Dinosaur, likely a large, powerful enemy or form. | 1 ||
| [`moonhead`](#object-moonhead) | Variable | A variable representing the Moon Head, likely a head type or entity associated with lunar themes. | 1 ||
| `alien` | Variable | A variable indicating the unit is an alien, affecting its type and interactions. | 1 ||
| [`AllyInfested`](#object-allyinfested) | Object | Defines the AllyInfested object, which spawns an infested ally under the player's control. | 1 ||
| `angeljunk` | Variable | A variable representing angel junk, likely a cosmetic or mechanical part of an angelic character. | 1 ||
| [`AntlerSwipe2`](#object-antlerswipe2) | Object | A variant of Antler Swipe with a different description and potentially different parameters. | 1 ||
| [`BasicDashAttackMove_NoKnockback`](#object-basicdashattackmove_noknockback) | Object | Defines a basic dash attack that deals damage without knocking back the target. | 1 ||
| `berserkIdle` | Variable | A variable that sets the unit's idle animation to a berserk state. | 1 ||
| `bonusbird` | Variable | A variable representing a bonus bird, likely an additional familiar or entity. | 1 ||
| [`Boris`](Characters_and_Bosses.md#object-boris) | Enum / Object | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 1 ||
| `BrambleTile` | Variable | Represents a tile of brambles on the map, which damages units crossing it. | 1 ||
| `chapter_corpse_medium` | Variable | A variable representing a medium-sized corpse prop used in chapter environments. | 1 ||
| [`Chitter`](#object-chitter) | Object | Defines the Chitter ability, a spell that deals magical damage or applies a status effect. | 1 ||
| [`cm_RaptorEggSpawn`](#object-cm_raptoreggspawn) | Object | Defines the template and meta properties for spawning a raptor egg entity. | 1 ||
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 ||
| [`Conditional_ActiveWeather_Any`](Abilities_and_Spells.md#object-conditional_activeweather_any) | Object | An object containing effects that execute only if any of the specified weather types are active. | 1 ||
| [`Conditional_Backstab`](Abilities_and_Spells.md#object-conditional_backstab) | Object | An object containing effects that execute only if the attack lands on the target's back. | 1 ||
| [`Conditional_CanBeHealed`](Abilities_and_Spells.md#object-conditional_canbehealed) | Object | An object containing effects that execute only if the target can be healed. | 1 ||
| [`Conditional_DebuffRoll`](Abilities_and_Spells.md#object-conditional_debuffroll) | Object | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 ||
| [`Conditional_FinishedSpawning`](Abilities_and_Spells.md#object-conditional_finishedspawning) | Object | Contains an inner effect block that only executes if the target has finished its spawning animation. | 1 ||
| [`Conditional_HasCleansableDebuffs`](Abilities_and_Spells.md#object-conditional_hascleansabledebuffs) | Object | An object containing effects that execute only if the unit has cleansable debuffs. | 1 ||
| [`Conditional_HasKnockback`](Characters_and_Bosses.md#object-conditional_hasknockback) | Object | An object containing actions that execute if the incoming damage has knockback. | 1 ||
| [`Conditional_IsPhysicalAttack`](Characters_and_Bosses.md#object-conditional_isphysicalattack) | Object | A conditional block that executes its child actions only if the triggering event is a physical attack. | 1 ||
| [`Conditional_IsTrample`](Abilities_and_Spells.md#object-conditional_istrample) | Object | An object containing effects that execute only if the ability is a trample attack. | 1 ||
| [`Conditional_LivingPlayerCat`](Abilities_and_Spells.md#object-conditional_livingplayercat) | Object | An object containing effects that execute only if the source is a living player-owned cat. | 1 ||
| [`Conditional_NotBig`](Abilities_and_Spells.md#object-conditional_notbig) | Object | An object containing effects that execute only if the target is not a 'big' unit. | 1 ||
| [`Conditional_SourceAbilityHasTag`](Abilities_and_Spells.md#object-conditional_sourceabilityhastag) | Object | An object containing effects that execute only if the source ability has the specified tag. | 1 ||
| [`Conditional_SourceHasStatus`](Abilities_and_Spells.md#object-conditional_sourcehasstatus) | Object | An object containing effects that execute only if the source unit has the specified status. | 1 ||
| `container` | Variable | A variable representing a generic container or inventory slot for items. | 1 ||
| [`DeathWormEat`](#object-deathwormeat) | Object | Defines the eat ability for Death Worm, using the return template and specifying its name and movement flag. | 1 ||
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 1 ||
| `DirtTile` | Variable | A variable representing a dirt tile type on the grid. | 1 ||
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Specifies the ability used to drop the consumed body. | 1 ||
| [`DualSword`](Characters_and_Bosses.md#object-dualsword) | Object | Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack. | 1 ||
| [`DybbukPossessed`](Abilities_and_Spells.md#object-dybbukpossessed) | Object | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 1 ||
| `EggSackTrap` | Variable | A variable representing an egg sack trap entity. | 1 ||
| [`EtherSoakedRag`](#object-ethersoakedrag) | Object | An object defining the properties of the Ether Soaked Rag item. | 1 ||
| [`Explosive`](Characters_and_Bosses.md#object-explosive) | Enum / Object | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 1 ||
| `GenericBuff` | Integer | A generic buff value applied to the unit. | 1 ||
| `ghost` | Variable | A variable representing a ghost unit or entity. | 1 ||
| `GlassTile` | Variable | A variable representing a glass tile type on the grid. | 1 ||
| `god` | Variable | A variable representing a god entity or modifier. | 1 ||
| [`Grown`](Characters_and_Bosses.md#object-grown) | Object | Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold. | 1 ||
| `grown_hitler_clone` | Variable | A variable representing a fully grown Hitler clone unit. | 1 ||
| [`HalfDead`](Characters_and_Bosses.md#object-halfdead) | Object | Defines the half-dead form with reduced movement and a dash attack. | 1 ||
| [`HardenSkin2`](#object-hardenskin2) | Object | An object defining the upgraded Harden Skin ability. | 1 ||
| [`head_CrownOfHorns`](#object-head_crownofhorns) | Object | A logic key that applies the Crown of Horns head item effect, causing retaliatory damage when the unit is hit. | 1 ||
| `hitler_clone` | Variable | A variable representing a Hitler clone unit. | 1 ||
| `hitler_clone_fetus` | Variable | A variable representing the fetus stage of a Hitler clone. | 1 ||
| [`Infested`](Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object | The number of stacks of Infested applied. | 1 ||
| `JesterMinusColorless` | Variable | A variable representing a Jester variant without colorless mechanics. | 1 ||
| [`JewelOfDrog`](#object-jewelofdrog) | Object | An object defining the properties of the Jewel of Drog item. | 1 ||
| `kill_on_consume` | Boolean | If true, the consumed unit is killed immediately upon consumption. | 1 ||
| [`MegaGuppy`](#object-megaguppy) | Object | An object defining the properties of the Mega Guppy transformation or item. | 1 ||
| [`MockSong`](#object-mocksong) | Object | Defines the Mock Song spell, the basic attack for mockingbird form, including its name and description. | 1 ||
| [`MockSong2`](#object-mocksong2) | Object | Defines the upgraded Mock Song spell variant for mockingbird form. | 1 ||
| [`MonkeyThrow2`](#object-monkeythrow2) | Object | An object defining the upgraded Monkey Throw ability. | 1 ||
| [`MoonHeadFlail`](#object-moonheadflail) | Object | An object defining the Moon Head Flail ability or item. | 1 ||
| `NoDeathrattle` | Variable | A variable flag that prevents the unit from triggering deathrattle effects. | 1 ||
| `OverrideChainKnockbackDamage` | Equation | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 1 ||
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 1 ||
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 1 ||
| [`Prance2`](#object-prance2) | Object | Defines an upgraded variant of the Prance ability, using a different description. | 1 ||
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. | 1 ||
| `rotate_right` | Variable | A variable representing a right rotation action or state. | 1 ||
| [`Scavenge2`](#object-scavenge2) | Object | Defines an upgraded variant of the Scavenge ability, using a different description. | 1 ||
| `Scrambled` | Integer | The number of stacks of Scrambled applied. | 1 ||
| [`Small`](Characters_and_Bosses.md#object-small) | Object | Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation. | 1 ||
| [`SmallHolding`](Characters_and_Bosses.md#object-smallholding) | Object | Form state when the unit is holding a small object, triggering a form change while consuming. | 1 ||
| [`SmallHoldingCat`](Characters_and_Bosses.md#object-smallholdingcat) | Object | Form state when the unit is holding a cat, triggering a form change while consuming. | 1 ||
| `spear` | Variable | A variable representing a spear weapon type. | 1 ||
| `SplashDamage` | Integer | The radius (in tiles) for splash damage applied to adjacent targets. | 1 ||
| [`Standing`](Characters_and_Bosses.md#object-standing) | Object | Form state where the unit is standing, with default movement and attack. | 1 ||
| [`Synthesize2`](#object-synthesize2) | Object | Defines an upgraded variant of the Synthesize ability, using a different description. | 1 ||
| [`TaintedOffering2`](#object-taintedoffering2) | Object | An object defining the upgraded Tainted Offering ability. | 1 ||
| `TallFlowerTile` | Variable | A variable representing a tall flower tile type on the grid. | 1 ||
| [`Tease2`](#object-tease2) | Object | Defines an upgraded variant of the Tease ability, using a different description. | 1 ||
| `the_nuke_bearer` | Variable | A variable representing the entity that carries the nuke. | 1 ||
| `themotherspike` | Variable | A variable representing the Mother Spike entity. | 1 ||
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 ||
| [`TigerSwipes2`](#object-tigerswipes2) | Object | An object defining the upgraded Tiger Swipes ability. | 1 ||
| [`Timber`](#object-timber) | Object | Defines the Timber trample dash ability, an alt basic attack for Tree Form. | 1 ||
| [`TinaFlail`](#object-tinaflail) | Object | An object defining the Tina Flail ability or item. | 1 ||
| [`TinaFlailRage`](#object-tinaflailrage) | Object | An object defining the rage variant of the Tina Flail ability. | 1 ||
| [`TransformWeapon`](Abilities_and_Spells.md#object-transformweapon) | Object | An object with `from` and `to` fields specifying the weapon transformation. | 1 ||
| `weapon_throw` | Variable | A variable representing a weapon throw action or projectile. | 1 ||
| [`weather`](./Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. |||
| `contact_requires_adjacency` | Boolean | If false, contact effects are not restricted to adjacent tiles, allowing contact to trigger at range. | 0 ||
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 0 ||
| `two_way_contact` | Boolean | If true, contact effects apply to both the attacker and the target when the damage instance hits. | 0 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 0 ||
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
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. || `all_disorders` (Enum), `{ ... }` (Object) |

</details>

---

#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 59

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. || `-item_aux` (Enum), `2` (Number), `1` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `EquipPermanentItem` | Enum | The name of the item to permanently equip to the source. || `BoneClub` (Enum), `Kidney` (Enum) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. || `Necromancer` (Enum), `Thief` (Enum), `{ ... }` (Object) |
| `FindItem` | Enum | The name of the specific item to find and add to the source's inventory. || `BoneClub` (Enum), `Pearl` (Enum) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. || `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `passive` (Enum), `Default` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. || `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `2*X` (Enum), `3*X` (Enum), `3` (Number), `8` (Number) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| [`weather`](./Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 0 ||

</details>

---

#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `2` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |

</details>

---

#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 8 | `[1 .5]` (Array), `6` (Number), `3` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 1 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. || `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. || `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Contains effects that apply only if the target is in the specified form. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomMutation` | Integer | The number of random mutations to apply. || `3` (Number), `1` (Number) |
| `SafeDoomed` | Enum / Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `LaunchOffScreen` | String | A formula string that determines the knockback force to launch the unit off-screen. || `10+bonus_melee_ability_damage` (Enum) |

</details>

---

#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 3 ||
| [`Conditional_PartyMember`](#conditional_partymember) | Object | A conditional block that executes its child actions only if the target is a party member. | 2 ||
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Conditional_FinishedSpawning`](Abilities_and_Spells.md#object-conditional_finishedspawning) | Object | Contains an inner effect block that only executes if the target has finished its spawning animation. | 1 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. || `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Marked`](Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `6` (Number), `-2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `-2` (Number), `5` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |

</details>

---

#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`formula`](./Enums.md#enum-formula) | Enum | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 8 ||
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 37 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `ChangeTilesUnder` | Enum | The tile type to change the ground tiles under the target to. || `LavaTile` (Enum), `DirtTile` (Enum) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. || `parasites` (Enum), `chapter_specific_item` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `cm_RaptorEggSpawn` (Enum), `tk_WeirdEgg_Spawn` (Enum), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. || `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `RandomMutation` | Integer | The number of random mutations to apply. || `3` (Number), `1` (Number) |

</details>

---

#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 20 ||
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `passive` (Enum), `Bully` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 47

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 6 ||
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Contains effects that apply only if the target is a boss enemy. | 4 ||
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Contains effects that apply only if the target is in the specified form. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `ChangeTilesUnder` | Enum | The tile type to change the ground tiles under the target to. || `LavaTile` (Enum), `DirtTile` (Enum) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. || `1` (Number), `6` (Number), `{ ... }` (Object) |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. || `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. || `HitlerCloneHeil` (Enum), `cm_Lard_Impl` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. || `Sprout` (Enum), `TheDestroyer` (Enum), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. || `MegaGuppy_SummonTheChild` (Enum), `ManglerThrowRemote` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 5 ||
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 ||
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 ||
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. || `1` (Number), `6` (Number), `{ ... }` (Object) |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. || `X` (Enum), `5` (Number), `2` (Number) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `[25 .01]` (Array), `50` (Number), `999` (Number) |

</details>

---

#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 7 ||
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `[1 .5]` (Array), `15` (Number), `20` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `Drunker` (Enum), `BigHolding` (Enum), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. || `MegaGuppy_SummonTheChild` (Enum), `ManglerThrowRemote` (Enum), `{ ... }` (Object) |

</details>

---

#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |

</details>

---

#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. || `1` (Number), `99` (Number) |

</details>

---

#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 2 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. || `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. || `10` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `[1 .25]` (Array), `6` (Number), `1` (Number) |

</details>

---

#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object | An object containing effects that are only applied if the target is the source unit itself. | 3 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 0 ||
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 0 ||

</details>

---

#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`SetItemAux`](Engine_StatusAndPassiveKeys.md#object-setitemaux) | Object | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. || `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. || `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |

</details>

---

#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||

</details>

---

#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. || `3` (Number), `10` (Number), `{ ... }` (Object) |

</details>

---

#### `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 85

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 2 ||
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| [`Revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| [`Conditional_Displaceable`](Abilities_and_Spells.md#object-conditional_displaceable) | Object | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 ||
| [`Conditional_HasKnockback`](Characters_and_Bosses.md#object-conditional_hasknockback) | Object | An object containing actions that execute if the incoming damage has knockback. | 1 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 ||
| [`Conditional_Object`](Abilities_and_Spells.md#object-conditional_object) | Object | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 1 ||
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`AllyInfested`](#object-allyinfested) | Array / Number / Object | Defines the AllyInfested object, which spawns an infested ally under the player's control. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `5` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`DybbukPossessed`](Abilities_and_Spells.md#object-dybbukpossessed) | Object | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `passive` (Enum), `Holy` (Enum), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. || `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. || `MoonHandMegaSqueeze` (Enum), `tk_ButterBean_Normal` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| [`Marked`](Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `Maggot` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. || `1` (Number), `9999` (Number) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. || `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. || `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2166

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 38 ||
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `[1 .5]` (Array), `3` (Number), `5` (Number), `{ ... }` (Object) |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 35 ||
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 25 ||
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 14 ||
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 | `[3 X-8]` (Array), `[1 .5]` (Array), `9` (Number), `6` (Number), `{ ... }` (Object) |
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Contains effects that apply only if the target is a boss enemy. | 13 ||
| [`Conditional_FormulaIsPositive`](Abilities_and_Spells.md#object-conditional_formulaispositive) | Object | Defines effects that apply only if a given formula evaluates to a positive value. | 10 ||
| [`Conditional_Speculative`](Abilities_and_Spells.md#object-conditional_speculative) | Object | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 10 ||
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .1]` (Array), `[3 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `5` (Number), `{ ... }` (Object) |
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 6 ||
| `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `[1 .25]` (Array), `[1 .10]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .2]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `3` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 5 ||
| [`Conditional_InForm`](Abilities_and_Spells.md#object-conditional_inform) | Object | Contains effects that apply only if the target is in the specified form. | 5 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 5 ||
| [`Conditional_Object`](Abilities_and_Spells.md#object-conditional_object) | Object | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 5 ||
| [`Conditional_PlayerCat`](Abilities_and_Spells.md#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 5 ||
| [`Conditional_Familiar`](Abilities_and_Spells.md#object-conditional_familiar) | Object | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 ||
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Reanimate`](Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object | The percentage chance to reanimate the target. | 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `SizeScale` | Number | The multiplier applied to the unit's visual and hitbox size. | 4 | `1.1` (Number), `1.3` (Number), `.6` (String), `.8` (String) |
| [`Conditional_AffectedByElement`](Abilities_and_Spells.md#object-conditional_affectedbyelement) | Object | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Container for effects applied only on the first application of this ability during the turn. | 3 ||
| [`Conditional_LastHit`](Abilities_and_Spells.md#object-conditional_lasthit) | Object | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 ||
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `[1 .5]` (Array), `15` (Number), `50` (Number), `{ ... }` (Object) |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 2 | `1` (Number) |
| [`Leeches`](Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 2 ||
| [`Conditional_BossOrBig`](Abilities_and_Spells.md#object-conditional_bossorbig) | Object | An object containing effects that are only applied if the target is a boss or large unit. | 2 ||
| [`Conditional_Buddy`](Abilities_and_Spells.md#object-conditional_buddy) | Object | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 ||
| [`Conditional_DestructibleCorpse`](Abilities_and_Spells.md#object-conditional_destructiblecorpse) | Object | An object containing effects that are only applied if the corpse is destructible. | 2 ||
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 ||
| [`Conditional_IsSelf`](Abilities_and_Spells.md#object-conditional_isself) | Object | An object containing effects that are only applied if the target is the source unit itself. | 2 ||
| [`Conditional_NotAlly`](Abilities_and_Spells.md#object-conditional_notally) | Object | An object containing effects that are only applied if the target is not an ally of the source. | 2 ||
| [`Conditional_NotBossOrBig`](Abilities_and_Spells.md#object-conditional_notbossorbig) | Object | An object containing effects that are only applied if the target is not a boss or large unit. | 2 ||
| [`Conditional_NotShielded`](Abilities_and_Spells.md#object-conditional_notshielded) | Object | An object containing effects that are only applied if the target does not have a shield active. | 2 ||
| [`Conditional_OncePerBattle`](Abilities_and_Spells.md#object-conditional_onceperbattle) | Object | An object containing effects that can only trigger once per battle, preventing double-activation. | 2 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 2 ||
| `MagicWeakness` | Array / Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`PoisonLace`](Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Purge`](Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object | The number of status effects to purge from the target. | 2 | `3` (Number), `0` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `3` (Number), `-3` (Number) |
| [`Reflect`](Engine_StatusAndPassiveKeys.md#object-reflect) | Integer / Object | The amount of reflect stacks applied. | 2 | `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| [`Revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| [`SoulLink`](Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object | The number of soul link stacks applied. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Infested`](Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object | The number of stacks of Infested applied. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 ||
| [`Conditional_ActiveWeather_Any`](Abilities_and_Spells.md#object-conditional_activeweather_any) | Object | An object containing effects that execute only if any of the specified weather types are active. | 1 ||
| [`Conditional_Backstab`](Abilities_and_Spells.md#object-conditional_backstab) | Object | An object containing effects that execute only if the attack lands on the target's back. | 1 ||
| [`Conditional_CanBeHealed`](Abilities_and_Spells.md#object-conditional_canbehealed) | Object | An object containing effects that execute only if the target can be healed. | 1 ||
| [`Conditional_DebuffRoll`](Abilities_and_Spells.md#object-conditional_debuffroll) | Object | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 ||
| [`Conditional_Displaceable`](Abilities_and_Spells.md#object-conditional_displaceable) | Object | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 ||
| [`Conditional_HasCleansableDebuffs`](Abilities_and_Spells.md#object-conditional_hascleansabledebuffs) | Object | An object containing effects that execute only if the unit has cleansable debuffs. | 1 ||
| [`Conditional_IsTrample`](Abilities_and_Spells.md#object-conditional_istrample) | Object | An object containing effects that execute only if the ability is a trample attack. | 1 ||
| [`Conditional_LivingPlayerCat`](Abilities_and_Spells.md#object-conditional_livingplayercat) | Object | An object containing effects that execute only if the source is a living player-owned cat. | 1 ||
| [`Conditional_NotBig`](Abilities_and_Spells.md#object-conditional_notbig) | Object | An object containing effects that execute only if the target is not a 'big' unit. | 1 ||
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 ||
| [`Conditional_SourceAbilityHasTag`](Abilities_and_Spells.md#object-conditional_sourceabilityhastag) | Object | An object containing effects that execute only if the source ability has the specified tag. | 1 ||
| [`Conditional_SourceHasStatus`](Abilities_and_Spells.md#object-conditional_sourcehasstatus) | Object | An object containing effects that execute only if the source unit has the specified status. | 1 ||
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object | Defines the rain weather effect with associated particle, sound, and rendering settings. | 1 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. |||
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BounceObject`](Abilities_and_Spells.md#object-bounceobject) | Enum / Object | Specifies the object or projectile to spawn and bounce from the target. || `CharmedFlea_Champion` (Enum), `CharmedDip` (Enum), `{ ... }` (Object) |
| `BurgleCoin` | Array / Integer | The number of coins stolen from the target, or an array of `[number, probability]`. || `[1 .5]` (Array), `3` (Number), `1` (Number) |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). || `FireTile` (Enum), `GrassTile` (Enum), `{ ... }` (Object) |
| `ChangeTilesUnder` | Enum | The tile type to change the ground tiles under the target to. || `LavaTile` (Enum), `DirtTile` (Enum) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .25]` (Array), `[1 .15]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | Defines global gameplay modifiers to activate. || `{ ... }` (Object) |
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). || `1` (Number) |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. || `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. || `Tinkerer` (Enum), `Fighter` (Enum), `{ ... }` (Object) |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .25]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `FindExtraItemFromPoolOnBattleEnd` | Enum | Specifies the item pool from which an extra item is granted at the end of combat. || `combat_reward_easy` (Enum), `pills` (Enum) |
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | If set to 1, forces the target to perform an attack against a random or specified target. || `1` (Number), `{ ... }` (Object) |
| `ForceMoveAway` | Integer | The distance to force the target away from the source. || `1` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .25]` (Array), `[1 .15]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. || `{ ... }` (Object) |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. || `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. || `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`KnockOutCoin`](Abilities_and_Spells.md#object-knockoutcoin) | Integer / Object | The number of coins knocked out, with an optional probability or an object with stacks and chance. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `3` (Number), `-4` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `item_aux` (Enum), `X-1` (Enum), `2` (Number), `6` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `SkeletonCatFamiliar` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `OverrideChainKnockbackDamage` | String | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). || `3+bonus_melee_ability_damage` (Enum), `0` (Number) |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. || `1` (Number), `9999` (Number) |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. || `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. || `1` (Number), `2` (Number) |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. || `1` (Number), `2` (Number) |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. || `1` (Number), `2` (Number) |
| `Petrify` | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. || `[1 .15]` (Array), `[1 .2]` (Array), `1` (Number), `{ ... }` (Object) |
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. || `TheDestroyer` (Enum), `StemCat_HalfHealth` (Enum), `{ ... }` (Object) |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomInjury` | Integer | The number of random injuries applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. || `[1 .5]` (Array), `5` (Number), `6` (Number), `{ ... }` (Object) |
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). || `-1` (Number), `-2` (Number) |
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `[1 .25]` (Array), `6` (Number), `1` (Number) |
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object | The number of revives granted, or an object defining revive properties. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SetDefaultFace` | Enum | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. || `insane` (Enum), `happy` (Enum) |
| `Sleep` | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`StatusAllCharactersOnSpawn`](House_and_Environment.md#object-statusallcharactersonspawn) | Object | Defines status effects applied to all characters when they spawn into the battlefield. || `{ ... }` (Object) |
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | A container grouping multiple status effects to be applied simultaneously. || `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. || `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempDexterityUp` | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempMovement` | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. || `[1 .5]` (Array), `20` (Number), `1` (Number), `{ ... }` (Object) |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. || `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempStrengthUp` | Enum | The number of stacks of temporary Strength Up applied to the unit. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. || `MegaGuppy_SummonTheChild` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `Alert`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Alert` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `AllAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 | `{ ... }` (Object) |

</details>

### Object: `AllyInfested`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `faction` | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 | `allies` (Enum) |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 1 | `CharmedMaggot` (Enum) |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `Infested` (Enum) |

</details>

### Object: `Angry`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Angry"` (Enum) |

</details>

### Object: `Antidote`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_Antidote` (Enum) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_ANTIDOTE_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `2` (Number) |
| `frame` | Integer | The sprite frame index to display. || `103` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_ANTIDOTE_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_common` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `Appeal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_APPEAL_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_APPEAL_DESC"` (String) |

</details>

### Object: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `YOffset` | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 4 | `-.18` (String), `.35` (String) |

</details>

### Object: `Attacker`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |

</details>

### Object: `Attraction`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_ATTRACTION_NAME"` (String) |
| `name_reference_applier` | String | A localization key for the name displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_REF"` (String) |
| `tooltip_reference_applier` | String | A localization key for the tooltip description displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_DESC_REF"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ATTRACTION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_ATTRACTION_DESC"` (String) |

</details>

### Object: `BagOfSeeds`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `tk_BagOfSeeds` (Enum) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_BAGOFSEEDS_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `182` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_BAGOFSEEDS_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `rare` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Druid` (Enum) |

</details>

### Object: `Basement0`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundBasement0` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `33` (Number) |

</details>

### Object: `Basement1`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundBasement1` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `33` (Number) |

</details>

### Object: `Basement2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundBasement2` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `33` (Number) |

</details>

### Object: `Basement3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundBasement3` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `33` (Number) |

</details>

### Object: `Basement4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `5` (Number) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundBasement4` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `33` (Number) |

</details>

### Object: `BasementUpgrade`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Basement0` (Enum) |

</details>

### Object: `BasementUpgrade2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Basement1` (Enum) |

</details>

### Object: `BasementUpgrade3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade2` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Basement2` (Enum) |

</details>

### Object: `BasementUpgrade4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade3` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Basement3` (Enum) |

</details>

### Object: `BasementUpgrade5`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade4` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Basement4` (Enum) |

</details>

### Object: `Bear`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `BellyFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Belly"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Big`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `Big` (Enum), `"Big"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `GameteSpawn` (Enum) |
| `follow_character_tag` | Enum | Determines which character this visual effect follows. | 2 | `zaratana` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `position` | Array | The world-space coordinates for this object. || `[4.5 4.5]` (Array) |

</details>

### Object: `BigCatnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `BigFood`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `FoodBase` (Enum) |

</details>

### Object: `BigHolding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"BigHolding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `BigHoldingCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"BigHoldingCat"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `BigScrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `BiggestFood`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `FoodBase` (Enum) |

</details>

### Object: `BirdFeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_BIRDFEED_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `191` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_BIRDFEED_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |

</details>

### Object: `BirdPoopHat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Enum / Integer | The Charisma stat value or modifier. || `-1` (Number) |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ARMOR_BIRDPOOPHAT_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `30` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `head` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ARMOR_BIRDPOOPHAT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Fecal` (Enum) |

</details>

### Object: `Bishop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Bishop"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BBXLightning` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CULTISTBISHOP_NAME"` (String), `"ITEM_BISHOP_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CULTISTBISHOP_DESC"` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `2.5` (Number) |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `tk_Bishop` (Enum) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_BISHOP_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `6` (Number) |
| `frame` | Integer | The sprite frame index to display. || `201` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |

</details>

### Object: `BlackBird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdSmall` (Enum) |

</details>

### Object: `BlackHole`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"BlackHole"` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"OBJECT_BLACKHOLE_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"OBJECT_BLACKHOLE_DESC"` (String) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `NeutronStar` (Enum) |

</details>

### Object: `Blessing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`intro`](Events_and_Encounters.md#object-intro) | Object | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. || `{ ... }` (Object) |
| [`main`](Events_and_Encounters.md#object-main) | Object | An object containing the primary prompt and options for an event. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `Bomb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Button` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `wp_Bomb` (Enum) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_BOMB_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `1` (Number) |
| `frame` | Integer | The sprite frame index to display. || `11` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `weapon` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_BOMB_NAME"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |

</details>

### Object: `BoneyardUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `Boris`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"2"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `BothObelisksUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ ... }` (Object) |

</details>

### Object: `Bully`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `BunkerUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `Butcher`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate SkullBash Shred Chomp Succ...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_BUTCHER0" "TEAMNAME_ADJECTIVE_BUTCHER1" "TEAMNAME_ADJECTIVE_BUTCHER2" "TEAMNAME_ADJECTIVE_BUTCHER3" "TEAMNAME_ADJECTIVE_BUTCHER4" "TEAMNAME_ADJECTIVE_BUTCHER5" "TEAMNAME_ADJECTIVE_BUTCHER6" "TEAMNAME_ADJECTIVE_BUTCHER7" "TEAMNAME_ADJECTIVE_BUTCHER8" "TEAMNAME_ADJECTIVE_BUTCHER9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicButcherMelee]` (Array) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_BUTCHER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`innate_items`](Cat_Classes.md#object-innate_items) | Object | An object specifying the class's starting equipment, with item slot names as keys. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[con str lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_BUTCHER_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_BUTCHER0" "TEAMNAME_NOUN_BUTCHER1" "TEAMNAME_NOUN_BUTCHER2" "TEAMNAME_NOUN_BUTCHER3" "TEAMNAME_NOUN_BUTCHER4" "TEAMNAME_NOUN_BUTCHER5" "TEAMNAME_NOUN_BUTCHER6" "TEAMNAME_NOUN_BUTCHER7" "TEAMNAME_NOUN_BUTCHER8" "TEAMNAME_NOUN_BUTCHER9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[Putrefy NeverFull MainCourse FreshMeat Masochist Glutton Hooked Stompy Barbed GrapplingHook...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[Succ HogRush Chomp BodySlam Vurp Tromp Spoil Grill Sharpen SliceAndDice]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

</details>

### Object: `Cat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `formchange` | Enum | Specifies the form to change into. | 6 | `SmallHoldingCat` (Enum), `BigHoldingCat` (Enum) |
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 4 | `{ ... }` (Object) |
| `animation` | Enum | Specifies the animation played when the ability is used. | 2 | `spawnHoldingCat` (Enum) |

</details>

### Object: `Catepillar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `Catnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_Catnip` (Enum) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `7` (Number) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_SMALLCATNIPBAGGY_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `1` (Number) |
| `frame` | Integer | The sprite frame index to display. || `22` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_SMALLCATNIPBAGGY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_common` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `CatnipBig`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_Catnip` (Enum) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `12` (Number) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_LARGECATNIPBAGGY_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `1` (Number) |
| `frame` | Integer | The sprite frame index to display. || `3` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_LARGECATNIPBAGGY_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_common` (Enum) |

</details>

### Object: `CaveBaby`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"CaveBaby"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `CaveBabyMelee` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CAVEBABY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CAVEBABY_DESC"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `CavePerson` (Enum) |

</details>

### Object: `CaveMan`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"CaveMan"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `CaveMan3HitCombo` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 | `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CAVEMANMAN_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CAVEMANMAN_DESC"` (String) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `CavePerson` (Enum) |

</details>

### Object: `CaveManSpear`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"SpearCaveMan"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `CaveManThrowSpear` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 | `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_SPEARCAVEMAN_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_SPEARCAVEMAN_DESC"` (String) |

</details>

### Object: `CaveWoman`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"CaveWoman"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `CaveWomanKick` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CAVEMANWOMAN_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CAVEMANWOMAN_DESC"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `CavePerson` (Enum) |

</details>

### Object: `CaveWomanHasCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"CatCaveWoman"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `CaveWomanCatSlap` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CAVEMANWOMAN2_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CAVEMANWOMAN2_DESC"` (String) |

</details>

### Object: `CavesUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `CerberubsJumpBlind`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum | Specifies the named set of decision weight presets used by the AI. | 2 | `nubs_fakeblind` (Enum) |

</details>

### Object: `CerberubsJumpNormal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `CerberubsJump` (Enum) |
| `decision_weights` | Enum | Specifies the named set of decision weight presets used by the AI. | 2 | `default` (Enum) |

</details>

### Object: `ChaosAntennaAttached`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ ... }` (Object) |

</details>

### Object: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| `Stealth` | Array / Integer | The number of stealth stacks applied. | 1 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

### Object: `Charging`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `MoonHead_Blow` (Enum) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Charging"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `CharmedDip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `Dip` (Enum) |

</details>

### Object: `CharmedFloater`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `Floater` (Enum) |

</details>

### Object: `CharmedPile`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `Pile` (Enum) |

</details>

### Object: `Cherub`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdSmall` (Enum) |

</details>

### Object: `Chicken`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_Heal` (Enum) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `15` (Number) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_ROTISSERIECHICKEN_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `3` (Number) |
| `frame` | Integer | The sprite frame index to display. || `59` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_ROTISSERIECHICKEN_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_rare` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdLarge` (Enum) |

</details>

### Object: `Close`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `CloseConvert`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `MarshmallowConvert` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_close` (Enum) |

</details>

### Object: `Cockroach`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. || `[0 20]` (Array), `[10 20]` (Array) |

</details>

### Object: `Coin`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `Coin10`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `Coin` (Enum) |

</details>

### Object: `Coin2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `Coin` (Enum) |

</details>

### Object: `Coin3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `Coin` (Enum) |

</details>

### Object: `Coin4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `Coin` (Enum) |

</details>

### Object: `Colorless`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[Block Rest Brace Roll SharpenClaws Reach ManaDrain SoothingGlow Ponder Brainstorm...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_COLORLESS0" "TEAMNAME_ADJECTIVE_COLORLESS1" "TEAMNAME_ADJECTIVE_COLORLESS2"]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicMelee BasicMelee BasicShortRanged BasicShortLobbed]` (Array) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[str dex con int spd cha lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `move_pool` | Array | An array of movement ability names available to the class. || `[DefaultMove]` (Array) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_COLORLESS0" "TEAMNAME_NOUN_COLORLESS1" "TEAMNAME_NOUN_COLORLESS2"]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[SelfAssured LuckDrain Infested Worms Amped Furious MetalDetector DeathProof Leader Mange...]` (Array) |
| `tutorial_levelup_active_pool` | Array | An array of active ability names presented during tutorial level-up. || `[Block LickHeal Dump]` (Array) |
| `tutorial_levelup_active_pool_2` | Array | An array of active ability names presented in a second tutorial level-up. || `[GainThorns ButtScoot Burst HireHitman]` (Array) |
| `tutorial_levelup_passive_pool` | Array | An array of passive ability names presented during tutorial level-up. || `[Furious PressurePoints LateBloomer ZenkaiBoost]` (Array) |

</details>

### Object: `Comfort`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_COMFORT_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_COMFORT_DESC"` (String) |

</details>

### Object: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

</details>

### Object: `Conditional_FinishedSpawning`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Imprison` | Enum | Specifies the type of unit or object to summon as a prison. | 2 | `Fly` (Enum), `BeefyCharmedLeech` (Enum) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

</details>

### Object: `CoreObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ ... }` (Object) |

</details>

### Object: `CoreUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `CraterUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](Map_Generation_and_Routing.md#object-exit1) | Object | An object defining the properties of the second exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `Cultist`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Cultist"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BasicMelee` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CULTISTLACKEY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CULTISTLACKEY_DESC"` (String) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `Damaged`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |

</details>

### Object: `DashRandomly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `ShamblerDash` (Enum) |
| `decision_weights` | Enum | Specifies the named set of decision weight presets used by the AI. | 4 | `blind` (Enum) |

</details>

### Object: `DeadHummingbird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_EatHummingbird` (Enum) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `20` (Number) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_DEADHUMMINGBIRD_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `2` (Number) |
| `frame` | Integer | The sprite frame index to display. || `245` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_DEADHUMMINGBIRD_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_very_rare` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Feathered` (Enum) |

</details>

### Object: `Default`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 54 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 20 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 4 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `LennyShove` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `LennyTrampleMove` (Enum) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `""` (String) |
| `set_house` | Enum | Specifies which house layout to use for this upgrade. | 2 | `House1` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Floor1_Large` (Enum) |

</details>

### Object: `Default_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Default_Ground`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `DemonicGlyph_Bite`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TOR_BITE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TOR_BITE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Bounce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TOR_BOUNCE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TOR_BOUNCE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Fire`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TOR_FIRE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TOR_FIRE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Movement`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TOR_MOVE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TOR_MOVE_DESC"` (String) |

</details>

### Object: `DemonicGlyph_Summon`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TOR_SUMMON_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TOR_SUMMON_DESC"` (String) |

</details>

### Object: `DesireMech`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |

</details>

### Object: `Die`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `DimensionXUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ ... }` (Object) |

</details>

### Object: `Dove`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdSmall` (Enum) |

</details>

### Object: `Down`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"Down"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `ButtFart` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `TeleportFlipUp` (Enum) |

</details>

### Object: `Druid`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[ManaBomb SongOfSpring GrantLife SquirrelSquad SummonSquirrel DruidSwap BattleCry SummonSnake SummonTurtle SummonToad...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_DRUID0" "TEAMNAME_ADJECTIVE_DRUID1" "TEAMNAME_ADJECTIVE_DRUID2" "TEAMNAME_ADJECTIVE_DRUID3" "TEAMNAME_ADJECTIVE_DRUID4" "TEAMNAME_ADJECTIVE_DRUID5" "TEAMNAME_ADJECTIVE_DRUID6" "TEAMNAME_ADJECTIVE_DRUID7" "TEAMNAME_ADJECTIVE_DRUID8" "TEAMNAME_ADJECTIVE_DRUID9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicDruidAbility]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_DRUID_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | An object defining innate passive abilities or effects that the class always possesses. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int str]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_DRUID_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_DRUID0" "TEAMNAME_NOUN_DRUID1" "TEAMNAME_NOUN_DRUID2" "TEAMNAME_NOUN_DRUID3" "TEAMNAME_NOUN_DRUID4" "TEAMNAME_NOUN_DRUID5" "TEAMNAME_NOUN_DRUID6" "TEAMNAME_NOUN_DRUID7" "TEAMNAME_NOUN_DRUID8" "TEAMNAME_NOUN_DRUID9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[SuperCrow NaturesGuidance PoisonIvy Pathfinder EmptyVessels WildAnimals BarkSkin SoothingSong Teamwork Bouquet...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[SummonSquirrel SummonToad Encourage Protection SongOfSpring BattleCry SafetyDance TigerForm RhinoForm InspirationalSong]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Drunker`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Drunk` (Enum) |

</details>

### Object: `DualSword`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"2"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's base movement speed. | 2 | `1.5` (Number) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |

</details>

### Object: `DualSword_Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Holy2"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `DestroyerAttack2` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's base movement speed. | 2 | `1.5` (Number) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_DESTROYER2_DESC"` (String) |

</details>

### Object: `Dumb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `DybbukPossessed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit_ability` | Enum | Determines the ability used when the Dybbuk possession ends. | 2 | `DybbukReturn` (Enum) |
| `punch_self_ability` | Enum | Determines the ability used for the possessed unit to attack itself. | 2 | `Dybbuk_StopHittingYourself` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DYBBUKED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_DYBBUKED_DESC"` (String) |

</details>

### Object: `Eagle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdLarge` (Enum) |

</details>

### Object: `Earth`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 4 | `X` (Equation) |

</details>

### Object: `Electric`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .1*X]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

### Object: `Empty`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""` (String) |

</details>

### Object: `EndOfTimeUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 4 | `{ ... }` (Object) |

</details>

### Object: `Escape`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `DybbukEscape` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `keep_distance_always_move` (Enum) |

</details>

### Object: `EventBounty`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_EVENTBOUNTY_NAME"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_EVENTBOUNTY_DESC"` (String) |

</details>

### Object: `Evolution`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_EVOLUTION_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_EVOLUTION_DESC"` (String) |

</details>

### Object: `EvolveAbilityFromPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 26 | `Fighter` (Enum), `Thief` (Enum) |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 26 | `true` (Boolean) |

</details>

### Object: `Explody`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Expl` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `ToxExplode` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Explosive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"3"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `FightPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `T3Shoot` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `FloatMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Fighter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[Spin Dash FirePunch IcePunch ThunderPunch FurySwipes SideSlash FighterLeap Uppercut Counter...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_FIGHTER0" "TEAMNAME_ADJECTIVE_FIGHTER1" "TEAMNAME_ADJECTIVE_FIGHTER2" "TEAMNAME_ADJECTIVE_FIGHTER3" "TEAMNAME_ADJECTIVE_FIGHTER4" "TEAMNAME_ADJECTIVE_FIGHTER5" "TEAMNAME_ADJECTIVE_FIGHTER6" "TEAMNAME_ADJECTIVE_FIGHTER7" "TEAMNAME_ADJECTIVE_FIGHTER8" "TEAMNAME_ADJECTIVE_FIGHTER9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicMelee_Fighter]` (Array) |
| `complicated_abilities` | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooHard Zoomzerk Bloodzerk ExhaustingBlow ChaosRampage...]` (Array) |
| `complicated_passives` | Array | An array of passive ability names flagged as complicated. || `[ShoulderCheck DumbMuscle ThickSkull MostValuableCat HitMe]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_FIGHTER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[str con spd]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_FIGHTER_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_FIGHTER0" "TEAMNAME_NOUN_FIGHTER1" "TEAMNAME_NOUN_FIGHTER2" "TEAMNAME_NOUN_FIGHTER3" "TEAMNAME_NOUN_FIGHTER4" "TEAMNAME_NOUN_FIGHTER5" "TEAMNAME_NOUN_FIGHTER6" "TEAMNAME_NOUN_FIGHTER7" "TEAMNAME_NOUN_FIGHTER8" "TEAMNAME_NOUN_FIGHTER9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[BloodLust Avenger Scars FasterWhenHit KillsHeal Vengeful HamsterStyle WeaponMaster ShoulderCheck SkullSmash...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `shield` | Enum / Integer | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. || `[1 .5]` (Array), `4` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[FurySwipes Dash Spin Confront FirePunch SideSlash Exert Berserk Stick Counter]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Fire`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `SpewerLobbed_Lava` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `FireFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Full` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `SpewerSpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `combo` | Array | A list of particle effect names that are spawned together in sequence. || `[FireSmoke FirePlumes FireWaves FireBase FireWhites]` (Array) |

</details>

### Object: `Firefly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. || `[0 2]` (Array) |

</details>

### Object: `FloatingDebris`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `20` (Number) |

</details>

### Object: `Floor1_Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 2 | `room1` (Enum) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. | 2 | `RoomBackgroundLargeF1` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 2 | `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. | 2 | `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. | 2 | `16` (Number) |

</details>

### Object: `Floor1_Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 2 | `room2` (Enum) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. | 2 | `RoomBackgroundSmallF1` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 2 | `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. | 2 | `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. | 2 | `16` (Number) |

</details>

### Object: `Floor2_Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame identifier used for the interstitial area of this room. || `room3` (Enum) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundLargeF2` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `16` (Number) |

</details>

### Object: `Floor2_Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `7` (Number) |
| `interstitial_bg_frame` | Enum | Specifies the background frame identifier used for the interstitial area of this room. || `room4` (Enum) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundSmallF2` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `16` (Number) |

</details>

### Object: `Flop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Down"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Flop2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Down"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Flush`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

</details>

### Object: `FlushBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `FlushHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Host` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `FlushNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Fly`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. || `[0 20]` (Array), `[10 20]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_FLY_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_FLY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `Food`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | If true, duplicate items of this type can appear in the same shop inventory. | 4 | `true` (Boolean) |
| `amount` | Array | For ambient light, the target brightness value (as a float or percentage array for RGB). | 4 | `10` (Number) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 4 | `5` (Number) |
| `weight` | Number | A multiplier or priority value for random selection or effect magnitude. | 2 | `5` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `FoodBase` (Enum) |

</details>

### Object: `FoodBig`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_Heal` (Enum) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `24` (Number) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_CATFOOD_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `1` (Number) |
| `frame` | Integer | The sprite frame index to display. || `2` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_CATFOOD_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_common` (Enum) |

</details>

### Object: `FoodMedium`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_Heal` (Enum) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `12` (Number) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_ASNACK_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `1` (Number) |
| `frame` | Integer | The sprite frame index to display. || `21` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_ASNACK_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_common` (Enum) |

</details>

### Object: `FoodMove`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `CaveBabyFoodMove` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_close_move_if_possible` (Enum) |

</details>

### Object: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean | If true, this option requires no cost to activate. | 2 | `false` (Boolean) |

</details>

### Object: `ForceTrample`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `BirthwortTrample` (Enum) |
| `decision_weights` | Enum | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast_careless` (Enum) |

</details>

### Object: `FreeSpell`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_FREESPELL_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_FREESPELL_DESC"` (String) |

</details>

### Object: `Full`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"Full"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `KirbySpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 | `{ ... }` (Object) |
| [`statuses_on_enter_form`](Characters_and_Bosses.md#object-statuses_on_enter_form) | Object | Statuses or abilities applied when entering this form. | 4 | `{ ... }` (Object) |

</details>

### Object: `FutureUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ ... }` (Object) |

</details>

### Object: `GenFlag_Boss_Spewer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](Combat_Rewards.md#object-boss) | Object | An object defining the properties of a boss encounter, such as rewards or level. | 2 | `{ ... }` (Object) |

</details>

### Object: `GenFlag_Boss_Stacy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](Combat_Rewards.md#object-boss) | Object | An object defining the properties of a boss encounter, such as rewards or level. | 2 | `{ ... }` (Object) |
| [`miniboss_event`](Map_Generation_and_Routing.md#object-miniboss_event) | Object | An object defining the properties of a mini-boss event at this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `GlowingSeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_GLOWINGSEED_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `71` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_GLOWINGSEED_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |

</details>

### Object: `GoldenEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_GOLDENEGG_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `190` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_GOLDENEGG_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |

</details>

### Object: `Grass`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |

</details>

### Object: `Gravity`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `Grown`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Grown` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `HitlerCloneSwipes` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_HITLERCLONE_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `1.5` (Number) |
| `weak_threshold` | Integer | The health threshold below which the unit is considered weakened. | 2 | `15` (Number) |

</details>

### Object: `GuaranteedJackpot`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Guarding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Guarding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `HalfDead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"2"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `RatKingDash` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `HardPathUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](Map_Generation_and_Routing.md#object-hard_initial) | Object | An object defining the properties of the initial hard path node. | 4 | `{ ... }` (Object) |

</details>

### Object: `Harpy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdLarge` (Enum) |

</details>

### Object: `HarpysClaw`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `wp_HarpyClaw` (Enum) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_HARPYSCLAW_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `199` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `weapon` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_HARPYSCLAW_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `very_rare` (Enum) |

</details>

### Object: `HasCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 10 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 10 | `LennyCatSlap` (Enum), `MoonHandSqueeze` (Enum) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 8 | `"Grabbing"` (Enum), `"Cat"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 8 | `{ ... }` (Object) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Swallowed"` (Enum) |

</details>

### Object: `HasDeadCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"CatDead"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `LennyCatSlap` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `HasRock`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"rock"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AmoebaRockBash` (Enum) |

</details>

### Object: `Headless`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Headless"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `HealRandomInjury`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `158` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_HEALRANDOMINJURY_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_HEALRANDOMINJURY_DESC"` (String) |

</details>

### Object: `Health`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_HEALTH_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_HEALTH_DESC"` (String) |

</details>

### Object: `Hint_CrackedVisuals`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Cracked"` (Enum) |

</details>

### Object: `Hint_CrackedVisuals2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"ChargingCracked"` (Enum) |

</details>

### Object: `Hint_CrackedVisuals3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"SwallowedCracked"` (Enum) |

</details>

### Object: `Holding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Holding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Holy`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 4 | `X` (Enum), `10` (Number), `1` (Number) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"1"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `House1`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](House_and_Environment.md#object-aux_positions) | Object | An object containing named coordinates for auxiliary objects like spawn points within this house. | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum | Specifies the background frame identifier used for positioning background elements. | 2 | `small` (Enum) |
| `movieclip_bg` | Enum | Specifies the background movie clip asset for this house. | 2 | `HouseBackground1` (Enum) |
| `movieclip_fg` | Enum | Specifies the foreground movie clip asset for this house. | 2 | `HouseForeground1` (Enum) |
| [`room_positions`](House_and_Environment.md#object-room_positions) | Object | An object containing named coordinates for each room's position within the house layout. | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 2 | `.8` (String) |

</details>

### Object: `House2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](House_and_Environment.md#object-aux_positions) | Object | An object containing named coordinates for auxiliary objects like spawn points within this house. | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum | Specifies the background frame identifier used for positioning background elements. | 2 | `large` (Enum) |
| `movieclip_bg` | Enum | Specifies the background movie clip asset for this house. | 2 | `HouseBackground2` (Enum) |
| `movieclip_fg` | Enum | Specifies the foreground movie clip asset for this house. | 2 | `HouseForeground2` (Enum) |
| [`room_positions`](House_and_Environment.md#object-room_positions) | Object | An object containing named coordinates for each room's position within the house layout. | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 2 | `.7` (String) |

</details>

### Object: `House3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](House_and_Environment.md#object-aux_positions) | Object | An object containing named coordinates for auxiliary objects like spawn points within this house. | 2 | `{ ... }` (Object) |
| `bg_placements_frame` | Enum | Specifies the background frame identifier used for positioning background elements. | 2 | `large` (Enum) |
| `movieclip_bg` | Enum | Specifies the background movie clip asset for this house. | 2 | `HouseBackground3` (Enum) |
| `movieclip_fg` | Enum | Specifies the foreground movie clip asset for this house. | 2 | `HouseForeground3` (Enum) |
| [`room_positions`](House_and_Environment.md#object-room_positions) | Object | An object containing named coordinates for each room's position within the house layout. | 2 | `{ ... }` (Object) |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 2 | `.6` (String) |

</details>

### Object: `HumanDead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `DH` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `HCSpin` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_HUMANCAT2_DESC"` (String) |

</details>

### Object: `HummingBird`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdSmall` (Enum) |

</details>

### Object: `Hunter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[LineShot SpawnMaggotFriend SpawnPooterFriend Marked HailOfNails ScatterShot BrambleShot BearTrap TwinShot CrossShot...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_HUNTER0" "TEAMNAME_ADJECTIVE_HUNTER1" "TEAMNAME_ADJECTIVE_HUNTER2" "TEAMNAME_ADJECTIVE_HUNTER3" "TEAMNAME_ADJECTIVE_HUNTER4" "TEAMNAME_ADJECTIVE_HUNTER5" "TEAMNAME_ADJECTIVE_HUNTER6" "TEAMNAME_ADJECTIVE_HUNTER7" "TEAMNAME_ADJECTIVE_HUNTER8" "TEAMNAME_ADJECTIVE_HUNTER9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicRanged_Hunter]` (Array) |
| `complicated_abilities` | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[Extend LastHit StakeOut Diversion ScoutMe CraftArrow BounceShot Vivisect SlopThePigs SpiderInjector...]` (Array) |
| `complicated_passives` | Array | An array of passive ability names flagged as complicated. || `[Hazardous Traps CatchProjectiles Host SleepDarts Survivalist]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_HUNTER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[dex spd int]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_HUNTER_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_HUNTER0" "TEAMNAME_NOUN_HUNTER1" "TEAMNAME_NOUN_HUNTER2" "TEAMNAME_NOUN_HUNTER3" "TEAMNAME_NOUN_HUNTER4" "TEAMNAME_NOUN_HUNTER5" "TEAMNAME_NOUN_HUNTER6" "TEAMNAME_NOUN_HUNTER7" "TEAMNAME_NOUN_HUNTER8" "TEAMNAME_NOUN_HUNTER9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[TakeAim HuntersBoon BroodMother TaintedMother Quiver SplitShot Hazardous ThornArrows Traps CatchProjectiles...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[SpawnPooterFriend BrambleShot SpawnBaitTrap BearTrap TerrainWalk NeedleShot ScatterShot Marked FleaShot HeavyShot]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Ice`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `IceAgeUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ ... }` (Object) |

</details>

### Object: `InitialPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `T3Shoot` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `FloatMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Insane_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Insane"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Insane_Ground`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Insane"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Item`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 21 | `15` (Number), `5` (Number) |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 18 | `[TutorialStick]` (Array), `[WaterBottle_Half]` (Array), `treasure_easy` (Enum), `rare` (Enum) |
| `mandatory` | Boolean | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 14 | `true` (Boolean) |
| `weight` | Number | A multiplier or priority value for random selection or effect magnitude. | 2 | `1` (Number) |

</details>

### Object: `Jack_Gainaltfurniture`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | String | Specifies a dialog entry or dialog tree to display. | 16 | `NPC_JACK_JACK_GAINALTFURNITURE_4` (String), `NPC_JACK_JACK_GAINALTFURNITURE_2` (String) |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 8 | `closeup` (Enum), `blocking` (Enum) |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 2 | `1` (Number) |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 2 | `1` (Number) |

</details>

### Object: `Jester`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[SmartMetronome RNGCannon Bump PowerUp]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_JESTER0" "TEAMNAME_ADJECTIVE_JESTER1" "TEAMNAME_ADJECTIVE_JESTER2" "TEAMNAME_ADJECTIVE_JESTER3" "TEAMNAME_ADJECTIVE_JESTER4" "TEAMNAME_ADJECTIVE_JESTER5" "TEAMNAME_ADJECTIVE_JESTER6" "TEAMNAME_ADJECTIVE_JESTER7" "TEAMNAME_ADJECTIVE_JESTER8" "TEAMNAME_ADJECTIVE_JESTER9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicMelee_Fighter BasicRanged_Hunter BasicMagicShortRanged BasicTankMelee BasicStraightShot_Thief BasicMedicMelee BasicButcherMelee BasicPsychicPull BasicNecroRanged]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_JESTER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[str dex con int spd cha lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_JESTER_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_JESTER0" "TEAMNAME_NOUN_JESTER1" "TEAMNAME_NOUN_JESTER2" "TEAMNAME_NOUN_JESTER3" "TEAMNAME_NOUN_JESTER4" "TEAMNAME_NOUN_JESTER5" "TEAMNAME_NOUN_JESTER6" "TEAMNAME_NOUN_JESTER7" "TEAMNAME_NOUN_JESTER8" "TEAMNAME_NOUN_JESTER9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[SuperLuck Goofball]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Johnny`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `JohnnyBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `JohnnyHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Host` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `JohnnyNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Joystick`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Joystick"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `JunkyardUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](Map_Generation_and_Routing.md#object-exit1) | Object | An object defining the properties of the second exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `JurassicUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `LargeAttic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `built_in_collision` | Array | A list of collision geometry definitions for the room. || `[[ 6 6 6 6 6 6 6 6 6...]` (Array) |
| `extra_bound_planes` | Array | A list of additional boundary planes for the room. || `[{ p [ 0 0 ] n [ 1 -2...]` (Array) |
| `height` | Integer | The height in tiles the target is launched into the air. || `9` (Number) |
| `id` | Enum | The unique numerical identifier for this injury or status effect. || `Attic` (Enum) |
| `interstitial_bg_frame` | Enum | Specifies the background frame identifier used for the interstitial area of this room. || `attic` (Enum) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RoomBackgroundAttic` (Enum) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |
| `width` | Number | The number of tiles the room spans horizontally. || `35` (Number) |

</details>

### Object: `LargeBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `LargeHouse`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `MediumHouse` (Enum) |
| `set_house` | Enum | Specifies which house layout to use for this upgrade. | 2 | `House3` (Enum) |

</details>

### Object: `LargeHouse_Floor2Large`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Floor2_Large` (Enum) |

</details>

### Object: `LargeHouse_Floor2Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `LargeHouse` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Floor2_Small` (Enum) |

</details>

### Object: `LastHit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `lobbed_attack` (Enum) |

</details>

### Object: `LeapClose`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `GKLeap` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `towards_aggro` (Enum) |

</details>

### Object: `Leave`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `leave` (Enum) |

</details>

### Object: `LevelUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 3 | `10` (Number) |

</details>

### Object: `Lifted`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Lift"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Lighting`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient` | String | A multiplier for the ambient light intensity. | 10 | `.6` (String), `.8` (String) |
| `smallray_clip` | Enum | Specifies the visual style or clip for small light rays. | 2 | `labligtht` (Enum), `Bunkerlight` (Enum) |
| `bigrays` | Array | A two-value array defining the intensity or count of large light rays. || `[0 0]` (Array), `[1 1]` (Array) |
| `smallrays` | Array | A two-value array defining the intensity or count of small light rays. || `[0 0]` (Array), `[4 8]` (Array) |

</details>

### Object: `Lit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Lit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `LostSoul`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ARMOR_LOSTSOUL_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `180` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `neck` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ARMOR_LOSTSOUL_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `very_rare` (Enum) |

</details>

### Object: `Mage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[Surf Bolt Fireball FreezeRay MagicMissile Blast WallOfFire HyperBeam MeteorStorm MegaBlast...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_MAGE0" "TEAMNAME_ADJECTIVE_MAGE1" "TEAMNAME_ADJECTIVE_MAGE2" "TEAMNAME_ADJECTIVE_MAGE3" "TEAMNAME_ADJECTIVE_MAGE4" "TEAMNAME_ADJECTIVE_MAGE5" "TEAMNAME_ADJECTIVE_MAGE6" "TEAMNAME_ADJECTIVE_MAGE7" "TEAMNAME_ADJECTIVE_MAGE8" "TEAMNAME_ADJECTIVE_MAGE9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicMagicShortRanged]` (Array) |
| `complicated_abilities` | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[DealWithTheDevil ForbiddenFlame ForbiddenFlood ForbiddenFulmination Corrupt FireSurge IceSurge LightningSurge Creshendo Divide...]` (Array) |
| `complicated_passives` | Array | An array of passive ability names flagged as complicated. || `[ElementalAttunement LatentEnergy MagicGuru One Two Four Five]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_MAGE_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[int cha dex]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_MAGE_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_MAGE0" "TEAMNAME_NOUN_MAGE1" "TEAMNAME_NOUN_MAGE2" "TEAMNAME_NOUN_MAGE3" "TEAMNAME_NOUN_MAGE4" "TEAMNAME_NOUN_MAGE5" "TEAMNAME_NOUN_MAGE6" "TEAMNAME_NOUN_MAGE7" "TEAMNAME_NOUN_MAGE8"]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[Micronaps HolyMantel Shrapnel BurningPaws LightningPaws IcePaws PawMissile Overload ChargeUp Recharged...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[MagicMissile Fireball FreezeRay Warp Surf WindSlash Absorb Bolt Inspire MegaBlast]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `MagicSeed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_MAGICSEED_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `113` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_MAGICSEED_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |

</details>

### Object: `MeatWorldUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 4 | `{ ... }` (Object) |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ ... }` (Object) |

</details>

### Object: `MeatWorldUnlockedFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](Map_Generation_and_Routing.md#object-mw_battle1) | Object | An object defining the properties of the first MeatWorld battle node. | 2 | `{ ... }` (Object) |
| [`mw_boss`](Map_Generation_and_Routing.md#object-mw_boss) | Object | An object defining the properties of the MeatWorld boss node. | 2 | `{ ... }` (Object) |
| [`mw_earlyhome`](Map_Generation_and_Routing.md#object-mw_earlyhome) | Object | An object defining the properties of the MeatWorld early home node. | 2 | `{ ... }` (Object) |
| [`mw_event1`](Map_Generation_and_Routing.md#object-mw_event1) | Object | An object defining the properties of the first MeatWorld event node. | 2 | `{ ... }` (Object) |
| [`mw_hard1`](Map_Generation_and_Routing.md#object-mw_hard1) | Object | An object defining the properties of the first MeatWorld hard path node. | 2 | `{ ... }` (Object) |
| [`mw_home`](Map_Generation_and_Routing.md#object-mw_home) | Object | An object defining the properties of the MeatWorld home node. | 2 | `{ ... }` (Object) |
| [`mw_quest_event`](Map_Generation_and_Routing.md#object-mw_quest_event) | Object | An object defining the properties of the MeatWorld quest event node. | 2 | `{ ... }` (Object) |
| [`mw_treasure`](Map_Generation_and_Routing.md#object-mw_treasure) | Object | An object defining the properties of the MeatWorld treasure node. | 2 | `{ ... }` (Object) |

</details>

### Object: `MedBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `MedCatnip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `MedScrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `Medic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[RangedHeal MeleeHeal Malaise OpenWounds Prayer Convert Cleanse HereticMark Zealot Haste...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_MEDIC0" "TEAMNAME_ADJECTIVE_MEDIC1" "TEAMNAME_ADJECTIVE_MEDIC2" "TEAMNAME_ADJECTIVE_MEDIC3" "TEAMNAME_ADJECTIVE_MEDIC4" "TEAMNAME_ADJECTIVE_MEDIC5" "TEAMNAME_ADJECTIVE_MEDIC6" "TEAMNAME_ADJECTIVE_MEDIC7" "TEAMNAME_ADJECTIVE_MEDIC8" "TEAMNAME_ADJECTIVE_MEDIC9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicMedicMelee]` (Array) |
| `complicated_abilities` | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[OpenWounds WitchHunt Adoubement DivineProtection ChosenWarrior SwiftSanctify DivineGift HolyWeapon GetDown Rebuke...]` (Array) |
| `complicated_passives` | Array | An array of passive ability names flagged as complicated. || `[RangedMedic ThouShaltNotKill BlessingOfHolyFire BlessingOfSpirit]` (Array) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_MEDIC0" "TEAMNAME_NOUN_MEDIC1" "TEAMNAME_NOUN_MEDIC2" "TEAMNAME_NOUN_MEDIC3" "TEAMNAME_NOUN_MEDIC4" "TEAMNAME_NOUN_MEDIC5" "TEAMNAME_NOUN_MEDIC6" "TEAMNAME_NOUN_MEDIC7" "TEAMNAME_NOUN_MEDIC8" "TEAMNAME_NOUN_MEDIC9"]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[HealingAura NaturalHealer Eternal Blessed EvilPatron AngelicInspiration TopOff SharingIsCaring Caretaker MoraleBoost...]` (Array) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[RangedHeal Rally Prayer FriendOrFoe HolyWeapon Zealot OpenWounds RallyCharge HallowedGround Cleanse]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `MediumHouse`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `Default` (Enum) |
| `set_house` | Enum | Specifies which house layout to use for this upgrade. | 2 | `House2` (Enum) |

</details>

### Object: `MediumHouse_SmallRoom`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `MediumHouse` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Floor1_Small` (Enum) |

</details>

### Object: `Monk`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[Propell Hadouken Cartwheel StoneFists Transcend HipToss Bruise Slapback Finisher Reverberate...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_MONK0" "TEAMNAME_ADJECTIVE_MONK1" "TEAMNAME_ADJECTIVE_MONK2" "TEAMNAME_ADJECTIVE_MONK3" "TEAMNAME_ADJECTIVE_MONK4" "TEAMNAME_ADJECTIVE_MONK5" "TEAMNAME_ADJECTIVE_MONK6" "TEAMNAME_ADJECTIVE_MONK7" "TEAMNAME_ADJECTIVE_MONK8" "TEAMNAME_ADJECTIVE_MONK9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicMonkMelee]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_MONK_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`innate_items`](Cat_Classes.md#object-innate_items) | Object | An object specifying the class's starting equipment, with item slot names as keys. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | An object defining innate passive abilities or effects that the class always possesses. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[int str lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_MONK_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_MONK0" "TEAMNAME_NOUN_MONK1" "TEAMNAME_NOUN_MONK2" "TEAMNAME_NOUN_MONK3" "TEAMNAME_NOUN_MONK4" "TEAMNAME_NOUN_MONK5" "TEAMNAME_NOUN_MONK6" "TEAMNAME_NOUN_MONK7" "TEAMNAME_NOUN_MONK8" "TEAMNAME_NOUN_MONK9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[SafeSwitching Mixup Turnabout MonkeyStyle BrickSkin JaggedEdges MindBreaker CobraStyle Tenderize LongArms...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[Propell Pogo ComboThrow ComboPull Bruise Anneal Hadouken ReallyFastRun Finisher UnbridledHits]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `MoonObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ ... }` (Object) |

</details>

### Object: `MoonUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `Mounted`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Cat"` (Enum) |

</details>

### Object: `MouthFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"MouthFull"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `MoveAway`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `ExtraMove` (Enum), `MoveTwoCantrip` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 8 | `stay_far` (Enum), `keep_distance_always_move` (Enum) |

</details>

### Object: `MoveCenter`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `move` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `stay_near_map_center` (Enum) |

</details>

### Object: `MoveClose`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `move` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 8 | `stay_close_avoid_allies` (Enum), `stay_close_always_move` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 6 | `Spin_Enemy` (Enum), `attack` (Enum) |

</details>

### Object: `MoveForBarrage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `ZaratanaVSBombardment` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_far` (Enum) |

</details>

### Object: `MoveForDash`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `attack` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveForGrass`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `StegoGrassStomp` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `StegoEatGrass` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `minimum_move` (Enum) |

</details>

### Object: `MoveForPounce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `attack` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveForSpin`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `PyrophinaVSRun` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `PyrophinaVSSpinThrow` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_close` (Enum) |

</details>

### Object: `MoveForThrow`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `move` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 4 | `PyrophinaVSCatThrow` (Enum), `PyrophinaSoloCatThrow` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `util_minmove` (Enum) |

</details>

### Object: `MoveOneForPuke`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AlienBeastMoveOne` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `keep_distance` (Enum) |

</details>

### Object: `MoveSpaced`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `move` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `terminator_keep_distance_always_move` (Enum) |

</details>

### Object: `MoveToHead`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `G3RunToHead` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `G3GrabHead` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `minimum_move` (Enum) |

</details>

### Object: `MoveTowards`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `move` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `attack` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_close` (Enum) |

</details>

### Object: `Mutant`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Mutant"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BBMutantSwipe` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's base movement speed. | 2 | `.5` (String) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CULTISTMUTANT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CULTISTMUTANT_DESC"` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdMed` (Enum) |

</details>

### Object: `NCGravecrawlFAR`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `NCGravecrawl` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_far` (Enum) |

</details>

### Object: `Necromancer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[MaggotArmy Reanimate Rebirth Pestilence Weakness SoulSuck EvilIncarnate SoulLink WeAreOne BloodRain...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_NECROMANCER0" "TEAMNAME_ADJECTIVE_NECROMANCER1" "TEAMNAME_ADJECTIVE_NECROMANCER2" "TEAMNAME_ADJECTIVE_NECROMANCER3" "TEAMNAME_ADJECTIVE_NECROMANCER4" "TEAMNAME_ADJECTIVE_NECROMANCER5" "TEAMNAME_ADJECTIVE_NECROMANCER6" "TEAMNAME_ADJECTIVE_NECROMANCER7" "TEAMNAME_ADJECTIVE_NECROMANCER8" "TEAMNAME_ADJECTIVE_NECROMANCER9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicNecroRanged]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_NECROMANCER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[dex cha con]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_NECROMANCER_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_NECROMANCER0" "TEAMNAME_NOUN_NECROMANCER1" "TEAMNAME_NOUN_NECROMANCER2" "TEAMNAME_NOUN_NECROMANCER3" "TEAMNAME_NOUN_NECROMANCER4" "TEAMNAME_NOUN_NECROMANCER5" "TEAMNAME_NOUN_NECROMANCER6" "TEAMNAME_NOUN_NECROMANCER7" "TEAMNAME_NOUN_NECROMANCER8" "TEAMNAME_NOUN_NECROMANCER9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[Vampirism OneWithNothing BedBugs WormLord InfiniteRebirth SacrificialLamb DeathIncarnate OffloadPain CambionConception Leechmother...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[SoulLink Reanimate Rebirth CarrionShot Pestilence BloodGeyser MaggotArmy Gravecrawl FullMoon CoffinFlop]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `NeutronStar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `NoEyes`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"0"` (Enum) |

</details>

### Object: `NoStick`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `ManglerJab` (Enum) |

</details>

### Object: `NonCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `formchange` | Enum | Specifies the form to change into. | 6 | `SmallHolding` (Enum), `BigHolding` (Enum) |
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 4 | `{ ... }` (Object) |
| `animation` | Enum | Specifies the animation played when the ability is used. | 2 | `spawnHolding` (Enum) |

</details>

### Object: `Normal`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 20 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 10 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `TinaBasicBigMeleeA` (Enum), `SpewerLobbed_Normal` (Enum) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Up"` (Enum) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `NormalFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Full` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `SpewerSpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `NotPriming`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 4 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Nothing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum | Specifies the animation played when the ability is used. | 2 | `spawn` (Enum) |

</details>

### Object: `Nuke`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Nuke` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ARMOR_NUKE_DESC"` (String) |
| `failable` | Boolean | If true, the event or action has a chance to fail. || `true` (Boolean) |
| `frame` | Integer | The sprite frame index to display. || `77` (Number) |
| `hint_destination` | Enum | Specifies the map destination hinted by this item or event. || `endoftime` (Enum) |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. || `true` (Boolean) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `neck` (Enum) |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. || `true` (Boolean) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ARMOR_NUKE_NAME"` (String) |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. || `true` (Boolean) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `quest` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Radioactive` (Enum) |
| `shield` | Enum / Integer | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. || `[1 .5]` (Array), `10` (Number) |
| `spd` | Enum / Integer | The Speed stat value or modifier. || `-2` (Number) |

</details>

### Object: `Obey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Off`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Off` (Enum) |

</details>

### Object: `OffMap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 6 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `OffScreen`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `OneAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 6 | `{ ... }` (Object) |

</details>

### Object: `OneEye`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"1"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Open`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Open` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `GSOpenAttack` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `OpenCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `OpenCat` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Out`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Parousworm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer | The Constitution stat value or modifier. || `-1` (Number) |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_PAROUSWORM_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `271` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_PAROUSWORM_NAME"` (String) |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. || `true` (Boolean) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |

</details>

### Object: `ParticleAttractor`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force_end` | Number | The final force applied to particles over time, as a scalar or 3D vector. | 6 | `200` (Number), `500` (Number) |
| `force_start` | Number | The initial force applied to particles, as a scalar or 3D vector. | 6 | `0` (Number) |
| `force` | Number | The force vector applied to particles. | 1 | `100` (Number) |
| `towards` | Array | A 3D vector point that the force pulls particles towards. || `[5 0 5]` (Array), `[0 .5 0]` (Array) |

</details>

### Object: `ParticleBouncePlane`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String | A multiplier for how much velocity is retained on bounce, from 0 (lost) to 1 (perfect). | 74 | `1` (Number), `0` (Number), `.1` (String), `.75` (String) |
| `friction` | Number / String | A scalar or 3D vector multiplier for velocity reduction applied over time. | 70 | `5` (Number), `2` (Number), `.1` (String), `.2` (String) |
| `plane` | Enum | Specifies the direction the particle bounces off. Valid values are "right" and "back". | 32 | `right` (Enum), `back` (Enum) |
| `position` | Number | The world-space coordinates for this object. | 32 | `10.5` (Number) |
| `rotation_dampening` | Number | The amount of rotational velocity retained after bouncing, where 1 is full retention. | 1 | `1` (Number) |

</details>

### Object: `ParticleCharacterCollision`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_sphere_offset` | Number | The vertical offset of the character collision sphere from the character's origin. | 1 | `0` (Number) |
| `inherit_velocity` | String | The fraction of the character's velocity inherited by the particle upon collision. | 1 | `.5` (String) |
| `pushforce` | Number | The magnitude of force applied to push the character away from the particle on collision. | 1 | `2` (Number) |

</details>

### Object: `ParticleGlobalForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Array | For ambient light, the target brightness value (as a float or percentage array for RGB). | 27 | `3` (Number), `1` (Number), `.1` (String), `.5` (String) |
| `id` | Enum | The unique numerical identifier for this injury or status effect. | 27 | `Wind` (Enum) |

</details>

### Object: `ParticleLineCollisions`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Number / String | A multiplier for how much velocity is retained on bounce, from 0 (lost) to 1 (perfect). | 6 | `1` (Number), `.5` (String) |
| `friction` | Number | A scalar or 3D vector multiplier for velocity reduction applied over time. | 6 | `1` (Number), `0` (Number) |
| `end_on_collision` | Boolean | If true, the particle is destroyed when it collides with a line. | 2 | `true` (Boolean) |

</details>

### Object: `ParticleRandomForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `begin` | Array | The initial force applied to the particle as a 3D vector, where any axis can be a random range [min, max]. || `[0 -20 0]` (Array), `[0 -10 0]` (Array) |
| `end` | Enum | Defines the final animation state or offset vector for a particle's lifespan. || `[0 -450 0]` (Array), `[0 [ 40 120 ] 0]` (Array) |

</details>

### Object: `ParticleTornadoForce`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force` | Number | The force vector applied to particles. | 19 | `8` (Number), `5` (Number) |
| `axis` | Array | The 3D vector defining the central axis around which the tornado force rotates. || `[0 -0.5 0]` (Array), `[0 1 0]` (Array) |
| `point` | Array | The 3D position of the tornado's center point relative to the particle system. || `[1 1 1]` (Array), `[0 0 0]` (Array) |

</details>

### Object: `PeaceSymbol`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ARMOR_PEACESYMBOL_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `91` (Number) |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `neck` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ARMOR_PEACESYMBOL_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `[Hippie Twine]` (Array) |

</details>

### Object: `PeaceSymbolFacePaint`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ARMOR_PEACESYMBOLFACEPAINT_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `194` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ARMOR_PEACESYMBOLFACEPAINT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `rare` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Hippie` (Enum) |

</details>

### Object: `PermanentCharm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `Charmed` (Enum) |

</details>

### Object: `Pigeon`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdMed` (Enum) |

</details>

### Object: `PopAndSpawn`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 4 | `BoyShade` (Enum), `PlayerCat_ClotClone` (Enum) |
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 2 | `false` (Boolean) |
| `clone_referenced_catdata` | Boolean | If true, the spawned unit is a clone of the referenced cat data, including its stats and equipment. | 2 | `true` (Boolean) |
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 2 | `false` (Boolean) |

</details>

### Object: `Possessing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Possessing"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `GA_Telekinesis_Big` (Enum) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `primed` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Priming`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 4 | `{ ... }` (Object) |

</details>

### Object: `Psychic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[Telekinesis Suggestion MindControl MegaGrav PsyFlutter MagnetPull MindBlast PsychicChoke SkyShatter Supernova...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_PSYCHIC0" "TEAMNAME_ADJECTIVE_PSYCHIC1" "TEAMNAME_ADJECTIVE_PSYCHIC2" "TEAMNAME_ADJECTIVE_PSYCHIC3" "TEAMNAME_ADJECTIVE_PSYCHIC4" "TEAMNAME_ADJECTIVE_PSYCHIC5" "TEAMNAME_ADJECTIVE_PSYCHIC6" "TEAMNAME_ADJECTIVE_PSYCHIC7" "TEAMNAME_ADJECTIVE_PSYCHIC8" "TEAMNAME_ADJECTIVE_PSYCHIC9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicPsychicPull]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_PSYCHIC_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | An object defining innate passive abilities or effects that the class always possesses. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[int cha spd]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_PSYCHIC_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_PSYCHIC0" "TEAMNAME_NOUN_PSYCHIC1" "TEAMNAME_NOUN_PSYCHIC2" "TEAMNAME_NOUN_PSYCHIC3" "TEAMNAME_NOUN_PSYCHIC4" "TEAMNAME_NOUN_PSYCHIC5" "TEAMNAME_NOUN_PSYCHIC6" "TEAMNAME_NOUN_PSYCHIC7" "TEAMNAME_NOUN_PSYCHIC8" "TEAMNAME_NOUN_PSYCHIC9"]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[Flying SoulShatter Glow Blink FullPower RealityShatter MentalStorm Wither Flourish PsySmack...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[Ping Telekinesis Suggestion SkyShatter MindMeld Glare MindCrack FlashForward CumulativeBlast IncreaseGravity]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Pulp2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `2` (Number) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp3`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `3` (Number) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp4`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `4` (Number) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp5`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `5` (Number) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp6`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `6` (Number) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `1` (Number) |

</details>

### Object: `Pulp7`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `7` (Number) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` (String) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `1` (Number) |

</details>

### Object: `Rage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 16 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 12 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 12 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 8 | `"Rage"` (Enum) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"Rage"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `ChubsSpinRage` (Enum) |
| `move_speed_multiplier` | Number | A multiplier for the unit's base movement speed. | 2 | `2` (Number) |

</details>

### Object: `Rain`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `adventure_weather` | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain` (Enum) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_rain.ogg` (String) |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `5` (Number) |
| `skybox_frame` | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain` (Enum) |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). || `.5` (String) |
| `chain` | Boolean | Specifies the ability to chain into and execute. || `splash` (Enum) |
| `combo` | Array | A list of particle effect names that are spawned together in sequence. || `[RainB RainM RainF]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_RAIN_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `emit_amount` | Number | The number of particles emitted per burst. || `1` (Number) |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array | The initial direction vector for emitted particles. || `[0 -1 0]` (Array) |
| `emit_rate` | Number | The rate of particle emission per second. || `200` (Number) |
| `emit_spread` | Number | The angle spread for particle emission direction. || `0` (Number) |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. || `true` (Boolean) |
| `force` | Array | The force vector applied to particles. || `[0 -10 0]` (Array) |
| `hint_persistent_elements` | Array | A list of element types that remain persistent on the ground during this weather. || `[Water]` (Array) |
| `live_bounds` | Array | The bounds within which particles can exist. || `[-999 999 0 999 -999 999]` (Array) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `RainParticle` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_RAIN_NAME"` (String) |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. || `5` (Number) |
| `particles` | Array | A list of particle system identifiers used to render the weather effects. || `[Rain]` (Array) |
| `projection_matrix` | Enum | The projection matrix mode for particle rendering (e.g., 'default'). || `default` (Enum) |
| `render_mode` | Enum | The rendering mode for particles (e.g., 'default', 'separate'). || `separate` (Enum) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. || `{ ... }` (Object) |
| `simulation_space` | Enum | The coordinate space for particle simulation ('local' or 'global'). || `global` (Enum) |
| `size_start` | String | The starting size of particles. || `.5` (String) |
| `speed_scale` | String | A multiplier for particle speed. || `.1` (String) |
| `speed_start` | Number | The initial speed of particles. || `10` (Number) |

</details>

### Object: `RandomArmorPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `RandomBiggerArmorPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `RandomBiggerCatnipPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `RandomBiggerFoodPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `RandomCatnipPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `RandomFoodPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `RaptorEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_RaptorEgg` (Enum) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_RAPTOREGG_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `1` (Number) |
| `frame` | Integer | The sprite frame index to display. || `263` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_RAPTOREGG_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |

</details>

### Object: `Raven`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdMed` (Enum) |

</details>

### Object: `RavenFeather`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ARMOR_RAVENFEATHER_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `179` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `neck` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ARMOR_RAVENFEATHER_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `rare` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Feathered` (Enum) |

</details>

### Object: `Return`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `return` (Enum) |

</details>

### Object: `ReturnA`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `HangerBotReturn` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_close` (Enum) |

</details>

### Object: `RunFar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `PyrophinaVSRun` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `run_far` (Enum) |

</details>

### Object: `Scrap`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_SCRAP_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_SCRAP_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `shield` | Enum / Integer | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. || `[1 .5]` (Array), `3` (Number) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `PickupBase` (Enum) |

</details>

### Object: `Seagull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdMed` (Enum) |

</details>

### Object: `SewersUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `Shadow`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Number | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 4 | `.05*X` (String) |
| `class` | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. || `Thief` (Enum) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"PASSIVE_STEALTHED_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"PASSIVE_STEALTHED_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `teleport` (Enum) |

</details>

### Object: `ShowFakeDamage`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `999` (Number) |
| `style` | Array | Specifies the visual styles (e.g., crit) used for the fake damage display. || `[crit]` (Array) |

</details>

### Object: `Sitting`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Chair` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `DoNothing` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `DoNothing` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `SlotResult_Explode`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

</details>

### Object: `SlotResult_Jackpot_Coins`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. || `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spawn` (Enum) |

</details>

### Object: `SlotResult_Nothing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

</details>

### Object: `SlotResult_RandomPickup`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spawn` (Enum) |

</details>

### Object: `Small`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""` (String) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `GameteInflate` (Enum) |

</details>

### Object: `SmallAttic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `5` (Number) |
| `id` | Enum | The unique numerical identifier for this injury or status effect. | 2 | `Attic` (Enum) |
| `interstitial_bg_frame` | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 2 | `attic` (Enum) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. | 2 | `RoomBackgroundSmallAttic` (Enum) |
| `width` | Number | The number of tiles the room spans horizontally. | 2 | `18` (Number) |
| `built_in_collision` | Array | A list of collision geometry definitions for the room. || `[[ 6 6 6 6 6 6 6 6 6...]` (Array) |
| `extra_bound_planes` | Array | A list of additional boundary planes for the room. || `[{ p [ 0 0 ] n [ 1 -2...]` (Array) |
| [`reverb_empty`](House_and_Environment.md#object-reverb_empty) | Object | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ ... }` (Object) |
| [`reverb_full`](House_and_Environment.md#object-reverb_full) | Object | Defines the audio reverb settings for a full room, including preset and amount. || `{ ... }` (Object) |

</details>

### Object: `SmallBirdPool`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |

</details>

### Object: `SmallHolding`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Holding"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `SmallHoldingCat`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"HoldingCat"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `SmallHouse_Attic`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `prereq` | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `Default` (Enum) |
| `unlock_room` | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic` (Enum) |

</details>

### Object: `Snake`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `SpawningPhase`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `SpearRun`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `CaveManSpearRun` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 4 | `CaveManPickupSpear` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `util_minmove` (Enum) |

</details>

### Object: `Squirrel`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `SquirrelForm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `BasicMelee` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `ENEMY_DRAVENSQUIRRELFORM_DESC` (String) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. || `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. || `{ ... }` (Object) |
| `tags` | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). || `[shapeshift summon]` (Array) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spawn` (Enum) |

</details>

### Object: `Standing`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BungaSmash` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `DefaultMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Standing2`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BungaSmash` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 2 | `BungaJumpMove` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ ... }` (Object) |

</details>

### Object: `Start_Ceiling`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Stimulation`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_STIMULATION_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_STIMULATION_DESC"` (String) |

</details>

### Object: `Stop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `SuckMF`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `TormentorSuck` (Enum) |
| `decision_weights` | Enum | Specifies the named set of decision weight presets used by the AI. | 2 | `careless` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `keep_distance` (Enum) |

</details>

### Object: `SwordAndShield`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `DestroyerAttack` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `SwordAndShield_Primed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Holy"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `DestroyerAttack` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `TF_TargetAllies`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum | Specifies the named set of decision weight presets used by the AI. | 2 | `util_target_allies` (Enum) |

</details>

### Object: `TF_TargetEnemies`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `TwistingFlames` (Enum) |
| `decision_weights` | Enum | Specifies the named set of decision weight presets used by the AI. | 2 | `util_target_enemies` (Enum) |

</details>

### Object: `TVBotDie`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `155` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ENEMY_TVBOT_DIE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"ENEMY_TVBOT_DIE_DESC"` (String) |

</details>

### Object: `TVBotDumb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `155` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ENEMY_TVBOT_DUMB_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"ENEMY_TVBOT_DUMB_DESC"` (String) |

</details>

### Object: `TVBotObey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `155` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ENEMY_TVBOT_OBEY_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"ENEMY_TVBOT_OBEY_DESC"` (String) |

</details>

### Object: `TVBotStop`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `155` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ENEMY_TVBOT_STOP_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"ENEMY_TVBOT_STOP_DESC"` (String) |

</details>

### Object: `Tank`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[HeadButt ThrowShield ChewCud AssBlast Chew BatterUp BackBreaker Suplex Intimidate Toss...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_TANK0" "TEAMNAME_ADJECTIVE_TANK1" "TEAMNAME_ADJECTIVE_TANK2" "TEAMNAME_ADJECTIVE_TANK3" "TEAMNAME_ADJECTIVE_TANK4" "TEAMNAME_ADJECTIVE_TANK5" "TEAMNAME_ADJECTIVE_TANK6" "TEAMNAME_ADJECTIVE_TANK7" "TEAMNAME_ADJECTIVE_TANK8" "TEAMNAME_ADJECTIVE_TANK9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicTankMelee]` (Array) |
| `complicated_abilities` | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[TankRockSong FlipFlop Lunge PlantFeet IronHead Aftershock Demolish FullForce Thicken Spur]` (Array) |
| `complicated_passives` | Array | An array of passive ability names flagged as complicated. || `[Plow ChainKnockback Wrestlemaniac MyLeg SlowAndSteady ShovingMatch]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_TANK_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[con str spd]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_TANK_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_TANK0" "TEAMNAME_NOUN_TANK1" "TEAMNAME_NOUN_TANK2" "TEAMNAME_NOUN_TANK3" "TEAMNAME_NOUN_TANK4" "TEAMNAME_NOUN_TANK5" "TEAMNAME_NOUN_TANK6" "TEAMNAME_NOUN_TANK7" "TEAMNAME_NOUN_TANK8" "TEAMNAME_NOUN_TANK9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[Thorns HeavyHanded SlackOff Scabs ThunderThighs Plow PetRocks ToadStyle ChainKnockback ProtectiveAura...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[TankSwap Toss BellyFlop BatterUp Chew ThrowShield DrawAttention BodyGuard Earthquake Spur]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Tar`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `SpewerLobbed_Tar` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `TarFull`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `Full` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `SpewerSpit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `TempDexterityUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `DexterityUp` (Enum) |

</details>

### Object: `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

</details>

### Object: `TempSpeedUp`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `SpeedUp` (Enum) |

</details>

### Object: `TheEndUnlocked`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](Map_Generation_and_Routing.md#object-exit0) | Object | An object defining the properties of the first exit from this node. | 2 | `{ ... }` (Object) |

</details>

### Object: `Thief`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[MoveAgain Assassinate BoostBackstab PoisonGas PoisonNail WeakeningNail SharpNail CoinToss Shadow TimeWalk...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_THIEF0" "TEAMNAME_ADJECTIVE_THIEF1" "TEAMNAME_ADJECTIVE_THIEF2" "TEAMNAME_ADJECTIVE_THIEF3" "TEAMNAME_ADJECTIVE_THIEF4" "TEAMNAME_ADJECTIVE_THIEF5" "TEAMNAME_ADJECTIVE_THIEF6" "TEAMNAME_ADJECTIVE_THIEF7" "TEAMNAME_ADJECTIVE_THIEF8" "TEAMNAME_ADJECTIVE_THIEF9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[BasicStraightShot_Thief]` (Array) |
| `complicated_abilities` | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[QuickRoll Shadowshift SlingShade ThiefSwap Pierce TripleNails SkinDisguise PoisonDip]` (Array) |
| `complicated_passives` | Array | An array of passive ability names flagged as complicated. || `[BountyHunter AfterImage Agile FlipACoin]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_THIEF_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[spd dex lck]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_THIEF_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_THIEF0" "TEAMNAME_NOUN_THIEF1" "TEAMNAME_NOUN_THIEF2" "TEAMNAME_NOUN_THIEF3" "TEAMNAME_NOUN_THIEF4" "TEAMNAME_NOUN_THIEF5" "TEAMNAME_NOUN_THIEF6" "TEAMNAME_NOUN_THIEF7" "TEAMNAME_NOUN_THIEF8" "TEAMNAME_NOUN_THIEF9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[Backstabber GoldenClaws Shadow PoisonTips Burgle SwiftKiller DoubleThrow BountyHunter RazorClaws Looter...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[Shadow PoisonNail MoveAgain Backflip Distract Rebound Stalk Assassinate CutPurse SeverArtery]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Throb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobBubs`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobHost`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Host` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobNettle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `ThrobbingArteryDone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ ... }` (Object) |

</details>

### Object: `Thunderstorm`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Thunderstorm` (Enum) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_thunderstorm.ogg` (String), `amb_heavyrain.ogg` (String) |
| `lightning_fx` | Boolean | If true, lightning visual effects will occur during this thunderstorm. | 1 | `true` (Boolean) |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `5` (Number) |
| `skybox_frame` | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_thunderstorm` (Enum) |
| `combo` | Array | A list of particle effect names that are spawned together in sequence. || `[TRainB TRainM TRainF WindDust]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_THUNDERSTORM_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `hint_persistent_elements` | Array | A list of element types that remain persistent on the ground during this weather. || `[Water Wind]` (Array) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_THUNDERSTORM_NAME"` (String) |
| `particles` | Array | A list of particle system identifiers used to render the weather effects. || `[Thunderstorm]` (Array) |

</details>

### Object: `TieDyeBandana`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ARMOR_TIEDYEBANDANA_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `209` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `head` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ARMOR_TIEDYEBANDANA_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `rare` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Hippie` (Enum) |

</details>

### Object: `Tinkerer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](Cat_Classes.md#object-ability_groups) | Object | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ ... }` (Object) |
| `ability_pool` | Array | An array of ability names available in the class's ability pool. || `[Research Discharge Repair ShoddyJetpack SpawnDecoy SpringShoes AutoPilot Recycle BuildTurret RocketSkates...]` (Array) |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `["TEAMNAME_ADJECTIVE_TINKERER0" "TEAMNAME_ADJECTIVE_TINKERER1" "TEAMNAME_ADJECTIVE_TINKERER2" "TEAMNAME_ADJECTIVE_TINKERER3" "TEAMNAME_ADJECTIVE_TINKERER4" "TEAMNAME_ADJECTIVE_TINKERER5" "TEAMNAME_ADJECTIVE_TINKERER6" "TEAMNAME_ADJECTIVE_TINKERER7" "TEAMNAME_ADJECTIVE_TINKERER8" "TEAMNAME_ADJECTIVE_TINKERER9"...]` (Array) |
| `attack_pool` | Array | An array of attack ability names available in the class's attack pool. || `[TinkererCraft]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_TINKERER_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`innate_passives`](Cat_Classes.md#object-innate_passives) | Object | An object defining innate passive abilities or effects that the class always possesses. || `{ ... }` (Object) |
| `levelup_stats` | Array | An array of stat abbreviations that are randomly increased upon leveling up. || `[dex cha int]` (Array) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_TINKERER_NAME"` (String) |
| `nouns` | Array | A list of naming words used to generate animal names. || `["TEAMNAME_NOUN_TINKERER0" "TEAMNAME_NOUN_TINKERER1" "TEAMNAME_NOUN_TINKERER2" "TEAMNAME_NOUN_TINKERER3" "TEAMNAME_NOUN_TINKERER4" "TEAMNAME_NOUN_TINKERER5" "TEAMNAME_NOUN_TINKERER6" "TEAMNAME_NOUN_TINKERER7" "TEAMNAME_NOUN_TINKERER8" "TEAMNAME_NOUN_TINKERER9"...]` (Array) |
| `passive_pool` | Array | An array of passive ability names available in the class's passive pool. || `[VersionTwo WeaponProficiency LivingBattery FuzzyFeet ArmorSpecialist EMP MrMega EscapeSequence ItemProxy LightningRod...]` (Array) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `starter_abilities` | Array | An array of ability names that the class starts with at level 1. || `[Research ArmorUp ShoddyJetpack BuildTurret RocketSkates Discharge Craft Catbot Electrolyze InstantBarrier]` (Array) |
| [`stat_mods`](Cat_Classes.md#object-stat_mods) | Object | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ ... }` (Object) |

</details>

### Object: `Toad`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `Transformed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Turkey`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_Heal` (Enum) |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `15` (Number) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_TURKEY_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `7` (Number) |
| `frame` | Integer | The sprite frame index to display. || `244` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_TURKEY_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_rare` (Enum) |
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `BirdLarge` (Enum) |

</details>

### Object: `Turtle`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

</details>

### Object: `Turtled`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `Turtle` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `None` (Enum) |
| `move` | Enum | Specifies the name of the class's default movement ability. | 4 | `None` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 | `{ ... }` (Object) |

</details>

### Object: `TwoAlive`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 | `{ ... }` (Object) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 6 | `{ ... }` (Object) |

</details>

### Object: `TwoEyes`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Unflip`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `TeleportFlipUp` (Enum) |
| `move_for_ability` | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `Spin_Enemy` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_close_always_move` (Enum) |

</details>

### Object: `Unlit`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Unlit` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Unwashed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Unwashed` (Enum) |

</details>

### Object: `Up`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 | `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `"Up"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"OBJECT_TIREUP_DESC"` (String) |

</details>

### Object: `VolcanoAntennaAttached`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ ... }` (Object) |

</details>

### Object: `WallOfFleshDone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](Map_Generation_and_Routing.md#object-quest_event) | Object | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ ... }` (Object) |

</details>

### Object: `Washed`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `Washer`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BasicMelee` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CULTISTWASHER_NAME"` (String) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Cultist"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CULTISTWASHER_DESC"` (String) |

</details>

### Object: `Water`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `"Water"` (Enum) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |

</details>

### Object: `WeirdEgg`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_WEIRDEGG_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `73` (Number) |
| [`intro`](Events_and_Encounters.md#object-intro) | Object | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| [`main`](Events_and_Encounters.md#object-main) | Object | An object containing the primary prompt and options for an event. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_WEIRDEGG_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `uncommon` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Baby` (Enum) |

</details>

### Object: `WereMan`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"WereMan"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `WereManFurySwipes` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_WEREMAN_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_WEREMAN_DESC"` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `variant_of` | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. || `CavePerson` (Enum) |

</details>

### Object: `Wind`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 4 | `X` (Enum) |

</details>

### Object: `WishBone`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `cm_WishBone` (Enum) |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `true` (Boolean) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_WISHBONE_DESC"` (String) |
| `durability` | Array / Integer | The amount of durability consumed by this ability or required for its use. || `1` (Number) |
| `frame` | Integer | The sprite frame index to display. || `193` (Number) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_WISHBONE_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `consumable_very_rare` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Bone` (Enum) |

</details>

### Object: `Zealot`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"Zealot"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BBStabby` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_CULTISTZEALOT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_CULTISTZEALOT_DESC"` (String) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

</details>

### Object: `ZealotBomb`

<details>
<summary><b>Expand</b></summary>


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ ... }` (Object) |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `"BombZealot"` (Enum) |
| `attack` | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `BBExplode` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 2 | `"ENEMY_BOMBZEALOT_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 | `{ ... }` (Object) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. | 2 | `"ENEMY_BOMBZEALOT_DESC"` (String) |

</details>


---

## Auto-Discovered Objects


### Object: `AntlerSwipe`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `throw_attack` |

</details>

### Object: `AntlerSwipe2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `AntlerSwipe` |

</details>

### Object: `BasicDashAttackMove_NoKnockback`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack` |

</details>

### Object: `BerserkDash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack` |

</details>

### Object: `BirthSquirrel`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `summon` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spawn` |

</details>

### Object: `BlackShard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `wp_BlackShard` |
| `aux` | Number | An auxiliary integer value used for item properties, such as hunger value. | 1 | `1` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"ITEM_BLACKSHARD_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `164` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `weapon` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"ITEM_BLACKSHARD_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `quest` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `Obelisk` |

</details>

### Object: `Boulder`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`sound`](Characters_and_Bosses.md#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. | 1 ||

</details>

### Object: `CharmTrap`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `lobbed_attack` |

</details>

### Object: `Chitter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `DeathWormEat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `return` |
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Applies temporary status effects on the caster upon using the ability. | 1 ||

</details>

### Object: `EtherSoakedRag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `wp_EtherSoakedRag` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"ITEM_ETHERSOAKEDRAG_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `121` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `weapon` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"ITEM_ETHERSOAKEDRAG_NAME"` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `uncommon` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `Rag` |

</details>

### Object: `HardenSkin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `HardenSkin2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `HardenSkin` |

</details>

### Object: `HeadTumor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `HornCharge`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack` |

</details>

### Object: `JewelOfDrog`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"ARMOR_JEWELOFDROG_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `137` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `head` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"ARMOR_JEWELOFDROG_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `Gemstone` |

</details>

### Object: `MegaGuppy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `MockSong`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `MockSong2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `MonkeyThrow`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `throw_attack` |

</details>

### Object: `MonkeyThrow2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `MonkeyThrow` |

</details>

### Object: `MoonHandDrop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Grants temporary passive abilities to the caster for the duration of the ability. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `MoonHandThrow` |

</details>

### Object: `MoonHeadFlail`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `FlailBase` |

</details>

### Object: `Pounce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `jump_attack` |

</details>

### Object: `Prance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `Prance2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Prance` |

</details>

### Object: `RandomPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](Characters_and_Bosses.md#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||

</details>

### Object: `Scavenge`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `move` |

</details>

### Object: `Scavenge2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Applies temporary status effects on the caster upon using the ability. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Scavenge` |

</details>

### Object: `Synthesize`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `Synthesize2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Synthesize` |

</details>

### Object: `TaintedOffering`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `jump_attack` |

</details>

### Object: `TaintedOffering2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `TaintedOffering` |

</details>

### Object: `Tease`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `targeted_status` |

</details>

### Object: `Tease2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Tease` |

</details>

### Object: `TheDestroyer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `Thrash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `ThrowPoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `lobbed_attack` |

</details>

### Object: `TigerSwipes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `TigerSwipes2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `TigerSwipes` |

</details>

### Object: `Timber`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `trample_dash` |
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Applies temporary status effects on the caster upon using the ability. | 1 ||

</details>

### Object: `TinaFlail`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `FlailBase` |

</details>

### Object: `TinaFlailRage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `FlailBase` |

</details>

### Object: `ZombieCatFamiliar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `cm_RaptorEggSpawn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `summon` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spawn` |

</details>

### Object: `head_CrownOfHorns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `straightshot_attack` |

</details>

### Object: `megadino`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_MEGADINO_QUOTE_1` | String | The first boss quote spoken by Megadino. | 1 ||
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `MegaDino` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `BOSS_MEGADINO_NAME` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 ||

</details>

### Object: `moonhead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_MOONHEAD_QUOTE_1` | String | The first boss quote spoken by Moonhead. | 1 ||
| `BOSS_MOONHEAD_QUOTE_2` | String | The second boss quote spoken by Moonhead. | 1 ||
| `BOSS_MOONHEAD_QUOTE_3` | String | The third boss quote spoken by Moonhead. | 1 ||
| `BOSS_MOONHEAD_QUOTE_4` | String | The fourth boss quote spoken by Moonhead. | 1 ||
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `MoonHead` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `BOSS_MOONHEAD_NAME` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 ||

</details>
