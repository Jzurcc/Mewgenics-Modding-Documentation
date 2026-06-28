---
title: "Logic Keys Schema"
description: "Core conditionals, loops, and execution flow."
---

# Logic Keys Schema

## Overview
> [!NOTE]
> This schema documents the low-level logic structures used by the engine to evaluate if/then statements inside GON files.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
CheckPoison {
    if_has_status "Poison"
    then {
        damage 5
    }
}
```

---



## Engine: Logic Keys

This document is the authoritative reference for Logic Blocks. All of the contexts below can appear as dynamic keys inside an `effects {}` block, or directly inside abilities. Many of these are conditional wrappers that evaluate a condition before executing their nested object, while others redirect execution flow (e.g. `ApplyToSource`).

> **Note:** Because many of these contexts accept arbitrary nested Logic Blocks, any entry marked `{Logic Keys}` recursively refers back to this same document.

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root), [`effects` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`temporary_effects` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temporary_effects), [`Else` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else), [`ApplyToSource` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_ally), [`Consumed` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-consumed), [`Conditional_Boss` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_speculative), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_formulaispositive), [`Conditional_Corpse` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_playercat), [`ApplyToConsumed` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytoconsumed), [`TimeDelayStatusApplication` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-post_spawn_statuses), [`Conditional_AffectedByElement` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_lasthit), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytorandompartymemberifpossible), [`ApplyToTile` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytotile), [`Conditional_BadRoll` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_badroll), [`Conditional_DestructibleCorpse` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_destructiblecorpse), [`Conditional_Displaceable` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_displaceable), [`Conditional_IsSelf` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_isself), [`Conditional_OncePerBattle` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_shielded), [`ApplyToRandomClosestAlly` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytorandomclosestally), [`Conditional_Backstab` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_backstab), [`Conditional_FinishedSpawning` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_finishedspawning), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hascleansabledebuffs), [`Conditional_IsTrample` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_istrample), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_livingplayercat), [`Conditional_NotBig` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notbig), [`Conditional_RandomChance` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_randomchance), [`NextBattleStatusStacks` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-nextbattlestatusstacks), [`ROOT` (Boss_Cutscene_Info)](../World_Maps_and_Events/Boss_Cutscene_Info.md#object-root), [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root), [`effects` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-effects), [`Conditional_RandomChance` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-conditional_randomchance), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-conditional_goodroll), [`ROOT` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-root), [`FormChanger` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchanger), [`effects` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-effects), [`Consumed` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-consumed), [`Conditional_GoodRoll` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_goodroll), [`Conditional_BadRoll` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-else), [`FinalBossBecomeTheChild` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbossbecomethechild), [`InfiniteRebirth` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-infiniterebirth), [`TVBotScreen` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tvbotscreen), [`ROOT` (Custom_Cats)](../Player_Progression_and_Cats/Custom_Cats.md#object-root), [`ROOT` (Damage_Text_Styles)](../Assets_and_Localization/Damage_Text_Styles.md#object-root), [`ROOT` (Difficulties)](../Reference_and_Meta/Difficulties.md#object-root), [`ROOT` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-root), [`effects` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-effects), [`ROOT` (Enemy_AI)](../Core_Entities_and_Combat/Enemy_AI.md#object-root), [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`global_effect_next_fight` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-global_effect_next_fight), [`ROOT` (Furniture_and_Metaprogression)](../World_Maps_and_Events/Furniture_and_Metaprogression.md#object-root), [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root), [`effects` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-effects), [`Else` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-statuscharactersonroundend), [`Conditional_GoodRoll` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_goodroll), [`Conditional_Corpse` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_partymember), [`ROOT` (Injuries)](../Player_Progression_and_Cats/Injuries.md#object-root), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root), [`effects` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects), [`Conditional_GoodRoll` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_goodroll), [`ApplyToSource` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-applytosource), [`Conditional_HasStatus` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_hasstatus), [`Else` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusontakehealthorshielddamage), [`Conditional_PartyMember` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_partymember), [`Conditional_Adjacent` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_onceperbattle), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-applytorandompartymemberifpossible), [`CastAgainWithStatus` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-castagainwithstatus), [`Conditional_Ally` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_enemy), `Conditional_HasCleansableDebuffs` (Items_and_Equipment), [`Conditional_HealthThreshold` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_healththreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_shielded), `CyborgTurns` (Items_and_Equipment), [`ScaldingOrbMoonBossOneShot` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-scaldingorbmoonbossoneshot), [`StatusAdjacentOnTheirTurnEnd` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusadjacentontheirturnend), [`StatusOnFallAsleep` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonfallasleep), `StatusOnTurnEndIfCastNSpells` (Items_and_Equipment), [`ROOT` (Item_Pools)](../Reference_and_Meta/Item_Pools.md#object-root), [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root), [`ROOT` (Miscellaneous)](../Reference_and_Meta/Miscellaneous.md#object-root), [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root), [`effects` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects), [`StatusOnStanceSwitch` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonstanceswitch), [`Conditional_Ally` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_ally), [`Conditional_Enemy` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_enemy), [`Else` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-else), [`StatusOnOverHealed` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonoverhealed), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_firstapplicationthisturn), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifmanaexact), [`Conditional_BadRoll` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hasstatus), [`AddStatusToBasicAttackWithCooldown` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattackwithcooldown), [`AddStatusToMeleeDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustomeleedamage), [`ApplyToSource` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-applytosource), [`Conditional_Adjacent` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_shielded), [`EscapeSequence` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-escapesequence), [`InfiniteRebirth` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-infiniterebirth), [`StatusOnDealtDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondealtdamage), [`on_throw` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-on_throw), [`Conditional_GoodRoll` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_goodroll), [`StatusAdjacentOnTheirTurnBegin` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusadjacentontheirturnbegin), [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root), [`ROOT` (Shops)](../World_Maps_and_Events/Shops.md#object-root), [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root), [`ROOT` (Status_Effect_Keywords)](../Core_Entities_and_Combat/Status_Effect_Keywords.md#object-root)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Default`](./Engine_LogicKeys.md#object-default) | Enum / Object  | The default form configuration for a unit, containing its standard stats and abilities. | 85 | `{ . . . }`<br>`release` |
| [`FormChange`](../Reference_and_Meta/Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 140 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Druid`](./Engine_LogicKeys.md#object-druid) | Object  | Specifies the 'Druid' form within FormChanger, used for boss dialogue. | 164 | `{ . . . }` |
| [`Fighter`](./Engine_LogicKeys.md#object-fighter) | Object  | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 136 | `{ . . . }` |
| [`Monk`](./Engine_LogicKeys.md#object-monk) | Object  | Defines a list of quotes for the Monk class. | 127 | `{ . . . }` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`ChangeTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 74 | `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 | `.1`<br>`.16666666`<br>`.3` |
| [`ApplyToSource`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 59 | `{ . . . }` |
| `rock` | Variable | A variable used in logic contexts. | 47 ||
| [`Conditional_HasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 47 | `{ . . . }` |
| [`Conditional_Enemy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 44 | `{ . . . }` |
| [`VisualFXTile`](../Reference_and_Meta/Enums.md#enum-visualfxtile) | Enum | Specifies the name of the visual effect to play on the target tile. | 39 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| [`BounceObject`](../Reference_and_Meta/Miscellaneous.md#object-bounceobject) | Enum / Object  | Specifies the object or projectile to spawn and bounce from the target. | 39 | `{ . . . }`<br>`AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`Conditional_Ally`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 37 | `{ . . . }` |
| [`EvolveAbilityFromPool`](./Engine_LogicKeys.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 26 | `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| [`Normal`](./Engine_LogicKeys.md#object-normal) | Integer / Object  | The normal form configuration, used as a baseline state for shape-shifting units. | 34 | `{ . . . }`<br>`0` |
| [`KnockUpAndAway`](../Reference_and_Meta/Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 25 | `{ . . . }` |
| [`Conditional_Boss`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 21 | `{ . . . }` |
| [`struggle_ability`](../Reference_and_Meta/Enums.md#enum-struggle_ability) | Enum | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 | `CHuskStruggle`<br>`CaveWomanEscape`<br>`LennyStruggle` |
| `force_contact` | Boolean | If true, the consumed unit is forced into contact with the consumer. | 15 | `true` |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 55 | `{ . . . }` |
| [`Conditional_NotBoss`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 16 | `{ . . . }` |
| [`Conditional_Speculative`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 12 | `{ . . . }` |
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 13 | `true` |
| [`mount_mode`](../Reference_and_Meta/Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 12 | `auto`<br>`true` |
| `do_not_pop_corpse` | Boolean | If true, the consumed unit's corpse is not popped upon consumption. | 11 | `true` |
| [`drop_on_death`](../Reference_and_Meta/Enums.md#enum-drop_on_death) | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 | `deferred`<br>`false`<br>`true` |
| [`Conditional_FormulaIsPositive`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_formulaispositive) | Object  | Defines effects that apply only if a given formula evaluates to a positive value. | 10 | `{ . . . }` |
| `X` | Variable | A generic variable placeholder often used for coordinates or unknown values. | 10 ||
| [`Nuke`](./Engine_LogicKeys.md#object-nuke) | Object  | Defines a nuke form with no attack or movement options. | 14 | `{ . . . }` |
| [`Conditional_Corpse`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 11 | `{ . . . }` |
| `formula` | Enum | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 8 | `X`<br>`X*10`<br>`X+1` |
| [`SpreadDisease`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 13 | `{ . . . }` |
| `wet` | Boolean | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 | `false`<br>`true` |
| [`BlackShard`](./Engine_LogicKeys.md#object-blackshard) | Object  | Defines the BlackShard object, likely a collectible item or a specific entity in the game. | 8 | `{ . . . }` |
| [`Conditional_InForm`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 7 | `{ . . . }` |
| [`Conditional_PlayerCat`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 7 | `{ . . . }` |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 95 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`Conditional_HealthThreshold`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 7 | `{ . . . }` |
| [`Conditional_Object`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 6 | `{ . . . }` |
| [`key`](../Reference_and_Meta/Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 6 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [`PopAndSpawn`](./Engine_LogicKeys.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 6 | `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 6 | `0`<br>`10`<br>`3` |
| [`UseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 14 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`Conditional_IsSelf`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_isself) | Object  | An object containing effects that are only applied if the target is the source unit itself. | 6 | `{ . . . }` |
| [`DestroyEquipmentAndAttachParasite`](../Reference_and_Meta/Miscellaneous.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 6 | `{ . . . }` |
| `LavaTile` | Variable | Represents a tile of lava on the map, which deals damage to units standing on it. | 14 ||
| [`Conditional_Familiar`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_familiar) | Object  | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 | `{ . . . }` |
| `moonhand` | Variable | A variable representing the Moon Hand, likely a limb or entity type associated with lunar or cosmic themes. | 8 ||
| [`Thrash`](./Engine_LogicKeys.md#object-thrash) | Object  | Defines the Thrash ability, likely a close-range, multi-hit attack. | 10 | `{ . . . }` |
| [`ZombieCatFamiliar`](./Engine_LogicKeys.md#object-zombiecatfamiliar) | Object  | Defines the ZombieCat familiar, a companion entity that follows the unit in combat. | 13 | `{ . . . }` |
| [`BirthSquirrel`](./Engine_LogicKeys.md#object-birthsquirrel) | Object  | Defines the Birth Squirrel ability, which spawns a squirrel ally when used. | 4 | `{ . . . }` |
| `WaterTile_Current` | Variable | Represents a water tile with a current, pushing units in a specific direction. | 5 ||
| [`Conditional_AffectedByElement`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_affectedbyelement) | Object  | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_FirstApplicationThisTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 8 | `{ . . . }` |
| [`Conditional_LastHit`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_lasthit) | Object  | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_OncePerBattle`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 4 | `{ . . . }` |
| [`DoDamage`](../Reference_and_Meta/Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 7 | `{ . . . }` |
| `drop_on_self_death` | Boolean | If true, the consumed unit is dropped when the consumer dies. | 3 | `true` |
| `WaterTile` | Variable | Represents a standard water tile on the map, which may slow or hinder movement. | 27 ||
| [`HeadTumor`](./Engine_LogicKeys.md#object-headtumor) | Object  | Defines the HeadTumor enemy, likely a swollen-headed unit with unique abilities. | 7 | `{ . . . }` |
| [`Craft`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 20 | `{ . . . }` |
| [`poop`](../Reference_and_Meta/Miscellaneous.md#object-poop) | Object  | Defines a poop event or interaction, often part of a random encounter or response in dialogue. | 19 | `{ . . . }` |
| [`ApplyToRandomPartyMemberIfPossible`](../Reference_and_Meta/Miscellaneous.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 3 | `{ . . . }` |
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. | 4 | `100%`<br>`50%` |
| [`Conditional_BossOrBig`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_bossorbig) | Object  | An object containing effects that are only applied if the target is a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_Buddy`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_buddy) | Object  | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 | `{ . . . }` |
| [`Conditional_DestructibleCorpse`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_destructiblecorpse) | Object  | An object containing effects that are only applied if the corpse is destructible. | 2 | `{ . . . }` |
| [`Conditional_Displaceable`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 2 | `{ . . . }` |
| [`Conditional_NotAlly`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notally) | Object  | An object containing effects that are only applied if the target is not an ally of the source. | 2 | `{ . . . }` |
| [`Conditional_NotBossOrBig`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notbossorbig) | Object  | An object containing effects that are only applied if the target is not a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_NotShielded`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notshielded) | Object  | An object containing effects that are only applied if the target does not have a shield active. | 2 | `{ . . . }` |
| `FireTile` | Variable | Represents a tile of fire on the map, which deals damage to units on it over time. | 9 ||
| [`GainDisorderFromPool`](../Reference_and_Meta/Miscellaneous.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 3 | `{ . . . }`<br>`all_disorders` |
| `gamewin` | Variable | A variable that triggers the end of the game, typically set to true when victory conditions are met. | 2 ||
| [`HornCharge`](./Engine_LogicKeys.md#object-horncharge) | Object  | Defines the Horn Charge ability, a dash attack that uses the character's horns to impale enemies. | 3 | `{ . . . }` |
| `humanoid` | Variable | A variable indicating whether the unit has a humanoid body type, affecting appearances and interactions. | 43 ||
| [`OffMap`](./Engine_LogicKeys.md#object-offmap) | Object  | The form configuration applied when the unit is off the battlefield map. | 9 | `{ . . . }` |
| `OilTile` | Variable | Represents a tile covered in oil on the map, which can ignite and explode when exposed to fire. | 9 ||
| `PartyExplosion` | Variable | A variable that triggers a large explosive effect, often an event-based mechanic. | 2 ||
| `Pilfer` | Object | Defines the Pilfer ability, which steals an item or resource from the target. | 3 | `{ . . . }` |
| [`Pulp2`](./Engine_LogicKeys.md#object-pulp2) | Object  | Form state for the second stage of pulping, with no attacks or movement. | 3 | `{ . . . }` |
| [`RandomPickup`](./Engine_LogicKeys.md#object-randompickup) | Object  | Defines the RandomPickup object, likely a lootable item with random contents. | 19 | `{ . . . }` |
| `TallGrassTile` | Number | The percentage chance of this tile being tall grass, which provides cover or concealment. | 16 | `15`<br>`80` |
| `the_coven` | Variable | A variable representing a group of characters called The Coven, likely a faction or story element. | 3 ||
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 | `25%`<br>`50%` |
| [`ThrowPoop`](./Engine_LogicKeys.md#object-throwpoop) | Object  | Defines the Throw Poop ability, which hurls a projectile of feces at the target. | 3 | `{ . . . }` |
| [`AntlerSwipe`](./Engine_LogicKeys.md#object-antlerswipe) | Object  | Defines the Antler Swipe ability, a basic melee attack that uses the character's antlers. | 3 | `{ . . . }` |
| [`BerserkDash`](./Engine_LogicKeys.md#object-berserkdash) | Object  | Defines the Berserk Dash ability, a close-range charge that damages and knocks back enemies. | 3 | `{ . . . }` |
| `BlankTile` | Number | The number of blank tiles in a map segment, which are empty spaces with no special properties. | 4 | `5` |
| [`Boulder`](./Engine_LogicKeys.md#object-boulder) | Object  | Defines the Boulder object, a large rock that blocks movement and can be destroyed or pushed. | 18 | `{ . . . }` |
| [`CharmTrap`](./Engine_LogicKeys.md#object-charmtrap) | Object  | Defines the Charm Trap, a hazard that charms units entering its area, turning them against allies. | 6 | `{ . . . }` |
| `flip` | Variable | A variable that triggers a flip animation or reverses the state of something. | 3 ||
| [`HardenSkin`](./Engine_LogicKeys.md#object-hardenskin) | Object  | Defines the Harden Skin ability, which increases the unit's defense by making its skin tougher. | 3 | `{ . . . }` |
| [`MonkeyThrow`](./Engine_LogicKeys.md#object-monkeythrow) | Object  | Defines the Monkey Throw ability, which hurls a projectile in a manner similar to a monkey. | 3 | `{ . . . }` |
| [`MoonHandDrop`](./Engine_LogicKeys.md#object-moonhanddrop) | Object  | A variant of MoonHandThrow that includes bonus passives to enable a finisher. | 6 | `{ . . . }` |
| [`Pounce`](./Engine_LogicKeys.md#object-pounce) | Object  | Defines the Pounce ability, a jumping attack that lunges at the target. | 4 | `{ . . . }` |
| [`Prance`](./Engine_LogicKeys.md#object-prance) | Object  | Defines the Prance ability, a self-targeted buff that increases evasion or mobility. | 3 | `{ . . . }` |
| [`Scavenge`](./Engine_LogicKeys.md#object-scavenge) | Object  | Defines the Scavenge ability, a movement skill that allows the unit to search for items. | 3 | `{ . . . }` |
| [`SquirrelForm`](./Engine_LogicKeys.md#object-squirrelform) | Object  | Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses. | 7 | `{ . . . }` |
| [`Synthesize`](./Engine_LogicKeys.md#object-synthesize) | Object  | Defines the Synthesize ability, a self-buff that creates or enhances items. | 3 | `{ . . . }` |
| [`TaintedOffering`](./Engine_LogicKeys.md#object-taintedoffering) | Object  | Defines the Tainted Offering ability, a harmful or corrupted gift bestowed upon a target. | 5 | `{ . . . }` |
| [`Tease`](./Engine_LogicKeys.md#object-tease) | Object  | Defines the Tease ability, a targeted status effect that provokes or irritates the target. | 3 | `{ . . . }` |
| [`TheDestroyer`](./Engine_LogicKeys.md#object-thedestroyer) | Object  | Defines The Destroyer object, likely a powerful boss or destructive entity. | 3 | `{ . . . }` |
| [`TigerSwipes`](./Engine_LogicKeys.md#object-tigerswipes) | Object  | Defines the Tiger Swipes ability, a rapid series of claw attacks. | 3 | `{ . . . }` |
| [`Else`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 86 | `{ . . . }` |
| [`Rain`](./Engine_LogicKeys.md#object-rain) | Object  | Defines the rain weather effect with associated particle, sound, and rendering settings. | 21 | `{ . . . }` |
| [`megadino`](./Engine_LogicKeys.md#object-megadino) | Variable | A variable representing a Mega Dinosaur, likely a large, powerful enemy or form. | 8 ||
| [`moonhead`](./Engine_LogicKeys.md#object-moonhead) | Variable | A variable representing the Moon Head, likely a head type or entity associated with lunar themes. | 5 ||
| `alien` | Variable | A variable indicating the unit is an alien, affecting its type and interactions. | 10 ||
| [`AllyInfested`](./Engine_LogicKeys.md#object-allyinfested) | Object  | Defines the AllyInfested object, which spawns an infested ally under the player's control. | 2 | `{ . . . }` |
| `angeljunk` | Variable | A variable representing angel junk, likely a cosmetic or mechanical part of an angelic character. | 2 ||
| [`AntlerSwipe2`](./Engine_LogicKeys.md#object-antlerswipe2) | Object  | A variant of Antler Swipe with a different description and potentially different parameters. | 2 | `{ . . . }` |
| [`BasicDashAttackMove_NoKnockback`](./Engine_LogicKeys.md#object-basicdashattackmove_noknockback) | Object  | Defines a basic dash attack that deals damage without knocking back the target. | 2 | `{ . . . }` |
| `berserkIdle` | Variable | A variable that sets the unit's idle animation to a berserk state. | 1 ||
| `bonusbird` | Variable | A variable representing a bonus bird, likely an additional familiar or entity. | 2 ||
| [`Boris`](./Engine_LogicKeys.md#object-boris) | Enum / Object  | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 8 | `{ . . . }`<br>`MegaGuppy_TransformBoris` |
| `BrambleTile` | Variable | Represents a tile of brambles on the map, which damages units crossing it. | 11 ||
| `chapter_corpse_medium` | Variable | A variable representing a medium-sized corpse prop used in chapter environments. | 8 ||
| [`Chitter`](./Engine_LogicKeys.md#object-chitter) | Object  | Defines the Chitter ability, a spell that deals magical damage or applies a status effect. | 2 | `{ . . . }` |
| [`cm_RaptorEggSpawn`](./Engine_LogicKeys.md#object-cm_raptoreggspawn) | Object  | Defines the template and meta properties for spawning a raptor egg entity. | 2 | `{ . . . }` |
| `Conditional_AbilityTargetIsSelf` | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 | `{ . . . }` |
| [`Conditional_ActiveWeather_Any`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_activeweather_any) | Object  | An object containing effects that execute only if any of the specified weather types are active. | 1 | `{ . . . }` |
| [`Conditional_Backstab`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_backstab) | Object  | An object containing effects that execute only if the attack lands on the target's back. | 1 | `{ . . . }` |
| [`Conditional_CanBeHealed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_canbehealed) | Object  | An object containing effects that execute only if the target can be healed. | 1 | `{ . . . }` |
| [`Conditional_DebuffRoll`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_debuffroll) | Object  | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`Conditional_FinishedSpawning`](./Engine_LogicKeys.md#object-conditional_finishedspawning) | Object  | Contains an inner effect block that only executes if the target has finished its spawning animation. | 1 | `{ . . . }` |
| [`Conditional_HasCleansableDebuffs`](./Engine_StatusAndPassiveKeys.md#object-conditional_hascleansabledebuffs) | Object  | An object containing effects that execute only if the unit has cleansable debuffs. | 2 | `{ . . . }` |
| [`Conditional_HasKnockback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_hasknockback) | Object  | An object containing actions that execute if the incoming damage has knockback. | 1 | `{ . . . }` |
| [`Conditional_IsPhysicalAttack`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_isphysicalattack) | Object  | A conditional block that executes its child actions only if the triggering event is a physical attack. | 1 | `{ . . . }` |
| [`Conditional_IsTrample`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_istrample) | Object  | An object containing effects that execute only if the ability is a trample attack. | 1 | `{ . . . }` |
| [`Conditional_LivingPlayerCat`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_livingplayercat) | Object  | An object containing effects that execute only if the source is a living player-owned cat. | 1 | `{ . . . }` |
| [`Conditional_NotBig`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notbig) | Object  | An object containing effects that execute only if the target is not a 'big' unit. | 1 | `{ . . . }` |
| [`Conditional_SourceAbilityHasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourceabilityhastag) | Object  | An object containing effects that execute only if the source ability has the specified tag. | 1 | `{ . . . }` |
| [`Conditional_SourceHasStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourcehasstatus) | Object  | An object containing effects that execute only if the source unit has the specified status. | 1 | `{ . . . }` |
| `container` | Variable | A variable representing a generic container or inventory slot for items. | 5 ||
| [`DeathWormEat`](./Engine_LogicKeys.md#object-deathwormeat) | Object  | Defines the eat ability for Death Worm, using the return template and specifying its name and movement flag. | 3 | `{ . . . }` |
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 6 | `true` |
| `DirtTile` | Variable | A variable representing a dirt tile type on the grid. | 4 ||
| [`drop_body_ability`](../Reference_and_Meta/Enums.md#enum-drop_body_ability) | Enum | Specifies the ability used to drop the consumed body. | 1 | `MoonHandDrop` |
| [`DualSword`](./Engine_LogicKeys.md#object-dualsword) | Object  | Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack. | 6 | `{ . . . }` |
| [`DybbukPossessed`](./Engine_LogicKeys.md#object-dybbukpossessed) | Object  | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 3 | `{ . . . }` |
| `EggSackTrap` | Variable | A variable representing an egg sack trap entity. | 2 ||
| [`EtherSoakedRag`](./Engine_LogicKeys.md#object-ethersoakedrag) | Object  | An object defining the properties of the Ether Soaked Rag item. | 3 | `{ . . . }` |
| [`Explosive`](./Engine_LogicKeys.md#object-explosive) | Enum / Object  | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 5 | `{ . . . }`<br>`MegaGuppy_TransformExplosive` |
| `ghost` | Variable | A variable representing a ghost unit or entity. | 9 ||
| `GlassTile` | Variable | A variable representing a glass tile type on the grid. | 18 ||
| `god` | Variable | A variable representing a god entity or modifier. | 5 ||
| [`Grown`](./Engine_LogicKeys.md#object-grown) | Object  | Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold. | 3 | `{ . . . }` |
| `grown_hitler_clone` | Variable | A variable representing a fully grown Hitler clone unit. | 3 ||
| [`HalfDead`](./Engine_LogicKeys.md#object-halfdead) | Object  | Defines the half-dead form with reduced movement and a dash attack. | 2 | `{ . . . }` |
| [`HardenSkin2`](./Engine_LogicKeys.md#object-hardenskin2) | Object  | An object defining the upgraded Harden Skin ability. | 2 | `{ . . . }` |
| [`head_CrownOfHorns`](./Engine_LogicKeys.md#object-head_crownofhorns) | Object  | A logic key that applies the Crown of Horns head item effect, causing retaliatory damage when the unit is hit. | 2 | `{ . . . }` |
| `hitler_clone` | Variable | A variable representing a Hitler clone unit. | 3 ||
| `hitler_clone_fetus` | Variable | A variable representing the fetus stage of a Hitler clone. | 4 ||
| `JesterMinusColorless` | Variable | A variable representing a Jester variant without colorless mechanics. | 2 ||
| [`JewelOfDrog`](./Engine_LogicKeys.md#object-jewelofdrog) | Object  | An object defining the properties of the Jewel of Drog item. | 3 | `{ . . . }` |
| `kill_on_consume` | Boolean | If true, the consumed unit is killed immediately upon consumption. | 1 | `true` |
| [`MegaGuppy`](./Engine_LogicKeys.md#object-megaguppy) | Object  | An object defining the properties of the Mega Guppy transformation or item. | 5 | `{ . . . }` |
| [`MockSong`](./Engine_LogicKeys.md#object-mocksong) | Object  | Defines the Mock Song spell, the basic attack for mockingbird form, including its name and description. | 2 | `{ . . . }` |
| [`MockSong2`](./Engine_LogicKeys.md#object-mocksong2) | Object  | Defines the upgraded Mock Song spell variant for mockingbird form. | 2 | `{ . . . }` |
| [`MonkeyThrow2`](./Engine_LogicKeys.md#object-monkeythrow2) | Object  | An object defining the upgraded Monkey Throw ability. | 2 | `{ . . . }` |
| [`MoonHeadFlail`](./Engine_LogicKeys.md#object-moonheadflail) | Object  | An object defining the Moon Head Flail ability or item. | 2 | `{ . . . }` |
| `NoDeathrattle` | Variable | A variable flag that prevents the unit from triggering deathrattle effects. | 1 ||
| [`Prance2`](./Engine_LogicKeys.md#object-prance2) | Object  | Defines an upgraded variant of the Prance ability, using a different description. | 2 | `{ . . . }` |
| `rotate_right` | Variable | A variable representing a right rotation action or state. | 1 ||
| [`Scavenge2`](./Engine_LogicKeys.md#object-scavenge2) | Object  | Defines an upgraded variant of the Scavenge ability, using a different description. | 2 | `{ . . . }` |
| [`Small`](./Engine_LogicKeys.md#object-small) | Object  | Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation. | 14 | `{ . . . }` |
| [`SmallHolding`](./Engine_LogicKeys.md#object-smallholding) | Object  | Form state when the unit is holding a small object, triggering a form change while consuming. | 3 | `{ . . . }` |
| [`SmallHoldingCat`](./Engine_LogicKeys.md#object-smallholdingcat) | Object  | Form state when the unit is holding a cat, triggering a form change while consuming. | 3 | `{ . . . }` |
| `spear` | Variable | A variable representing a spear weapon type. | 3 ||
| [`Standing`](./Engine_LogicKeys.md#object-standing) | Object  | Form state where the unit is standing, with default movement and attack. | 4 | `{ . . . }` |
| [`Synthesize2`](./Engine_LogicKeys.md#object-synthesize2) | Object  | Defines an upgraded variant of the Synthesize ability, using a different description. | 2 | `{ . . . }` |
| [`TaintedOffering2`](./Engine_LogicKeys.md#object-taintedoffering2) | Object  | An object defining the upgraded Tainted Offering ability. | 2 | `{ . . . }` |
| `TallFlowerTile` | Variable | A variable representing a tall flower tile type on the grid. | 9 ||
| [`Tease2`](./Engine_LogicKeys.md#object-tease2) | Object  | Defines an upgraded variant of the Tease ability, using a different description. | 2 | `{ . . . }` |
| `the_nuke_bearer` | Variable | A variable representing the entity that carries the nuke. | 2 ||
| `themotherspike` | Variable | A variable representing the Mother Spike entity. | 3 ||
| `threshold_expr` | Enum | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 | `item_aux` |
| [`TigerSwipes2`](./Engine_LogicKeys.md#object-tigerswipes2) | Object  | An object defining the upgraded Tiger Swipes ability. | 2 | `{ . . . }` |
| [`Timber`](./Engine_LogicKeys.md#object-timber) | Object  | Defines the Timber trample dash ability, an alt basic attack for Tree Form. | 3 | `{ . . . }` |
| [`TinaFlail`](./Engine_LogicKeys.md#object-tinaflail) | Object  | An object defining the Tina Flail ability or item. | 2 | `{ . . . }` |
| [`TinaFlailRage`](./Engine_LogicKeys.md#object-tinaflailrage) | Object  | An object defining the rage variant of the Tina Flail ability. | 2 | `{ . . . }` |
| [`TransformWeapon`](../Reference_and_Meta/Miscellaneous.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. | 2 | `{ . . . }` |
| `weapon_throw` | Variable | A variable representing a weapon throw action or projectile. | 33 ||
| [`weather`](../Reference_and_Meta/Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 1 | `[FlySwarm FireflySwarm ButterflySwarm]` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1038 | passives<br>class<br>tag |
| `contact_requires_adjacency` | Boolean | If false, contact effects are not restricted to adjacent tiles, allowing contact to trigger at range. | 14 | `false` |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 | `.1`<br>`.16666666`<br>`.3` |
| `two_way_contact` | Boolean | If true, contact effects apply to both the attacker and the target when the damage instance hits. | 2 | `true` |
| [`UseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 14 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

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
| [`GainDisorderFromPool`](../Reference_and_Meta/Miscellaneous.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 3 | `{ . . . }`<br>`all_disorders` |

</details>


---


#### `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 59

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`EquipPermanentItem`](../Reference_and_Meta/Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 5 | `BoneClub`<br>`Kidney` |
| [`EvolveAbilityFromPool`](./Engine_LogicKeys.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 26 | `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| [`FindItem`](../Reference_and_Meta/Enums.md#enum-finditem) | Enum  | The name of the specific item to find and add to the source's inventory. | 3 | `BoneClub`<br>`Molars`<br>`Pearl` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`FormChange`](../Reference_and_Meta/Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 140 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`GainCoinsRange`](../Reference_and_Meta/Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 11 | `{ . . . }` |

</details>


---


#### ``Conditional_ActiveWeather_Any`


**Definition:** An object containing effects that execute only if any of the specified weather types are active.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weather`](../Reference_and_Meta/Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 1 | `[FlySwarm FireflySwarm ButterflySwarm]` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_Adjacent`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_AffectedByElement`


**Definition:** Container for effects applied if the target is affected by a specified element, with optional Else block.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 80 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_Ally`


**Definition:** Defines effects that apply only if the target is an ally, with an optional else block for non-allies.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Reference_and_Meta/Miscellaneous.md#object-addstatustobasicattack), [`AddStatusToElementAbilities`](../Reference_and_Meta/Miscellaneous.md#object-addstatustoelementabilities), `Conditional_Adjacent`, `Conditional_SourceHasTag`, [`ExtraStatusWhenDealingDamage`](../Reference_and_Meta/Miscellaneous.md#object-extrastatuswhendealingdamage), [`StatusKilledCharacters`](../Reference_and_Meta/Miscellaneous.md#object-statuskilledcharacters), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 21 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 4 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_Backstab`


**Definition:** An object containing effects that execute only if the attack lands on the target's back.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_BadRoll`


**Definition:** An object containing an `odds` value and effects that are applied when a random roll succeeds.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](../Reference_and_Meta/Miscellaneous.md#object-statuseachturnbegin), [`StatusEachTurnEnd`](../Reference_and_Meta/Miscellaneous.md#object-statuseachturnend), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 8 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_Boss`


**Definition:** Contains effects that apply only if the target is a boss enemy.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `Conditional_HasTag`, [`StatusAllCharactersOnSpawn`](../Reference_and_Meta/Miscellaneous.md#object-statusallcharactersonspawn), [`StatusKillers`](../Reference_and_Meta/Miscellaneous.md#object-statuskillers), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 14 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_BossOrBig`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_Buddy`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_CanBeHealed`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
`damage_instance`<br>`spell`<br>`self_damage`

</details>


---




#### ``Conditional_Corpse`


**Definition:** Contains an inner effect block that only executes if the target is a corpse.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](../Reference_and_Meta/Miscellaneous.md#object-addstatustoelementdamage), `Conditional_Ally`, `Conditional_GoodRoll`, [`StatusOnBattleEnd`](../Reference_and_Meta/Miscellaneous.md#object-statusonbattleend), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_DebuffRoll`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_DestructibleCorpse`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_Displaceable`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_Enemy`


**Definition:** An object containing status effects or actions applied only if the target is an enemy.  
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Reference_and_Meta/Miscellaneous.md#object-addstatustobasicattack), [`AddStatusToElementAbilities`](../Reference_and_Meta/Miscellaneous.md#object-addstatustoelementabilities), [`AddStatusToSpells`](../Reference_and_Meta/Miscellaneous.md#object-addstatustospells), `Conditional_Corpse`, `Conditional_NotBoss`, [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 8 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_Familiar`


**Definition:** Container for effects applied if the unit has a familiar, with an optional Else block.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_FirstApplicationThisTurn`


**Definition:** Container for effects applied only on the first application of this ability during the turn.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](../Reference_and_Meta/Miscellaneous.md#object-statusonendmove), [`StatusOnKill`](../Reference_and_Meta/Miscellaneous.md#object-statusonkill), [`StatusOnUseAbilityWithTag`](../Reference_and_Meta/Miscellaneous.md#object-statusonuseabilitywithtag), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 5 | Default<br>FormChange<br>Druid |
| [`key`](../Reference_and_Meta/Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 6 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |

</details>


---




#### ``Conditional_FormulaIsPositive`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Reference_and_Meta/Miscellaneous.md#object-addstatustobasicattack), [`Else`](../Reference_and_Meta/Miscellaneous.md#object-else), [`StatusCharactersOnRoundEnd`](../Reference_and_Meta/Miscellaneous.md#object-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](../Reference_and_Meta/Miscellaneous.md#object-statuscharactersonroundstart), [`StatusEachTurnBegin`](../Reference_and_Meta/Miscellaneous.md#object-statuseachturnbegin), [`StatusEachTurnEnd`](../Reference_and_Meta/Miscellaneous.md#object-statuseachturnend), [`StatusOnBattleEnd`](../Reference_and_Meta/Miscellaneous.md#object-statusonbattleend), [`StatusOnEndMove`](../Reference_and_Meta/Miscellaneous.md#object-statusonendmove), [`StatusOnKill`](../Reference_and_Meta/Miscellaneous.md#object-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](../Reference_and_Meta/Miscellaneous.md#object-statusontakehealthorshielddamage), [`ally_rewards`](../Reference_and_Meta/Miscellaneous.md#object-ally_rewards), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 37 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 15 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_HasKnockback`


**Definition:** An object containing actions that execute if the incoming damage has knockback.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](../Reference_and_Meta/Miscellaneous.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_HasStatus`


**Definition:** Contains an inner effect block that only executes if the target has the specified status effect.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](../Reference_and_Meta/Miscellaneous.md#object-addstatustoalldamage), `Conditional_Boss`, [`CritsApplyStatus`](../Reference_and_Meta/Miscellaneous.md#object-critsapplystatus), [`Else`](../Reference_and_Meta/Miscellaneous.md#object-else), [`StatusOnTookDamage`](../Reference_and_Meta/Miscellaneous.md#object-statusontookdamage), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 160 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 22 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 10 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_HasTag`


**Definition:** Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](../Reference_and_Meta/Miscellaneous.md#object-addstatustoalldamage), [`AddStatusToBasicAttack`](../Reference_and_Meta/Miscellaneous.md#object-addstatustobasicattack), `Conditional_Object`, [`Else`](../Reference_and_Meta/Miscellaneous.md#object-else), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects), [`extra_statuses`](../Reference_and_Meta/Miscellaneous.md#object-extra_statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 49 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 43 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_HealthThreshold`


**Definition:** Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `Conditional_NotBoss`, `Conditional_Speculative`, [`Else`](../Reference_and_Meta/Miscellaneous.md#object-else), [`StatusOnTookDamage`](../Reference_and_Meta/Miscellaneous.md#object-statusontookdamage), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 7 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 6 | `0`<br>`10`<br>`3` |
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 | `25%`<br>`50%` |
| `threshold_expr` | Equation | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 | `item_aux` |

</details>


---




#### ``Conditional_InForm`


**Definition:** Contains effects that apply only if the target is in the specified form.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `Conditional_Buddy`, `Conditional_HasTag`, [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 95 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 7 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_IsPhysicalAttack`


**Definition:** A conditional block that executes its child actions only if the triggering event is a physical attack.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](../Reference_and_Meta/Miscellaneous.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_IsSelf`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_IsTrample`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_LastHit`


**Definition:** Container for effects applied only on the final hit of a multi-hit attack, with optional Else block.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_LivingPlayerCat`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_ManaThreshold`


**Definition:** Defines a conditional block that applies effects only if a unit's mana meets a specified threshold.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](../Reference_and_Meta/Miscellaneous.md#object-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 6 | `0`<br>`10`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_NotAlly`


**Definition:** An object containing effects that are only applied if the target is not an ally of the source.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_NotBig`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_NotBoss`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_NotBossOrBig`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_NotShielded`


**Definition:** An object containing effects that are only applied if the target does not have a shield active.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_Object`


**Definition:** Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](../Reference_and_Meta/Miscellaneous.md#object-else), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_OncePerBattle`


**Definition:** An object containing effects that can only trigger once per battle, preventing double-activation.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `Conditional_HealthThreshold`, [`StatusOnFullMana`](../Reference_and_Meta/Miscellaneous.md#object-statusonfullmana), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`key`](../Reference_and_Meta/Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 6 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_PartyMember`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_PlayerCat`


**Definition:** Defines effects that only apply if the target is a player-controlled cat.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `Conditional_Adjacent`, `Conditional_Ally`, [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_RandomChance`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_Shielded`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---




#### ``Conditional_SourceAbilityHasTag`


**Definition:** An object containing effects that execute only if the source ability has the specified tag.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_SourceHasStatus`


**Definition:** An object containing effects that execute only if the source unit has the specified status.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 160 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_SourceHasTag`


**Definition:** Defines a conditional block that applies effects only if the source of the effect has a specified tag.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Reference_and_Meta/Miscellaneous.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---




#### ``Conditional_Speculative`


**Definition:** Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `Conditional_AffectedByElement`, [`Else`](../Reference_and_Meta/Miscellaneous.md#object-else), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |

</details>


---




#### `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 85

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 20 | `{ . . . }` |
| [`Conditional_Displaceable`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 2 | `{ . . . }` |
| [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| [`Conditional_HasKnockback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_hasknockback) | Object  | An object containing actions that execute if the incoming damage has knockback. | 1 | `{ . . . }` |
| [`Conditional_HasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 47 | `{ . . . }` |
| [`Conditional_HealthThreshold`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 7 | `{ . . . }` |
| [`Conditional_Object`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 6 | `{ . . . }` |
| [`Conditional_Speculative`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 12 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 14 | Default<br>FormChange<br>Druid |
| [`AllyInfested`](./Engine_LogicKeys.md#object-allyinfested) | Array / Float / Object  | Defines the AllyInfested object, which spawns an infested ally under the player's control. | 2 | `{ . . . }` |
| [`DybbukPossessed`](./Engine_LogicKeys.md#object-dybbukpossessed) | Object  | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 3 | `{ . . . }` |
| [`FormChange`](../Reference_and_Meta/Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 140 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`GainCoinsRange`](../Reference_and_Meta/Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 11 | `{ . . . }` |
| [`ImmediateUseAbility`](../Reference_and_Meta/Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 11 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`ObjectOnHitCharacter`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`ScatterCoins`](../Reference_and_Meta/Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 8 | `{ . . . }` |

</details>


---


#### `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2166

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 47 | `{ . . . }` |
| [`Conditional_Enemy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 44 | `{ . . . }` |
| [`Conditional_Ally`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 37 | `{ . . . }` |
| [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| [`Conditional_Boss`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 21 | `{ . . . }` |
| [`Conditional_FormulaIsPositive`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_formulaispositive) | Object  | Defines effects that apply only if a given formula evaluates to a positive value. | 10 | `{ . . . }` |
| [`Conditional_Speculative`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 12 | `{ . . . }` |
| [`Conditional_Corpse`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 11 | `{ . . . }` |
| [`Conditional_HasStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 20 | `{ . . . }` |
| [`Conditional_InForm`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 7 | `{ . . . }` |
| [`Conditional_NotBoss`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 16 | `{ . . . }` |
| [`Conditional_Object`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 6 | `{ . . . }` |
| [`Conditional_PlayerCat`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 7 | `{ . . . }` |
| [`Conditional_Familiar`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_familiar) | Object  | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 | `{ . . . }` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 20 | `.4`<br>`.6`<br>`.7` |
| [`Conditional_AffectedByElement`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_affectedbyelement) | Object  | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_FirstApplicationThisTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 8 | `{ . . . }` |
| [`Conditional_LastHit`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_lasthit) | Object  | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_BadRoll`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 8 | `{ . . . }` |
| [`Conditional_BossOrBig`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_bossorbig) | Object  | An object containing effects that are only applied if the target is a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_Buddy`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_buddy) | Object  | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 | `{ . . . }` |
| [`Conditional_DestructibleCorpse`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_destructiblecorpse) | Object  | An object containing effects that are only applied if the corpse is destructible. | 2 | `{ . . . }` |
| [`Conditional_HealthThreshold`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 7 | `{ . . . }` |
| [`Conditional_IsSelf`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_isself) | Object  | An object containing effects that are only applied if the target is the source unit itself. | 6 | `{ . . . }` |
| [`Conditional_NotAlly`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notally) | Object  | An object containing effects that are only applied if the target is not an ally of the source. | 2 | `{ . . . }` |
| [`Conditional_NotBossOrBig`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notbossorbig) | Object  | An object containing effects that are only applied if the target is not a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_NotShielded`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notshielded) | Object  | An object containing effects that are only applied if the target does not have a shield active. | 2 | `{ . . . }` |
| [`Conditional_OncePerBattle`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 4 | `{ . . . }` |
| [`Conditional_Shielded`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 5 | `{ . . . }` |
| `Conditional_AbilityTargetIsSelf` | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 | `{ . . . }` |
| [`Conditional_ActiveWeather_Any`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_activeweather_any) | Object  | An object containing effects that execute only if any of the specified weather types are active. | 1 | `{ . . . }` |
| [`Conditional_Backstab`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_backstab) | Object  | An object containing effects that execute only if the attack lands on the target's back. | 1 | `{ . . . }` |
| [`Conditional_CanBeHealed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_canbehealed) | Object  | An object containing effects that execute only if the target can be healed. | 1 | `{ . . . }` |
| [`Conditional_DebuffRoll`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_debuffroll) | Object  | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`Conditional_Displaceable`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 2 | `{ . . . }` |
| [`Conditional_HasCleansableDebuffs`](./Engine_StatusAndPassiveKeys.md#object-conditional_hascleansabledebuffs) | Object  | An object containing effects that execute only if the unit has cleansable debuffs. | 2 | `{ . . . }` |
| [`Conditional_IsTrample`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_istrample) | Object  | An object containing effects that execute only if the ability is a trample attack. | 1 | `{ . . . }` |
| [`Conditional_LivingPlayerCat`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_livingplayercat) | Object  | An object containing effects that execute only if the source is a living player-owned cat. | 1 | `{ . . . }` |
| [`Conditional_NotBig`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notbig) | Object  | An object containing effects that execute only if the target is not a 'big' unit. | 1 | `{ . . . }` |
| [`Conditional_RandomChance`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 4 | `{ . . . }` |
| [`Conditional_SourceAbilityHasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourceabilityhastag) | Object  | An object containing effects that execute only if the source ability has the specified tag. | 1 | `{ . . . }` |
| [`Conditional_SourceHasStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourcehasstatus) | Object  | An object containing effects that execute only if the source unit has the specified status. | 1 | `{ . . . }` |
| [`Rain`](./Engine_LogicKeys.md#object-rain) | Object  | Defines the rain weather effect with associated particle, sound, and rendering settings. | 21 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 624 | Default<br>FormChange<br>Druid |
| [`BounceObject`](../Reference_and_Meta/Miscellaneous.md#object-bounceobject) | Enum / Object  | Specifies the object or projectile to spawn and bounce from the target. | 39 | `{ . . . }`<br>`AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`ChangeTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 74 | `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 9 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`CreateGlobalModifiers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 5 | `{ . . . }` |
| [`EvolveAbilityFromPool`](./Engine_LogicKeys.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 26 | `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| [`FindExtraItemFromPoolOnBattleEnd`](../Reference_and_Meta/Enums.md#enum-findextraitemfrompoolonbattleend) | Enum  | Specifies the item pool from which an extra item is granted at the end of combat. | 3 | `combat_reward_easy`<br>`pills` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`GainCoinsRange`](../Reference_and_Meta/Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 11 | `{ . . . }` |
| [`ImmediateUseAbility`](../Reference_and_Meta/Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 11 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`ObjectOnHitCharacter`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`PopAndSpawn`](./Engine_LogicKeys.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 6 | `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| [`SetDefaultFace`](../Reference_and_Meta/Enums.md#enum-setdefaultface) | Enum  | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 3 | `happy`<br>`insane`<br>`sad` |
| [`StatusAllCharactersOnSpawn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusallcharactersonspawn) | Object  | Defines status effects applied to all characters when they spawn into the battlefield. | 5 | `{ . . . }` |
| [`StatusGroup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. | 6 | `{ . . . }` |
| `TempDexterityUp` | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 5 | `2`<br>`X` |
| `TempStrengthUp` | Enum | The number of stacks of temporary Strength Up applied to the unit. | 7 | `1`<br>`2`<br>`X` |
| [`UseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 14 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>
## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `RandomPickup`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 19

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `Boulder`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `ZombieCatFamiliar`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Thrash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `megadino`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |
| `BOSS_MEGADINO_QUOTE_1` | String | The first boss quote spoken by Megadino. | 1 ||

</details>


### Object: `BlackShard`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `aux` | Number | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| `hint_destination` | String | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |

</details>


### Object: `HeadTumor`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `MoonHandDrop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`bonus_passives`](../Reference_and_Meta/Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |

</details>


### Object: `CharmTrap`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`keyword_tooltips`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |

</details>


### Object: `TaintedOffering`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |

</details>


### Object: `moonhead`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |
| `BOSS_MOONHEAD_QUOTE_1` | String | The first boss quote spoken by Moonhead. | 1 ||
| `BOSS_MOONHEAD_QUOTE_2` | String | The second boss quote spoken by Moonhead. | 1 ||
| `BOSS_MOONHEAD_QUOTE_3` | String | The third boss quote spoken by Moonhead. | 1 ||
| `BOSS_MOONHEAD_QUOTE_4` | String | The fourth boss quote spoken by Moonhead. | 1 ||

</details>#### ``Conditional_HasCleansableDebuffs`


**Definition:** An object containing effects that execute only if the unit has cleansable debuffs.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](../Reference_and_Meta/Miscellaneous.md#object-statuseachturnend), [`effects`](../Reference_and_Meta/Miscellaneous.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |

</details>


---


#### ``Conditional_DoesDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


#### ``Conditional_FinishedSpawning`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---
### Object: `MegaGuppy`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Pounce`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BirthSquirrel`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `Timber`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`temporary_effects`](../Reference_and_Meta/Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |

</details>


### Object: `TigerSwipes`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `ThrowPoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `TheDestroyer`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Tease`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `Synthesize`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |

</details>


### Object: `Scavenge`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Prance`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |

</details>


### Object: `MonkeyThrow`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `JewelOfDrog`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `HornCharge`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `HardenSkin`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |

</details>


### Object: `EtherSoakedRag`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `set` | String | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `rarity` | String | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


### Object: `DeathWormEat`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`temporary_effects`](../Reference_and_Meta/Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |

</details>


### Object: `BerserkDash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `AntlerSwipe`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `TinaFlailRage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `TinaFlail`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `TigerSwipes2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Tease2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `TaintedOffering2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |

</details>


### Object: `Synthesize2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Scavenge2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`temporary_effects`](../Reference_and_Meta/Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |

</details>


### Object: `Prance2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `MoonHeadFlail`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `MonkeyThrow2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `MockSong2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `MockSong`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `head_CrownOfHorns`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `HardenSkin2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `cm_RaptorEggSpawn`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `Chitter`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `BasicDashAttackMove_NoKnockback`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |

</details>


### Object: `AntlerSwipe2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `ZealotBomb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


---


## Auto-Discovered Objects


### Object: `Zealot`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |

</details>


### Object: `WishBone`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |

</details>


### Object: `Wind`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 2 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


### Object: `WereMan`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `WeirdEgg`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`intro`](../World_Maps_and_Events/NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 1 | `{ . . . }` |
| [`main`](../Reference_and_Meta/Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 1 | `{ . . . }` |

</details>


### Object: `Water`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Washer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Washed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `WallOfFleshDone`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


### Object: `VolcanoAntennaAttached`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `Up`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Unwashed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Unlit`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Unflip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `TwoEyes`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `TwoAlive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 3 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `TVBotStop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |

</details>


### Object: `TVBotObey`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |

</details>


### Object: `TVBotDumb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |

</details>


### Object: `TVBotDie`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |

</details>


### Object: `Turtled`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Turtle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Turkey`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


### Object: `Transformed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `Toad`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Tinkerer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`innate_passives`](../Reference_and_Meta/Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `TieDyeBandana`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Thunderstorm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 2 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `lightning_fx` | Boolean | If true, lightning visual effects will occur during this thunderstorm. | 1 | `true` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`combo`](../Reference_and_Meta/Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. | 1 | `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| [`hint_persistent_elements`](../Reference_and_Meta/Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. | 1 | `[Fire]`<br>`[Heat]`<br>`[Holy]` |

</details>


### Object: `ThrobNettle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `ThrobHost`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `ThrobBubs`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `ThrobbingArteryDone`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


### Object: `Throb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `Thief`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`complicated_abilities`](../Reference_and_Meta/Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 1 | `[` |
| [`complicated_passives`](../Reference_and_Meta/Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `TheEndUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `TF_TargetEnemies`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `TF_TargetAllies`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `TempSpeedUp`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `TempPassiveWhileHasStatus`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 4 | `{ . . . }` |

</details>


### Object: `TempDexterityUp`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `TarFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Tar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `Tank`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`complicated_abilities`](../Reference_and_Meta/Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 1 | `[` |
| [`complicated_passives`](../Reference_and_Meta/Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `SwordAndShield_Primed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `SwordAndShield`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `SuckMF`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `Stop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`keyword_tooltips`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |

</details>


### Object: `Stimulation`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Start_Ceiling`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Standing2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Standing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `SquirrelForm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array / Enum  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `Squirrel`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `SpearRun`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `SpawningPhase`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Snake`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `SmallHouse_Attic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `SmallHoldingCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `SmallHolding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `SmallBirdPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `SmallAttic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`id`](../Reference_and_Meta/Enums.md#enum-id) | Enum  | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |
| [`extra_bound_planes`](../Reference_and_Meta/Arrays.md#array-extra_bound_planes) | Array   | A list of additional boundary planes for the room. | 1 | `[` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 0 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 0 | `{ . . . }` |
| [`built_in_collision`](../Reference_and_Meta/Arrays.md#array-built_in_collision) | Array   | A list of collision geometry definitions for the room. | 0 | `[` |

</details>


### Object: `Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `SlotResult_RandomPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `SlotResult_Nothing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `SlotResult_Jackpot_Coins`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |

</details>


### Object: `SlotResult_Explode`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |

</details>


### Object: `Sitting`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `ShowFakeDamage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`style`](../Reference_and_Meta/Arrays.md#array-style) | Array  | Specifies the visual styles (e.g., crit) used for the fake damage display. | 1 | `[crit]` |

</details>


### Object: `Shadow`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Equation | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 2 | `-999999`<br>`.05*X`<br>`.25` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |

</details>


### Object: `SewersUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `Seagull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `Scrap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`shield`](../Reference_and_Meta/Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 1 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `RunFar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `ReturnA`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Return`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `RavenFeather`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Raven`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `RaptorEgg`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |

</details>


### Object: `RandomFoodPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `RandomCatnipPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `RandomBiggerFoodPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `RandomBiggerCatnipPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `RandomBiggerArmorPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `RandomArmorPickup`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `Rain`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 2 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`render_mode`](../Reference_and_Meta/Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| [`simulation_space`](../Reference_and_Meta/Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`projection_matrix`](../Reference_and_Meta/Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `size_start` | String | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | String | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| [`force`](../Reference_and_Meta/Arrays.md#array-force) | Array  | The force vector applied to particles. | 1 | `0`<br>`1`<br>`1.5` |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |
| `chain` | Boolean | Specifies the ability to chain into and execute. | 1 | `AcidSplash`<br>`CaveSplash`<br>`FireFullSmall` |
| [`combo`](../Reference_and_Meta/Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. | 1 | `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| [`hint_persistent_elements`](../Reference_and_Meta/Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. | 1 | `[Fire]`<br>`[Heat]`<br>`[Holy]` |

</details>


### Object: `Rage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 8 | `{ . . . }` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 6 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 4 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |

</details>


### Object: `Pulp7`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Pulp6`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Pulp5`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Pulp4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Pulp3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Pulp2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Psychic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`innate_passives`](../Reference_and_Meta/Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `Priming`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Primed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Possessing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `PopAndSpawn`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 1 | `false`<br>`true` |
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 1 | `false`<br>`true` |
| `clone_referenced_catdata` | Boolean | If true, the spawned unit is a clone of the referenced cat data, including its stats and equipment. | 1 | `true` |

</details>


### Object: `Pigeon`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `PermanentCharm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `PeaceSymbolFacePaint`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `PeaceSymbol`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`keyword_tooltips`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |

</details>


### Object: `ParticleTornadoForce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `force` | Float | The force vector applied to particles. | 19 | `0`<br>`1`<br>`1.5` |
| [`axis`](../Reference_and_Meta/Arrays.md#array-axis) | Array  | The 3D vector defining the central axis around which the tornado force rotates. | 19 | `[-1 0 0]`<br>`[0 -0.5 0]`<br>`[0 -1 0]` |
| [`point`](../Reference_and_Meta/Arrays.md#array-point) | Array  | The 3D position of the tornado's center point relative to the particle system. | 19 | `[0 -8 0]`<br>`[0 .8 0]`<br>`[0 0 0]` |

</details>


### Object: `ParticleRandomForce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`end`](../Reference_and_Meta/Enums.md#enum-end) | Enum  | Defines the final animation state or offset vector for a particle's lifespan. | 7 | `[-20, 0, 20]`<br>`[0, -450, 0]`<br>`[0, [200, 900], 0]` |
| [`begin`](../Reference_and_Meta/Arrays.md#array-begin) | Array  | The initial force applied to the particle as a 3D vector, where any axis can be a random range [min, max]. | 7 | `[0, -10, 0]`<br>`[0, -20, 0]`<br>`[0, [-20, 20], 0]` |

</details>


### Object: `ParticleLineCollisions`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `friction` | Float | A scalar or 3D vector multiplier for velocity reduction applied over time. | 6 | `.1`<br>`.2`<br>`.5` |
| `dampening` | Float | A multiplier for how much velocity is retained on bounce, from 0 (lost) to 1 (perfect). | 6 | `.1`<br>`.25`<br>`.5` |
| `end_on_collision` | Boolean | If true, the particle is destroyed when it collides with a line. | 2 | `true` |

</details>


### Object: `ParticleGlobalForce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`amount`](../Reference_and_Meta/Arrays.md#array-amount) | Array  | For ambient light, the target brightness value (as a float or percentage array for RGB). | 27 | `.1`<br>`.25`<br>`.35` |
| [`id`](../Reference_and_Meta/Enums.md#enum-id) | Enum  | The unique numerical identifier for this injury or status effect. | 27 | `-1`<br>`0`<br>`1` |

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


### Object: `ParticleBouncePlane`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dampening` | Float | A multiplier for how much velocity is retained on bounce, from 0 (lost) to 1 (perfect). | 74 | `.1`<br>`.25`<br>`.5` |
| `friction` | Float | A scalar or 3D vector multiplier for velocity reduction applied over time. | 70 | `.1`<br>`.2`<br>`.5` |
| `position` | Float | The world-space coordinates for this object. | 32 | `10.5`<br>`[4.5 4.5]` |
| [`plane`](../Reference_and_Meta/Enums.md#enum-plane) | Enum  | Specifies the direction the particle bounces off. Valid values are "right" and "back". | 32 | `back`<br>`right` |
| `rotation_dampening` | Number | The amount of rotational velocity retained after bouncing, where 1 is full retention. | 1 | `1` |

</details>


### Object: `ParticleAttractor`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`towards`](../Reference_and_Meta/Arrays.md#array-towards) | Array  | A 3D vector point that the force pulls particles towards. | 7 | `[0 .5 0]`<br>`[5 0 5]` |
| `force_start` | Number | The initial force applied to particles, as a scalar or 3D vector. | 6 | `0`<br>`[0 -10 0]`<br>`[0 -20 0]` |
| `force_end` | Number | The final force applied to particles over time, as a scalar or 3D vector. | 6 | `200`<br>`500`<br>`[0 -1 0]` |
| `force` | Float | The force vector applied to particles. | 1 | `0`<br>`1`<br>`1.5` |

</details>


### Object: `Parousworm`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 1 | `-1`<br>`-2`<br>`-3` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |
| `parasite` | Boolean | If true, the item is a parasite that attaches to a unit and cannot be removed normally. | 1 | `true` |

</details>


### Object: `Out`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `OpenCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Open`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `OneEye`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `OneAlive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 3 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `OffScreen`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `OffMap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 3 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Off`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Obey`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`keyword_tooltips`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |

</details>


### Object: `Nuke`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 1 | `-1`<br>`-10`<br>`-2` |
| [`shield`](../Reference_and_Meta/Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 1 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| `quest_item` | Boolean | If true, this item is a quest item and cannot be sold or destroyed. | 1 | `false`<br>`true` |
| `indestructible` | Boolean | If true, the item cannot be destroyed or removed. | 1 | `true` |
| `legacy_quest` | Boolean | If true, this item is part of a legacy quest. | 1 | `true` |
| [`hint_destination`](../Reference_and_Meta/Enums.md#enum-hint_destination) | Enum   | Specifies the map destination hinted by this item or event. | 1 | `boneyard`<br>`caves`<br>`core` |
| `failable` | Boolean | If true, the event or action has a chance to fail. | 1 | `true` |

</details>


### Object: `NotPriming`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Nothing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


### Object: `NoStick`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `NormalFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Normal`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 10 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 4 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `NonCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](../Reference_and_Meta/Enums.md#enum-formchange) | Enum  | Specifies the form to change into. | 3 | `BigHolding`<br>`BigHoldingCat`<br>`SmallHolding` |
| [`statuses`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 2 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


### Object: `NoEyes`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `NeutronStar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Necromancer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `NCGravecrawlFAR`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Mutant`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `MoveTowards`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveToHead`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveSpaced`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveOneForPuke`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveForThrow`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveForSpin`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveForPounce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveForGrass`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveForDash`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveForBarrage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveClose`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](../Reference_and_Meta/Enums.md#enum-move_for_ability) | Enum   | Specifies the ability that the unit needs to move close to use. | 3 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


### Object: `MoveCenter`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MoveAway`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `MouthFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Mounted`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `MoonUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `MoonObeliskUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


### Object: `Monk`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`innate_passives`](../Reference_and_Meta/Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. | 1 | `{ . . . }` |
| [`innate_items`](../Reference_and_Meta/Miscellaneous.md#object-innate_items) | Object  | An object specifying the class's starting equipment, with item slot names as keys. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `MedScrap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `MediumHouse_SmallRoom`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `MediumHouse`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](../Reference_and_Meta/Enums.md#enum-set_house) | Enum   | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

</details>


### Object: `Medic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`complicated_abilities`](../Reference_and_Meta/Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 1 | `[` |
| [`complicated_passives`](../Reference_and_Meta/Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `MedCatnip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `MedBirdPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `MeatWorldUnlockedFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](../Reference_and_Meta/Miscellaneous.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](../Reference_and_Meta/Miscellaneous.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](../Reference_and_Meta/Miscellaneous.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](../Reference_and_Meta/Miscellaneous.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](../Reference_and_Meta/Miscellaneous.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](../Reference_and_Meta/Miscellaneous.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](../Reference_and_Meta/Miscellaneous.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](../Reference_and_Meta/Miscellaneous.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |

</details>


### Object: `MeatWorldUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `MagicSeed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Mage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`complicated_abilities`](../Reference_and_Meta/Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 1 | `[` |
| [`complicated_passives`](../Reference_and_Meta/Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `LostSoul`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `Lit`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Lighting`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient` | String | A multiplier for the ambient light intensity. | 10 | `.4`<br>`.5`<br>`.6` |
| [`bigrays`](../Reference_and_Meta/Arrays.md#array-bigrays) | Array  | A two-value array defining the intensity or count of large light rays. | 6 | `[0, 0]`<br>`[1, 1]` |
| [`smallrays`](../Reference_and_Meta/Arrays.md#array-smallrays) | Array  | A two-value array defining the intensity or count of small light rays. | 6 | `[0, 0]`<br>`[1, 2]`<br>`[2, 6]` |
| [`smallray_clip`](../Reference_and_Meta/Enums.md#enum-smallray_clip) | Enum   | Specifies the visual style or clip for small light rays. | 2 | `Bunkerlight`<br>`labligtht` |

</details>


### Object: `Lifted`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `LevelUp`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 3 | `{ . . . }` |

</details>


### Object: `Leave`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |

</details>


### Object: `LeapClose`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `LastHit`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `LargeHouse_Floor2Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `LargeHouse_Floor2Large`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `LargeHouse`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](../Reference_and_Meta/Enums.md#enum-set_house) | Enum   | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

</details>


### Object: `LargeBirdPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`alt_spawn_pool`](../Reference_and_Meta/Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 1 | `{ . . . }` |

</details>


### Object: `LargeAttic`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`id`](../Reference_and_Meta/Enums.md#enum-id) | Enum  | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |
| [`extra_bound_planes`](../Reference_and_Meta/Arrays.md#array-extra_bound_planes) | Array   | A list of additional boundary planes for the room. | 1 | `[` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 0 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 0 | `{ . . . }` |
| [`built_in_collision`](../Reference_and_Meta/Arrays.md#array-built_in_collision) | Array   | A list of collision geometry definitions for the room. | 0 | `[` |

</details>


### Object: `JurassicUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `JunkyardUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](../Reference_and_Meta/Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `Joystick`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `JohnnyNettle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `JohnnyHost`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `JohnnyBubs`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `Johnny`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Jester`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `Jack_Gainaltfurniture`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | String | Specifies a dialog entry or dialog tree to display. | 8 | `NPC_BEANIES_ALSO_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`<br>`NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2` |
| `set_state` | Enum | Specifies the state or flag to set on the character or game system. | 4 | `beanies_intensestatic`<br>`beanies_right`<br>`blocking` |
| `unlock_controls` | Number | The amount of time in seconds before unlocking player controls. | 1 | `1` |
| `lock_controls` | Number | The amount of time in seconds to lock player controls. | 1 | `1` |

</details>


### Object: `Item`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 37 | `2`<br>`3`<br>`4` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 21 | `{ . . . }` |
| `mandatory` | Boolean | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 14 | `1`<br>`3`<br>`6` |
| `weight` | Float | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |

</details>


### Object: `Insane_Ground`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Insane_Ceiling`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `InitialPhase`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `IceAgeUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


### Object: `Ice`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `Hunter`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`complicated_abilities`](../Reference_and_Meta/Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 1 | `[` |
| [`complicated_passives`](../Reference_and_Meta/Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `HummingBird`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `HumanDead`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `House3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](../Reference_and_Meta/Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](../Reference_and_Meta/Enums.md#enum-bg_placements_frame) | Enum   | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](../Reference_and_Meta/Enums.md#enum-movieclip_bg) | Enum   | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](../Reference_and_Meta/Enums.md#enum-movieclip_fg) | Enum   | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](../Reference_and_Meta/Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

</details>


### Object: `House2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](../Reference_and_Meta/Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](../Reference_and_Meta/Enums.md#enum-bg_placements_frame) | Enum   | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](../Reference_and_Meta/Enums.md#enum-movieclip_bg) | Enum   | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](../Reference_and_Meta/Enums.md#enum-movieclip_fg) | Enum   | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](../Reference_and_Meta/Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

</details>


### Object: `House1`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](../Reference_and_Meta/Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](../Reference_and_Meta/Enums.md#enum-bg_placements_frame) | Enum   | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](../Reference_and_Meta/Enums.md#enum-movieclip_bg) | Enum   | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](../Reference_and_Meta/Enums.md#enum-movieclip_fg) | Enum   | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](../Reference_and_Meta/Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | String | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

</details>


### Object: `Holy`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Holding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Hint_CrackedVisuals3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Hint_CrackedVisuals2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Hint_CrackedVisuals`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Health`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `HealRandomInjury`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |

</details>


### Object: `Headless`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `HasRock`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `HasDeadCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `HasCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 5 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 5 | `{ . . . }` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `HarpysClaw`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


### Object: `Harpy`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `HardPathUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](../Reference_and_Meta/Miscellaneous.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |

</details>


### Object: `HalfDead`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Guarding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `GuaranteedJackpot`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Grown`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| `weak_threshold` | Integer | The health threshold below which the unit is considered weakened. | 1 | `0`<br>`1`<br>`15` |

</details>


### Object: `Gravity`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `Grass`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |

</details>


### Object: `GoldenEgg`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `GlowingSeed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `GenFlag_Boss_Stacy`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](../Reference_and_Meta/Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |
| [`miniboss_event`](../Reference_and_Meta/Miscellaneous.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |

</details>


### Object: `GenFlag_Boss_Spewer`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](../Reference_and_Meta/Miscellaneous.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |

</details>


### Object: `FutureUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


### Object: `Full`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`statuses_on_enter_form`](../Reference_and_Meta/Miscellaneous.md#object-statuses_on_enter_form) | Object  | Statuses or abilities applied when entering this form. | 2 | `{ . . . }` |

</details>


### Object: `FreeSpell`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `ForceTrample`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `ForceMoveAway`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean | If true, this option requires no cost to activate. | 1 | `false` |

</details>


### Object: `FoodMove`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `FoodMedium`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


### Object: `FoodBig`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


### Object: `Food`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 4 | `{ . . . }` |
| [`amount`](../Reference_and_Meta/Arrays.md#array-amount) | Array  | For ambient light, the target brightness value (as a float or percentage array for RGB). | 4 | `.1`<br>`.25`<br>`.35` |
| `allow_duplicates` | Boolean | If true, duplicate items of this type can appear in the same shop inventory. | 4 | `true` |
| `weight` | Float | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `Fly`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 7 | `0`<br>`1`<br>`10` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `FlushNettle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `FlushHost`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `FlushBubs`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `Flush`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Flop2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Flop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Floor2_Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |

</details>


### Object: `Floor2_Large`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |

</details>


### Object: `Floor1_Small`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |

</details>


### Object: `Floor1_Large`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum   | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |

</details>


### Object: `FloatingDebris`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


### Object: `FireFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`combo`](../Reference_and_Meta/Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. | 1 | `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |

</details>


### Object: `Firefly`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


### Object: `Fire`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


### Object: `FightPhase`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Fighter`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`shield`](../Reference_and_Meta/Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 1 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`complicated_abilities`](../Reference_and_Meta/Arrays.md#array-complicated_abilities) | Array   | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 1 | `[` |
| [`complicated_passives`](../Reference_and_Meta/Arrays.md#array-complicated_passives) | Array   | An array of passive ability names flagged as complicated. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `Explosive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Explody`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `EvolveAbilityFromPool`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 13 | `2`<br>`3`<br>`4` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 13 | `true` |

</details>


### Object: `Evolution`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `EventBounty`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |

</details>


### Object: `Escape`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `EndOfTimeUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


### Object: `Empty`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `Electric`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `Earth`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


### Object: `Eagle`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `DybbukPossessed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](../Reference_and_Meta/Enums.md#enum-exit_ability) | Enum   | Determines the ability used when the Dybbuk possession ends. | 1 | `DybbukReturn` |
| [`punch_self_ability`](../Reference_and_Meta/Enums.md#enum-punch_self_ability) | Enum   | Determines the ability used for the possessed unit to attack itself. | 1 | `Dybbuk_StopHittingYourself` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Dumb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`keyword_tooltips`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |

</details>


### Object: `DualSword_Primed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |

</details>


### Object: `DualSword`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |

</details>


### Object: `Drunker`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Druid`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`innate_passives`](../Reference_and_Meta/Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. | 1 | `{ . . . }` |

</details>


### Object: `Down`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |

</details>


### Object: `Dove`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `DimensionXUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `Die`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`keyword_tooltips`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |

</details>


### Object: `DesireMech`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `DemonicGlyph_Summon`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Movement`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Fire`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Bounce`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `DemonicGlyph_Bite`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Default_Ground`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Default_Ceiling`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `Default`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 24 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 10 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |
| [`set_house`](../Reference_and_Meta/Enums.md#enum-set_house) | Enum   | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

</details>


### Object: `DeadHummingbird`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


### Object: `DashRandomly`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `Damaged`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `Cultist`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `CraterUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](../Reference_and_Meta/Miscellaneous.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `CoreUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `CoreObeliskUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


### Object: `Conditional_FinishedSpawning`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Imprison`](../Reference_and_Meta/Enums.md#enum-imprison) | Enum  | Specifies the type of unit or object to summon as a prison. | 1 | `BeefyCharmedLeech`<br>`CharmedLeech`<br>`Fly` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


### Object: `Conditional_DoesDamage`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


### Object: `Comfort`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Colorless`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`move_pool`](../Reference_and_Meta/Arrays.md#array-move_pool) | Array   | An array of movement ability names available to the class. | 1 | `[` |
| [`tutorial_levelup_active_pool`](../Reference_and_Meta/Arrays.md#array-tutorial_levelup_active_pool) | Array   | An array of active ability names presented during tutorial level-up. | 1 | `[` |
| [`tutorial_levelup_active_pool_2`](../Reference_and_Meta/Arrays.md#array-tutorial_levelup_active_pool_2) | Array   | An array of active ability names presented in a second tutorial level-up. | 1 | `[` |
| [`tutorial_levelup_passive_pool`](../Reference_and_Meta/Arrays.md#array-tutorial_levelup_passive_pool) | Array   | An array of passive ability names presented during tutorial level-up. | 1 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `Coin4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin10`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Coin`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `Cockroach`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 | `0`<br>`1`<br>`10` |

</details>


### Object: `CloseConvert`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


### Object: `Close`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `Chicken`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


### Object: `Cherub`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedPile`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `CharmedFloater`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `CharmedDip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `Charging`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `CharacterTypeGainsStatusAtBattleStart`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 8 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | Default<br>FormChange<br>Druid |
| [`Else`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |

</details>


### Object: `ChaosAntennaAttached`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


### Object: `CerberubsJumpNormal`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `CerberubsJumpBlind`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum   | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


### Object: `CaveWomanHasCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `CaveWoman`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `CavesUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `CaveManSpear`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `CaveMan`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CaveBaby`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `CatnipBig`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


### Object: `Catnip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |

</details>


### Object: `Catepillar`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Cat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](../Reference_and_Meta/Enums.md#enum-formchange) | Enum  | Specifies the form to change into. | 3 | `BigHolding`<br>`BigHoldingCat`<br>`SmallHolding` |
| [`statuses`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 2 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


### Object: `Butcher`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 2 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `adjectives` | Array | A list of descriptive words used to generate animal names. | 1 | `[` |
| `nouns` | Array | A list of naming words used to generate animal names. | 1 | `[` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array   | An array of ability names available in the class's ability pool. | 1 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array   | An array of attack ability names available in the class's attack pool. | 1 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array   | An array of stat abbreviations that are randomly increased upon leveling up. | 1 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array   | An array of passive ability names available in the class's passive pool. | 1 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 1 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 1 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array   | An array of ability names that the class starts with at level 1. | 1 | `[` |
| [`innate_items`](../Reference_and_Meta/Miscellaneous.md#object-innate_items) | Object  | An object specifying the class's starting equipment, with item slot names as keys. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `BunkerUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `Bully`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


### Object: `BothObelisksUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](../Reference_and_Meta/Miscellaneous.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


### Object: `Boris`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


### Object: `BoneyardUnlocked`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](../Reference_and_Meta/Miscellaneous.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


### Object: `Bomb`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `Blessing`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`intro`](../World_Maps_and_Events/NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 1 | `{ . . . }` |
| [`main`](../Reference_and_Meta/Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 1 | `{ . . . }` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `BlackHole`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BlackBird`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `Bishop`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |

</details>


### Object: `BirdPoopHat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 1 | `+1`<br>`-1`<br>`-2` |
| `cursed` | Boolean | If true, the item is cursed and may have negative effects when equipped or used. | 1 | `true` |

</details>


### Object: `BirdFeed`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |

</details>


### Object: `BigScrap`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `BigHoldingCat`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `BigHolding`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


### Object: `BiggestFood`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `BigFood`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `BigCatnip`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `Big`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`position`](../Reference_and_Meta/Arrays.md#array-position) | Array  | The world-space coordinates for this object. | 2 | `10.5`<br>`[4.5 4.5]` |
| [`follow_character_tag`](../Reference_and_Meta/Enums.md#enum-follow_character_tag) | Enum   | Determines which character this visual effect follows. | 2 | `zaratana` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


### Object: `BellyFull`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `Bear`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `BasementUpgrade5`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `BasementUpgrade`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum  | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum   | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


### Object: `Basement4`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |

</details>


### Object: `Basement3`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |

</details>


### Object: `Basement2`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |

</details>


### Object: `Basement1`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |

</details>


### Object: `Basement0`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Number | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |

</details>


### Object: `BagOfSeeds`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


### Object: `Attraction`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`name_reference_applier`](../Assets_and_Localization/Strings.md#string-name_reference_applier) | String | A localization key for the name displayed to the applier of this status effect. | 1 | `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| [`tooltip_reference_applier`](../Assets_and_Localization/Strings.md#string-tooltip_reference_applier) | String | A localization key for the tooltip description displayed to the applier of this status effect. | 1 | `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |

</details>


### Object: `Attacker`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


### Object: `ApplyPassives`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 13 | `{ . . . }` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 2 | `-.18`<br>`.25`<br>`.35` |

</details>


### Object: `Appeal`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


### Object: `Antidote`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum   | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`durability`](../Reference_and_Meta/Arrays.md#array-durability) | Array / Integer  | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 1 | `1`<br>`2`<br>`true` |
| [`sound`](../Reference_and_Meta/Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 1 | `{ . . . }` |

</details>


### Object: `Angry`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


### Object: `AllyInfested`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum  | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 | `allies`<br>`auto`<br>`birds` |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


### Object: `AllAlive`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |

</details>


### Object: `Alert`


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>

