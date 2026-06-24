# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Map Generation & Routing

> **Associated Files:** `data/maps/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 39

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 890 |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Object |  | 39 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 27 |
| [`easy`](./Arrays.md#array-easy) | Array |  | 20 |
| [`folder`](./Enums.md#enum-folder) | Enum |  | 20 |
| [`hard`](./Arrays.md#array-hard) | Array |  | 20 |
| [`miniboss`](./Arrays.md#array-miniboss) | Array |  | 20 |
| [`normal`](./Arrays.md#array-normal) | Array |  | 20 |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum |  | 19 |
| [`include`](./Strings.md#string-include) | String | Examples: `"standard_nodes.gon"` | 19 |
| [`large`](./Arrays.md#array-large) | Array |  | 19 |
| [`medium`](./Arrays.md#array-medium) | Array |  | 19 |
| [`small`](./Arrays.md#array-small) | Array |  | 19 |
| [`special`](./Arrays.md#array-special) | Array |  | 19 |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 15 |
| [`level`](./Enums.md#enum-level) | Enum |  | 12 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 12 |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 9 |
| [`time_machine`](./Map_Generation_and_Routing.md#context-time_machine) | Object |  | 4 |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Object |  | 3 |
| [`jestercat`](./Enums.md#enum-jestercat) | Enum |  | 3 |
| [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked) | Object | Applies or references the 'BothObelisksUnlocked' effect/state. | 2 |
| [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked) | Object | Applies or references the 'DimensionXUnlocked' effect/state. | 2 |
| [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked) | Object | Applies or references the 'EndOfTimeUnlocked' effect/state. | 2 |
| [`hard_initial`](./Map_Generation_and_Routing.md#context-hard_initial) | Object |  | 2 |
| [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked) | Object | Applies or references the 'HardPathUnlocked' effect/state. | 2 |
| [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked) | Object | Applies or references the 'MeatWorldUnlocked' effect/state. | 2 |
| [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached) | Object | Applies or references the 'VolcanoAntennaAttached' effect/state. | 2 |
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum |  | 1 |
| `advance` | Number |  | 1 |
| `alley` | Object |  | 1 |
| `boneyard` | Object |  | 1 |
| [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked) | Object | Applies or references the 'BoneyardUnlocked' effect/state. | 1 |
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum |  | 1 |
| `bunker` | Object |  | 1 |
| [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked) | Object | Applies or references the 'BunkerUnlocked' effect/state. | 1 |
| [`butchercat`](./Enums.md#enum-butchercat) | Enum |  | 1 |
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum |  | 1 |
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum |  | 1 |
| `caves` | Object |  | 1 |
| [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked) | Object | Applies or references the 'CavesUnlocked' effect/state. | 1 |
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum |  | 1 |
| [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached) | Object | Applies or references the 'ChaosAntennaAttached' effect/state. | 1 |
| [`choose_one`](./Arrays.md#array-choose_one) | Array |  | 1 |
| [`clericcat`](./Enums.md#enum-clericcat) | Enum |  | 1 |
| `core` | Object |  | 1 |
| [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked) | Object | Applies or references the 'CoreObeliskUnlocked' effect/state. | 1 |
| [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked) | Object | Applies or references the 'CoreUnlocked' effect/state. | 1 |
| `crater` | Object |  | 1 |
| [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked) | Object | Applies or references the 'CraterUnlocked' effect/state. | 1 |
| `desert` | Object |  | 1 |
| [`dimensionx`](./Map_Generation_and_Routing.md#context-dimensionx) | Object |  | 1 |
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum |  | 1 |
| [`drmangler`](./Enums.md#enum-drmangler) | Enum |  | 1 |
| [`druidcat`](./Enums.md#enum-druidcat) | Enum |  | 1 |
| [`endoftime`](./Map_Generation_and_Routing.md#context-endoftime) | Object |  | 1 |
| [`event`](./Map_Generation_and_Routing.md#context-event) | Object |  | 1 |
| [`exit_desert`](./Map_Generation_and_Routing.md#context-exit_desert) | Object |  | 1 |
| [`exit_lab`](./Map_Generation_and_Routing.md#context-exit_lab) | Object |  | 1 |
| [`fightercat`](./Enums.md#enum-fightercat) | Enum |  | 1 |
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum |  | 1 |
| [`future`](./Map_Generation_and_Routing.md#context-future) | Object |  | 1 |
| [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked) | Object | Applies or references the 'FutureUnlocked' effect/state. | 1 |
| [`gambit`](./Enums.md#enum-gambit) | Enum |  | 1 |
| [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer) | Object | Applies or references the 'GenFlag_Boss_Spewer' effect/state. | 1 |
| [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy) | Object | Applies or references the 'GenFlag_Boss_Stacy' effect/state. | 1 |
| `head_start` | Number |  | 1 |
| [`home`](./Map_Generation_and_Routing.md#context-home) | Object |  | 1 |
| [`huntercat`](./Enums.md#enum-huntercat) | Enum |  | 1 |
| [`iceage`](./Map_Generation_and_Routing.md#context-iceage) | Object |  | 1 |
| [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked) | Object | Applies or references the 'IceAgeUnlocked' effect/state. | 1 |
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum |  | 1 |
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum |  | 1 |
| `junkyard` | Object |  | 1 |
| [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked) | Object | Applies or references the 'JunkyardUnlocked' effect/state. | 1 |
| [`jurassic`](./Map_Generation_and_Routing.md#context-jurassic) | Object |  | 1 |
| [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked) | Object | Applies or references the 'JurassicUnlocked' effect/state. | 1 |
| `lab` | Object |  | 1 |
| [`lenny`](./Enums.md#enum-lenny) | Enum |  | 1 |
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum |  | 1 |
| `locked` | Boolean |  | 1 |
| [`magecat`](./Enums.md#enum-magecat) | Enum |  | 1 |
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum |  | 1 |
| `meatworld` | Object |  | 1 |
| [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull) | Object | Applies or references the 'MeatWorldUnlockedFull' effect/state. | 1 |
| [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event) | Object |  | 1 |
| [`monkcat`](./Enums.md#enum-monkcat) | Enum |  | 1 |
| `moon` | Object |  | 1 |
| [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked) | Object | Applies or references the 'MoonObeliskUnlocked' effect/state. | 1 |
| [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked) | Object | Applies or references the 'MoonUnlocked' effect/state. | 1 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum |  | 1 |
| [`mw_altar`](./Map_Generation_and_Routing.md#context-mw_altar) | Object |  | 1 |
| [`mw_battle1`](./Map_Generation_and_Routing.md#context-mw_battle1) | Object |  | 1 |
| [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss) | Object |  | 1 |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#context-mw_earlyhome) | Object |  | 1 |
| [`mw_event1`](./Map_Generation_and_Routing.md#context-mw_event1) | Object |  | 1 |
| [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1) | Object |  | 1 |
| [`mw_home`](./Map_Generation_and_Routing.md#context-mw_home) | Object |  | 1 |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event) | Object |  | 1 |
| [`mw_treasure`](./Map_Generation_and_Routing.md#context-mw_treasure) | Object |  | 1 |
| [`necrocat`](./Enums.md#enum-necrocat) | Enum |  | 1 |
| [`nemesis`](./Arrays.md#array-nemesis) | Array |  | 1 |
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum |  | 1 |
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum |  | 1 |
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum |  | 1 |
| [`ratking`](./Enums.md#enum-ratking) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum |  | 1 |
| `sewers` | Object |  | 1 |
| [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked) | Object | Applies or references the 'SewersUnlocked' effect/state. | 1 |
| [`shop_cheapwater`](./Map_Generation_and_Routing.md#context-shop_cheapwater) | Object |  | 1 |
| [`shop_water`](./Map_Generation_and_Routing.md#context-shop_water) | Object |  | 1 |
| [`slime`](./Enums.md#enum-slime) | Enum |  | 1 |
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum |  | 1 |
| [`spewer`](./Enums.md#enum-spewer) | Enum |  | 1 |
| [`stacy`](./Enums.md#enum-stacy) | Enum |  | 1 |
| [`start`](./Map_Generation_and_Routing.md#context-start) | Object |  | 1 |
| [`tankcat`](./Enums.md#enum-tankcat) | Enum |  | 1 |
| [`thebloat`](./Enums.md#enum-thebloat) | Enum |  | 1 |
| [`theend`](./Map_Generation_and_Routing.md#context-theend) | Object |  | 1 |
| [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked) | Object | Applies or references the 'TheEndUnlocked' effect/state. | 1 |
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum |  | 1 |
| [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone) | Object | Applies or references the 'ThrobbingArteryDone' effect/state. | 1 |
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum |  | 1 |
| [`trampy`](./Enums.md#enum-trampy) | Enum |  | 1 |
| [`treasure`](./Map_Generation_and_Routing.md#context-treasure) | Object |  | 1 |
| [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone) | Object | Applies or references the 'WallOfFleshDone' effect/state. | 1 |
| [`weather_event`](./Map_Generation_and_Routing.md#context-weather_event) | Object |  | 1 |
| [`zodiac`](./Enums.md#enum-zodiac) | Enum |  | 1 |
| `battle` | `Block` | | Field Key | Inferred Type | Example Values | Definition | | :--- | :--- | :--- | :--- | | `type` | Enum/String | `battle` | Classification type. | | 0 |
| `rare` | `Array` |  | 0 |

</details>

---

### Object: `boss`
### Object: `boss`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 41

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 19 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum |  | 16 |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`override_music`](./Enums.md#enum-override_music) | Enum |  | 2 |
| `is_final_boss` | Boolean |  | 2 |
| [`tileset`](./Enums.md#enum-tileset) | Enum |  | 1 |
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum |  | 1 |

</details>

---

### Object: `exit0`
### Object: `exit0`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 17 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 15 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 15 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 15 |
| `hidden` | Boolean |  | 10 |

</details>

---

### Object: `quest_event`
### Object: `quest_event`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 24 |
| [`level`](./Enums.md#enum-level) | Enum |  | 19 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 11 |

</details>

---

### Object: `exit1`
### Object: `exit1`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 5 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 3 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 3 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 3 |

</details>

---

### Object: `hard_initial`
### Object: `hard_initial`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `time_machine`
### Object: `time_machine`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 4 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 |

</details>

---

### Object: `BothObelisksUnlocked`
### Object: `BothObelisksUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `DimensionXUnlocked`
### Object: `DimensionXUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `EndOfTimeUnlocked`
### Object: `EndOfTimeUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `HardPathUnlocked`
### Object: `HardPathUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`hard_initial`](./Map_Generation_and_Routing.md#context-hard_initial) | Object |  | 2 |

</details>

---

### Object: `MeatWorldUnlocked`
### Object: `MeatWorldUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `VolcanoAntennaAttached`
### Object: `VolcanoAntennaAttached`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `miniboss_event`
### Object: `miniboss_event`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |

</details>

---

### Object: `mw_battle1`
### Object: `mw_battle1`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `mw_boss`
### Object: `mw_boss`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum |  | 1 |
| [`override_music`](./Enums.md#enum-override_music) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `mw_earlyhome`
### Object: `mw_earlyhome`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |
| `hidden` | Boolean |  | 1 |

</details>

---

### Object: `mw_event1`
### Object: `mw_event1`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `mw_hard1`
### Object: `mw_hard1`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `mw_home`
### Object: `mw_home`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `mw_quest_event`
### Object: `mw_quest_event`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `mw_treasure`
### Object: `mw_treasure`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `BoneyardUnlocked`
### Object: `BoneyardUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `BunkerUnlocked`
### Object: `BunkerUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `CavesUnlocked`
### Object: `CavesUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `ChaosAntennaAttached`
### Object: `ChaosAntennaAttached`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 1 |

</details>

---

### Object: `CoreObeliskUnlocked`
### Object: `CoreObeliskUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 1 |

</details>

---

### Object: `CoreUnlocked`
### Object: `CoreUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `CraterUnlocked`
### Object: `CraterUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Object |  | 1 |

</details>

---

### Object: `FutureUnlocked`
### Object: `FutureUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 1 |

</details>

---

### Object: `GenFlag_Boss_Spewer`
### Object: `GenFlag_Boss_Spewer`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Object |  | 1 |

</details>

---

### Object: `GenFlag_Boss_Stacy`
### Object: `GenFlag_Boss_Stacy`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Object |  | 1 |
| [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event) | Object |  | 1 |

</details>

---

### Object: `IceAgeUnlocked`
### Object: `IceAgeUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 1 |

</details>

---

### Object: `JunkyardUnlocked`
### Object: `JunkyardUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Object |  | 1 |

</details>

---

### Object: `JurassicUnlocked`
### Object: `JurassicUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `MeatWorldUnlockedFull`
### Object: `MeatWorldUnlockedFull`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mw_battle1`](./Map_Generation_and_Routing.md#context-mw_battle1) | Object |  | 1 |
| [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss) | Object |  | 1 |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#context-mw_earlyhome) | Object |  | 1 |
| [`mw_event1`](./Map_Generation_and_Routing.md#context-mw_event1) | Object |  | 1 |
| [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1) | Object |  | 1 |
| [`mw_home`](./Map_Generation_and_Routing.md#context-mw_home) | Object |  | 1 |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event) | Object |  | 1 |
| [`mw_treasure`](./Map_Generation_and_Routing.md#context-mw_treasure) | Object |  | 1 |

</details>

---

### Object: `MoonObeliskUnlocked`
### Object: `MoonObeliskUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 1 |

</details>

---

### Object: `MoonUnlocked`
### Object: `MoonUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `SewersUnlocked`
### Object: `SewersUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `TheEndUnlocked`
### Object: `TheEndUnlocked`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 1 |

</details>

---

### Object: `ThrobbingArteryDone`
### Object: `ThrobbingArteryDone`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 1 |

</details>

---

### Object: `WallOfFleshDone`
### Object: `WallOfFleshDone`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 1 |

</details>

---

### Object: `battle`
### Object: `battle`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `dimensionx`
### Object: `dimensionx`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Object: `endoftime`
### Object: `endoftime`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Object: `event`
### Object: `event`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `exit_desert`
### Object: `exit_desert`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |
| `hidden` | Boolean |  | 1 |
| `locked` | Boolean |  | 1 |

</details>

---

### Object: `exit_lab`
### Object: `exit_lab`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |
| `hidden` | Boolean |  | 1 |
| `locked` | Boolean |  | 1 |

</details>

---

### Object: `future`
### Object: `future`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Object: `home`
### Object: `home`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `iceage`
### Object: `iceage`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Object: `jurassic`
### Object: `jurassic`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Object: `mw_altar`
### Object: `mw_altar`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `shop_cheapwater`
### Object: `shop_cheapwater`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `shop_water`
### Object: `shop_water`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `start`
### Object: `start`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `theend`
### Object: `theend`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 1 |

</details>

---

### Object: `treasure`
### Object: `treasure`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Object: `weather_event`
### Object: `weather_event`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

