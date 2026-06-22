# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Cat Classes

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability_pool` | [`Array`](./Arrays.md#array-ability_pool) | `[ ManaBomb SongOfSpring GrantLife SquirrelSquad SummonSqu..., [ HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate Sk..., [ Propell Hadouken Cartwheel StoneFists Transcend HipToss...` |  |
| `attack_pool` | [`Array`](./Arrays.md#array-attack_pool) | `[ BasicDruidAbility ], [ BasicButcherMelee ], [ BasicMonkMelee ]` |  |
| `graphics` | [`Block`](./Cat_Classes.md#context-graphics) | `{ ... }` |  |
| `levelup_stats` | [`Array`](./Arrays.md#array-levelup_stats) | `[ int str lck ], [ cha int str ], [ con str lck ]` |  |
| `meta` | [`Block`](./Cat_Classes.md#context-meta) | `{ ... }` |  |
| `passive_pool` | [`Array`](./Arrays.md#array-passive_pool) | `[ Putrefy NeverFull MainCourse FreshMeat Masochist Glutto..., [ SuperCrow NaturesGuidance PoisonIvy Pathfinder EmptyVes..., [ SafeSwitching Mixup Turnabout MonkeyStyle BrickSkin Jag...` |  |
| `stat_mods` | [`Block`](./Cat_Classes.md#context-stat_mods) | `{ ... }` |  |
| `ability_groups` | [`Block`](./Cat_Classes.md#context-ability_groups) | `{ ... }` |  |
| `starter_abilities` | [`Array`](./Arrays.md#array-starter_abilities) | `[ Propell Pogo ComboThrow ComboPull Bruise Anneal Hadouke..., [ Succ HogRush Chomp BodySlam Vurp Tromp Spoil Grill Shar..., [ SummonSquirrel SummonToad Encourage Protection SongOfSp...` |  |
| `complicated_abilities` | [`Array`](./Arrays.md#array-complicated_abilities) | `[ DealWithTheDevil ForbiddenFlame ForbiddenFlood Forbidde..., [ Extend LastHit StakeOut Diversion ScoutMe CraftArrow Bo..., [ FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooH...` |  |
| `complicated_passives` | [`Array`](./Arrays.md#array-complicated_passives) | `[ ElementalAttunement LatentEnergy MagicGuru One Two Four..., [ Hazardous Traps CatchProjectiles Host SleepDarts Surviv..., [ ShoulderCheck DumbMuscle ThickSkull MostValuableCat Hit...` |  |
| `innate_passives` | [`Block`](./Cat_Classes.md#context-innate_passives) | `{ ... }` |  |
| `innate_items` | [`Block`](./Cat_Classes.md#context-innate_items) | `{ ... }` |  |
| `move_pool` | [`Array`](./Arrays.md#array-move_pool) | `[ DefaultMove ]` |  |
| `tutorial_levelup_active_pool` | [`Array`](./Arrays.md#array-tutorial_levelup_active_pool) | `[ Block LickHeal Dump ]` |  |
| `tutorial_levelup_active_pool_2` | [`Array`](./Arrays.md#array-tutorial_levelup_active_pool_2) | `[ GainThorns ButtScoot Burst HireHitman ]` |  |
| `tutorial_levelup_passive_pool` | [`Array`](./Arrays.md#array-tutorial_levelup_passive_pool) | `[ Furious PressurePoints LateBloomer ZenkaiBoost ]` |  |

</details>

---

### Context: `ability_groups`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Array`](./Arrays.md#array-attack) | `[ SquirrelSquad SummonSquirrel SummonSnake SummonToad Bra..., [ Propell Hadouken HipToss Slapback Finisher ComboThrow C..., [ Fartoom Mutilate SkullBash Shred Chomp BodySlam SliceAn...` |  |
| `misc` | [`Array`](./Arrays.md#array-misc) | `[ SelfMutilate Succ Consume BloodMagic SmellBlood Vurp Li..., [ ManaBomb BattleCry Encourage GrantLife Promote MonkeyFo..., [ StoneFists Bruise TrainArms TrainMind DetectWeakness Ai...` |  |
| `move` | [`Array`](./Arrays.md#array-move) | `[ Cartwheel OneWithTheWind Pogo HopAndBlock TrainLegs Rea..., [ HogRush Trudge LunchTime Tromp CannonBall BadGas Butche..., [ DruidSwap FlowerFeet ThornyFeet RaccoonForm HydroPump C...` |  |
| `defense` | [`Array`](./Arrays.md#array-defense) | `[ Transcend Reverberate Porcupine Anneal DeepDive Meditat..., [ Burp ForceFeed Binge Gib DeliciousScent Tryptophan Regu..., [ SongOfSpring SummonTurtle PullToSafety Protection Safet...` |  |

</details>

---

### Context: `graphics`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alt_animations` | [`Array`](./Arrays.md#array-alt_animations) | `[ [ idle, ButcherIdle ], [ [ idle, DruidIdle ], [ [ idle, MonkIdle ]` |  |
| `palette` | Number | `66, 64, 65` |  |
| `portrait_face` | [`Enum/String`](./Enums.md#enum-portrait_face) | `butcher_portrait, druid_portrait, monk_portrait` |  |
| `default_face` | [`Enum/String`](./Enums.md#enum-default_face) | `happy` |  |
| `hud_palette` | Number | `11` |  |

</details>

---

### Context: `stat_mods`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2, -2, 3` |  |
| `cha` | Number | `2, 3, -1` |  |
| `int` | Number | `2, 1, 4` |  |
| `spd` | Number | `-2, 1, -1` |  |
| `str` | Number | `-2, 2, -1` |  |
| `dex` | Number | `3, -1` |  |
| `lck` | Number | `2, 1, -1` |  |

</details>

---

### Context: `meta`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `description` | String | `"CAT_CLASS_BUTCHER_DESC", "CAT_CLASS_MONK_DESC", "CAT_CLASS_DRUID_DESC"` |  |
| `name` | String | `"CAT_CLASS_DRUID_NAME", "CAT_CLASS_BUTCHER_NAME", "CAT_CLASS_MONK_NAME"` |  |

</details>

---

### Context: `innate_passives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddStartingMana` | Number | `5` |  |
| `MonkStances` | [`Array`](./Arrays.md#array-monkstances) | `[ BasicMonkMelee BasicMonkRanged ]` |  |
| `SpawnOnBattleStart` | [`Enum/String`](./Enums.md#enum-spawnonbattlestart) | `Crow` |  |
| `TinkererBasicAttackSwitching` | [`Block`](./Cat_Classes.md#context-tinkererbasicattackswitching) | `{ ... }` |  |

</details>

---

### Context: `innate_items`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weapon` | [`Enum/String`](./Enums.md#enum-weapon) | `ButcherHook, MonkFist` |  |
| `trinket` | [`Enum/String`](./Enums.md#enum-trinket) | `MonkStyleChanger` |  |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#context-innate_passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `craft_ability` | [`Enum/String`](./Enums.md#enum-craft_ability) | `TinkererCraft` |  |
| `throw_ability` | [`Enum/String`](./Enums.md#enum-throw_ability) | `TinkererThrow` |  |

</details>

---

