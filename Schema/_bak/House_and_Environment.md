# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## House & Environment

> **Associated Files:** `data/house.gon, data/house_weather.gon, data/weather.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 59

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`desc`](./Strings.md#string-desc) | String |  | 59 |
| [`name`](./Strings.md#string-name) | String |  | 59 |
| [`effects`](#context-effects) | Block |  | 58 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 13 |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array |  | 12 |
| `height` | Number |  | 8 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 8 |
| `width` | Number |  | 8 |
| [`reverb_empty`](#context-reverb_empty) | Block |  | 7 |
| [`reverb_full`](#context-reverb_full) | Block |  | 7 |
| [`amount`](./Enums.md#enum-amount) | Enum |  | 4 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 4 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 3 |
| [`n`](./Arrays.md#array-n) | Array |  | 2 |
| `volume_adjustment` | Number |  | 2 |
| [`BasementUpgrade`](#context-basementupgrade) | Block |  | 1 |
| [`BasementUpgrade2`](#context-basementupgrade2) | Block |  | 1 |
| [`BasementUpgrade3`](#context-basementupgrade3) | Block |  | 1 |
| [`BasementUpgrade4`](#context-basementupgrade4) | Block |  | 1 |
| [`BasementUpgrade5`](#context-basementupgrade5) | Block |  | 1 |
| [`Default`](#context-default) | Block |  | 1 |
| [`Floor1_Large`](#context-floor1_large) | Block |  | 1 |
| [`Floor1_Small`](#context-floor1_small) | Block |  | 1 |
| [`House1`](#context-house1) | Block |  | 1 |
| [`House2`](#context-house2) | Block |  | 1 |
| [`House3`](#context-house3) | Block |  | 1 |
| [`LargeHouse`](#context-largehouse) | Block |  | 1 |
| [`LargeHouse_Floor2Large`](#context-largehouse_floor2large) | Block |  | 1 |
| [`LargeHouse_Floor2Small`](#context-largehouse_floor2small) | Block |  | 1 |
| [`MediumHouse`](#context-mediumhouse) | Block |  | 1 |
| [`MediumHouse_SmallRoom`](#context-mediumhouse_smallroom) | Block |  | 1 |
| [`Rain`](#context-rain) | Block |  | 1 |
| [`SmallAttic`](#context-smallattic) | Block |  | 1 |
| [`SmallHouse_Attic`](#context-smallhouse_attic) | Block |  | 1 |
| [`Snow`](#context-snow) | Block |  | 1 |
| [`Thunderstorm`](#context-thunderstorm) | Block |  | 1 |
| [`Windy`](#context-windy) | Block |  | 1 |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| [`id`](./Enums.md#enum-id) | Enum |  | 1 |
| [`p`](./Arrays.md#array-p) | Array |  | 1 |

</details>

---

### Context: `effects`

> **Engine Dictionary:** This block accepts dynamic nodes. See [`Engine_LogicBlocks.md`](./Engine_LogicBlocks.md) for the full list of valid nested blocks.

<details>
<summary><b>Expand</b></summary>

**Total Count:** 59

> **Referenced by:** [`ROOT`](#context-root), [`SolarFlare`](#context-solarflare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| [`CharacterTypeGainsStatusAtBattleStart`](#context-charactertypegainsstatusatbattlestart) | Block |  | 2 |
| [`StatusAllCharactersOnSpawn`](#context-statusallcharactersonspawn) | Block |  | 2 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 28

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 27 |
| [`object`](./Arrays.md#array-object) | Enum |  | 19 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 7 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |

</details>

---

### Context: `reverb_empty`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`Floor1_Large`](#context-floor1_large), [`Floor1_Small`](#context-floor1_small), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Enums.md#enum-amount) | Enum |  | 9 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 9 |
| `volume_adjustment` | Number |  | 9 |

</details>

---

### Context: `reverb_full`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`Floor1_Large`](#context-floor1_large), [`Floor1_Small`](#context-floor1_small), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Enums.md#enum-amount) | Enum |  | 9 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 9 |

</details>

---

### Context: `Else`

> **Engine Dictionary:** This block accepts dynamic nodes. See [`Engine_LogicBlocks.md`](./Engine_LogicBlocks.md) for the full list of valid nested blocks.

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](#context-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](#context-statuscharactersonroundstart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `SpawnVolcanoOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| `max_radius` | Number |  | 2 |
| [`min_radius`](./Enums.md#enum-min_radius) | Number |  | 2 |
| [`puddle_tile`](./Enums.md#enum-puddle_tile) | Array |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Context: `StatusCharactersOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Conditional_GoodRoll`](#context-conditional_goodroll) | Block |  | 1 |
| `FloatingRockTrap` | Number |  | 1 |
| `Thorns` | Number |  | 1 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  | 1 |

</details>

---

### Context: `aux_positions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`House1`](#context-house1), [`House2`](#context-house2), [`House3`](#context-house3)

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

### Context: `room_positions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`House1`](#context-house1), [`House2`](#context-house2), [`House3`](#context-house3)

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

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_HasTag`](#context-conditional_hastag), [`Conditional_PartyMember`](#context-conditional_partymember)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`StatusOnBattleEnd`](#context-statusonbattleend) | Block |  | 1 |

</details>

---

### Context: `Big`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`SpecialGodRays`](#context-specialgodrays)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum |  | 2 |
| [`position`](./Arrays.md#array-position) | Array |  | 2 |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `Conditional_Flying` | Block |  | 1 |
| [`Else`](#context-else) | Block |  | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusCharactersOnRoundEnd`](#context-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](#context-statuscharactersonroundstart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`odds`](./Enums.md#enum-odds) | Enum |  | 2 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `GlobalSpawnOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_GoodRoll`](#context-conditional_goodroll), [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `SpecialGodRays`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Big`](#context-big) | Block |  | 2 |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Conditional_Tiny` | Block |  | 1 |
| [`Else`](#context-else) | Block |  | 1 |

</details>

---

### Context: `StatusCharactersOnRoundStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Conditional_GoodRoll`](#context-conditional_goodroll) | Block |  | 1 |
| [`Else`](#context-else) | Block |  | 1 |
| [`Madness`](./Arrays.md#array-madness) | Array |  | 1 |

</details>

---

### Context: `AddPostProcessEffect`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean |  | 1 |
| [`shader`](./Enums.md#enum-shader) | Enum |  | 1 |

</details>

---

### Context: `AddTilesetObjects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FloatingDebris`](#context-floatingdebris) | Block |  | 1 |

</details>

---

### Context: `AllyInfested`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `BasementUpgrade5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_GoodRoll`](#context-conditional_goodroll)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`extra_statuses`](#context-extra_statuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyPassives`](#context-applypassives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusAllCharactersOnSpawn`](#context-statusallcharactersonspawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyPassives`](#context-applypassives) | Block |  | 1 |

</details>

---

### Context: `Default`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `FactionUprising`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`extra_statuses`](#context-extra_statuses) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `FloatingDebris`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddTilesetObjects`](#context-addtilesetobjects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number |  | 1 |

</details>

---

### Context: `Floor1_Large`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `height` | Number |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 1 |
| [`reverb_empty`](#context-reverb_empty) | Block |  | 1 |
| [`reverb_full`](#context-reverb_full) | Block |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `Floor1_Small`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `height` | Number |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 1 |
| [`reverb_empty`](#context-reverb_empty) | Block |  | 1 |
| [`reverb_full`](#context-reverb_full) | Block |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `House1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 1 |
| [`room_positions`](#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum |  | 1 |

</details>

---

### Context: `House2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 1 |
| [`room_positions`](#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum |  | 1 |

</details>

---

### Context: `House3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 1 |
| [`room_positions`](#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum |  | 1 |

</details>

---

### Context: `LargeHouse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 1 |

</details>

---

### Context: `LargeHouse_Floor2Large`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `LargeHouse_Floor2Small`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `MediumHouse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 1 |

</details>

---

### Context: `MediumHouse_SmallRoom`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `Rain`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Context: `SmallAttic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

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

### Context: `SmallHouse_Attic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 1 |

</details>

---

### Context: `Snow`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Context: `SolarFlare`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 1 |
| [`effects`](#context-effects) | Block |  | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `SpawnTilePuddleOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_radius` | Number |  | 1 |
| `min_radius` | Number |  | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 1 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ApplyPassives`](#context-applypassives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Thunderstorm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

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

### Context: `Windy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FactionUprising`](#context-factionuprising)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>
 | `AllStatsUp` | Number |  | 1 | 
 | [`Conditional_HasTag`](./House_and_Environment.md#context-conditional_hastag) | Block |  | 1 | 
 | `HealthGain` | Number |  | 1 | 

---

