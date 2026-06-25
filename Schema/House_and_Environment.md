# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## House & Environment

> **Associated Files:** `data/house.gon, data/house_weather.gon, data/weather.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 59

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1274 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 199 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 13 |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array |  | 12 |
| `height` | Integer |  | 16 |
| `width` | Integer |  | 16 |
| [`reverb_empty`](#object-reverb_empty) | Object |  | 16 |
| [`reverb_full`](#object-reverb_full) | Object |  | 16 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 8 |
| `amount` | Float |  | 8 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 6 |
| [`n`](./Arrays.md#array-n) | Array |  | 2 |
| `volume_adjustment` | Float |  | 4 |
| [`BasementUpgrade2`](#object-basementupgrade2) | Object |  | 2 |
| [`BasementUpgrade3`](#object-basementupgrade3) | Object |  | 2 |
| [`BasementUpgrade4`](#object-basementupgrade4) | Object |  | 2 |
| [`BasementUpgrade5`](#object-basementupgrade5) | Object |  | 2 |
| [`BasementUpgrade`](#object-basementupgrade) | Object |  | 2 |
| [`Default`](#object-default) | Object |  | 199 |
| [`Floor1_Large`](#object-floor1_large) | Object |  | 2 |
| [`Floor1_Small`](#object-floor1_small) | Object |  | 2 |
| [`House1`](#object-house1) | Object |  | 2 |
| [`House2`](#object-house2) | Object |  | 2 |
| [`House3`](#object-house3) | Object |  | 2 |
| [`LargeHouse_Floor2Large`](#object-largehouse_floor2large) | Object |  | 2 |
| [`LargeHouse_Floor2Small`](#object-largehouse_floor2small) | Object |  | 2 |
| [`LargeHouse`](#object-largehouse) | Object |  | 2 |
| [`MediumHouse_SmallRoom`](#object-mediumhouse_smallroom) | Object |  | 2 |
| [`MediumHouse`](#object-mediumhouse) | Object |  | 2 |
| [`SmallAttic`](#object-smallattic) | Object |  | 2 |
| [`SmallHouse_Attic`](#object-smallhouse_attic) | Object |  | 2 |
| [`Thunderstorm`](#object-thunderstorm) | Object |  | 1 |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| [`id`](./Enums.md#enum-id) | Enum |  | 16 |
| [`p`](./Arrays.md#array-p) | Array |  | 1 |

</details>

---

### Object: `effects`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2166

> **Referenced by:** [`ROOT`](#object-root), [`SolarFlare`](#object-solarflare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1886 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 552 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 59 |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | Game-state flag identifiers for tracking world progression and event states. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 32

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 3 |
| [`object`](./Arrays.md#array-object) | Enum |  | 19 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 7 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |

</details>

---

### Object: `reverb_empty`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 18 |
| `amount` | Float |  | 18 |
| `volume_adjustment` | Float |  | 18 |

</details>

---

### Object: `reverb_full`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 18 |
| `amount` | Float |  | 18 |

</details>

---

### Object: `Else`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 85

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](#object-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 71 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 20 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |

</details>

---

### Object: `SpawnVolcanoOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| [`min_radius`](./Enums.md#enum-min_radius) | Float |  | 2 |
| [`puddle_tile`](./Enums.md#enum-puddle_tile) | Array |  | 1 |
| `max_radius` | Float |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Object: `StatusCharactersOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |

</details>

---

### Object: `aux_positions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`House1`](#object-house1), [`House2`](#object-house2), [`House3`](#object-house3)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ButchBox`](./Arrays.md#array-butchbox) | Array |  | 3 |
| [`HousePipe`](./Arrays.md#array-housepipe) | Array |  | 3 |
| [`Roof_LeftEdge`](./Arrays.md#array-roof_leftedge) | Array |  | 3 |
| [`Roof_RightEdge`](./Arrays.md#array-roof_rightedge) | Array |  | 3 |
| [`Roof_Top`](./Arrays.md#array-roof_top) | Array |  | 3 |
| [`StraySpawn`](./Arrays.md#array-strayspawn) | Array |  | 3 |

</details>

---

### Object: `room_positions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`House1`](#object-house1), [`House2`](#object-house2), [`House3`](#object-house3)

| Key | Type | Definition | Count |
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

### Object: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

> **Referenced by:** [`Conditional_HasTag`](#object-conditional_hastag), [`Conditional_PartyMember`](#object-conditional_partymember)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 13 |

</details>

---

### Object: `Big`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`SpecialGodRays`](#object-specialgodrays)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum |  | 2 |
| [`position`](./Arrays.md#array-position) | Array |  | 2 |

</details>

---

### Object: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 8 |

</details>

---

### Object: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 37

> **Referenced by:** [`StatusCharactersOnRoundEnd`](#object-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 72 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 14 |
| [`odds`](./Math_Equations.md) | Equation |  (Must be float values) | 72 |

</details>

---

### Object: `GlobalSpawnOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Object: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 35

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll), [`Else`](#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `SpecialGodRays`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Big`](#object-big) | Object |  | 2 |

</details>

---

### Object: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `StatusCharactersOnRoundStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddPostProcessEffect`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`shader`](./Enums.md#enum-shader) | Enum |  | 1 |
| `requires_framebuffer` | Boolean |  | 1 |

</details>

---

### Object: `AddTilesetObjects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FloatingDebris`](#object-floatingdebris) | Object |  | 1 |

</details>

---

### Object: `AllyInfested`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Else`](#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Object: `BasementUpgrade`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 10 |
</details>

---

### Object: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 47

> **Referenced by:** [`extra_statuses`](#object-extra_statuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 91 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 91 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 91 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `Default`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 38

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `FactionUprising`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Object: `FloatingDebris`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddTilesetObjects`](#object-addtilesetobjects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Integer |  | 1 |

</details>

---

### Object: `Floor1_Large`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 2 |
| [`reverb_empty`](#object-reverb_empty) | Object |  | 2 |
| [`reverb_full`](#object-reverb_full) | Object |  | 2 |
| `height` | Integer |  | 2 |
| `width` | Integer |  | 2 |

</details>

---

### Object: `Floor1_Small`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 2 |
| [`reverb_empty`](#object-reverb_empty) | Object |  | 2 |
| [`reverb_full`](#object-reverb_full) | Object |  | 2 |
| `height` | Integer |  | 2 |
| `width` | Integer |  | 2 |

</details>

---

### Object: `House1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](#object-aux_positions) | Object |  | 2 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 2 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 2 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 2 |
| [`room_positions`](#object-room_positions) | Object |  | 2 |
| `zoomout_catvolume` | Float |  | 2 |

</details>

---

### Object: `House2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](#object-aux_positions) | Object |  | 2 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 2 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 2 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 2 |
| [`room_positions`](#object-room_positions) | Object |  | 2 |
| `zoomout_catvolume` | Float |  | 2 |

</details>

---

### Object: `House3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](#object-aux_positions) | Object |  | 2 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum |  | 2 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum |  | 2 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum |  | 2 |
| [`room_positions`](#object-room_positions) | Object |  | 2 |
| `zoomout_catvolume` | Float |  | 2 |

</details>

---

### Object: `LargeHouse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 2 |

</details>

---

### Object: `LargeHouse_Floor2Large`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `LargeHouse_Floor2Small`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `MediumHouse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 2 |

</details>

---

### Object: `MediumHouse_SmallRoom`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `Rain`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |
| `prewarm` | Integer |  | 1 |

</details>

---

### Object: `SmallAttic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| [`id`](./Enums.md#enum-id) | Enum |  | 2 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 2 |
| [`n`](./Arrays.md#array-n) | Array |  | 1 |
| `height` | Integer |  | 2 |
| `width` | Integer |  | 2 |

</details>

---

### Object: `SmallHouse_Attic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `Snow`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |
| `prewarm` | Integer |  | 1 |

</details>

---

### Object: `SolarFlare`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |
| `damage` | Integer |  | 1 |

</details>

---

### Object: `SpawnTilePuddleOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 1 |
| `max_radius` | Float |  | 1 |
| `min_radius` | Float |  | 1 |

</details>

---

### Object: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 53

> **Referenced by:** [`ApplyPassives`](#object-applypassives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `Thunderstorm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |
| `lightning_fx` | Boolean |  | 1 |
| `prewarm` | Integer |  | 1 |

</details>

---

### Object: `Windy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |
| `prewarm` | Integer |  | 1 |

</details>

---

### Object: `extra_statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`FactionUprising`](#object-factionuprising)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
 | `AllStatsUp` | Number |  | 1 | 
 | [`Conditional_HasTag`](./House_and_Environment.md#object-conditional_hastag) | Object |  | 1 | 
 | `HealthGain` | Number |  | 1 | 
</details> 

---

