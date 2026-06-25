# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Progression Unlocks

> **Associated Files:** `data/adventure_progression_unlocks.gon, data/npc_favor_unlocks.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 266

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 890 |
| [`popup`](#object-popup) | Object |  | 266 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 206 |
| [`complete_chapter_with_class`](./Arrays.md#array-complete_chapter_with_class) | Array |  | 129 |
| [`unlock_item_immediate`](./Enums.md#enum-unlock_item_immediate) | Enum |  | 127 |
| [`trigger_npc_sequence`](./Enums.md#enum-trigger_npc_sequence) | Enum |  | 55 |
| [`beat_house_boss`](./Enums.md#enum-beat_house_boss) | Enum |  | 48 |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum |  | 36 |
| `required_difficulty` | Integer |  | 36 |
| `repeat` | Integer |  | 32 |
| [`beat_chapter_boss`](./Enums.md#enum-beat_chapter_boss) | Enum |  | 31 |
| [`unlock_ability`](./Enums.md#enum-unlock_ability) | Enum |  | 31 |
| [`unlock_passive`](./Enums.md#enum-unlock_passive) | Enum |  | 29 |
| [`unlock_song`](./Enums.md#enum-unlock_song) | Enum |  | 29 |
| [`set_mapgen_flag`](./Enums.md#enum-set_mapgen_flag) | Enum |  | 23 |
| [`complete_checklist_with_class`](./Enums.md#enum-complete_checklist_with_class) | Enum |  | 14 |
| [`unlock_quest_item`](./Enums.md#enum-unlock_quest_item) | Enum |  | 13 |
| [`trigger_house_boss`](./Enums.md#enum-trigger_house_boss) | Enum |  | 10 |
| `repeatable` | Boolean |  | 10 |
| [`complete_act_difficulty`](./Arrays.md#array-complete_act_difficulty) | Array |  | 9 |
| [`unlock_act_difficulty`](./Arrays.md#array-unlock_act_difficulty) | Array |  | 9 |
| [`queue_cutscene_immediate`](./Enums.md#enum-queue_cutscene_immediate) | Enum |  | 8 |
| [`reset_npc_sequence`](./Enums.md#enum-reset_npc_sequence) | Enum |  | 8 |
| [`preempt_npc_sequence`](./Enums.md#enum-preempt_npc_sequence) | Enum |  | 6 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 6 |
| [`unlock_boss`](./Enums.md#enum-unlock_boss) | Enum |  | 6 |
| [`fail_item_quest`](./Enums.md#enum-fail_item_quest) | Enum |  | 4 |
| [`post_combat_cutscene`](./Enums.md#enum-post_combat_cutscene) | Enum |  | 4 |
| [`trigger_npc_sequence_tomorrow`](./Enums.md#enum-trigger_npc_sequence_tomorrow) | Enum |  | 4 |
| [`unlock_npc_tomorrow`](./Enums.md#enum-unlock_npc_tomorrow) | Enum |  | 4 |
| [`visit_chapter`](./Enums.md#enum-visit_chapter) | Enum |  | 4 |
| `fully_complete_difficulty` | Integer |  | 4 |
| [`complete_chapters`](./Arrays.md#array-complete_chapters) | Array |  | 3 |
| [`requires_unlocked_npc`](./Enums.md#enum-requires_unlocked_npc) | Enum |  | 3 |
| `requires_monoclass_run` | Boolean |  | 3 |
| [`complete_adventure`](./Enums.md#enum-complete_adventure) | Enum |  | 2 |
| [`require_beat_house_boss`](./Enums.md#enum-require_beat_house_boss) | Enum |  | 2 |
| [`require_mapgen_flag`](./Enums.md#enum-require_mapgen_flag) | Enum |  | 2 |
| [`surviving_kaiju`](./Enums.md#enum-surviving_kaiju) | Enum |  | 2 |
| [`unlock_levelgroup`](./Enums.md#enum-unlock_levelgroup) | Enum |  | 2 |
| [`beanies_quests_intro`](#object-beanies_quests_intro) | Object |  | 1 |
| [`beanies_quests_repeat`](#object-beanies_quests_repeat) | Object |  | 1 |
| [`destinations`](#object-destinations) | Object |  | 1 |
| [`fail_adventure`](./Enums.md#enum-fail_adventure) | Enum |  | 1 |
| [`finish_quest`](./Enums.md#enum-finish_quest) | Enum |  | 1 |
| [`frank_max_intro`](#object-frank_max_intro) | Object |  | 1 |
| [`frank_max_repeating`](#object-frank_max_repeating) | Object |  | 1 |
| [`house_upgrade_4throom`](#object-house_upgrade_4throom) | Object |  | 1 |
| [`house_upgrade_attic`](#object-house_upgrade_attic) | Object |  | 1 |
| [`house_upgrade_largehouse`](#object-house_upgrade_largehouse) | Object |  | 1 |
| [`house_upgrade_mediumhouse`](#object-house_upgrade_mediumhouse) | Object |  | 1 |
| [`increment_savefile_counter`](./Enums.md#enum-increment_savefile_counter) | String |  | 1 |
| [`intro`](./Arrays.md#array-intro) | Array |  | 1 |
| [`jack_max_intro`](#object-jack_max_intro) | Object |  | 1 |
| [`jack_max_repeating`](#object-jack_max_repeating) | Object |  | 1 |
| [`jack_shopupgrade1`](#object-jack_shopupgrade1) | Object |  | 1 |
| [`jack_shopupgrade2`](#object-jack_shopupgrade2) | Object |  | 1 |
| [`jack_shopupgrade3`](#object-jack_shopupgrade3) | Object |  | 1 |
| [`jack_shopupgrade4`](#object-jack_shopupgrade4) | Object |  | 1 |
| [`main_pool`](./Arrays.md#array-main_pool) | Array |  | 1 |
| [`organ_max_intro`](#object-organ_max_intro) | Object |  | 1 |
| [`organ_max_repeating`](#object-organ_max_repeating) | Object |  | 1 |
| [`organ_unlock`](#object-organ_unlock) | Object |  | 1 |
| [`organ_upgrade1`](#object-organ_upgrade1) | Object |  | 1 |
| [`organ_upgrade2`](#object-organ_upgrade2) | Object |  | 1 |
| [`organ_upgrade3`](#object-organ_upgrade3) | Object |  | 1 |
| [`organ_upgrade4`](#object-organ_upgrade4) | Object |  | 1 |
| [`organ_upgrade5`](#object-organ_upgrade5) | Object |  | 1 |
| [`organ_upgrade6`](#object-organ_upgrade6) | Object |  | 1 |
| [`prereqs`](#object-prereqs) | Object |  | 1 |
| [`reset_unlock`](./Enums.md#enum-reset_unlock) | Enum |  | 1 |
| [`steven_milliontrashed`](#object-steven_milliontrashed) | Object |  | 1 |
| [`tink_aggression`](#object-tink_aggression) | Object |  | 1 |
| [`tink_basestats`](#object-tink_basestats) | Object |  | 1 |
| [`tink_inbreeding`](#object-tink_inbreeding) | Object |  | 1 |
| [`tink_max_intro`](#object-tink_max_intro) | Object |  | 1 |
| [`tink_max_repeating`](#object-tink_max_repeating) | Object |  | 1 |
| [`tink_prettybow`](#object-tink_prettybow) | Object |  | 1 |
| [`tink_relationships`](#object-tink_relationships) | Object |  | 1 |
| [`tink_sexuality`](#object-tink_sexuality) | Object |  | 1 |
| [`tink_tags`](#object-tink_tags) | Object |  | 1 |
| [`tracy_blankcollar1`](#object-tracy_blankcollar1) | Object |  | 1 |
| [`tracy_blankcollar2`](#object-tracy_blankcollar2) | Object |  | 1 |
| [`tracy_blankcollar3`](#object-tracy_blankcollar3) | Object |  | 1 |
| [`tracy_foodstorage10`](#object-tracy_foodstorage10) | Object |  | 1 |
| [`tracy_foodstorage1`](#object-tracy_foodstorage1) | Object |  | 1 |
| [`tracy_foodstorage2`](#object-tracy_foodstorage2) | Object |  | 1 |
| [`tracy_foodstorage3`](#object-tracy_foodstorage3) | Object |  | 1 |
| [`tracy_foodstorage4`](#object-tracy_foodstorage4) | Object |  | 1 |
| [`tracy_foodstorage5`](#object-tracy_foodstorage5) | Object |  | 1 |
| [`tracy_foodstorage6`](#object-tracy_foodstorage6) | Object |  | 1 |
| [`tracy_foodstorage7`](#object-tracy_foodstorage7) | Object |  | 1 |
| [`tracy_foodstorage8`](#object-tracy_foodstorage8) | Object |  | 1 |
| [`tracy_foodstorage9`](#object-tracy_foodstorage9) | Object |  | 1 |
| [`tracy_idol1`](#object-tracy_idol1) | Object |  | 1 |
| [`tracy_idol2`](#object-tracy_idol2) | Object |  | 1 |
| [`tracy_idol3`](#object-tracy_idol3) | Object |  | 1 |
| [`tracy_idol4`](#object-tracy_idol4) | Object |  | 1 |
| [`tracy_idol5`](#object-tracy_idol5) | Object |  | 1 |
| [`tracy_idol6`](#object-tracy_idol6) | Object |  | 1 |
| [`tracy_idol7`](#object-tracy_idol7) | Object |  | 1 |
| [`tracy_max_intro`](#object-tracy_max_intro) | Object |  | 1 |
| [`tracy_max_repeating`](#object-tracy_max_repeating) | Object |  | 1 |
| [`unlock_item`](./Enums.md#enum-unlock_item) | Enum |  | 1 |
| [`upgrade_storage_1`](#object-upgrade_storage_1) | Object |  | 1 |
| [`upgrade_storage_2`](#object-upgrade_storage_2) | Object |  | 1 |
| [`upgrade_storage_3`](#object-upgrade_storage_3) | Object |  | 1 |
| [`upgrade_storage_4`](#object-upgrade_storage_4) | Object |  | 1 |
| [`upgrade_storage_5`](#object-upgrade_storage_5) | Object |  | 1 |
| [`upgrade_storage_6`](#object-upgrade_storage_6) | Object |  | 1 |
| [`upgrade_storage_7`](#object-upgrade_storage_7) | Object |  | 1 |
| [`upgrade_storage_repeating_crazy`](#object-upgrade_storage_repeating_crazy) | Object |  | 1 |
| [`upgrade_storage_repeating_hard`](#object-upgrade_storage_repeating_hard) | Object |  | 1 |
| [`upgrade_storage_repeating_impossible`](#object-upgrade_storage_repeating_impossible) | Object |  | 1 |
| [`upgrade_storage_repeating_intro`](#object-upgrade_storage_repeating_intro) | Object |  | 1 |
| [`upgrade_storage_repeating_normal`](#object-upgrade_storage_repeating_normal) | Object |  | 1 |
| `requires_hard_path` | Boolean |  | 1 |

</details>

---

### Object: `popup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 266

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 266 |
| `immediate` | Boolean |  | 221 |
| [`frame`](./Enums.md#enum-frame) | Enum |  | 159 |

</details>

---

### Object: `tracy_special_item`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 22

> **Referenced by:** [`tracy_blankcollar1`](#object-tracy_blankcollar1), [`tracy_blankcollar2`](#object-tracy_blankcollar2), [`tracy_blankcollar3`](#object-tracy_blankcollar3), [`tracy_foodstorage1`](#object-tracy_foodstorage1), [`tracy_foodstorage10`](#object-tracy_foodstorage10), [`tracy_foodstorage2`](#object-tracy_foodstorage2), [`tracy_foodstorage3`](#object-tracy_foodstorage3), [`tracy_foodstorage4`](#object-tracy_foodstorage4), [`tracy_foodstorage5`](#object-tracy_foodstorage5), [`tracy_foodstorage6`](#object-tracy_foodstorage6), [`tracy_foodstorage7`](#object-tracy_foodstorage7), [`tracy_foodstorage8`](#object-tracy_foodstorage8), [`tracy_foodstorage9`](#object-tracy_foodstorage9), [`tracy_idol1`](#object-tracy_idol1), [`tracy_idol2`](#object-tracy_idol2), [`tracy_idol3`](#object-tracy_idol3), [`tracy_idol4`](#object-tracy_idol4), [`tracy_idol5`](#object-tracy_idol5), [`tracy_idol6`](#object-tracy_idol6), [`tracy_idol7`](#object-tracy_idol7), [`tracy_max_intro`](#object-tracy_max_intro), [`tracy_max_repeating`](#object-tracy_max_repeating)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum |  | 22 |
| `cost` | Integer |  | 22 |

</details>

---

### Object: `beanies_quests_intro`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `beanies_quests_repeat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `destinations`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `boneyard` | Integer |  | 1 |
| `caves` | Integer |  | 1 |
| `core` | Integer |  | 1 |
| `dimensionx` | Integer |  | 1 |
| `endoftime` | Integer |  | 1 |
| `jurassic` | Integer |  | 1 |
| `meatworld` | Integer |  | 1 |
| `moon` | Integer |  | 1 |
| `theend` | Integer |  | 1 |

</details>

---

### Object: `frank_max_intro`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `frank_max_repeating`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `house_upgrade_4throom`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `house_upgrade_attic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `house_upgrade_largehouse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 2 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `house_upgrade_mediumhouse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum |  | 2 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `jack_max_intro`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `rep_reward_count` | Integer |  | 1 |

</details>

---

### Object: `jack_max_repeating`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `rep_reward_count` | Integer |  | 1 |

</details>

---

### Object: `jack_shopupgrade1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `jack_shopupgrade2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `jack_shopupgrade3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `jack_shopupgrade4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `organ_max_intro`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `organ_max_repeating`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `organ_unlock`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `organ_upgrade1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `organ_upgrade2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `organ_upgrade3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `organ_upgrade4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `organ_upgrade5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `organ_upgrade6`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `prereqs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`core`](./Enums.md#enum-core) | Enum |  | 1 |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum |  | 1 |
| [`endoftime`](./Enums.md#enum-endoftime) | Enum |  | 1 |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum |  | 1 |
| [`moon`](./Enums.md#enum-moon) | Enum |  | 1 |
| [`theend`](./Enums.md#enum-theend) | Enum |  | 1 |

</details>

---

### Object: `steven_milliontrashed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_aggression`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_basestats`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_inbreeding`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_max_intro`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `coins` | Integer |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_max_repeating`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `coins` | Integer |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_prettybow`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_relationships`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_sexuality`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tink_tags`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | String |  | 1 |
| `favor` | Integer |  | 1 |

</details>

---

### Object: `tracy_blankcollar1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_blankcollar2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_blankcollar3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage10`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage6`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage7`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage8`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_foodstorage9`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_idol1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_idol2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_idol3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_idol4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_idol5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_idol6`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_idol7`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |
| `shop_level_up` | Integer |  | 1 |

</details>

---

### Object: `tracy_max_intro`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |

</details>

---

### Object: `tracy_max_repeating`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| [`tracy_special_item`](#object-tracy_special_item) | Object |  | 1 |
| `favor` | Integer |  | 1 |
| `required_age` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `storage_expansion` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `storage_expansion` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `storage_expansion` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `storage_expansion` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `storage_expansion` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_6`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `storage_expansion` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_7`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `storage_expansion` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_repeating_crazy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `rep_reward_count` | Integer |  | 1 |
| `repeat` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `required_difficulty` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_repeating_hard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `rep_reward_count` | Integer |  | 1 |
| `repeat` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `required_difficulty` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_repeating_impossible`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `rep_reward_count` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `required_difficulty` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_repeating_intro`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `rep_reward_count` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `required_difficulty` | Integer |  | 1 |

</details>

---

### Object: `upgrade_storage_repeating_normal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`level_display`](./Enums.md#enum-level_display) | Enum |  | 1 |
| [`reward_text`](./Strings.md#string-reward_text) | String |  | 1 |
| `favor` | Integer |  | 1 |
| `rep_reward_count` | Integer |  | 1 |
| `repeat` | Integer |  | 1 |
| `required_act` | Integer |  | 1 |
| `required_chapter` | Integer |  | 1 |
| `required_difficulty` | Integer |  | 1 |

</details>

---

