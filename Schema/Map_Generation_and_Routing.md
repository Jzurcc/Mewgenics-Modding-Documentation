# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Map Generation & Routing

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/39) |
| :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Block |  | 39 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 27 |
| [`easy`](./Arrays.md#array-easy) | Array |  | 20 |
| [`folder`](./Enums.md#enum-folder) | Enum/String |  | 20 |
| [`hard`](./Arrays.md#array-hard) | Array |  | 20 |
| [`miniboss`](./Arrays.md#array-miniboss) | Array |  | 20 |
| [`normal`](./Arrays.md#array-normal) | Array |  | 20 |
| [`rare`](./Arrays.md#array-rare) | Array |  | 20 |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum/String |  | 19 |
| [`large`](./Arrays.md#array-large) | Array |  | 19 |
| [`medium`](./Arrays.md#array-medium) | Array |  | 19 |
| [`small`](./Arrays.md#array-small) | Array |  | 19 |
| [`special`](./Arrays.md#array-special) | Array |  | 19 |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 15 |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 12 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 12 |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 9 |
| [`time_machine`](./Map_Generation_and_Routing.md#context-time_machine) | Block |  | 4 |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Block |  | 3 |
| [`jestercat`](./Enums.md#enum-jestercat) | Enum/String |  | 3 |
| [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked) | Block | Applies or references the 'BothObelisksUnlocked' effect/state. | 2 |
| [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked) | Block | Applies or references the 'DimensionXUnlocked' effect/state. | 2 |
| [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked) | Block | Applies or references the 'EndOfTimeUnlocked' effect/state. | 2 |
| [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked) | Block | Applies or references the 'HardPathUnlocked' effect/state. | 2 |
| [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked) | Block | Applies or references the 'MeatWorldUnlocked' effect/state. | 2 |
| [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached) | Block | Applies or references the 'VolcanoAntennaAttached' effect/state. | 2 |
| [`hard_initial`](./Map_Generation_and_Routing.md#context-hard_initial) | Block |  | 2 |
| [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked) | Block | Applies or references the 'BoneyardUnlocked' effect/state. | 1 |
| [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked) | Block | Applies or references the 'BunkerUnlocked' effect/state. | 1 |
| [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked) | Block | Applies or references the 'CavesUnlocked' effect/state. | 1 |
| [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached) | Block | Applies or references the 'ChaosAntennaAttached' effect/state. | 1 |
| [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked) | Block | Applies or references the 'CoreObeliskUnlocked' effect/state. | 1 |
| [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked) | Block | Applies or references the 'CoreUnlocked' effect/state. | 1 |
| [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked) | Block | Applies or references the 'CraterUnlocked' effect/state. | 1 |
| [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked) | Block | Applies or references the 'FutureUnlocked' effect/state. | 1 |
| [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer) | Block | Applies or references the 'GenFlag_Boss_Spewer' effect/state. | 1 |
| [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy) | Block | Applies or references the 'GenFlag_Boss_Stacy' effect/state. | 1 |
| [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked) | Block | Applies or references the 'IceAgeUnlocked' effect/state. | 1 |
| [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked) | Block | Applies or references the 'JunkyardUnlocked' effect/state. | 1 |
| [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked) | Block | Applies or references the 'JurassicUnlocked' effect/state. | 1 |
| [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull) | Block | Applies or references the 'MeatWorldUnlockedFull' effect/state. | 1 |
| [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked) | Block | Applies or references the 'MoonObeliskUnlocked' effect/state. | 1 |
| [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked) | Block | Applies or references the 'MoonUnlocked' effect/state. | 1 |
| [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked) | Block | Applies or references the 'SewersUnlocked' effect/state. | 1 |
| [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked) | Block | Applies or references the 'TheEndUnlocked' effect/state. | 1 |
| [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone) | Block | Applies or references the 'ThrobbingArteryDone' effect/state. | 1 |
| [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone) | Block | Applies or references the 'WallOfFleshDone' effect/state. | 1 |
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum/String |  | 1 |
| `advance` | Number |  | 1 |
| `alley` | Block |  | 1 |
| [`battle`](./Map_Generation_and_Routing.md#context-battle) | Block |  | 1 |
| `boneyard` | Block |  | 1 |
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum/String |  | 1 |
| `bunker` | Block |  | 1 |
| [`butchercat`](./Enums.md#enum-butchercat) | Enum/String |  | 1 |
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum/String |  | 1 |
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum/String |  | 1 |
| `caves` | Block |  | 1 |
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum/String |  | 1 |
| [`choose_one`](./Arrays.md#array-choose_one) | Array |  | 1 |
| [`clericcat`](./Enums.md#enum-clericcat) | Enum/String |  | 1 |
| `core` | Block |  | 1 |
| `crater` | Block |  | 1 |
| `desert` | Block |  | 1 |
| [`dimensionx`](./Map_Generation_and_Routing.md#context-dimensionx) | Block |  | 1 |
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum/String |  | 1 |
| [`drmangler`](./Enums.md#enum-drmangler) | Enum/String |  | 1 |
| [`druidcat`](./Enums.md#enum-druidcat) | Enum/String |  | 1 |
| [`endoftime`](./Map_Generation_and_Routing.md#context-endoftime) | Block |  | 1 |
| [`event`](./Map_Generation_and_Routing.md#context-event) | Block |  | 1 |
| [`exit_desert`](./Map_Generation_and_Routing.md#context-exit_desert) | Block |  | 1 |
| [`exit_lab`](./Map_Generation_and_Routing.md#context-exit_lab) | Block |  | 1 |
| [`fightercat`](./Enums.md#enum-fightercat) | Enum/String |  | 1 |
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum/String |  | 1 |
| [`future`](./Map_Generation_and_Routing.md#context-future) | Block |  | 1 |
| [`gambit`](./Enums.md#enum-gambit) | Enum/String |  | 1 |
| `head_start` | Number |  | 1 |
| [`home`](./Map_Generation_and_Routing.md#context-home) | Block |  | 1 |
| [`huntercat`](./Enums.md#enum-huntercat) | Enum/String |  | 1 |
| [`iceage`](./Map_Generation_and_Routing.md#context-iceage) | Block |  | 1 |
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum/String |  | 1 |
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum/String |  | 1 |
| `junkyard` | Block |  | 1 |
| [`jurassic`](./Map_Generation_and_Routing.md#context-jurassic) | Block |  | 1 |
| `lab` | Block |  | 1 |
| [`lenny`](./Enums.md#enum-lenny) | Enum/String |  | 1 |
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum/String |  | 1 |
| `locked` | Boolean |  | 1 |
| [`magecat`](./Enums.md#enum-magecat) | Enum/String |  | 1 |
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum/String |  | 1 |
| `meatworld` | Block |  | 1 |
| [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event) | Block |  | 1 |
| [`monkcat`](./Enums.md#enum-monkcat) | Enum/String |  | 1 |
| `moon` | Block |  | 1 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum/String |  | 1 |
| [`mw_altar`](./Map_Generation_and_Routing.md#context-mw_altar) | Block |  | 1 |
| [`mw_battle1`](./Map_Generation_and_Routing.md#context-mw_battle1) | Block |  | 1 |
| [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss) | Block |  | 1 |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#context-mw_earlyhome) | Block |  | 1 |
| [`mw_event1`](./Map_Generation_and_Routing.md#context-mw_event1) | Block |  | 1 |
| [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1) | Block |  | 1 |
| [`mw_home`](./Map_Generation_and_Routing.md#context-mw_home) | Block |  | 1 |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event) | Block |  | 1 |
| [`mw_treasure`](./Map_Generation_and_Routing.md#context-mw_treasure) | Block |  | 1 |
| [`necrocat`](./Enums.md#enum-necrocat) | Enum/String |  | 1 |
| [`nemesis`](./Arrays.md#array-nemesis) | Array |  | 1 |
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum/String |  | 1 |
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum/String |  | 1 |
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum/String |  | 1 |
| [`ratking`](./Enums.md#enum-ratking) | Enum/String |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum/String |  | 1 |
| `sewers` | Block |  | 1 |
| [`shop_cheapwater`](./Map_Generation_and_Routing.md#context-shop_cheapwater) | Block |  | 1 |
| [`shop_water`](./Map_Generation_and_Routing.md#context-shop_water) | Block |  | 1 |
| [`slime`](./Enums.md#enum-slime) | Enum/String |  | 1 |
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum/String |  | 1 |
| [`spewer`](./Enums.md#enum-spewer) | Enum/String |  | 1 |
| [`stacy`](./Enums.md#enum-stacy) | Enum/String |  | 1 |
| [`start`](./Map_Generation_and_Routing.md#context-start) | Block |  | 1 |
| [`tankcat`](./Enums.md#enum-tankcat) | Enum/String |  | 1 |
| [`thebloat`](./Enums.md#enum-thebloat) | Enum/String |  | 1 |
| [`theend`](./Map_Generation_and_Routing.md#context-theend) | Block |  | 1 |
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum/String |  | 1 |
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum/String |  | 1 |
| [`trampy`](./Enums.md#enum-trampy) | Enum/String |  | 1 |
| [`treasure`](./Map_Generation_and_Routing.md#context-treasure) | Block |  | 1 |
| [`weather_event`](./Map_Generation_and_Routing.md#context-weather_event) | Block |  | 1 |
| [`zodiac`](./Enums.md#enum-zodiac) | Enum/String |  | 1 |

</details>

---

### Context: `quest_event`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone)

| Property Key | Type | Definition | Count (X/24) |
| :--- | :--- | :--- | :--- |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 24 |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 19 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 11 |

</details>

---

### Context: `boss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/19) |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 19 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum/String |  | 16 |
| `is_final_boss` | Boolean |  | 2 |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 2 |
| [`override_music`](./Enums.md#enum-override_music) | Enum/String |  | 2 |
| [`tileset`](./Enums.md#enum-tileset) | Enum/String |  | 1 |
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum/String |  | 1 |

</details>

---

### Context: `exit0`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked)

| Property Key | Type | Definition | Count (X/17) |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 17 |
| [`next_map`](./Enums.md#enum-next_map) | Enum/String |  | 15 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 15 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 15 |
| `hidden` | Boolean |  | 10 |

</details>

---

### Context: `exit1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 5 |
| [`next_map`](./Enums.md#enum-next_map) | Enum/String |  | 3 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 3 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 3 |

</details>

---

### Context: `hard_initial`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 2 |

</details>

---

### Context: `time_machine`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 4 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 4 |

</details>

---

### Context: `BothObelisksUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `DimensionXUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `EndOfTimeUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 2 |

</details>

---

### Context: `HardPathUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`hard_initial`](./Map_Generation_and_Routing.md#context-hard_initial) | Block |  | 2 |

</details>

---

### Context: `MeatWorldUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 2 |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `VolcanoAntennaAttached`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 2 |

</details>

---

### Context: `miniboss_event`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 2 |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |

</details>

---

### Context: `mw_battle1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `mw_boss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum/String |  | 1 |
| [`override_music`](./Enums.md#enum-override_music) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `mw_event1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `mw_hard1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `mw_home`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `mw_quest_event`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `mw_treasure`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `BoneyardUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `BunkerUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `CavesUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `ChaosAntennaAttached`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `CoreObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `CoreUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `CraterUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Block |  | 1 |

</details>

---

### Context: `FutureUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `GenFlag_Boss_Spewer`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Block |  | 1 |

</details>

---

### Context: `GenFlag_Boss_Stacy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Block |  | 1 |
| [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event) | Block |  | 1 |

</details>

---

### Context: `IceAgeUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `JunkyardUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Block |  | 1 |

</details>

---

### Context: `JurassicUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `MeatWorldUnlockedFull`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`mw_battle1`](./Map_Generation_and_Routing.md#context-mw_battle1) | Block |  | 1 |
| [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss) | Block |  | 1 |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#context-mw_earlyhome) | Block |  | 1 |
| [`mw_event1`](./Map_Generation_and_Routing.md#context-mw_event1) | Block |  | 1 |
| [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1) | Block |  | 1 |
| [`mw_home`](./Map_Generation_and_Routing.md#context-mw_home) | Block |  | 1 |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event) | Block |  | 1 |
| [`mw_treasure`](./Map_Generation_and_Routing.md#context-mw_treasure) | Block |  | 1 |

</details>

---

### Context: `MoonObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `MoonUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `SewersUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `TheEndUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Block |  | 1 |

</details>

---

### Context: `ThrobbingArteryDone`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `WallOfFleshDone`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Block |  | 1 |

</details>

---

### Context: `battle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `dimensionx`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `endoftime`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `event`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `exit_desert`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 1 |
| `locked` | Boolean |  | 1 |
| [`next_map`](./Enums.md#enum-next_map) | Enum/String |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `exit_lab`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 1 |
| `locked` | Boolean |  | 1 |
| [`next_map`](./Enums.md#enum-next_map) | Enum/String |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `future`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `home`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `iceage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `jurassic`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `mw_altar`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `mw_earlyhome`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `shop_cheapwater`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `shop_water`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `start`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `theend`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Context: `treasure`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `weather_event`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum/String |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

