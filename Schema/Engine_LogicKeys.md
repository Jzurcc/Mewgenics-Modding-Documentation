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
| [`Default`](./Miscellaneous.md#object-default) | Enum / Object  | The default form configuration for a unit, containing its standard stats and abilities. | 199 | `{ . . . }`<br>`release` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 114 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Druid`](./Engine_LogicKeys.md#object-druid) | Object  | Specifies the 'Druid' form within FormChanger, used for boss dialogue. | 80 | `{ . . . }` |
| [`Fighter`](./Engine_LogicKeys.md#object-fighter) | Object  | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 80 | `{ . . . }` |
| [`Monk`](./Engine_LogicKeys.md#object-monk) | Object  | Defines a list of quotes for the Monk class. | 66 | `{ . . . }` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 62 | `{ . . . }` |
| [`ChangeTile`](./Passives_and_Statuses.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 62 | `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 | `.1`<br>`.16666666`<br>`.3` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 47 | `{ . . . }` |
| `rock` | Variable | A variable used in logic contexts. | 46 ||
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 42 | `{ . . . }` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 38 | `{ . . . }` |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Specifies the name of the visual effect to play on the target tile. | 36 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| [`BounceObject`](./Miscellaneous.md#object-bounceobject) | Enum / Object  | Specifies the object or projectile to spawn and bounce from the target. | 35 | `{ . . . }`<br>`AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 29 | `1`<br>`2`<br>`[1 .01]` |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. | 28 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 27 | `{ . . . }` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 26 | `-1`<br>`-2`<br>`1` |
| [`EvolveAbilityFromPool`](./Miscellaneous.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 26 | `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| [`Normal`](./Miscellaneous.md#object-normal) | Integer / Object  | The normal form configuration, used as a baseline state for shape-shifting units. | 24 | `{ . . . }`<br>`0` |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 23 | `{ . . . }` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 21 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 21 | `1`<br>`2`<br>`3` |
| [`Conditional_Boss`](./Passives_and_Statuses.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 17 | `{ . . . }` |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 | `CHuskStruggle`<br>`CaveWomanEscape`<br>`LennyStruggle` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 15 | `{ . . . }`<br>`1` |
| `force_contact` | Boolean | If true, the consumed unit is forced into contact with the consumer. | 15 | `true` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 14 | `{ . . . }` |
| [`Conditional_NotBoss`](./Passives_and_Statuses.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 14 | `{ . . . }` |
| [`Conditional_Speculative`](./Miscellaneous.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 12 | `{ . . . }` |
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 12 | `true` |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 12 | `auto`<br>`true` |
| `do_not_pop_corpse` | Boolean | If true, the consumed unit's corpse is not popped upon consumption. | 11 | `true` |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 | `deferred`<br>`false`<br>`true` |
| [`Conditional_FormulaIsPositive`](./Miscellaneous.md#object-conditional_formulaispositive) | Object  | Defines effects that apply only if a given formula evaluates to a positive value. | 10 | `{ . . . }` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 10 | `-1`<br>`1`<br>`2` |
| `X` | Variable | A generic variable placeholder often used for coordinates or unknown values. | 10 ||
| [`Nuke`](./Miscellaneous.md#object-nuke) | Object  | Defines a nuke form with no attack or movement options. | 10 | `{ . . . }` |
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. | 9 | `0`<br>`1`<br>`10` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 8 | `{ . . . }` |
| [`formula`](./Enums.md#enum-formula) | Enum | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 8 | `X`<br>`X*10`<br>`X+1` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 8 | `{ . . . }` |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 8 | `1`<br>`2`<br>`[1 .1]` |
| `wet` | Boolean | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 | `false`<br>`true` |
| [`BlackShard`](./Engine_LogicKeys.md#object-blackshard) | Object  | Defines the BlackShard object, likely a collectible item or a specific entity in the game. | 8 | `{ . . . }` |
| [`Conditional_InForm`](./Miscellaneous.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 7 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Miscellaneous.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 7 | `{ . . . }` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 7 | `1`<br>`8` |
| [`ForceAttack`](./Miscellaneous.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. | 7 | `{ . . . }`<br>`1` |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 7 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 7 | `-1`<br>`1`<br>`2` |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. | 7 | `1`<br>`2`<br>`20` |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 6 | `{ . . . }` |
| [`Conditional_Object`](./Miscellaneous.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 6 | `{ . . . }` |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 6 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [`PopAndSpawn`](./Miscellaneous.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 6 | `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| `RandomInjury` | Integer | The number of random injuries applied. | 6 | `1` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 6 | `1`<br>`2`<br>`4` |
| [`TempSpeedUp`](./Enums.md#enum-tempspeedup) | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 6 | `10`<br>`4`<br>`X` |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 6 | `0`<br>`10`<br>`3` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 6 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`Conditional_IsSelf`](./Miscellaneous.md#object-conditional_isself) | Object  | An object containing effects that are only applied if the target is the source unit itself. | 5 | `{ . . . }` |
| [`DestroyEquipmentAndAttachParasite`](./Miscellaneous.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 5 | `{ . . . }` |
| `LavaTile` | Variable | Represents a tile of lava on the map, which deals damage to units standing on it. | 5 ||
| `MovementUp` | Integer | The amount of movement increase or decrease applied. | 5 | `-2`<br>`1`<br>`2` |
| `SafeDie` | Integer | The number of times the unit can survive a fatal hit. | 5 | `1` |
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array / Integer | The number of coins stolen from the target, or an array of `[number, probability]`. | 4 | `1`<br>`3`<br>`[1 .5]` |
| [`Conditional_Familiar`](./Miscellaneous.md#object-conditional_familiar) | Object  | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 | `{ . . . }` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 4 | `1`<br>`2` |
| `moonhand` | Variable | A variable representing the Moon Hand, likely a limb or entity type associated with lunar or cosmic themes. | 4 ||
| [`Reanimate`](./Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object  | The percentage chance to reanimate the target. | 4 | `{ . . . }`<br>`100%`<br>`33%`<br>`50%` |
| `RepairAll` | Integer | The amount of durability restored to all equipped items. | 4 | `1`<br>`10` |
| [`Thrash`](./Engine_LogicKeys.md#object-thrash) | Object  | Defines the Thrash ability, likely a close-range, multi-hit attack. | 4 | `{ . . . }` |
| [`ZombieCatFamiliar`](./Engine_LogicKeys.md#object-zombiecatfamiliar) | Object  | Defines the ZombieCat familiar, a companion entity that follows the unit in combat. | 4 | `{ . . . }` |
| [`BirthSquirrel`](./Engine_LogicKeys.md#object-birthsquirrel) | Object  | Defines the Birth Squirrel ability, which spawns a squirrel ally when used. | 4 | `{ . . . }` |
| `WaterTile_Current` | Variable | Represents a water tile with a current, pushing units in a specific direction. | 4 ||
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 3 | `1` |
| [`Conditional_AffectedByElement`](./Miscellaneous.md#object-conditional_affectedbyelement) | Object  | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 3 | `{ . . . }` |
| [`Conditional_LastHit`](./Miscellaneous.md#object-conditional_lasthit) | Object  | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 3 | `{ . . . }` |
| [`DoDamage`](./Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 3 | `{ . . . }` |
| `drop_on_self_death` | Boolean | If true, the consumed unit is dropped when the consumer dies. | 3 | `true` |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. | 3 | `1` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 3 | `1` |
| `PullSourceToTarget` | Integer | The amount of tiles the source is pulled towards the target after the attack. | 3 | `1` |
| [`ReviveNextRound`](./Miscellaneous.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. | 3 | `{ . . . }`<br>`2` |
| `WaterTile` | Variable | Represents a standard water tile on the map, which may slow or hinder movement. | 3 ||
| [`HeadTumor`](./Engine_LogicKeys.md#object-headtumor) | Object  | Defines the HeadTumor enemy, likely a swollen-headed unit with unique abilities. | 3 | `{ . . . }` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| [`Craft`](./Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 2 | `{ . . . }` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`Purge`](./Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object  | The number of status effects to purge from the target. | 2 | `{ . . . }`<br>`0`<br>`3` |
| [`SoulLink`](./Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object  | The number of soul link stacks applied. | 2 | `{ . . . }`<br>`1` |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer | The number of stealth stacks applied. | 2 | `1`<br>`2`<br>`[1 .1]` |
| [`PoisonLace`](./Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String  | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 | `{ . . . }`<br>`"X/3"`<br>`"X/5"`<br>`1` |
| [`poop`](./Miscellaneous.md#object-poop) | Object  | Defines a poop event or interaction, often part of a random encounter or response in dialogue. | 2 | `{ . . . }` |
| [`ApplyToRandomPartyMemberIfPossible`](./Miscellaneous.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 2 | `{ . . . }` |
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. | 2 | `100%`<br>`50%` |
| [`Conditional_BossOrBig`](./Miscellaneous.md#object-conditional_bossorbig) | Object  | An object containing effects that are only applied if the target is a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_Buddy`](./Miscellaneous.md#object-conditional_buddy) | Object  | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 | `{ . . . }` |
| [`Conditional_DestructibleCorpse`](./Miscellaneous.md#object-conditional_destructiblecorpse) | Object  | An object containing effects that are only applied if the corpse is destructible. | 2 | `{ . . . }` |
| [`Conditional_Displaceable`](./Miscellaneous.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 2 | `{ . . . }` |
| [`Conditional_NotAlly`](./Miscellaneous.md#object-conditional_notally) | Object  | An object containing effects that are only applied if the target is not an ally of the source. | 2 | `{ . . . }` |
| [`Conditional_NotBossOrBig`](./Miscellaneous.md#object-conditional_notbossorbig) | Object  | An object containing effects that are only applied if the target is not a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_NotShielded`](./Miscellaneous.md#object-conditional_notshielded) | Object  | An object containing effects that are only applied if the target does not have a shield active. | 2 | `{ . . . }` |
| `FireTile` | Variable | Represents a tile of fire on the map, which deals damage to units on it over time. | 2 ||
| [`GainDisorderFromPool`](./Miscellaneous.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 2 | `{ . . . }`<br>`all_disorders` |
| `gamewin` | Variable | A variable that triggers the end of the game, typically set to true when victory conditions are met. | 2 ||
| [`HornCharge`](./Engine_LogicKeys.md#object-horncharge) | Object  | Defines the Horn Charge ability, a dash attack that uses the character's horns to impale enemies. | 2 | `{ . . . }` |
| `humanoid` | Variable | A variable indicating whether the unit has a humanoid body type, affecting appearances and interactions. | 2 ||
| `ManaLeeches` | Integer | The number of mana leech stacks applied. | 2 | `1`<br>`2` |
| [`OffMap`](./Miscellaneous.md#object-offmap) | Object  | The form configuration applied when the unit is off the battlefield map. | 2 | `{ . . . }` |
| `OilTile` | Variable | Represents a tile covered in oil on the map, which can ignite and explode when exposed to fire. | 2 ||
| `Ostracized` | Integer | The number of stacks of Ostracized applied. | 2 | `1`<br>`2`<br>`4` |
| `PartyExplosion` | Variable | A variable that triggers a large explosive effect, often an event-based mechanic. | 2 ||
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 2 | `1`<br>`2` |
| [`Pilfer`](Events_and_Encounters.md#object-pilfer) | Object | Defines the Pilfer ability, which steals an item or resource from the target. | 2 | `{ . . . }` |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. | 2 | `1` |
| `PullSourceToKnockbackImmuneTarget` | Integer | The amount of pull force applied to the source toward a knockback-immune target. | 2 | `1` |
| [`Pulp2`](./Miscellaneous.md#object-pulp2) | Object  | Form state for the second stage of pulping, with no attacks or movement. | 2 | `{ . . . }` |
| [`RandomPickup`](./Engine_LogicKeys.md#object-randompickup) | Object  | Defines the RandomPickup object, likely a lootable item with random contents. | 2 | `{ . . . }` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. | 2 | `1`<br>`2` |
| `RepairWeaponCondition` | Integer | The amount of weapon condition restored. | 2 | `1` |
| `TallGrassTile` | Number | The percentage chance of this tile being tall grass, which provides cover or concealment. | 2 | `15`<br>`80` |
| `TempMovement` | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. | 2 | `1`<br>`20`<br>`mov` |
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. | 2 | `1` |
| `the_coven` | Variable | A variable representing a group of characters called The Coven, likely a faction or story element. | 2 ||
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 | `25%`<br>`50%` |
| [`ThrowPoop`](./Engine_LogicKeys.md#object-throwpoop) | Object  | Defines the Throw Poop ability, which hurls a projectile of feces at the target. | 2 | `{ . . . }` |
| [`AntlerSwipe`](./Engine_LogicKeys.md#object-antlerswipe) | Object  | Defines the Antler Swipe ability, a basic melee attack that uses the character's antlers. | 2 | `{ . . . }` |
| [`BerserkDash`](./Engine_LogicKeys.md#object-berserkdash) | Object  | Defines the Berserk Dash ability, a close-range charge that damages and knocks back enemies. | 2 | `{ . . . }` |
| `BlankTile` | Number | The number of blank tiles in a map segment, which are empty spaces with no special properties. | 2 | `5` |
| [`Boulder`](./Engine_LogicKeys.md#object-boulder) | Object  | Defines the Boulder object, a large rock that blocks movement and can be destroyed or pushed. | 2 | `{ . . . }` |
| [`CharmTrap`](./Engine_LogicKeys.md#object-charmtrap) | Object  | Defines the Charm Trap, a hazard that charms units entering its area, turning them against allies. | 2 | `{ . . . }` |
| `flip` | Variable | A variable that triggers a flip animation or reverses the state of something. | 2 ||
| [`HardenSkin`](./Engine_LogicKeys.md#object-hardenskin) | Object  | Defines the Harden Skin ability, which increases the unit's defense by making its skin tougher. | 2 | `{ . . . }` |
| [`MonkeyThrow`](./Engine_LogicKeys.md#object-monkeythrow) | Object  | Defines the Monkey Throw ability, which hurls a projectile in a manner similar to a monkey. | 2 | `{ . . . }` |
| [`MoonHandDrop`](./Engine_LogicKeys.md#object-moonhanddrop) | Object  | A variant of MoonHandThrow that includes bonus passives to enable a finisher. | 2 | `{ . . . }` |
| [`Pounce`](./Engine_LogicKeys.md#object-pounce) | Object  | Defines the Pounce ability, a jumping attack that lunges at the target. | 2 | `{ . . . }` |
| [`Prance`](./Engine_LogicKeys.md#object-prance) | Object  | Defines the Prance ability, a self-targeted buff that increases evasion or mobility. | 2 | `{ . . . }` |
| [`Scavenge`](./Engine_LogicKeys.md#object-scavenge) | Object  | Defines the Scavenge ability, a movement skill that allows the unit to search for items. | 2 | `{ . . . }` |
| [`SquirrelForm`](./Miscellaneous.md#object-squirrelform) | Object  | Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses. | 2 | `{ . . . }` |
| [`Synthesize`](./Engine_LogicKeys.md#object-synthesize) | Object  | Defines the Synthesize ability, a self-buff that creates or enhances items. | 2 | `{ . . . }` |
| [`TaintedOffering`](./Engine_LogicKeys.md#object-taintedoffering) | Object  | Defines the Tainted Offering ability, a harmful or corrupted gift bestowed upon a target. | 2 | `{ . . . }` |
| [`Tease`](./Engine_LogicKeys.md#object-tease) | Object  | Defines the Tease ability, a targeted status effect that provokes or irritates the target. | 2 | `{ . . . }` |
| [`TheDestroyer`](./Engine_LogicKeys.md#object-thedestroyer) | Object  | Defines The Destroyer object, likely a powerful boss or destructive entity. | 2 | `{ . . . }` |
| [`TigerSwipes`](./Engine_LogicKeys.md#object-tigerswipes) | Object  | Defines the Tiger Swipes ability, a rapid series of claw attacks. | 2 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`Rain`](./Miscellaneous.md#object-rain) | Object  | Defines the rain weather effect with associated particle, sound, and rendering settings. | 1 | `{ . . . }` |
| [`megadino`](#object-megadino) | Variable | A variable representing a Mega Dinosaur, likely a large, powerful enemy or form. | 1 ||
| [`moonhead`](#object-moonhead) | Variable | A variable representing the Moon Head, likely a head type or entity associated with lunar themes. | 1 ||
| `alien` | Variable | A variable indicating the unit is an alien, affecting its type and interactions. | 1 ||
| [`AllyInfested`](./Miscellaneous.md#object-allyinfested) | Object  | Defines the AllyInfested object, which spawns an infested ally under the player's control. | 1 | `{ . . . }` |
| `angeljunk` | Variable | A variable representing angel junk, likely a cosmetic or mechanical part of an angelic character. | 1 ||
| [`AntlerSwipe2`](./Engine_LogicKeys.md#object-antlerswipe2) | Object  | A variant of Antler Swipe with a different description and potentially different parameters. | 1 | `{ . . . }` |
| [`BasicDashAttackMove_NoKnockback`](./Engine_LogicKeys.md#object-basicdashattackmove_noknockback) | Object  | Defines a basic dash attack that deals damage without knocking back the target. | 1 | `{ . . . }` |
| `berserkIdle` | Variable | A variable that sets the unit's idle animation to a berserk state. | 1 ||
| `bonusbird` | Variable | A variable representing a bonus bird, likely an additional familiar or entity. | 1 ||
| [`Boris`](./Miscellaneous.md#object-boris) | Enum / Object  | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 1 | `{ . . . }`<br>`MegaGuppy_TransformBoris` |
| `BrambleTile` | Variable | Represents a tile of brambles on the map, which damages units crossing it. | 1 ||
| `chapter_corpse_medium` | Variable | A variable representing a medium-sized corpse prop used in chapter environments. | 1 ||
| [`Chitter`](./Engine_LogicKeys.md#object-chitter) | Object  | Defines the Chitter ability, a spell that deals magical damage or applies a status effect. | 1 | `{ . . . }` |
| [`cm_RaptorEggSpawn`](./Engine_LogicKeys.md#object-cm_raptoreggspawn) | Object  | Defines the template and meta properties for spawning a raptor egg entity. | 1 | `{ . . . }` |
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 | `{ . . . }` |
| [`Conditional_ActiveWeather_Any`](./Miscellaneous.md#object-conditional_activeweather_any) | Object  | An object containing effects that execute only if any of the specified weather types are active. | 1 | `{ . . . }` |
| [`Conditional_Backstab`](./Miscellaneous.md#object-conditional_backstab) | Object  | An object containing effects that execute only if the attack lands on the target's back. | 1 | `{ . . . }` |
| [`Conditional_CanBeHealed`](./Miscellaneous.md#object-conditional_canbehealed) | Object  | An object containing effects that execute only if the target can be healed. | 1 | `{ . . . }` |
| [`Conditional_DebuffRoll`](./Miscellaneous.md#object-conditional_debuffroll) | Object  | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`Conditional_FinishedSpawning`](./Miscellaneous.md#object-conditional_finishedspawning) | Object  | Contains an inner effect block that only executes if the target has finished its spawning animation. | 1 | `{ . . . }` |
| [`Conditional_HasCleansableDebuffs`](./Miscellaneous.md#object-conditional_hascleansabledebuffs) | Object  | An object containing effects that execute only if the unit has cleansable debuffs. | 1 | `{ . . . }` |
| [`Conditional_HasKnockback`](./Miscellaneous.md#object-conditional_hasknockback) | Object  | An object containing actions that execute if the incoming damage has knockback. | 1 | `{ . . . }` |
| [`Conditional_IsPhysicalAttack`](./Miscellaneous.md#object-conditional_isphysicalattack) | Object  | A conditional block that executes its child actions only if the triggering event is a physical attack. | 1 | `{ . . . }` |
| [`Conditional_IsTrample`](./Miscellaneous.md#object-conditional_istrample) | Object  | An object containing effects that execute only if the ability is a trample attack. | 1 | `{ . . . }` |
| [`Conditional_LivingPlayerCat`](./Miscellaneous.md#object-conditional_livingplayercat) | Object  | An object containing effects that execute only if the source is a living player-owned cat. | 1 | `{ . . . }` |
| [`Conditional_NotBig`](./Miscellaneous.md#object-conditional_notbig) | Object  | An object containing effects that execute only if the target is not a 'big' unit. | 1 | `{ . . . }` |
| [`Conditional_SourceAbilityHasTag`](./Miscellaneous.md#object-conditional_sourceabilityhastag) | Object  | An object containing effects that execute only if the source ability has the specified tag. | 1 | `{ . . . }` |
| [`Conditional_SourceHasStatus`](./Miscellaneous.md#object-conditional_sourcehasstatus) | Object  | An object containing effects that execute only if the source unit has the specified status. | 1 | `{ . . . }` |
| `container` | Variable | A variable representing a generic container or inventory slot for items. | 1 ||
| [`DeathWormEat`](./Engine_LogicKeys.md#object-deathwormeat) | Object  | Defines the eat ability for Death Worm, using the return template and specifying its name and movement flag. | 1 | `{ . . . }` |
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 1 | `true` |
| `DirtTile` | Variable | A variable representing a dirt tile type on the grid. | 1 ||
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Specifies the ability used to drop the consumed body. | 1 | `MoonHandDrop` |
| [`DualSword`](./Miscellaneous.md#object-dualsword) | Object  | Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack. | 1 | `{ . . . }` |
| [`DybbukPossessed`](./Miscellaneous.md#object-dybbukpossessed) | Object  | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 1 | `{ . . . }` |
| `EggSackTrap` | Variable | A variable representing an egg sack trap entity. | 1 ||
| [`EtherSoakedRag`](./Engine_LogicKeys.md#object-ethersoakedrag) | Object  | An object defining the properties of the Ether Soaked Rag item. | 1 | `{ . . . }` |
| [`Explosive`](./Miscellaneous.md#object-explosive) | Enum / Object  | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 1 | `{ . . . }`<br>`MegaGuppy_TransformExplosive` |
| `GenericBuff` | Integer | A generic buff value applied to the unit. | 1 | `100`<br>`5` |
| `ghost` | Variable | A variable representing a ghost unit or entity. | 1 ||
| `GlassTile` | Variable | A variable representing a glass tile type on the grid. | 1 ||
| `god` | Variable | A variable representing a god entity or modifier. | 1 ||
| [`Grown`](./Miscellaneous.md#object-grown) | Object  | Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold. | 1 | `{ . . . }` |
| `grown_hitler_clone` | Variable | A variable representing a fully grown Hitler clone unit. | 1 ||
| [`HalfDead`](./Miscellaneous.md#object-halfdead) | Object  | Defines the half-dead form with reduced movement and a dash attack. | 1 | `{ . . . }` |
| [`HardenSkin2`](./Engine_LogicKeys.md#object-hardenskin2) | Object  | An object defining the upgraded Harden Skin ability. | 1 | `{ . . . }` |
| [`head_CrownOfHorns`](./Engine_LogicKeys.md#object-head_crownofhorns) | Object  | A logic key that applies the Crown of Horns head item effect, causing retaliatory damage when the unit is hit. | 1 | `{ . . . }` |
| `hitler_clone` | Variable | A variable representing a Hitler clone unit. | 1 ||
| `hitler_clone_fetus` | Variable | A variable representing the fetus stage of a Hitler clone. | 1 ||
| [`Infested`](./Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object  | The number of stacks of Infested applied. | 1 | `{ . . . }`<br>`1` |
| `JesterMinusColorless` | Variable | A variable representing a Jester variant without colorless mechanics. | 1 ||
| [`JewelOfDrog`](./Engine_LogicKeys.md#object-jewelofdrog) | Object  | An object defining the properties of the Jewel of Drog item. | 1 | `{ . . . }` |
| `kill_on_consume` | Boolean | If true, the consumed unit is killed immediately upon consumption. | 1 | `true` |
| [`MegaGuppy`](./Engine_LogicKeys.md#object-megaguppy) | Object  | An object defining the properties of the Mega Guppy transformation or item. | 1 | `{ . . . }` |
| [`MockSong`](./Engine_LogicKeys.md#object-mocksong) | Object  | Defines the Mock Song spell, the basic attack for mockingbird form, including its name and description. | 1 | `{ . . . }` |
| [`MockSong2`](./Engine_LogicKeys.md#object-mocksong2) | Object  | Defines the upgraded Mock Song spell variant for mockingbird form. | 1 | `{ . . . }` |
| [`MonkeyThrow2`](./Engine_LogicKeys.md#object-monkeythrow2) | Object  | An object defining the upgraded Monkey Throw ability. | 1 | `{ . . . }` |
| [`MoonHeadFlail`](./Engine_LogicKeys.md#object-moonheadflail) | Object  | An object defining the Moon Head Flail ability or item. | 1 | `{ . . . }` |
| `NoDeathrattle` | Variable | A variable flag that prevents the unit from triggering deathrattle effects. | 1 ||
| `OverrideChainKnockbackDamage` | Equation | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 1 | `0`<br>`3+bonus_melee_ability_damage` |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 1 | `1`<br>`2` |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 1 | `1`<br>`2` |
| [`Prance2`](./Engine_LogicKeys.md#object-prance2) | Object  | Defines an upgraded variant of the Prance ability, using a different description. | 1 | `{ . . . }` |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. | 1 | `1` |
| `rotate_right` | Variable | A variable representing a right rotation action or state. | 1 ||
| [`Scavenge2`](./Engine_LogicKeys.md#object-scavenge2) | Object  | Defines an upgraded variant of the Scavenge ability, using a different description. | 1 | `{ . . . }` |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. | 1 | `1`<br>`2` |
| [`Small`](./Miscellaneous.md#object-small) | Object  | Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation. | 1 | `{ . . . }` |
| [`SmallHolding`](./Miscellaneous.md#object-smallholding) | Object  | Form state when the unit is holding a small object, triggering a form change while consuming. | 1 | `{ . . . }` |
| [`SmallHoldingCat`](./Miscellaneous.md#object-smallholdingcat) | Object  | Form state when the unit is holding a cat, triggering a form change while consuming. | 1 | `{ . . . }` |
| `spear` | Variable | A variable representing a spear weapon type. | 1 ||
| `SplashDamage` | Integer | The radius (in tiles) for splash damage applied to adjacent targets. | 1 | `1`<br>`2` |
| [`Standing`](./Miscellaneous.md#object-standing) | Object  | Form state where the unit is standing, with default movement and attack. | 1 | `{ . . . }` |
| [`Synthesize2`](./Engine_LogicKeys.md#object-synthesize2) | Object  | Defines an upgraded variant of the Synthesize ability, using a different description. | 1 | `{ . . . }` |
| [`TaintedOffering2`](./Engine_LogicKeys.md#object-taintedoffering2) | Object  | An object defining the upgraded Tainted Offering ability. | 1 | `{ . . . }` |
| `TallFlowerTile` | Variable | A variable representing a tall flower tile type on the grid. | 1 ||
| [`Tease2`](./Engine_LogicKeys.md#object-tease2) | Object  | Defines an upgraded variant of the Tease ability, using a different description. | 1 | `{ . . . }` |
| `the_nuke_bearer` | Variable | A variable representing the entity that carries the nuke. | 1 ||
| `themotherspike` | Variable | A variable representing the Mother Spike entity. | 1 ||
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 | `item_aux` |
| [`TigerSwipes2`](./Engine_LogicKeys.md#object-tigerswipes2) | Object  | An object defining the upgraded Tiger Swipes ability. | 1 | `{ . . . }` |
| [`Timber`](./Engine_LogicKeys.md#object-timber) | Object  | Defines the Timber trample dash ability, an alt basic attack for Tree Form. | 1 | `{ . . . }` |
| [`TinaFlail`](./Engine_LogicKeys.md#object-tinaflail) | Object  | An object defining the Tina Flail ability or item. | 1 | `{ . . . }` |
| [`TinaFlailRage`](./Engine_LogicKeys.md#object-tinaflailrage) | Object  | An object defining the rage variant of the Tina Flail ability. | 1 | `{ . . . }` |
| [`TransformWeapon`](./Miscellaneous.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. | 1 | `{ . . . }` |
| `weapon_throw` | Variable | A variable representing a weapon throw action or projectile. | 1 ||
| [`weather`](./Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 1 | `[FlySwarm FireflySwarm ButterflySwarm]` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. || `passives`<br>`class`<br>`tag` |
| `contact_requires_adjacency` | Boolean | If false, contact effects are not restricted to adjacent tiles, allowing contact to trigger at range. | 0 | `false` |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 0 | `.1`<br>`.16666666`<br>`.3` |
| `two_way_contact` | Boolean | If true, contact effects apply to both the attacker and the target when the damage instance hits. | 0 | `true` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 0 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

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
| [`GainDisorderFromPool`](./Miscellaneous.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. || `{ . . . }`<br>`all_disorders` |

</details>


---


#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 59

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `1`<br>`2`<br>`3` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| `AddWeaponAux` | Equation | The amount or expression to add to the source's weapon auxiliary stat. || `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `Charge` | Equation | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. || `BoneClub`<br>`Kidney` |
| [`EvolveAbilityFromPool`](./Miscellaneous.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. || `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| [`FindItem`](./Enums.md#enum-finditem) | Enum  | The name of the specific item to find and add to the source's inventory. || `BoneClub`<br>`Molars`<br>`Pearl` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. || `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. || `1`<br>`2` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. || `{ . . . }` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`weather`](./Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 0 | `[FlySwarm FireflySwarm ButterflySwarm]` |

</details>


---


#### `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Miscellaneous.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |

</details>


---


#### `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Speculative`](./Miscellaneous.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 | `{ . . . }` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 1 | `Electric`<br>`Fire`<br>`Gravity` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `1`<br>`2`<br>`3` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 8 | `1`<br>`2`<br>`3` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 1 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Miscellaneous.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `-1`<br>`1`<br>`2` |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. || `10`<br>`4`<br>`X` |

</details>


---


#### `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |

</details>


---


#### `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 8 | `.1`<br>`.16666666`<br>`.3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `25`<br>`50`<br>`999` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


---


#### `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 6 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. || `1`<br>`8` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](./Miscellaneous.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. || `1` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `1` |
| `RandomMutation` | Integer | The number of random mutations to apply. || `1`<br>`3` |
| [`SafeDoomed`](./Enums.md#enum-safedoomed) | Enum / Integer  | The number of SafeDoomed stacks applied, or 'level' to scale with character level. || `1`<br>`2`<br>`level` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |

</details>


---


#### `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 1 | `.1`<br>`.16666666`<br>`.3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `LaunchOffScreen` | String | A formula string that determines the knockback force to launch the unit off-screen. || `10+bonus_melee_ability_damage` |

</details>


---


#### `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_NotBoss`](./Passives_and_Statuses.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 3 | `{ . . . }` |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#object-conditional_partymember) | Object  | A conditional block that executes its child actions only if the target is a party member. | 2 | `{ . . . }` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_FinishedSpawning`](./Miscellaneous.md#object-conditional_finishedspawning) | Object  | Contains an inner effect block that only executes if the target has finished its spawning animation. | 1 | `{ . . . }` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. || `1` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. || `1`<br>`2`<br>`3` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. || `1` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`3`<br>`5` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `1` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `-1`<br>`1`<br>`2` |

</details>


---


#### `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |

</details>


---


#### `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `Charge` | Equation | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `1`<br>`[1 .10]`<br>`[1 .25]` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


#### `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`formula`](./Enums.md#enum-formula) | Enum | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 8 | `X`<br>`X*10`<br>`X+1` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. || `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. || `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. || `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `RandomMutation` | Integer | The number of random mutations to apply. || `1`<br>`3` |

</details>


---


#### `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 20 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`5` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |

</details>


---


#### `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 47

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 981 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`Conditional_NotBoss`](./Passives_and_Statuses.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 6 | `{ . . . }` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Conditional_Boss`](./Passives_and_Statuses.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 4 | `{ . . . }` |
| [`Conditional_InForm`](./Miscellaneous.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. || `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. || `{ . . . }`<br>`1`<br>`6` |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. || `5` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. || `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `25`<br>`50`<br>`999` |
| [`PopAndSpawn`](./Miscellaneous.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. || `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. || `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


#### `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 5 | `0`<br>`10`<br>`3` |
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 | `25%`<br>`50%` |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 1 | `{ . . . }` |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 | `item_aux` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. || `{ . . . }`<br>`1`<br>`6` |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. || `1`<br>`10`<br>`2` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `25`<br>`50`<br>`999` |

</details>


---


#### `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `1`<br>`10`<br>`100` |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 7 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. || `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


#### `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |

</details>


---


#### `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 1 | `0`<br>`10`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. || `1`<br>`99` |

</details>


---


#### `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 2 | `{ . . . }` |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. || `1`<br>`2`<br>`3` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `1` |

</details>


---


#### `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. || `1`<br>`10`<br>`2` |

</details>


---


#### `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `1`<br>`6`<br>`99` |

</details>


---


#### `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. || `1`<br>`2` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `1`<br>`3` |

</details>


---


#### `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](./Miscellaneous.md#object-conditional_isself) | Object  | An object containing effects that are only applied if the target is the source unit itself. | 3 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 0 | `1`<br>`2`<br>`3` |
| [`ApplyPassives`](./Miscellaneous.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 0 | `{ . . . }` |

</details>


---


#### `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `Charge` | Equation | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. || `1`<br>`2` |

</details>


---


#### `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 4 | `.1`<br>`.16666666`<br>`.3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `{ . . . }`<br>`1` |
| [`SetItemAux`](./Miscellaneous.md#object-setitemaux) | Object  | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. || `{ . . . }` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 981 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| [`ScatterCoins`](./Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. || `{ . . . }` |

</details>


---


#### `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 981 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |

</details>


---


#### `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. || `1`<br>`10`<br>`2` |

</details>


---


#### `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 85

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `1`<br>`10`<br>`100` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 2 | `{ . . . }` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [`Conditional_Displaceable`](./Miscellaneous.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 | `{ . . . }` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [`Conditional_HasKnockback`](./Miscellaneous.md#object-conditional_hasknockback) | Object  | An object containing actions that execute if the incoming damage has knockback. | 1 | `{ . . . }` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |
| [`Conditional_Object`](./Miscellaneous.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| [`Conditional_Speculative`](./Miscellaneous.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`AllyInfested`](./Miscellaneous.md#object-allyinfested) | Array / Float / Object  | Defines the AllyInfested object, which spawns an infested ally under the player's control. || `{ . . . }` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `{ . . . }`<br>`1` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| [`DybbukPossessed`](./Miscellaneous.md#object-dybbukpossessed) | Object  | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. || `{ . . . }` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. || `{ . . . }` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. || `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `25`<br>`50`<br>`999` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`3`<br>`5` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. || `1`<br>`9999` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. || `1` |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| [`ScatterCoins`](./Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. || `{ . . . }` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. || `10`<br>`4`<br>`X` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |

</details>


---


#### `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2166

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 38 | `{ . . . }` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `1`<br>`10`<br>`100` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `1`<br>`2`<br>`3` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 35 | `{ . . . }` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 25 | `{ . . . }` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 14 | `{ . . . }` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 | `1`<br>`3`<br>`4` |
| [`Conditional_Boss`](./Passives_and_Statuses.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 13 | `{ . . . }` |
| [`Conditional_FormulaIsPositive`](./Miscellaneous.md#object-conditional_formulaispositive) | Object  | Defines effects that apply only if a given formula evaluates to a positive value. | 10 | `{ . . . }` |
| [`Conditional_Speculative`](./Miscellaneous.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 10 | `{ . . . }` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 6 | `{ . . . }` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `1`<br>`2`<br>`3` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `1`<br>`2` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 5 | `{ . . . }` |
| [`Conditional_InForm`](./Miscellaneous.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 5 | `{ . . . }` |
| [`Conditional_NotBoss`](./Passives_and_Statuses.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 5 | `{ . . . }` |
| [`Conditional_Object`](./Miscellaneous.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 5 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Miscellaneous.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 5 | `{ . . . }` |
| [`Conditional_Familiar`](./Miscellaneous.md#object-conditional_familiar) | Object  | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 | `{ . . . }` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`Reanimate`](./Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object  | The percentage chance to reanimate the target. | 4 | `{ . . . }`<br>`100%`<br>`33%`<br>`50%` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 4 | `.4`<br>`.6`<br>`.7` |
| [`Conditional_AffectedByElement`](./Miscellaneous.md#object-conditional_affectedbyelement) | Object  | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 3 | `{ . . . }` |
| [`Conditional_LastHit`](./Miscellaneous.md#object-conditional_lasthit) | Object  | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 | `{ . . . }` |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | `1` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 2 | `1` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 2 | `{ . . . }` |
| [`Conditional_BossOrBig`](./Miscellaneous.md#object-conditional_bossorbig) | Object  | An object containing effects that are only applied if the target is a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_Buddy`](./Miscellaneous.md#object-conditional_buddy) | Object  | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 | `{ . . . }` |
| [`Conditional_DestructibleCorpse`](./Miscellaneous.md#object-conditional_destructiblecorpse) | Object  | An object containing effects that are only applied if the corpse is destructible. | 2 | `{ . . . }` |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 | `{ . . . }` |
| [`Conditional_IsSelf`](./Miscellaneous.md#object-conditional_isself) | Object  | An object containing effects that are only applied if the target is the source unit itself. | 2 | `{ . . . }` |
| [`Conditional_NotAlly`](./Miscellaneous.md#object-conditional_notally) | Object  | An object containing effects that are only applied if the target is not an ally of the source. | 2 | `{ . . . }` |
| [`Conditional_NotBossOrBig`](./Miscellaneous.md#object-conditional_notbossorbig) | Object  | An object containing effects that are only applied if the target is not a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_NotShielded`](./Miscellaneous.md#object-conditional_notshielded) | Object  | An object containing effects that are only applied if the target does not have a shield active. | 2 | `{ . . . }` |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 2 | `{ . . . }` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 2 | `{ . . . }` |
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer  | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| [`PoisonLace`](./Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String  | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 | `{ . . . }`<br>`"X/3"`<br>`"X/5"`<br>`1` |
| [`Purge`](./Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object  | The number of status effects to purge from the target. | 2 | `{ . . . }`<br>`0`<br>`3` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Reflect`](./Engine_StatusAndPassiveKeys.md#object-reflect) | Integer / Object  | The amount of reflect stacks applied. | 2 | `{ . . . }`<br>`1`<br>`5` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [`SoulLink`](./Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object  | The number of soul link stacks applied. | 2 | `{ . . . }`<br>`1` |
| [`Infested`](./Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object  | The number of stacks of Infested applied. | 1 | `{ . . . }`<br>`1` |
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 | `{ . . . }` |
| [`Conditional_ActiveWeather_Any`](./Miscellaneous.md#object-conditional_activeweather_any) | Object  | An object containing effects that execute only if any of the specified weather types are active. | 1 | `{ . . . }` |
| [`Conditional_Backstab`](./Miscellaneous.md#object-conditional_backstab) | Object  | An object containing effects that execute only if the attack lands on the target's back. | 1 | `{ . . . }` |
| [`Conditional_CanBeHealed`](./Miscellaneous.md#object-conditional_canbehealed) | Object  | An object containing effects that execute only if the target can be healed. | 1 | `{ . . . }` |
| [`Conditional_DebuffRoll`](./Miscellaneous.md#object-conditional_debuffroll) | Object  | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`Conditional_Displaceable`](./Miscellaneous.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 | `{ . . . }` |
| [`Conditional_HasCleansableDebuffs`](./Miscellaneous.md#object-conditional_hascleansabledebuffs) | Object  | An object containing effects that execute only if the unit has cleansable debuffs. | 1 | `{ . . . }` |
| [`Conditional_IsTrample`](./Miscellaneous.md#object-conditional_istrample) | Object  | An object containing effects that execute only if the ability is a trample attack. | 1 | `{ . . . }` |
| [`Conditional_LivingPlayerCat`](./Miscellaneous.md#object-conditional_livingplayercat) | Object  | An object containing effects that execute only if the source is a living player-owned cat. | 1 | `{ . . . }` |
| [`Conditional_NotBig`](./Miscellaneous.md#object-conditional_notbig) | Object  | An object containing effects that execute only if the target is not a 'big' unit. | 1 | `{ . . . }` |
| [`Conditional_RandomChance`](./Miscellaneous.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`Conditional_SourceAbilityHasTag`](./Miscellaneous.md#object-conditional_sourceabilityhastag) | Object  | An object containing effects that execute only if the source ability has the specified tag. | 1 | `{ . . . }` |
| [`Conditional_SourceHasStatus`](./Miscellaneous.md#object-conditional_sourcehasstatus) | Object  | An object containing effects that execute only if the source unit has the specified status. | 1 | `{ . . . }` |
| [`Rain`](./Miscellaneous.md#object-rain) | Object  | Defines the rain weather effect with associated particle, sound, and rendering settings. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. || `Default`<br>`FormChange`<br>`Druid` |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. || `1` |
| [`BounceObject`](./Miscellaneous.md#object-bounceobject) | Enum / Object  | Specifies the object or projectile to spawn and bounce from the target. || `{ . . . }`<br>`AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array / Integer  | The number of coins stolen from the target, or an array of `[number, probability]`. || `1`<br>`3`<br>`[1 .5]` |
| [`ChangeTile`](./Passives_and_Statuses.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). || `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. || `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| `Charge` | Equation | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `-1`<br>`-2`<br>`1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `{ . . . }`<br>`1` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. || `{ . . . }` |
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). || `1` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. || `-1`<br>`1`<br>`2` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `1`<br>`2`<br>`3` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. || `1`<br>`2`<br>`3` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. || `1`<br>`8` |
| [`EvolveAbilityFromPool`](./Miscellaneous.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. || `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. || `1` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. || `1` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum  | Specifies the item pool from which an extra item is granted at the end of combat. || `combat_reward_easy`<br>`pills` |
| [`ForceAttack`](./Miscellaneous.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. || `{ . . . }`<br>`1` |
| `ForceMoveAway` | Integer | The distance to force the target away from the source. || `1` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. || `1`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. || `{ . . . }` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. || `1` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. || `1` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. || `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `25`<br>`50`<br>`999` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. || `1`<br>`10`<br>`2` |
| [`KnockOutCoin`](./Miscellaneous.md#object-knockoutcoin) | Integer / Object  | The number of coins knocked out, with an optional probability or an object with stacks and chance. || `{ . . . }`<br>`1`<br>`[1 .5]` |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. || `1`<br>`3` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. || `1`<br>`2` |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. || `-2`<br>`1`<br>`2` |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. || `1` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. || `1`<br>`2`<br>`4` |
| `OverrideChainKnockbackDamage` | String | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). || `0`<br>`3+bonus_melee_ability_damage` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. || `1`<br>`9999` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. || `-1`<br>`-2`<br>`1` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. || `1`<br>`2` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. || `-1`<br>`1`<br>`2` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. || `-1`<br>`1`<br>`2` |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. || `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`PopAndSpawn`](./Miscellaneous.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. || `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. || `1` |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. || `1` |
| `RandomInjury` | Integer | The number of random injuries applied. || `1` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. || `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). || `-1`<br>`-2`<br>`-3` |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. || `1` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. || `1`<br>`2` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `1`<br>`6`<br>`99` |
| [`ReviveNextRound`](./Miscellaneous.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. || `{ . . . }`<br>`2` |
| [`Rot`](./Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `-999999`<br>`1`<br>`2` |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum  | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. || `happy`<br>`insane`<br>`sad` |
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`3` |
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `1`<br>`[1 .5]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `1`<br>`3` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. || `1`<br>`2`<br>`4` |
| [`StatusAllCharactersOnSpawn`](./Passives_and_Statuses.md#object-statusallcharactersonspawn) | Object  | Defines status effects applied to all characters when they spawn into the battlefield. || `{ . . . }` |
| [`StatusGroup`](./Passives_and_Statuses.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. || `{ . . . }` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Tangled`](./Miscellaneous.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. || `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. || `1` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `-1`<br>`1`<br>`2` |
| `TempDexterityUp` | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. || `2`<br>`X` |
| `TempMovement` | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. || `1`<br>`20`<br>`mov` |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. || `1`<br>`2`<br>`20` |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. || `10`<br>`4`<br>`X` |
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. || `1` |
| `TempStrengthUp` | Enum | The number of stacks of temporary Strength Up applied to the unit. || `1`<br>`2`<br>`X` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. || `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |

</details>
## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `Alert`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `AllAlive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |

</details>


### Object: `AllyInfested`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum  | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 | `allies`<br>`auto`<br>`birds` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |

</details>


### Object: `Angry`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Antidote`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Appeal`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `ApplyPassives`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 4 | `1` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 4 | `-.18`<br>`.25`<br>`.35` |

</details>


### Object: `Attacker`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |

</details>


### Object: `Attraction`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_reference_applier` | String | A localization key for the name displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| `tooltip_reference_applier` | String | A localization key for the tooltip description displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |

</details>


### Object: `BagOfSeeds`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Basement0`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `Basement1`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `Basement2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `Basement3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `Basement4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `BasementUpgrade`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade5`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `Bear`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `BellyFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Big`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum   | Determines which character this visual effect follows. | 2 | `zaratana` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`position`](./Arrays.md#array-position) | Array  | The world-space coordinates for this object. || `10.5`<br>`[4.5 4.5]` |

</details>


### Object: `BigCatnip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BigFood`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BigHolding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `BigHoldingCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `BigScrap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BiggestFood`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BirdFeed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `BirdPoopHat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. || `+1`<br>`-1`<br>`-2` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. || `true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Bishop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `BlackBird`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BlackHole`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Blessing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`intro`](./NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. || `{ . . . }` |
| [`main`](./Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Bomb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |

</details>


### Object: `BoneyardUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `Boris`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `BothObelisksUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ . . . }` |

</details>


### Object: `Bully`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `BunkerUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `Butcher`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`innate_items`](./Miscellaneous.md#object-innate_items) | Object  | An object specifying the class's starting equipment, with item slot names as keys. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Cat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum  | Specifies the form to change into. | 6 | `BigHolding`<br>`BigHoldingCat`<br>`SmallHolding` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 4 | `{ . . . }` |
| [`animation`](./Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


### Object: `Catepillar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `Catnip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `-1`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CatnipBig`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `-1`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `CaveBaby`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CaveMan`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CaveManSpear`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `CaveWoman`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CaveWomanHasCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `CavesUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `CerberubsJumpBlind`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `CerberubsJumpNormal`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `ChaosAntennaAttached`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `CharacterTypeGainsStatusAtBattleStart`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | - | `CharacterTypeGainsStatusAtBattleStart` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |

</details>


### Object: `Charging`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `CharmedDip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedFloater`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedPile`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Cherub`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Chicken`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `-1`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Close`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `CloseConvert`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Cockroach`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. || `0`<br>`1`<br>`10` |

</details>


### Object: `Coin`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin10`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Colorless`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`move_pool`](./Arrays.md#array-move_pool) | Array   | An array of movement ability names available to the class. || `[` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`tutorial_levelup_active_pool`](./Arrays.md#array-tutorial_levelup_active_pool) | Array   | An array of active ability names presented during tutorial level-up. || `[` |
| [`tutorial_levelup_active_pool_2`](./Arrays.md#array-tutorial_levelup_active_pool_2) | Array   | An array of active ability names presented in a second tutorial level-up. || `[` |
| [`tutorial_levelup_passive_pool`](./Arrays.md#array-tutorial_levelup_passive_pool) | Array   | An array of passive ability names presented during tutorial level-up. || `[` |

</details>


### Object: `Comfort`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Conditional_DoesDamage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_DoesDamage` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. || `1`<br>`10`<br>`2` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |

</details>


### Object: `Conditional_FinishedSpawning`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_FinishedSpawning` |
| [`Imprison`](./Enums.md#enum-imprison) | Enum  | Specifies the type of unit or object to summon as a prison. | 2 | `BeefyCharmedLeech`<br>`CharmedLeech`<br>`Fly` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |

</details>


### Object: `CoreObeliskUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `CoreUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `CraterUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](./Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `Cultist`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `Damaged`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |

</details>


### Object: `DashRandomly`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 4 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `DeadHummingbird`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `-1`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Default`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 54 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 20 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`set_house`](./Enums.md#enum-set_house) | Enum   | Specifies which house layout to use for this upgrade. | 2 | `House1`<br>`House2`<br>`House3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `Default_Ceiling`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Default_Ground`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `DemonicGlyph_Bite`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Bounce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Fire`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Movement`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Summon`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DesireMech`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |

</details>


### Object: `Die`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `DimensionXUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ . . . }` |

</details>


### Object: `Dove`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Down`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |

</details>


### Object: `Druid`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`innate_passives`](./Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Drunker`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `DualSword`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 2 | `.5`<br>`.66`<br>`.75` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DualSword_Primed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 2 | `.5`<br>`.66`<br>`.75` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Dumb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `DybbukPossessed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum   | Determines the ability used when the Dybbuk possession ends. | 2 | `DybbukReturn` |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum   | Determines the ability used for the possessed unit to attack itself. | 2 | `Dybbuk_StopHittingYourself` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Eagle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Earth`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 4 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


### Object: `Electric`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


### Object: `Empty`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `EndOfTimeUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 4 | `{ . . . }` |

</details>


### Object: `Escape`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `EventBounty`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |

</details>


### Object: `Evolution`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `EvolveAbilityFromPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 26 | `2`<br>`3`<br>`4` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 26 | `true` |

</details>


### Object: `Explody`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Explosive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `FightPhase`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Fighter`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[` |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`shield`](./Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. || `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Fire`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `1`<br>`10`<br>`2` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `FireFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`combo`](./Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. || `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |

</details>


### Object: `Firefly`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. || `0`<br>`1`<br>`10` |

</details>


### Object: `FloatingDebris`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


### Object: `Floor1_Large`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `0`<br>`1`<br>`2` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 2 | `attic`<br>`room1`<br>`room2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 2 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 2 | `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 2 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 2 | `16`<br>`18`<br>`33` |

</details>


### Object: `Floor1_Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `0`<br>`1`<br>`2` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 2 | `attic`<br>`room1`<br>`room2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 2 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 2 | `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 2 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 2 | `16`<br>`18`<br>`33` |

</details>


### Object: `Floor2_Large`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. || `attic`<br>`room1`<br>`room2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `Floor2_Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. || `attic`<br>`room1`<br>`room2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `Flop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Flop2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Flush`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `FlushBubs`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `FlushHost`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `FlushNettle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Fly`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. || `0`<br>`1`<br>`10` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `Food`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | If true, duplicate items of this type can appear in the same shop inventory. | 4 | `true` |
| [`amount`](./Arrays.md#array-amount) | Array  | For ambient light, the target brightness value (as a float or percentage array for RGB). | 4 | `.1`<br>`.25`<br>`.35` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 4 | `{ . . . }` |
| `weight` | Float | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `FoodBig`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `-1`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `FoodMedium`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `-1`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `FoodMove`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `ForceMoveAway`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean | If true, this option requires no cost to activate. | 2 | `false` |

</details>


### Object: `ForceTrample`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `FreeSpell`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Full`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`statuses_on_enter_form`](./Miscellaneous.md#object-statuses_on_enter_form) | Object  | Statuses or abilities applied when entering this form. | 4 | `{ . . . }` |

</details>


### Object: `FutureUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `GenFlag_Boss_Spewer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](./Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 2 | `{ . . . }` |

</details>


### Object: `GenFlag_Boss_Stacy`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](./Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 2 | `{ . . . }` |
| [`miniboss_event`](./Miscellaneous.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 2 | `{ . . . }` |

</details>


### Object: `GlowingSeed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `GoldenEgg`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Grass`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`10`<br>`2` |

</details>


### Object: `Gravity`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Grown`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |
| `weak_threshold` | Integer | The health threshold below which the unit is considered weakened. | 2 | `0`<br>`1`<br>`15` |

</details>


### Object: `GuaranteedJackpot`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Guarding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `HalfDead`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `HardPathUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](./Miscellaneous.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 4 | `{ . . . }` |

</details>


### Object: `Harpy`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `HarpysClaw`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `HasCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 10 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 10 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 8 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 8 | `{ . . . }` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `HasDeadCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `HasRock`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


### Object: `Headless`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `HealRandomInjury`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Health`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Hint_CrackedVisuals`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Hint_CrackedVisuals2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Hint_CrackedVisuals3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Holding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Holy`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 4 | `1`<br>`10`<br>`2` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `House1`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](./Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 2 | `{ . . . }` |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum   | Specifies the background frame identifier used for positioning background elements. | 2 | `large`<br>`small` |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum   | Specifies the background movie clip asset for this house. | 2 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum   | Specifies the foreground movie clip asset for this house. | 2 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](./Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 2 | `{ . . . }` |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 2 | `.6`<br>`.7`<br>`.8` |

</details>


### Object: `House2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](./Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 2 | `{ . . . }` |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum   | Specifies the background frame identifier used for positioning background elements. | 2 | `large`<br>`small` |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum   | Specifies the background movie clip asset for this house. | 2 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum   | Specifies the foreground movie clip asset for this house. | 2 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](./Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 2 | `{ . . . }` |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 2 | `.6`<br>`.7`<br>`.8` |

</details>


### Object: `House3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](./Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 2 | `{ . . . }` |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum   | Specifies the background frame identifier used for positioning background elements. | 2 | `large`<br>`small` |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum   | Specifies the background movie clip asset for this house. | 2 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum   | Specifies the foreground movie clip asset for this house. | 2 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](./Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 2 | `{ . . . }` |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 2 | `.6`<br>`.7`<br>`.8` |

</details>


### Object: `HumanDead`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `HummingBird`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Hunter`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[` |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Ice`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |

</details>


### Object: `IceAgeUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `InitialPhase`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Insane_Ceiling`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Insane_Ground`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Item`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 21 | `{ . . . }` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 18 | `2`<br>`3`<br>`4` |
| `mandatory` | Boolean | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 14 | `1`<br>`3`<br>`6` |
| `weight` | Float | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |

</details>


### Object: `Jack_Gainaltfurniture`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | String | Specifies a dialog entry or dialog tree to display. | 16 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 8 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 2 | `1` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 2 | `1` |

</details>


### Object: `Jester`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Johnny`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `JohnnyBubs`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `JohnnyHost`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `JohnnyNettle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Joystick`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `JunkyardUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](./Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `JurassicUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `LargeAttic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`built_in_collision`](./Arrays.md#array-built_in_collision) | Array   | A list of collision geometry definitions for the room. || `[` |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array   | A list of additional boundary planes for the room. || `[` |
| `height` | Integer | The height in tiles the target is launched into the air. || `0`<br>`1`<br>`2` |
| [`id`](./Enums.md#enum-id) | Enum  | The unique numerical identifier for this injury or status effect. || `-1`<br>`0`<br>`1` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. || `attic`<br>`room1`<br>`room2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. || `16`<br>`18`<br>`33` |

</details>


### Object: `LargeBirdPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `LargeHouse`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](./Enums.md#enum-set_house) | Enum   | Specifies which house layout to use for this upgrade. | 2 | `House1`<br>`House2`<br>`House3` |

</details>


### Object: `LargeHouse_Floor2Large`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `LargeHouse_Floor2Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `LastHit`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `LeapClose`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Leave`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `LevelUp`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 3 | `{ . . . }` |

</details>


### Object: `Lifted`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Lighting`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient` | String | A multiplier for the ambient light intensity. | 10 | `.4`<br>`.5`<br>`.6` |
| [`smallray_clip`](./Enums.md#enum-smallray_clip) | Enum   | Specifies the visual style or clip for small light rays. | 2 | `Bunkerlight`<br>`labligtht` |
| [`bigrays`](./Arrays.md#array-bigrays) | Array  | A two-value array defining the intensity or count of large light rays. || `[0, 0]`<br>`[1, 1]` |
| [`smallrays`](./Arrays.md#array-smallrays) | Array  | A two-value array defining the intensity or count of small light rays. || `[0, 0]`<br>`[1, 2]`<br>`[2, 6]` |

</details>


### Object: `Lit`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `LostSoul`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Mage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[` |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `MagicSeed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `MeatWorldUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 4 | `{ . . . }` |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ . . . }` |

</details>


### Object: `MeatWorldUnlockedFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](./Miscellaneous.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 2 | `{ . . . }` |
| [`mw_boss`](./Miscellaneous.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 2 | `{ . . . }` |
| [`mw_earlyhome`](./Miscellaneous.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 2 | `{ . . . }` |
| [`mw_event1`](./Miscellaneous.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 2 | `{ . . . }` |
| [`mw_hard1`](./Miscellaneous.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 2 | `{ . . . }` |
| [`mw_home`](./Miscellaneous.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 2 | `{ . . . }` |
| [`mw_quest_event`](./Miscellaneous.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 2 | `{ . . . }` |
| [`mw_treasure`](./Miscellaneous.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 2 | `{ . . . }` |

</details>


### Object: `MedBirdPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `MedCatnip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `MedScrap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Medic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[` |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. || `[` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `MediumHouse`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](./Enums.md#enum-set_house) | Enum   | Specifies which house layout to use for this upgrade. | 2 | `House1`<br>`House2`<br>`House3` |

</details>


### Object: `MediumHouse_SmallRoom`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `Monk`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`innate_items`](./Miscellaneous.md#object-innate_items) | Object  | An object specifying the class's starting equipment, with item slot names as keys. || `{ . . . }` |
| [`innate_passives`](./Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `MoonObeliskUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `MoonUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `Mounted`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `MouthFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `MoveAway`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 8 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveCenter`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveClose`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 8 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 6 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveForBarrage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveForDash`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveForGrass`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveForPounce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveForSpin`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveForThrow`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 4 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveOneForPuke`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveSpaced`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveToHead`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveTowards`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Mutant`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 2 | `.5`<br>`.66`<br>`.75` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `NCGravecrawlFAR`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Necromancer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `NeutronStar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `NoEyes`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `NoStick`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


### Object: `NonCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum  | Specifies the form to change into. | 6 | `BigHolding`<br>`BigHoldingCat`<br>`SmallHolding` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 4 | `{ . . . }` |
| [`animation`](./Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


### Object: `Normal`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 20 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 10 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `NormalFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `NotPriming`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Nothing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


### Object: `Nuke`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `failable` | Boolean | If true, the event or action has a chance to fail. || `true` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum   | Specifies the map destination hinted by this item or event. || `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. || `true` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. || `true` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. || `false`<br>`true` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`shield`](./Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. || `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. || `-1`<br>`-10`<br>`-2` |

</details>


### Object: `Obey`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Off`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `OffMap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 6 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `OffScreen`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `OneAlive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 6 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `OneEye`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Open`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `OpenCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Out`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Parousworm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. || `-1`<br>`-2`<br>`-3` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. || `true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. || `true` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |

</details>


### Object: `ParticleAttractor`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force_end` | Number | The final force applied to particles over time, as a scalar or 3D vector. | 6 | `200`<br>`500`<br>`[0 -1 0]` |
| `force_start` | Number | The initial force applied to particles, as a scalar or 3D vector. | 6 | `0`<br>`[0 -10 0]`<br>`[0 -20 0]` |
| `force` | Float | The force vector applied to particles. | 1 | `0`<br>`1`<br>`1.5` |
| [`towards`](./Arrays.md#array-towards) | Array  | A 3D vector point that the force pulls particles towards. || `[0 .5 0]`<br>`[5 0 5]` |

</details>


### Object: `ParticleBouncePlane`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Float | A multiplier for how much velocity is retained on bounce, from 0 (lost) to 1 (perfect). | 74 | `.1`<br>`.25`<br>`.5` |
| `friction` | Float | A scalar or 3D vector multiplier for velocity reduction applied over time. | 70 | `.1`<br>`.2`<br>`.5` |
| [`plane`](./Enums.md#enum-plane) | Enum  | Specifies the direction the particle bounces off. Valid values are "right" and "back". | 32 | `back`<br>`right` |
| `position` | Float | The world-space coordinates for this object. | 32 | `10.5`<br>`[4.5 4.5]` |
| `rotation_dampening` | Number | The amount of rotational velocity retained after bouncing, where 1 is full retention. | 1 | `1` |

</details>


### Object: `ParticleCharacterCollision`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_sphere_offset` | Number | The vertical offset of the character collision sphere from the character's origin. | 1 | `0` |
| `inherit_velocity` | String | The fraction of the character's velocity inherited by the particle upon collision. | 1 | `.5` |
| `pushforce` | Number | The magnitude of force applied to push the character away from the particle on collision. | 1 | `2` |

</details>


### Object: `ParticleGlobalForce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array  | For ambient light, the target brightness value (as a float or percentage array for RGB). | 27 | `.1`<br>`.25`<br>`.35` |
| [`id`](./Enums.md#enum-id) | Enum  | The unique numerical identifier for this injury or status effect. | 27 | `-1`<br>`0`<br>`1` |

</details>


### Object: `ParticleLineCollisions`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Float | A multiplier for how much velocity is retained on bounce, from 0 (lost) to 1 (perfect). | 6 | `.1`<br>`.25`<br>`.5` |
| `friction` | Float | A scalar or 3D vector multiplier for velocity reduction applied over time. | 6 | `.1`<br>`.2`<br>`.5` |
| `end_on_collision` | Boolean | If true, the particle is destroyed when it collides with a line. | 2 | `true` |

</details>


### Object: `ParticleRandomForce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`begin`](./Arrays.md#array-begin) | Array  | The initial force applied to the particle as a 3D vector, where any axis can be a random range [min, max]. || `[0, -10, 0]`<br>`[0, -20, 0]`<br>`[0, [-20, 20], 0]` |
| [`end`](./Enums.md#enum-end) | Enum  | Defines the final animation state or offset vector for a particle's lifespan. || `[-20, 0, 20]`<br>`[0, -450, 0]`<br>`[0, [200, 900], 0]` |

</details>


### Object: `ParticleTornadoForce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force` | Float | The force vector applied to particles. | 19 | `0`<br>`1`<br>`1.5` |
| [`axis`](./Arrays.md#array-axis) | Array  | The 3D vector defining the central axis around which the tornado force rotates. || `[-1 0 0]`<br>`[0 -0.5 0]`<br>`[0 -1 0]` |
| [`point`](./Arrays.md#array-point) | Array  | The 3D position of the tornado's center point relative to the particle system. || `[0 -8 0]`<br>`[0 .8 0]`<br>`[0 0 0]` |

</details>


### Object: `PeaceSymbol`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `PeaceSymbolFacePaint`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `PermanentCharm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |

</details>


### Object: `Pigeon`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `PopAndSpawn`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 4 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 2 | `false`<br>`true` |
| `clone_referenced_catdata` | Boolean | If true, the spawned unit is a clone of the referenced cat data, including its stats and equipment. | 2 | `true` |
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 2 | `false`<br>`true` |

</details>


### Object: `Possessing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Primed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Priming`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Psychic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`innate_passives`](./Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Pulp2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |

</details>


### Object: `Pulp3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |

</details>


### Object: `Pulp4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |

</details>


### Object: `Pulp5`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |

</details>


### Object: `Pulp6`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |

</details>


### Object: `Pulp7`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 | `.5`<br>`1`<br>`1.3` |

</details>


### Object: `Rage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 16 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 12 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 12 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 8 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 2 | `.5`<br>`.66`<br>`.75` |

</details>


### Object: `Rain`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). || `.005`<br>`.01`<br>`.03` |
| `chain` | Boolean | Specifies the ability to chain into and execute. || `AcidSplash`<br>`CaveSplash`<br>`FireFullSmall` |
| [`combo`](./Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. || `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| `emit_amount` | Number | The number of particles emitted per burst. || `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. || `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Float | The rate of particle emission per second. || `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. || `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. || `false`<br>`true` |
| [`force`](./Arrays.md#array-force) | Array  | The force vector applied to particles. || `0`<br>`1`<br>`1.5` |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. || `[Fire]`<br>`[Heat]`<br>`[Holy]` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. || `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. || `.`<br>`.025`<br>`.35` |
| [`particles`](./Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. || `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| [`projection_matrix`](./Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). || `default` |
| [`render_mode`](./Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). || `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. || `{ . . . }` |
| [`simulation_space`](./Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). || `global`<br>`local` |
| `size_start` | String | The starting size of particles. || `.1`<br>`.2`<br>`.3` |
| `speed_scale` | String | A multiplier for particle speed. || `.05`<br>`.1`<br>`.2` |
| `speed_start` | Float | The initial speed of particles. || `-2`<br>`.001`<br>`.1` |

</details>


### Object: `RandomArmorPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `RandomBiggerArmorPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `RandomBiggerCatnipPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `RandomBiggerFoodPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `RandomCatnipPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `RandomFoodPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `RaptorEgg`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |

</details>


### Object: `Raven`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `RavenFeather`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Return`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ReturnA`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `RunFar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Scrap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`shield`](./Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. || `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Seagull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `SewersUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `Shadow`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Equation | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 4 | `-999999`<br>`.05*X`<br>`.25` |
| [`class`](./Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. || `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ShowFakeDamage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`style`](./Arrays.md#array-style) | Array  | Specifies the visual styles (e.g., crit) used for the fake damage display. || `[crit]` |

</details>


### Object: `Sitting`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `SlotResult_Explode`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. || `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `SlotResult_Jackpot_Coins`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. || `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `SlotResult_Nothing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `SlotResult_RandomPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


### Object: `SmallAttic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `0`<br>`1`<br>`2` |
| [`id`](./Enums.md#enum-id) | Enum  | The unique numerical identifier for this injury or status effect. | 2 | `-1`<br>`0`<br>`1` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 2 | `attic`<br>`room1`<br>`room2` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 2 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `width` | Number | The number of tiles the room spans horizontally. | 2 | `16`<br>`18`<br>`33` |
| [`built_in_collision`](./Arrays.md#array-built_in_collision) | Array   | A list of collision geometry definitions for the room. || `[` |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array   | A list of additional boundary planes for the room. || `[` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. || `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. || `{ . . . }` |

</details>


### Object: `SmallBirdPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |

</details>


### Object: `SmallHolding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `SmallHoldingCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `SmallHouse_Attic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 2 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 2 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `Snake`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `SpawningPhase`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `SpearRun`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 4 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Squirrel`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `SquirrelForm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. || `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. || `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array / Enum  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). || `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Standing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Standing2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Start_Ceiling`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Stimulation`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Stop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `SuckMF`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `SwordAndShield`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `SwordAndShield_Primed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `TF_TargetAllies`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `TF_TargetEnemies`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `TVBotDie`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `TVBotDumb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `TVBotObey`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `TVBotStop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Tank`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[` |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Tar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `TarFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `TempDexterityUp`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |

</details>


### Object: `TempPassiveWhileHasStatus`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 2 | `1`<br>`2`<br>`3` |

</details>


### Object: `TempSpeedUp`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |

</details>


### Object: `TheEndUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `Thief`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. || `[` |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Throb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |

</details>


### Object: `ThrobBubs`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `ThrobHost`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `ThrobNettle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `ThrobbingArteryDone`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `Thunderstorm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| `lightning_fx` | Boolean | If true, lightning visual effects will occur during this thunderstorm. | 1 | `true` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| [`combo`](./Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. || `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. || `[Fire]`<br>`[Heat]`<br>`[Holy]` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`particles`](./Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. || `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |

</details>


### Object: `TieDyeBandana`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Tinkerer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. || `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. || `[` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. || `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. || `[` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`innate_passives`](./Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. || `{ . . . }` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. || `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `nouns` | Array | A list of naming words used to generate animal names. || `[` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. || `[` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. || `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. || `{ . . . }` |

</details>


### Object: `Toad`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `Transformed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Turkey`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. || `-1`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Turtle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |

</details>


### Object: `Turtled`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 4 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 4 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |

</details>


### Object: `TwoAlive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 6 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `TwoEyes`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Unflip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Unlit`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Unwashed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Up`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `VolcanoAntennaAttached`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 4 | `{ . . . }` |

</details>


### Object: `WallOfFleshDone`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `Washed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `Washer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Water`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


### Object: `WeirdEgg`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`intro`](./NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`main`](./Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `WereMan`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. || `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Wind`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 4 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


### Object: `WishBone`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. || `1`<br>`2`<br>`true` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`durability`](./Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. || `0`<br>`1`<br>`10` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Zealot`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ZealotBomb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 2 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


---


## Auto-Discovered Objects


### Object: `AntlerSwipe`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `AntlerSwipe2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BasicDashAttackMove_NoKnockback`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BerserkDash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BirthSquirrel`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BlackShard`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Number | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `Boulder`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `CharmTrap`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Chitter`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `DeathWormEat`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`temporary_effects`](./Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |

</details>


### Object: `EtherSoakedRag`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `HardenSkin`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `HardenSkin2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `HeadTumor`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `HornCharge`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `JewelOfDrog`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |

</details>


### Object: `MegaGuppy`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `MockSong`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MockSong2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MonkeyThrow`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MonkeyThrow2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `MoonHandDrop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `MoonHeadFlail`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Pounce`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Prance`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Prance2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `RandomPickup`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `Scavenge`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Scavenge2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`temporary_effects`](./Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Synthesize`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Synthesize2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `TaintedOffering`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TaintedOffering2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Tease`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Tease2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `TheDestroyer`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Thrash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ThrowPoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TigerSwipes`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TigerSwipes2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Timber`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`temporary_effects`](./Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |

</details>


### Object: `TinaFlail`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `TinaFlailRage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `ZombieCatFamiliar`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `cm_RaptorEggSpawn`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `head_CrownOfHorns`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `megadino`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_MEGADINO_QUOTE_1` | String | The first boss quote spoken by Megadino. | 1 ||
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |

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
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |

</details>