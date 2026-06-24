# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Cat Classes

> **Associated Files:** `data/classes/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array | Examples: `[ HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate Sk..., [ Propell Hadou...` | 14 |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array | Examples: `[ BasicButcherMelee ], [ BasicDruidAbility ], [ BasicMonkMelee ]` | 14 |
| [`graphics`](./Cat_Classes.md#context-graphics) | Block | Examples: `{ ... }` | 14 |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array | Examples: `[ int str lck ], [ con str lck ], [ cha int str ]` | 14 |
| [`meta`](./Cat_Classes.md#context-meta) | Block | Examples: `{ ... }` | 14 |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array | Examples: `[ Putrefy NeverFull MainCourse FreshMeat Masochist Glutto..., [ SafeSwitching...` | 14 |
| [`stat_mods`](./Cat_Classes.md#context-stat_mods) | Block | Examples: `{ ... }` | 13 |
| [`ability_groups`](./Cat_Classes.md#context-ability_groups) | Block | Examples: `{ ... }` | 12 |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array | Examples: `[ SummonSquirrel SummonToad Encourage Protection SongOfSp..., [ Succ HogRush ...` | 12 |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array | Examples: `[ FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooH..., [ DealWithTheDe...` | 6 |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array | Examples: `[ ElementalAttunement LatentEnergy MagicGuru One Two Four..., [ ShoulderCheck...` | 6 |
| [`innate_passives`](./Cat_Classes.md#context-innate_passives) | Block | Examples: `{ ... }` | 4 |
| [`innate_items`](./Cat_Classes.md#context-innate_items) | Block | Examples: `{ ... }` | 2 |
| [`move_pool`](./Arrays.md#array-move_pool) | Array | Examples: `[ DefaultMove ]` | 1 |
| [`tutorial_levelup_active_pool_2`](./Arrays.md#array-tutorial_levelup_active_pool_2) | Array | Examples: `[ GainThorns ButtScoot Burst HireHitman ]` | 1 |
| [`tutorial_levelup_active_pool`](./Arrays.md#array-tutorial_levelup_active_pool) | Array | Examples: `[ Block LickHeal Dump ]` | 1 |
| [`tutorial_levelup_passive_pool`](./Arrays.md#array-tutorial_levelup_passive_pool) | Array | Examples: `[ Furious PressurePoints LateBloomer ZenkaiBoost ]` | 1 |

</details>

---

### Context: `graphics`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 14 |
| `palette` | Number |  | 13 |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum |  | 13 |
| [`default_face`](./Enums.md#enum-default_face) | Enum |  | 1 |
| `hud_palette` | Number |  | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2339 |
| [`description`](./Strings.md#string-description) | String | Examples: `"CAT_CLASS_DRUID_DESC", "CAT_CLASS_MONK_DESC", "CAT_CLASS_BUTCHER_DESC"` | 14 |

</details>

---

### Context: `stat_mods`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number | Examples: `3, 2, -2` | 9 |
| `cha` | Number | Examples: `3, 2, -1` | 7 |
| `int` | Number | Examples: `4, 2, 1` | 6 |
| `spd` | Number | Examples: `1, -1, -2` | 6 |
| `str` | Number | Examples: `2, -1, -2` | 6 |
| `dex` | Number | Examples: `3, -1` | 4 |
| `lck` | Number | Examples: `2, -1, 1` | 4 |

</details>

---

### Context: `ability_groups`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Arrays.md#array-attack) | Array | Examples: `[ Fartoom Mutilate SkullBash Shred Chomp BodySlam SliceAn..., [ SquirrelSquad...` | 12 |
| [`misc`](./Arrays.md#array-misc) | Array | Examples: `[ SelfMutilate Succ Consume BloodMagic SmellBlood Vurp Li..., [ StoneFists Br...` | 12 |
| [`move`](./Arrays.md#array-move) | Array | Examples: `[ DruidSwap FlowerFeet ThornyFeet RaccoonForm HydroPump C..., [ HogRush Trudg...` | 12 |
| [`defense`](./Arrays.md#array-defense) | Array | Examples: `[ SongOfSpring SummonTurtle PullToSafety Protection Safet..., [ Burp ForceFee...` | 10 |

</details>

---

### Context: `innate_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`MonkStances`](./Arrays.md#array-monkstances) | Array | Examples: `[ BasicMonkMelee BasicMonkRanged ]` | 1 |

</details>

---

### Context: `innate_items`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Examples: `MonkFist, ButcherHook` | 2 |
| [`trinket`](./Enums.md#enum-trinket) | Enum | Examples: `MonkStyleChanger` | 1 |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#context-innate_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | Examples: `TinkererCraft` | 1 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | Examples: `TinkererThrow` | 1 |

</details>

---

