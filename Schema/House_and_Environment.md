# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 206 |
| [`Default`](#object-default) | Object |  | 199 |
| `height` | Integer |  | 16 |
| [`id`](./Enums.md#enum-id) | Enum |  | 16 |
| [`reverb_empty`](#object-reverb_empty) | Object |  | 16 |
| [`reverb_full`](#object-reverb_full) | Object |  | 16 |
| `width` | Integer |  | 16 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 13 |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array |  | 12 |
| `amount` | Float |  | 8 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 8 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 6 |
| `volume_adjustment` | Float |  | 4 |
| [`BasementUpgrade`](#object-basementupgrade) | Object |  | 2 |
| [`BasementUpgrade2`](#object-basementupgrade2) | Object |  | 2 |
| [`BasementUpgrade3`](#object-basementupgrade3) | Object |  | 2 |
| [`BasementUpgrade4`](#object-basementupgrade4) | Object |  | 2 |
| [`BasementUpgrade5`](#object-basementupgrade5) | Object |  | 2 |
| [`Floor1_Large`](#object-floor1_large) | Object |  | 2 |
| [`Floor1_Small`](#object-floor1_small) | Object |  | 2 |
| [`House1`](#object-house1) | Object |  | 2 |
| [`House2`](#object-house2) | Object |  | 2 |
| [`House3`](#object-house3) | Object |  | 2 |
| [`LargeHouse`](#object-largehouse) | Object |  | 2 |
| [`LargeHouse_Floor2Large`](#object-largehouse_floor2large) | Object |  | 2 |
| [`LargeHouse_Floor2Small`](#object-largehouse_floor2small) | Object |  | 2 |
| [`MediumHouse`](#object-mediumhouse) | Object |  | 2 |
| [`MediumHouse_SmallRoom`](#object-mediumhouse_smallroom) | Object |  | 2 |
| [`n`](./Arrays.md#array-n) | Array |  | 2 |
| [`SmallAttic`](#object-smallattic) | Object |  | 2 |
| [`SmallHouse_Attic`](#object-smallhouse_attic) | Object |  | 2 |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| [`p`](./Arrays.md#array-p) | Array |  | 1 |
| [`Thunderstorm`](#object-thunderstorm) | Object |  | 1 |

</details>

---

### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 2166


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root), [`SolarFlare`](#object-solarflare)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1888 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1390 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 59 |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | Game-state flag identifiers for tracking world progression and event states. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 85


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](#object-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 76 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 72 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 53


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ApplyPassives`](#object-applypassives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 47


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`extra_statuses`](#object-extra_statuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 91 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 63 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 63 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `Default`


**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 38


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 37


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`StatusCharactersOnRoundEnd`](#object-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`odds`](./Math_Equations.md) | Equation |  (Must be float values) | 72 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 40 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 30 |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll), [`Else`](#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 32


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Enum |  | 19 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 7 |
| [`number`](./Arrays.md#array-number) | Array |  | 3 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |

</details>

---

### Object: `ApplyPassives`


**Definition:** Grants the nested passive abilities dynamically.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_HasTag`](#object-conditional_hastag), [`Conditional_PartyMember`](#object-conditional_partymember)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 13 |

</details>

---

### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 10 |
</details>

---

### Object: `reverb_empty`


**Definition:** No definition provided.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Float |  | 18 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 18 |
| `volume_adjustment` | Float |  | 18 |

</details>

---

### Object: `reverb_full`


**Definition:** No definition provided.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Float |  | 18 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 18 |

</details>

---

### Object: `CharacterTypeGainsStatusAtBattleStart`


**Definition:** Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `Rain`


**Definition:** Character Form: Behavior and stats for the 'Rain' state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Integer |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Object: `StatusAllCharactersOnSpawn`


**Definition:** Applies or references the 'StatusAllCharactersOnSpawn' effect/state.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

### Object: `Big`


**Definition:** Character Form / AI State: Behavior and stats for the \'Big\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`SpecialGodRays`](#object-specialgodrays)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum |  | 2 |
| [`position`](./Arrays.md#array-position) | Array |  | 2 |

</details>

---

### Object: `extra_statuses`


**Definition:** Additional generic status applications.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`FactionUprising`](#object-factionuprising)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
 | `AllStatsUp` | Number |  | 1 | 
 | [`Conditional_HasTag`](./House_and_Environment.md#object-conditional_hastag) | Object |  | 1 | 
 | `HealthGain` | Number |  | 1 | 
</details> 

---


<details>
<summary><b>ApplyPassives</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>CharacterTypeGainsStatusAtBattleStart</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>Conditional_Corpse</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 11 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>RandomStatusFromPool</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusAllCharactersOnSpawn</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusCharactersOnRoundEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusCharactersOnRoundStart</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusOnBattleEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>extra_statuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

### Object: `Snow`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Integer |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Object: `aux_positions`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

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


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

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

### Object: `SpawnVolcanoOnBattleStart`


**Definition:** Examples: `{ ... }`  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| `max_radius` | Float |  | 2 |
| [`min_radius`](./Enums.md#enum-min_radius) | Float |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |
| [`puddle_tile`](./Enums.md#enum-puddle_tile) | Array |  | 1 |

</details>

---

### Object: `StatusCharactersOnRoundEnd`


**Definition:** Examples: `{ ... }`  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |

</details>

---

### Object: `Thunderstorm`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| `lightning_fx` | Boolean |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Integer |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Object: `AllyInfested`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Else`](#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Object: `GlobalSpawnOnRoundEnd`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Object: `SolarFlare`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer |  | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `SpecialGodRays`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Big`](#object-big) | Object |  | 2 |

</details>

---

### Object: `StatusCharactersOnRoundStart`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `Windy`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Integer |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum |  | 1 |

</details>

---

### Object: `AddPostProcessEffect`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean |  | 1 |
| [`shader`](./Enums.md#enum-shader) | Enum |  | 1 |

</details>

---

### Object: `AddTilesetObjects`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FloatingDebris`](#object-floatingdebris) | Object |  | 1 |

</details>

---

### Object: `BasementUpgrade`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `BasementUpgrade5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `FactionUprising`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Object: `FloatingDebris`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`AddTilesetObjects`](#object-addtilesetobjects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Integer |  | 1 |

</details>

---

### Object: `Floor1_Large`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `height` | Integer |  | 2 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 2 |
| [`reverb_empty`](#object-reverb_empty) | Object |  | 2 |
| [`reverb_full`](#object-reverb_full) | Object |  | 2 |
| `width` | Integer |  | 2 |

</details>

---

### Object: `Floor1_Small`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `height` | Integer |  | 2 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 2 |
| [`reverb_empty`](#object-reverb_empty) | Object |  | 2 |
| [`reverb_full`](#object-reverb_full) | Object |  | 2 |
| `width` | Integer |  | 2 |

</details>

---

### Object: `House1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

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


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 2 |

</details>

---

### Object: `LargeHouse_Floor2Large`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `LargeHouse_Floor2Small`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `MediumHouse`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`set_house`](./Enums.md#enum-set_house) | Enum |  | 2 |

</details>

---

### Object: `MediumHouse_SmallRoom`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `SmallAttic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `height` | Integer |  | 2 |
| [`id`](./Enums.md#enum-id) | Enum |  | 2 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum |  | 2 |
| `width` | Integer |  | 2 |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| [`n`](./Arrays.md#array-n) | Array |  | 1 |

</details>

---

### Object: `SmallHouse_Attic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum |  | 2 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum |  | 2 |

</details>

---

### Object: `SpawnTilePuddleOnBattleStart`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_radius` | Float |  | 1 |
| `min_radius` | Float |  | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 1 |

</details>

---
