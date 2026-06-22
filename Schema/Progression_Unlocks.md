# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Progression Unlocks

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `popup` | [`Block`](./Progression_Unlocks.md#context-popup) | `{ ... }` |  |
| `complete_chapter_with_class` | [`Array`](./Arrays.md#array-complete_chapter_with_class) | `[ caves Mage ], [ caves Hunter ], [ caves Fighter ]` |  |
| `unlock_item_immediate` | [`Enum/String`](./Enums.md#enum-unlock_item_immediate) | `InfinityArrow, StaffOfFlame, BattleAxe` |  |
| `trigger_npc_sequence` | [`Enum/String`](./Enums.md#enum-trigger_npc_sequence) | `class_unlock_thief, class_unlock_medic, class_unlock_necromancer` |  |
| `beat_house_boss` | [`Enum/String`](./Enums.md#enum-beat_house_boss) | `guillotina_2, pyrophina, guillotina_1` |  |
| `complete_chapter` | [`Enum/String`](./Enums.md#enum-complete_chapter) | `alley, boneyard, sewers` |  |
| `required_difficulty` | Number | `2, 1, 3` |  |
| `repeat` | Number | `6, 1, 3` |  |
| `beat_chapter_boss` | [`Enum/String`](./Enums.md#enum-beat_chapter_boss) | `alley, junkyard, sewers` |  |
| `unlock_ability` | [`Enum/String`](./Enums.md#enum-unlock_ability) | `Pawbreaker, HyperBeam, BallOfSpiders` |  |
| `unlock_passive` | [`Enum/String`](./Enums.md#enum-unlock_passive) | `ThrillOfTheHunt, DualWield, EnergyStorm` |  |
| `unlock_song` | [`Enum/String`](./Enums.md#enum-unlock_song) | `chumbucket_kitty, eatin_rats, flush` |  |
| `set_mapgen_flag` | [`Enum/String`](./Enums.md#enum-set_mapgen_flag) | `SewersUnlocked, HardPathUnlocked, JunkyardUnlocked` |  |
| `complete_checklist_with_class` | [`Enum/String`](./Enums.md#enum-complete_checklist_with_class) | `Mage, Fighter, Hunter` |  |
| `unlock_quest_item` | [`Enum/String`](./Enums.md#enum-unlock_quest_item) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `repeatable` | Boolean | `true` |  |
| `trigger_house_boss` | [`Enum/String`](./Enums.md#enum-trigger_house_boss) | `guillotina_2, guillotina_3, guillotina_1` |  |
| `complete_act_difficulty` | [`Array`](./Arrays.md#array-complete_act_difficulty) | `[ 1 2 ], [ 1 1 ], [ 1 0 ]` |  |
| `complete_item_quest` | [`Enum/String`](./Enums.md#enum-complete_item_quest) | `BlackShard, ScaldingOrb, JarOfRadiation` |  |
| `unlock_act_difficulty` | [`Array`](./Arrays.md#array-unlock_act_difficulty) | `[ 1 3 ], [ 1 1 ], [ 1 2 ]` |  |
| `queue_cutscene_immediate` | [`Enum/String`](./Enums.md#enum-queue_cutscene_immediate) | `desert_intro, dybbuk, caves_intro` |  |
| `reset_npc_sequence` | [`Enum/String`](./Enums.md#enum-reset_npc_sequence) | `beanies_bombquest_fail_jarofradiation, beanies_bombquest_2, beanies_bombquest_3` |  |
| `preempt_npc_sequence` | [`Enum/String`](./Enums.md#enum-preempt_npc_sequence) | `beanies_bombquest_2, beanies_bombquest_3, beanies_bombquest_amnesia` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `PlotFlag_Beanies_Homeless, RestlessDeadUnlocked, PlotFlag_FrankBeanies` |  |
| `unlock_boss` | [`Enum/String`](./Enums.md#enum-unlock_boss) | `gambit, jestercat, queenhippo` |  |
| `fail_item_quest` | [`Enum/String`](./Enums.md#enum-fail_item_quest) | `JarOfRadiatedBlood, JarOfRadiation, JarOfChaos` |  |
| `fully_complete_difficulty` | Number | `1, 2, 0` |  |
| `post_combat_cutscene` | [`Enum/String`](./Enums.md#enum-post_combat_cutscene) | `obelisk1_moon, obelisk1_core, obelisk2_moon` |  |
| `trigger_npc_sequence_tomorrow` | [`Enum/String`](./Enums.md#enum-trigger_npc_sequence_tomorrow) | `frank_caves_intro, organ_boneyard_intro, butch_boneyard_intro` |  |
| `unlock_npc_tomorrow` | [`Enum/String`](./Enums.md#enum-unlock_npc_tomorrow) | `tracy, beanies, jack` |  |
| `visit_chapter` | [`Enum/String`](./Enums.md#enum-visit_chapter) | `future, dimensionx, theend` |  |
| `complete_chapters` | [`Array`](./Arrays.md#array-complete_chapters) | `[ caves boneyard ], [ core moon ]` |  |
| `requires_monoclass_run` | Boolean | `true` |  |
| `requires_unlocked_npc` | [`Enum/String`](./Enums.md#enum-requires_unlocked_npc) | `tracy, frank, jack` |  |
| `complete_adventure` | [`Enum/String`](./Enums.md#enum-complete_adventure) | `anywhere` |  |
| `require_beat_house_boss` | [`Enum/String`](./Enums.md#enum-require_beat_house_boss) | `zaratana, pyrophina` |  |
| `require_mapgen_flag` | [`Enum/String`](./Enums.md#enum-require_mapgen_flag) | `CoreObeliskUnlocked, MoonObeliskUnlocked` |  |
| `surviving_kaiju` | [`Enum/String`](./Enums.md#enum-surviving_kaiju) | `zaratana, pyrophina` |  |
| `unlock_levelgroup` | [`Enum/String`](./Enums.md#enum-unlock_levelgroup) | `bigsharklevels` |  |
| `beanies_quests_intro` | [`Block`](./Progression_Unlocks.md#context-beanies_quests_intro) | `{ ... }` |  |
| `beanies_quests_repeat` | [`Block`](./Progression_Unlocks.md#context-beanies_quests_repeat) | `{ ... }` |  |
| `destinations` | [`Block`](./Progression_Unlocks.md#context-destinations) | `{ ... }` |  |
| `fail_adventure` | [`Enum/String`](./Enums.md#enum-fail_adventure) | `anywhere` |  |
| `finish_quest` | [`Enum/String`](./Enums.md#enum-finish_quest) | `JarOfChaos` |  |
| `frank_max_intro` | [`Block`](./Progression_Unlocks.md#context-frank_max_intro) | `{ ... }` |  |
| `frank_max_repeating` | [`Block`](./Progression_Unlocks.md#context-frank_max_repeating) | `{ ... }` |  |
| `house_upgrade_4throom` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_4throom) | `{ ... }` |  |
| `house_upgrade_attic` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_attic) | `{ ... }` |  |
| `house_upgrade_largehouse` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_largehouse) | `{ ... }` |  |
| `house_upgrade_mediumhouse` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_mediumhouse) | `{ ... }` |  |
| `increment_savefile_counter` | [`Enum/String`](./Enums.md#enum-increment_savefile_counter) | `GameStat_CountNukeQuestCompletions` |  |
| `intro` | [`Array`](./Arrays.md#array-intro) | `[ PersuasionDevice ]` |  |
| `jack_max_intro` | [`Block`](./Progression_Unlocks.md#context-jack_max_intro) | `{ ... }` |  |
| `jack_max_repeating` | [`Block`](./Progression_Unlocks.md#context-jack_max_repeating) | `{ ... }` |  |
| `jack_shopupgrade1` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade1) | `{ ... }` |  |
| `jack_shopupgrade2` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade2) | `{ ... }` |  |
| `jack_shopupgrade3` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade3) | `{ ... }` |  |
| `jack_shopupgrade4` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade4) | `{ ... }` |  |
| `main_pool` | [`Array`](./Arrays.md#array-main_pool) | `[ ChaosDevice MagicMirror MeStone AngryFace FartFace Spid...` |  |
| `organ_max_intro` | [`Block`](./Progression_Unlocks.md#context-organ_max_intro) | `{ ... }` |  |
| `organ_max_repeating` | [`Block`](./Progression_Unlocks.md#context-organ_max_repeating) | `{ ... }` |  |
| `organ_unlock` | [`Block`](./Progression_Unlocks.md#context-organ_unlock) | `{ ... }` |  |
| `organ_upgrade1` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade1) | `{ ... }` |  |
| `organ_upgrade2` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade2) | `{ ... }` |  |
| `organ_upgrade3` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade3) | `{ ... }` |  |
| `organ_upgrade4` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade4) | `{ ... }` |  |
| `organ_upgrade5` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade5) | `{ ... }` |  |
| `organ_upgrade6` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade6) | `{ ... }` |  |
| `prereqs` | [`Block`](./Progression_Unlocks.md#context-prereqs) | `{ ... }` |  |
| `requires_hard_path` | Boolean | `true` |  |
| `reset_unlock` | [`Enum/String`](./Enums.md#enum-reset_unlock) | `nuke_quest_begin` |  |
| `steven_milliontrashed` | [`Block`](./Progression_Unlocks.md#context-steven_milliontrashed) | `{ ... }` |  |
| `tink_aggression` | [`Block`](./Progression_Unlocks.md#context-tink_aggression) | `{ ... }` |  |
| `tink_basestats` | [`Block`](./Progression_Unlocks.md#context-tink_basestats) | `{ ... }` |  |
| `tink_inbreeding` | [`Block`](./Progression_Unlocks.md#context-tink_inbreeding) | `{ ... }` |  |
| `tink_max_intro` | [`Block`](./Progression_Unlocks.md#context-tink_max_intro) | `{ ... }` |  |
| `tink_max_repeating` | [`Block`](./Progression_Unlocks.md#context-tink_max_repeating) | `{ ... }` |  |
| `tink_prettybow` | [`Block`](./Progression_Unlocks.md#context-tink_prettybow) | `{ ... }` |  |
| `tink_relationships` | [`Block`](./Progression_Unlocks.md#context-tink_relationships) | `{ ... }` |  |
| `tink_sexuality` | [`Block`](./Progression_Unlocks.md#context-tink_sexuality) | `{ ... }` |  |
| `tink_tags` | [`Block`](./Progression_Unlocks.md#context-tink_tags) | `{ ... }` |  |
| `tracy_blankcollar1` | [`Block`](./Progression_Unlocks.md#context-tracy_blankcollar1) | `{ ... }` |  |
| `tracy_blankcollar2` | [`Block`](./Progression_Unlocks.md#context-tracy_blankcollar2) | `{ ... }` |  |
| `tracy_blankcollar3` | [`Block`](./Progression_Unlocks.md#context-tracy_blankcollar3) | `{ ... }` |  |
| `tracy_foodstorage1` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage1) | `{ ... }` |  |
| `tracy_foodstorage10` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage10) | `{ ... }` |  |
| `tracy_foodstorage2` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage2) | `{ ... }` |  |
| `tracy_foodstorage3` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage3) | `{ ... }` |  |
| `tracy_foodstorage4` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage4) | `{ ... }` |  |
| `tracy_foodstorage5` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage5) | `{ ... }` |  |
| `tracy_foodstorage6` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage6) | `{ ... }` |  |
| `tracy_foodstorage7` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage7) | `{ ... }` |  |
| `tracy_foodstorage8` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage8) | `{ ... }` |  |
| `tracy_foodstorage9` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage9) | `{ ... }` |  |
| `tracy_idol1` | [`Block`](./Progression_Unlocks.md#context-tracy_idol1) | `{ ... }` |  |
| `tracy_idol2` | [`Block`](./Progression_Unlocks.md#context-tracy_idol2) | `{ ... }` |  |
| `tracy_idol3` | [`Block`](./Progression_Unlocks.md#context-tracy_idol3) | `{ ... }` |  |
| `tracy_idol4` | [`Block`](./Progression_Unlocks.md#context-tracy_idol4) | `{ ... }` |  |
| `tracy_idol5` | [`Block`](./Progression_Unlocks.md#context-tracy_idol5) | `{ ... }` |  |
| `tracy_idol6` | [`Block`](./Progression_Unlocks.md#context-tracy_idol6) | `{ ... }` |  |
| `tracy_idol7` | [`Block`](./Progression_Unlocks.md#context-tracy_idol7) | `{ ... }` |  |
| `tracy_max_intro` | [`Block`](./Progression_Unlocks.md#context-tracy_max_intro) | `{ ... }` |  |
| `tracy_max_repeating` | [`Block`](./Progression_Unlocks.md#context-tracy_max_repeating) | `{ ... }` |  |
| `unlock_item` | [`Enum/String`](./Enums.md#enum-unlock_item) | `MomsKnife` |  |
| `upgrade_storage_1` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_1) | `{ ... }` |  |
| `upgrade_storage_2` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_2) | `{ ... }` |  |
| `upgrade_storage_3` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_3) | `{ ... }` |  |
| `upgrade_storage_4` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_4) | `{ ... }` |  |
| `upgrade_storage_5` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_5) | `{ ... }` |  |
| `upgrade_storage_6` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_6) | `{ ... }` |  |
| `upgrade_storage_7` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_7) | `{ ... }` |  |
| `upgrade_storage_repeating_crazy` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_crazy) | `{ ... }` |  |
| `upgrade_storage_repeating_hard` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_hard) | `{ ... }` |  |
| `upgrade_storage_repeating_impossible` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_impossible) | `{ ... }` |  |
| `upgrade_storage_repeating_intro` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_intro) | `{ ... }` |  |
| `upgrade_storage_repeating_normal` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_normal) | `{ ... }` |  |

</details>

---

### Context: `popup`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | [`Enum/String`](./Enums.md#enum-prompt) | `AREA_UNLOCK_JUNKYARD, AREA_UNLOCK_BUNKER, AREA_UNLOCK_SEWERS` |  |
| `immediate` | Boolean | `false, true` |  |
| `frame` | [`Enum/String`](./Enums.md#enum-frame) | `UnlockArea_Junkyard, UnlockArea_Sewers, UnlockArea_Bunker` |  |

</details>

---

### Context: `tracy_special_item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`tracy_blankcollar1`](./Progression_Unlocks.md#context-tracy_blankcollar1), [`tracy_blankcollar2`](./Progression_Unlocks.md#context-tracy_blankcollar2), [`tracy_blankcollar3`](./Progression_Unlocks.md#context-tracy_blankcollar3), [`tracy_foodstorage1`](./Progression_Unlocks.md#context-tracy_foodstorage1), [`tracy_foodstorage10`](./Progression_Unlocks.md#context-tracy_foodstorage10), [`tracy_foodstorage2`](./Progression_Unlocks.md#context-tracy_foodstorage2), [`tracy_foodstorage3`](./Progression_Unlocks.md#context-tracy_foodstorage3), [`tracy_foodstorage4`](./Progression_Unlocks.md#context-tracy_foodstorage4), [`tracy_foodstorage5`](./Progression_Unlocks.md#context-tracy_foodstorage5), [`tracy_foodstorage6`](./Progression_Unlocks.md#context-tracy_foodstorage6), [`tracy_foodstorage7`](./Progression_Unlocks.md#context-tracy_foodstorage7), [`tracy_foodstorage8`](./Progression_Unlocks.md#context-tracy_foodstorage8), [`tracy_foodstorage9`](./Progression_Unlocks.md#context-tracy_foodstorage9), [`tracy_idol1`](./Progression_Unlocks.md#context-tracy_idol1), [`tracy_idol2`](./Progression_Unlocks.md#context-tracy_idol2), [`tracy_idol3`](./Progression_Unlocks.md#context-tracy_idol3), [`tracy_idol4`](./Progression_Unlocks.md#context-tracy_idol4), [`tracy_idol5`](./Progression_Unlocks.md#context-tracy_idol5), [`tracy_idol6`](./Progression_Unlocks.md#context-tracy_idol6), [`tracy_idol7`](./Progression_Unlocks.md#context-tracy_idol7), [`tracy_max_intro`](./Progression_Unlocks.md#context-tracy_max_intro), [`tracy_max_repeating`](./Progression_Unlocks.md#context-tracy_max_repeating)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cost` | Number | `100, 150, 10` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `blankcollar, special_foodbox, random_unique_idol` |  |

</details>

---

### Context: `destinations`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `boneyard` | Number | `200` |  |
| `caves` | Number | `200` |  |
| `core` | Number | `300` |  |
| `dimensionx` | Number | `400` |  |
| `endoftime` | Number | `500` |  |
| `jurassic` | Number | `400` |  |
| `meatworld` | Number | `300` |  |
| `moon` | Number | `300` |  |
| `theend` | Number | `400` |  |

</details>

---

### Context: `upgrade_storage_repeating_crazy`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | Number | `25` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_hard`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | Number | `23` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_impossible`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_normal`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | Number | `20` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `0` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `0` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `prereqs`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `core` | [`Enum/String`](./Enums.md#enum-core) | `mapflag_IceAgeUnlocked` |  |
| `dimensionx` | [`Enum/String`](./Enums.md#enum-dimensionx) | `mapflag_IceAgeUnlocked` |  |
| `endoftime` | [`Enum/String`](./Enums.md#enum-endoftime) | `endoftime` |  |
| `jurassic` | [`Enum/String`](./Enums.md#enum-jurassic) | `endoftime` |  |
| `moon` | [`Enum/String`](./Enums.md#enum-moon) | `mapflag_IceAgeUnlocked` |  |
| `theend` | [`Enum/String`](./Enums.md#enum-theend) | `endoftime` |  |

</details>

---

### Context: `tracy_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_RARE"` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `beanies_quests_repeat`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `5` |  |
| `generate_beanies_quest` | [`Enum/String`](./Enums.md#enum-generate_beanies_quest) | `main_pool` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_BEANIES_REPEAT"` |  |

</details>

---

### Context: `frank_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item_from_pool` | [`Enum/String`](./Enums.md#enum-gift_item_from_pool) | `parasites` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_FRANK_PARASITE"` |  |

</details>

---

### Context: `jack_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_JACK_MAX"` |  |

</details>

---

### Context: `organ_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item` | [`Enum/String`](./Enums.md#enum-gift_item) | `disorder_needle` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_GRINDER_SYRINGE"` |  |

</details>

---

### Context: `tink_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | Number | `25` |  |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_TINK_MAX"` |  |

</details>

---

### Context: `tracy_blankcollar1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_COLLAR"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_blankcollar2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_COLLAR"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_blankcollar3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_COLLAR"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage10`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage7`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage8`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage9`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol7`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_RARE"` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `upgrade_storage_1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `required_act` | Number | `0` |  |
| `required_chapter` | Number | `0` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_act` | Number | `1` |  |
| `required_chapter` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_act` | Number | `1` |  |
| `required_chapter` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `15` |  |
| `required_act` | Number | `2` |  |
| `required_chapter` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `15` |  |
| `required_act` | Number | `2` |  |
| `required_chapter` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `20` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_7`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `20` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `frank_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item_from_pool` | [`Enum/String`](./Enums.md#enum-gift_item_from_pool) | `parasites` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `reward_text` | String | `"FAVOR_FRANK_PARASITE"` |  |

</details>

---

### Context: `house_upgrade_largehouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `LargeHouse_Floor2Large, LargeHouse` |  |
| `favor` | Number | `50` |  |
| `reward_text` | String | `"FAVOR_FRANK_ROOM"` |  |

</details>

---

### Context: `house_upgrade_mediumhouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `MediumHouse, MediumHouse_SmallRoom` |  |
| `favor` | Number | `25` |  |
| `reward_text` | String | `"FAVOR_FRANK_ROOM"` |  |

</details>

---

### Context: `jack_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_JACK_MAX"` |  |

</details>

---

### Context: `organ_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item` | [`Enum/String`](./Enums.md#enum-gift_item) | `disorder_needle` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `reward_text` | String | `"FAVOR_GRINDER_SYRINGE"` |  |

</details>

---

### Context: `tink_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | Number | `25` |  |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `reward_text` | String | `"FAVOR_TINK_MAX"` |  |

</details>

---

### Context: `beanies_quests_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `generate_beanies_quest` | [`Enum/String`](./Enums.md#enum-generate_beanies_quest) | `intro` |  |
| `reward_text` | String | `"FAVOR_BEANIES_INTRO"` |  |

</details>

---

### Context: `house_upgrade_4throom`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `100` |  |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `LargeHouse_Floor2Small` |  |
| `reward_text` | String | `"FAVOR_FRANK_ROOM"` |  |

</details>

---

### Context: `house_upgrade_attic`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `SmallHouse_Attic` |  |
| `reward_text` | String | `"FAVOR_FRANK_ATTIC"` |  |

</details>

---

### Context: `jack_shopupgrade1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `jack_shopupgrade2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `jack_shopupgrade3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `20` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `jack_shopupgrade4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `30` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_unlock`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `25` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `50` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `75` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `100` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `150` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `steven_milliontrashed`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1000000` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |

</details>

---

### Context: `tink_aggression`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_AGRESSION"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_aggression` |  |

</details>

---

### Context: `tink_basestats`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_BASESTATS"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_basestats` |  |

</details>

---

### Context: `tink_inbreeding`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_INBREEDING"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_inbreeding` |  |

</details>

---

### Context: `tink_prettybow`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `gift_item` | [`Enum/String`](./Enums.md#enum-gift_item) | `TinksBow` |  |
| `reward_text` | String | `"FAVOR_TINK_BOW"` |  |

</details>

---

### Context: `tink_relationships`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_RELATIONSHIPS"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_relationships` |  |

</details>

---

### Context: `tink_sexuality`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_SEXUALITY"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_sexuality` |  |

</details>

---

### Context: `tink_tags`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_TAGS"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_tags` |  |

</details>

---

