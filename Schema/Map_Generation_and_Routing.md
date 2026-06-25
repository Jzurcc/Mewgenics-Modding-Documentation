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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 967 |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Object |  | 63 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 54 |
| [`easy`](./Arrays.md#array-easy) | Array |  | 16 |
| [`folder`](./Enums.md#enum-folder) | Enum |  | 40 |
| [`hard`](./Arrays.md#array-hard) | Array |  | 42 |
| [`miniboss`](./Arrays.md#array-miniboss) | Array |  | 24 |
| [`normal`](./Arrays.md#array-normal) | Array |  | 24 |
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum |  | 38 |
| [`include`](./Strings.md#string-include) | String | Examples: `"standard_nodes.gon"` | 38 |
| [`large`](./Arrays.md#array-large) | Array |  | 19 |
| [`medium`](./Arrays.md#array-medium) | Array |  | 19 |
| [`small`](./Arrays.md#array-small) | Array |  | 19 |
| [`special`](./Arrays.md#array-special) | Array |  | 10 |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 30 |
| [`level`](./Enums.md#enum-level) | Enum |  | 33 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 24 |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 18 |
| [`time_machine`](./Map_Generation_and_Routing.md#context-time_machine) | Object |  | 8 |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Object |  | 6 |
| [`jestercat`](./Enums.md#enum-jestercat) | Enum |  | 8 |
| [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked) | Object | Applies or references the 'BothObelisksUnlocked' effect/state. | 8 |
| [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked) | Object | Applies or references the 'DimensionXUnlocked' effect/state. | 4 |
| [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked) | Object | Applies or references the 'EndOfTimeUnlocked' effect/state. | 4 |
| [`hard_initial`](./Map_Generation_and_Routing.md#context-hard_initial) | Object |  | 4 |
| [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked) | Object | Applies or references the 'HardPathUnlocked' effect/state. | 4 |
| [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked) | Object | Applies or references the 'MeatWorldUnlocked' effect/state. | 6 |
| [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached) | Object | Applies or references the 'VolcanoAntennaAttached' effect/state. | 4 |
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum |  | 2 |
| `advance` | Number |  | 2 |
| [`alley`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 18 |
| [`boneyard`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 21 |
| [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked) | Object | Applies or references the 'BoneyardUnlocked' effect/state. | 2 |
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum |  | 3 |
| [`bunker`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 20 |
| [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked) | Object | Applies or references the 'BunkerUnlocked' effect/state. | 2 |
| [`butchercat`](./Enums.md#enum-butchercat) | Enum |  | 4 |
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum |  | 2 |
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum |  | 2 |
| [`caves`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 12 |
| [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked) | Object | Applies or references the 'CavesUnlocked' effect/state. | 2 |
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum |  | 2 |
| [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached) | Object | Applies or references the 'ChaosAntennaAttached' effect/state. | 2 |
| [`choose_one`](./Arrays.md#array-choose_one) | Array |  | 1 |
| [`clericcat`](./Enums.md#enum-clericcat) | Enum |  | 2 |
| [`core`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 20 |
| [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked) | Object | Applies or references the 'CoreObeliskUnlocked' effect/state. | 6 |
| [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked) | Object | Applies or references the 'CoreUnlocked' effect/state. | 2 |
| [`crater`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 16 |
| [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked) | Object | Applies or references the 'CraterUnlocked' effect/state. | 2 |
| [`desert`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 16 |
| [`dimensionx`](./Map_Generation_and_Routing.md#context-dimensionx) | Object |  | 27 |
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum |  | 2 |
| [`drmangler`](./Enums.md#enum-drmangler) | Enum |  | 2 |
| [`druidcat`](./Enums.md#enum-druidcat) | Enum |  | 2 |
| [`endoftime`](./Map_Generation_and_Routing.md#context-endoftime) | Object |  | 18 |
| [`event`](./Map_Generation_and_Routing.md#context-event) | Object |  | 3 |
| [`exit_desert`](./Map_Generation_and_Routing.md#context-exit_desert) | Object |  | 2 |
| [`exit_lab`](./Map_Generation_and_Routing.md#context-exit_lab) | Object |  | 2 |
| [`fightercat`](./Enums.md#enum-fightercat) | Enum |  | 4 |
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum |  | 3 |
| [`future`](./Map_Generation_and_Routing.md#context-future) | Object |  | 16 |
| [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked) | Object | Applies or references the 'FutureUnlocked' effect/state. | 2 |
| [`gambit`](./Enums.md#enum-gambit) | Enum |  | 3 |
| [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer) | Object | Applies or references the 'GenFlag_Boss_Spewer' effect/state. | 2 |
| [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy) | Object | Applies or references the 'GenFlag_Boss_Stacy' effect/state. | 2 |
| `head_start` | Number |  | 2 |
| [`home`](./Map_Generation_and_Routing.md#context-home) | Object |  | 2 |
| [`huntercat`](./Enums.md#enum-huntercat) | Enum |  | 2 |
| [`iceage`](./Map_Generation_and_Routing.md#context-iceage) | Object |  | 14 |
| [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked) | Object | Applies or references the 'IceAgeUnlocked' effect/state. | 2 |
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum |  | 2 |
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum |  | 2 |
| [`junkyard`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 12 |
| [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked) | Object | Applies or references the 'JunkyardUnlocked' effect/state. | 2 |
| [`jurassic`](./Map_Generation_and_Routing.md#context-jurassic) | Object |  | 14 |
| [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked) | Object | Applies or references the 'JurassicUnlocked' effect/state. | 2 |
| [`lab`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 14 |
| [`lenny`](./Enums.md#enum-lenny) | Enum |  | 2 |
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum |  | 2 |
| `locked` | Boolean |  | 2 |
| [`magecat`](./Enums.md#enum-magecat) | Enum |  | 4 |
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum |  | 2 |
| [`meatworld`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 24 |
| [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull) | Object | Applies or references the 'MeatWorldUnlockedFull' effect/state. | 2 |
| [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event) | Object |  | 2 |
| [`monkcat`](./Enums.md#enum-monkcat) | Enum |  | 4 |
| [`moon`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 20 |
| [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked) | Object | Applies or references the 'MoonObeliskUnlocked' effect/state. | 6 |
| [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked) | Object | Applies or references the 'MoonUnlocked' effect/state. | 2 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum |  | 2 |
| [`mw_altar`](./Map_Generation_and_Routing.md#context-mw_altar) | Object |  | 2 |
| [`mw_battle1`](./Map_Generation_and_Routing.md#context-mw_battle1) | Object |  | 2 |
| [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss) | Object |  | 2 |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#context-mw_earlyhome) | Object |  | 2 |
| [`mw_event1`](./Map_Generation_and_Routing.md#context-mw_event1) | Object |  | 2 |
| [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1) | Object |  | 2 |
| [`mw_home`](./Map_Generation_and_Routing.md#context-mw_home) | Object |  | 2 |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event) | Object |  | 2 |
| [`mw_treasure`](./Map_Generation_and_Routing.md#context-mw_treasure) | Object |  | 2 |
| [`necrocat`](./Enums.md#enum-necrocat) | Enum |  | 4 |
| [`nemesis`](./Arrays.md#array-nemesis) | Array |  | 1 |
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum |  | 4 |
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum |  | 5 |
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum |  | 3 |
| [`ratking`](./Enums.md#enum-ratking) | Enum |  | 2 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 66 |
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum |  | 2 |
| [`sewers`](./Engine_EventKeys.md#valid-property-keys) | Object |  | 16 |
| [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked) | Object | Applies or references the 'SewersUnlocked' effect/state. | 2 |
| [`shop_cheapwater`](./Map_Generation_and_Routing.md#context-shop_cheapwater) | Object |  | 2 |
| [`shop_water`](./Map_Generation_and_Routing.md#context-shop_water) | Object |  | 2 |
| [`slime`](./Enums.md#enum-slime) | Enum |  | 2 |
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum |  | 2 |
| [`spewer`](./Enums.md#enum-spewer) | Enum |  | 3 |
| [`stacy`](./Enums.md#enum-stacy) | Enum |  | 2 |
| [`start`](./Map_Generation_and_Routing.md#context-start) | Object |  | 4 |
| [`tankcat`](./Enums.md#enum-tankcat) | Enum |  | 2 |
| [`thebloat`](./Enums.md#enum-thebloat) | Enum |  | 2 |
| [`theend`](./Map_Generation_and_Routing.md#context-theend) | Object |  | 14 |
| [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked) | Object | Applies or references the 'TheEndUnlocked' effect/state. | 2 |
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum |  | 4 |
| [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone) | Object | Applies or references the 'ThrobbingArteryDone' effect/state. | 2 |
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum |  | 4 |
| [`trampy`](./Enums.md#enum-trampy) | Enum |  | 2 |
| [`treasure`](./Map_Generation_and_Routing.md#context-treasure) | Object |  | 26 |
| [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone) | Object | Applies or references the 'WallOfFleshDone' effect/state. | 2 |
| [`weather_event`](./Map_Generation_and_Routing.md#context-weather_event) | Object |  | 2 |
| [`zodiac`](./Enums.md#enum-zodiac) | Enum |  | 3 |
| [`battle`](./Map_Generation_and_Routing.md#object-battle) | Object | | Field Key | Inferred Type | Example Values | Definition | | :--- | :--- | :--- | :--- | | `type` | Enum/String | `battle` | Classification type. | | 0 |
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 673 |

</details>

---

### Object: `boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 41

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 38 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum |  | 32 |
| [`level`](./Enums.md#enum-level) | Enum |  | 4 |
| [`override_music`](./Enums.md#enum-override_music) | Enum |  | 4 |
| `is_final_boss` | Boolean |  | 4 |
| [`tileset`](./Enums.md#enum-tileset) | Enum |  | 2 |
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum |  | 2 |

</details>

---

### Object: `exit0`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 34 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 30 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 30 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 30 |
| `hidden` | Boolean |  | 20 |

</details>

---

### Object: `quest_event`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 48 |
| [`level`](./Enums.md#enum-level) | Enum |  | 38 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 22 |

</details>

---

### Object: `exit1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 10 |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 6 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 6 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 6 |

</details>

---

### Object: `hard_initial`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean |  | 8 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 |

</details>

---

### Object: `time_machine`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 8 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 8 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 8 |

</details>

---

### Object: `BothObelisksUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 4 |

</details>

---

### Object: `DimensionXUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 4 |

</details>

---

### Object: `EndOfTimeUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 4 |

</details>

---

### Object: `HardPathUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`hard_initial`](./Map_Generation_and_Routing.md#context-hard_initial) | Object |  | 4 |

</details>

---

### Object: `MeatWorldUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 4 |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 4 |

</details>

---

### Object: `VolcanoAntennaAttached`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 4 |

</details>

---

### Object: `miniboss_event`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |

</details>

---

### Object: `mw_battle1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `mw_boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 4 |
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum |  | 2 |
| [`override_music`](./Enums.md#enum-override_music) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `mw_earlyhome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |
| `hidden` | Boolean |  | 2 |

</details>

---

### Object: `mw_event1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `mw_hard1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 4 |
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `mw_home`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `mw_quest_event`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 4 |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `mw_treasure`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `BoneyardUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `BunkerUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `CavesUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `ChaosAntennaAttached`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `CoreObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `CoreUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `CraterUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Object |  | 2 |

</details>

---

### Object: `FutureUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `GenFlag_Boss_Spewer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Object |  | 2 |

</details>

---

### Object: `GenFlag_Boss_Stacy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#context-boss) | Object |  | 2 |
| [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event) | Object |  | 2 |

</details>

---

### Object: `IceAgeUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `JunkyardUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#context-exit1) | Object |  | 2 |

</details>

---

### Object: `JurassicUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `MeatWorldUnlockedFull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mw_battle1`](./Map_Generation_and_Routing.md#context-mw_battle1) | Object |  | 2 |
| [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss) | Object |  | 2 |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#context-mw_earlyhome) | Object |  | 2 |
| [`mw_event1`](./Map_Generation_and_Routing.md#context-mw_event1) | Object |  | 2 |
| [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1) | Object |  | 2 |
| [`mw_home`](./Map_Generation_and_Routing.md#context-mw_home) | Object |  | 2 |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event) | Object |  | 2 |
| [`mw_treasure`](./Map_Generation_and_Routing.md#context-mw_treasure) | Object |  | 2 |

</details>

---

### Object: `MoonObeliskUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `MoonUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `SewersUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `TheEndUnlocked`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#context-exit0) | Object |  | 2 |

</details>

---

### Object: `ThrobbingArteryDone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `WallOfFleshDone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event) | Object |  | 2 |

</details>

---

### Object: `battle`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `dimensionx`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 2 |

</details>

---

### Object: `endoftime`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 2 |

</details>

---

### Object: `event`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `exit_desert`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 2 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |
| `hidden` | Boolean |  | 2 |
| `locked` | Boolean |  | 2 |

</details>

---

### Object: `exit_lab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`next_map`](./Enums.md#enum-next_map) | Enum |  | 2 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |
| `hidden` | Boolean |  | 2 |
| `locked` | Boolean |  | 2 |

</details>

---

### Object: `future`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 2 |

</details>

---

### Object: `home`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `iceage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 2 |

</details>

---

### Object: `jurassic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 2 |

</details>

---

### Object: `mw_altar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `shop_cheapwater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `shop_water`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`override_art`](./Enums.md#enum-override_art) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `start`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `theend`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean |  | 2 |

</details>

---

### Object: `treasure`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

### Object: `weather_event`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |

</details>

---

