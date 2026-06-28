---
title: "House & Environment Schema"
description: "Overworld tiles and intractable house objects."
---

# House & Environment Schema

## Overview
> [!NOTE]
> This schema covers physical objects the player can interact with outside of combat, particularly inside the customizable house hub.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
Forecast [ //the first and last week of each month's odds are blended with the next month
    { //Winter 2 (January)
		None 14
		Snow 1
	}
	{ //Winter 3
		None 14
		Snow 1
	}
	{ //Spring 1 (March)
		None 14
		Rain 1
	}
	{ //Spring 2
		None 14
		Rain 1
	}
	{ //Spring 3
		None 14
		Rain 1
	}
	{ //Summer 1 (June)
		None 14
		Thunderstorm 1
	}
	{ //Summer 2
		None 14
		Thunderstorm 1
	}
	{ //Summer 3
		None 14
		Thunderstorm 1
	}
	{ //Autumn 1 (September)
		None 14
		Windy 1
	}
	{ //Autumn 2
		None 14
		Windy 1
	}
	{ //Autumn 3
		None 14
		Windy 1
	}
	{ //Winter 1 (December)
		None 14
		Snow 1
	}
]
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`House_and_Environment.md`](../../Directory/World_and_Events/House_and_Environment.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## House & Environment

> **Associated Files:** `data/house.gon, data/house_weather.gon, data/weather.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 59

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 60 | Default<br>FormChange<br>Druid |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 58 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`ambient_sound`](../Reference_and_Meta/Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 13 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`hint_persistent_elements`](../Reference_and_Meta/Arrays.md#array-hint_persistent_elements) | Array | A list of element types that remain persistent on the ground during this weather. | 12 | `[Fire]`<br>`[Heat]`<br>`[Holy]` |
| `height` | Integer | The height in tiles the target is launched into the air. | 8 | `0`<br>`1`<br>`2` |
| `width` | Integer | The number of tiles the room spans horizontally. | 8 | `16`<br>`18`<br>`33` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 7 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 7 | `{ . . . }` |
| `amount` | Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 4 | `.1`<br>`.25`<br>`.35` |
| [`preset`](../Reference_and_Meta/Enums.md#enum-preset) | Enum | Specifies the audio reverb preset to use. | 4 | `AUDITORIUM`<br>`Alley`<br>`Cave` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 3 | `attic`<br>`room1`<br>`room2` |
| `n` | Array | An array of [x, y] coordinates representing the north-facing connection point of a room. | 2 | `[-1 -2]`<br>`[1 -2]` |
| `p` | Array | A coordinate pair [x, y] representing a position. | 2 | `[18 0]`<br>`[35 0]` |
| `volume_adjustment` | Float | A multiplier for the volume of audio in a given room or reverb zone. | 2 | `1.3`<br>`1.35`<br>`1.5` |
| [`Thunderstorm`](../Reference_and_Meta/Miscellaneous.md#object-thunderstorm) | Object | Defines the Thunderstorm weather type, including ambient sound, particles, and lightning effect. | 1 | `{ . . . }` |
| [`Default`](../Reference_and_Meta/Miscellaneous.md#object-default) | Enum / Object | The default form configuration for a unit, containing its standard stats and abilities. | 1 | `{ . . . }`<br>`release` |
| [`id`](../Reference_and_Meta/Enums.md#enum-id) | Enum | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| [`Floor1_Large`](../Reference_and_Meta/Miscellaneous.md#object-floor1_large) | Object | Defines a large room on Floor 1, with dimensions (width 16, height 7) and associated movieclip and background frame. | 1 | `{ . . . }` |
| [`MediumHouse`](../Reference_and_Meta/Miscellaneous.md#object-mediumhouse) | Object | An upgrade that requires the Default house as a prerequisite and sets the house to House2. | 1 | `{ . . . }` |
| [`Floor1_Small`](../Reference_and_Meta/Miscellaneous.md#object-floor1_small) | Object | Defines a small room on Floor 1, with dimensions (width 16, height 7) and associated movieclip and background frame. | 1 | `{ . . . }` |
| [`LargeHouse`](../Reference_and_Meta/Miscellaneous.md#object-largehouse) | Object | An upgrade that requires MediumHouse as a prerequisite and sets the house to House3. | 1 | `{ . . . }` |
| [`BasementUpgrade`](../Reference_and_Meta/Miscellaneous.md#object-basementupgrade) | Object | An upgrade object that unlocks the first basement room (Basement0) after its prerequisite is met. | 1 | `{ . . . }` |
| [`BasementUpgrade2`](../Reference_and_Meta/Miscellaneous.md#object-basementupgrade2) | Object | An upgrade object that unlocks the second basement room (Basement1) after its prerequisite is met. | 1 | `{ . . . }` |
| [`BasementUpgrade3`](../Reference_and_Meta/Miscellaneous.md#object-basementupgrade3) | Object | An upgrade object that unlocks the third basement room (Basement2) after its prerequisite is met. | 1 | `{ . . . }` |
| [`BasementUpgrade4`](../Reference_and_Meta/Miscellaneous.md#object-basementupgrade4) | Object | An upgrade object that unlocks the fourth basement room (Basement3) after its prerequisite is met. | 1 | `{ . . . }` |
| [`House1`](../Reference_and_Meta/Miscellaneous.md#object-house1) | Object | Defines house 1 with its background and foreground movieclips, placement frame, and zoom-out volume. | 1 | `{ . . . }` |
| [`House2`](../Reference_and_Meta/Miscellaneous.md#object-house2) | Object | Defines house 2 with its background and foreground movieclips, placement frame, and zoom-out volume. | 1 | `{ . . . }` |
| [`House3`](../Reference_and_Meta/Miscellaneous.md#object-house3) | Object | Defines house 3 with its background and foreground movieclips, placement frame, and zoom-out volume. | 1 | `{ . . . }` |
| [`LargeHouse_Floor2Large`](../Reference_and_Meta/Miscellaneous.md#object-largehouse_floor2large) | Object | An upgrade that requires LargeHouse and unlocks the Floor2_Large room. | 1 | `{ . . . }` |
| [`LargeHouse_Floor2Small`](../Reference_and_Meta/Miscellaneous.md#object-largehouse_floor2small) | Object | An upgrade that requires LargeHouse and unlocks the Floor2_Small room. | 1 | `{ . . . }` |
| [`MediumHouse_SmallRoom`](../Reference_and_Meta/Miscellaneous.md#object-mediumhouse_smallroom) | Object | An upgrade that requires MediumHouse and unlocks the Floor1_Small room. | 1 | `{ . . . }` |
| [`SmallAttic`](../Reference_and_Meta/Miscellaneous.md#object-smallattic) | Object | Room definition for the Small Attic, including its dimensions and position. | 1 | `{ . . . }` |
| [`SmallHouse_Attic`](../Reference_and_Meta/Miscellaneous.md#object-smallhouse_attic) | Object | Upgrade that unlocks the Attic room in a small house. | 1 | `{ . . . }` |
| [`extra_bound_planes`](../Reference_and_Meta/Arrays.md#array-extra_bound_planes) | Array | A list of additional boundary planes for the room. | 1 | `[` |
| [`BasementUpgrade5`](../Reference_and_Meta/Miscellaneous.md#object-basementupgrade5) | Object | An upgrade object that unlocks the fifth basement room (Basement4) after its prerequisite is met. | 1 | `{ . . . }` |

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.  
**Total Count:** 2166

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root), [`SolarFlare`](#object-solarflare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 57 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 7 | Default<br>FormChange<br>Druid |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |
| [`{Global Modifier Keys}`](../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | If true, activates a global modifier effect on the house environment. | 0 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start.  
**Total Count:** 32

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 27 | `1`<br>`10`<br>`2` |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 19 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [`trap`](../Reference_and_Meta/Enums.md#enum-trap) | Enum | The type of trap to spawn. Specifies which trap template to use. | 2 | `BearTrap`<br>`LandMine`<br>`WaterKittenTrap` |

</details>


---


### Object: `reverb_full`


**Definition:** Defines the audio reverb settings for a full room, including preset and amount.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 9 | `.1`<br>`.25`<br>`.35` |
| [`preset`](../Reference_and_Meta/Enums.md#enum-preset) | Enum | Specifies the audio reverb preset to use. | 9 | `AUDITORIUM`<br>`Alley`<br>`Cave` |

</details>


---


### Object: `reverb_empty`


**Definition:** Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Floor1_Large`](#object-floor1_large), [`Floor1_Small`](#object-floor1_small), [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 9 | `.1`<br>`.25`<br>`.35` |
| [`preset`](../Reference_and_Meta/Enums.md#enum-preset) | Enum | Specifies the audio reverb preset to use. | 9 | `AUDITORIUM`<br>`Alley`<br>`Cave` |
| `volume_adjustment` | Float | A multiplier for the volume of audio in a given room or reverb zone. | 9 | `1.3`<br>`1.35`<br>`1.5` |

</details>


---


### Object: `room_positions`


**Definition:** An object containing named coordinates for each room's position within the house layout.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`House1`](#object-house1), [`House2`](#object-house2), [`House3`](#object-house3)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Floor1_Large`](../Reference_and_Meta/Arrays.md#array-floor1_large) | Array | Defines a large room on Floor 1, with dimensions (width 16, height 7) and associated movieclip and background frame. | 3 | `[1, 1]` |
| [`Basement0`](../Reference_and_Meta/Arrays.md#array-basement0) | Array | The grid position [x, y] of the first basement room. | 2 | `[1 -6]` |
| [`Basement1`](../Reference_and_Meta/Arrays.md#array-basement1) | Array | The grid position [x, y] of the second basement room. | 2 | `[1 -12]` |
| [`Basement2`](../Reference_and_Meta/Arrays.md#array-basement2) | Array | The grid position [x, y] of the third basement room. | 2 | `[1 -18]` |
| [`Basement3`](../Reference_and_Meta/Arrays.md#array-basement3) | Array | The grid position [x, y] of the fourth basement room. | 2 | `[1 -24]` |
| [`Basement4`](../Reference_and_Meta/Arrays.md#array-basement4) | Array | The grid position [x, y] of the fifth basement room. | 2 | `[1 -30]` |
| [`Floor1_Small`](../Reference_and_Meta/Arrays.md#array-floor1_small) | Array | Defines a small room on Floor 1, with dimensions (width 16, height 7) and associated movieclip and background frame. | 2 | `[18, 1]` |
| [`LargeAttic`](../Reference_and_Meta/Arrays.md#array-largeattic) | Array | The grid position [x, y] of the large attic room. | 2 | `[0, 17]`<br>`[0, 9]` |
| [`Floor2_Large`](../Reference_and_Meta/Arrays.md#array-floor2_large) | Array | The grid position [x, y] of the large room on the second floor. | 1 | `[18, 9]` |
| [`Floor2_Small`](../Reference_and_Meta/Arrays.md#array-floor2_small) | Array | The grid position [x, y] of the small room on the second floor. | 1 | `[1, 9]` |
| [`SmallAttic`](../Reference_and_Meta/Arrays.md#array-smallattic) | Array | Room definition for the Small Attic, including its dimensions and position. | 1 | `[0, 9]` |

</details>


---


### Object: `aux_positions``damage_instance`<br>`spell`<br>`self_damage`


**Definition:** An object containing named coordinates for auxiliary objects like spawn points within this house.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`House1`](#object-house1), [`House2`](#object-house2), [`House3`](#object-house3)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ButchBox`](../Reference_and_Meta/Arrays.md#array-butchbox) | Array | An array [x, y] defining the auxiliary position offset for the ButchBox object on the house. | 3 | `[21, 0]`<br>`[38, 0]` |
| [`HousePipe`](../Reference_and_Meta/Arrays.md#array-housepipe) | Array | The [X, Y] offset from the house origin where a pipe spawns on the exterior. | 3 | `[-2 0]` |
| [`Roof_LeftEdge`](../Reference_and_Meta/Arrays.md#array-roof_leftedge) | Array | The [X, Y] position of the left edge of the roof relative to the house origin. | 3 | `[-3.388 8.138]`<br>`[-3.482 16.11]`<br>`[-3.617 8.112]` |
| [`Roof_RightEdge`](../Reference_and_Meta/Arrays.md#array-roof_rightedge) | Array | The [X, Y] position of the right edge of the roof relative to the house origin. | 3 | `[21.548 8.175]`<br>`[38.408 16.185]`<br>`[38.518 8.207]` |
| [`Roof_Top`](../Reference_and_Meta/Arrays.md#array-roof_top) | Array | The [X, Y] position of the top of the roof relative to the house origin. | 3 | `[17.562 26.715]`<br>`[17.563 18.677]`<br>`[8.983 14.4]` |
| [`StraySpawn`](../Reference_and_Meta/Arrays.md#array-strayspawn) | Array | The [X, Y] offset from the house origin where a stray cat spawns. | 3 | `[-3 0]` |

</details>


---


### Object: `StatusCharactersOnRoundEnd`


**Definition:** An object whose nested keys define statuses or effects applied to characters at the end of each round.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusCharactersOnRoundEnd`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>
### Object: `SpawnVolcanoOnBattleStart`


**Definition:** An object containing parameters (object type, tile, radius) for spawning a volcano effect at the start of battle.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `max_radius` | Float | The maximum radius of the spawned puddle or volcano in tiles. | 2 | `2.2`<br>`3.5` |
| `min_radius` | Float | The minimum radius of the spawned puddle or volcano in tiles. | 2 | `.2`<br>`1`<br>`1.5` |
| [`puddle_tile`](../Reference_and_Meta/Arrays.md#array-puddle_tile) | Array | An array specifying the tile types to use for the puddle or volcano. | 2 | `LavaTile`<br>`[BrambleTile TallBrambleTile]` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Else`


**Definition:** Contains the fallback effects to apply when a preceding conditional check fails.  
**Total Count:** 86

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](#object-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>

---`damage_instance`<br>`spell`<br>`self_damage`


### Object: `Windy`


**Definition:** The number representing the Windy weather intensity or whether it is active.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ambient_sound`](../Reference_and_Meta/Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |

</details>


---


### Object: `Thunderstorm`


**Definition:** Defines the Thunderstorm weather type, including ambient sound, particles, and lightning effect.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ambient_sound`](../Reference_and_Meta/Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| `lightning_fx` | Boolean | If true, lightning visual effects will occur during this thunderstorm. | 1 | `true` |

</details>


---


### Object: `StatusCharactersOnRoundStart`


**Definition:** An object containing status effects to apply to all characters on the battlefield at the start of each round.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)
`damage_instance`<br>`spell`<br>`self_damage`
| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusCharactersOnRoundStart`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>
### Object: `StatusAllCharactersOnSpawn`


**Definition:** Defines status effects applied to all characters when they spawn into the battlefield.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `StatusAllCharactersOnSpawn`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>
### Object: `SpecialGodRays`


**Definition:** An object defining visual god rays that follow a specific character tag, used for cinematic or boss effects.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Big`](../Reference_and_Meta/Miscellaneous.md#object-big) | Object | Defines the 'Big' form, including its animation, attack, passives, and positional data. | 2 | `{ . . . }` |

</details>


---


### Object: `SolarFlare`


**Definition:** Defines the Solar Flare weather effect, which applies damage and status effects (burn, blind) to units each turn.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `Snow`


`damage_instance`<br>`spell`<br>`self_damage`

**Definition:** The number of snow particle instances or the integer value controlling snow intensity for weather effects.  
**Total Count:** 17

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| [`ambient_sound`](../Reference_and_Meta/Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** A collection of status effects; one is randomly chosen and applied to the target.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll), [`Else`](#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `RandomStatusFromPool`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
### Object: `Rain`


**Definition:** Defines the rain weather effect with associated particle, sound, and rendering settings.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ambient_sound`](../Reference_and_Meta/Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |

</details>


---


### Object: `GlobalSpawnOnRoundEnd`


**Definition:** Specifies the object to spawn globally at the end of each round.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`StatusCharactersOnRoundEnd`](#object-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| `odds` | Equation | The probability of the effect occurring, expressed as a decimal or percentage. | 2 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_GoodRoll`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
### Object: `CharacterTypeGainsStatusAtBattleStart`


**Definition:** Defines status effects applied to characters with a specific tag at the start of a battle.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CharacterTypeGainsStatusAtBattleStart`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
### Object: `Big`


**Definition:** Defines the 'Big' form, including its animation, attack, passives, and positional data.  
**Total Count:** 59

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`SpecialGodRays`](#object-specialgodrays)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`position`](../Reference_and_Meta/Arrays.md#array-position) | Array | The world-space coordinates for this object. | 2 | `10.5`<br>`[4.5 4.5]` |
| [`follow_character_tag`](../Reference_and_Meta/Enums.md#enum-follow_character_tag) | Enum | Determines which character this visual effect follows. | 2 | `zaratana` |

</details>


---


### Object: `ApplyPassives`


**Definition:** Specifies the passives or status effects to apply to the unit.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_HasTag`](#object-conditional_hastag), [`Conditional_PartyMember`](#object-conditional_partymember)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `ApplyPassives`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
### Object: `extra_statuses`


**Definition:** An object containing additional status effects (with stack counts) applied to the consumed unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`FactionUprising`](#object-factionuprising)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [`Conditional_HasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |

</details>


---


### Object: `extra_statuses`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>


### Object: `StatusOnBattleEnd`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


### Object: `StatusOnBattleEnd`


**Definition:** An object containing status effects or passives applied to the unit when the battle ends.  
**Total Count:** 53

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ApplyPassives`](#object-applypassives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `SpawnTilePuddleOnBattleStart`


**Definition:** Defines a puddle of a specific tile type (e.g., OilTile) that is spawned on the battlefield at the start, with a radius range.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 1 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| `max_radius` | Float | The maximum radius of the spawned puddle or volcano in tiles. | 1 | `2.2`<br>`3.5` |
| `min_radius` | Float | The minimum radius of the spawned puddle or volcano in tiles. | 1 | `.2`<br>`1`<br>`1.5` |

</details>


---
### Object: `SmallHouse_Attic`


**Definition:** Upgrade that unlocks the Attic room in a small house.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `SmallAttic`


**Definition:** Room definition for the Small Attic, including its dimensions and position.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`id`](../Reference_and_Meta/Enums.md#enum-id) | Enum | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| `width` | Integer | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |
| [`extra_bound_planes`](../Reference_and_Meta/Arrays.md#array-extra_bound_planes) | Array | A list of additional boundary planes for the room. | 1 | `[` |
| `n` | Array | An array of [x, y] coordinates representing the north-facing connection point of a room. | 1 | `[-1 -2]`<br>`[1 -2]` |

</details>


---


### Object: `MediumHouse_SmallRoom`


**Definition:** An upgrade that requires MediumHouse and unlocks the Floor1_Small room.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `MediumHouse`


**Definition:** An upgrade that requires the Default house as a prerequisite and sets the house to House2.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](../Reference_and_Meta/Enums.md#enum-set_house) | Enum | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

</details>


---


### Object: `LargeHouse_Floor2Small`


**Definition:** An upgrade that requires LargeHouse and unlocks the Floor2_Small room.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `LargeHouse_Floor2Large`


**Definition:** An upgrade that requires LargeHouse and unlocks the Floor2_Large room.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `LargeHouse`


**Definition:** An upgrade that requires MediumHouse as a prerequisite and sets the house to House3.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](../Reference_and_Meta/Enums.md#enum-set_house) | Enum | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

</details>


---


### Object: `House3`


**Definition:** Defines house 3 with its background and foreground movieclips, placement frame, and zoom-out volume.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](../Reference_and_Meta/Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](../Reference_and_Meta/Enums.md#enum-bg_placements_frame) | Enum | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](../Reference_and_Meta/Enums.md#enum-movieclip_bg) | Enum | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](../Reference_and_Meta/Enums.md#enum-movieclip_fg) | Enum | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](../Reference_and_Meta/Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | Float | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

</details>


---


### Object: `House2`


**Definition:** Defines house 2 with its background and foreground movieclips, placement frame, and zoom-out volume.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](../Reference_and_Meta/Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](../Reference_and_Meta/Enums.md#enum-bg_placements_frame) | Enum | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](../Reference_and_Meta/Enums.md#enum-movieclip_bg) | Enum | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](../Reference_and_Meta/Enums.md#enum-movieclip_fg) | Enum | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](../Reference_and_Meta/Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | Float | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

</details>


---


### Object: `House1`


**Definition:** Defines house 1 with its background and foreground movieclips, placement frame, and zoom-out volume.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aux_positions`](../Reference_and_Meta/Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](../Reference_and_Meta/Enums.md#enum-bg_placements_frame) | Enum | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](../Reference_and_Meta/Enums.md#enum-movieclip_bg) | Enum | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](../Reference_and_Meta/Enums.md#enum-movieclip_fg) | Enum | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](../Reference_and_Meta/Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | Float | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

</details>


---


### Object: `Floor1_Small`


**Definition:** Defines a small room on Floor 1, with dimensions (width 16, height 7) and associated movieclip and background frame.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Integer | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |

</details>


---


### Object: `Floor1_Large`


**Definition:** Defines a large room on Floor 1, with dimensions (width 16, height 7) and associated movieclip and background frame.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](../Reference_and_Meta/Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](../Reference_and_Meta/Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Integer | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](../Reference_and_Meta/Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |

</details>


---


### Object: `FloatingDebris`


**Definition:** An object defining parameters for spawning floating debris tileset objects.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`AddTilesetObjects`](#object-addtilesetobjects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `FactionUprising`


**Definition:** Specifies which faction triggers a global uprising event, adding allied units of that faction.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

</details>


---


### Object: `Default`


**Definition:** The default form configuration for a unit, containing its standard stats and abilities.  
**Total Count:** 85

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |
| [`set_house`](../Reference_and_Meta/Enums.md#enum-set_house) | Enum | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

</details>


---


### Object: `Conditional_PartyMember`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
### Object: `Conditional_PartyMember`


**Definition:** A conditional block that executes its child actions only if the target is a party member.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`StatusAllCharactersOnSpawn`](#object-statusallcharactersonspawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_HasTag`


**Definition:** Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`extra_statuses`](#object-extra_statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


`damage_instance`<br>`spell`<br>`self_damage`


### Object: `Conditional_Corpse`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
### Object: `Conditional_Corpse`


**Definition:** Contains an inner effect block that only executes if the target is a corpse.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Conditional_GoodRoll`](#object-conditional_goodroll)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `BasementUpgrade5`


**Definition:** An upgrade object that unlocks the fifth basement room (Basement4) after its prerequisite is met.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `BasementUpgrade4`


**Definition:** An upgrade object that unlocks the fourth basement room (Basement3) after its prerequisite is met.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `BasementUpgrade3`


**Definition:** An upgrade object that unlocks the third basement room (Basement2) after its prerequisite is met.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `BasementUpgrade2`


**Definition:** An upgrade object that unlocks the second basement room (Basement1) after its prerequisite is met.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `BasementUpgrade`


**Definition:** An upgrade object that unlocks the first basement room (Basement0) after its prerequisite is met.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`prereq`](../Reference_and_Meta/Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](../Reference_and_Meta/Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `AllyInfested`


**Definition:** Defines the AllyInfested object, which spawns an infested ally under the player's control.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`Else`](#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 | `allies`<br>`auto`<br>`birds` |

</details>


---


### Object: `AddTilesetObjects`


**Definition:** An object configuring the spawning of decorative debris or objects on the tileset for an effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FloatingDebris`](../Reference_and_Meta/Miscellaneous.md#object-floatingdebris) | Object | An object defining parameters for spawning floating debris tileset objects. | 1 | `{ . . . }` |

</details>


---


### Object: `AddPostProcessEffect`


**Definition:** Specifies a post-process shader effect to apply to the scene.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean | If true, the post-process effect requires a framebuffer to be active. | 1 | `false` |
| [`shader`](../Reference_and_Meta/Enums.md#enum-shader) | Enum | Specifies which shader to use for the post-process effect. | 1 | `shimmervignette` |

</details>


---

