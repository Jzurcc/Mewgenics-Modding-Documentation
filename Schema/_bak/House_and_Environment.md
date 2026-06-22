# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## House & Environment

> **Associated Files:** `data/house.gon, data/house_weather.gon, data/weather.gon`


### Context: `ROOT` (59 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 59 |
| [`name`](./Strings.md#string-name) | String |  | 59 |
| [`effects`](./House_and_Environment.md#context-effects) | Block |  | 58 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 13 |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array |  | 12 |
| `height` | Number |  | 8 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 8 |
| `width` | Number |  | 8 |
| [`reverb_empty`](./House_and_Environment.md#context-reverb_empty) | Block |  | 7 |
| [`reverb_full`](./House_and_Environment.md#context-reverb_full) | Block |  | 7 |
| [`amount`](./Enums.md#enum-amount) | Enum |  | 4 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 4 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 3 |
| [`n`](./Arrays.md#array-n) | Array |  | 2 |
| `volume_adjustment` | Number |  | 2 |
| [`BasementUpgrade`](./House_and_Environment.md#context-basementupgrade) | Block |  | 1 |
| [`BasementUpgrade2`](./House_and_Environment.md#context-basementupgrade2) | Block |  | 1 |
| [`BasementUpgrade3`](./House_and_Environment.md#context-basementupgrade3) | Block |  | 1 |
| [`BasementUpgrade4`](./House_and_Environment.md#context-basementupgrade4) | Block |  | 1 |
| [`BasementUpgrade5`](./House_and_Environment.md#context-basementupgrade5) | Block |  | 1 |
| [`Default`](./House_and_Environment.md#context-default) | Block |  | 1 |
| [`Floor1_Large`](./House_and_Environment.md#context-floor1_large) | Block |  | 1 |
| [`Floor1_Small`](./House_and_Environment.md#context-floor1_small) | Block |  | 1 |
| [`House1`](./House_and_Environment.md#context-house1) | Block |  | 1 |
| [`House2`](./House_and_Environment.md#context-house2) | Block |  | 1 |
| [`House3`](./House_and_Environment.md#context-house3) | Block |  | 1 |
| [`LargeHouse`](./House_and_Environment.md#context-largehouse) | Block |  | 1 |
| [`LargeHouse_Floor2Large`](./House_and_Environment.md#context-largehouse_floor2large) | Block |  | 1 |
| [`LargeHouse_Floor2Small`](./House_and_Environment.md#context-largehouse_floor2small) | Block |  | 1 |
| [`MediumHouse`](./House_and_Environment.md#context-mediumhouse) | Block |  | 1 |
| [`MediumHouse_SmallRoom`](./House_and_Environment.md#context-mediumhouse_smallroom) | Block |  | 1 |
| [`Rain`](./House_and_Environment.md#context-rain) | Block |  | 1 |
| [`SmallAttic`](./House_and_Environment.md#context-smallattic) | Block |  | 1 |
| [`SmallHouse_Attic`](./House_and_Environment.md#context-smallhouse_attic) | Block |  | 1 |
| [`Snow`](./House_and_Environment.md#context-snow) | Block |  | 1 |
| [`Thunderstorm`](./House_and_Environment.md#context-thunderstorm) | Block |  | 1 |
| [`Windy`](./House_and_Environment.md#context-windy) | Block |  | 1 |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| [`id`](./Enums.md#enum-id) | Enum |  | 1 |
| [`p`](./Arrays.md#array-p) | Array |  | 1 |

</details>

---

### Context: `effects` (59 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`SolarFlare`](./House_and_Environment.md#context-solarflare)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`CharacterTypeGainsStatusAtBattleStart`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart) | Block |  | 2 |
| [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn) | Block |  | 2 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart` (28 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 27 |
| [`object`](./Arrays.md#array-object) | Array |  | 19 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 7 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |

</details>

---

### Context: `reverb_empty` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Enums.md#enum-amount) | Enum |  | 9 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 9 |
| `volume_adjustment` | Number |  | 9 |

</details>

---

### Context: `reverb_full` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Enums.md#enum-amount) | Enum |  | 9 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 9 |

</details>

---

### Context: `Else` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`RandomStatusFromPool`](./House_and_Environment.md#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `SpawnVolcanoOnBattleStart` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| `max_radius` | Number |  | 2 |
| [`min_radius`](./Enums.md#enum-min_radius) | Enum |  | 2 |
| [`puddle_tile`](./Enums.md#enum-puddle_tile) | Enum |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Context: `StatusCharactersOnRoundEnd` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll) | Block |  | 1 |
| `FloatingRockTrap` | Number |  | 1 |
| `Thorns` | Number |  | 1 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  | 1 |

</details>

---

### Context: `aux_positions` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ButchBox`](./Arrays.md#array-butchbox) | Array |  | 3 |
| [`HousePipe`](./Arrays.md#array-housepipe) | Array |  | 3 |
| [`Roof_LeftEdge`](./Arrays.md#array-roof_leftedge) | Array |  | 3 |
| [`Roof_RightEdge`](./Arrays.md#array-roof_rightedge) | Array |  | 3 |
| [`Roof_Top`](./Arrays.md#array-roof_top) | Array |  | 3 |
| [`StraySpawn`](./Arrays.md#array-strayspawn) | Array |  | 3 |

</details>

---

### Context: `room_positions` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Floor1_Large`](./Arrays.md#array-floor1_large) | Array |  | 3 |
| [`Basement0`](./Arrays.md#array-basement0) | Array |  | 2 |
| [`Basement1`](./Arrays.md#array-basement1) | Array |  | 2 |
| [`Basement2`](./Arrays.md#array-basement2) | Array |  | 2 |
| [`Basement3`](./Arrays.md#array-basement3) | Array |  | 2 |
| [`Basement4`](./Arrays.md#array-basement4) | Array |  | 2 |
| [`Floor1_Small`](./Arrays.md#array-floor1_small) | Array |  | 2 |
| [`LargeAttic`](./Arrays.md#array-largeattic) | Array |  | 2 |
| [`Floor2_Large`](./Arrays.md#array-floor2_large) | Array |  | 1 |
| [`Floor2_Small`](./Arrays.md#array-floor2_small) | Array |  | 1 |
| [`SmallAttic`](./Arrays.md#array-smallattic) | Array |  | 1 |

</details>

---

### Context: `ApplyPassives` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember`](./House_and_Environment.md#context-conditional_partymember)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`StatusOnBattleEnd`](./House_and_Environment.md#context-statusonbattleend) | Block |  | 1 |

</details>

---

### Context: `Big` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpecialGodRays`](./House_and_Environment.md#context-specialgodrays)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum |  | 2 |
| [`position`](./Arrays.md#array-position) | Array |  | 2 |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `Conditional_Flying` | Block |  | 1 |
| [`Else`](./House_and_Environment.md#context-else) | Block |  | 1 |

</details>

---

### Context: `Conditional_GoodRoll` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusCharactersOnRoundEnd`](./House_and_Environment.md#context-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`odds`](./Enums.md#enum-odds) | Enum |  | 2 |
| [`RandomStatusFromPool`](./House_and_Environment.md#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `GlobalSpawnOnRoundEnd` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Context: `RandomStatusFromPool` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll), [`Else`](./House_and_Environment.md#context-else)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `SpecialGodRays` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Big`](./House_and_Environment.md#context-big) | Block |  | 2 |

</details>

---

### Context: `StatusAllCharactersOnSpawn` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| `Conditional_Tiny` | Block |  | 1 |
| [`Else`](./House_and_Environment.md#context-else) | Block |  | 1 |

</details>

---

### Context: `StatusCharactersOnRoundStart` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll) | Block |  | 1 |
| [`Else`](./House_and_Environment.md#context-else) | Block |  | 1 |
| [`Madness`](./Arrays.md#array-madness) | Array |  | 1 |

</details>

---

### Context: `AddPostProcessEffect` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean |  | 1 |
| [`shader`](./Enums.md#enum-shader) | Enum |  | 1 |

</details>

---

### Context: `AddTilesetObjects` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FloatingDebris`](./House_and_Environment.md#context-floatingdebris) | Block |  | 1 |

</details>

---

### Context: `AllyInfested` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./House_and_Environment.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade2` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade3` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade4` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade5` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Corpse` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_HasTag` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`extra_statuses`](./House_and_Environment.md#context-extra_statuses)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`ApplyPassives`](./House_and_Environment.md#context-applypassives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `Conditional_PartyMember` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`ApplyPassives`](./House_and_Environment.md#context-applypassives) | Block |  | 1 |

</details>

---

### Context: `Default` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `FactionUprising` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`extra_statuses`](./House_and_Environment.md#context-extra_statuses) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `FloatingDebris` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTilesetObjects`](./House_and_Environment.md#context-addtilesetobjects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number |  | 1 |

</details>

---

### Context: `Floor1_Large` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `height` | Number |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 1 |
| [`reverb_empty`](./House_and_Environment.md#context-reverb_empty) | Block |  | 1 |
| [`reverb_full`](./House_and_Environment.md#context-reverb_full) | Block |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `Floor1_Small` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `height` | Number |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 1 |
| [`reverb_empty`](./House_and_Environment.md#context-reverb_empty) | Block |  | 1 |
| [`reverb_full`](./House_and_Environment.md#context-reverb_full) | Block |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `House1` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](./House_and_Environment.md#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 1 |
| [`room_positions`](./House_and_Environment.md#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum |  | 1 |

</details>

---

### Context: `House2` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](./House_and_Environment.md#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 1 |
| [`room_positions`](./House_and_Environment.md#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum |  | 1 |

</details>

---

### Context: `House3` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](./House_and_Environment.md#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 1 |
| [`room_positions`](./House_and_Environment.md#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum |  | 1 |

</details>

---

### Context: `LargeHouse` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 1 |

</details>

---

### Context: `LargeHouse_Floor2Large` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `LargeHouse_Floor2Small` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `MediumHouse` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 1 |

</details>

---

### Context: `MediumHouse_SmallRoom` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `Rain` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Context: `SmallAttic` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| `height` | Number |  | 1 |
| [`id`](./Enums.md#enum-id) | Enum |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 1 |
| [`n`](./Arrays.md#array-n) | Array |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `SmallHouse_Attic` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `Snow` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Context: `SolarFlare` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 1 |
| [`effects`](./House_and_Environment.md#context-effects) | Block |  | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `SpawnTilePuddleOnBattleStart` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_radius` | Number |  | 1 |
| `min_radius` | Number |  | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 1 |

</details>

---

### Context: `StatusOnBattleEnd` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./House_and_Environment.md#context-applypassives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `Thunderstorm` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| `lightning_fx` | Boolean |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Context: `Windy` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Context: `extra_statuses` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FactionUprising`](./House_and_Environment.md#context-factionuprising)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

