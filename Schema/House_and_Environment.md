# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## House & Environment

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/59) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 59 |
| `name` | String |  | 59 |
| [`effects`](./House_and_Environment.md#context-effects) | Block |  | 58 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum/String |  | 13 |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array |  | 12 |
| `height` | Number |  | 8 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum/String |  | 8 |
| `width` | Number |  | 8 |
| [`reverb_empty`](./House_and_Environment.md#context-reverb_empty) | Block |  | 7 |
| [`reverb_full`](./House_and_Environment.md#context-reverb_full) | Block |  | 7 |
| [`amount`](./Enums.md#enum-amount) | Enum/String |  | 4 |
| [`preset`](./Enums.md#enum-preset) | Enum/String |  | 4 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum/String |  | 3 |
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
| [`id`](./Enums.md#enum-id) | Enum/String |  | 1 |
| [`p`](./Arrays.md#array-p) | Array |  | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`SolarFlare`](./House_and_Environment.md#context-solarflare)

| Property Key | Type | Definition | Count (X/28) |
| :--- | :--- | :--- | :--- |
| [`SpawnExtraThingsOnBattleStart`](./House_and_Environment.md#context-spawnextrathingsonbattlestart) | Block |  | 28 |
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum/String |  | 4 |
| `LowerAmbientLight` | Number |  | 4 |
| `Rain` | Number |  | 4 |
| `Windy` | Number |  | 4 |
| `Meteornado` | Number |  | 3 |
| [`SpawnVolcanoOnBattleStart`](./House_and_Environment.md#context-spawnvolcanoonbattlestart) | Block |  | 3 |
| [`StatusCharactersOnRoundEnd`](./House_and_Environment.md#context-statuscharactersonroundend) | Block |  | 3 |
| [`CharacterTypeGainsStatusAtBattleStart`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart) | Block |  | 2 |
| `FireStorm` | Number |  | 2 |
| [`GlobalSpawnOnRoundEnd`](./House_and_Environment.md#context-globalspawnonroundend) | Block |  | 2 |
| `RandomLightning` | Number |  | 2 |
| `Snow` | Number |  | 2 |
| [`SpecialGodRays`](./House_and_Environment.md#context-specialgodrays) | Block |  | 2 |
| [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn) | Block |  | 2 |
| [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart) | Block |  | 2 |
| `AcidRain` | Number |  | 1 |
| [`AddPostProcessEffect`](./House_and_Environment.md#context-addpostprocesseffect) | Block |  | 1 |
| [`AddTilesetObjects`](./House_and_Environment.md#context-addtilesetobjects) | Block |  | 1 |
| `Blind` | Number |  | 1 |
| `Burn` | Number |  | 1 |
| `ButterflySwarm` | Number |  | 1 |
| `ClearDefaultDebris` | Number |  | 1 |
| `CockroachSwarm` | Number |  | 1 |
| `DeleteInanimateObjectsChance` | Number |  | 1 |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum/String |  | 1 |
| `FireflySwarm` | Number |  | 1 |
| `FlySwarm` | Number |  | 1 |
| `Fog` | Number |  | 1 |
| `GlobalHealthRegenAura` | Number |  | 1 |
| `HeatWave` | Number |  | 1 |
| `JudgementDay` | Number |  | 1 |
| `LowGravityKnockbackBoost` | Number |  | 1 |
| `LowGravityRangeBoost` | Number |  | 1 |
| `MeteorShower` | Number |  | 1 |
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum/String |  | 1 |
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array |  | 1 |
| `Sandstorm` | Number |  | 1 |
| [`SolarFlare`](./House_and_Environment.md#context-solarflare) | Block |  | 1 |
| [`SpawnTilePuddleOnBattleStart`](./House_and_Environment.md#context-spawntilepuddleonbattlestart) | Block |  | 1 |
| `VisualFlySwarm` | Number |  | 1 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/27) |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 27 |
| [`object`](./Arrays.md#array-object) | Array |  | 19 |
| [`tile`](./Enums.md#enum-tile) | Enum/String |  | 7 |
| [`trap`](./Enums.md#enum-trap) | Enum/String |  | 2 |

</details>

---

### Context: `reverb_empty`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`amount`](./Enums.md#enum-amount) | Enum/String |  | 9 |
| [`preset`](./Enums.md#enum-preset) | Enum/String |  | 9 |
| `volume_adjustment` | Number |  | 9 |

</details>

---

### Context: `reverb_full`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`amount`](./Enums.md#enum-amount) | Enum/String |  | 9 |
| [`preset`](./Enums.md#enum-preset) | Enum/String |  | 9 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll), [`Else`](./House_and_Environment.md#context-else)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `RandomStatDown` | Number |  | 4 |
| `RandomStatUp` | Number |  | 4 |
| `Bleed` | Number |  | 1 |
| `Blind` | Number |  | 1 |
| `Brace` | Number |  | 1 |
| `Bruise` | Number |  | 1 |
| `DamageUp` | Number |  | 1 |
| `DivineShield` | Number |  | 1 |
| `Drowsy` | Number |  | 1 |
| `KineticSpikes` | Number |  | 1 |
| `Poison` | Number |  | 1 |
| `Shield` | Number |  | 1 |
| `Slow` | Number |  | 1 |
| `SpellDamageUp` | Number |  | 1 |
| `Thorns` | Number |  | 1 |
| `Weakness` | Number |  | 1 |

</details>

---

### Context: `SpawnVolcanoOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 3 |
| `max_radius` | Number |  | 2 |
| `min_radius` | Number |  | 2 |
| [`puddle_tile`](./Enums.md#enum-puddle_tile) | Enum/String |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Context: `aux_positions`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Definition | Count (X/3) |
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

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Definition | Count (X/3) |
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

### Context: `Big`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpecialGodRays`](./House_and_Environment.md#context-specialgodrays)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`follow_character_tag`](./Enums.md#enum-follow_character_tag) | Enum/String |  | 2 |
| [`position`](./Arrays.md#array-position) | Array |  | 2 |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 2 |
| `Conditional_Flying` | Block |  | 1 |
| [`Else`](./House_and_Environment.md#context-else) | Block |  | 1 |
| `Stealth` | Number |  | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusCharactersOnRoundEnd`](./House_and_Environment.md#context-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Enum/String |  | 2 |
| [`Conditional_Corpse`](./House_and_Environment.md#context-conditional_corpse) | Block |  | 1 |
| [`RandomStatusFromPool`](./House_and_Environment.md#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `GlobalSpawnOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 2 |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |

</details>

---

### Context: `SpecialGodRays`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Big`](./House_and_Environment.md#context-big) | Block |  | 2 |

</details>

---

### Context: `AddPostProcessEffect`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean |  | 1 |
| [`shader`](./Enums.md#enum-shader) | Enum/String |  | 1 |

</details>

---

### Context: `AddTilesetObjects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`FloatingDebris`](./House_and_Environment.md#context-floatingdebris) | Block |  | 1 |

</details>

---

### Context: `AllyInfested`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./House_and_Environment.md#context-else)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum/String |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember`](./House_and_Environment.md#context-conditional_partymember)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddInitiative` | Number |  | 1 |
| [`StatusOnBattleEnd`](./House_and_Environment.md#context-statusonbattleend) | Block |  | 1 |

</details>

---

### Context: `BasementUpgrade`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `BasementUpgrade2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `BasementUpgrade3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `BasementUpgrade4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `BasementUpgrade5`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Madness` | Number |  | 1 |
| `Revive` | Number |  | 1 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`extra_statuses`](./House_and_Environment.md#context-extra_statuses)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddExtraTurnsBeforeRun` | Number |  | 1 |
| [`ApplyPassives`](./House_and_Environment.md#context-applypassives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ApplyPassives`](./House_and_Environment.md#context-applypassives) | Block |  | 1 |

</details>

---

### Context: `Default`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`set_house`](./Enums.md#enum-set_house) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`AllyInfested`](./House_and_Environment.md#context-allyinfested) | Block |  | 1 |
| [`Fear`](./Arrays.md#array-fear) | Array |  | 1 |
| [`Poison`](./Arrays.md#array-poison) | Array |  | 1 |
| [`RandomStatusFromPool`](./House_and_Environment.md#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `FactionUprising`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`extra_statuses`](./House_and_Environment.md#context-extra_statuses) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `FloatingDebris`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTilesetObjects`](./House_and_Environment.md#context-addtilesetobjects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `count` | Number |  | 1 |

</details>

---

### Context: `Floor1_Large`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `height` | Number |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum/String |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum/String |  | 1 |
| [`reverb_empty`](./House_and_Environment.md#context-reverb_empty) | Block |  | 1 |
| [`reverb_full`](./House_and_Environment.md#context-reverb_full) | Block |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `Floor1_Small`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `height` | Number |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum/String |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum/String |  | 1 |
| [`reverb_empty`](./House_and_Environment.md#context-reverb_empty) | Block |  | 1 |
| [`reverb_full`](./House_and_Environment.md#context-reverb_full) | Block |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `House1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](./House_and_Environment.md#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum/String |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum/String |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum/String |  | 1 |
| [`room_positions`](./House_and_Environment.md#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum/String |  | 1 |

</details>

---

### Context: `House2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](./House_and_Environment.md#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum/String |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum/String |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum/String |  | 1 |
| [`room_positions`](./House_and_Environment.md#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum/String |  | 1 |

</details>

---

### Context: `House3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`aux_positions`](./House_and_Environment.md#context-aux_positions) | Block |  | 1 |
| [`bg_placements_frame`](./Enums.md#enum-bg_placements_frame) | Enum/String |  | 1 |
| [`movieclip_bg`](./Enums.md#enum-movieclip_bg) | Enum/String |  | 1 |
| [`movieclip_fg`](./Enums.md#enum-movieclip_fg) | Enum/String |  | 1 |
| [`room_positions`](./House_and_Environment.md#context-room_positions) | Block |  | 1 |
| [`zoomout_catvolume`](./Enums.md#enum-zoomout_catvolume) | Enum/String |  | 1 |

</details>

---

### Context: `LargeHouse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`set_house`](./Enums.md#enum-set_house) | Enum/String |  | 1 |

</details>

---

### Context: `LargeHouse_Floor2Large`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `LargeHouse_Floor2Small`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `MediumHouse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`set_house`](./Enums.md#enum-set_house) | Enum/String |  | 1 |

</details>

---

### Context: `MediumHouse_SmallRoom`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `Rain`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum/String |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum/String |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum/String |  | 1 |

</details>

---

### Context: `SmallAttic`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`extra_bound_planes`](./Arrays.md#array-extra_bound_planes) | Array |  | 1 |
| `height` | Number |  | 1 |
| [`id`](./Enums.md#enum-id) | Enum/String |  | 1 |
| [`interstitial_bg_frame`](./Enums.md#enum-interstitial_bg_frame) | Enum/String |  | 1 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum/String |  | 1 |
| [`n`](./Arrays.md#array-n) | Array |  | 1 |
| `width` | Number |  | 1 |

</details>

---

### Context: `SmallHouse_Attic`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`prereq`](./Enums.md#enum-prereq) | Enum/String |  | 1 |
| [`unlock_room`](./Enums.md#enum-unlock_room) | Enum/String |  | 1 |

</details>

---

### Context: `Snow`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum/String |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum/String |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum/String |  | 1 |

</details>

---

### Context: `SolarFlare`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 1 |
| [`effects`](./House_and_Environment.md#context-effects) | Block |  | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `SpawnTilePuddleOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `max_radius` | Number |  | 1 |
| `min_radius` | Number |  | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum/String |  | 1 |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](./House_and_Environment.md#context-conditional_partymember) | Block |  | 1 |
| `Conditional_Tiny` | Block |  | 1 |
| [`Else`](./House_and_Environment.md#context-else) | Block |  | 1 |

</details>

---

### Context: `StatusCharactersOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll) | Block |  | 1 |
| `FloatingRockTrap` | Number |  | 1 |
| `Thorns` | Number |  | 1 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum/String |  | 1 |

</details>

---

### Context: `StatusCharactersOnRoundStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll) | Block |  | 1 |
| [`Else`](./House_and_Environment.md#context-else) | Block |  | 1 |
| [`Madness`](./Arrays.md#array-madness) | Array |  | 1 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./House_and_Environment.md#context-applypassives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number |  | 1 |

</details>

---

### Context: `Thunderstorm`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum/String |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum/String |  | 1 |
| `lightning_fx` | Boolean |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum/String |  | 1 |

</details>

---

### Context: `Windy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum/String |  | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum/String |  | 1 |
| [`particles`](./Arrays.md#array-particles) | Array |  | 1 |
| `prewarm` | Number |  | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum/String |  | 1 |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FactionUprising`](./House_and_Environment.md#context-factionuprising)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number |  | 1 |
| [`Conditional_HasTag`](./House_and_Environment.md#context-conditional_hastag) | Block |  | 1 |
| `HealthGain` | Number |  | 1 |

</details>

---

