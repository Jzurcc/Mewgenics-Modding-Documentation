---
title: "Arrays Schema"
description: "Specialized array formats."
---

# Arrays Schema

## Overview
This schema describes arrays that require a highly specific internal structure beyond just a flat list of items.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
LootTable {
    special_array [ [ "Item1" 50% ] [ "Item2" 50% ] ]
}
```

---

This document provides exhaustive lists of all array properties found in the base game's `.gon` files. 

## Arrays Dictionary


### Array: `image`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`editor`](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-editor), `editor`

**Accepted Elements:**
- List of [Enum: `image`](./Enums.md#enum-image)

**Examples:**
`[ "shadow.png" "cat.png" ]`
`[ "rat.png" ]`
`[ "fly.png" ]`

</details>


---


### Array: `elements`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-dodamage), [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`self_damage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-self_damage), [`splash_damage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-splash_damage), [`MeleeRevengeDamage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-meleerevengedamage), [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties), [`DamageNeighborsAfterMove`](../Core_Entities_and_Combat/Elite_Buffs.md#object-damageneighborsaftermove), [`MeleeRevengeDamage`](../Core_Entities_and_Combat/Elite_Buffs.md#object-meleerevengedamage), [`SolarFlare`](../World_Maps_and_Events/House_and_Environment.md#object-solarflare), [`RevengeDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-revengedamage), [`AddStatusesIfPersistentWeatherElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatusesifpersistentweatherelement), [`AddStatusesToReceivedElementalDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatusestoreceivedelementaldamage), [`DamageNeighborsAfterMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageneighborsaftermove), [`GravityWell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-gravitywell), [`MeleeRevengeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-meleerevengedamage), [`SmiteEnemiesWhoKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-smiteenemieswhokill), [`fire`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-fire), [`ice`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-ice), [`lightning`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lightning), [`triattack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-triattack)

**Accepted Elements:**
- [Enum: `element`](./Enums.md#enum-element)

</details>


---


### Array: `spells`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`abilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilities)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

</details>


---


### Array: `tags`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root), [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties), [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- [Enum: `tags`](./Enums.md#enum-tags)

</details>


---


### Array: `image_tint`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`editor`](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-editor), `editor`

**Accepted Elements:**
- Enum: `image_tint`

</details>


---


### Array: `emit_direction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Array`
  - `Integer` *(inner elements)*

**Examples:**
`[ 0 1 0 ]`
`[ 0 1 0 ]`
`[ 0 -1 0 ]`

</details>


---


### Array: `restrictions`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- [Enum: `restrictions`](./Enums.md#enum-restrictions)

</details>


---


### Array: `tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Accepted Elements:**
- [Enum: `tag`](./Enums.md#enum-tag)

</details>


---


### Array: `do_priority`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bonusturn_pattern), [`fallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fallback), [`mainturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mainturn_pattern), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern), [`round_end_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-round_end_bonusturn_pattern), [`round_start_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-round_start_bonusturn_pattern)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

**Examples:**
`[ *RockToss_BomberRat RockToss_BomberRat ]`
`[ attack Simon_Shot ]`
`[ BumblefootEatCorpse BumblefootEatCat BumblefootBoneShot ]`

</details>


---


### Array: `complete_chapter_with_class`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Accepted Elements:**
- List of [`Enum: class`](./Enums.md#enum-class)

**Examples:**
`[ caves Fighter ]`
`[ caves Hunter ]`
`[ caves Mage ]`

</details>


---


### Array: `set`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Accepted Elements:**
- List of [`Enum: set`](./Enums.md#enum-set)

**Examples:**
`[ Lucky Leafy ]`
`[ Hunter Leather ]`
`[ Psychic Scrap ]`

</details>


---


### Array: `live_bounds`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ -999 999 -999 999 -999 999 ]`
`[ -999 999 -999 999 -999 999 ]`
`[ -999 999 -999 999 -999 999 ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `-.2` | |

</details>


---


### Array: `do_all`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bonusturn_pattern), [`fallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fallback), [`mainturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mainturn_pattern), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern), [`round_end_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-round_end_bonusturn_pattern)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

**Examples:**
`[ attack DustTeleport ]`
`[ attack AlienBeastOpenEyes ]`
`[ *AlienBeastScream *AlienBeastEat *AlienBeastPuke *AlienBeastRampage ]`

</details>


---


### Array: `play_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`outcome`](../World_Maps_and_Events/Events_and_Encounters.md#object-outcome), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Accepted Elements:**
- List of [`Enum: play_animation`](./Enums.md#enum-play_animation)

**Examples:**
`[ resultLeave 0 ]`
`[ resultLeave 0 ]`
`[ resultLeave 0 ]`

</details>


---


### Array: `emit_box`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 10 10 10 0 10 ]`
`[ 0 .4 0 0 0 .4 ]`
`[ 0 10 10 10 0 10 ]`

</details>


---


### Array: `particle_lifetime`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ .1 2 ]`
`[ .1 .5 ]`
`[ 1 2 ]`

</details>


---


### Array: `random_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`outcome`](../World_Maps_and_Events/Events_and_Encounters.md#object-outcome), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block Block Block ]`
`[ Block Block Block ]`
`[ Block Block Block ]`

</details>


---


### Array: `custom_aoe`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- `Array`
  - `Integer` *(coordinate pair: x, y)*

**Examples:**
`[ [ 1 1 ] [ 1 0 ] ]`
`[ [ 1 -1 ] [ 1 0 ] [ 1 1 ] ]`
`[ [ 1 -1 ] [ 1 0 ] [ 1 1 ] ]`

</details>


---


### Array: `Stun`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_enemy), [`TakeBonusTurnWithStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-takebonusturnwithstatus), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustobasicattack), [`AddStatusToElementDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustoelementdamage), [`AddStatusToKnockbackDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustoknockbackdamage), [`effects`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicmeleeattack), [`Conditional_Enemy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_enemy), [`CritsApplyStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-critsapplystatus), [`Electric`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-electric), [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`
`[ 1 .25 ]`
`[ 1 .25 ]`

</details>


---


### Array: `friction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ .1 .1 .1 ]`
`[ .2 .2 .2 ]`
`[ .1 .1 .1 ]`

</details>


---


### Array: `speed_start`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 4 ]`
`[ 8 10 ]`
`[ 0 4 ]`

</details>


---


### Array: `alt_sounds`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Accepted Elements:**
- `Array`
  - [Enum: `sound`](./Enums.md#enum-sound) *(sound ID to replace)*
  - [Enum: `sound`](./Enums.md#enum-sound) *(replacement sound ID)*

**Examples:**
`[ [ SE_BirdSmall_DyingCall SE_BirdDying_Blackbird ] ]`
`[ [ SE_BirdSmall_DyingCall SE_BirdDying_Dove ] ]`
`[ [ SE_BirdSmall_DyingCall SE_BirdDying_Hummingbird ] ]`

</details>


---


### Array: `aoe_restrictions`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- List of [`Enum: aoe_restrictions`](./Enums.md#enum-aoe_restrictions)

**Examples:**
`[ exclude_blocking ]`
`[ must_be_empty ]`
`[ must_be_empty ]`

</details>


---


### Array: `alt_animations`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics), [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics), [`ROOT` (Injuries)](../Player_Progression_and_Cats/Injuries.md#object-root)

**Accepted Elements:**
- `Array`
  - [Enum: `animation`](./Enums.md#enum-animation) *(animation state to replace)*
  - [Enum: `animation`](./Enums.md#enum-animation) *(replacement animation state)*

**Examples:**
`[ [ idle girlyIdle ] ]`
`[ [ idle twitchyIdle ] ]`
`[ [ idle cuteIdle ] ]`

</details>


---


### Array: `rotation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 360 ]`
`[ 0 360 ]`
`[ -10 10 ]`

</details>


---


### Array: `size`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ .3 .8 ]`
`[ .6 .8 ]`
`[ .6 .85 ]`

</details>


---


### Array: `coins`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](../Player_Progression_and_Cats/Combat_Rewards.md#object-boss), [`hard`](../Player_Progression_and_Cats/Combat_Rewards.md#object-hard), [`miniboss`](../Player_Progression_and_Cats/Combat_Rewards.md#object-miniboss), [`normal`](../Player_Progression_and_Cats/Combat_Rewards.md#object-normal)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 6 ]`
`[ 1 6 ]`
`[ 10 20 ]`

</details>


---


### Array: `food`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](../Player_Progression_and_Cats/Combat_Rewards.md#object-boss), [`hard`](../Player_Progression_and_Cats/Combat_Rewards.md#object-hard), [`miniboss`](../Player_Progression_and_Cats/Combat_Rewards.md#object-miniboss), [`normal`](../Player_Progression_and_Cats/Combat_Rewards.md#object-normal)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 3 ]`
`[ 4 7 ]`
`[ 2 5 ]`

</details>


---


### Array: `size_start`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ .1 1 ]`
`[ .2 1.2 ]`
`[ 3 5 ]`

</details>


---


### Array: `banned_elite_buffs`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ Twin ]`
`[ Twin ]`
`[ Twin ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `Twin` | |
| `Shielded1` | |
| `Shielded2` | |
| `Shielded3` | |
| `Shielded4` | |
| `Protected` | |
| `Depressing` | |
| `Mad` | |

</details>


---


### Array: `object`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn), [`TransformInXTurns`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transforminxturns), `ROOT`, [`spawn_unit_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-spawn_unit_next_fight), [`SpawnExtraThingsOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnextrathingsonbattlestart), [`SpawnEachTurn`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawneachturn), [`SpawnEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawneachturn), [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestart)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ CharmedRaptorBaby ]`
`[ Squirrel Turtle Snake Toad Catepillar Crow ]`
`[ TumorousMaggot ChargeyMaggot SwappyMaggot ]`

</details>


---


### Array: `number`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnExtraThingsOnBattleStart`](../Player_Progression_and_Cats/Cat_Mutations.md#object-spawnextrathingsonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](../Player_Progression_and_Cats/Cat_Mutations.md#object-spawnonbattlestartrandomemptytile), [`GlobalSpawnOnRoundEnd`](../World_Maps_and_Events/House_and_Environment.md#object-globalspawnonroundend), [`SpawnExtraThingsOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnextrathingsonbattlestart), [`SpawnVolcanoOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnvolcanoonbattlestart), [`SpawnExtraThingsOnBattleStart`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnextrathingsonbattlestart), [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnonbattlestartrandomemptytile), [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 2 3 ]`
`[ 2 4 ]`
`[ 2 3 ]`

</details>


---


### Array: `durability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 2 4 ]`
`[ 2 4 ]`
`[ 2 6 ]`

</details>


---


### Array: `counter_range`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements), [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Accepted Elements:**
- List of [`Enum: increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter)

**Examples:**
`[ WorldEventLegacyCounter_SealedCrypt 0 0 ]`
`[ WorldEventLegacyCounter_SealedCrypt 1 1 ]`
`[ WorldEventLegacyCounter_SealedCrypt 2 2 ]`

</details>


---


### Array: `gain_coins`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 4 8 ]`
`[ 10 15 ]`
`[ 10 15 ]`

</details>


---


### Array: `color`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CharacterLightSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-characterlightsource), [`ROOT` (Damage_Text_Styles)](../Assets_and_Localization/Damage_Text_Styles.md#object-root)

**Accepted Elements:**
- `Float`

**Examples:**
`[ .3 .7 1 ]`
`[ .3 .7 1 ]`
`[ .8 .9 1 ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `.7` | |
| `.74` | |
| `.9` | |
| `.39` | |
| `.3` | |
| `.71` | |
| `.75` | |
| `.8` | |
| `.10` | |
| `.12` | |
| `.21` | |
| `.43` | |
| `.5` | |
| `.50` | |
| `.76` | |
| `.80` | |
| `.83` | |
| `.18` | |
| `.27` | |
| `.32` | |
| `.37` | |
| `.45` | |
| `.47` | |
| `.54` | |
| `.58` | |
| `.60` | |
| `.63` | |
| `.73` | |
| `.91` | |
| `.94` | |
| `.99` | |

</details>


---


### Array: `EliteTint`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives)

**Accepted Elements:**
- `Float`

**Examples:**
`[ .6 .6 .6 .50 ]`
`[ .4 .4 .4 ]`
`[ .7 .7 1 1 ]`

</details>


---


### Array: `Fear`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_NotBoss`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notboss), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`effects`](../Player_Progression_and_Cats/Cat_Mutations.md#object-effects), [`Else`](../World_Maps_and_Events/House_and_Environment.md#object-else), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustobasicattack), [`effects`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack), [`StatusDamagers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusdamagers), [`StatusEachTurnBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnbegin)

**Accepted Elements:**
- `Integer` *(stacks)*
- `Float` *(chance)*

**Examples:**
`[ 1 .25 ]`
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `force`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 -10 0 ]`
`[ 0 -20 0 ]`
`[ 0 -1 0 ]`

</details>


---


### Array: `rotation_speed_start`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ -900 900 ]`
`[ -1000 1000 ]`
`[ -1000 1000 ]`

</details>


---


### Array: `StatusImmunity`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: status`](./Enums.md#enum-status)

**Examples:**
`[ Fear Madness PermanentMadness ]`
`[ Sleep SleepParalysis ]`
`[ Burn ]`

</details>


---


### Array: `counter_minimum`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements), [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Accepted Elements:**
- List of [`Enum: increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter)

**Examples:**
`[ WorldEventLegacyCounter_CrackInTheWall 4 ]`
`[ WorldEventLegacyCounter_CrackInTheWall 4 ]`
`[ WorldEventLegacyCounter_CrackInTheWall 4 ]`

</details>


---


### Array: `force_start`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 -70 0 ]`
`[ 0 100 0 ]`
`[ 150 70 150 ]`

</details>


---


### Array: `pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DestroyEquipmentAndAttachParasite`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-destroyequipmentandattachparasite), [`PoolMetronome`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-poolmetronome), [`SwapWeapon`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-swapweapon), [`DestroyEquipmentAndAttachParasite`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-destroyequipmentandattachparasite), [`TourettesMeows`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tourettesmeows), [`Item`](../World_Maps_and_Events/Shops.md#object-item)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ Shockwave Ping Telefrag Stasis Reduce Zealot ]`
`[ AmoebaHat AmoebaNeck AmoebaFace ]`
`[ TerminatorShotgun TerminatorSniper TerminatorUzi ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `WaterBottle_Empty` | |
| `FlyHat` | |
| `FlyMask` | |
| `FlyNeck` | |
| `FurnitureBox` | |
| `FurnitureBox_Rare` | |
| `LearnAbility` | |
| `WaterBottle_Full` | |
| `WaterBottle_Half` | |
| `AmoebaFace` | |
| `AmoebaHat` | |
| `AmoebaNeck` | |
| `AncestorsBones` | |
| `AncestorsJaw` | |
| `AncestorsSkull` | |
| `FaceGrub` | |
| `GlowingBone` | |
| `HeadGrub` | |
| `Hiss` | |
| `Hit` | |
| `IrradiatedObject_Bleed` | |
| `IrradiatedObject_Bruise` | |
| `IrradiatedObject_Burn` | |
| `IrradiatedObject_Charmed` | |
| `IrradiatedObject_Confusion` | |
| `IrradiatedObject_Fear` | |
| `IrradiatedObject_Poison` | |
| `IrradiatedObject_Sleep` | |
| `IrradiatedObject_Stun` | |
| `IrradiatedObject_Weakness` | |
| `LargeMeteor` | |
| `LearnPassive` | |
| `MoneyBag_Huge` | |
| `MoneyBag_Large` | |
| `MoneyBag_Medium` | |
| `NeckGrub` | |
| `Normal` | |
| `Ping` | |
| `Reduce` | |
| `Shockwave` | |
| `SmallMeteor` | |
| `Stasis` | |
| `Telefrag` | |
| `TerminatorShotgun` | |
| `TerminatorSniper` | |
| `TerminatorUzi` | |
| `TutorialStick` | |
| `Zealot` | |

</details>


---


### Array: `combo`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- List of Enum: `combo_effect`

**Examples:**
`[ FevaporateLight FevaporateDark ]`
`[ firework_bursta firework_burstb ]`
`[ MegaBlastA MegaBlastB ]`

</details>


---


### Array: `emit_amount`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 3 ]`
`[ 10 100 ]`
`[ 50,100 ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `0,2` | |
| `1,2` | |
| `50,100` | |

</details>


---


### Array: `gain_food`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 5 10 ]`
`[ 1 4 ]`
`[ 1 4 ]`

</details>


---


### Array: `frame_range`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ArmorPickup`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-armorpickup), [`HealthPickup`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-healthpickup), [`ManaPickup`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-manapickup)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 2 ]`
`[ 1 2 ]`
`[ 3 4 ]`

</details>


---


### Array: `get_item_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ CarvingKnife RazorBlade ButterflyKnife ]`
`[ GutsHeart GutsLiver GutsIntestines ]`
`[ MinerHat MinerMask MinerArmor ]`

</details>


---


### Array: `speed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rocket_swirl`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-rocket_swirl), `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1.5 2.5 ]`
`[ .25 1.0 ]`
`[ 1.5 2.5 ]`

</details>


---


### Array: `boss`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: type`](./Enums.md#enum-type)

**Examples:**
`[ boss ]`
`[ boss ]`
`[ boss ]`

</details>


---


### Array: `easy`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: unlock_levelgroup`](./Enums.md#enum-unlock_levelgroup)

**Examples:**
`[ easy ]`
`[ easy ]`
`[ easy ]`

</details>


---


### Array: `hard`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: type`](./Enums.md#enum-type)

**Examples:**
`[ easy ]`
`[ easy ]`
`[ easy ]`

</details>


---


### Array: `miniboss`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: type`](./Enums.md#enum-type)

**Examples:**
`[ miniboss ]`
`[ miniboss ]`
`[ miniboss ]`

</details>


---


### Array: `normal`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of Enum: `event_file`

**Examples:**
`[ common alley_events.gon ]`
`[ common boneyard_events.gon ]`
`[ common bunker_events.gon ]`

</details>


---


### Array: `rare`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: pool`](./Enums.md#enum-pool)

**Examples:**
`[ rare ]`
`[ rare ]`
`[ rare ]`

</details>


---


### Array: `axis`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ParticleTornadoForce`](./Miscellaneous.md#object-particletornadoforce)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 1 0 ]`
`[ 0 1 0 ]`
`[ 0 1 0 ]`

</details>


---


### Array: `counter_maximum`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements), [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Accepted Elements:**
- List of [`Enum: increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter)

**Examples:**
`[ WorldEventLegacyCounter_SealedCrypt 4 ]`
`[ WorldEventLegacyCounter_CrackInTheWall 0 ]`
`[ WorldEventLegacyCounter_CrackInTheWall 3 ]`

</details>


---


### Array: `large`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[  ]`
`[ Shambler ]`
`[ KillDozer ]`

</details>


---


### Array: `lock_orientation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ -1 0 ]`
`[ -1 0 ]`
`[ -1 0 ]`

</details>


---


### Array: `medium`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ Rat Leaper Pooter Kitten TomTom Mangy CatCaller ]`
`[ ZombieCat SkeletonCat TallSkeletonCat WolfCat Tatters Spookie Scary Reaper TallRobes GraveWorm ButtZombie ]`
`[ AtomicKitten RoboTom CatCultist Cultist CultistZealot CultistMutant CultistBishop BishopHat LoveBot SecurityBot Hive FloatingHive ]`

</details>


---


### Array: `point`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ParticleTornadoForce`](./Miscellaneous.md#object-particletornadoforce)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 5 0 5 ]`
`[ 5 0 5 ]`
`[ 0 0 0 ]`

</details>


---


### Array: `small`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- [Enum: `object`](./Enums.md#enum-object)

</details>


---


### Array: `special`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: animation`](./Enums.md#enum-animation)

**Examples:**
`[ special ]`
`[ special ]`
`[ special ]`

</details>


---


### Array: `projectile_spawn_offset`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Accepted Elements:**
- `Float`

**Examples:**
`[ .25 1 ]`
`[ 0 1.5 ]`
`[ 0 1 ]`

</details>


---


### Array: `force_end`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 90 0 ]`
`[ 0 70 0 ]`
`[ 0 70 0 ]`

</details>


---


### Array: `is_not_chapter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Accepted Elements:**
- List of [`Enum: hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit)

**Examples:**
`[ future theend ]`
`[ future theend ]`
`[ jurassic iceage ]`

</details>


---


### Array: `size_end`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ .5 1 ]`
`[ .7 1.3 ]`
`[ 1 2 ]`

</details>


---


### Array: `ReplaceSpawnedObjects`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ Crow2 Crow3 ]`
`[ Crow Crow2 ]`
`[ Crow2 Crow3 ]`

</details>


---


### Array: `damage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 5 10 ]`
`[ 3 6 ]`
`[ 2 4 ]`

</details>


---


### Array: `rotation_speed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ -100 100 ]`
`[ -1000 1000 ]`
`[ -100 100 ]`

</details>


---


### Array: `ability_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Propell Hadouken Cartwheel StoneFists Transcend HipToss Bruise Slapback Finisher Reverberate ComboThrow ComboPull OneWithTheWind Pogo TrainArms Porcupine Anneal DeepDive HopAndBlock TrainMind Meditate DoomPunch KiBurst DragonPunch TrainLegs ReallyFastRun DetectWeakness HundredHandSlap KineticCharge AirBurst TrainBody ReleaseEnergy Pummel QuickAttack PerfectForm WarmupStretch FlyingFist SpiritBomb OnePunch UnbridledHits Kamehameha SideStep UnimpededLunge DoubleDragon FistOfFate Nirvana EmptyMind Position ChargeFists Apprentice ]`
`[ HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate SkullBash Shred Chomp Succ Trudge BodySlam Consume BloodMagic SmellBlood Vurp SliceAndDice LunchTime Tromp LightenTheLoad Crushinator CannonBall Monch DeathWind Spoil Grill Roast BadGas ButcherPurge Binge MyTurn Gib Swallow Track Sharpen FireFart RoughToss TaintedOffering DeliciousScent Cough Reflux Tryptophan HookBind Regurge Grapnel Rehook Contaminate LodgeHook Butcher Chonkwalk ]`
`[ ManaBomb SongOfSpring GrantLife SquirrelSquad SummonSquirrel DruidSwap BattleCry SummonSnake SummonTurtle SummonToad SummonBear PullToSafety BrambleBurst FlowerFeet ThornyFeet Encourage Protection Promote SafetyDance WarCry TigerForm MonkeyForm RhinoForm SummonCatepillar CallTheWind InspirationalSong DeathMetal ChaChaSlide BestowWisdom RaccoonForm SummonCrow WeWillRockYou TreeForm HydroPump ControlPlants ControlWater ControlAir Entangle Lullaby WeAreTheChampions Cheerlead NaturesBlessing ThrowEgg SquirrelForm PlantMushroom Serenade WindyStep ElkForm MockingbirdForm FromTheTrees ]`

</details>


---


### Array: `attack_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- List of [`Enum: attack`](./Enums.md#enum-attack)

**Examples:**
`[ BasicMonkMelee ]`
`[ BasicButcherMelee ]`
`[ BasicDruidAbility ]`

</details>


---


### Array: `count`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MultiSpawnOnDeath`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-multispawnondeath), [`spawn_unit_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-spawn_unit_next_fight), [`SpawnRandomPickupsOnTaggedUnitKilled`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnrandompickupsontaggedunitkilled), [`Cockroach`](./Miscellaneous.md#object-cockroach), [`Firefly`](./Miscellaneous.md#object-firefly), [`Fly`](./Miscellaneous.md#object-fly)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 2 3 ]`
`[ 0 2 ]`
`[ 6 8 ]`

</details>


---


### Array: `levelup_stats`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ int str lck ]`
`[ con str lck ]`
`[ cha int str ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `int` | |
| `cha` | |
| `con` | |
| `dex` | |
| `spd` | |
| `str` | |
| `lck` | |

</details>


---


### Array: `passive_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- Enum: `passive_pool`

</details>


---


### Array: `tint`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 0 0 1 ]`
`[ .7 1 .7 1 ]`
`[ .7 1 .7 1 ]`

</details>


---


### Array: `Freeze`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`MeleeRevengeDamage`](../Player_Progression_and_Cats/Cat_Mutations.md#object-meleerevengedamage), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustobasicattack), [`effects`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack), [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`
`[ 1 .25 ]`

</details>


---


### Array: `ParticleRandomForce`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`scripts`](./Miscellaneous.md#object-scripts), [`scripts`](./Miscellaneous.md#object-scripts)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ 0 [ -20 20 ] 0 ]`
`[ 0 [ 40 80 ] 0 ]`
`[ 0 [ 10 60 ] 0 ]`

</details>


---


### Array: `do_random`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`fallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fallback), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern), [`round_end_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-round_end_bonusturn_pattern)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

**Examples:**
`[ SimonSays_Scatter SimonSays_ComeHere SimonSays_GoAway ]`
`[ Escape attack DybbukReanimate ]`
`[ Escape attack DybbukReanimate DybbukWisps ]`

</details>


---


### Array: `do_strict`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bonusturn_pattern), [`mainturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mainturn_pattern), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

**Examples:**
`[ *WizSpellShield WizBlizzard ]`
`[ WizFlamethrower ]`
`[ WizStorm ]`

</details>


---


### Array: `restrict`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`get_item_from_pool`](../World_Maps_and_Events/Events_and_Encounters.md#object-get_item_from_pool)

**Accepted Elements:**
- [Enum: `restrict`](./Enums.md#enum-restrict)

</details>


---


### Array: `Confusion`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_enemy), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`effects`](../Player_Progression_and_Cats/Cat_Mutations.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .2 ]`
`[ 1 .2 ]`
`[ 1 .2 ]`

</details>


---


### Array: `attack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ability_groups`](../Player_Progression_and_Cats/Cat_Classes.md#object-ability_groups)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Propell Hadouken HipToss Slapback Finisher ComboThrow ComboPull DoomPunch DragonPunch HundredHandSlap ReleaseEnergy Pummel FlyingFist SpiritBomb OnePunch UnbridledHits Kamehameha UnimpededLunge ]`
`[ Fartoom Mutilate SkullBash Shred Chomp BodySlam SliceAndDice Monch DeathWind Roast Swallow FireFart RoughToss Reflux HookBind LodgeHook Butcher ]`
`[ SquirrelSquad SummonSquirrel SummonSnake SummonToad BrambleBurst SummonBear WarCry TigerForm SummonCatepillar DeathMetal ThrowEgg FromTheTrees ]`

</details>


---


### Array: `global_tags`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Accepted Elements:**
- List of Enum: `global_tags`

**Examples:**
`[ all_cats_are_jester ]`
`[ fail_all_events ]`
`[ always_ambushed ]`

</details>


---


### Array: `hint_persistent_elements`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root)

**Accepted Elements:**
- List of [`Enum: AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack)

**Examples:**
`[ Water ]`
`[ Water ]`
`[ Wind ]`

</details>


---


### Array: `misc`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ability_groups`](../Player_Progression_and_Cats/Cat_Classes.md#object-ability_groups)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ StoneFists Bruise TrainArms TrainMind DetectWeakness AirBurst WarmupStretch DoubleDragon EmptyMind ChargeFists Apprentice ]`
`[ SelfMutilate Succ Consume BloodMagic SmellBlood Vurp LightenTheLoad Spoil Grill MyTurn Sharpen Cough Rehook Contaminate ]`
`[ ManaBomb BattleCry Encourage GrantLife Promote MonkeyForm InspirationalSong BestowWisdom SummonCrow ControlPlants WeAreTheChampions Cheerlead SquirrelForm PlantMushroom MockingbirdForm ]`

</details>


---


### Array: `move`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ability_groups`](../Player_Progression_and_Cats/Cat_Classes.md#object-ability_groups)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Cartwheel OneWithTheWind Pogo HopAndBlock TrainLegs ReallyFastRun QuickAttack SideStep FistOfFate Position ]`
`[ HogRush Trudge LunchTime Tromp CannonBall BadGas ButcherPurge Track TaintedOffering Grapnel Chonkwalk ]`
`[ DruidSwap FlowerFeet ThornyFeet RaccoonForm HydroPump ControlAir WindyStep ElkForm ]`

</details>


---


### Array: `starter_abilities`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- [Enum: `do`](./Enums.md#enum-do)

</details>


---


### Array: `Charmed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`effects`](../Player_Progression_and_Cats/Cat_Mutations.md#object-effects), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack), [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1+.02*cha ]`
`[ 1 .1 ]`
`[ 1 .25 ]`

</details>


---


### Array: `EliteFlatTint`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1.1 1.1 1.1 ]`
`[ 1.1 1.1 1.3 ]`
`[ 1.1 1.1 1 ]`

</details>


---


### Array: `Petrify`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`effects`](../Player_Progression_and_Cats/Cat_Mutations.md#object-effects), [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `eq`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DurabilityTransform`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-durabilitytransform)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 JarOfNothing ]`
`[ 1 WaterBottle_Half ]`
`[ 0 WaterBottle_Empty ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `EstusFlask_Half` | |
| `EstusFlask_Empty` | |
| `WaterBottle_Empty` | |
| `WaterBottle_Half` | |
| `JarOfNothing` | |

</details>


---


### Array: `global_particles`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of Enum: `global_particles`

**Examples:**
`[ CaveDrip ]`
`[ CaveDrip ]`
`[ Mist ]`

</details>


---


### Array: `party_damage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 5 10 ]`
`[ 1 6 ]`
`[ 2 6 ]`

</details>


---


### Array: `Immobile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BossOrBig`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_bossorbig), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicmeleeattack)

**Accepted Elements:**
- `Integer` *(stacks)*
- `Float` *(chance)*

**Examples:**
`[ 1 .25 ]`
`[ 1 .25 ]`
`[ 1 .1 ]`

</details>


---


### Array: `defense`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ability_groups`](../Player_Progression_and_Cats/Cat_Classes.md#object-ability_groups)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Transcend Reverberate Porcupine Anneal DeepDive Meditate KiBurst KineticCharge TrainBody PerfectForm Nirvana ]`
`[ Burp ForceFeed Binge Gib DeliciousScent Tryptophan Regurge ]`
`[ SongOfSpring SummonTurtle PullToSafety Protection SafetyDance RhinoForm CallTheWind ChaChaSlide WeWillRockYou TreeForm ControlWater Entangle Lullaby NaturesBlessing Serenade ]`

</details>


---


### Array: `friction_end`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 1 1 ]`
`[ 1 1 1 ]`
`[ .5 .5 .5 ]`

</details>


---


### Array: `complete_act_difficulty`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 0 ]`
`[ 1 1 ]`
`[ 1 2 ]`

</details>


---


### Array: `friction_start`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ .2 .2 .2 ]`
`[ 0 0 0 ]`
`[ .06 .06 .06 ]`

</details>


---


### Array: `initial_cooldown`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 ]`
`[ 3 7 ]`
`[ 3 7 ]`

</details>


---


### Array: `random_delay`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 30 50 ]`
`[ 0 120 ]`
`[ 0 120 ]`

</details>


---


### Array: `rematch_cooldown`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 3 7 ]`
`[ 3 7 ]`
`[ 3 7 ]`

</details>


---


### Array: `tooltip_values`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta)

**Accepted Elements:**
- `Enum`

**Examples:**
`[ "max((X-1)*2, 0)" ]`
`[ "max(X*3, 0)" ]`
`[ "max((X-1)*2, 0)" ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---


### Array: `unlock_act_difficulty`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 1 ]`
`[ 1 2 ]`
`[ 1 3 ]`

</details>


---


### Array: `Poison`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`Else`](../World_Maps_and_Events/House_and_Environment.md#object-else), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .2 ]`
`[ 1 .2 ]`
`[ 1 .1 ]`

</details>


---


### Array: `RandomizeAIWeightsEachTurn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block ]`
`[ Block Block Block Block ]`
`[ Block Block ]`

</details>


---


### Array: `bonus_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `1`, `2`, [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem)

**Examples:**
`[ Eyeball ]`
`[ Pipe ]`
`[ Stick Stick Stick ]`

</details>


---


### Array: `choose_cat_with_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

**Accepted Elements:**
- List of [`Enum: cat_has_item_equipped`](./Enums.md#enum-cat_has_item_equipped)

**Examples:**
`[ CryogenicTimeChamber_Empty JarOfRadiation ]`
`[ PyrophinasCollar ZaratanasCollar ]`
`[ PyrophinasCollar ZaratanasCollar ]`

</details>


---


### Array: `emit_rate`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ .5 1 ]`
`[ 1,5 ]`
`[ .5 5 ]`

</details>


---


### Array: `gain_disorder_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ Psychosis Touched Soulless ]`
`[ Psychosis Pica Vegan ]`
`[ EatingDisorder Pica ]`

</details>


---


### Array: `glow`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CharacterLightSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-characterlightsource)

**Accepted Elements:**
- `Float`

**Examples:**
`[ .3 .7 1 .5 ]`
`[ .7 .8 .9 .5 ]`
`[ 1 1 1 .5 ]`

</details>


---


### Array: `is_chapter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Accepted Elements:**
- List of [`Enum: hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit)

**Examples:**
`[ future ]`
`[ theend ]`
`[ future theend ]`

</details>


---


### Array: `rotation_start`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 360 ]`
`[ 0 360 ]`
`[ 0 360 ]`

</details>


---


### Array: `tile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChangeTile`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-changetile), [`PassiveWhenOnTile`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passivewhenontile)

**Accepted Elements:**
- [Enum: `tile`](./Enums.md#enum-tile)

</details>


---


### Array: `Burn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .25 ]`
`[ 1 .25 ]`
`[ 1 .25 ]`

</details>


---


### Array: `begin`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ParticleRandomForce`](./Miscellaneous.md#object-particlerandomforce)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ 0 -20 0 ]`
`[ 0 -10 0 ]`
`[ 0 -20 0 ]`

</details>


---


### Array: `custom_range`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ [ -2 0 ] [ -2 -1 ] [ -1 -2 ] [ 0 -2 ] [ -1 1 ] [ 0 1 ] [ 1 0 ] [ 1 -1 ] ]`
`[ [ 1 2 ] ]`
`[ [ -2 0 ] [ -2 -1 ] [ -1 -2 ] [ 0 -2 ] [ -1 1 ] [ 0 1 ] [ 1 0 ] [ 1 -1 ] ]`

</details>


---


### Array: `end`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ParticleRandomForce`](./Miscellaneous.md#object-particlerandomforce)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ 0 [ 40 120 ] 0 ]`
`[ 0 [ 200 900 ] 0 ]`
`[ 0 [ 40 120 ] 0 ]`

</details>


---


### Array: `held_coins`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 5 10 ]`
`[ 2 15 ]`
`[ 1 10 ]`

</details>


---


### Array: `hidden_tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Accepted Elements:**
- List of [`Enum: tag`](./Enums.md#enum-tag)

**Examples:**
`[ bird bonusbird ]`
`[ moonhead moonboss ]`
`[ moonhand moonboss ]`

</details>


---


### Array: `shopkeeper_fights`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../World_Maps_and_Events/Shops.md#object-meta)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ test.lvl ]`
`[ test.lvl ]`
`[ test.lvl ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `test.lvl` | |

</details>


---


### Array: `towards`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ParticleAttractor`](./Miscellaneous.md#object-particleattractor)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 5 0 5 ]`
`[ 0 .5 0 ]`
`[ 0 .5 0 ]`

</details>


---


### Array: `Bleed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`Conditional_DoesDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_doesdamage)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .2 ]`
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `areas`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`complete_checkmarks`](./Miscellaneous.md#object-complete_checkmarks)

**Accepted Elements:**
- List of [`Enum: hint_destination`](./Enums.md#enum-hint_destination)

**Examples:**
`[ caves boneyard moon core jurassic theend meatworld dimensionx endoftime ]`
`[ caves boneyard moon core jurassic theend meatworld dimensionx endoftime ]`
`[ caves boneyard moon core jurassic theend meatworld dimensionx endoftime ]`

</details>


---


### Array: `bigrays`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Lighting`](./Miscellaneous.md#object-lighting)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 1 ]`
`[ 0 0 ]`
`[ 0 0 ]`

</details>


---


### Array: `classes`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`complete_checkmarks`](./Miscellaneous.md#object-complete_checkmarks)

**Accepted Elements:**
- List of [`Enum: class`](./Enums.md#enum-class)

**Examples:**
`[ Fighter Hunter Mage Medic Tank Thief Colorless Monk Butcher Druid Tinkerer Necromancer Psychic Jester ]`
`[ Fighter Hunter Mage Medic Tank Thief Colorless Monk Butcher Druid Tinkerer Necromancer Psychic Jester ]`
`[ Fighter Hunter Mage Medic Tank Thief Colorless Monk Butcher Druid Tinkerer Necromancer Psychic Jester ]`

</details>


---


### Array: `complicated_abilities`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooHard Zoomzerk Bloodzerk ExhaustingBlow ChaosRampage MeteorSlam MuscleMemory Huddle BreakingPoint AssertDominance ]`
`[ Extend LastHit StakeOut Diversion ScoutMe CraftArrow BounceShot Vivisect SlopThePigs SpiderInjector PersistentHunt ]`
`[ DealWithTheDevil ForbiddenFlame ForbiddenFlood ForbiddenFulmination Corrupt FireSurge IceSurge LightningSurge Creshendo Divide ForbiddenFrost Teach TriAttack ]`

</details>


---


### Array: `complicated_passives`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- Enum: `passive_pool`

**Examples:**
`[ ShoulderCheck DumbMuscle ThickSkull MostValuableCat HitMe ]`
`[ Hazardous Traps CatchProjectiles Host SleepDarts Survivalist ]`
`[ ElementalAttunement LatentEnergy MagicGuru One Two Four Five ]`

</details>


---


### Array: `custom_aoe_util`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ [ 0 1 ] [ 1 1 ] [ 0 0 ] [ 1 0 ] ]`
`[ [ 1 1 ] [ 1 1 ] [ 1 1 ] [ 1 0 ] [ 1 0 ] [ 1 0 ] ]`
`[ [ -1 1 ] [ 0 1 ] [ 1 1 ] [ -1 -1 ] [ 0 -1 ] [ 1 -1 ] ]`

</details>


---


### Array: `ge`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DurabilityTransform`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-durabilitytransform), [`ItemAuxTransform`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-itemauxtransform)

**Accepted Elements:**
- List of [`Enum: item`](./Enums.md#enum-item)

**Examples:**
`[ 10 NuclearKnife_Glowing ]`
`[ 20 BlackShard_Glowing ]`
`[ 2 WaterBottle_Full ]`

</details>


---


### Array: `head`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`scars`](../Player_Progression_and_Cats/Injuries.md#object-scars)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 23 33 ]`
`[ 23 33 ]`
`[ 15 22 ]`

</details>


---


### Array: `le`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ItemAuxTransform`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-itemauxtransform)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 10 MoneyBag_Small ]`
`[ 10 MoneyBag_Small ]`
`[ 25 MoneyBag_Medium ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `MoneyBag_Small` | |
| `MoneyBag_Medium` | |
| `MoneyBag_Large` | |

</details>


---


### Array: `miss_random_delay`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 20 ]`
`[ 0 60 ]`
`[ 0 60 ]`

</details>


---


### Array: `random_pool_consider_luck`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block Block Block ]`
`[ Block Block Block Block Block Block Block Block Block Block ]`
`[ Block Block Block ]`

</details>


---


### Array: `slot`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`lock_item_slot`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lock_item_slot)

**Accepted Elements:**
- [Enum: `slot`](./Enums.md#enum-slot)

</details>


---


### Array: `smallrays`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Lighting`](./Miscellaneous.md#object-lighting)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 2 ]`
`[ 0 0 ]`
`[ 2 6 ]`

</details>


---


### Array: `Blind`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`effects`](../Player_Progression_and_Cats/Cat_Mutations.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .25 ]`
`[ 2 .33 ]`
`[ 1 .1 ]`

</details>


---


### Array: `Bruise`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .25 ]`
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `ScatterCoins`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusondie)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`
`[ 1 .5 ]`
`[ 1 .5 ]`

</details>


---


### Array: `Slow`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .25 ]`
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `Tangled`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustobasicattack), `GlobalFlowerTrapperAura`

**Accepted Elements:**
- `Integer` *(stacks)*
- `Float` *(chance)*

**Examples:**
`[ 1 .05 ]`
`[ 1 .05 ]`
`[ 1 .05 ]`

</details>


---


### Array: `TriggerWerewolfTransform`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .15 ]`
`[ 1 .5 ]`
`[ 1 .5 ]`

</details>


---


### Array: `do_nothing`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`fallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fallback), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern), [`round_end_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-round_end_bonusturn_pattern)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[  ]`
`[  ]`
`[  ]`

</details>


---


### Array: `get_parasite_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Accepted Elements:**
- List of [Enum: `parasite`](./Enums.md#enum-parasite)

**Examples:**
`[ CrimsonMask_Cursed RedCap_Cursed PoundOfFlesh_Cursed ]`
`[ AmoebaHat AmoebaNeck AmoebaFace ]`
`[ Tapeworm Pinworm Ringworm Heartworm EyeWorm Parousworm Hookworm Roundworm ]`

</details>


---


### Array: `self_damage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 10 ]`
`[ 4 8 ]`
`[ 6 10 ]`

</details>


---


### Array: `Grappled`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .50 ]`
`[ 1 .50 ]`
`[ 1 .50 ]`

</details>


---


### Array: `RandomSeededStatModifier`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 2 -1 ]`
`[ 2 -1 ]`
`[ 2 -1 ]`

</details>


---


### Array: `ScatterHeldCoin`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`
`[ 1 .5 ]`
`[ 1 .5 ]`

</details>


---


### Array: `Weakness`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .25 ]`
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `element`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeonelementinfluence), [`ElementalManaCostReduction`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-elementalmanacostreduction), [`ElementalManaCostReduction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-elementalmanacostreduction)

**Accepted Elements:**
- List of [`Enum: AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack)

**Examples:**
`[ Fire Ice Electric Earth Wind Water Grass Holy Gravity ]`
`[ Holy ]`
`[ Fire Earth ]`

</details>


---


### Array: `inherit_speed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 5 30 ]`
`[ 7 12 ]`
`[ .1 .9 ]`

</details>


---


### Array: `mouse_offset`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- `Float`

**Examples:**
`[ .5 .5 ]`
`[ .5 .5 ]`
`[ .5 .5 ]`

</details>


---


### Array: `particles`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Rain`](../World_Maps_and_Events/House_and_Environment.md#object-rain), [`Snow`](../World_Maps_and_Events/House_and_Environment.md#object-snow), [`Thunderstorm`](../World_Maps_and_Events/House_and_Environment.md#object-thunderstorm), [`Windy`](../World_Maps_and_Events/House_and_Environment.md#object-windy)

**Accepted Elements:**
- List of [`Enum: adventure_weather`](./Enums.md#enum-adventure_weather)

**Examples:**
`[ Rain ]`
`[ Thunderstorm ]`
`[ WindFull ]`

</details>


---


### Array: `radius`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rocket_swirl`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-rocket_swirl)

**Accepted Elements:**
- `Float`

**Examples:**
`[ .5 1 ]`
`[ .25 .5 ]`
`[ .5 1 ]`

</details>


---


### Array: `transform_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Accepted Elements:**
- [Enum: `item`](./Enums.md#enum-item)

</details>


---


### Array: `BonusTurnPattern`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block ]`
`[ Block Block ]`
`[ Block Block ]`

</details>


---


### Array: `ButchBox`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `aux_positions`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 21 0 ]`
`[ 38 0 ]`
`[ 38 0 ]`

</details>


---


### Array: `DivineShield`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTakeHealthOrShieldDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusontakehealthorshielddamage), [`StatusOnTookDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusontookdamage)

**Accepted Elements:**
- Equation: `aoe_chance`

**Examples:**
`[ 1 .33 ]`
`[ 1 .5 ]`
`[ 1 .33 ]`

</details>


---


### Array: `Floor1_Large`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 1 ]`
`[ 1 1 ]`
`[ 1 1 ]`

</details>


---


### Array: `HousePipe`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `aux_positions`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ -2 0 ]`
`[ -2 0 ]`
`[ -2 0 ]`

</details>


---


### Array: `Madness`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`StatusCharactersOnRoundStart`](../World_Maps_and_Events/House_and_Environment.md#object-statuscharactersonroundstart)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`
`[ 1 .25 ]`

</details>


---


### Array: `Quivered`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseachturnbegin), [`AddSelfStatusToBasicAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addselfstatustobasicattack)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .10 ]`
`[ 1 0.1 ]`
`[ 1 0.1 ]`

</details>


---


### Array: `RandomStatDown`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .25 ]`
`[ 1 .25 ]`
`[ 1 .25 ]`

</details>


---


### Array: `Roof_LeftEdge`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `aux_positions`

**Accepted Elements:**
- `Float`

**Examples:**
`[ -3.388 8.138 ]`
`[ -3.617 8.112 ]`
`[ -3.482 16.11 ]`

</details>


---


### Array: `Roof_RightEdge`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `aux_positions`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 21.548 8.175 ]`
`[ 38.518 8.207 ]`
`[ 38.408 16.185 ]`

</details>


---


### Array: `Roof_Top`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `aux_positions`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 8.983 14.4 ]`
`[ 17.563 18.677 ]`
`[ 17.562 26.715 ]`

</details>


---


### Array: `StraySpawn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `aux_positions`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ -3 0 ]`
`[ -3 0 ]`
`[ -3 0 ]`

</details>


---


### Array: `XIsMultipliedPercentHealth`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 12 ]`
`[ 14 1 ]`
`[ 6 2 ]`

</details>


---


### Array: `amount`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`LowerAmbientLight`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-lowerambientlight), [`LowerAmbientLight`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-lowerambientlight)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 50% 60% 60% ]`
`[ 50% 60% 60% ]`
`[ 50% 60% 60% ]`

</details>


---


### Array: `body`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`scars`](../Player_Progression_and_Cats/Injuries.md#object-scars)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 2 9 ]`
`[ 16 25 ]`
`[ 26 30 ]`

</details>


---


### Array: `character_filter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveTowardsKillers`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowardskillers)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ SpiderCat TallSpiderCat ]`
`[ SpiderCat TallSpiderCat ]`
`[ SpiderCat TallSpiderCat ]`

</details>


---


### Array: `complete_chapters`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Accepted Elements:**
- List of [`Enum: hint_destination`](./Enums.md#enum-hint_destination)

**Examples:**
`[ caves boneyard ]`
`[ core moon ]`
`[ caves boneyard ]`

</details>


---


### Array: `innate_weather`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- List of [`Enum: adventure_weather`](./Enums.md#enum-adventure_weather)

**Examples:**
`[ HeatWave ]`
`[ Snow ]`
`[ LowGravity ]`

</details>


---


### Array: `move_then_do_priority`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- List of [`Enum: do`](./Enums.md#enum-do)

**Examples:**
`[ DrinkUp attack ]`
`[ BBPickupCrown *attack *BBToss ]`
`[ BBPickupCrown *BBToss *attack ]`

</details>


---


### Array: `move_then_do_random`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

**Examples:**
`[ ClotEvolveCatCopy ClotFailEvolve ]`
`[ CerberubsJumpBlind CerberubsJumpNormal ]`
`[ ClotEvolve ClotFailEvolve ]`

</details>


---


### Array: `weights`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SetCrazyEyeBackgroundWeights`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-setcrazyeyebackgroundweights)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 0 0 ]`
`[ 0 0 1 ]`
`[ 0 1 0 ]`

</details>


---


### Array: `Basement0`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 -6 ]`
`[ 1 -6 ]`

</details>


---


### Array: `Basement1`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 -12 ]`
`[ 1 -12 ]`

</details>


---


### Array: `Basement2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 -18 ]`
`[ 1 -18 ]`

</details>


---


### Array: `Basement3`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 -24 ]`
`[ 1 -24 ]`

</details>


---


### Array: `Basement4`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 -30 ]`
`[ 1 -30 ]`

</details>


---


### Array: `BounceRock`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .2 ]`
`[ 1 .2 ]`

</details>


---


### Array: `BurgleCoin`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`
`[ 1 .5 ]`

</details>


---


### Array: `CanMutateTo`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ Lumpy Leaper ]`
`[ TumorousMaggot ChargeyMaggot SwappyMaggot ]`

</details>


---


### Array: `Dyslexia`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 3 5 ]`
`[ 6 9 ]`

</details>


---


### Array: `FillMana`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnbegin)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .10 ]`
`[ 1 .25 ]`

</details>


---


### Array: `Floor1_Small`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 18 1 ]`
`[ 18 1 ]`

</details>


---


### Array: `LargeAttic`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 9 ]`
`[ 0 17 ]`

</details>


---


### Array: `MagicWeakness`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `Marked`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `Rot`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `Sleep`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `SpawnFlames`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .20 ]`
`[ 1 .20+.1*level ]`

</details>


---


### Array: `SpawnRock`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .20 ]`
`[ 1 .20 ]`

</details>


---


### Array: `StatusReplacement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: status`](./Enums.md#enum-status)

**Examples:**
`[ Petrify PetrifyCharmed ]`
`[ Petrify PetrifyCharmed ]`

</details>


---


### Array: `Tarred`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`
`[ 1 .1 ]`

</details>


---


### Array: `active_pieces`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChaosBossFormChangeGuide`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chaosbossformchangeguide), [`ChaosBossPieces`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chaosbosspieces)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Johnny Throb Flush ]`
`[ Johnny Throb Flush ]`

</details>


---


### Array: `alpha_start`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 3 ]`
`[ .1 2 ]`

</details>


---


### Array: `built_in_collision`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `LargeAttic`, [`SmallAttic`](../World_Maps_and_Events/House_and_Environment.md#object-smallattic)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ [ 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 6 6 8 8 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 8 7 0 0 7 8 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 8 7 0 0 0 0 0 0 7 8 6 6 6 6 6 ] [ 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 ] [ 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 ] [ 6 8 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 8 6 ] ]`
`[ [ 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 8 7 8 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 8 7 0 0 0 7 8 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6 ] [ 6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6 ] [ 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 ] [ 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 ] [ 6 8 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 8 6 ] ]`

</details>


---


### Array: `do_all_shuffle`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- List of [`Enum: attack`](./Enums.md#enum-attack)

**Examples:**
`[ attack DybbukWisps DybbukRePossess ]`
`[ YetiSlam YetiSlam YetiSlam YetiBite YetiBite YetiBite YetiKick YetiKick YetiKick ]`

</details>


---


### Array: `do_best`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`fallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fallback), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- List of [`Enum: do`](./Enums.md#enum-do)

**Examples:**
`[ JohnnyPush JohnnyPull ]`
`[ Magnetize attack GuillotinaTossCollide YeetTowardsBuddy Tina2Call ]`

</details>


---


### Array: `do_one`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`round_end_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-round_end_bonusturn_pattern)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ **PyrophinaVSWeatherRoar **PyrophinaVSRoar ]`
`[ **ZaratanaVSWeatherRoar **ZaratanaVSRoar ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `**PyrophinaVSRoar` | |
| `**PyrophinaVSWeatherRoar` | |
| `**ZaratanaVSRoar` | |
| `**ZaratanaVSWeatherRoar` | |

</details>


---


### Array: `extra_bound_planes`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `LargeAttic`, [`SmallAttic`](../World_Maps_and_Events/House_and_Environment.md#object-smallattic)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block ]`
`[ Block Block ]`

</details>


---


### Array: `learn_ability_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Smack Meow Hiss ]`
`[ Smack Meow Hiss ]`

</details>


---


### Array: `learn_passive_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Accepted Elements:**
- List of [`Enum: learn_passive`](./Enums.md#enum-learn_passive)

**Examples:**
`[ MiniMe SkillShare ]`
`[ MiniMe SkillShare ]`

</details>


---


### Array: `obj`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnOnDeath`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spawnondeath)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ Spookie Spookie Scary Coin2 Coin3 Coin4 ]`
`[ Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCaller GlassSpitter SpiderCat SharkyCat WolfCat ]`

</details>


---


### Array: `party_gain_disorder_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Accepted Elements:**
- List of [Enum: `disorder`](./Enums.md#enum-disorder)

**Examples:**
`[ Dwarfism ]`
`[ Gigantism ]`

</details>


---


### Array: `passive_pieces`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChaosBossFormChangeGuide`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chaosbossformchangeguide), [`ChaosBossPieces`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chaosbosspieces)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ Host Nettle Bubs ]`
`[ Host Nettle Bubs ]`

</details>


---


### Array: `position`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Big`](../World_Maps_and_Events/House_and_Environment.md#object-big)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 4.5 4.5 ]`
`[ 4.5 4.5 ]`

</details>


---


### Array: `speed_scale`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 1.6 ]`
`[ .05 .1 ]`

</details>


---


### Array: `target_requires_element`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- [Enum: `element`](./Enums.md#enum-element)

</details>


---


### Array: `thresholds`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HPAltStates`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hpaltstates), [`ScalingAttackAnimation`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-scalingattackanimation)

**Accepted Elements:**
- `Array`
  - `Integer` *(threshold value)*
  - [Enum: `movieclip`](./Enums.md#enum-movieclip) *(animation state at threshold)*

**Examples:**
`[ [ 5 bite2 ] [ 10 bite3 ] ]`
`[ [ 1 0 ] [ 0 3 ] ]`

</details>


---


### Array: `AdvancedTint`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- `Float`

**Examples:**
`[ .6 .6 .6 1 .5 .5 .5 0 ]`

</details>


---


### Array: `AlienBeastDangerZones`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

**Examples:**
`[ AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeastRampage ]`

</details>


---


### Array: `AllStatsUp`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_ally)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`

</details>


---


### Array: `BasicAttackPool`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ BasicMelee BasicRanged ]`

</details>


---


### Array: `BasicAttackStatusSwap`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: status`](./Enums.md#enum-status)

**Examples:**
`[ TempDamageUp DamageUp ]`

</details>


---


### Array: `Bird_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BirdHead BirdFeed Feather FeatheredMask FeatheredWing Turkey Chicken BirdPoopHat ]`

</details>


---


### Array: `CatAbilityPool`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ RangedHeal Surf Bolt Fireball Dash Spin FreezeRay MagicMissile ExtraMeleeAttack Block WindSlash ]`

</details>


---


### Array: `CatGenAbilityPool`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Surf Bolt Fireball Dash FreezeRay ExtraMeleeAttack BoostBackstab WindSlash ]`

</details>


---


### Array: `Coin_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BloodyCoin GlowingCoin ElectricCoin CounterfeitCoin LuckyCoin MoneyBag_Small MoneyBag_Medium MoneyBag_Large MoneyBag_Huge RollOfPennies ]`

</details>


---


### Array: `ColorlessAbilities`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ WindSlash ExtraMeleeAttack Block MoveAgain Rest Brace ]`

</details>


---


### Array: `CompletionCheckmarkTooltip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: hint_destination`](./Enums.md#enum-hint_destination)

**Examples:**
`[ meatworld dimensionx endoftime ]`

</details>


---


### Array: `ConstitutionUp`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`

</details>


---


### Array: `CounterAttack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: type`](./Enums.md#enum-type)

**Examples:**
`[ attack GSScream ]`

</details>


---


### Array: `Crazy_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ Rabies PTSD ASRFight ASRFlight BloodFrenzy Anxiety Kamikazee ViolentOutbursts Paranoia Hypomania Cannibal ]`

</details>


---


### Array: `DicerArt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 59 52 65 50 54 63 64 ]`

</details>


---


### Array: `Eye_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ MysteriousEye BlinkingEyeball SmallEye GorgonsEye ConjoinedEye ThirdEye Eyeball WitchsEye ]`

</details>


---


### Array: `Floor2_Large`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 18 9 ]`

</details>


---


### Array: `Floor2_Small`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 9 ]`

</details>


---


### Array: `Forecast`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block Block Block Block Block Block Block Block Block Block Block ]`

</details>


---


### Array: `GainCoins`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbattleend)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 3 5 ]`

</details>


---


### Array: `ImmediateAbilityReaction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ ManglerFumbleEven ManglerFumbleOdd ]`

</details>


---


### Array: `Instakill`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 25 .01 ]`

</details>


---


### Array: `KnockOutCoin`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`

</details>


---


### Array: `LockOrientationFaceTile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 0 ]`

</details>


---


### Array: `MonkStances`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_passives`](../Player_Progression_and_Cats/Cat_Classes.md#object-innate_passives)

**Accepted Elements:**
- List of [`Enum: ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack)

**Examples:**
`[ BasicMonkMelee BasicMonkRanged ]`

</details>


---


### Array: `MoveQuivered`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseachturnbegin)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 0.1 ]`

</details>


---


### Array: `RandomWeatherEachFight`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../World_Maps_and_Events/House_and_Environment.md#object-effects)

**Accepted Elements:**
- List of [`Enum: adventure_weather`](./Enums.md#enum-adventure_weather)

**Examples:**
`[ Fog Rain Windy Sandstorm HeatWave Snow Thunderstorm Blizzard Tornado ]`

</details>


---


### Array: `ReceivedStatusReplacement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: RemoveStatus`](./Enums.md#enum-removestatus)

**Examples:**
`[ Sleep SleepParalysis ]`

</details>


---


### Array: `RemoveGlobalModifiers`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusondie)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ BloodRain ]`

</details>


---


### Array: `RepairWeapon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddSelfStatusToWeapons`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addselfstatustoweapons)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .25 ]`

</details>


---


### Array: `SelfStun`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`

</details>


---


### Array: `SmallAttic`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`room_positions`](../World_Maps_and_Events/House_and_Environment.md#object-room_positions)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 0 9 ]`

</details>


---


### Array: `SmallCompletionCheckmarkTooltip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: hint_destination`](./Enums.md#enum-hint_destination)

**Examples:**
`[ caves boneyard moon core jurassic theend ]`

</details>


---


### Array: `SpawnCoinAnywhere`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .5 ]`

</details>


---


### Array: `Stealth`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnend)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`

</details>


---


### Array: `Steven_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [Enum: `disorder`](./Enums.md#enum-disorder)

**Examples:**
`[ Invincible Paranoia Triskaidekaphobia Autism Bipolar Premonitions Dyslexia Schizophrenia Insomnia ADHD ]`

</details>


---


### Array: `Trample`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveLevelScaledStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivelevelscaledstatus)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 3 X-8 ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `X-8` | |

</details>


---


### Array: `TransformOnDeath`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ Hive FloatingHive ]`

</details>


---


### Array: `VaporizeCorpseFlipAdvantage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Accepted Elements:**
- Equation: `aoe_chance`

**Examples:**
`[ 1 .33 ]`

</details>


---


### Array: `Webbed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 .1 ]`

</details>


---


### Array: `add`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TintItem`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-tintitem)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0.05 0.05 0.05 ]`

</details>


---


### Array: `all_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ Rabies Boils Depression BrokenLimb WrenchedNeck Declawed HeadTrauma DeepCut PuncturedEye OCD Distemper BrainDamage SeveredThumb PTSD IBS Dyskinesia Anemia Empath Infestation Leprosy ASRFight ASRFlight BloodFrenzy Shunned Dysentery Anxiety Kamikazee Traumatophobia StockholmSyndrome ViolentOutbursts GamblingAddict Scleroderma Pacifist Gigachad ImposterSyndrome Vegan FrozenKnee SchrodingerDisorder ScalyScabs FattyLiver CommonCold Pox Psychosis Necrosis Touched Charred Invincible ExplosiveGas Toxoplasmosis Ebola Fidgety Narcolepsy Paranoia EatingDisorder Gastritis Hypomania Hypersomnia KidneyStones Cancer Stinky Incontinence Fossilized Triskaidekaphobia Tourettes SleepParalysis Diabetes Bipolar Soulless Premonitions PillPopper BorrowedTime Brave Scatological Cannibal CrohnsDisease Pica FelineAids Dyslexia Covid Flu BirdFlu Nudist Elephantiasis Sociopathy SkillShare_Disorder Schizophrenia Lycanthropy WobblyCat Singleton Insomnia Phony AcidReflux SpontaneousCombustion TheHunger Paralyzed GlassBones ADHD IntestinalProlapse ]`

</details>


---


### Array: `alley`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Unknown`

**Examples:**
`[  ]`

</details>


---


### Array: `allsticks_0`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererStick TinkererBigStick TinkererBiggestStick TinkererLog ]`

</details>


---


### Array: `allsticks_1`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ TinkererBiggestStick BiggestStick TinkererLog ]`

</details>


---


### Array: `allsticks_2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererBiggestStick TinkererLog ]`

</details>


---


### Array: `allsticks_3`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererLog ]`

</details>


---


### Array: `arms`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`scars`](../Player_Progression_and_Cats/Injuries.md#object-scars)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 10 20 ]`

</details>


---


### Array: `banned_abilities`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Metronome`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-metronome)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine ]`

</details>


---


### Array: `barbed_armor`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BarbedHat BarbedMask BarbedNeck ]`

</details>


---


### Array: `barbed_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BarbedPaw BarbedHat BarbedMask BarbedNeck ]`

</details>


---


### Array: `birth_defects`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [Enum: `disorder`](./Enums.md#enum-disorder)

**Examples:**
`[ Autism Tourettes Narcolepsy Albinism Diabetes Dyslexia Dwarfism PrimordialDwarf WobblyCat GlassBones Anemia SpinaBifida WilliamsSyndrome SavantSyndrome Tachysensia DownsSyndrome Depression OCD Tourettes Bipolar Schizophrenia ADHD ]`

</details>


---


### Array: `blood_altar_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ GutsHeart GutsLiver GutsIntestines SackOfMeat SacredHeart BoneMarrow Stomach LeakyBrain SnaggleTooth BoneMarrow ExtraLimb CatPaw CrimsonMask RedCap PoundOfFlesh LostSoul ]`

</details>


---


### Array: `bloody_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ MeatBomb BloodyStick BucketOfBlood BloodyButterflyKnife BloodyBearTraps BloodyBagOfGlass MeatSlugger BloodyMeatHook BloodySoulClaw BloodBucket BloodySpikes BottlesOfBlood BloodyRazor ]`

</details>


---


### Array: `bombs_0`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ SmallBomb ]`

</details>


---


### Array: `bombs_1`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: projectile`](./Enums.md#enum-projectile)

**Examples:**
`[ Bomb ]`

</details>


---


### Array: `bombs_2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: projectile`](./Enums.md#enum-projectile)

**Examples:**
`[ Bomb ]`

</details>


---


### Array: `bombs_3`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: projectile`](./Enums.md#enum-projectile)

**Examples:**
`[ Bomb ]`

</details>


---


### Array: `bone_armor`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BonesHat BonesMask BonesNeck DryBoneMask DryBoneHat DryBoneNecklace ]`

</details>


---


### Array: `bone_equipment`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BonesHat BonesMask BonesNeck BoneClub Molars VibratingSkull BoneMarrow CatRib HumanLeg DryBoneMask DryBoneHat DryBoneNecklace FingerBone ]`

</details>


---


### Array: `bone_weapons`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: FindItem`](./Enums.md#enum-finditem)

**Examples:**
`[ BoneClub Molars FingerBone ]`

</details>


---


### Array: `boneyard`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ junkyard alley ]`

</details>


---


### Array: `bunker`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ desert ]`

</details>


---


### Array: `can_items_common`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ SixPack ]`

</details>


---


### Array: `can_items_rare`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: unlock_item_immediate`](./Enums.md#enum-unlock_item_immediate)

**Examples:**
`[ TankJuice RageJuice EnergyDrink ]`

</details>


---


### Array: `cat_armor`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ CatHideHat CatHideMask CatHideArmor ]`

</details>


---


### Array: `cat_has_item_equipped`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements)

**Accepted Elements:**
- List of [`Enum: cat_has_item_equipped`](./Enums.md#enum-cat_has_item_equipped)

**Examples:**
`[ FaceCovering InfamousMask ]`

</details>


---


### Array: `caves`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ sewers alley ]`

</details>


---


### Array: `chapter_id_enum`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ debug tutorial alley sewers junkyard caves boneyard meatworld desert crater bunker moon core dimensionx lab iceage future jurassic theend endoftime ]`

</details>


---


### Array: `choose_one`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ GenFlag_Boss_Stacy GenFlag_Boss_Spewer ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `GenFlag_Boss_Spewer` | |
| `GenFlag_Boss_Stacy` | |

</details>


---


### Array: `class_seals`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of Enum: `class_seals`

**Examples:**
`[ FighterSeal HunterSeal TankSeal ClericSeal ThiefSeal MageSeal ColorlessSeal PsychicSeal JesterSeal TinkererSeal ButcherSeal DruidSeal MonkSeal NecromancerSeal ]`

</details>


---


### Array: `common`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of Enum: `event_file`

**Examples:**
`[ dead_body.gon monster.gon misc_events.gon npc_events.gon treasure_box.gon legacy_events.gon ]`

</details>


---


### Array: `common_bones`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: FindItem`](./Enums.md#enum-finditem)

**Examples:**
`[ BonesHat BonesMask BonesNeck BoneClub Molars ]`

</details>


---


### Array: `considered_forms`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mothertumorpassive)

**Accepted Elements:**
- List of [`Enum: FormChange`](./Enums.md#enum-formchange)

**Examples:**
`[ Big BigHolding BigHoldingCat ]`

</details>


---


### Array: `cooldown`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TourettesMeows`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tourettesmeows)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 8 15 ]`

</details>


---


### Array: `core`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ bunker desert ]`

</details>


---


### Array: `crater`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ desert ]`

</details>


---


### Array: `cursed_barbed_wire_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: get_parasite`](./Enums.md#enum-get_parasite)

**Examples:**
`[ FaceShards PawShards Splinters ]`

</details>


---


### Array: `cursed_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: get_parasite`](./Enums.md#enum-get_parasite)

**Examples:**
`[ Splinters BadSplinters SludgeMask SludgeNeck SludgeHat AlluringDoodie ChildSkull CursedHairball PawShards FaceShards ]`

</details>


---


### Array: `custom_aoe_mirror`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ [ 1 0 ] [ 1 0 ] [ 1 0 ] [ 1 0 ] [ 1 0 ] [ 1 0 ] ]`

</details>


---


### Array: `custom_aoe_util_mirror`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ [ 1 1 ] [ 1 0 ] [ 1 1 ] [ 1 0 ] [ 1 1 ] [ 1 0 ] ]`

</details>


---


### Array: `damagescale_thresholds`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Damage_Text_Styles)](../Assets_and_Localization/Damage_Text_Styles.md#object-root)

**Accepted Elements:**
- `Array`
  - `Integer` *(each inner array element)*

**Examples:**
`[ [ 0 damagescale_zero ] [ 1 damagescale_small ] [ 5 damagescale_medium ] [ 10 damagescale_large ] [ 25 damagescale_extreme ] ]`

</details>


---


### Array: `deadcat_equipment`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BonesHat BonesMask BonesNeck BoneClub Molars VibratingSkull BoneMarrow CatRib HumanLeg DryBoneMask DryBoneHat DryBoneNecklace FingerBone BoneClub Molars FingerBone CatHideHat CatHideMask CatHideArmor ]`

</details>


---


### Array: `debug`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Unknown`

**Examples:**
`[  ]`

</details>


---


### Array: `default_unlocked_classes`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: class`](./Enums.md#enum-class)

**Examples:**
`[ Colorless Fighter Hunter Mage Tank ]`

</details>


---


### Array: `demon_themed_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BlackCandle CrownOfHorns ObsidianChunk DemonicHat DemonicMask DemonicNecklace DarkFriend ]`

</details>


---


### Array: `desert`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Unknown`

**Examples:**
`[  ]`

</details>


---


### Array: `dice_abilities`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai)

**Accepted Elements:**
- [Enum: `spells`](./Enums.md#enum-spells)

**Examples:**
`[ D6Fizzle D6Confused D6Poop D6Laser D6Quake D6Storm D6Wrath ]`

</details>


---


### Array: `dimensionx`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ moon core bunker crater desert ]`

</details>


---


### Array: `diseases`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: disease`](./Enums.md#enum-disease)

**Examples:**
`[ Rabies Boils Distemper Infestation IBS Dysentery Scleroderma CommonCold Pox Necrosis Leprosy ExplosiveGas Toxoplasmosis Ebola Gastritis Cancer FelineAids Covid Flu BirdFlu Elephantiasis Lycanthropy ]`

</details>


---


### Array: `do_best_multiple`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ attack spell0 spell1 spell2 spell3 spell4 weapon trinket ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `spell0` | |
| `spell1` | |
| `spell2` | |
| `spell3` | |
| `spell4` | |
| `trinket` | |
| `weapon` | |

</details>


---


### Array: `do_priority_alternating`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ *BadBone *GoodBone BadBone_copy GoodBone_copy BadBone GoodBone ]`

</details>


---


### Array: `eagle_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ Shotgun 22Rifle Uzi RocketLauncher Revolver Sniper Grenade ]`

</details>


---


### Array: `emitshape_scale`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 1 0.5625 ]`

</details>


---


### Array: `endoftime`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ jurassic theend iceage future lab ]`

</details>


---


### Array: `eyes_nonrare`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ SmallEye GorgonsEye Eyeball WitchsEye BlinkingEyeball ConjoinedEye ]`

</details>


---


### Array: `fallback_spawn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`KillEnemyOfTypeAtBattleStart`](../World_Maps_and_Events/Events_and_Encounters.md#object-killenemyoftypeatbattlestart)

**Accepted Elements:**
- List of [`Enum: object`](./Enums.md#enum-object)

**Examples:**
`[ TomTom Kitten CatCaller Mangy ]`

</details>


---


### Array: `flesh_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ PoundOfFlesh HumanFleshMask HumanFleshHat HumanFleshArmor HumanHead HumanHand HumanToe ]`

</details>


---


### Array: `fleshhead_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: get_item`](./Enums.md#enum-get_item)

**Examples:**
`[ PoundOfFlesh HumanFleshMask HumanFleshHat HumanFleshArmor HumanHand HumanBrain MysteriousEye BoneMarrow BlinkingEyeball ConjoinedEye ]`

</details>


---


### Array: `forbidden_spell_consequences`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ Depression Anemia Kamikazee Necrosis PTSD ]`

</details>


---


### Array: `forbidden_spell_consequences_crippling`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [Enum: `disorder`](./Enums.md#enum-disorder)

**Examples:**
`[ Psychosis BorrowedTime Schizophrenia Insomnia TheHunger ]`

</details>


---


### Array: `future`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: hint_destination`](./Enums.md#enum-hint_destination)

**Examples:**
`[ lab ]`

</details>


---


### Array: `get_and_equip_item_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ GutsHeart GutsLiver GutsIntestines ]`

</details>


---


### Array: `glitched_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BarbedScrap LeatherHideMask RecycledGimpMask GemstoneBones CoolRocks MinerImplant RottenGuts PaperRags DirtyBionicArmor LuckyTwine ]`

</details>


---


### Array: `godly_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BlessedHalo HolyTears EyeOfGod TheMind TheBody TheSoul Scapular CrownOfThorns ImmaculateHeart BlessedAnointingOil ]`

</details>


---


### Array: `good_parasites`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `parasite`](./Enums.md#enum-parasite)

**Examples:**
`[ BestBud SoulSucker AngryWorm HealWorm ]`

</details>


---


### Array: `grass_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ BagOfGrass SeedBombs GlowingSeed MagicSeed TwineHat TwineMask TwineArmor LeafyMask LeafyHat LeafyNecklace KiloOfCatnip CatnipBig LuckyMask ]`

</details>


---


### Array: `groups`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TerminatorSkin`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-terminatorskin)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block ]`

</details>


---


### Array: `grub_armor`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ FaceGrub HeadGrub NeckGrub ]`

</details>


---


### Array: `guts_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ GutsHeart GutsLiver GutsIntestines BoneMarrow Stomach LeakyBrain HumanBrain HumanHeart MysteriousEye ]`

</details>


---


### Array: `heal`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 5 10 ]`

</details>


---


### Array: `heal_disorder`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ Anxiety Depression ]`

</details>


---


### Array: `hidden_tags`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Accepted Elements:**
- List of [`Enum: tag_restriction`](./Enums.md#enum-tag_restriction)

**Examples:**
`[ terminator_mini dc_cat ]`

</details>


---


### Array: `hide_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ CatHideHat CatHideMask CatHideArmor ThickHide RatHat RatMask RatNecklace ThickHide ]`

</details>


---


### Array: `iceage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: hint_destination`](./Enums.md#enum-hint_destination)

**Examples:**
`[ lab ]`

</details>


---


### Array: `inanimate_can_receive_specific_statuses`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Accepted Elements:**
- List of [`Enum: status`](./Enums.md#enum-status)

**Examples:**
`[ Burn ]`

</details>


---


### Array: `intro`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ PersuasionDevice ]`

</details>


---


### Array: `isaac_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ Technology D6 RazorBlade Teleport MomsRing ButterBean SacredHeart FetusInAJar Breakfast Ipecac SoyMilk SpoonBender Cancer Wafer ]`

</details>


---


### Array: `junkyard`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter`](./Enums.md#enum-chapter)

**Examples:**
`[ alley ]`

</details>


---


### Array: `junkyard_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ ScrapHat ScrapMask ScrapArmor RubberHat RubberMask RubberArmor BarbedHat BarbedMask BarbedNeck RecycledHat RecycledMask RecycledArmor BagOfChum HumanHead ]`

</details>


---


### Array: `jurassic`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ iceage lab ]`

</details>


---


### Array: `lab`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Unknown`

**Examples:**
`[  ]`

</details>


---


### Array: `legs`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`scars`](../Player_Progression_and_Cats/Injuries.md#object-scars)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 2 9 ]`

</details>


---


### Array: `limbs`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`scars`](../Player_Progression_and_Cats/Injuries.md#object-scars)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 21 31 ]`

</details>


---


### Array: `locked_abilities`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: unlock_ability`](./Enums.md#enum-unlock_ability)

**Examples:**
`[ PathOfTheMage PathOfTheHunter PathOfTheThief PathOfTheFighter PathOfTheTank PathOfTheCleric PathOfTheButcher PathOfThePsychic PathOfTheTinkerer PathOfTheMonk PathOfTheDruid PathOfTheNecromancer PathOfTheJester PathOfTheVoid Pawbreaker BallOfSpiders HyperBeam Ethereal NailFlurry Suplex SummonShade Supernova MechSuit SliceAndDice SummonBear HundredHandSlap Metronome SmartMetronome RNGCannon Bump PowerUp ]`

</details>


---


### Array: `locked_bosses`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: unlock_boss`](./Enums.md#enum-unlock_boss)

**Examples:**
`[ queenhippo jestercat gambit ratking bumblefoot infestedduo ]`

</details>


---


### Array: `locked_items`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: unlock_item_immediate`](./Enums.md#enum-unlock_item_immediate)

**Examples:**
`[ FighterHelm FighterScar FighterShoulderPad BattleAxe RageJuice Steroids HunterCap HunterMonocle HunterQuiver InfinityArrow HuntersFlute BagOfSeeds MageHat MageRobe MageScarf StaffOfFlame RingOfFrost SpellBook ClericHat ClericTears ClericRelic AnointingOil HolyWater PrayerCard ThiefHood ThiefTattoo ThiefCloak LacedNeedle LuckyCoinPurse BagOfBags TankHelmet TankTattoo TankPads Girder TankJuice TankToy SpiderHat DeathMask LeechNecklace UnderworldStaff SatanicBible CambionConception TinfoilHat MysticEye DivinersCloth BentSpoon TarotDeck FriendshipBracelet ScrappersHat ScrappersMask ScrappersBackpack BallPeenHammer ScrapBag Fireworks FleshShroud IronJaw HookedNecklace ButchersCleaver Cookbook SackOfMeat MushroomHat GreenmanMask RingOfMushrooms RainStaff DruidsWhistle TinyCage HeadBrand FaceBrand PrayerBeads Bo EmptyHand TinyPebble CatEars CatWhiskers CatCollar LilKitty BallOfYarn SkillSplit CapAndBells ClownMakeup Ruffle NinnyStick ToyGun JokerCard CopycatHat CopycatMask CopycatScarf TheBoxCardboard TheBoxChest TheBox TheBlackBox MomsKnife ThrobbingCrown CrownOfChaos ChildsCrown TinasBellyButton TinasLarynx TinasFriend PyrophinasToenail ZaratanaTurd ScorchedEarth RoboticArm LiquidMetal HitlersToupe StevensGobbler StevensFartFace StevensShotgun StevensMustache StevensGristle StevensBagofRocks StevensHelmet StevensFriend StevenStone StevenMarrow StevensBottle StevensHat StevenHat1 StevenMask1 StevenNeck1 StevenTrinket1 StevenWeapon1 StevensConsumable1 StevenHat2 StevenMask2 StevenNeck2 StevenTrinket2 StevenWeapon2 StevensConsumable2 ]`

</details>


---


### Array: `locked_levelgroups`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: unlock_levelgroup`](./Enums.md#enum-unlock_levelgroup)

**Examples:**
`[ bigsharklevels ]`

</details>


---


### Array: `locked_passives`


<details>
<summary><b>Expand</b></summary>

**Accepted Elements:**
- List of [`Enum: unlock_passive`](./Enums.md#enum-unlock_passive)

**Examples:**
`[ FightersSoul MagesSoul TanksSoul HuntersSoul ThiefsSoul ClericsSoul NecromancersSoul TinkerersSoul DruidsSoul MonksSoul ButchersSoul PsychicsSoul JestersSoul VoidSoul DualWield ThrillOfTheHunt EnergyStorm EvilPatron AlphaStrike Bouncer DeathIncarnate GravityWell ArmorSpecialist Indigestion SuicideSquad Unstoppable SkillShare SuperLuck Goofball ]`

</details>


---


### Array: `look_at_offset`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossPupils`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbosspupils)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 2.5 0 ]`

</details>


---


### Array: `low_hygeine_in_house_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ Boils Depression OCD PTSD IBS Infestation Leprosy Dysentery Anxiety StockholmSyndrome CommonCold Pox Necrosis ExplosiveGas Toxoplasmosis Paranoia EatingDisorder Gastritis KidneyStones Cancer Stinky Incontinence PillPopper Scatological Cannibal CrohnsDisease Pica Covid Flu BirdFlu AcidReflux ]`

</details>


---


### Array: `lt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ItemAuxTransform`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-itemauxtransform)

**Accepted Elements:**
- List of [`Enum: quest_item_alias`](./Enums.md#enum-quest_item_alias)

**Examples:**
`[ 10 NuclearKnife ]`

</details>


---


### Array: `magic_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ Touched Triskaidekaphobia Soulless Premonitions BorrowedTime TheHunger ]`

</details>


---


### Array: `main_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ ChaosDevice MagicMirror MeStone AngryFace FartFace SpiderInjector PartyDetonator AirHorn TheLoner GlassCannon PrincessHat HardPill BubbleBoy Redacted Stopwatch StorageLocker MysteriousDice ExperimentalTreatment UltraVision3000 NuclearKnife ]`

</details>


---


### Array: `major_class_checkmarks`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: hint_destination`](./Enums.md#enum-hint_destination)

**Examples:**
`[ caves boneyard moon core jurassic theend meatworld dimensionx endoftime ]`

</details>


---


### Array: `meat_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ RottenMeat BagOfMeat GutsHeart GutsLiver GutsIntestines BoneMarrow SackOfMeat ]`

</details>


---


### Array: `meatworld`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ caves boneyard junkyard sewers alley ]`

</details>


---


### Array: `mental_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [Enum: `disorder`](./Enums.md#enum-disorder)

**Examples:**
`[ Depression OCD PTSD Dyskinesia Empath ASRFight ASRFlight BloodFrenzy Shunned BrainDamage Anxiety Traumatophobia StockholmSyndrome ViolentOutbursts GamblingAddict Pacifist ImposterSyndrome Vegan Psychosis Fidgety Narcolepsy Paranoia EatingDisorder Hypomania Hypersomnia Triskaidekaphobia Tourettes SleepParalysis Bipolar Premonitions Brave Scatological Cannibal Pica Dyslexia Nudist Sociopathy SkillShare_Disorder Schizophrenia Lycanthropy Singleton Insomnia Phony ADHD ]`

</details>


---


### Array: `mom_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: get_item`](./Enums.md#enum-get_item)

**Examples:**
`[ MomsRing MomsRing MomsRing MomsRing MangyWig MangyWig MangyWig MomsToeNail MomsKnife ChildSkull ]`

</details>


---


### Array: `moon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ crater desert ]`

</details>


---


### Array: `move_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ DefaultMove ]`

</details>


---


### Array: `move_then_do_all`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

**Accepted Elements:**
- List of [`Enum: attack`](./Enums.md#enum-attack)

**Examples:**
`[ LennyShove LennyGrabDead LennyGrab ]`

</details>


---


### Array: `movieclip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Accepted Elements:**
- List of [Enum: `animation`](./Enums.md#enum-animation)

**Examples:**
`[ TinyTumorA TinyTumorB TinyTumorC ]`

</details>


---


### Array: `mul`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TintItem`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-tintitem)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0.45 0.3 0.25 ]`

</details>


---


### Array: `nemesis`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ nemesis ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `nemesis` | |

</details>


---


### Array: `non_blocking_animations`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Accepted Elements:**
- `Enum`

**Examples:**
`[ "hit" "critical" ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `critical` | |
| `hit` | |

</details>


---


### Array: `options`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddAdvantageToEvent`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addadvantagetoevent)

**Accepted Elements:**
- List of [`Enum: animation`](./Enums.md#enum-animation)

**Examples:**
`[ smash bash open ]`

</details>


---


### Array: `palette`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 54 50 55 52 51 53 66 64 63 65 68 62 ]`

</details>


---


### Array: `parasites`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `parasite`](./Enums.md#enum-parasite)

**Examples:**
`[ Tapeworm Pinworm Ringworm Heartworm BotflyLarva BrainMaggot Cordyceps CymothoaExigua EyeWorm Malaria NaegleriaFowleri Scabies BeanParasite EuhaplorchisCaliforniensis Roundworm SacculinaCarcini Lice Cooties Hookworm Parousworm TheTick ]`

</details>


---


### Array: `pelts`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ CatHideHat CatHideMask CatHideArmor ]`

</details>


---


### Array: `physical_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- List of [`Enum: gain_disorder`](./Enums.md#enum-gain_disorder)

**Examples:**
`[ BrokenLimb WrenchedNeck Declawed HeadTrauma DeepCut PuncturedEye BrainDamage SeveredThumb IBS Dysentery Infestation Kamikazee Scleroderma Gigachad FrozenKnee SchrodingerDisorder ScalyScabs FattyLiver Charred Invincible Gastritis KidneyStones Stinky Incontinence Fossilized SleepParalysis Diabetes CrohnsDisease FelineAids Lycanthropy WobblyCat AcidReflux SpontaneousCombustion Paralyzed GlassBones IntestinalProlapse ]`

</details>


---


### Array: `pills`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ RoidRage SpeedBall BrainCandy DiscoBiscuit Clover Upper Percs ]`

</details>


---


### Array: `poop_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ ColostomyBag MegaPoop PoopHat DoodieMask FecalMask FecalHood FecalNecklace PetrifiedPoop EnchantingPoop ]`

</details>


---


### Array: `puddle_tile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnVolcanoOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnvolcanoonbattlestart)

**Accepted Elements:**
- List of [`Enum: ChangeTile`](./Enums.md#enum-changetile)

**Examples:**
`[ BrambleTile TallBrambleTile ]`

</details>


---


### Array: `raptor_nest_eggs`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- Enum: `raptor_nest_eggs`

</details>


---


### Array: `rat_trinkets`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ RatTail RatHeart RatBeezer RatHat RatMask RatNecklace HybridMask PetrifiedPinky RatBomb ]`

</details>


---


### Array: `recycled_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ RecycledHat RecycledMask RecycledArmor ]`

</details>


---


### Array: `rock_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ MundaneStone MindStone TinyPebble SkillStone Neverstone HeavyRock Geode StoneOrbit StoneHelmet StoneHelmet StoneHelmet StoneHelmet Rocks Rocks Rocks Rocks Rocks BagOfRocks RockHat RockMask RockArmor RockyMask RockyHat RockyNecklace BigRockHat BigRockMask BigRockNecklace ]`

</details>


---


### Array: `rotten_armor`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ RottenHat RottenMask RottenArmor ]`

</details>


---


### Array: `sewers`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter`](./Enums.md#enum-chapter)

**Examples:**
`[ alley ]`

</details>


---


### Array: `sludge_armor`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- Enum: `sludge_armor`

</details>


---


### Array: `spawn_offset`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0 .5 0 ]`

</details>


---


### Array: `speed_end`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Float`

**Examples:**
`[ 0.7 1 ]`

</details>


---


### Array: `spell_use_groups`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`T3HitlerSpawningPhase`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-t3hitlerspawningphase)

**Accepted Elements:**
- `Array`
  - [Enum: `spells`](./Enums.md#enum-spells) *(each inner array element)*

**Examples:**
`[ [ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Tank T3Spawn_Mage T3Spawn_Hunter T3Spawn_Thief T3Spawn_Medic T3Spawn_Fighter T3Spawn_Necromancer T3Spawn_Tinkerer T3Spawn_Butcher T3Spawn_Psychic T3Spawn_Druid T3Spawn_Jester ] [ T3Spawn_Colorless ] [ T3JoinFight ] ]`

</details>


---


### Array: `state_health`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossShieldHealth`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbossshieldhealth)

**Accepted Elements:**
- Enum: `state_health`

</details>


---


### Array: `stats`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `RandomPermanentStatsDistinct`

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 -1 ]`

</details>


---


### Array: `stick_0`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererStick ]`

</details>


---


### Array: `stick_1`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererBigStick ]`

</details>


---


### Array: `stick_2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererBiggestStick ]`

</details>


---


### Array: `stick_3`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererLog ]`

</details>


---


### Array: `stomach_disorders`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Accepted Elements:**
- Enum: `gain_disorder`

</details>


---


### Array: `style`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ShowFakeDamage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-showfakedamage)

**Accepted Elements:**
- `Unknown`

**Examples:**
`[ crit ]`

**All Possible Values:**

| Value | Definition |
| :--- | :--- |
| `crit` | |

</details>


---


### Array: `tech_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ Technology FrankBolts RadarDish RoboArm HappyHelmet VisionPlugin OcularChip CerebralChip SpinalChip BionicHat BionicMask BionicArmor CyborgHat CyborgMask CyborgArmor ]`

</details>


---


### Array: `theend`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- List of [`Enum: chapter_id`](./Enums.md#enum-chapter_id)

**Examples:**
`[ future lab ]`

</details>


---


### Array: `tinkerer_0`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererStick TinkererGlassShard PogoStick SmallBomb TinkererBattery Spitball JankAlloyHat JankAlloyMask JankAlloyArmor ]`

</details>


---


### Array: `tinkerer_0_bombs`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ SmallBomb JankAlloyHat JankAlloyMask JankAlloyArmor ]`

</details>


---


### Array: `tinkerer_1`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererBigStick StunGun MiniJetpack TinkererBottles TinkererSlingShot Bomb AlloyHat AlloyMask AlloyArmor ]`

</details>


---


### Array: `tinkerer_1_bombs`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ Bomb AlloyHat AlloyMask AlloyArmor ]`

</details>


---


### Array: `tinkerer_2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererBiggestStick NailBoard BucketOfAcid TinkererTaser TinkererCrossbow Deathbot AdvancedAlloyHat AdvancedAlloyMask AdvancedAlloyArmor ]`

</details>


---


### Array: `tinkerer_3`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ TinkererLog Shotgun 22Rifle Uzi RocketLauncher TeslaCannon EliteAlloyHat EliteAlloyMask EliteAlloyArmor ]`

</details>


---


### Array: `tracy_idols`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ special_comfortidol special_appealidol special_healthidol special_evolutionidol special_stimulationidol special_fightidol special_suppressoridol ]`

</details>


---


### Array: `turns`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TransformInXTurns`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transforminxturns)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 1 4 ]`

</details>


---


### Array: `tutorial`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Accepted Elements:**
- `Unknown`

**Examples:**
`[  ]`

</details>


---


### Array: `tutorial_levelup_active_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- List of [`Enum: variant_of`](./Enums.md#enum-variant_of)

**Examples:**
`[ Block LickHeal Dump ]`

</details>


---


### Array: `tutorial_levelup_active_pool_2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- [Enum: `do`](./Enums.md#enum-do)

</details>


---


### Array: `tutorial_levelup_passive_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-root)

**Accepted Elements:**
- Enum: `passive_pool`

**Examples:**
`[ Furious PressurePoints LateBloomer ZenkaiBoost ]`

</details>


---


### Array: `type`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTurnEndIfDidntCastAbilityTypes`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes)

**Accepted Elements:**
- [Enum: `type`](./Enums.md#enum-type)

</details>


---


### Array: `unique`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ Shotgun Revolver Sniper 22Rifle RocketLauncher MomsKnife Grenade ]`

</details>


---


### Array: `virtual_head_position`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossPupils`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbosspupils)

**Accepted Elements:**
- `Integer`

**Examples:**
`[ 11 2 11 ]`

</details>


---


### Array: `weapons`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Accepted Elements:**
- List of [Enum: `item`](./Enums.md#enum-item)

**Examples:**
`[ GlassShard RailSpikes NailBoard LilSlugger ChumBucket MeatHook Kebab Pipe ObsidianChunk SoulClaw Bomb BoneClub Molars Whetstone Hairspray Lighter SeedBombs Battery OldHose SixPack IceCubes DryIce Bottles Stick RubberFist BarbedPaw GnarledClaw Garbage Shotgun Revolver Sniper SmallBomb PogoStick Spitball MiniJetpack BigStick BiggestStick Log Taser Deathbot Crossbow BucketOfAcid StunGun SlingShot 22Rifle Uzi BagOfRocks Textbook BucketOfLard NailGun StrongMagnet SawBlades OddRemote ButterflyKnife BearTraps RustyRazor Bricks Mjolnir Blackjack BigSpring Grenade Pinwheel CrispPaper PurpleMushroom BlackMushroom RedMushroom PoisonVial PopCap CreepyPhoto FingerBone SpringBoard Shovel Trowel StaffOfFlame LacedNeedle BattleAxe TractorBeam RollOfPennies GrapplingHook Chainsaw BurningCoal RainbowRemote RubberBat RustedRod MeatCleaver SharpStraw BagOfGlass BagOfMeat BagOfGlitter BagOfStuff Pickaxe RocketLauncher MiniNuke FreyedWires OldExtinguisher TrashCanLid Kandarian Geode Rocks ExtraLimb GripTrainer ShoeHorn Cheese LipFiller EnergyDrink CatPaw FlowerMix PuzzleBox Crowbar FireFlower Bible CarBattery ModelingClay ]`

</details>


---


### Array: `weather`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_ActiveWeather_Any`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_activeweather_any)

**Accepted Elements:**
- Enum: `add_weather`

</details>


---


### Array: `weather_roll`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`outcome`](../World_Maps_and_Events/Events_and_Encounters.md#object-outcome)

**Accepted Elements:**
- `Block`

**Examples:**
`[ Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block Block ]`

</details>


---


### Array: `requires_counter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `prompt`

**Accepted Elements:**
- List of [Enum: `TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer)
- List of `Integer`

**Examples:**
`[ BonusBirdsKilled 25 ]`

</details>


---