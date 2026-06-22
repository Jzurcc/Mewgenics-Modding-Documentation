# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## House & Environment

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"WEATHER_RAIN_DESC", "WEATHER_NONE_DESC", "WEATHER_FOG_DESC"` |  |
| `name` | String | `"WEATHER_RAIN_NAME", "WEATHER_NONE_NAME", "WEATHER_FOG_NAME"` |  |
| `effects` | [`Block`](./House_and_Environment.md#context-effects) | `{ ... }` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_rain.ogg, amb_heavyrain.ogg, amb_windy.ogg` |  |
| `hint_persistent_elements` | [`Array`](./Arrays.md#array-hint_persistent_elements) | `[ Wind ], [ Heat ], [ Water ]` |  |
| `height` | Number | `7, 9, 5` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundSmallF2, RoomBackgroundAttic, RoomBackgroundLargeF2` |  |
| `width` | Number | `16, 35, 33` |  |
| `reverb_empty` | [`Block`](./House_and_Environment.md#context-reverb_empty) | `{ ... }` |  |
| `reverb_full` | [`Block`](./House_and_Environment.md#context-reverb_full) | `{ ... }` |  |
| `amount` | [`Enum/String`](./Enums.md#enum-amount) | `.25, .65` |  |
| `preset` | [`Enum/String`](./Enums.md#enum-preset) | `AUDITORIUM, LIVINGROOM` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `attic, room3, room4` |  |
| `n` | [`Array`](./Arrays.md#array-n) | `[ 1 -2 ], [ -1 -2 ]` |  |
| `volume_adjustment` | Number | `1.50` |  |
| `BasementUpgrade` | [`Block`](./House_and_Environment.md#context-basementupgrade) | `{ ... }` |  |
| `BasementUpgrade2` | [`Block`](./House_and_Environment.md#context-basementupgrade2) | `{ ... }` |  |
| `BasementUpgrade3` | [`Block`](./House_and_Environment.md#context-basementupgrade3) | `{ ... }` |  |
| `BasementUpgrade4` | [`Block`](./House_and_Environment.md#context-basementupgrade4) | `{ ... }` |  |
| `BasementUpgrade5` | [`Block`](./House_and_Environment.md#context-basementupgrade5) | `{ ... }` |  |
| `Default` | [`Block`](./House_and_Environment.md#context-default) | `{ ... }` |  |
| `Floor1_Large` | [`Block`](./House_and_Environment.md#context-floor1_large) | `{ ... }` |  |
| `Floor1_Small` | [`Block`](./House_and_Environment.md#context-floor1_small) | `{ ... }` |  |
| `House1` | [`Block`](./House_and_Environment.md#context-house1) | `{ ... }` |  |
| `House2` | [`Block`](./House_and_Environment.md#context-house2) | `{ ... }` |  |
| `House3` | [`Block`](./House_and_Environment.md#context-house3) | `{ ... }` |  |
| `LargeHouse` | [`Block`](./House_and_Environment.md#context-largehouse) | `{ ... }` |  |
| `LargeHouse_Floor2Large` | [`Block`](./House_and_Environment.md#context-largehouse_floor2large) | `{ ... }` |  |
| `LargeHouse_Floor2Small` | [`Block`](./House_and_Environment.md#context-largehouse_floor2small) | `{ ... }` |  |
| `MediumHouse` | [`Block`](./House_and_Environment.md#context-mediumhouse) | `{ ... }` |  |
| `MediumHouse_SmallRoom` | [`Block`](./House_and_Environment.md#context-mediumhouse_smallroom) | `{ ... }` |  |
| `Rain` | [`Block`](./House_and_Environment.md#context-rain) | `{ ... }` |  |
| `SmallAttic` | [`Block`](./House_and_Environment.md#context-smallattic) | `{ ... }` |  |
| `SmallHouse_Attic` | [`Block`](./House_and_Environment.md#context-smallhouse_attic) | `{ ... }` |  |
| `Snow` | [`Block`](./House_and_Environment.md#context-snow) | `{ ... }` |  |
| `Thunderstorm` | [`Block`](./House_and_Environment.md#context-thunderstorm) | `{ ... }` |  |
| `Windy` | [`Block`](./House_and_Environment.md#context-windy) | `{ ... }` |  |
| `extra_bound_planes` | [`Array`](./Arrays.md#array-extra_bound_planes) | `[ { p [ 0 0 ]` |  |
| `id` | [`Enum/String`](./Enums.md#enum-id) | `Attic` |  |
| `p` | [`Array`](./Arrays.md#array-p) | `[ 18 0 ]` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`SolarFlare`](./House_and_Environment.md#context-solarflare)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpawnExtraThingsOnBattleStart` | [`Block`](./House_and_Environment.md#context-spawnextrathingsonbattlestart) | `{ ... }` |  |
| `FactionUprising` | [`Enum/String`](./Enums.md#enum-factionuprising) | `alien, robot, ghost` |  |
| `LowerAmbientLight` | Number | `50%, 33%` |  |
| `Rain` | Number | `2, 1, 4` |  |
| `Windy` | Number | `10, 1` |  |
| `Meteornado` | Number | `1` |  |
| `SpawnVolcanoOnBattleStart` | [`Block`](./House_and_Environment.md#context-spawnvolcanoonbattlestart) | `{ ... }` |  |
| `StatusCharactersOnRoundEnd` | [`Block`](./House_and_Environment.md#context-statuscharactersonroundend) | `{ ... }` |  |
| `CharacterTypeGainsStatusAtBattleStart` | [`Block`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart) | `{ ... }` |  |
| `FireStorm` | Number | `0%, 33%` |  |
| `GlobalSpawnOnRoundEnd` | [`Block`](./House_and_Environment.md#context-globalspawnonroundend) | `{ ... }` |  |
| `RandomLightning` | Number | `50%` |  |
| `Snow` | Number | `1` |  |
| `SpecialGodRays` | [`Block`](./House_and_Environment.md#context-specialgodrays) | `{ ... }` |  |
| `StatusAllCharactersOnSpawn` | [`Block`](./House_and_Environment.md#context-statusallcharactersonspawn) | `{ ... }` |  |
| `StatusCharactersOnRoundStart` | [`Block`](./House_and_Environment.md#context-statuscharactersonroundstart) | `{ ... }` |  |
| `AcidRain` | Number | `2` |  |
| `AddPostProcessEffect` | [`Block`](./House_and_Environment.md#context-addpostprocesseffect) | `{ ... }` |  |
| `AddTilesetObjects` | [`Block`](./House_and_Environment.md#context-addtilesetobjects) | `{ ... }` |  |
| `Blind` | Number | `3` |  |
| `Burn` | Number | `3` |  |
| `ButterflySwarm` | Number | `2` |  |
| `ClearDefaultDebris` | Number | `1` |  |
| `CockroachSwarm` | Number | `1` |  |
| `DeleteInanimateObjectsChance` | Number | `25%` |  |
| `FindExtraItemFromPoolOnBattleEnd` | [`Enum/String`](./Enums.md#enum-findextraitemfrompoolonbattleend) | `pills` |  |
| `FireflySwarm` | Number | `2` |  |
| `FlySwarm` | Number | `50%` |  |
| `Fog` | Number | `1` |  |
| `GlobalHealthRegenAura` | Number | `3` |  |
| `HeatWave` | Number | `1` |  |
| `JudgementDay` | Number | `25` |  |
| `LowGravityKnockbackBoost` | Number | `1` |  |
| `LowGravityRangeBoost` | Number | `2` |  |
| `MeteorShower` | Number | `25%` |  |
| `PersistentElement` | [`Enum/String`](./Enums.md#enum-persistentelement) | `Holy` |  |
| `RandomWeatherEachFight` | [`Array`](./Arrays.md#array-randomweathereachfight) | `[ Fog Rain Windy Sandstorm HeatWave Snow Thunderstorm Bli...` |  |
| `Sandstorm` | Number | `1` |  |
| `SolarFlare` | [`Block`](./House_and_Environment.md#context-solarflare) | `{ ... }` |  |
| `SpawnTilePuddleOnBattleStart` | [`Block`](./House_and_Environment.md#context-spawntilepuddleonbattlestart) | `{ ... }` |  |
| `VisualFlySwarm` | Number | `1` |  |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 3 5 ], [ 2 5 ], [ 12 20 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Boulder, SmallRock, [ Junk Junk TrashBag ]` |  |
| `tile` | [`Enum/String`](./Enums.md#enum-tile) | `WaterTile, TallGrassTile, BrambleTile` |  |
| `trap` | [`Enum/String`](./Enums.md#enum-trap) | `LandMine, BearTrap` |  |

</details>

---

### Context: `reverb_empty`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | [`Enum/String`](./Enums.md#enum-amount) | `.65` |  |
| `preset` | [`Enum/String`](./Enums.md#enum-preset) | `AUDITORIUM, STONEROOM` |  |
| `volume_adjustment` | Number | `1.50, 2` |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll), [`Else`](./House_and_Environment.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatDown` | Number | `1` |  |
| `RandomStatUp` | Number | `1` |  |
| `Bleed` | Number | `1` |  |
| `Blind` | Number | `1` |  |
| `Brace` | Number | `1` |  |
| `Bruise` | Number | `1` |  |
| `DamageUp` | Number | `1` |  |
| `DivineShield` | Number | `1` |  |
| `Drowsy` | Number | `1` |  |
| `KineticSpikes` | Number | `1` |  |
| `Poison` | Number | `1` |  |
| `Shield` | Number | `1` |  |
| `Slow` | Number | `1` |  |
| `SpellDamageUp` | Number | `1` |  |
| `Thorns` | Number | `1` |  |
| `Weakness` | Number | `1` |  |

</details>

---

### Context: `room_positions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Floor1_Large` | [`Array`](./Arrays.md#array-floor1_large) | `[ 1, 1 ]` |  |
| `Basement0` | [`Array`](./Arrays.md#array-basement0) | `[ 1 -6 ]` |  |
| `Basement1` | [`Array`](./Arrays.md#array-basement1) | `[ 1 -12 ]` |  |
| `Basement2` | [`Array`](./Arrays.md#array-basement2) | `[ 1 -18 ]` |  |
| `Basement3` | [`Array`](./Arrays.md#array-basement3) | `[ 1 -24 ]` |  |
| `Basement4` | [`Array`](./Arrays.md#array-basement4) | `[ 1 -30 ]` |  |
| `Floor1_Small` | [`Array`](./Arrays.md#array-floor1_small) | `[ 18, 1 ]` |  |
| `LargeAttic` | [`Array`](./Arrays.md#array-largeattic) | `[ 0, 9 ], [ 0, 17 ]` |  |
| `Floor2_Large` | [`Array`](./Arrays.md#array-floor2_large) | `[ 18, 9 ]` |  |
| `Floor2_Small` | [`Array`](./Arrays.md#array-floor2_small) | `[ 1, 9 ]` |  |
| `SmallAttic` | [`Array`](./Arrays.md#array-smallattic) | `[ 0, 9 ]` |  |

</details>

---

### Context: `aux_positions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ButchBox` | [`Array`](./Arrays.md#array-butchbox) | `[ 21, 0 ], [ 38, 0 ]` |  |
| `HousePipe` | [`Array`](./Arrays.md#array-housepipe) | `[ -2 0 ]` |  |
| `Roof_LeftEdge` | [`Array`](./Arrays.md#array-roof_leftedge) | `[ -3.482 16.11 ], [ -3.617 8.112 ], [ -3.388 8.138 ]` |  |
| `Roof_RightEdge` | [`Array`](./Arrays.md#array-roof_rightedge) | `[ 21.548 8.175 ], [ 38.518 8.207 ], [ 38.408 16.185 ]` |  |
| `Roof_Top` | [`Array`](./Arrays.md#array-roof_top) | `[ 17.563 18.677 ], [ 8.983 14.4 ], [ 17.562 26.715 ]` |  |
| `StraySpawn` | [`Array`](./Arrays.md#array-strayspawn) | `[ -3 0 ]` |  |

</details>

---

### Context: `reverb_full`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | [`Enum/String`](./Enums.md#enum-amount) | `.25` |  |
| `preset` | [`Enum/String`](./Enums.md#enum-preset) | `LIVINGROOM` |  |

</details>

---

### Context: `SpawnVolcanoOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Sprout, PunchingBag, MiniVolcano` |  |
| `max_radius` | Number | `2.2` |  |
| `min_radius` | Number | `1, .2` |  |
| `puddle_tile` | [`Enum/String`](./Enums.md#enum-puddle_tile) | `LavaTile, [ BrambleTile TallBrambleTile ]` |  |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 3 5 ]` |  |

</details>

---

### Context: `SmallAttic`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `extra_bound_planes` | [`Array`](./Arrays.md#array-extra_bound_planes) | `[ { p [ 0 0 ]` |  |
| `height` | Number | `5` |  |
| `id` | [`Enum/String`](./Enums.md#enum-id) | `Attic` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `attic` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundSmallAttic` |  |
| `n` | [`Array`](./Arrays.md#array-n) | `[ 1 -2 ]` |  |
| `width` | Number | `18` |  |

</details>

---

### Context: `Floor1_Large`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `height` | Number | `7` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `room1` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundLargeF1` |  |
| `reverb_empty` | [`Block`](./House_and_Environment.md#context-reverb_empty) | `{ ... }` |  |
| `reverb_full` | [`Block`](./House_and_Environment.md#context-reverb_full) | `{ ... }` |  |
| `width` | Number | `16` |  |

</details>

---

### Context: `Floor1_Small`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `height` | Number | `7` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `room2` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundSmallF1` |  |
| `reverb_empty` | [`Block`](./House_and_Environment.md#context-reverb_empty) | `{ ... }` |  |
| `reverb_full` | [`Block`](./House_and_Environment.md#context-reverb_full) | `{ ... }` |  |
| `width` | Number | `16` |  |

</details>

---

### Context: `House1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aux_positions` | [`Block`](./House_and_Environment.md#context-aux_positions) | `{ ... }` |  |
| `bg_placements_frame` | [`Enum/String`](./Enums.md#enum-bg_placements_frame) | `small` |  |
| `movieclip_bg` | [`Enum/String`](./Enums.md#enum-movieclip_bg) | `HouseBackground1` |  |
| `movieclip_fg` | [`Enum/String`](./Enums.md#enum-movieclip_fg) | `HouseForeground1` |  |
| `room_positions` | [`Block`](./House_and_Environment.md#context-room_positions) | `{ ... }` |  |
| `zoomout_catvolume` | [`Enum/String`](./Enums.md#enum-zoomout_catvolume) | `.8` |  |

</details>

---

### Context: `House2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aux_positions` | [`Block`](./House_and_Environment.md#context-aux_positions) | `{ ... }` |  |
| `bg_placements_frame` | [`Enum/String`](./Enums.md#enum-bg_placements_frame) | `large` |  |
| `movieclip_bg` | [`Enum/String`](./Enums.md#enum-movieclip_bg) | `HouseBackground2` |  |
| `movieclip_fg` | [`Enum/String`](./Enums.md#enum-movieclip_fg) | `HouseForeground2` |  |
| `room_positions` | [`Block`](./House_and_Environment.md#context-room_positions) | `{ ... }` |  |
| `zoomout_catvolume` | [`Enum/String`](./Enums.md#enum-zoomout_catvolume) | `.7` |  |

</details>

---

### Context: `House3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aux_positions` | [`Block`](./House_and_Environment.md#context-aux_positions) | `{ ... }` |  |
| `bg_placements_frame` | [`Enum/String`](./Enums.md#enum-bg_placements_frame) | `large` |  |
| `movieclip_bg` | [`Enum/String`](./Enums.md#enum-movieclip_bg) | `HouseBackground3` |  |
| `movieclip_fg` | [`Enum/String`](./Enums.md#enum-movieclip_fg) | `HouseForeground3` |  |
| `room_positions` | [`Block`](./House_and_Environment.md#context-room_positions) | `{ ... }` |  |
| `zoomout_catvolume` | [`Enum/String`](./Enums.md#enum-zoomout_catvolume) | `.6` |  |

</details>

---

### Context: `Thunderstorm`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Thunderstorm` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_heavyrain.ogg` |  |
| `lightning_fx` | Boolean | `true` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ Thunderstorm ]` |  |
| `prewarm` | Number | `5` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_thunderstorm` |  |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `any` |  |
| `Conditional_Flying` | Block | `{ ... }` |  |
| `Else` | [`Block`](./House_and_Environment.md#context-else) | `{ ... }` |  |
| `Stealth` | Number | `1` |  |

</details>

---

### Context: `Rain`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Rain` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_rain.ogg` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ Rain ]` |  |
| `prewarm` | Number | `5` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_rain` |  |

</details>

---

### Context: `Snow`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Snow` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_snow.ogg` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ Snow ]` |  |
| `prewarm` | Number | `20` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_snow` |  |

</details>

---

### Context: `Windy`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Windy` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_windy.ogg` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ WindFull ]` |  |
| `prewarm` | Number | `5` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_windy` |  |

</details>

---

### Context: `Big`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`SpecialGodRays`](./House_and_Environment.md#context-specialgodrays)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `follow_character_tag` | [`Enum/String`](./Enums.md#enum-follow_character_tag) | `zaratana` |  |
| `position` | [`Array`](./Arrays.md#array-position) | `[ 4.5 4.5 ]` |  |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusCharactersOnRoundEnd`](./House_and_Environment.md#context-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `25%, .5` |  |
| `Conditional_Corpse` | [`Block`](./House_and_Environment.md#context-conditional_corpse) | `{ ... }` |  |
| `RandomStatusFromPool` | [`Block`](./House_and_Environment.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllyInfested` | [`Block`](./House_and_Environment.md#context-allyinfested) | `{ ... }` |  |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .25 ]` |  |
| `Poison` | [`Array`](./Arrays.md#array-poison) | `[ 1 .25 ]` |  |
| `RandomStatusFromPool` | [`Block`](./House_and_Environment.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `StatusCharactersOnRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | [`Block`](./House_and_Environment.md#context-conditional_goodroll) | `{ ... }` |  |
| `FloatingRockTrap` | Number | `1` |  |
| `Thorns` | Number | `1` |  |
| `tag_filter` | [`Enum/String`](./Enums.md#enum-tag_filter) | `rock` |  |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`extra_statuses`](./House_and_Environment.md#context-extra_statuses)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddExtraTurnsBeforeRun` | Number | `2` |  |
| `ApplyPassives` | [`Block`](./House_and_Environment.md#context-applypassives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bonusbird` |  |

</details>

---

### Context: `GlobalSpawnOnRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `NeutralTwister, NeutralZombieKitten` |  |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 1 2 ]` |  |

</details>

---

### Context: `SolarFlare`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `5` |  |
| `effects` | [`Block`](./House_and_Environment.md#context-effects) | `{ ... }` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |

</details>

---

### Context: `SpawnTilePuddleOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max_radius` | Number | `3.5` |  |
| `min_radius` | Number | `1.5` |  |
| `tile` | [`Enum/String`](./Enums.md#enum-tile) | `OilTile` |  |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_PartyMember` | [`Block`](./House_and_Environment.md#context-conditional_partymember) | `{ ... }` |  |
| `Conditional_Tiny` | Block | `{ ... }` |  |
| `Else` | [`Block`](./House_and_Environment.md#context-else) | `{ ... }` |  |

</details>

---

### Context: `StatusCharactersOnRoundStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | [`Block`](./House_and_Environment.md#context-conditional_goodroll) | `{ ... }` |  |
| `Else` | [`Block`](./House_and_Environment.md#context-else) | `{ ... }` |  |
| `Madness` | [`Array`](./Arrays.md#array-madness) | `[ 1 .25 ]` |  |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`FactionUprising`](./House_and_Environment.md#context-factionuprising)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` |  |
| `Conditional_HasTag` | [`Block`](./House_and_Environment.md#context-conditional_hastag) | `{ ... }` |  |
| `HealthGain` | Number | `8` |  |

</details>

---

### Context: `AddPostProcessEffect`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean | `false` |  |
| `shader` | [`Enum/String`](./Enums.md#enum-shader) | `shimmervignette` |  |

</details>

---

### Context: `AllyInfested`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./House_and_Environment.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `allies` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedMaggot` |  |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember`](./House_and_Environment.md#context-conditional_partymember)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddInitiative` | Number | `999` |  |
| `StatusOnBattleEnd` | [`Block`](./House_and_Environment.md#context-statusonbattleend) | `{ ... }` |  |

</details>

---

### Context: `BasementUpgrade`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `MediumHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement0` |  |

</details>

---

### Context: `BasementUpgrade2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement1` |  |

</details>

---

### Context: `BasementUpgrade3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade2` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement2` |  |

</details>

---

### Context: `BasementUpgrade4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade3` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement3` |  |

</details>

---

### Context: `BasementUpgrade5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade4` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement4` |  |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `5` |  |
| `Revive` | Number | `50%` |  |

</details>

---

### Context: `Default`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `set_house` | [`Enum/String`](./Enums.md#enum-set_house) | `House1` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor1_Large` |  |

</details>

---

### Context: `FactionUprising`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `extra_statuses` | [`Block`](./House_and_Environment.md#context-extra_statuses) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `LargeHouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `MediumHouse` |  |
| `set_house` | [`Enum/String`](./Enums.md#enum-set_house) | `House3` |  |

</details>

---

### Context: `LargeHouse_Floor2Large`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `LargeHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor2_Large` |  |

</details>

---

### Context: `LargeHouse_Floor2Small`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `LargeHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor2_Small` |  |

</details>

---

### Context: `MediumHouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `Default` |  |
| `set_house` | [`Enum/String`](./Enums.md#enum-set_house) | `House2` |  |

</details>

---

### Context: `MediumHouse_SmallRoom`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `MediumHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor1_Small` |  |

</details>

---

### Context: `SmallHouse_Attic`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `Default` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Attic` |  |

</details>

---

### Context: `SpecialGodRays`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Big` | [`Block`](./House_and_Environment.md#context-big) | `{ ... }` |  |

</details>

---

### Context: `AddTilesetObjects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FloatingDebris` | [`Block`](./House_and_Environment.md#context-floatingdebris) | `{ ... }` |  |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyPassives` | [`Block`](./House_and_Environment.md#context-applypassives) | `{ ... }` |  |

</details>

---

### Context: `FloatingDebris`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddTilesetObjects`](./House_and_Environment.md#context-addtilesetobjects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `20` |  |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ApplyPassives`](./House_and_Environment.md#context-applypassives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | `1` |  |

</details>

---

