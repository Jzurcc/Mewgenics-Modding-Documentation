# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Progression Unlocks

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/266) |
| :--- | :--- | :--- | :--- |
| [`popup`](./Progression_Unlocks.md#context-popup) | Block |  | 266 |
| [`complete_chapter_with_class`](./Arrays.md#array-complete_chapter_with_class) | Array |  | 129 |
| [`unlock_item_immediate`](./Enums.md#enum-unlock_item_immediate) | Enum/String |  | 127 |
| [`trigger_npc_sequence`](./Enums.md#enum-trigger_npc_sequence) | Enum/String |  | 55 |
| [`beat_house_boss`](./Enums.md#enum-beat_house_boss) | Enum/String |  | 48 |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum/String |  | 36 |
| `required_difficulty` | Number |  | 36 |
| `repeat` | Number |  | 32 |
| [`beat_chapter_boss`](./Enums.md#enum-beat_chapter_boss) | Enum/String |  | 31 |
| [`unlock_ability`](./Enums.md#enum-unlock_ability) | Enum/String |  | 31 |
| [`unlock_passive`](./Enums.md#enum-unlock_passive) | Enum/String |  | 29 |
| [`unlock_song`](./Enums.md#enum-unlock_song) | Enum/String |  | 29 |
| [`set_mapgen_flag`](./Enums.md#enum-set_mapgen_flag) | Enum/String |  | 23 |
| [`complete_checklist_with_class`](./Enums.md#enum-complete_checklist_with_class) | Enum/String |  | 14 |
| [`unlock_quest_item`](./Enums.md#enum-unlock_quest_item) | Enum/String |  | 13 |
| `repeatable` | Boolean |  | 10 |
| [`trigger_house_boss`](./Enums.md#enum-trigger_house_boss) | Enum/String |  | 10 |
| [`complete_act_difficulty`](./Arrays.md#array-complete_act_difficulty) | Array |  | 9 |
| [`complete_item_quest`](./Enums.md#enum-complete_item_quest) | Enum/String |  | 9 |
| [`unlock_act_difficulty`](./Arrays.md#array-unlock_act_difficulty) | Array |  | 9 |
| [`queue_cutscene_immediate`](./Enums.md#enum-queue_cutscene_immediate) | Enum/String |  | 8 |
| [`reset_npc_sequence`](./Enums.md#enum-reset_npc_sequence) | Enum/String |  | 8 |
| [`preempt_npc_sequence`](./Enums.md#enum-preempt_npc_sequence) | Enum/String |  | 6 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | Enum/String |  | 6 |
| [`unlock_boss`](./Enums.md#enum-unlock_boss) | Enum/String |  | 6 |
| [`fail_item_quest`](./Enums.md#enum-fail_item_quest) | Enum/String |  | 4 |
| `fully_complete_difficulty` | Number |  | 4 |
| [`post_combat_cutscene`](./Enums.md#enum-post_combat_cutscene) | Enum/String |  | 4 |
| [`trigger_npc_sequence_tomorrow`](./Enums.md#enum-trigger_npc_sequence_tomorrow) | Enum/String |  | 4 |
| [`unlock_npc_tomorrow`](./Enums.md#enum-unlock_npc_tomorrow) | Enum/String |  | 4 |
| [`visit_chapter`](./Enums.md#enum-visit_chapter) | Enum/String |  | 4 |
| [`complete_chapters`](./Arrays.md#array-complete_chapters) | Array |  | 3 |
| `requires_monoclass_run` | Boolean |  | 3 |
| [`requires_unlocked_npc`](./Enums.md#enum-requires_unlocked_npc) | Enum/String |  | 3 |
| [`complete_adventure`](./Enums.md#enum-complete_adventure) | Enum/String |  | 2 |
| [`require_beat_house_boss`](./Enums.md#enum-require_beat_house_boss) | Enum/String |  | 2 |
| [`require_mapgen_flag`](./Enums.md#enum-require_mapgen_flag) | Enum/String |  | 2 |
| [`surviving_kaiju`](./Enums.md#enum-surviving_kaiju) | Enum/String |  | 2 |
| [`unlock_levelgroup`](./Enums.md#enum-unlock_levelgroup) | Enum/String |  | 2 |
| [`beanies_quests_intro`](./Progression_Unlocks.md#context-beanies_quests_intro) | Block |  | 1 |
| [`beanies_quests_repeat`](./Progression_Unlocks.md#context-beanies_quests_repeat) | Block |  | 1 |
| [`destinations`](./Progression_Unlocks.md#context-destinations) | Block |  | 1 |
| [`fail_adventure`](./Enums.md#enum-fail_adventure) | Enum/String |  | 1 |
| [`finish_quest`](./Enums.md#enum-finish_quest) | Enum/String |  | 1 |
| [`frank_max_intro`](./Progression_Unlocks.md#context-frank_max_intro) | Block |  | 1 |
| [`frank_max_repeating`](./Progression_Unlocks.md#context-frank_max_repeating) | Block |  | 1 |
| [`house_upgrade_4throom`](./Progression_Unlocks.md#context-house_upgrade_4throom) | Block |  | 1 |
| [`house_upgrade_attic`](./Progression_Unlocks.md#context-house_upgrade_attic) | Block |  | 1 |
| [`house_upgrade_largehouse`](./Progression_Unlocks.md#context-house_upgrade_largehouse) | Block |  | 1 |
| [`house_upgrade_mediumhouse`](./Progression_Unlocks.md#context-house_upgrade_mediumhouse) | Block |  | 1 |
| [`increment_savefile_counter`](./Enums.md#enum-increment_savefile_counter) | Enum/String |  | 1 |
| [`intro`](./Arrays.md#array-intro) | Array |  | 1 |
| [`jack_max_intro`](./Progression_Unlocks.md#context-jack_max_intro) | Block |  | 1 |
| [`jack_max_repeating`](./Progression_Unlocks.md#context-jack_max_repeating) | Block |  | 1 |
| [`jack_shopupgrade1`](./Progression_Unlocks.md#context-jack_shopupgrade1) | Block |  | 1 |
| [`jack_shopupgrade2`](./Progression_Unlocks.md#context-jack_shopupgrade2) | Block |  | 1 |
| [`jack_shopupgrade3`](./Progression_Unlocks.md#context-jack_shopupgrade3) | Block |  | 1 |
| [`jack_shopupgrade4`](./Progression_Unlocks.md#context-jack_shopupgrade4) | Block |  | 1 |
| [`main_pool`](./Arrays.md#array-main_pool) | Array |  | 1 |
| [`organ_max_intro`](./Progression_Unlocks.md#context-organ_max_intro) | Block |  | 1 |
| [`organ_max_repeating`](./Progression_Unlocks.md#context-organ_max_repeating) | Block |  | 1 |
| [`organ_unlock`](./Progression_Unlocks.md#context-organ_unlock) | Block |  | 1 |
| [`organ_upgrade1`](./Progression_Unlocks.md#context-organ_upgrade1) | Block |  | 1 |
| [`organ_upgrade2`](./Progression_Unlocks.md#context-organ_upgrade2) | Block |  | 1 |
| [`organ_upgrade3`](./Progression_Unlocks.md#context-organ_upgrade3) | Block |  | 1 |
| [`organ_upgrade4`](./Progression_Unlocks.md#context-organ_upgrade4) | Block |  | 1 |
| [`organ_upgrade5`](./Progression_Unlocks.md#context-organ_upgrade5) | Block |  | 1 |
| [`organ_upgrade6`](./Progression_Unlocks.md#context-organ_upgrade6) | Block |  | 1 |
| [`prereqs`](./Progression_Unlocks.md#context-prereqs) | Block |  | 1 |
| `requires_hard_path` | Boolean |  | 1 |
| [`reset_unlock`](./Enums.md#enum-reset_unlock) | Enum/String |  | 1 |
| [`steven_milliontrashed`](./Progression_Unlocks.md#context-steven_milliontrashed) | Block |  | 1 |
| [`tink_aggression`](./Progression_Unlocks.md#context-tink_aggression) | Block |  | 1 |
| [`tink_basestats`](./Progression_Unlocks.md#context-tink_basestats) | Block |  | 1 |
| [`tink_inbreeding`](./Progression_Unlocks.md#context-tink_inbreeding) | Block |  | 1 |
| [`tink_max_intro`](./Progression_Unlocks.md#context-tink_max_intro) | Block |  | 1 |
| [`tink_max_repeating`](./Progression_Unlocks.md#context-tink_max_repeating) | Block |  | 1 |
| [`tink_prettybow`](./Progression_Unlocks.md#context-tink_prettybow) | Block |  | 1 |
| [`tink_relationships`](./Progression_Unlocks.md#context-tink_relationships) | Block |  | 1 |
| [`tink_sexuality`](./Progression_Unlocks.md#context-tink_sexuality) | Block |  | 1 |
| [`tink_tags`](./Progression_Unlocks.md#context-tink_tags) | Block |  | 1 |
| [`tracy_blankcollar1`](./Progression_Unlocks.md#context-tracy_blankcollar1) | Block |  | 1 |
| [`tracy_blankcollar2`](./Progression_Unlocks.md#context-tracy_blankcollar2) | Block |  | 1 |
| [`tracy_blankcollar3`](./Progression_Unlocks.md#context-tracy_blankcollar3) | Block |  | 1 |
| [`tracy_foodstorage1`](./Progression_Unlocks.md#context-tracy_foodstorage1) | Block |  | 1 |
| [`tracy_foodstorage10`](./Progression_Unlocks.md#context-tracy_foodstorage10) | Block |  | 1 |
| [`tracy_foodstorage2`](./Progression_Unlocks.md#context-tracy_foodstorage2) | Block |  | 1 |
| [`tracy_foodstorage3`](./Progression_Unlocks.md#context-tracy_foodstorage3) | Block |  | 1 |
| [`tracy_foodstorage4`](./Progression_Unlocks.md#context-tracy_foodstorage4) | Block |  | 1 |
| [`tracy_foodstorage5`](./Progression_Unlocks.md#context-tracy_foodstorage5) | Block |  | 1 |
| [`tracy_foodstorage6`](./Progression_Unlocks.md#context-tracy_foodstorage6) | Block |  | 1 |
| [`tracy_foodstorage7`](./Progression_Unlocks.md#context-tracy_foodstorage7) | Block |  | 1 |
| [`tracy_foodstorage8`](./Progression_Unlocks.md#context-tracy_foodstorage8) | Block |  | 1 |
| [`tracy_foodstorage9`](./Progression_Unlocks.md#context-tracy_foodstorage9) | Block |  | 1 |
| [`tracy_idol1`](./Progression_Unlocks.md#context-tracy_idol1) | Block |  | 1 |
| [`tracy_idol2`](./Progression_Unlocks.md#context-tracy_idol2) | Block |  | 1 |
| [`tracy_idol3`](./Progression_Unlocks.md#context-tracy_idol3) | Block |  | 1 |
| [`tracy_idol4`](./Progression_Unlocks.md#context-tracy_idol4) | Block |  | 1 |
| [`tracy_idol5`](./Progression_Unlocks.md#context-tracy_idol5) | Block |  | 1 |
| [`tracy_idol6`](./Progression_Unlocks.md#context-tracy_idol6) | Block |  | 1 |
| [`tracy_idol7`](./Progression_Unlocks.md#context-tracy_idol7) | Block |  | 1 |
| [`tracy_max_intro`](./Progression_Unlocks.md#context-tracy_max_intro) | Block |  | 1 |
| [`tracy_max_repeating`](./Progression_Unlocks.md#context-tracy_max_repeating) | Block |  | 1 |
| [`unlock_item`](./Enums.md#enum-unlock_item) | Enum/String |  | 1 |
| [`upgrade_storage_1`](./Progression_Unlocks.md#context-upgrade_storage_1) | Block |  | 1 |
| [`upgrade_storage_2`](./Progression_Unlocks.md#context-upgrade_storage_2) | Block |  | 1 |
| [`upgrade_storage_3`](./Progression_Unlocks.md#context-upgrade_storage_3) | Block |  | 1 |
| [`upgrade_storage_4`](./Progression_Unlocks.md#context-upgrade_storage_4) | Block |  | 1 |
| [`upgrade_storage_5`](./Progression_Unlocks.md#context-upgrade_storage_5) | Block |  | 1 |
| [`upgrade_storage_6`](./Progression_Unlocks.md#context-upgrade_storage_6) | Block |  | 1 |
| [`upgrade_storage_7`](./Progression_Unlocks.md#context-upgrade_storage_7) | Block |  | 1 |
| [`upgrade_storage_repeating_crazy`](./Progression_Unlocks.md#context-upgrade_storage_repeating_crazy) | Block |  | 1 |
| [`upgrade_storage_repeating_hard`](./Progression_Unlocks.md#context-upgrade_storage_repeating_hard) | Block |  | 1 |
| [`upgrade_storage_repeating_impossible`](./Progression_Unlocks.md#context-upgrade_storage_repeating_impossible) | Block |  | 1 |
| [`upgrade_storage_repeating_intro`](./Progression_Unlocks.md#context-upgrade_storage_repeating_intro) | Block |  | 1 |
| [`upgrade_storage_repeating_normal`](./Progression_Unlocks.md#context-upgrade_storage_repeating_normal) | Block |  | 1 |

</details>

---

### Context: `popup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/266) |
| :--- | :--- | :--- | :--- |
| [`prompt`](./Enums.md#enum-prompt) | Enum/String |  | 266 |
| `immediate` | Boolean |  | 221 |
| [`frame`](./Enums.md#enum-frame) | Enum/String |  | 159 |

</details>

---

### Context: `tracy_special_item`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`tracy_blankcollar1`](./Progression_Unlocks.md#context-tracy_blankcollar1), [`tracy_blankcollar2`](./Progression_Unlocks.md#context-tracy_blankcollar2), [`tracy_blankcollar3`](./Progression_Unlocks.md#context-tracy_blankcollar3), [`tracy_foodstorage1`](./Progression_Unlocks.md#context-tracy_foodstorage1), [`tracy_foodstorage10`](./Progression_Unlocks.md#context-tracy_foodstorage10), [`tracy_foodstorage2`](./Progression_Unlocks.md#context-tracy_foodstorage2), [`tracy_foodstorage3`](./Progression_Unlocks.md#context-tracy_foodstorage3), [`tracy_foodstorage4`](./Progression_Unlocks.md#context-tracy_foodstorage4), [`tracy_foodstorage5`](./Progression_Unlocks.md#context-tracy_foodstorage5), [`tracy_foodstorage6`](./Progression_Unlocks.md#context-tracy_foodstorage6), [`tracy_foodstorage7`](./Progression_Unlocks.md#context-tracy_foodstorage7), [`tracy_foodstorage8`](./Progression_Unlocks.md#context-tracy_foodstorage8), [`tracy_foodstorage9`](./Progression_Unlocks.md#context-tracy_foodstorage9), [`tracy_idol1`](./Progression_Unlocks.md#context-tracy_idol1), [`tracy_idol2`](./Progression_Unlocks.md#context-tracy_idol2), [`tracy_idol3`](./Progression_Unlocks.md#context-tracy_idol3), [`tracy_idol4`](./Progression_Unlocks.md#context-tracy_idol4), [`tracy_idol5`](./Progression_Unlocks.md#context-tracy_idol5), [`tracy_idol6`](./Progression_Unlocks.md#context-tracy_idol6), [`tracy_idol7`](./Progression_Unlocks.md#context-tracy_idol7), [`tracy_max_intro`](./Progression_Unlocks.md#context-tracy_max_intro), [`tracy_max_repeating`](./Progression_Unlocks.md#context-tracy_max_repeating)

| Property Key | Type | Definition | Count (X/22) |
| :--- | :--- | :--- | :--- |
| `cost` | Number |  | 22 |
| [`type`](./Enums.md#enum-type) | Enum/String |  | 22 |

</details>

---

### Context: `house_upgrade_largehouse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum/String |  | 2 |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `house_upgrade_mediumhouse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum/String |  | 2 |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `beanies_quests_intro`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `beanies_quests_repeat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`generate_beanies_quest`](./Enums.md#enum-generate_beanies_quest) | Enum/String |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `destinations`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `boneyard` | Number |  | 1 |
| `caves` | Number |  | 1 |
| `core` | Number |  | 1 |
| `dimensionx` | Number |  | 1 |
| `endoftime` | Number |  | 1 |
| `jurassic` | Number |  | 1 |
| `meatworld` | Number |  | 1 |
| `moon` | Number |  | 1 |
| `theend` | Number |  | 1 |

</details>

---

### Context: `frank_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum/String |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `frank_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`gift_item_from_pool`](./Enums.md#enum-gift_item_from_pool) | Enum/String |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `house_upgrade_4throom`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `house_upgrade_attic`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`house_upgrade`](./Enums.md#enum-house_upgrade) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `jack_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `rep_reward_count` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `jack_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `rep_reward_count` | Number |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `jack_shopupgrade1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `jack_shopupgrade2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `jack_shopupgrade3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `jack_shopupgrade4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `organ_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum/String |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `organ_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum/String |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `organ_unlock`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `organ_upgrade1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `organ_upgrade2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `organ_upgrade3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `organ_upgrade4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `organ_upgrade5`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `organ_upgrade6`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |

</details>

---

### Context: `prereqs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`core`](./Enums.md#enum-core) | Enum/String |  | 1 |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum/String |  | 1 |
| [`endoftime`](./Enums.md#enum-endoftime) | Enum/String |  | 1 |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum/String |  | 1 |
| [`moon`](./Enums.md#enum-moon) | Enum/String |  | 1 |
| [`theend`](./Enums.md#enum-theend) | Enum/String |  | 1 |

</details>

---

### Context: `steven_milliontrashed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |

</details>

---

### Context: `tink_aggression`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | Enum/String |  | 1 |

</details>

---

### Context: `tink_basestats`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | Enum/String |  | 1 |

</details>

---

### Context: `tink_inbreeding`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | Enum/String |  | 1 |

</details>

---

### Context: `tink_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `coins` | Number |  | 1 |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `tink_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `coins` | Number |  | 1 |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `tink_prettybow`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`gift_item`](./Enums.md#enum-gift_item) | Enum/String |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `tink_relationships`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | Enum/String |  | 1 |

</details>

---

### Context: `tink_sexuality`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | Enum/String |  | 1 |

</details>

---

### Context: `tink_tags`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`set_savefile_flag`](./Enums.md#enum-set_savefile_flag) | Enum/String |  | 1 |

</details>

---

### Context: `tracy_blankcollar1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_blankcollar2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_blankcollar3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage10`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage5`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage6`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage7`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage8`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_foodstorage9`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_idol1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_idol2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_idol3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_idol4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_idol5`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_idol6`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_idol7`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `shop_level_up` | Number |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `tracy_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| `required_age` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item) | Block |  | 1 |

</details>

---

### Context: `upgrade_storage_1`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `storage_expansion` | Number |  | 1 |

</details>

---

### Context: `upgrade_storage_2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `storage_expansion` | Number |  | 1 |

</details>

---

### Context: `upgrade_storage_3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `storage_expansion` | Number |  | 1 |

</details>

---

### Context: `upgrade_storage_4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `storage_expansion` | Number |  | 1 |

</details>

---

### Context: `upgrade_storage_5`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `storage_expansion` | Number |  | 1 |

</details>

---

### Context: `upgrade_storage_6`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `storage_expansion` | Number |  | 1 |

</details>

---

### Context: `upgrade_storage_7`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `reward_text` | String |  | 1 |
| `storage_expansion` | Number |  | 1 |

</details>

---

### Context: `upgrade_storage_repeating_crazy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `rep_reward_count` | Number |  | 1 |
| `repeat` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `required_difficulty` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `upgrade_storage_repeating_hard`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `rep_reward_count` | Number |  | 1 |
| `repeat` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `required_difficulty` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `upgrade_storage_repeating_impossible`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `rep_reward_count` | Number |  | 1 |
| [`repeat`](./Enums.md#enum-repeat) | Enum/String |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `required_difficulty` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `upgrade_storage_repeating_intro`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `rep_reward_count` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `required_difficulty` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

### Context: `upgrade_storage_repeating_normal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `favor` | Number |  | 1 |
| [`level_display`](./Enums.md#enum-level_display) | Enum/String |  | 1 |
| `rep_reward_count` | Number |  | 1 |
| `repeat` | Number |  | 1 |
| `required_act` | Number |  | 1 |
| `required_chapter` | Number |  | 1 |
| `required_difficulty` | Number |  | 1 |
| `reward_text` | String |  | 1 |

</details>

---

