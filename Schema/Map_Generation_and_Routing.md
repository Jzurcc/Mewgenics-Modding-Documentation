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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 664 |  |
| [`boss`](Combat_Rewards.md#object-boss) | Object | Configures boss encounter properties, including type, rewards, and cutscene. | 131 ||
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `Array` | Specifies the rare reward table or specific reward given. | 34 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 33 |  |
| [`special`](./Arrays.md#array-special) | Array || 29 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 27 ||
| [`battle`](#object-battle) | Object || 25 ||
| [`hard`](./Arrays.md#array-hard) | Array | Defines the reward and encounter parameters for the hard difficulty level. | 23 ||
| [`miniboss`](./Arrays.md#array-miniboss) | Array || 23 ||
| [`normal`](./Arrays.md#array-normal) | Array || 23 ||
| [`event`](./Map_Generation_and_Routing.md#context-event) | Enum || 22 ||
| [`level`](./Enums.md#enum-level) | Enum || 21 ||
| [`folder`](./Enums.md#enum-folder) | Enum || 20 ||
| [`easy`](./Arrays.md#array-easy) | Array | Defines the reward and encounter parameters for the easy difficulty level. | 20 ||
| [`chapter_item_pool`](./Enums.md#enum-chapter_item_pool) | Enum || 19 ||
| [`include`](./Strings.md#string-include) | String | Examples: `"standard_nodes.gon"` | 19 ||
| [`large`](./Arrays.md#array-large) | Array || 19 ||
| [`medium`](./Arrays.md#array-medium) | Array || 19 ||
| [`small`](./Arrays.md#array-small) | Array || 19 ||
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 15 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 12 ||
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 9 ||
| [`time_machine`](#object-time_machine) | Object || 4 ||
| [`dimensionx`](#object-dimensionx) | Object || 3 ||
| [`meatworld`](#object-meatworld) | Object || 3 ||
| [`boneyard`](#object-boneyard) | Object || 3 ||
| [`bunker`](#object-bunker) | Object || 3 ||
| [`core`](#object-core) | Object || 3 ||
| [`moon`](#object-moon) | Object || 3 ||
| [`alley`](#object-alley) | Object || 3 ||
| [`endoftime`](#object-endoftime) | Object || 3 ||
| [`crater`](#object-crater) | Object || 3 ||
| [`desert`](#object-desert) | Object || 3 ||
| [`future`](Events_and_Encounters.md#object-future) | Object || 3 ||
| [`sewers`](#object-sewers) | Object || 3 ||
| [`iceage`](#object-iceage) | Object || 3 ||
| [`jurassic`](#object-jurassic) | Object || 3 ||
| [`lab`](#object-lab) | Object || 3 ||
| [`theend`](#object-theend) | Object || 3 ||
| [`caves`](#object-caves) | Object || 3 ||
| [`junkyard`](#object-junkyard) | Object || 3 ||
| [`jestercat`](./Enums.md#enum-jestercat) | Enum || 3 ||
| [`exit1`](#object-exit1) | Object | Defines the properties of the second exit node on a map, such as its type, destination, and locked state. | 3 ||
| [`BothObelisksUnlocked`](Engine_LogicKeys.md#object-bothobelisksunlocked) | Object | Applies or references the 'BothObelisksUnlocked' effect/state. | 2 ||
| [`MeatWorldUnlocked`](Engine_LogicKeys.md#object-meatworldunlocked) | Object | Applies or references the 'MeatWorldUnlocked' effect/state. | 2 ||
| [`DimensionXUnlocked`](Engine_LogicKeys.md#object-dimensionxunlocked) | Object | Applies or references the 'DimensionXUnlocked' effect/state. | 2 ||
| [`EndOfTimeUnlocked`](Engine_LogicKeys.md#object-endoftimeunlocked) | Object | Applies or references the 'EndOfTimeUnlocked' effect/state. | 2 ||
| [`hard_initial`](#object-hard_initial) | Object | Defines initial properties for the hard path node, such as type and locked state. | 2 ||
| [`HardPathUnlocked`](Engine_LogicKeys.md#object-hardpathunlocked) | Object | Applies or references the 'HardPathUnlocked' effect/state. | 2 ||
| [`VolcanoAntennaAttached`](Engine_LogicKeys.md#object-volcanoantennaattached) | Object | Applies or references the 'VolcanoAntennaAttached' effect/state. | 2 ||
| [`treasure`](#object-treasure) | Object || 1 ||
| [`CoreObeliskUnlocked`](Engine_LogicKeys.md#object-coreobeliskunlocked) | Object | Applies or references the 'CoreObeliskUnlocked' effect/state. | 1 ||
| [`MoonObeliskUnlocked`](Engine_LogicKeys.md#object-moonobeliskunlocked) | Object | Applies or references the 'MoonObeliskUnlocked' effect/state. | 1 ||
| [`queenhippo`](./Enums.md#enum-queenhippo) | Enum || 1 ||
| [`butchercat`](./Enums.md#enum-butchercat) | Enum || 1 ||
| [`fightercat`](./Enums.md#enum-fightercat) | Enum || 1 ||
| [`magecat`](./Enums.md#enum-magecat) | Enum || 1 ||
| [`monkcat`](./Enums.md#enum-monkcat) | Enum || 1 ||
| [`necrocat`](./Enums.md#enum-necrocat) | Enum || 1 ||
| [`psychiccat`](./Enums.md#enum-psychiccat) | Enum || 1 ||
| [`start`](./Map_Generation_and_Routing.md#context-start) | Enum || 1 ||
| [`thiefcat`](./Enums.md#enum-thiefcat) | Enum || 1 ||
| [`tinkerercat`](./Enums.md#enum-tinkerercat) | Enum || 1 ||
| [`bumblefoot`](./Enums.md#enum-bumblefoot) | Enum || 1 ||
| [`flushmaster`](./Enums.md#enum-flushmaster) | Enum || 1 ||
| [`gambit`](./Enums.md#enum-gambit) | Enum || 1 ||
| [`radicalrat`](./Enums.md#enum-radicalrat) | Enum || 1 ||
| [`spewer`](./Enums.md#enum-spewer) | Enum || 1 ||
| [`zodiac`](./Enums.md#enum-zodiac) | Enum || 1 ||
| [`abandonedones`](./Enums.md#enum-abandonedones) | Enum || 1 ||
| `advance` | Number || 1 ||
| [`BoneyardUnlocked`](Engine_LogicKeys.md#object-boneyardunlocked) | Object | Applies or references the 'BoneyardUnlocked' effect/state. | 1 ||
| [`BunkerUnlocked`](Engine_LogicKeys.md#object-bunkerunlocked) | Object | Applies or references the 'BunkerUnlocked' effect/state. | 1 ||
| [`cancreeper`](./Enums.md#enum-cancreeper) | Enum || 1 ||
| [`cavecatfamily`](./Enums.md#enum-cavecatfamily) | Enum || 1 ||
| [`CavesUnlocked`](Engine_LogicKeys.md#object-cavesunlocked) | Object | Applies or references the 'CavesUnlocked' effect/state. | 1 ||
| [`cerberubs`](./Enums.md#enum-cerberubs) | Enum || 1 ||
| [`ChaosAntennaAttached`](Engine_LogicKeys.md#object-chaosantennaattached) | Object | Applies or references the 'ChaosAntennaAttached' effect/state. | 1 ||
| [`clericcat`](./Enums.md#enum-clericcat) | Enum || 1 ||
| [`CoreUnlocked`](Engine_LogicKeys.md#object-coreunlocked) | Object | Applies or references the 'CoreUnlocked' effect/state. | 1 ||
| [`CraterUnlocked`](Engine_LogicKeys.md#object-craterunlocked) | Object | Applies or references the 'CraterUnlocked' effect/state. | 1 ||
| [`dinocouple`](./Enums.md#enum-dinocouple) | Enum || 1 ||
| [`drmangler`](./Enums.md#enum-drmangler) | Enum || 1 ||
| [`druidcat`](./Enums.md#enum-druidcat) | Enum || 1 ||
| [`exit_desert`](#object-exit_desert) | Object || 1 ||
| [`exit_lab`](#object-exit_lab) | Object || 1 ||
| [`FutureUnlocked`](Engine_LogicKeys.md#object-futureunlocked) | Object | Applies or references the 'FutureUnlocked' effect/state. | 1 ||
| [`GenFlag_Boss_Spewer`](Engine_LogicKeys.md#object-genflag_boss_spewer) | Object | Applies or references the 'GenFlag_Boss_Spewer' effect/state. | 1 ||
| [`GenFlag_Boss_Stacy`](Engine_LogicKeys.md#object-genflag_boss_stacy) | Object | Applies or references the 'GenFlag_Boss_Stacy' effect/state. | 1 ||
| `head_start` | Number || 1 ||
| [`home`](Events_and_Encounters.md#object-home) | Object || 1 ||
| [`huntercat`](./Enums.md#enum-huntercat) | Enum || 1 ||
| [`IceAgeUnlocked`](Engine_LogicKeys.md#object-iceageunlocked) | Object | Applies or references the 'IceAgeUnlocked' effect/state. | 1 ||
| [`iceelemental`](./Enums.md#enum-iceelemental) | Enum || 1 ||
| [`infestedduo`](./Enums.md#enum-infestedduo) | Enum || 1 ||
| [`JunkyardUnlocked`](Engine_LogicKeys.md#object-junkyardunlocked) | Object | Applies or references the 'JunkyardUnlocked' effect/state. | 1 ||
| [`JurassicUnlocked`](Engine_LogicKeys.md#object-jurassicunlocked) | Object | Applies or references the 'JurassicUnlocked' effect/state. | 1 ||
| [`lenny`](./Enums.md#enum-lenny) | Enum || 1 ||
| [`lightningelemental`](./Enums.md#enum-lightningelemental) | Enum || 1 ||
| `locked` | Boolean || 1 ||
| [`mamamaggot`](./Enums.md#enum-mamamaggot) | Enum || 1 ||
| [`MeatWorldUnlockedFull`](Engine_LogicKeys.md#object-meatworldunlockedfull) | Object | Applies or references the 'MeatWorldUnlockedFull' effect/state. | 1 ||
| [`miniboss_event`](#object-miniboss_event) | Object | Defines a miniboss event node, specifying its type and level. | 1 ||
| [`MoonUnlocked`](Engine_LogicKeys.md#object-moonunlocked) | Object | Applies or references the 'MoonUnlocked' effect/state. | 1 ||
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum || 1 ||
| [`mw_altar`](#object-mw_altar) | Object || 1 ||
| [`mw_battle1`](#object-mw_battle1) | Object | Defines a battle node on the Meat World map, with properties like type, hidden status, and music override. | 1 ||
| [`mw_boss`](#object-mw_boss) | Object | Defines a boss encounter node on the Meat World map, with properties for cutscene and music. | 1 ||
| [`mw_earlyhome`](#object-mw_earlyhome) | Object | Defines an early home node on the Meat World map, typically hidden or used for early access. | 1 ||
| [`mw_event1`](#object-mw_event1) | Object | Defines an event node on the Meat World map, with properties like type and hidden status. | 1 ||
| [`mw_hard1`](#object-mw_hard1) | Object | Defines a hard difficulty battle node on the Meat World map, with optional music layer override. | 1 ||
| [`mw_home`](#object-mw_home) | Object | Defines a home node on the Meat World map, with properties for type and visibility. | 1 ||
| [`mw_quest_event`](#object-mw_quest_event) | Object | Defines a quest event node on the Meat World map, with overrides for level and art. | 1 ||
| [`mw_treasure`](#object-mw_treasure) | Object | Defines a treasure node on the Meat World map, with type and hidden status. | 1 ||
| [`ratking`](./Enums.md#enum-ratking) | Enum || 1 ||
| [`rockybobo`](./Enums.md#enum-rockybobo) | Enum || 1 ||
| [`SewersUnlocked`](Engine_LogicKeys.md#object-sewersunlocked) | Object | Applies or references the 'SewersUnlocked' effect/state. | 1 ||
| [`shop_cheapwater`](#object-shop_cheapwater) | Object || 1 ||
| [`shop_water`](#object-shop_water) | Object || 1 ||
| [`slime`](./Enums.md#enum-slime) | Enum || 1 ||
| [`spawn_node`](./Enums.md#enum-spawn_node) | Enum || 1 ||
| [`stacy`](./Enums.md#enum-stacy) | Enum || 1 ||
| [`tankcat`](./Enums.md#enum-tankcat) | Enum || 1 ||
| [`thebloat`](./Enums.md#enum-thebloat) | Enum || 1 ||
| [`TheEndUnlocked`](Engine_LogicKeys.md#object-theendunlocked) | Object | Applies or references the 'TheEndUnlocked' effect/state. | 1 ||
| [`ThrobbingArteryDone`](Engine_LogicKeys.md#object-throbbingarterydone) | Object | Applies or references the 'ThrobbingArteryDone' effect/state. | 1 ||
| [`trampy`](./Enums.md#enum-trampy) | Enum || 1 ||
| [`WallOfFleshDone`](Engine_LogicKeys.md#object-walloffleshdone) | Object | Applies or references the 'WallOfFleshDone' effect/state. | 1 ||
| [`weather_event`](#object-weather_event) | Object || 1 ||
| [`choose_one`](./Arrays.md#array-choose_one) | Array || 1 ||
| [`nemesis`](./Arrays.md#array-nemesis) | Array || 1 ||
| :--- | :--- | :--- | :--- | :--- |

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
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 19 ||
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum || 16 ||
| `is_final_boss` | Boolean || 2 ||
| [`level`](./Enums.md#enum-level) | Enum || 2 ||
| [`override_music`](./Enums.md#enum-override_music) | Enum || 2 ||
| [`tileset`](./Enums.md#enum-tileset) | Enum || 1 ||
| [`unlockcheck_on_complete`](./Enums.md#enum-unlockcheck_on_complete) | Enum || 1 ||

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
| `locked` | Boolean || 17 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 15 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 15 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 15 ||
| `hidden` | Boolean || 10 ||

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
| [`override_art`](./Enums.md#enum-override_art) | Enum || 24 ||
| [`level`](./Enums.md#enum-level) | Enum || 19 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 11 ||

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
| `locked` | Boolean || 5 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 3 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 3 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 3 ||

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
| `locked` | Boolean || 4 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||

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
| [`level`](./Enums.md#enum-level) | Enum || 4 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 4 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 ||

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
| [`hard_initial`](#object-hard_initial) | Object | Defines initial properties for the hard path node, such as type and locked state. | 2 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 2 ||
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 ||

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
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 ||
| [`level`](./Enums.md#enum-level) | Enum || 1 ||

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
| `hidden` | Boolean || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 2 ||
| [`boss_cutscene`](./Enums.md#enum-boss_cutscene) | Enum || 1 ||
| [`override_music`](./Enums.md#enum-override_music) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 2 ||
| [`musiclayer`](./Enums.md#enum-musiclayer) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 2 ||
| [`level`](./Enums.md#enum-level) | Enum || 1 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 2 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 2 ||

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
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`exit1`](#object-exit1) | Object | Defines the properties of the second exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| `spin_cats` | Boolean || 1 ||

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
| `spin_cats` | Boolean || 1 ||

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
| [`level`](./Enums.md#enum-level) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 1 ||
| `locked` | Boolean || 1 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 1 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `hidden` | Boolean || 1 ||
| `locked` | Boolean || 1 ||
| [`next_map`](./Enums.md#enum-next_map) | Enum || 1 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `spin_cats` | Boolean || 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 1 ||

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
| [`boss`](Combat_Rewards.md#object-boss) | Object | Configures boss encounter properties, including type, rewards, and cutscene. | 1 ||

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
| [`boss`](Combat_Rewards.md#object-boss) | Object | Configures boss encounter properties, including type, rewards, and cutscene. | 1 ||
| [`miniboss_event`](#object-miniboss_event) | Object | Defines a miniboss event node, specifying its type and level. | 1 ||

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
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `spin_cats` | Boolean || 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 1 ||

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
| [`exit1`](#object-exit1) | Object | Defines the properties of the second exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| `spin_cats` | Boolean || 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`mw_battle1`](#object-mw_battle1) | Object | Defines a battle node on the Meat World map, with properties like type, hidden status, and music override. | 1 ||
| [`mw_boss`](#object-mw_boss) | Object | Defines a boss encounter node on the Meat World map, with properties for cutscene and music. | 1 ||
| [`mw_earlyhome`](#object-mw_earlyhome) | Object | Defines an early home node on the Meat World map, typically hidden or used for early access. | 1 ||
| [`mw_event1`](#object-mw_event1) | Object | Defines an event node on the Meat World map, with properties like type and hidden status. | 1 ||
| [`mw_hard1`](#object-mw_hard1) | Object | Defines a hard difficulty battle node on the Meat World map, with optional music layer override. | 1 ||
| [`mw_home`](#object-mw_home) | Object | Defines a home node on the Meat World map, with properties for type and visibility. | 1 ||
| [`mw_quest_event`](#object-mw_quest_event) | Object | Defines a quest event node on the Meat World map, with overrides for level and art. | 1 ||
| [`mw_treasure`](#object-mw_treasure) | Object | Defines a treasure node on the Meat World map, with type and hidden status. | 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`level`](./Enums.md#enum-level) | Enum || 1 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`level`](./Enums.md#enum-level) | Enum || 1 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| [`level`](./Enums.md#enum-level) | Enum || 1 ||
| [`override_art`](./Enums.md#enum-override_art) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| `spin_cats` | Boolean || 1 ||

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
| [`exit0`](#object-exit0) | Object | Defines the properties of the first exit node on a map, such as its type, destination, and locked state. | 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 1 ||

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
| [`level`](./Enums.md#enum-level) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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
| [`quest_event`](#object-quest_event) | Object | Defines a quest-related event node on the map, specifying the quest level and optional art override. | 1 ||

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
| [`level`](./Enums.md#enum-level) | Enum || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 ||

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

</details>

### Object: `boneyard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `bunker`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `caves`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `core`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `crater`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `desert`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `junkyard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `lab`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `meatworld`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `moon`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `sewers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
