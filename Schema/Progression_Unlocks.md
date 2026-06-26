# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Progression Unlocks

> **Associated Files:** `data/adventure_progression_unlocks.gon, data/npc_favor_unlocks.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 266

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 883 |  |
| [`popup`](#object-popup) | Object |  | 532 |  |
| [`unlock_item_immediate`](./Enums.md#enum-unlock_item_immediate) | Enum |  | 254 |  |
| [`intro`](./Arrays.md#array-intro) | Array |  | 216 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 206 |  |
| [`complete_chapter_with_class`](./Arrays.md#array-complete_chapter_with_class) | Array |  | 129 |  |
| [`trigger_npc_sequence`](./Enums.md#enum-trigger_npc_sequence) | Enum |  | 110 |  |
| [`beat_house_boss`](./Enums.md#enum-beat_house_boss) | Enum |  | 96 |  |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum |  | 90 |  |
| `required_difficulty` | Integer |  | 72 |  |
| `repeat` | Integer |  | 66 |  |
| [`beat_chapter_boss`](./Enums.md#enum-beat_chapter_boss) | Enum |  | 62 |  |
| [`unlock_ability`](./Enums.md#enum-unlock_ability) | Enum |  | 62 |  |
| [`unlock_passive`](./Enums.md#enum-unlock_passive) | Enum |  | 58 |  |
| [`unlock_song`](./Enums.md#enum-unlock_song) | Enum |  | 58 |  |
| [`set_mapgen_flag`](./Enums.md#enum-set_mapgen_flag) | Enum |  | 46 |  |
| [`complete_checklist_with_class`](./Enums.md#enum-complete_checklist_with_class) | Enum |  | 28 |  |
| [`unlock_quest_item`](./Enums.md#enum-unlock_quest_item) | Enum |  | 26 |  |
| `repeatable` | Boolean |  | 20 |  |
| [`trigger_house_boss`](./Enums.md#enum-trigger_house_boss) | Enum |  | 20 |  |
| [`queue_cutscene_immediate`](./Enums.md#enum-queue_cutscene_immediate) | Enum |  | 16 |  |
| [`reset_npc_sequence`](./Enums.md#enum-reset_npc_sequence) | Enum |  | 16 |  |
| [`preempt_npc_sequence`](./Enums.md#enum-preempt_npc_sequence) | Enum |  | 12 |  |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 12 |  |
| [`unlock_boss`](./Enums.md#enum-unlock_boss) | Enum |  | 12 |  |
| [`complete_act_difficulty`](./Arrays.md#array-complete_act_difficulty) | Array |  | 9 |  |
| [`unlock_act_difficulty`](./Arrays.md#array-unlock_act_difficulty) | Array |  | 9 |  |
| [`fail_item_quest`](./Enums.md#enum-fail_item_quest) | Enum |  | 8 |  |
| `fully_complete_difficulty` | Integer |  | 8 |  |
| [`post_combat_cutscene`](./Enums.md#enum-post_combat_cutscene) | Enum |  | 8 |  |
| [`trigger_npc_sequence_tomorrow`](./Enums.md#enum-trigger_npc_sequence_tomorrow) | Enum |  | 8 |  |
| [`unlock_npc_tomorrow`](./Enums.md#enum-unlock_npc_tomorrow) | Enum |  | 8 |  |
| [`visit_chapter`](./Enums.md#enum-visit_chapter) | Enum |  | 8 |  |
| `requires_monoclass_run` | Boolean |  | 6 |  |
| [`requires_unlocked_npc`](./Enums.md#enum-requires_unlocked_npc) | Enum |  | 6 |  |
| [`beanies_quests_intro`](#object-beanies_quests_intro) | Object |  | 4 |  |
| [`beanies_quests_repeat`](#object-beanies_quests_repeat) | Object |  | 4 |  |
| [`complete_adventure`](./Enums.md#enum-complete_adventure) | Enum |  | 4 |  |
| [`frank_max_intro`](#object-frank_max_intro) | Object |  | 4 |  |
| [`frank_max_repeating`](#object-frank_max_repeating) | Object |  | 4 |  |
| [`house_upgrade_4throom`](#object-house_upgrade_4throom) | Object |  | 4 |  |
| [`house_upgrade_attic`](#object-house_upgrade_attic) | Object |  | 4 |  |
| [`house_upgrade_largehouse`](#object-house_upgrade_largehouse) | Object |  | 4 |  |
| [`house_upgrade_mediumhouse`](#object-house_upgrade_mediumhouse) | Object |  | 4 |  |
| [`jack_max_intro`](#object-jack_max_intro) | Object |  | 4 |  |
| [`jack_max_repeating`](#object-jack_max_repeating) | Object |  | 4 |  |
| [`jack_shopupgrade1`](#object-jack_shopupgrade1) | Object |  | 4 |  |
| [`jack_shopupgrade2`](#object-jack_shopupgrade2) | Object |  | 4 |  |
| [`jack_shopupgrade3`](#object-jack_shopupgrade3) | Object |  | 4 |  |
| [`jack_shopupgrade4`](#object-jack_shopupgrade4) | Object |  | 4 |  |
| [`organ_max_intro`](#object-organ_max_intro) | Object |  | 4 |  |
| [`organ_max_repeating`](#object-organ_max_repeating) | Object |  | 4 |  |
| [`organ_unlock`](#object-organ_unlock) | Object |  | 4 |  |
| [`organ_upgrade1`](#object-organ_upgrade1) | Object |  | 4 |  |
| [`organ_upgrade2`](#object-organ_upgrade2) | Object |  | 4 |  |
| [`organ_upgrade3`](#object-organ_upgrade3) | Object |  | 4 |  |
| [`organ_upgrade4`](#object-organ_upgrade4) | Object |  | 4 |  |
| [`organ_upgrade5`](#object-organ_upgrade5) | Object |  | 4 |  |
| [`organ_upgrade6`](#object-organ_upgrade6) | Object |  | 4 |  |
| [`require_beat_house_boss`](./Enums.md#enum-require_beat_house_boss) | Enum |  | 4 |  |
| [`require_mapgen_flag`](./Enums.md#enum-require_mapgen_flag) | Enum |  | 4 |  |
| [`steven_milliontrashed`](#object-steven_milliontrashed) | Object |  | 4 |  |
| [`surviving_kaiju`](./Enums.md#enum-surviving_kaiju) | Enum |  | 4 |  |
| [`tink_aggression`](#object-tink_aggression) | Object |  | 4 |  |
| [`tink_basestats`](#object-tink_basestats) | Object |  | 4 |  |
| [`tink_inbreeding`](#object-tink_inbreeding) | Object |  | 4 |  |
| [`tink_max_intro`](#object-tink_max_intro) | Object |  | 4 |  |
| [`tink_max_repeating`](#object-tink_max_repeating) | Object |  | 4 |  |
| [`tink_prettybow`](#object-tink_prettybow) | Object |  | 4 |  |
| [`tink_relationships`](#object-tink_relationships) | Object |  | 4 |  |
| [`tink_sexuality`](#object-tink_sexuality) | Object |  | 4 |  |
| [`tink_tags`](#object-tink_tags) | Object |  | 4 |  |
| [`tracy_blankcollar1`](#object-tracy_blankcollar1) | Object |  | 4 |  |
| [`tracy_blankcollar2`](#object-tracy_blankcollar2) | Object |  | 4 |  |
| [`tracy_blankcollar3`](#object-tracy_blankcollar3) | Object |  | 4 |  |
| [`tracy_foodstorage1`](#object-tracy_foodstorage1) | Object |  | 4 |  |
| [`tracy_foodstorage10`](#object-tracy_foodstorage10) | Object |  | 4 |  |
| [`tracy_foodstorage2`](#object-tracy_foodstorage2) | Object |  | 4 |  |
| [`tracy_foodstorage3`](#object-tracy_foodstorage3) | Object |  | 4 |  |
| [`tracy_foodstorage4`](#object-tracy_foodstorage4) | Object |  | 4 |  |
| [`tracy_foodstorage5`](#object-tracy_foodstorage5) | Object |  | 4 |  |
| [`tracy_foodstorage6`](#object-tracy_foodstorage6) | Object |  | 4 |  |
| [`tracy_foodstorage7`](#object-tracy_foodstorage7) | Object |  | 4 |  |
| [`tracy_foodstorage8`](#object-tracy_foodstorage8) | Object |  | 4 |  |
| [`tracy_foodstorage9`](#object-tracy_foodstorage9) | Object |  | 4 |  |
| [`tracy_idol1`](#object-tracy_idol1) | Object |  | 4 |  |
| [`tracy_idol2`](#object-tracy_idol2) | Object |  | 4 |  |
| [`tracy_idol3`](#object-tracy_idol3) | Object |  | 4 |  |
| [`tracy_idol4`](#object-tracy_idol4) | Object |  | 4 |  |
| [`tracy_idol5`](#object-tracy_idol5) | Object |  | 4 |  |
| [`tracy_idol6`](#object-tracy_idol6) | Object |  | 4 |  |
| [`tracy_idol7`](#object-tracy_idol7) | Object |  | 4 |  |
| [`tracy_max_intro`](#object-tracy_max_intro) | Object |  | 4 |  |
| [`tracy_max_repeating`](#object-tracy_max_repeating) | Object |  | 4 |  |
| [`unlock_levelgroup`](./Enums.md#enum-unlock_levelgroup) | Enum |  | 4 |  |
| [`upgrade_storage_1`](#object-upgrade_storage_1) | Object |  | 4 |  |
| [`upgrade_storage_2`](#object-upgrade_storage_2) | Object |  | 4 |  |
| [`upgrade_storage_3`](#object-upgrade_storage_3) | Object |  | 4 |  |
| [`upgrade_storage_4`](#object-upgrade_storage_4) | Object |  | 4 |  |
| [`upgrade_storage_5`](#object-upgrade_storage_5) | Object |  | 4 |  |
| [`upgrade_storage_6`](#object-upgrade_storage_6) | Object |  | 4 |  |
| [`upgrade_storage_7`](#object-upgrade_storage_7) | Object |  | 4 |  |
| [`upgrade_storage_repeating_crazy`](#object-upgrade_storage_repeating_crazy) | Object |  | 4 |  |
| [`upgrade_storage_repeating_hard`](#object-upgrade_storage_repeating_hard) | Object |  | 4 |  |
| [`upgrade_storage_repeating_impossible`](#object-upgrade_storage_repeating_impossible) | Object |  | 4 |  |
| [`upgrade_storage_repeating_intro`](#object-upgrade_storage_repeating_intro) | Object |  | 4 |  |
| [`upgrade_storage_repeating_normal`](#object-upgrade_storage_repeating_normal) | Object |  | 4 |  |
| [`complete_chapters`](./Arrays.md#array-complete_chapters) | Array |  | 3 |  |
| [`destinations`](#object-destinations) | Object |  | 2 |  |
| [`fail_adventure`](./Enums.md#enum-fail_adventure) | Enum |  | 2 |  |
| [`finish_quest`](./Enums.md#enum-finish_quest) | Enum |  | 2 |  |
| [`increment_savefile_counter`](./Enums.md#enum-increment_savefile_counter) | String |  | 2 |  |
| [`prereqs`](#object-prereqs) | Object |  | 2 |  |
| `requires_hard_path` | Boolean |  | 2 |  |
| [`reset_unlock`](./Enums.md#enum-reset_unlock) | Enum |  | 2 |  |
| [`unlock_item`](./Enums.md#enum-unlock_item) | Enum |  | 2 |  |
| [`main_pool`](./Arrays.md#array-main_pool) | Array |  | 1 |  |

</details>

---

### Object: `popup`


**Definition:** No definition provided.  
**Total Count:** 266


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `immediate` | Boolean |  | 442 |  |
| [`frame`](./Enums.md#enum-frame) | Enum |  | 318 |  |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 266 |  |

</details>

---

### Object: `tracy_special_item`


**Definition:** No definition provided.  
**Total Count:** 22


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`tracy_blankcollar1`](#object-tracy_blankcollar1), [`tracy_blankcollar2`](#object-tracy_blankcollar2), [`tracy_blankcollar3`](#object-tracy_blankcollar3), [`tracy_foodstorage1`](#object-tracy_foodstorage1), [`tracy_foodstorage10`](#object-tracy_foodstorage10), [`tracy_foodstorage2`](#object-tracy_foodstorage2), [`tracy_foodstorage3`](#object-tracy_foodstorage3), [`tracy_foodstorage4`](#object-tracy_foodstorage4), [`tracy_foodstorage5`](#object-tracy_foodstorage5), [`tracy_foodstorage6`](#object-tracy_foodstorage6), [`tracy_foodstorage7`](#object-tracy_foodstorage7), [`tracy_foodstorage8`](#object-tracy_foodstorage8), [`tracy_foodstorage9`](#object-tracy_foodstorage9), [`tracy_idol1`](#object-tracy_idol1), [`tracy_idol2`](#object-tracy_idol2), [`tracy_idol3`](#object-tracy_idol3), [`tracy_idol4`](#object-tracy_idol4), [`tracy_idol5`](#object-tracy_idol5), [`tracy_idol6`](#object-tracy_idol6), [`tracy_idol7`](#object-tracy_idol7), [`tracy_max_intro`](#object-tracy_max_intro), [`tracy_max_repeating`](#object-tracy_max_repeating)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Integer |  | 44 |  |
| [`type`](./Enums.md#enum-type) | Enum |  | 44 |  |

</details>

---

### Object: `beanies_quests_intro`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `beanies_quests_repeat`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `frank_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `frank_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `house_upgrade_4throom`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `house_upgrade_attic`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `house_upgrade_largehouse`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 4 |  |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `house_upgrade_mediumhouse`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 4 |  |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `jack_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `rep_reward_count` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `jack_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `rep_reward_count` | Integer |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `jack_shopupgrade1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `jack_shopupgrade2`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `jack_shopupgrade3`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `jack_shopupgrade4`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `organ_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `organ_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `organ_unlock`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `organ_upgrade1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `organ_upgrade2`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `organ_upgrade3`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `organ_upgrade4`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `organ_upgrade5`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `organ_upgrade6`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |

</details>

---

### Object: `steven_milliontrashed`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |

</details>

---

### Object: `tink_aggression`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 2 |  |

</details>

---

### Object: `tink_basestats`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 2 |  |

</details>

---

### Object: `tink_inbreeding`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 2 |  |

</details>

---

### Object: `tink_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer |  | 2 |  |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `tink_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer |  | 2 |  |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `tink_prettybow`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `tink_relationships`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 2 |  |

</details>

---

### Object: `tink_sexuality`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 2 |  |

</details>

---

### Object: `tink_tags`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 2 |  |

</details>

---

### Object: `tracy_blankcollar1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_blankcollar2`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_blankcollar3`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage10`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage2`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage3`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage4`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage5`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage6`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage7`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage8`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_foodstorage9`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_idol1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_idol2`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_idol3`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_idol4`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_idol5`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_idol6`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_idol7`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `shop_level_up` | Integer |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_max_intro`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `tracy_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |
| `required_age` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 2 |  |

</details>

---

### Object: `upgrade_storage_1`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `storage_expansion` | Integer |  | 2 |  |

</details>

---

### Object: `upgrade_storage_2`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `storage_expansion` | Integer |  | 2 |  |

</details>

---

### Object: `upgrade_storage_3`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `storage_expansion` | Integer |  | 2 |  |

</details>

---

### Object: `upgrade_storage_4`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `storage_expansion` | Integer |  | 2 |  |

</details>

---

### Object: `upgrade_storage_5`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `storage_expansion` | Integer |  | 2 |  |

</details>

---

### Object: `upgrade_storage_6`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `storage_expansion` | Integer |  | 2 |  |

</details>

---

### Object: `upgrade_storage_7`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |
| `storage_expansion` | Integer |  | 2 |  |

</details>

---

### Object: `upgrade_storage_repeating_crazy`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `rep_reward_count` | Integer |  | 2 |  |
| `repeat` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| `required_difficulty` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `upgrade_storage_repeating_hard`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `rep_reward_count` | Integer |  | 2 |  |
| `repeat` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| `required_difficulty` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `upgrade_storage_repeating_impossible`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `rep_reward_count` | Integer |  | 2 |  |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| `required_difficulty` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `upgrade_storage_repeating_intro`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `rep_reward_count` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| `required_difficulty` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---

### Object: `upgrade_storage_repeating_normal`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `favor` | Integer |  | 2 |  |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 2 |  |
| `rep_reward_count` | Integer |  | 2 |  |
| `repeat` | Integer |  | 2 |  |
| `required_act` | Integer |  | 2 |  |
| `required_chapter` | Integer |  | 2 |  |
| `required_difficulty` | Integer |  | 2 |  |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 2 |  |

</details>

---


### Object: `destinations`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `boneyard` | Integer |  | 2 |  |
| `caves` | Integer |  | 2 |  |
| `core` | Integer |  | 2 |  |
| `dimensionx` | Integer |  | 2 |  |
| `endoftime` | Integer |  | 2 |  |
| `jurassic` | Integer |  | 2 |  |
| `meatworld` | Integer |  | 2 |  |
| `moon` | Integer |  | 2 |  |
| `theend` | Integer |  | 2 |  |

</details>

---

### Object: `prereqs`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`endoftime`](./Enums.md#enum-endoftime) | Enum |  | 6 |  |
| [`core`](./Enums.md#enum-core) | Enum |  | 2 |  |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum |  | 2 |  |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum |  | 2 |  |
| [`moon`](./Enums.md#enum-moon) | Enum |  | 2 |  |
| [`theend`](./Enums.md#enum-theend) | Enum |  | 2 |  |

</details>

---
