# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Map Generation & Routing

> **Associated Files:** `data/maps/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 39

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 883 |  |
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `Array` |  | 673 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 66 |  |
| [`boss`](Combat_Rewards.md#object-boss) | Object || 63 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 54 ||
| [`hard`](./Arrays.md#array-hard) | Array || 42 ||
| [`folder`](./Enums.md#enum-folder) | Enum || 40 ||
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum || 38 ||
| [`include`](./Strings.md#string-include) | String | Examples: `"standard_nodes.gon"` | 38 ||
| [`level`](./Enums.md#enum-level) | Enum || 33 ||
| [`exit0`](#object-exit0) | Object || 30 ||
| [`dimensionx`](#object-dimensionx) | Object || 27 ||
| [`treasure`](#object-treasure) | Object || 26 ||
| [`meatworld`](#object-meatworld) | Object || 24 ||
| [`miniboss`](./Arrays.md#array-miniboss) | Array || 24 ||
| [`normal`](./Arrays.md#array-normal) | Array || 24 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 24 ||
| [`boneyard`](#object-boneyard) | Object || 21 ||
| [`bunker`](#object-bunker) | Object || 20 ||
| [`core`](#object-core) | Object || 20 ||
| [`moon`](#object-moon) | Object || 20 ||
| [`large`](./Arrays.md#array-large) | Array || 19 ||
| [`medium`](./Arrays.md#array-medium) | Array || 19 ||
| [`small`](./Arrays.md#array-small) | Array || 19 ||
| [`alley`](#object-alley) | Object || 18 ||
| [`endoftime`](#object-endoftime) | Object || 18 ||
| [`quest_event`](#object-quest_event) | Object || 18 ||
| [`crater`](#object-crater) | Object || 16 ||
| [`desert`](#object-desert) | Object || 16 ||
| [`easy`](./Arrays.md#array-easy) | Array || 16 ||
| [`future`](Events_and_Encounters.md#object-future) | Object || 16 ||
| [`sewers`](#object-sewers) | Object || 16 ||
| [`iceage`](#object-iceage) | Object || 14 ||
| [`jurassic`](#object-jurassic) | Object || 14 ||
| [`lab`](#object-lab) | Object || 14 ||
| [`theend`](#object-theend) | Object || 14 ||
| [`caves`](#object-caves) | Object || 12 ||
| [`junkyard`](#object-junkyard) | Object || 12 ||
| [`special`](./Arrays.md#array-special) | Array || 10 ||
| [`BothObelisksUnlocked`](Engine_LogicKeys.md#object-bothobelisksunlocked) | Object | Applies or references the 'BothObelisksUnlocked' effect/state. | 8 ||
| [`jestercat`](./Enums.md#enum-jestercat) | Enum || 8 ||
| [`time_machine`](#object-time_machine) | Object || 8 ||
| [`CoreObeliskUnlocked`](Engine_LogicKeys.md#object-coreobeliskunlocked) | Object | Applies or references the 'CoreObeliskUnlocked' effect/state. | 6 ||
| [`exit1`](#object-exit1) | Object || 6 ||
| [`MeatWorldUnlocked`](Engine_LogicKeys.md#object-meatworldunlocked) | Object | Applies or references the 'MeatWorldUnlocked' effect/state. | 6 ||
| [`MoonObeliskUnlocked`](Engine_LogicKeys.md#object-moonobeliskunlocked) | Object | Applies or references the 'MoonObeliskUnlocked' effect/state. | 6 ||
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum || 5 ||
| [`butchercat`](./Enums.md#enum-butchercat) | Enum || 4 ||
| [`DimensionXUnlocked`](Engine_LogicKeys.md#object-dimensionxunlocked) | Object | Applies or references the 'DimensionXUnlocked' effect/state. | 4 ||
| [`EndOfTimeUnlocked`](Engine_LogicKeys.md#object-endoftimeunlocked) | Object | Applies or references the 'EndOfTimeUnlocked' effect/state. | 4 ||
| [`fightercat`](./Enums.md#enum-fightercat) | Enum || 4 ||
| [`hard_initial`](#object-hard_initial) | Object || 4 ||
| [`HardPathUnlocked`](Engine_LogicKeys.md#object-hardpathunlocked) | Object | Applies or references the 'HardPathUnlocked' effect/state. | 4 ||
| [`magecat`](./Enums.md#enum-magecat) | Enum || 4 ||
| [`monkcat`](./Enums.md#enum-monkcat) | Enum || 4 ||
| [`necrocat`](./Enums.md#enum-necrocat) | Enum || 4 ||
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum || 4 ||
| [`start`](./Map_Generation_and_Routing.md#context-start) | Enum || 4 ||
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum || 4 ||
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum || 4 ||
| [`VolcanoAntennaAttached`](Engine_LogicKeys.md#object-volcanoantennaattached) | Object | Applies or references the 'VolcanoAntennaAttached' effect/state. | 4 ||
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum || 3 ||
| [`event`](./Map_Generation_and_Routing.md#context-event) | Enum || 3 ||
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum || 3 ||
| [`gambit`](./Enums.md#enum-gambit) | Enum || 3 ||
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum || 3 ||
| [`spewer`](./Enums.md#enum-spewer) | Enum || 3 ||
| [`zodiac`](./Enums.md#enum-zodiac) | Enum || 3 ||
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum || 2 ||
| `advance` | Number || 2 ||
| [`BoneyardUnlocked`](Engine_LogicKeys.md#object-boneyardunlocked) | Object | Applies or references the 'BoneyardUnlocked' effect/state. | 2 ||
| [`BunkerUnlocked`](Engine_LogicKeys.md#object-bunkerunlocked) | Object | Applies or references the 'BunkerUnlocked' effect/state. | 2 ||
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum || 2 ||
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum || 2 ||
| [`CavesUnlocked`](Engine_LogicKeys.md#object-cavesunlocked) | Object | Applies or references the 'CavesUnlocked' effect/state. | 2 ||
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum || 2 ||
| [`ChaosAntennaAttached`](Engine_LogicKeys.md#object-chaosantennaattached) | Object | Applies or references the 'ChaosAntennaAttached' effect/state. | 2 ||
| [`clericcat`](./Enums.md#enum-clericcat) | Enum || 2 ||
| [`CoreUnlocked`](Engine_LogicKeys.md#object-coreunlocked) | Object | Applies or references the 'CoreUnlocked' effect/state. | 2 ||
| [`CraterUnlocked`](Engine_LogicKeys.md#object-craterunlocked) | Object | Applies or references the 'CraterUnlocked' effect/state. | 2 ||
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum || 2 ||
| [`drmangler`](./Enums.md#enum-drmangler) | Enum || 2 ||
| [`druidcat`](./Enums.md#enum-druidcat) | Enum || 2 ||
| [`exit_desert`](#object-exit_desert) | Object || 2 ||
| [`exit_lab`](#object-exit_lab) | Object || 2 ||
| [`FutureUnlocked`](Engine_LogicKeys.md#object-futureunlocked) | Object | Applies or references the 'FutureUnlocked' effect/state. | 2 ||
| [`GenFlag_Boss_Spewer`](Engine_LogicKeys.md#object-genflag_boss_spewer) | Object | Applies or references the 'GenFlag_Boss_Spewer' effect/state. | 2 ||
| [`GenFlag_Boss_Stacy`](Engine_LogicKeys.md#object-genflag_boss_stacy) | Object | Applies or references the 'GenFlag_Boss_Stacy' effect/state. | 2 ||
| `head_start` | Number || 2 ||
| [`home`](Events_and_Encounters.md#object-home) | Object || 2 ||
| [`huntercat`](./Enums.md#enum-huntercat) | Enum || 2 ||
| [`IceAgeUnlocked`](Engine_LogicKeys.md#object-iceageunlocked) | Object | Applies or references the 'IceAgeUnlocked' effect/state. | 2 ||
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum || 2 ||
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum || 2 ||
| [`JunkyardUnlocked`](Engine_LogicKeys.md#object-junkyardunlocked) | Object | Applies or references the 'JunkyardUnlocked' effect/state. | 2 ||
| [`JurassicUnlocked`](Engine_LogicKeys.md#object-jurassicunlocked) | Object | Applies or references the 'JurassicUnlocked' effect/state. | 2 ||
| [`lenny`](./Enums.md#enum-lenny) | Enum || 2 ||
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum || 2 ||
| `locked` | Boolean || 2 ||
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum || 2 ||
| [`MeatWorldUnlockedFull`](Engine_LogicKeys.md#object-meatworldunlockedfull) | Object | Applies or references the 'MeatWorldUnlockedFull' effect/state. | 2 ||
| [`miniboss_event`](#object-miniboss_event) | Object || 2 ||
| [`MoonUnlocked`](Engine_LogicKeys.md#object-moonunlocked) | Object | Applies or references the 'MoonUnlocked' effect/state. | 2 ||
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum || 2 ||
| [`mw_altar`](#object-mw_altar) | Object || 2 ||
| [`mw_battle1`](#object-mw_battle1) | Object || 2 ||
| [`mw_boss`](#object-mw_boss) | Object || 2 ||
| [`mw_earlyhome`](#object-mw_earlyhome) | Object || 2 ||
| [`mw_event1`](#object-mw_event1) | Object || 2 ||
| [`mw_hard1`](#object-mw_hard1) | Object || 2 ||
| [`mw_home`](#object-mw_home) | Object || 2 ||
| [`mw_quest_event`](#object-mw_quest_event) | Object || 2 ||
| [`mw_treasure`](#object-mw_treasure) | Object || 2 ||
| [`ratking`](./Enums.md#enum-ratking) | Enum || 2 ||
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum || 2 ||
| [`SewersUnlocked`](Engine_LogicKeys.md#object-sewersunlocked) | Object | Applies or references the 'SewersUnlocked' effect/state. | 2 ||
| [`shop_cheapwater`](#object-shop_cheapwater) | Object || 2 ||
| [`shop_water`](#object-shop_water) | Object || 2 ||
| [`slime`](./Enums.md#enum-slime) | Enum || 2 ||
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum || 2 ||
| [`stacy`](./Enums.md#enum-stacy) | Enum || 2 ||
| [`tankcat`](./Enums.md#enum-tankcat) | Enum || 2 ||
| [`thebloat`](./Enums.md#enum-thebloat) | Enum || 2 ||
| [`TheEndUnlocked`](Engine_LogicKeys.md#object-theendunlocked) | Object | Applies or references the 'TheEndUnlocked' effect/state. | 2 ||
| [`ThrobbingArteryDone`](Engine_LogicKeys.md#object-throbbingarterydone) | Object | Applies or references the 'ThrobbingArteryDone' effect/state. | 2 ||
| [`trampy`](./Enums.md#enum-trampy) | Enum || 2 ||
| [`WallOfFleshDone`](Engine_LogicKeys.md#object-walloffleshdone) | Object | Applies or references the 'WallOfFleshDone' effect/state. | 2 ||
| [`weather_event`](#object-weather_event) | Object || 2 ||
| [`choose_one`](./Arrays.md#array-choose_one) | Array || 1 ||
| [`nemesis`](./Arrays.md#array-nemesis) | Array || 1 ||
| :--- | :--- | :--- | :--- | :--- |
| [`battle`](#object-battle) | Object || 6 ||

</details>

---

### Object: `boss`


**Definition:** No definition provided.  
**Total Count:** 41


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#context-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 38 ||
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum || 32 ||
| `is_final_boss` | Boolean || 4 ||
| [`level`](./Enums.md#enum-level) | Enum || 4 ||
| [`override_music`](./Enums.md#enum-override_music) | Enum || 4 ||
| [`tileset`](./Enums.md#enum-tileset) | Enum || 2 ||
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum || 2 ||

</details>

---

### Object: `exit0`


**Definition:** No definition provided.  
**Total Count:** 27


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#context-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#context-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#context-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#context-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#context-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#context-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#context-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#context-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#context-theendunlocked)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean || 34 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 30 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 30 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 30 ||
| `hidden` | Boolean || 20 ||

</details>

---

### Object: `quest_event`


**Definition:** No definition provided.  
**Total Count:** 24


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#context-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#context-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#context-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#context-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#context-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#context-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#context-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#context-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#context-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#context-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#context-walloffleshdone)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`override_art`](./Enums.md#enum-override_art) | Enum || 48 ||
| [`level`](./Enums.md#enum-level) | Enum || 38 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 22 ||

</details>

---

### Object: `exit1`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#context-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#context-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean || 10 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 6 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 6 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 6 ||

</details>

---

### Object: `hard_initial`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#context-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean || 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 ||

</details>

---

### Object: `time_machine`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 8 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 8 ||

</details>

---

### Object: `BothObelisksUnlocked`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 4 ||

</details>

---

### Object: `DimensionXUnlocked`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 4 ||

</details>

---

### Object: `EndOfTimeUnlocked`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 4 ||

</details>

---

### Object: `HardPathUnlocked`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](#object-hard_initial) | Object || 4 ||

</details>

---

### Object: `MeatWorldUnlocked`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 4 ||
| [`quest_event`](#object-quest_event) | Object || 4 ||

</details>

---

### Object: `miniboss_event`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#context-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 ||
| [`level`](./Enums.md#enum-level) | Enum || 2 ||

</details>

---

### Object: `mw_battle1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 4 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `mw_boss`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 4 ||
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum || 2 ||
| [`override_music`](./Enums.md#enum-override_music) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `mw_earlyhome`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `mw_event1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 4 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `mw_hard1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 4 ||
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `mw_home`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 4 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `mw_quest_event`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 4 ||
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `mw_treasure`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#context-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 4 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `VolcanoAntennaAttached`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 4 ||

</details>

---

### Object: `battle`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `BoneyardUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `BunkerUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `CavesUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `ChaosAntennaAttached`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 2 ||

</details>

---

### Object: `CoreObeliskUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 2 ||

</details>

---

### Object: `CoreUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `CraterUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](#object-exit1) | Object || 2 ||

</details>

---

### Object: `dimensionx`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 2 ||

</details>

---

### Object: `endoftime`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 2 ||

</details>

---

### Object: `event`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `exit_desert`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 ||
| `locked` | Boolean || 2 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 2 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `exit_lab`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean || 2 ||
| `locked` | Boolean || 2 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 2 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `future`


**Definition:** Event Node: Story branch or dialog option representing the 'Future' action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 2 ||

</details>

---

### Object: `FutureUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 2 ||

</details>

---

### Object: `GenFlag_Boss_Spewer`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](Combat_Rewards.md#object-boss) | Object || 2 ||

</details>

---

### Object: `GenFlag_Boss_Stacy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](Combat_Rewards.md#object-boss) | Object || 2 ||
| [`miniboss_event`](#object-miniboss_event) | Object || 2 ||

</details>

---

### Object: `home`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `iceage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 2 ||

</details>

---

### Object: `IceAgeUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 2 ||

</details>

---

### Object: `JunkyardUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](#object-exit1) | Object || 2 ||

</details>

---

### Object: `jurassic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 2 ||

</details>

---

### Object: `JurassicUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `MeatWorldUnlockedFull`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](#object-mw_battle1) | Object || 2 ||
| [`mw_boss`](#object-mw_boss) | Object || 2 ||
| [`mw_earlyhome`](#object-mw_earlyhome) | Object || 2 ||
| [`mw_event1`](#object-mw_event1) | Object || 2 ||
| [`mw_hard1`](#object-mw_hard1) | Object || 2 ||
| [`mw_home`](#object-mw_home) | Object || 2 ||
| [`mw_quest_event`](#object-mw_quest_event) | Object || 2 ||
| [`mw_treasure`](#object-mw_treasure) | Object || 2 ||

</details>

---

### Object: `MoonObeliskUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 2 ||

</details>

---

### Object: `MoonUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `mw_altar`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `SewersUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `shop_cheapwater`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `shop_water`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `start`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `theend`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean || 2 ||

</details>

---

### Object: `TheEndUnlocked`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](#object-exit0) | Object || 2 ||

</details>

---

### Object: `ThrobbingArteryDone`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 2 ||

</details>

---

### Object: `treasure`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---

### Object: `WallOfFleshDone`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](#object-quest_event) | Object || 2 ||

</details>

---

### Object: `weather_event`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

</details>

---



---

## Auto-Discovered Objects


### Object: `alley`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `AlleyBGTest` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Background` |
| `debris` | String | Undocumented. | 1 | `Debris` |
| `event_piece_frame` | String | Undocumented. | 1 | `alley` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `Rubble` |
| `static_1x1_b` | String | Undocumented. | 1 | `Bricks` |
| `static_1x1_c` | String | Undocumented. | 1 | `Bricks` |
| `static_2x2_a` | String | Undocumented. | 1 | `Dumpster` |
| `static_2x2_b` | String | Undocumented. | 1 | `Dumpster` |
| `static_tall_a` | String | Undocumented. | 1 | `PowerPole` |
| `static_tall_b` | String | Undocumented. | 1 | `PhoneBooth` |

</details>

### Object: `boneyard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `BoneYardBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Background_Graves` |
| `debris` | String | Undocumented. | 1 | `GravesDebris` |
| `event_piece_frame` | String | Undocumented. | 1 | `graves` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| `global_particles` | Array | Undocumented. | 1 | `Mist` |
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `GraveRocks1` |
| `static_1x1_b` | String | Undocumented. | 1 | `GraveRocks2` |
| `static_1x1_c` | String | Undocumented. | 1 | `GraveRocks2` |
| `static_2x2_a` | String | Undocumented. | 1 | `BigGraveRocks1` |
| `static_2x2_b` | String | Undocumented. | 1 | `BigGraveRocks1` |
| `static_tall_a` | String | Undocumented. | 1 | `TallGraveRocks1` |
| `static_tall_b` | String | Undocumented. | 1 | `TallGraveRocks1` |

</details>

### Object: `bunker`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `BunkerBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Background_Bunker` |
| `debris` | String | Undocumented. | 1 | `Debris7` |
| `event_piece_frame` | String | Undocumented. | 1 | `bunker` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `BunkerObjects1` |
| `static_1x1_b` | String | Undocumented. | 1 | `BunkerObjects2` |
| `static_1x1_c` | String | Undocumented. | 1 | `SmallGravelPile` |
| `static_2x2_a` | String | Undocumented. | 1 | `Bunker2x2` |
| `static_2x2_b` | String | Undocumented. | 1 | `BigGravelPile` |
| `static_tall_a` | String | Undocumented. | 1 | `BunkerTall1` |
| `static_tall_b` | String | Undocumented. | 1 | `BunkerTall2` |

</details>

### Object: `caves`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `CavesBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Background_Caves` |
| `debris` | String | Undocumented. | 1 | `CaveDebris` |
| `event_piece_frame` | String | Undocumented. | 1 | `caves` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| `global_particles` | Array | Undocumented. | 1 | `CaveDrip` |
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `CaveRock1` |
| `static_1x1_b` | String | Undocumented. | 1 | `CaveRock2` |
| `static_1x1_c` | String | Undocumented. | 1 | `CaveRock3` |
| `static_2x2_a` | String | Undocumented. | 1 | `BigCaveRock1` |
| `static_2x2_b` | String | Undocumented. | 1 | `BigCaveRock1` |
| `static_tall_a` | String | Undocumented. | 1 | `TallCaveRock1` |
| `static_tall_b` | String | Undocumented. | 1 | `TallCaveRock2` |

</details>

### Object: `core`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boss_background_alt` | String | Undocumented. | 1 | `CoreBossBG` |
| `combat_background` | String | Undocumented. | 1 | `CoreBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `CoreUI` |
| `debris` | String | Undocumented. | 1 | `Debris9` |
| `event_piece_frame` | String | Undocumented. | 1 | `core` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| `global_particles` | Array | Undocumented. | 1 | `Embers CoreHeatWave_Distortion` |
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `CoreObjects1` |
| `static_1x1_b` | String | Undocumented. | 1 | `CoreObjects2` |
| `static_1x1_c` | String | Undocumented. | 1 | `CoreObjects3` |
| `static_2x2_a` | String | Undocumented. | 1 | `Core2x2` |
| `static_2x2_b` | String | Undocumented. | 1 | `Desert2x2` |
| `static_tall_a` | String | Undocumented. | 1 | `CoreTall1` |
| `static_tall_b` | String | Undocumented. | 1 | `CoreTall2` |

</details>

### Object: `crater`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `CraterBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Background_Crater` |
| `debris` | String | Undocumented. | 1 | `Debris8` |
| `event_piece_frame` | String | Undocumented. | 1 | `crater` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| `global_particles` | Array | Undocumented. | 1 | `CraterLeaves` |
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `CraterObjects1` |
| `static_1x1_b` | String | Undocumented. | 1 | `CraterObjects2` |
| `static_1x1_c` | String | Undocumented. | 1 | `CraterObjects1` |
| `static_2x2_a` | String | Undocumented. | 1 | `Crater2x2` |
| `static_2x2_b` | String | Undocumented. | 1 | `Desert2x2` |
| `static_tall_a` | String | Undocumented. | 1 | `CraterTall1` |
| `static_tall_b` | String | Undocumented. | 1 | `CraterTall2` |

</details>

### Object: `desert`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `DesertBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `DesertUI` |
| `debris` | String | Undocumented. | 1 | `DesertDebris` |
| `event_piece_frame` | String | Undocumented. | 1 | `desert` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `DesertRocks` |
| `static_1x1_b` | String | Undocumented. | 1 | `DesertCactus` |
| `static_1x1_c` | String | Undocumented. | 1 | `DesertRocks` |
| `static_2x2_a` | String | Undocumented. | 1 | `Desert2x2` |
| `static_2x2_b` | String | Undocumented. | 1 | `Desert2x2` |
| `static_tall_a` | String | Undocumented. | 1 | `DesertTall` |
| `static_tall_b` | String | Undocumented. | 1 | `DesertTall2` |

</details>

### Object: `junkyard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `JunkyardBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Background_Junkyard` |
| `debris` | String | Undocumented. | 1 | `Debris2` |
| `event_piece_frame` | String | Undocumented. | 1 | `junkyard` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `StaticJunkSmall` |
| `static_1x1_b` | String | Undocumented. | 1 | `Stump` |
| `static_1x1_c` | String | Undocumented. | 1 | `SmallGravelPile` |
| `static_2x2_a` | String | Undocumented. | 1 | `StaticJunkCube` |
| `static_2x2_b` | String | Undocumented. | 1 | `BigGravelPile` |
| `static_tall_a` | String | Undocumented. | 1 | `Tree` |
| `static_tall_b` | String | Undocumented. | 1 | `StaticTires` |

</details>

### Object: `lab`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `LabBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `LabUI` |
| `debris` | String | Undocumented. | 1 | `Debris11` |
| `event_piece_frame` | String | Undocumented. | 1 | `lab` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 2 ||
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `LabObjects1` |
| `static_1x1_b` | String | Undocumented. | 1 | `Labobjects2` |
| `static_1x1_c` | String | Undocumented. | 1 | `LabObjects1` |
| `static_2x2_a` | String | Undocumented. | 1 | `Lab2x2` |
| `static_2x2_b` | String | Undocumented. | 1 | `Moon2x22` |
| `static_tall_a` | String | Undocumented. | 1 | `Labtall1` |
| `static_tall_b` | String | Undocumented. | 1 | `Labtall2` |

</details>

### Object: `meatworld`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `background_extra_shader` | String | Undocumented. | 1 | `meatpulse` |
| `background_shader` | String | Undocumented. | 1 | `meatpulse_ground` |
| `combat_background` | String | Undocumented. | 1 | `meatBGpulsing` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Meat` |
| `debris` | String | Undocumented. | 1 | `meatdebris` |
| `event_piece_frame` | String | Undocumented. | 1 | `meatworld` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| `global_particles` | Array | Undocumented. | 1 | `MeatCaveDrip CoreHeatWave_Dist` |
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `Meatobjects` |
| `static_1x1_b` | String | Undocumented. | 1 | `Meatobjects2` |
| `static_1x1_c` | String | Undocumented. | 1 | `Meatobjects` |
| `static_2x2_a` | String | Undocumented. | 1 | `Meat2x2` |
| `static_2x2_b` | String | Undocumented. | 1 | `Dumpster` |
| `static_tall_a` | String | Undocumented. | 1 | `Meatt` |
| `static_tall_b` | String | Undocumented. | 1 | `meattall1` |
| `water_alt_shader` | String | Undocumented. | 1 | `blood` |
| `water_alt_shroud` | String | Undocumented. | 1 | `BloodShroud` |
| `water_alt_tile` | String | Undocumented. | 1 | `BloodTile` |

</details>

### Object: `moon`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combat_background` | String | Undocumented. | 1 | `MoonBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `MoonUI` |
| `debris` | String | Undocumented. | 1 | `Debris10` |
| `event_piece_frame` | String | Undocumented. | 1 | `moon` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `MoonObjects1` |
| `static_1x1_b` | String | Undocumented. | 1 | `MoonObjects2` |
| `static_1x1_c` | String | Undocumented. | 1 | `MoonObjects2` |
| `static_2x2_a` | String | Undocumented. | 1 | `Moon2x2` |
| `static_2x2_b` | String | Undocumented. | 1 | `Moon2x22` |
| `static_tall_a` | String | Undocumented. | 1 | `MoonTall1` |
| `static_tall_b` | String | Undocumented. | 1 | `MoonTall2` |

</details>

### Object: `sewers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `background_extra_shader` | String | Undocumented. | 1 | `water` |
| `combat_background` | String | Undocumented. | 1 | `SewerBG` |
| `combat_ui_background` | String | Undocumented. | 1 | `UI_Background_Sewers` |
| `debris` | String | Undocumented. | 1 | `Debris3` |
| `event_piece_frame` | String | Undocumented. | 1 | `sewers` |
| [`global_objects`](Miscellaneous.md#object-global_objects) | Object | Undocumented. | 1 ||
| `global_particles` | Array | Undocumented. | 1 | `CaveDrip` |
| [`reverb`](Miscellaneous.md#object-reverb) | Object | Undocumented. | 1 ||
| `static_1x1_a` | String | Undocumented. | 1 | `SmallPipes` |
| `static_1x1_b` | String | Undocumented. | 1 | `Bricks3` |
| `static_1x1_c` | String | Undocumented. | 1 | `Sludge` |
| `static_2x2_a` | String | Undocumented. | 1 | `BigPipes` |
| `static_2x2_b` | String | Undocumented. | 1 | `Dumpster` |
| `static_tall_a` | String | Undocumented. | 1 | `TallPipe` |
| `static_tall_b` | String | Undocumented. | 1 | `PhoneBooth` |

</details>
