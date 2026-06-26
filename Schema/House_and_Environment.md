# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## House & Environment

> **Associated Files:** `data/house.gon, data/house_weather.gon, data/weather.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 59

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2731 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 291 |  |
| [`id`](./Enums.md#enum-id) | Enum | Specifies the unique identifier for the object or room, used for referencing or categorization. | 14 ||
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather event. | 13 ||
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array | An array of element types that persist as hints during this weather (e.g., [Ice Wind]). | 12 ||
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 8 ||
| [`reverb_empty`](#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. | 8 ||
| [`reverb_full`](#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. | 8 ||
| `width` | Integer | The width of the room in grid tiles. | 8 ||
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame name used for interstitial room transition screens. | 3 ||
| `amount` | Float | A scalar value for the strength or intensity of an ambient effect, or a percentage range. | 2 ||
| [`preset`](./Enums.md#enum-preset) | Enum || 2 ||
| [`n`](./Arrays.md#array-n) | Array || 2 ||
| [`Default`](Characters_and_Bosses.md#object-default) | Enum / Object || 1 ||
| `volume_adjustment` | Float || 1 ||
| [`BasementUpgrade`](Engine_LogicKeys.md#object-basementupgrade) | Object || 1 ||
| [`BasementUpgrade2`](Engine_LogicKeys.md#object-basementupgrade2) | Object || 1 ||
| [`BasementUpgrade3`](Engine_LogicKeys.md#object-basementupgrade3) | Object || 1 ||
| [`BasementUpgrade4`](Engine_LogicKeys.md#object-basementupgrade4) | Object || 1 ||
| [`BasementUpgrade5`](Engine_LogicKeys.md#object-basementupgrade5) | Object || 1 ||
| [`Floor1_Large`](Engine_LogicKeys.md#object-floor1_large) | Object || 1 ||
| [`Floor1_Small`](Engine_LogicKeys.md#object-floor1_small) | Object || 1 ||
| [`House1`](Engine_LogicKeys.md#object-house1) | Object || 1 ||
| [`House2`](Engine_LogicKeys.md#object-house2) | Object || 1 ||
| [`House3`](Engine_LogicKeys.md#object-house3) | Object || 1 ||
| [`LargeHouse`](Engine_LogicKeys.md#object-largehouse) | Object || 1 ||
| [`LargeHouse_Floor2Large`](Engine_LogicKeys.md#object-largehouse_floor2large) | Object || 1 ||
| [`LargeHouse_Floor2Small`](Engine_LogicKeys.md#object-largehouse_floor2small) | Object || 1 ||
| [`MediumHouse`](Engine_LogicKeys.md#object-mediumhouse) | Object || 1 ||
| [`MediumHouse_SmallRoom`](Engine_LogicKeys.md#object-mediumhouse_smallroom) | Object || 1 ||
| [`SmallAttic`](Engine_LogicKeys.md#object-smallattic) | Object || 1 ||
| [`SmallHouse_Attic`](Engine_LogicKeys.md#object-smallhouse_attic) | Object || 1 ||
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array | An array defining additional collision planes that bound the room's playable area. | 1 ||
| [`p`](./Arrays.md#array-p) | Array || 1 ||
| [`Thunderstorm`](Engine_LogicKeys.md#object-thunderstorm) | Object || 1 ||

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 2166


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root), [`SolarFlare`](#object-solarflare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1695 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 750 ||
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | Game-state flag identifiers for tracking world progression and event states. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 85


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](#object-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 66 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 23 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 53


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ApplyPassives`](#object-applypassives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
</details>

---

### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 47


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`extra_statuses`](#object-extra_statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the name of the tag to check for on the target. | 46 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 46 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 11 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Default`


**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 38


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_house`](./Enums.md#enum-set_house) | Enum | Specifies which house type to set for the upgrade. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 37


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`StatusCharactersOnRoundEnd`](#object-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Math_Equations.md) | Equation | (Must be float values) | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 37 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 28 ||

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll), [`Else`](#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
</details>

---

### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 32


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array / Integer || 31 ||
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 23 ||
| [`tile`](./Enums.md#enum-tile) | Array / Enum | Specifies the tile type(s) to change to (e.g., RoadTile, WaterTile). Can be a single tile or an array of tiles. | 7 ||
| [`trap`](./Enums.md#enum-trap) | Enum || 2 ||

</details>

---

### Object: `ApplyPassives`


**Definition:** Grants the nested passive abilities dynamically.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_HasTag`](#object-conditional_hastag), [`Conditional_PartyMember`](#object-conditional_partymember)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 13 ||

</details>

---

### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
</details>

---

### Object: `reverb_empty`


**Definition:** No definition provided.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Float | A scalar value for the strength or intensity of an ambient effect, or a percentage range. | 10 ||
| [`preset`](./Enums.md#enum-preset) | Enum || 10 ||
| `volume_adjustment` | Float || 10 ||

</details>

---

### Object: `reverb_full`


**Definition:** No definition provided.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Float | A scalar value for the strength or intensity of an ambient effect, or a percentage range. | 10 ||
| [`preset`](./Enums.md#enum-preset) | Enum || 10 ||

</details>

---

### Object: `CharacterTypeGainsStatusAtBattleStart`


**Definition:** Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the name of the tag to check for on the target. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||

</details>

---

### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 3 | |

</details>

---

### Object: `Rain`


**Definition:** Character Form: Behavior and stats for the 'Rain' state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type for the adventure map (e.g., Snow, Rain, Windy, Thunderstorm). | 1 ||
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather event. | 1 ||
| [`particles`](./Arrays.md#array-particles) | Array | An array of particle system names to be used for this weather effect. | 1 ||
| `prewarm` | Integer | The number of seconds to prewarm the particle system before displaying. | 1 ||
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Specifies the skybox visual frame to use for this weather. | 1 ||

</details>

---

### Object: `StatusAllCharactersOnSpawn`


**Definition:** Applies or references the 'StatusAllCharactersOnSpawn' effect/state.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 3 ||

</details>

---

### Object: `Big`


**Definition:** Character Form / AI State: Behavior and stats for the \'Big\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`SpecialGodRays`](#object-specialgodrays)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum | The character tag this visual effect follows. | 2 ||
| [`position`](./Arrays.md#array-position) | Array | The 2D position (x, y) or single-coordinate value for placement. | 2 ||

</details>

---

### Object: `extra_statuses`


**Definition:** Additional generic status applications.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`FactionUprising`](#object-factionuprising)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | An object that executes inner effects if the target has the specified tag, else falls back. | 1 ||
| `HealthGain` | Integer | The amount of health restored to the source. | 1 ||
</details> 

---


<details>
<summary><b>ApplyPassives</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>CharacterTypeGainsStatusAtBattleStart</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_Corpse</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 3 ||
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 3 ||
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>RandomStatusFromPool</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusAllCharactersOnSpawn</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusCharactersOnRoundEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusCharactersOnRoundStart</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 3 ||
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnBattleEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>extra_statuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

### Object: `Snow`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type for the adventure map (e.g., Snow, Rain, Windy, Thunderstorm). | 1 ||
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather event. | 1 ||
| [`particles`](./Arrays.md#array-particles) | Array | An array of particle system names to be used for this weather effect. | 1 ||
| `prewarm` | Integer | The number of seconds to prewarm the particle system before displaying. | 1 ||
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Specifies the skybox visual frame to use for this weather. | 1 ||

</details>

---

### Object: `aux_positions`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`House1`](#object-house1), [`House2`](#object-house2), [`House3`](#object-house3)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ButchBox`](./Arrays.md#array-butchbox) | Array || 3 ||
| [`HousePipe`](./Arrays.md#array-housepipe) | Array || 3 ||
| [`Roof_LeftEdge`](./Arrays.md#array-roof_leftedge) | Array || 3 ||
| [`Roof_RightEdge`](./Arrays.md#array-roof_rightedge) | Array || 3 ||
| [`Roof_Top`](./Arrays.md#array-roof_top) | Array || 3 ||
| [`StraySpawn`](./Arrays.md#array-strayspawn) | Array || 3 ||

</details>

---

### Object: `room_positions`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`House1`](#object-house1), [`House2`](#object-house2), [`House3`](#object-house3)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Floor1_Large`](./Arrays.md#array-floor1_large) | Array || 3 ||
| [`Basement0`](./Arrays.md#array-basement0) | Array || 2 ||
| [`Basement1`](./Arrays.md#array-basement1) | Array || 2 ||
| [`Basement2`](./Arrays.md#array-basement2) | Array || 2 ||
| [`Basement3`](./Arrays.md#array-basement3) | Array || 2 ||
| [`Basement4`](./Arrays.md#array-basement4) | Array || 2 ||
| [`Floor1_Small`](./Arrays.md#array-floor1_small) | Array || 2 ||
| [`LargeAttic`](./Arrays.md#array-largeattic) | Array || 2 ||
| [`Floor2_Large`](./Arrays.md#array-floor2_large) | Array || 1 ||
| [`Floor2_Small`](./Arrays.md#array-floor2_small) | Array || 1 ||
| [`SmallAttic`](./Arrays.md#array-smallattic) | Array || 1 ||

</details>

---

### Object: `SpawnVolcanoOnBattleStart`


**Definition:** Examples: `{ ... }`  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 3 ||
| `max_radius` | Float || 2 ||
| [`min_radius`](./Enums.md#enum-min_radius) | Float || 2 ||
| [`puddle_tile`](./Enums.md#enum-puddle_tile) | Array || 2 ||
| [`number`](./Arrays.md#array-number) | Array / Integer || 1 ||

</details>

---

### Object: `StatusCharactersOnRoundEnd`


**Definition:** Examples: `{ ... }`  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Thunderstorm`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type for the adventure map (e.g., Snow, Rain, Windy, Thunderstorm). | 1 ||
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather event. | 1 ||
| `lightning_fx` | Boolean | If true, enables lightning visual effects during the thunderstorm. | 1 ||
| [`particles`](./Arrays.md#array-particles) | Array | An array of particle system names to be used for this weather effect. | 1 ||
| `prewarm` | Integer | The number of seconds to prewarm the particle system before displaying. | 1 ||
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Specifies the skybox visual frame to use for this weather. | 1 ||

</details>

---

### Object: `AllyInfested`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Else`](#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines which faction the spawned entity belongs to, controlling its team allegiance and targeting behavior. | 1 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 ||

</details>

---

### Object: `GlobalSpawnOnRoundEnd`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 ||
| [`number`](./Arrays.md#array-number) | Array / Integer || 1 ||

</details>

---

### Object: `SolarFlare`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The damage dealt, which can be a numeric value, a formula string, or a defined damage object. | 1 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `SpecialGodRays`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Big`](Characters_and_Bosses.md#object-big) | Object || 2 ||

</details>

---

### Object: `StatusCharactersOnRoundStart`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Windy`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type for the adventure map (e.g., Snow, Rain, Windy, Thunderstorm). | 1 ||
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather event. | 1 ||
| [`particles`](./Arrays.md#array-particles) | Array | An array of particle system names to be used for this weather effect. | 1 ||
| `prewarm` | Integer | The number of seconds to prewarm the particle system before displaying. | 1 ||
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Specifies the skybox visual frame to use for this weather. | 1 ||

</details>

---

### Object: `AddPostProcessEffect`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean || 1 ||
| [`shader`](./Enums.md#enum-shader) | Enum || 1 ||

</details>

---

### Object: `AddTilesetObjects`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FloatingDebris`](Engine_LogicKeys.md#object-floatingdebris) | Object || 1 ||

</details>

---

### Object: `BasementUpgrade`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `BasementUpgrade2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `BasementUpgrade3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `BasementUpgrade4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `BasementUpgrade5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `FactionUprising`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the name of the tag to check for on the target. | 1 ||

</details>

---

### Object: `FloatingDebris`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`AddTilesetObjects`](#object-addtilesetobjects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The number of times or items to generate, spawn, or apply. | 1 ||

</details>

---

### Object: `Floor1_Large`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 1 ||
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame name used for interstitial room transition screens. | 1 ||
| [`reverb_empty`](#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 ||
| [`reverb_full`](#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. | 1 ||
| `width` | Integer | The width of the room in grid tiles. | 1 ||

</details>

---

### Object: `Floor1_Small`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 1 ||
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame name used for interstitial room transition screens. | 1 ||
| [`reverb_empty`](#object-reverb_empty) | Object | Reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 ||
| [`reverb_full`](#object-reverb_full) | Object | Reverb settings for a full room, including preset, amount, and volume adjustment. | 1 ||
| `width` | Integer | The width of the room in grid tiles. | 1 ||

</details>

---

### Object: `House1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](#object-aux_positions) | Object | Maps auxiliary object names to their [x, y] coordinates in the house scene. | 1 ||
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum | Specifies which placement frame to use for background decorations in the house. | 1 ||
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum | Specifies the movieclip identifier for the house background layer. | 1 ||
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum | Specifies the movieclip identifier for the house foreground layer. | 1 ||
| [`room_positions`](#object-room_positions) | Object | Maps room names to their [x, y] grid positions within the house layout. | 1 ||
| `zoomout_catvolume` | Float | The volume level for cat sounds when the camera is zoomed out, as a float. | 1 ||

</details>

---

### Object: `House2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](#object-aux_positions) | Object | Maps auxiliary object names to their [x, y] coordinates in the house scene. | 1 ||
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum | Specifies which placement frame to use for background decorations in the house. | 1 ||
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum | Specifies the movieclip identifier for the house background layer. | 1 ||
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum | Specifies the movieclip identifier for the house foreground layer. | 1 ||
| [`room_positions`](#object-room_positions) | Object | Maps room names to their [x, y] grid positions within the house layout. | 1 ||
| `zoomout_catvolume` | Float | The volume level for cat sounds when the camera is zoomed out, as a float. | 1 ||

</details>

---

### Object: `House3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](#object-aux_positions) | Object | Maps auxiliary object names to their [x, y] coordinates in the house scene. | 1 ||
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum | Specifies which placement frame to use for background decorations in the house. | 1 ||
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum | Specifies the movieclip identifier for the house background layer. | 1 ||
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum | Specifies the movieclip identifier for the house foreground layer. | 1 ||
| [`room_positions`](#object-room_positions) | Object | Maps room names to their [x, y] grid positions within the house layout. | 1 ||
| `zoomout_catvolume` | Float | The volume level for cat sounds when the camera is zoomed out, as a float. | 1 ||

</details>

---

### Object: `LargeHouse`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`set_house`](./Enums.md#enum-set_house) | Enum | Specifies which house type to set for the upgrade. | 1 ||

</details>

---

### Object: `LargeHouse_Floor2Large`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `LargeHouse_Floor2Small`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `MediumHouse`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`set_house`](./Enums.md#enum-set_house) | Enum | Specifies which house type to set for the upgrade. | 1 ||

</details>

---

### Object: `MediumHouse_SmallRoom`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `SmallAttic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 1 ||
| [`id`](./Enums.md#enum-id) | Enum | Specifies the unique identifier for the object or room, used for referencing or categorization. | 1 ||
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame name used for interstitial room transition screens. | 1 ||
| `width` | Integer | The width of the room in grid tiles. | 1 ||
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array | An array defining additional collision planes that bound the room's playable area. | 1 ||
| [`n`](./Arrays.md#array-n) | Array || 1 ||

</details>

---

### Object: `SmallHouse_Attic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum | The prerequisite upgrade that must be built before this basement upgrade is available. | 1 ||
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | The room type unlocked by this basement upgrade (e.g., Basement2, Attic). | 1 ||

</details>

---

### Object: `SpawnTilePuddleOnBattleStart`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_radius` | Float || 1 ||
| `min_radius` | Float || 1 ||
| [`tile`](./Enums.md#enum-tile) | Array / Enum | Specifies the tile type(s) to change to (e.g., RoadTile, WaterTile). Can be a single tile or an array of tiles. | 1 ||

</details>

---
