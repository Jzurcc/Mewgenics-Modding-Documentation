# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** Some keys labeled as `Number` actually support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Map Generation & Routing

> **Associated Files:** `data/maps/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 39

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effects}`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`boss`](#context-boss) | Block |  | 39 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 27 |
| [`easy`](./Arrays.md#array-easy) | Array |  | 20 |
| [`folder`](./Enums.md#enum-folder) | Enum |  | 20 |
| [`hard`](./Arrays.md#array-hard) | Array |  | 20 |
| [`miniboss`](./Arrays.md#array-miniboss) | Array |  | 20 |
| [`normal`](./Arrays.md#array-normal) | Array |  | 20 |
| [`rare`](./Arrays.md#array-rare) | Array |  | 20 |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum |  | 19 |
| [`large`](./Arrays.md#array-large) | Array |  | 19 |
| [`medium`](./Arrays.md#array-medium) | Array |  | 19 |
| [`small`](./Arrays.md#array-small) | Array |  | 19 |
| [`special`](./Arrays.md#array-special) | Array |  | 19 |
| [`exit0`](#context-exit0) | Block |  | 15 |
| [`level`](./Enums.md#enum-level) | Enum |  | 12 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 12 |
| [`quest_event`](#context-quest_event) | Block |  | 9 |
| [`time_machine`](#context-time_machine) | Block |  | 4 |
| [`exit1`](#context-exit1) | Block |  | 3 |
| [`jestercat`](./Enums.md#enum-jestercat) | Enum |  | 3 |
| [`BothObelisksUnlocked`](#context-bothobelisksunlocked) | Block | Applies or references the 'BothObelisksUnlocked' effect/state. | 2 |
| [`DimensionXUnlocked`](#context-dimensionxunlocked) | Block | Applies or references the 'DimensionXUnlocked' effect/state. | 2 |
| [`EndOfTimeUnlocked`](#context-endoftimeunlocked) | Block | Applies or references the 'EndOfTimeUnlocked' effect/state. | 2 |
| [`HardPathUnlocked`](#context-hardpathunlocked) | Block | Applies or references the 'HardPathUnlocked' effect/state. | 2 |
| [`MeatWorldUnlocked`](#context-meatworldunlocked) | Block | Applies or references the 'MeatWorldUnlocked' effect/state. | 2 |
| [`VolcanoAntennaAttached`](#context-volcanoantennaattached) | Block | Applies or references the 'VolcanoAntennaAttached' effect/state. | 2 |
| [`hard_initial`](#context-hard_initial) | Block |  | 2 |
| [`BoneyardUnlocked`](#context-boneyardunlocked) | Block | Applies or references the 'BoneyardUnlocked' effect/state. | 1 |
| [`BunkerUnlocked`](#context-bunkerunlocked) | Block | Applies or references the 'BunkerUnlocked' effect/state. | 1 |
| [`CavesUnlocked`](#context-cavesunlocked) | Block | Applies or references the 'CavesUnlocked' effect/state. | 1 |
| [`ChaosAntennaAttached`](#context-chaosantennaattached) | Block | Applies or references the 'ChaosAntennaAttached' effect/state. | 1 |
| [`CoreObeliskUnlocked`](#context-coreobeliskunlocked) | Block | Applies or references the 'CoreObeliskUnlocked' effect/state. | 1 |
| [`CoreUnlocked`](#context-coreunlocked) | Block | Applies or references the 'CoreUnlocked' effect/state. | 1 |
| [`CraterUnlocked`](#context-craterunlocked) | Block | Applies or references the 'CraterUnlocked' effect/state. | 1 |
| [`FutureUnlocked`](#context-futureunlocked) | Block | Applies or references the 'FutureUnlocked' effect/state. | 1 |
| [`GenFlag_Boss_Spewer`](#context-genflag_boss_spewer) | Block | Applies or references the 'GenFlag_Boss_Spewer' effect/state. | 1 |
| [`GenFlag_Boss_Stacy`](#context-genflag_boss_stacy) | Block | Applies or references the 'GenFlag_Boss_Stacy' effect/state. | 1 |
| [`IceAgeUnlocked`](#context-iceageunlocked) | Block | Applies or references the 'IceAgeUnlocked' effect/state. | 1 |
| [`JunkyardUnlocked`](#context-junkyardunlocked) | Block | Applies or references the 'JunkyardUnlocked' effect/state. | 1 |
| [`JurassicUnlocked`](#context-jurassicunlocked) | Block | Applies or references the 'JurassicUnlocked' effect/state. | 1 |
| [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull) | Block | Applies or references the 'MeatWorldUnlockedFull' effect/state. | 1 |
| [`MoonObeliskUnlocked`](#context-moonobeliskunlocked) | Block | Applies or references the 'MoonObeliskUnlocked' effect/state. | 1 |
| [`MoonUnlocked`](#context-moonunlocked) | Block | Applies or references the 'MoonUnlocked' effect/state. | 1 |
| [`SewersUnlocked`](#context-sewersunlocked) | Block | Applies or references the 'SewersUnlocked' effect/state. | 1 |
| [`TheEndUnlocked`](#context-theendunlocked) | Block | Applies or references the 'TheEndUnlocked' effect/state. | 1 |
| [`ThrobbingArteryDone`](#context-throbbingarterydone) | Block | Applies or references the 'ThrobbingArteryDone' effect/state. | 1 |
| [`WallOfFleshDone`](#context-walloffleshdone) | Block | Applies or references the 'WallOfFleshDone' effect/state. | 1 |
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum |  | 1 |
| `advance` | Number |  | 1 |
| `alley` | Block |  | 1 |
| [`battle`](#context-battle) | Block |  | 1 |
| `boneyard` | Block |  | 1 |
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum |  | 1 |
| `bunker` | Block |  | 1 |
| [`butchercat`](./Enums.md#enum-butchercat) | Enum |  | 1 |
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum |  | 1 |
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum |  | 1 |
| `caves` | Block |  | 1 |
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum |  | 1 |
| [`choose_one`](./Arrays.md#array-choose_one) | Array |  | 1 |
| [`clericcat`](./Enums.md#enum-clericcat) | Enum |  | 1 |
| `core` | Block |  | 1 |
| `crater` | Block |  | 1 |
| `desert` | Block |  | 1 |
| [`dimensionx`](#context-dimensionx) | Block |  | 1 |
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum |  | 1 |
| [`drmangler`](./Enums.md#enum-drmangler) | Enum |  | 1 |
| [`druidcat`](./Enums.md#enum-druidcat) | Enum |  | 1 |
| [`endoftime`](#context-endoftime) | Block |  | 1 |
| [`event`](#context-event) | Block |  | 1 |
| [`exit_desert`](#context-exit_desert) | Block |  | 1 |
| [`exit_lab`](#context-exit_lab) | Block |  | 1 |
| [`fightercat`](./Enums.md#enum-fightercat) | Enum |  | 1 |
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum |  | 1 |
| [`future`](#context-future) | Block |  | 1 |
| [`gambit`](./Enums.md#enum-gambit) | Enum |  | 1 |
| `head_start` | Number |  | 1 |
| [`home`](#context-home) | Block |  | 1 |
| [`huntercat`](./Enums.md#enum-huntercat) | Enum |  | 1 |
| [`iceage`](#context-iceage) | Block |  | 1 |
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum |  | 1 |
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum |  | 1 |
| `junkyard` | Block |  | 1 |
| [`jurassic`](#context-jurassic) | Block |  | 1 |
| `lab` | Block |  | 1 |
| [`lenny`](./Enums.md#enum-lenny) | Enum |  | 1 |
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum |  | 1 |
| `locked` | Boolean |  | 1 |
| [`magecat`](./Enums.md#enum-magecat) | Enum |  | 1 |
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum |  | 1 |
| `meatworld` | Block |  | 1 |
| [`miniboss_event`](#context-miniboss_event) | Block |  | 1 |
| [`monkcat`](./Enums.md#enum-monkcat) | Enum |  | 1 |
| `moon` | Block |  | 1 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum |  | 1 |
| [`mw_altar`](#context-mw_altar) | Block |  | 1 |
| [`mw_battle1`](#context-mw_battle1) | Block |  | 1 |
| [`mw_boss`](#context-mw_boss) | Block |  | 1 |
| [`mw_earlyhome`](#context-mw_earlyhome) | Block |  | 1 |
| [`mw_event1`](#context-mw_event1) | Block |  | 1 |
| [`mw_hard1`](#context-mw_hard1) | Block |  | 1 |
| [`mw_home`](#context-mw_home) | Block |  | 1 |
| [`mw_quest_event`](#context-mw_quest_event) | Block |  | 1 |
| [`mw_treasure`](#context-mw_treasure) | Block |  | 1 |
| [`necrocat`](./Enums.md#enum-necrocat) | Enum |  | 1 |
| [`nemesis`](./Arrays.md#array-nemesis) | Array |  | 1 |
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum |  | 1 |
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum |  | 1 |
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum |  | 1 |
| [`ratking`](./Enums.md#enum-ratking) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum |  | 1 |
| `sewers` | Block |  | 1 |
| [`shop_cheapwater`](#context-shop_cheapwater) | Block |  | 1 |
| [`shop_water`](#context-shop_water) | Block |  | 1 |
| [`slime`](./Enums.md#enum-slime) | Enum |  | 1 |
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum |  | 1 |
| [`spewer`](./Enums.md#enum-spewer) | Enum |  | 1 |
| [`stacy`](./Enums.md#enum-stacy) | Enum |  | 1 |
| [`start`](#context-start) | Block |  | 1 |
| [`tankcat`](./Enums.md#enum-tankcat) | Enum |  | 1 |
| [`thebloat`](./Enums.md#enum-thebloat) | Enum |  | 1 |
| [`theend`](#context-theend) | Block |  | 1 |
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum |  | 1 |
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum |  | 1 |
| [`trampy`](./Enums.md#enum-trampy) | Enum |  | 1 |
| [`treasure`](#context-treasure) | Block |  | 1 |
| [`weather_event`](#context-weather_event) | Block |  | 1 |
| [`zodiac`](./Enums.md#enum-zodiac) | Enum |  | 1 |

</details>

---

### Context: `boss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 41

> **Referenced by:** [`GenFlag_Boss_Spewer`](#context-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](#context-genflag_boss_stacy), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 19 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum |  | 16 |
| `is_final_boss` | Boolean |  | 2 |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`override_music`](./Enums.md#enum-override_music) | Enum |  | 2 |
| [`tileset`](./Enums.md#enum-tileset) | Enum |  | 1 |
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum |  | 1 |

</details>

---

### Context: `exit0`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 27

> **Referenced by:** [`BoneyardUnlocked`](#context-boneyardunlocked), [`BunkerUnlocked`](#context-bunkerunlocked), [`CavesUnlocked`](#context-cavesunlocked), [`CoreUnlocked`](#context-coreunlocked), [`EndOfTimeUnlocked`](#context-endoftimeunlocked), [`JurassicUnlocked`](#context-jurassicunlocked), [`MeatWorldUnlocked`](#context-meatworldunlocked), [`MoonUnlocked`](#context-moonunlocked), [`ROOT`](#context-root), [`SewersUnlocked`](#context-sewersunlocked), [`TheEndUnlocked`](#context-theendunlocked)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 17 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 15 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 15 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 15 |
| `hidden` | Boolean |  | 10 |

</details>

---

### Context: `quest_event`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 24

> **Referenced by:** [`BothObelisksUnlocked`](#context-bothobelisksunlocked), [`ChaosAntennaAttached`](#context-chaosantennaattached), [`CoreObeliskUnlocked`](#context-coreobeliskunlocked), [`DimensionXUnlocked`](#context-dimensionxunlocked), [`FutureUnlocked`](#context-futureunlocked), [`IceAgeUnlocked`](#context-iceageunlocked), [`MeatWorldUnlocked`](#context-meatworldunlocked), [`MoonObeliskUnlocked`](#context-moonobeliskunlocked), [`ROOT`](#context-root), [`ThrobbingArteryDone`](#context-throbbingarterydone), [`VolcanoAntennaAttached`](#context-volcanoantennaattached), [`WallOfFleshDone`](#context-walloffleshdone)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 24 |
| [`level`](./Enums.md#enum-level) | Enum |  | 19 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 11 |

</details>

---

### Context: `exit1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`CraterUnlocked`](#context-craterunlocked), [`JunkyardUnlocked`](#context-junkyardunlocked), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 5 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 3 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 3 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 3 |

</details>

---

### Context: `hard_initial`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`HardPathUnlocked`](#context-hardpathunlocked), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Context: `time_machine`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 4 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 |

</details>

---

### Context: `BothObelisksUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `DimensionXUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `EndOfTimeUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 2 |

</details>

---

### Context: `HardPathUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`hard_initial`](#context-hard_initial) | Block |  | 2 |

</details>

---

### Context: `MeatWorldUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 2 |
| [`quest_event`](#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `VolcanoAntennaAttached`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `miniboss_event`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`GenFlag_Boss_Stacy`](#context-genflag_boss_stacy), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |

</details>

---

### Context: `mw_battle1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `mw_boss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum |  | 1 |
| [`override_music`](./Enums.md#enum-override_music) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `mw_earlyhome`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `mw_event1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `mw_hard1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `mw_home`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `mw_quest_event`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `mw_treasure`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](#context-meatworldunlockedfull), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `BoneyardUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `BunkerUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `CavesUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `ChaosAntennaAttached`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `CoreObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `CoreUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `CraterUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit1`](#context-exit1) | Block |  | 1 |

</details>

---

### Context: `FutureUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `GenFlag_Boss_Spewer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](#context-boss) | Block |  | 1 |

</details>

---

### Context: `GenFlag_Boss_Stacy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](#context-boss) | Block |  | 1 |
| [`miniboss_event`](#context-miniboss_event) | Block |  | 1 |

</details>

---

### Context: `IceAgeUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `JunkyardUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit1`](#context-exit1) | Block |  | 1 |

</details>

---

### Context: `JurassicUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `MeatWorldUnlockedFull`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mw_battle1`](#context-mw_battle1) | Block |  | 1 |
| [`mw_boss`](#context-mw_boss) | Block |  | 1 |
| [`mw_earlyhome`](#context-mw_earlyhome) | Block |  | 1 |
| [`mw_event1`](#context-mw_event1) | Block |  | 1 |
| [`mw_hard1`](#context-mw_hard1) | Block |  | 1 |
| [`mw_home`](#context-mw_home) | Block |  | 1 |
| [`mw_quest_event`](#context-mw_quest_event) | Block |  | 1 |
| [`mw_treasure`](#context-mw_treasure) | Block |  | 1 |

</details>

---

### Context: `MoonObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `MoonUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `SewersUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `TheEndUnlocked`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](#context-exit0) | Block |  | 1 |

</details>

---

### Context: `ThrobbingArteryDone`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `WallOfFleshDone`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `battle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `dimensionx`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `endoftime`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `event`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `exit_desert`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 1 |
| `locked` | Boolean |  | 1 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `exit_lab`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 1 |
| `locked` | Boolean |  | 1 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `future`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `home`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `iceage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `jurassic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `mw_altar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `shop_cheapwater`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `shop_water`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `start`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `theend`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `treasure`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `weather_event`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

