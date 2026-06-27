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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2731 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 291 | `Default`<br>`FormChange`<br>`Druid` |
| [`id`](./Enums.md#enum-id) | Enum | The unique numerical identifier for this injury or status effect. | 14 | `-1`<br>`0`<br>`1` |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 13 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array | A list of element types that remain persistent on the ground during this weather. | 12 | `[Fire]`<br>`[Heat]`<br>`[Holy]` |
| `height` | Integer | The height in tiles the target is launched into the air. | 8 | `0`<br>`1`<br>`2` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 8 | `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 8 | `{ . . . }` |
| `width` | Integer | The number of tiles the room spans horizontally. | 8 | `16`<br>`18`<br>`33` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 3 | `attic`<br>`room1`<br>`room2` |
| `amount` | Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 2 | `.1`<br>`.25`<br>`.35` |
| [`preset`](./Enums.md#enum-preset) | Enum || 2 | `AUDITORIUM`<br>`Alley`<br>`Cave` |
| [`n`](./Arrays.md#array-n) | Array || 2 | `[-1 -2]`<br>`[1 -2]` |
| [`Default`](./Miscellaneous.md#object-default) | Enum / Object  || 1 | `{ . . . }`<br>`release` |
| `volume_adjustment` | Float || 1 | `1.3`<br>`1.35`<br>`1.5` |
| [`BasementUpgrade`](./Miscellaneous.md#object-basementupgrade) | Object  || 1 | `{ . . . }` |
| [`BasementUpgrade2`](./Miscellaneous.md#object-basementupgrade2) | Object  || 1 | `{ . . . }` |
| [`BasementUpgrade3`](./Miscellaneous.md#object-basementupgrade3) | Object  || 1 | `{ . . . }` |
| [`BasementUpgrade4`](./Miscellaneous.md#object-basementupgrade4) | Object  || 1 | `{ . . . }` |
| [`BasementUpgrade5`](./Miscellaneous.md#object-basementupgrade5) | Object  || 1 | `{ . . . }` |
| [`Floor1_Large`](./Miscellaneous.md#object-floor1_large) | Object  || 1 | `{ . . . }` |
| [`Floor1_Small`](./Miscellaneous.md#object-floor1_small) | Object  || 1 | `{ . . . }` |
| [`House1`](./Miscellaneous.md#object-house1) | Object  || 1 | `{ . . . }` |
| [`House2`](./Miscellaneous.md#object-house2) | Object  || 1 | `{ . . . }` |
| [`House3`](./Miscellaneous.md#object-house3) | Object  || 1 | `{ . . . }` |
| [`LargeHouse`](./Miscellaneous.md#object-largehouse) | Object  || 1 | `{ . . . }` |
| [`LargeHouse_Floor2Large`](./Miscellaneous.md#object-largehouse_floor2large) | Object  || 1 | `{ . . . }` |
| [`LargeHouse_Floor2Small`](./Miscellaneous.md#object-largehouse_floor2small) | Object  || 1 | `{ . . . }` |
| [`MediumHouse`](./Miscellaneous.md#object-mediumhouse) | Object  || 1 | `{ . . . }` |
| [`MediumHouse_SmallRoom`](./Miscellaneous.md#object-mediumhouse_smallroom) | Object  || 1 | `{ . . . }` |
| [`SmallAttic`](./Miscellaneous.md#object-smallattic) | Object  || 1 | `{ . . . }` |
| [`SmallHouse_Attic`](./Miscellaneous.md#object-smallhouse_attic) | Object  || 1 | `{ . . . }` |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array | A list of additional boundary planes for the room. | 1 | `[` |
| [`p`](./Arrays.md#array-p) | Array || 1 | `[18 0]`<br>`[35 0]` |
| [`Thunderstorm`](./Miscellaneous.md#object-thunderstorm) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 2166

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root), [`SolarFlare`](#object-solarflare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1695 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 | `Default`<br>`FormChange`<br>`Druid` |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | Inherits game-wide rule modifiers. You can utilize any key from the Engine Global Modifier Keys list here to alter overarching game mechanics (e.g., changing gravity or stamina costs). | 1 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

`damage_instance`<br>`spell`<br>`self_damage`


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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 66 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 23 | `Default`<br>`FormChange`<br>`Druid` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>

---`damage_instance`<br>`spell`<br>`self_damage`


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
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 46 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 46 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 11 | `Default`<br>`FormChange`<br>`Druid` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


`damage_instance`<br>`spell`<br>`self_damage`


### Object: `Default`


**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 38

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_house`](./Enums.md#enum-set_house) | Enum | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| [`odds`](./Math_Equations.md) | Equation | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 | `Default`<br>`FormChange`<br>`Druid` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 | `passives`<br>`class`<br>`tag` |

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
| [`number`](./Arrays.md#array-number) | Array / Integer || 31 | `1`<br>`10`<br>`2` |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 23 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`tile`](./Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [`trap`](./Enums.md#enum-trap) | Enum || 2 | `BearTrap`<br>`LandMine`<br>`WaterKittenTrap` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 13 | `passives`<br>`class`<br>`tag` |

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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_Corpse` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` |

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
| `amount` | Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 10 | `.1`<br>`.25`<br>`.35` |
| [`preset`](./Enums.md#enum-preset) | Enum || 10 | `AUDITORIUM`<br>`Alley`<br>`Cave` |
| `volume_adjustment` | Float || 10 | `1.3`<br>`1.35`<br>`1.5` |

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
| `amount` | Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 10 | `.1`<br>`.25`<br>`.35` |
| [`preset`](./Enums.md#enum-preset) | Enum || 10 | `AUDITORIUM`<br>`Alley`<br>`Cave` |

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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | - | `CharacterTypeGainsStatusAtBattleStart` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 8 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |

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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_PartyMember` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` |

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
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`particles`](./Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |

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
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum | Determines which character this visual effect follows. | 2 | `zaratana` |
| [`position`](./Arrays.md#array-position) | Array | The world-space coordinates for this object. | 2 | `10.5`<br>`[4.5 4.5]` |

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
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


<details>
<summary><b>ApplyPassives</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
<details>
<summary><b>CharacterTypeGainsStatusAtBattleStart</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
<details>
<summary><b>Conditional_Corpse</b></summary>

> **Total Count:** 11`damage_instance`<br>`spell`<br>`self_damage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 0`damage_instance`<br>`spell`<br>`self_damage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
<details>
<summary><b>RandomStatusFromPool</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
<details>
<summary><b>StatusAllCharactersOnSpawn</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>
<details>
<summary><b>StatusCharactersOnRoundEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>
<details>
<summary><b>StatusCharactersOnRoundStart</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>
<details>
<summary><b>StatusOnBattleEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


<details>
<summary><b>extra_statuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>


### Object: `Snow`


`damage_instance`<br>`spell`<br>`self_damage`

**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`particles`](./Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |

</details>


---


### Object: `aux_positions``damage_instance`<br>`spell`<br>`self_damage`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`House1`](#object-house1), [`House2`](#object-house2), [`House3`](#object-house3)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ButchBox`](./Arrays.md#array-butchbox) | Array || 3 | `[21, 0]`<br>`[38, 0]` |
| [`HousePipe`](./Arrays.md#array-housepipe) | Array || 3 | `[-2 0]` |
| [`Roof_LeftEdge`](./Arrays.md#array-roof_leftedge) | Array || 3 | `[-3.388 8.138]`<br>`[-3.482 16.11]`<br>`[-3.617 8.112]` |
| [`Roof_RightEdge`](./Arrays.md#array-roof_rightedge) | Array || 3 | `[21.548 8.175]`<br>`[38.408 16.185]`<br>`[38.518 8.207]` |
| [`Roof_Top`](./Arrays.md#array-roof_top) | Array || 3 | `[17.562 26.715]`<br>`[17.563 18.677]`<br>`[8.983 14.4]` |
| [`StraySpawn`](./Arrays.md#array-strayspawn) | Array || 3 | `[-3 0]` |

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
| [`Floor1_Large`](./Arrays.md#array-floor1_large) | Array || 3 | `[1, 1]` |
| [`Basement0`](./Arrays.md#array-basement0) | Array || 2 | `[1 -6]` |
| [`Basement1`](./Arrays.md#array-basement1) | Array || 2 | `[1 -12]` |
| [`Basement2`](./Arrays.md#array-basement2) | Array || 2 | `[1 -18]` |
| [`Basement3`](./Arrays.md#array-basement3) | Array || 2 | `[1 -24]` |
| [`Basement4`](./Arrays.md#array-basement4) | Array || 2 | `[1 -30]` |
| [`Floor1_Small`](./Arrays.md#array-floor1_small) | Array || 2 | `[18, 1]` |
| [`LargeAttic`](./Arrays.md#array-largeattic) | Array || 2 | `[0, 17]`<br>`[0, 9]` |
| [`Floor2_Large`](./Arrays.md#array-floor2_large) | Array || 1 | `[18, 9]` |
| [`Floor2_Small`](./Arrays.md#array-floor2_small) | Array || 1 | `[1, 9]` |
| [`SmallAttic`](./Arrays.md#array-smallattic) | Array || 1 | `[0, 9]` |

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
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `max_radius` | Float || 2 | `2.2`<br>`3.5` |
| [`min_radius`](./Enums.md#enum-min_radius) | Float || 2 | `.2`<br>`1`<br>`1.5` |
| [`puddle_tile`](./Arrays.md#array-puddle_tile) | Array  || 2 | `LavaTile`<br>`[BrambleTile TallBrambleTile]` |
| [`number`](./Arrays.md#array-number) | Array / Integer || 1 | `1`<br>`10`<br>`2` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

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
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| `lightning_fx` | Boolean | If true, lightning visual effects will occur during this thunderstorm. | 1 | `true` |
| [`particles`](./Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |

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
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 | `allies`<br>`auto`<br>`birds` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

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
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer || 1 | `1`<br>`10`<br>`2` |

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
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 | `damage_instance`<br>`spell`<br>`false` |

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
| [`Big`](./Miscellaneous.md#object-big) | Object  || 2 | `{ . . . }` |

</details>


---


### Object: `StatusCharactersOnRoundStart`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`effects`](#object-effects)
`damage_instance`<br>`spell`<br>`self_damage`
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
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`particles`](./Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| `prewarm` | Integer | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |

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
| `requires_framebuffer` | Boolean || 1 | `false` |
| [`shader`](./Enums.md#enum-shader) | Enum || 1 | `shimmervignette` |

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
| [`FloatingDebris`](./Miscellaneous.md#object-floatingdebris) | Object  || 1 | `{ . . . }` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

</details>


---


### Object: `FactionUprising`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `FactionUprising` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

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
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

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
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Integer | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |

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
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |
| [`reverb_empty`](./Miscellaneous.md#object-reverb_empty) | Object  | Defines the audio reverb settings for an empty room, including preset, amount, and volume adjustment. | 1 | `{ . . . }` |
| [`reverb_full`](./Miscellaneous.md#object-reverb_full) | Object  | Defines the audio reverb settings for a full room, including preset and amount. | 1 | `{ . . . }` |
| `width` | Integer | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |

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
| [`aux_positions`](./Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](./Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | Float | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

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
| [`aux_positions`](./Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](./Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | Float | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

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
| [`aux_positions`](./Miscellaneous.md#object-aux_positions) | Object  | An object containing named coordinates for auxiliary objects like spawn points within this house. | 1 | `{ . . . }` |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum | Specifies the background frame identifier used for positioning background elements. | 1 | `large`<br>`small` |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum | Specifies the background movie clip asset for this house. | 1 | `HouseBackground1`<br>`HouseBackground2`<br>`HouseBackground3` |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum | Specifies the foreground movie clip asset for this house. | 1 | `HouseForeground1`<br>`HouseForeground2`<br>`HouseForeground3` |
| [`room_positions`](./Miscellaneous.md#object-room_positions) | Object  | An object containing named coordinates for each room's position within the house layout. | 1 | `{ . . . }` |
| `zoomout_catvolume` | Float | A multiplier for the volume of cat sounds when the camera is zoomed out. | 1 | `.6`<br>`.7`<br>`.8` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](./Enums.md#enum-set_house) | Enum | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`set_house`](./Enums.md#enum-set_house) | Enum | Specifies which house layout to use for this upgrade. | 1 | `House1`<br>`House2`<br>`House3` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| `height` | Integer | The height in tiles the target is launched into the air. | 1 | `0`<br>`1`<br>`2` |
| [`id`](./Enums.md#enum-id) | Enum | The unique numerical identifier for this injury or status effect. | 1 | `-1`<br>`0`<br>`1` |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum | Specifies the background frame identifier used for the interstitial area of this room. | 1 | `attic`<br>`room1`<br>`room2` |
| `width` | Integer | The number of tiles the room spans horizontally. | 1 | `16`<br>`18`<br>`33` |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array | A list of additional boundary planes for the room. | 1 | `[` |
| [`n`](./Arrays.md#array-n) | Array || 1 | `[-1 -2]`<br>`[1 -2]` |

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
| [`prereq`](./Enums.md#enum-prereq) | Enum | Determines which upgrade must be purchased before this upgrade becomes available. | 1 | `BasementUpgrade`<br>`BasementUpgrade2`<br>`BasementUpgrade3` |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum | Specifies the room that is unlocked by purchasing this upgrade. | 1 | `Attic`<br>`Basement0`<br>`Basement1` |

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
| `max_radius` | Float || 1 | `2.2`<br>`3.5` |
| `min_radius` | Float || 1 | `.2`<br>`1`<br>`1.5` |
| [`tile`](./Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 1 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |

</details>


---