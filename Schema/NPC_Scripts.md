# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## NPC Scripts


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`intro`](Events_and_Encounters.md#object-intro) | Object | Examples: `{ ... }` | 239 ||
| [`tooltip`](./NPC_Scripts.md#context-tooltip) | Enum | Examples: `{ ... }` | 161 ||
| [`states`](Miscellaneous.md#object-states) | Object | Examples: `{ ... }` | 12 ||
| [`transitions`](Miscellaneous.md#object-transitions) | Object | Examples: `{ ... }` | 12 ||
| [`unprompted`](Miscellaneous.md#object-unprompted) | Object | Examples: `{ ... }` | 8 ||
| [`also`](Miscellaneous.md#object-also) | Object | Examples: `{ ... }` | 8 ||
| [`unknown`](Miscellaneous.md#object-unknown) | Object | Examples: `{ ... }` | 8 ||
| [`hide_text`](Miscellaneous.md#object-hide_text) | Object | Examples: `{ ... }` | 4 ||
| [`purchase_item`](Miscellaneous.md#object-purchase_item) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_a`](Miscellaneous.md#object-unprompted_a) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_b`](Miscellaneous.md#object-unprompted_b) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_c`](Miscellaneous.md#object-unprompted_c) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_d`](Miscellaneous.md#object-unprompted_d) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_e`](Miscellaneous.md#object-unprompted_e) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_f`](Miscellaneous.md#object-unprompted_f) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_g`](Miscellaneous.md#object-unprompted_g) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_h`](Miscellaneous.md#object-unprompted_h) | Object | Examples: `{ ... }` | 4 ||
| [`unprompted_i`](Miscellaneous.md#object-unprompted_i) | Object | Examples: `{ ... }` | 4 ||
| [`cant_afford`](Miscellaneous.md#object-cant_afford) | Object | Examples: `{ ... }` | 3 ||
| [`forward_to_tips`](Miscellaneous.md#object-forward_to_tips) | Object | Examples: `{ ... }` | 3 ||
| [`out_of_stock`](Miscellaneous.md#object-out_of_stock) | Object | Examples: `{ ... }` | 3 ||
| [`beanies_quests_intro`](Miscellaneous.md#object-beanies_quests_intro) | Object | Examples: `{ ... }` | 2 ||
| [`beanies_quests_repeat`](Miscellaneous.md#object-beanies_quests_repeat) | Object | Examples: `{ ... }` | 2 ||
| [`frank_max_intro`](Miscellaneous.md#object-frank_max_intro) | Object | Examples: `{ ... }` | 2 ||
| [`frank_max_repeating`](Miscellaneous.md#object-frank_max_repeating) | Object | Examples: `{ ... }` | 2 ||
| [`house_upgrade_4throom`](Miscellaneous.md#object-house_upgrade_4throom) | Object | Examples: `{ ... }` | 2 ||
| [`house_upgrade_attic`](Miscellaneous.md#object-house_upgrade_attic) | Object | Examples: `{ ... }` | 2 ||
| [`house_upgrade_largehouse`](Miscellaneous.md#object-house_upgrade_largehouse) | Object | Examples: `{ ... }` | 2 ||
| [`house_upgrade_mediumhouse`](Miscellaneous.md#object-house_upgrade_mediumhouse) | Object | Examples: `{ ... }` | 2 ||
| [`jack_max_intro`](Miscellaneous.md#object-jack_max_intro) | Object | Examples: `{ ... }` | 2 ||
| [`jack_max_repeating`](Miscellaneous.md#object-jack_max_repeating) | Object | Examples: `{ ... }` | 2 ||
| [`jack_shopupgrade1`](Miscellaneous.md#object-jack_shopupgrade1) | Object | Examples: `{ ... }` | 2 ||
| [`jack_shopupgrade2`](Miscellaneous.md#object-jack_shopupgrade2) | Object | Examples: `{ ... }` | 2 ||
| [`jack_shopupgrade3`](Miscellaneous.md#object-jack_shopupgrade3) | Object | Examples: `{ ... }` | 2 ||
| [`jack_shopupgrade4`](Miscellaneous.md#object-jack_shopupgrade4) | Object | Examples: `{ ... }` | 2 ||
| [`organ_max_intro`](Miscellaneous.md#object-organ_max_intro) | Object | Examples: `{ ... }` | 2 ||
| [`organ_max_repeating`](Miscellaneous.md#object-organ_max_repeating) | Object | Examples: `{ ... }` | 2 ||
| [`organ_unlock`](Miscellaneous.md#object-organ_unlock) | Object | Examples: `{ ... }` | 2 ||
| [`organ_upgrade1`](Miscellaneous.md#object-organ_upgrade1) | Object | Examples: `{ ... }` | 2 ||
| [`organ_upgrade2`](Miscellaneous.md#object-organ_upgrade2) | Object | Examples: `{ ... }` | 2 ||
| [`organ_upgrade3`](Miscellaneous.md#object-organ_upgrade3) | Object | Examples: `{ ... }` | 2 ||
| [`organ_upgrade4`](Miscellaneous.md#object-organ_upgrade4) | Object | Examples: `{ ... }` | 2 ||
| [`organ_upgrade5`](Miscellaneous.md#object-organ_upgrade5) | Object | Examples: `{ ... }` | 2 ||
| [`organ_upgrade6`](Miscellaneous.md#object-organ_upgrade6) | Object | Examples: `{ ... }` | 2 ||
| [`steven_milliontrashed`](Miscellaneous.md#object-steven_milliontrashed) | Object | Examples: `{ ... }` | 2 ||
| [`tink_aggression`](Miscellaneous.md#object-tink_aggression) | Object | Examples: `{ ... }` | 2 ||
| [`tink_basestats`](Miscellaneous.md#object-tink_basestats) | Object | Examples: `{ ... }` | 2 ||
| [`tink_inbreeding`](Miscellaneous.md#object-tink_inbreeding) | Object | Examples: `{ ... }` | 2 ||
| [`tink_max_intro`](Miscellaneous.md#object-tink_max_intro) | Object | Examples: `{ ... }` | 2 ||
| [`tink_max_repeating`](Miscellaneous.md#object-tink_max_repeating) | Object | Examples: `{ ... }` | 2 ||
| [`tink_prettybow`](Miscellaneous.md#object-tink_prettybow) | Object | Examples: `{ ... }` | 2 ||
| [`tink_relationships`](Miscellaneous.md#object-tink_relationships) | Object | Examples: `{ ... }` | 2 ||
| [`tink_sexuality`](Miscellaneous.md#object-tink_sexuality) | Object | Examples: `{ ... }` | 2 ||
| [`tink_tags`](Miscellaneous.md#object-tink_tags) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_blankcollar1`](Miscellaneous.md#object-tracy_blankcollar1) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_blankcollar2`](Miscellaneous.md#object-tracy_blankcollar2) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_blankcollar3`](Miscellaneous.md#object-tracy_blankcollar3) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage1`](Miscellaneous.md#object-tracy_foodstorage1) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage10`](Miscellaneous.md#object-tracy_foodstorage10) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage2`](Miscellaneous.md#object-tracy_foodstorage2) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage3`](Miscellaneous.md#object-tracy_foodstorage3) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage4`](Miscellaneous.md#object-tracy_foodstorage4) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage5`](Miscellaneous.md#object-tracy_foodstorage5) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage6`](Miscellaneous.md#object-tracy_foodstorage6) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage7`](Miscellaneous.md#object-tracy_foodstorage7) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage8`](Miscellaneous.md#object-tracy_foodstorage8) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_foodstorage9`](Miscellaneous.md#object-tracy_foodstorage9) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_idol1`](Miscellaneous.md#object-tracy_idol1) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_idol2`](Miscellaneous.md#object-tracy_idol2) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_idol3`](Miscellaneous.md#object-tracy_idol3) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_idol4`](Miscellaneous.md#object-tracy_idol4) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_idol5`](Miscellaneous.md#object-tracy_idol5) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_idol6`](Miscellaneous.md#object-tracy_idol6) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_idol7`](Miscellaneous.md#object-tracy_idol7) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_max_intro`](Miscellaneous.md#object-tracy_max_intro) | Object | Examples: `{ ... }` | 2 ||
| [`tracy_max_repeating`](Miscellaneous.md#object-tracy_max_repeating) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_1`](Miscellaneous.md#object-upgrade_storage_1) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_2`](Miscellaneous.md#object-upgrade_storage_2) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_3`](Miscellaneous.md#object-upgrade_storage_3) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_4`](Miscellaneous.md#object-upgrade_storage_4) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_5`](Miscellaneous.md#object-upgrade_storage_5) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_6`](Miscellaneous.md#object-upgrade_storage_6) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_7`](Miscellaneous.md#object-upgrade_storage_7) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_repeating_crazy`](Miscellaneous.md#object-upgrade_storage_repeating_crazy) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_repeating_hard`](Miscellaneous.md#object-upgrade_storage_repeating_hard) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_repeating_impossible`](Miscellaneous.md#object-upgrade_storage_repeating_impossible) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_repeating_intro`](Miscellaneous.md#object-upgrade_storage_repeating_intro) | Object | Examples: `{ ... }` | 2 ||
| [`upgrade_storage_repeating_normal`](Miscellaneous.md#object-upgrade_storage_repeating_normal) | Object | Examples: `{ ... }` | 2 ||
| [`beanies_bombquest_2`](Miscellaneous.md#object-beanies_bombquest_2) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_bombquest_3`](Miscellaneous.md#object-beanies_bombquest_3) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_bombquest_fail_jarofblood`](Miscellaneous.md#object-beanies_bombquest_fail_jarofblood) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_bombquest_fail_jarofchaos`](Miscellaneous.md#object-beanies_bombquest_fail_jarofchaos) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_bombquest_amnesia`](Miscellaneous.md#object-beanies_bombquest_amnesia) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_bombquest_begin`](Miscellaneous.md#object-beanies_bombquest_begin) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_bombquest_fail_jarofradiation`](Miscellaneous.md#object-beanies_bombquest_fail_jarofradiation) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_bombquest_fail_nuke`](Miscellaneous.md#object-beanies_bombquest_fail_nuke) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_future_intro`](Miscellaneous.md#object-beanies_future_intro) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_jurassic_intro`](Miscellaneous.md#object-beanies_jurassic_intro) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_lab_intro`](Miscellaneous.md#object-beanies_lab_intro) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_theend_intro`](Miscellaneous.md#object-beanies_theend_intro) | Object | Examples: `{ ... }` | 1 ||
| [`butch_boneyard_intro`](Miscellaneous.md#object-butch_boneyard_intro) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_jester`](Miscellaneous.md#object-class_unlock_jester) | Object | Examples: `{ ... }` | 1 ||
| [`frank_caves_intro`](Miscellaneous.md#object-frank_caves_intro) | Object | Examples: `{ ... }` | 1 ||
| [`frank_ending`](Miscellaneous.md#object-frank_ending) | Object | Examples: `{ ... }` | 1 ||
| [`jack_desert_intro`](Miscellaneous.md#object-jack_desert_intro) | Object | Examples: `{ ... }` | 1 ||
| [`organ_boneyard_intro`](Miscellaneous.md#object-organ_boneyard_intro) | Object | Examples: `{ ... }` | 1 ||
| [`organ_throbbingdomain_intro`](Miscellaneous.md#object-organ_throbbingdomain_intro) | Object | Examples: `{ ... }` | 1 ||
| [`steven_postendgame`](Miscellaneous.md#object-steven_postendgame) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_begin_accepting_cats`](Miscellaneous.md#object-beanies_begin_accepting_cats) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_hitler3`](Miscellaneous.md#object-beanies_hitler3) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_hitler3_defeat`](Miscellaneous.md#object-beanies_hitler3_defeat) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_iloveyou`](Miscellaneous.md#object-beanies_iloveyou) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_infinite_intro`](Miscellaneous.md#object-beanies_infinite_intro) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_quest_complete`](Miscellaneous.md#object-beanies_quest_complete) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_quest_fail`](Miscellaneous.md#object-beanies_quest_fail) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_rift_intro`](Miscellaneous.md#object-beanies_rift_intro) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_screenshake_test`](Miscellaneous.md#object-beanies_screenshake_test) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_seefuture`](Miscellaneous.md#object-beanies_seefuture) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_seetheend`](Miscellaneous.md#object-beanies_seetheend) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_terminator1_defeat`](Miscellaneous.md#object-beanies_terminator1_defeat) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_terminator2_defeat`](Miscellaneous.md#object-beanies_terminator2_defeat) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_timemachine_2`](Miscellaneous.md#object-beanies_timemachine_2) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_timemachine_intro`](Miscellaneous.md#object-beanies_timemachine_intro) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_vscreator1`](Miscellaneous.md#object-beanies_vscreator1) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_vscreator2`](Miscellaneous.md#object-beanies_vscreator2) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_vscreator3`](Miscellaneous.md#object-beanies_vscreator3) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_vscreator4`](Miscellaneous.md#object-beanies_vscreator4) | Object | Examples: `{ ... }` | 1 ||
| [`beanies_vscreatorintro`](Miscellaneous.md#object-beanies_vscreatorintro) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_AI`](Miscellaneous.md#object-beaniesquest_complete_ai) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_AirHorn`](Miscellaneous.md#object-beaniesquest_complete_airhorn) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_AngryFace`](Miscellaneous.md#object-beaniesquest_complete_angryface) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_AnimalHands`](Miscellaneous.md#object-beaniesquest_complete_animalhands) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_BubbleBoy`](Miscellaneous.md#object-beaniesquest_complete_bubbleboy) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_ChadImplant`](Miscellaneous.md#object-beaniesquest_complete_chadimplant) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_ChaosDevice`](Miscellaneous.md#object-beaniesquest_complete_chaosdevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_DimensionalDivider`](Miscellaneous.md#object-beaniesquest_complete_dimensionaldivider) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_DiseaseJar`](Miscellaneous.md#object-beaniesquest_complete_diseasejar) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_ExperimentalTreatment`](Miscellaneous.md#object-beaniesquest_complete_experimentaltreatment) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_FartFace`](Miscellaneous.md#object-beaniesquest_complete_fartface) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_FigLeaf`](Miscellaneous.md#object-beaniesquest_complete_figleaf) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_Generic`](Miscellaneous.md#object-beaniesquest_complete_generic) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_GlassCannon`](Miscellaneous.md#object-beaniesquest_complete_glasscannon) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_HardPill`](Miscellaneous.md#object-beaniesquest_complete_hardpill) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_HiveMind`](Miscellaneous.md#object-beaniesquest_complete_hivemind) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_MagicMirror`](Miscellaneous.md#object-beaniesquest_complete_magicmirror) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_MeStone`](Miscellaneous.md#object-beaniesquest_complete_mestone) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_MultilinkCable`](Miscellaneous.md#object-beaniesquest_complete_multilinkcable) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_MysteriousDice`](Miscellaneous.md#object-beaniesquest_complete_mysteriousdice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_MysteriousGlasses`](Miscellaneous.md#object-beaniesquest_complete_mysteriousglasses) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_NDEDevice`](Miscellaneous.md#object-beaniesquest_complete_ndedevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_NuclearKnife`](Miscellaneous.md#object-beaniesquest_complete_nuclearknife) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_PartialLobotomy`](Miscellaneous.md#object-beaniesquest_complete_partiallobotomy) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_PartyDetonator`](Miscellaneous.md#object-beaniesquest_complete_partydetonator) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_PersonalHeater`](Miscellaneous.md#object-beaniesquest_complete_personalheater) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_PersuasionDevice`](Miscellaneous.md#object-beaniesquest_complete_persuasiondevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_PrincessHat`](Miscellaneous.md#object-beaniesquest_complete_princesshat) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_RealityScrambler`](Miscellaneous.md#object-beaniesquest_complete_realityscrambler) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_Redacted`](Miscellaneous.md#object-beaniesquest_complete_redacted) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_SpiderInjector`](Miscellaneous.md#object-beaniesquest_complete_spiderinjector) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_Stopwatch`](Miscellaneous.md#object-beaniesquest_complete_stopwatch) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_StorageLocker`](Miscellaneous.md#object-beaniesquest_complete_storagelocker) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_TheIOU`](Miscellaneous.md#object-beaniesquest_complete_theiou) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_TheLoner`](Miscellaneous.md#object-beaniesquest_complete_theloner) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_Trapfest99`](Miscellaneous.md#object-beaniesquest_complete_trapfest99) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_complete_UltraVision3000`](Miscellaneous.md#object-beaniesquest_complete_ultravision3000) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_AI`](Miscellaneous.md#object-beaniesquest_fail_ai) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_AirHorn`](Miscellaneous.md#object-beaniesquest_fail_airhorn) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_AngryFace`](Miscellaneous.md#object-beaniesquest_fail_angryface) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_AnimalHands`](Miscellaneous.md#object-beaniesquest_fail_animalhands) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_BubbleBoy`](Miscellaneous.md#object-beaniesquest_fail_bubbleboy) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_ChadImplant`](Miscellaneous.md#object-beaniesquest_fail_chadimplant) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_ChaosDevice`](Miscellaneous.md#object-beaniesquest_fail_chaosdevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_DimensionalDivider`](Miscellaneous.md#object-beaniesquest_fail_dimensionaldivider) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_DiseaseJar`](Miscellaneous.md#object-beaniesquest_fail_diseasejar) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_ExperimentalTreatment`](Miscellaneous.md#object-beaniesquest_fail_experimentaltreatment) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_FartFace`](Miscellaneous.md#object-beaniesquest_fail_fartface) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_FigLeaf`](Miscellaneous.md#object-beaniesquest_fail_figleaf) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_Generic`](Miscellaneous.md#object-beaniesquest_fail_generic) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_GlassCannon`](Miscellaneous.md#object-beaniesquest_fail_glasscannon) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_HardPill`](Miscellaneous.md#object-beaniesquest_fail_hardpill) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_HiveMind`](Miscellaneous.md#object-beaniesquest_fail_hivemind) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_MagicMirror`](Miscellaneous.md#object-beaniesquest_fail_magicmirror) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_MeStone`](Miscellaneous.md#object-beaniesquest_fail_mestone) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_MultilinkCable`](Miscellaneous.md#object-beaniesquest_fail_multilinkcable) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_MysteriousDice`](Miscellaneous.md#object-beaniesquest_fail_mysteriousdice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_MysteriousGlasses`](Miscellaneous.md#object-beaniesquest_fail_mysteriousglasses) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_NDEDevice`](Miscellaneous.md#object-beaniesquest_fail_ndedevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_NuclearKnife`](Miscellaneous.md#object-beaniesquest_fail_nuclearknife) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_PartialLobotomy`](Miscellaneous.md#object-beaniesquest_fail_partiallobotomy) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_PartyDetonator`](Miscellaneous.md#object-beaniesquest_fail_partydetonator) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_PersonalHeater`](Miscellaneous.md#object-beaniesquest_fail_personalheater) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_PersuasionDevice`](Miscellaneous.md#object-beaniesquest_fail_persuasiondevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_PrincessHat`](Miscellaneous.md#object-beaniesquest_fail_princesshat) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_RealityScrambler`](Miscellaneous.md#object-beaniesquest_fail_realityscrambler) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_Redacted`](Miscellaneous.md#object-beaniesquest_fail_redacted) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_SpiderInjector`](Miscellaneous.md#object-beaniesquest_fail_spiderinjector) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_Stopwatch`](Miscellaneous.md#object-beaniesquest_fail_stopwatch) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_StorageLocker`](Miscellaneous.md#object-beaniesquest_fail_storagelocker) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_TheIOU`](Miscellaneous.md#object-beaniesquest_fail_theiou) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_TheLoner`](Miscellaneous.md#object-beaniesquest_fail_theloner) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_Trapfest99`](Miscellaneous.md#object-beaniesquest_fail_trapfest99) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_fail_UltraVision3000`](Miscellaneous.md#object-beaniesquest_fail_ultravision3000) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_AI`](Miscellaneous.md#object-beaniesquest_intro_ai) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_AirHorn`](Miscellaneous.md#object-beaniesquest_intro_airhorn) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_AngryFace`](Miscellaneous.md#object-beaniesquest_intro_angryface) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_AnimalHands`](Miscellaneous.md#object-beaniesquest_intro_animalhands) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_BubbleBoy`](Miscellaneous.md#object-beaniesquest_intro_bubbleboy) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_ChadImplant`](Miscellaneous.md#object-beaniesquest_intro_chadimplant) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_ChaosDevice`](Miscellaneous.md#object-beaniesquest_intro_chaosdevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_DimensionalDivider`](Miscellaneous.md#object-beaniesquest_intro_dimensionaldivider) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_DiseaseJar`](Miscellaneous.md#object-beaniesquest_intro_diseasejar) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_ExperimentalTreatment`](Miscellaneous.md#object-beaniesquest_intro_experimentaltreatment) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_FartFace`](Miscellaneous.md#object-beaniesquest_intro_fartface) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_FigLeaf`](Miscellaneous.md#object-beaniesquest_intro_figleaf) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_Generic`](Miscellaneous.md#object-beaniesquest_intro_generic) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_GlassCannon`](Miscellaneous.md#object-beaniesquest_intro_glasscannon) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_HardPill`](Miscellaneous.md#object-beaniesquest_intro_hardpill) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_HiveMind`](Miscellaneous.md#object-beaniesquest_intro_hivemind) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_MagicMirror`](Miscellaneous.md#object-beaniesquest_intro_magicmirror) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_MeStone`](Miscellaneous.md#object-beaniesquest_intro_mestone) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_MultilinkCable`](Miscellaneous.md#object-beaniesquest_intro_multilinkcable) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_MysteriousDice`](Miscellaneous.md#object-beaniesquest_intro_mysteriousdice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_MysteriousGlasses`](Miscellaneous.md#object-beaniesquest_intro_mysteriousglasses) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_NDEDevice`](Miscellaneous.md#object-beaniesquest_intro_ndedevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_NuclearKnife`](Miscellaneous.md#object-beaniesquest_intro_nuclearknife) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_PartialLobotomy`](Miscellaneous.md#object-beaniesquest_intro_partiallobotomy) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_PartyDetonator`](Miscellaneous.md#object-beaniesquest_intro_partydetonator) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_PersonalHeater`](Miscellaneous.md#object-beaniesquest_intro_personalheater) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_PersuasionDevice`](Miscellaneous.md#object-beaniesquest_intro_persuasiondevice) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_PrincessHat`](Miscellaneous.md#object-beaniesquest_intro_princesshat) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_RealityScrambler`](Miscellaneous.md#object-beaniesquest_intro_realityscrambler) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_Redacted`](Miscellaneous.md#object-beaniesquest_intro_redacted) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_SpiderInjector`](Miscellaneous.md#object-beaniesquest_intro_spiderinjector) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_Stopwatch`](Miscellaneous.md#object-beaniesquest_intro_stopwatch) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_StorageLocker`](Miscellaneous.md#object-beaniesquest_intro_storagelocker) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_TheIOU`](Miscellaneous.md#object-beaniesquest_intro_theiou) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_TheLoner`](Miscellaneous.md#object-beaniesquest_intro_theloner) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_Trapfest99`](Miscellaneous.md#object-beaniesquest_intro_trapfest99) | Object | Examples: `{ ... }` | 1 ||
| [`beaniesquest_intro_UltraVision3000`](Miscellaneous.md#object-beaniesquest_intro_ultravision3000) | Object | Examples: `{ ... }` | 1 ||
| [`boss_fight_intro`](Miscellaneous.md#object-boss_fight_intro) | Object | Examples: `{ ... }` | 1 ||
| [`boss_fight_round2`](Miscellaneous.md#object-boss_fight_round2) | Object | Examples: `{ ... }` | 1 ||
| [`butch_begin_accepting_cats`](Miscellaneous.md#object-butch_begin_accepting_cats) | Object | Examples: `{ ... }` | 1 ||
| [`butch_first_house_boss_beat`](Miscellaneous.md#object-butch_first_house_boss_beat) | Object | Examples: `{ ... }` | 1 ||
| [`butch_pyro`](Miscellaneous.md#object-butch_pyro) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tina1`](Miscellaneous.md#object-butch_tina1) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_backstab`](Miscellaneous.md#object-butch_tips_backstab) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_charisma`](Miscellaneous.md#object-butch_tips_charisma) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_combat`](Miscellaneous.md#object-butch_tips_combat) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_disorders`](Miscellaneous.md#object-butch_tips_disorders) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_drafting`](Miscellaneous.md#object-butch_tips_drafting) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_elements`](Miscellaneous.md#object-butch_tips_elements) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_hard`](Miscellaneous.md#object-butch_tips_hard) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_headhome`](Miscellaneous.md#object-butch_tips_headhome) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_houseboss`](Miscellaneous.md#object-butch_tips_houseboss) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_info`](Miscellaneous.md#object-butch_tips_info) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_intelligence`](Miscellaneous.md#object-butch_tips_intelligence) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_intro`](Miscellaneous.md#object-butch_tips_intro) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_items`](Miscellaneous.md#object-butch_tips_items) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_lesscats`](Miscellaneous.md#object-butch_tips_lesscats) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_magicdamage`](Miscellaneous.md#object-butch_tips_magicdamage) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_passives`](Miscellaneous.md#object-butch_tips_passives) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_reorient`](Miscellaneous.md#object-butch_tips_reorient) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_rewards`](Miscellaneous.md#object-butch_tips_rewards) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_tacticalview`](Miscellaneous.md#object-butch_tips_tacticalview) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_turnorder`](Miscellaneous.md#object-butch_tips_turnorder) | Object | Examples: `{ ... }` | 1 ||
| [`butch_tips_wellrounded`](Miscellaneous.md#object-butch_tips_wellrounded) | Object | Examples: `{ ... }` | 1 ||
| [`can_still_use_attack`](Miscellaneous.md#object-can_still_use_attack) | Object | Examples: `{ ... }` | 1 ||
| [`can_still_use_attack_didntspell`](Miscellaneous.md#object-can_still_use_attack_didntspell) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_a`](Miscellaneous.md#object-cant_afford_a) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_b`](Miscellaneous.md#object-cant_afford_b) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_c`](Miscellaneous.md#object-cant_afford_c) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_d`](Miscellaneous.md#object-cant_afford_d) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_iceage`](Miscellaneous.md#object-cant_afford_iceage) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_jurassic`](Miscellaneous.md#object-cant_afford_jurassic) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_moon`](Miscellaneous.md#object-cant_afford_moon) | Object | Examples: `{ ... }` | 1 ||
| [`cant_afford_theend`](Miscellaneous.md#object-cant_afford_theend) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_butcher`](Miscellaneous.md#object-class_unlock_butcher) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_druid`](Miscellaneous.md#object-class_unlock_druid) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_medic`](Miscellaneous.md#object-class_unlock_medic) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_monk`](Miscellaneous.md#object-class_unlock_monk) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_necromancer`](Miscellaneous.md#object-class_unlock_necromancer) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_psychic`](Miscellaneous.md#object-class_unlock_psychic) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_thief`](Miscellaneous.md#object-class_unlock_thief) | Object | Examples: `{ ... }` | 1 ||
| [`class_unlock_tinkerer`](Miscellaneous.md#object-class_unlock_tinkerer) | Object | Examples: `{ ... }` | 1 ||
| [`collected_new_items`](Miscellaneous.md#object-collected_new_items) | Object | Examples: `{ ... }` | 1 ||
| [`collected_nothing`](Miscellaneous.md#object-collected_nothing) | Object | Examples: `{ ... }` | 1 ||
| [`do_not_end_turn`](Miscellaneous.md#object-do_not_end_turn) | Object | Examples: `{ ... }` | 1 ||
| [`done_spitting_fail_ally`](Miscellaneous.md#object-done_spitting_fail_ally) | Object | Examples: `{ ... }` | 1 ||
| [`done_spitting_fail_miss`](Miscellaneous.md#object-done_spitting_fail_miss) | Object | Examples: `{ ... }` | 1 ||
| [`done_spitting_fail_rat`](Miscellaneous.md#object-done_spitting_fail_rat) | Object | Examples: `{ ... }` | 1 ||
| [`done_spitting_success`](Miscellaneous.md#object-done_spitting_success) | Object | Examples: `{ ... }` | 1 ||
| [`ending`](Miscellaneous.md#object-ending) | Object | Examples: `{ ... }` | 1 ||
| [`finish_adventure`](Miscellaneous.md#object-finish_adventure) | Object | Examples: `{ ... }` | 1 ||
| [`first_fight_intro`](Miscellaneous.md#object-first_fight_intro) | Object | Examples: `{ ... }` | 1 ||
| [`first_house_boss_tomorrow`](Miscellaneous.md#object-first_house_boss_tomorrow) | Object | Examples: `{ ... }` | 1 ||
| [`first_house_hint_retired`](Miscellaneous.md#object-first_house_hint_retired) | Object | Examples: `{ ... }` | 1 ||
| [`frank_max1`](Miscellaneous.md#object-frank_max1) | Object | Examples: `{ ... }` | 1 ||
| [`frank_max2`](Miscellaneous.md#object-frank_max2) | Object | Examples: `{ ... }` | 1 ||
| [`frank_max3`](Miscellaneous.md#object-frank_max3) | Object | Examples: `{ ... }` | 1 ||
| [`frank_max4`](Miscellaneous.md#object-frank_max4) | Object | Examples: `{ ... }` | 1 ||
| [`frank_max5`](Miscellaneous.md#object-frank_max5) | Object | Examples: `{ ... }` | 1 ||
| [`frank_terminator2`](Miscellaneous.md#object-frank_terminator2) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_1`](Miscellaneous.md#object-frank_tips_1) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_10`](Miscellaneous.md#object-frank_tips_10) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_2`](Miscellaneous.md#object-frank_tips_2) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_3`](Miscellaneous.md#object-frank_tips_3) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_4`](Miscellaneous.md#object-frank_tips_4) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_5`](Miscellaneous.md#object-frank_tips_5) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_6`](Miscellaneous.md#object-frank_tips_6) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_7`](Miscellaneous.md#object-frank_tips_7) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_8`](Miscellaneous.md#object-frank_tips_8) | Object | Examples: `{ ... }` | 1 ||
| [`frank_tips_9`](Miscellaneous.md#object-frank_tips_9) | Object | Examples: `{ ... }` | 1 ||
| [`gone`](Miscellaneous.md#object-gone) | Object | Examples: `{ ... }` | 1 ||
| [`house_intro`](Miscellaneous.md#object-house_intro) | Object | Examples: `{ ... }` | 1 ||
| [`house_kitten_box`](Miscellaneous.md#object-house_kitten_box) | Object | Examples: `{ ... }` | 1 ||
| [`house_pass_day`](Miscellaneous.md#object-house_pass_day) | Object | Examples: `{ ... }` | 1 ||
| [`house_pass_day2`](Miscellaneous.md#object-house_pass_day2) | Object | Examples: `{ ... }` | 1 ||
| [`house_pipe`](Miscellaneous.md#object-house_pipe) | Object | Examples: `{ ... }` | 1 ||
| [`house_retired_cat_box`](Miscellaneous.md#object-house_retired_cat_box) | Object | Examples: `{ ... }` | 1 ||
| [`house_starred_box`](Miscellaneous.md#object-house_starred_box) | Object | Examples: `{ ... }` | 1 ||
| [`house_strays`](Miscellaneous.md#object-house_strays) | Object | Examples: `{ ... }` | 1 ||
| [`house_upgrade_basement`](Miscellaneous.md#object-house_upgrade_basement) | Object | Examples: `{ ... }` | 1 ||
| [`house_upgrade_basement2`](Miscellaneous.md#object-house_upgrade_basement2) | Object | Examples: `{ ... }` | 1 ||
| [`house_upgrade_basement3`](Miscellaneous.md#object-house_upgrade_basement3) | Object | Examples: `{ ... }` | 1 ||
| [`house_upgrade_basement4`](Miscellaneous.md#object-house_upgrade_basement4) | Object | Examples: `{ ... }` | 1 ||
| [`house_upgrade_basement5`](Miscellaneous.md#object-house_upgrade_basement5) | Object | Examples: `{ ... }` | 1 ||
| [`introduce_hard_path`](Miscellaneous.md#object-introduce_hard_path) | Object | Examples: `{ ... }` | 1 ||
| [`jack_begin_accepting_cats`](Miscellaneous.md#object-jack_begin_accepting_cats) | Object | Examples: `{ ... }` | 1 ||
| [`Jack_Gainaltfurniture`](Engine_LogicKeys.md#object-jack_gainaltfurniture) | Object | Examples: `{ ... }` | 1 ||
| [`jack_introduction`](Miscellaneous.md#object-jack_introduction) | Object | Examples: `{ ... }` | 1 ||
| [`jack_max1`](Miscellaneous.md#object-jack_max1) | Object | Examples: `{ ... }` | 1 ||
| [`jack_max2`](Miscellaneous.md#object-jack_max2) | Object | Examples: `{ ... }` | 1 ||
| [`jack_max3`](Miscellaneous.md#object-jack_max3) | Object | Examples: `{ ... }` | 1 ||
| [`jack_max4`](Miscellaneous.md#object-jack_max4) | Object | Examples: `{ ... }` | 1 ||
| [`jack_max5`](Miscellaneous.md#object-jack_max5) | Object | Examples: `{ ... }` | 1 ||
| [`jack_zara`](Miscellaneous.md#object-jack_zara) | Object | Examples: `{ ... }` | 1 ||
| [`level_up_didnt_select_sunburn`](Miscellaneous.md#object-level_up_didnt_select_sunburn) | Object | Examples: `{ ... }` | 1 ||
| [`level_up_intro`](Miscellaneous.md#object-level_up_intro) | Object | Examples: `{ ... }` | 1 ||
| [`level_up_selected_sunburn`](Miscellaneous.md#object-level_up_selected_sunburn) | Object | Examples: `{ ... }` | 1 ||
| [`low_on_food`](Miscellaneous.md#object-low_on_food) | Object | Examples: `{ ... }` | 1 ||
| [`map_click_node`](Miscellaneous.md#object-map_click_node) | Object | Examples: `{ ... }` | 1 ||
| [`map_equip_items`](Miscellaneous.md#object-map_equip_items) | Object | Examples: `{ ... }` | 1 ||
| [`map_equip_items2`](Miscellaneous.md#object-map_equip_items2) | Object | Examples: `{ ... }` | 1 ||
| [`melee_attack_rat`](Miscellaneous.md#object-melee_attack_rat) | Object | Examples: `{ ... }` | 1 ||
| [`melee_cat_spit`](Miscellaneous.md#object-melee_cat_spit) | Object | Examples: `{ ... }` | 1 ||
| [`melee_cat_spit_fail_ally`](Miscellaneous.md#object-melee_cat_spit_fail_ally) | Object | Examples: `{ ... }` | 1 ||
| [`melee_cat_spit_fail_miss`](Miscellaneous.md#object-melee_cat_spit_fail_miss) | Object | Examples: `{ ... }` | 1 ||
| [`melee_cat_spit_fail_rat`](Miscellaneous.md#object-melee_cat_spit_fail_rat) | Object | Examples: `{ ... }` | 1 ||
| [`melee_cat_spit_ignore`](Miscellaneous.md#object-melee_cat_spit_ignore) | Object | Examples: `{ ... }` | 1 ||
| [`melee_cat_spit_success`](Miscellaneous.md#object-melee_cat_spit_success) | Object | Examples: `{ ... }` | 1 ||
| [`melee_killed_rat`](Miscellaneous.md#object-melee_killed_rat) | Object | Examples: `{ ... }` | 1 ||
| [`melee_move2`](Miscellaneous.md#object-melee_move2) | Object | Examples: `{ ... }` | 1 ||
| [`melee_out_of_actions`](Miscellaneous.md#object-melee_out_of_actions) | Object | Examples: `{ ... }` | 1 ||
| [`new_adventure`](Miscellaneous.md#object-new_adventure) | Object | Examples: `{ ... }` | 1 ||
| [`organ_intro`](Miscellaneous.md#object-organ_intro) | Object | Examples: `{ ... }` | 1 ||
| [`organ_max1`](Miscellaneous.md#object-organ_max1) | Object | Examples: `{ ... }` | 1 ||
| [`organ_max2`](Miscellaneous.md#object-organ_max2) | Object | Examples: `{ ... }` | 1 ||
| [`organ_max3`](Miscellaneous.md#object-organ_max3) | Object | Examples: `{ ... }` | 1 ||
| [`organ_max4`](Miscellaneous.md#object-organ_max4) | Object | Examples: `{ ... }` | 1 ||
| [`organ_max5`](Miscellaneous.md#object-organ_max5) | Object | Examples: `{ ... }` | 1 ||
| [`organ_rename`](Miscellaneous.md#object-organ_rename) | Object | Examples: `{ ... }` | 1 ||
| [`organ_tina3`](Miscellaneous.md#object-organ_tina3) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_a`](Miscellaneous.md#object-purchase_item_a) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_b`](Miscellaneous.md#object-purchase_item_b) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_c`](Miscellaneous.md#object-purchase_item_c) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_d`](Miscellaneous.md#object-purchase_item_d) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_iceage`](Miscellaneous.md#object-purchase_item_iceage) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_jurassic`](Miscellaneous.md#object-purchase_item_jurassic) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_moon`](Miscellaneous.md#object-purchase_item_moon) | Object | Examples: `{ ... }` | 1 ||
| [`purchase_item_theend`](Miscellaneous.md#object-purchase_item_theend) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_attack_tomtom`](Miscellaneous.md#object-ranged_attack_tomtom) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_attack_tomtom_fail_ally`](Miscellaneous.md#object-ranged_attack_tomtom_fail_ally) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_attack_tomtom_fail_miss`](Miscellaneous.md#object-ranged_attack_tomtom_fail_miss) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_attack_tomtom_fail_rat`](Miscellaneous.md#object-ranged_attack_tomtom_fail_rat) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_attack`](Miscellaneous.md#object-ranged_cat_attack) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_early_attack2_ally`](Miscellaneous.md#object-ranged_cat_early_attack2_ally) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_early_attack2_miss`](Miscellaneous.md#object-ranged_cat_early_attack2_miss) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_early_attack2_rat`](Miscellaneous.md#object-ranged_cat_early_attack2_rat) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_early_attack_ally`](Miscellaneous.md#object-ranged_cat_early_attack_ally) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_early_attack_miss`](Miscellaneous.md#object-ranged_cat_early_attack_miss) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_early_attack_rat`](Miscellaneous.md#object-ranged_cat_early_attack_rat) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_failmove`](Miscellaneous.md#object-ranged_cat_failmove) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_intro`](Miscellaneous.md#object-ranged_cat_intro) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_roll`](Miscellaneous.md#object-ranged_cat_roll) | Object | Examples: `{ ... }` | 1 ||
| [`ranged_cat_rolled_first`](Miscellaneous.md#object-ranged_cat_rolled_first) | Object | Examples: `{ ... }` | 1 ||
| [`steven_100`](Miscellaneous.md#object-steven_100) | Object | Examples: `{ ... }` | 1 ||
| [`steven_introduction`](Miscellaneous.md#object-steven_introduction) | Object | Examples: `{ ... }` | 1 ||
| [`steven_resummon`](Miscellaneous.md#object-steven_resummon) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_1`](Miscellaneous.md#object-steven_savescum_1) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_100`](Miscellaneous.md#object-steven_savescum_100) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_1alt1`](Miscellaneous.md#object-steven_savescum_1alt1) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_1alt2`](Miscellaneous.md#object-steven_savescum_1alt2) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_1alt3`](Miscellaneous.md#object-steven_savescum_1alt3) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_2`](Miscellaneous.md#object-steven_savescum_2) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_2alt1`](Miscellaneous.md#object-steven_savescum_2alt1) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_2alt2`](Miscellaneous.md#object-steven_savescum_2alt2) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_2alt3`](Miscellaneous.md#object-steven_savescum_2alt3) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_3`](Miscellaneous.md#object-steven_savescum_3) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_3alt1`](Miscellaneous.md#object-steven_savescum_3alt1) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_3alt2`](Miscellaneous.md#object-steven_savescum_3alt2) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_3alt3`](Miscellaneous.md#object-steven_savescum_3alt3) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_4`](Miscellaneous.md#object-steven_savescum_4) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_4alt1`](Miscellaneous.md#object-steven_savescum_4alt1) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_4alt2`](Miscellaneous.md#object-steven_savescum_4alt2) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_4alt3`](Miscellaneous.md#object-steven_savescum_4alt3) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_houseboss_1`](Miscellaneous.md#object-steven_savescum_houseboss_1) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_houseboss_100`](Miscellaneous.md#object-steven_savescum_houseboss_100) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_houseboss_2`](Miscellaneous.md#object-steven_savescum_houseboss_2) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_houseboss_3`](Miscellaneous.md#object-steven_savescum_houseboss_3) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_intro`](Miscellaneous.md#object-steven_savescum_intro) | Object | Examples: `{ ... }` | 1 ||
| [`steven_savescum_intro_houseboss`](Miscellaneous.md#object-steven_savescum_intro_houseboss) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act1_crazy`](Miscellaneous.md#object-steven_unlock_act1_crazy) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act1_impossible`](Miscellaneous.md#object-steven_unlock_act1_impossible) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act2_crazy`](Miscellaneous.md#object-steven_unlock_act2_crazy) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act2_hard`](Miscellaneous.md#object-steven_unlock_act2_hard) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act2_impossible`](Miscellaneous.md#object-steven_unlock_act2_impossible) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act3_crazy`](Miscellaneous.md#object-steven_unlock_act3_crazy) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act3_hard`](Miscellaneous.md#object-steven_unlock_act3_hard) | Object | Examples: `{ ... }` | 1 ||
| [`steven_unlock_act3_impossible`](Miscellaneous.md#object-steven_unlock_act3_impossible) | Object | Examples: `{ ... }` | 1 ||
| [`take_cats_inside`](Miscellaneous.md#object-take_cats_inside) | Object | Examples: `{ ... }` | 1 ||
| [`test_gamepad_prompts`](Miscellaneous.md#object-test_gamepad_prompts) | Object | Examples: `{ ... }` | 1 ||
| [`tink_begin_accepting_cats`](Miscellaneous.md#object-tink_begin_accepting_cats) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max1`](Miscellaneous.md#object-tink_max1) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max10`](Miscellaneous.md#object-tink_max10) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max2`](Miscellaneous.md#object-tink_max2) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max3`](Miscellaneous.md#object-tink_max3) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max4`](Miscellaneous.md#object-tink_max4) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max5`](Miscellaneous.md#object-tink_max5) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max6`](Miscellaneous.md#object-tink_max6) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max7`](Miscellaneous.md#object-tink_max7) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max8`](Miscellaneous.md#object-tink_max8) | Object | Examples: `{ ... }` | 1 ||
| [`tink_max9`](Miscellaneous.md#object-tink_max9) | Object | Examples: `{ ... }` | 1 ||
| [`tink_terminator`](Miscellaneous.md#object-tink_terminator) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tina2`](Miscellaneous.md#object-tink_tina2) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_appeal`](Miscellaneous.md#object-tink_tips_appeal) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_basestats`](Miscellaneous.md#object-tink_tips_basestats) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_cleaning`](Miscellaneous.md#object-tink_tips_cleaning) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_comfort`](Miscellaneous.md#object-tink_tips_comfort) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_health`](Miscellaneous.md#object-tink_tips_health) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_inbreeding`](Miscellaneous.md#object-tink_tips_inbreeding) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_intro`](Miscellaneous.md#object-tink_tips_intro) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_multiclassing`](Miscellaneous.md#object-tink_tips_multiclassing) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_mutation`](Miscellaneous.md#object-tink_tips_mutation) | Object | Examples: `{ ... }` | 1 ||
| [`tink_tips_stimulation`](Miscellaneous.md#object-tink_tips_stimulation) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_foodbonus1`](Miscellaneous.md#object-tracy_foodbonus1) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_introduction`](Miscellaneous.md#object-tracy_introduction) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_kaijufight`](Miscellaneous.md#object-tracy_kaijufight) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_max1`](Miscellaneous.md#object-tracy_max1) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_max2`](Miscellaneous.md#object-tracy_max2) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_max3`](Miscellaneous.md#object-tracy_max3) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_max4`](Miscellaneous.md#object-tracy_max4) | Object | Examples: `{ ... }` | 1 ||
| [`tracy_max5`](Miscellaneous.md#object-tracy_max5) | Object | Examples: `{ ... }` | 1 ||
| [`try_again_attack_rat`](Miscellaneous.md#object-try_again_attack_rat) | Object | Examples: `{ ... }` | 1 ||
| [`try_again_melee_move`](Miscellaneous.md#object-try_again_melee_move) | Object | Examples: `{ ... }` | 1 ||
| [`tutorial_cat_dies`](Miscellaneous.md#object-tutorial_cat_dies) | Object | Examples: `{ ... }` | 1 ||
| [`unprompted1`](Miscellaneous.md#object-unprompted1) | Object | Examples: `{ ... }` | 1 ||
| [`unprompted2`](Miscellaneous.md#object-unprompted2) | Object | Examples: `{ ... }` | 1 ||
| [`unprompted3`](Miscellaneous.md#object-unprompted3) | Object | Examples: `{ ... }` | 1 ||
| [`unprompted4`](Miscellaneous.md#object-unprompted4) | Object | Examples: `{ ... }` | 1 ||
| [`unprompted5`](Miscellaneous.md#object-unprompted5) | Object | Examples: `{ ... }` | 1 ||
| [`unprompted6`](Miscellaneous.md#object-unprompted6) | Object | Examples: `{ ... }` | 1 ||
| [`upgrade_storage_max1`](Miscellaneous.md#object-upgrade_storage_max1) | Object | Examples: `{ ... }` | 1 ||
| [`upgrade_storage_max2`](Miscellaneous.md#object-upgrade_storage_max2) | Object | Examples: `{ ... }` | 1 ||
| [`upgrade_storage_max3`](Miscellaneous.md#object-upgrade_storage_max3) | Object | Examples: `{ ... }` | 1 ||
| [`upgrade_storage_max4`](Miscellaneous.md#object-upgrade_storage_max4) | Object | Examples: `{ ... }` | 1 ||
| [`upgrade_storage_max5`](Miscellaneous.md#object-upgrade_storage_max5) | Object | Examples: `{ ... }` | 1 ||
| [`use_attack_after_used_weapon`](Miscellaneous.md#object-use_attack_after_used_weapon) | Object | Examples: `{ ... }` | 1 ||
| [`use_weapon`](Events_and_Encounters.md#object-use_weapon) | Object | Examples: `{ ... }` | 1 ||
| [`welcome`](Miscellaneous.md#object-welcome) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_boneyard`](Miscellaneous.md#object-welcome_boneyard) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_bunker`](Miscellaneous.md#object-welcome_bunker) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_caves`](Miscellaneous.md#object-welcome_caves) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_core`](Miscellaneous.md#object-welcome_core) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_crater`](Miscellaneous.md#object-welcome_crater) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_desert`](Miscellaneous.md#object-welcome_desert) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_future`](Miscellaneous.md#object-welcome_future) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_iceage`](Miscellaneous.md#object-welcome_iceage) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_junkyard`](Miscellaneous.md#object-welcome_junkyard) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_jurassic`](Miscellaneous.md#object-welcome_jurassic) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_lab`](Miscellaneous.md#object-welcome_lab) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_moon`](Miscellaneous.md#object-welcome_moon) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_sewers`](Miscellaneous.md#object-welcome_sewers) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_theend`](Miscellaneous.md#object-welcome_theend) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_water`](Miscellaneous.md#object-welcome_water) | Object | Examples: `{ ... }` | 1 ||
| [`welcome_water_cheap`](Miscellaneous.md#object-welcome_water_cheap) | Object | Examples: `{ ... }` | 1 ||

</details>

---

### Object: `states`


**Definition:** No definition provided.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`idle`](./Arrays.md#array-idle) | Array | Examples: `[ "idle" "blocking" ], [ "idle" ], [ "idle" "blocking" "gone" ]` | 10 ||
| [`closeup`](./Arrays.md#array-closeup) | Array | Examples: `[ "closeup" ]` | 3 ||
| [`verycloseup`](./Arrays.md#array-verycloseup) | Array | Examples: `[ "verycloseup" ]` | 3 ||
| [`zoomedout`](./Arrays.md#array-zoomedout) | Array | Examples: `[ "zoomedout" ]` | 3 ||
| [`beanies_intensestatic`](./Arrays.md#array-beanies_intensestatic) | Array | Examples: `[ "beanies_intensestatic" ]` | 1 ||
| [`beanies_right`](./Arrays.md#array-beanies_right) | Array | Examples: `[ "beanies_right" ]` | 1 ||
| [`butch_left`](./Arrays.md#array-butch_left) | Array | Examples: `[ "butch_left" "butch_point_move" "butch_point_attack" "b...` | 1 ||
| [`butch_right`](./Arrays.md#array-butch_right) | Array | Examples: `[ "butch_right" "butch_point_spells" "butch_point_turnord...` | 1 ||
| [`choosecats`](./Arrays.md#array-choosecats) | Array | Examples: `[ "choosecats" ]` | 1 ||
| [`closerup`](./Arrays.md#array-closerup) | Array | Examples: `[ "closerup" ]` | 1 ||
| [`frank_right`](./Arrays.md#array-frank_right) | Array | Examples: `[ "frank_right" "frank_point_pipe" ]` | 1 ||
| [`jack_right`](./Arrays.md#array-jack_right) | Array | Examples: `[ "jack_right" "jack_point_furniture" ]` | 1 ||
| [`offscreen`](./Arrays.md#array-offscreen) | Array | Examples: `[ "offscreen" ]` | 1 ||
| [`steven_center`](./Arrays.md#array-steven_center) | Array | Examples: `[ "steven_center" "steven_cat" ]` | 1 ||
| [`tink_left`](./Arrays.md#array-tink_left) | Array | Examples: `[ "tink_left" "tink_point_cats" "tink_point_food" "tink_p...` | 1 ||
| [`tink_right`](./Arrays.md#array-tink_right) | Array | Examples: `[ "tink_right" "tink_point_strays" ]` | 1 ||

</details>

---

### Object: `transitions`


**Definition:** No definition provided.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`beanies_intensestatic_to_offscreen`](./Arrays.md#array-beanies_intensestatic_to_offscreen) | Array | Examples: `[ beanies_intensestatic offscreen ]` | 1 ||
| [`beanies_offscreen_to_intensestatic`](./Arrays.md#array-beanies_offscreen_to_intensestatic) | Array | Examples: `[ offscreen beanies_intensestatic ]` | 1 ||
| [`beanies_offscreen_to_right`](./Arrays.md#array-beanies_offscreen_to_right) | Array | Examples: `[ offscreen beanies_right ]` | 1 ||
| [`beanies_right_to_offscreen`](./Arrays.md#array-beanies_right_to_offscreen) | Array | Examples: `[ beanies_right offscreen ]` | 1 ||
| [`butch_left_to_offscreen`](./Arrays.md#array-butch_left_to_offscreen) | Array | Examples: `[ butch_left offscreen ]` | 1 ||
| [`butch_left_to_right`](./Arrays.md#array-butch_left_to_right) | Array | Examples: `[ butch_left butch_right ]` | 1 ||
| [`butch_offscreen_to_left`](./Arrays.md#array-butch_offscreen_to_left) | Array | Examples: `[ offscreen butch_left ]` | 1 ||
| [`butch_offscreen_to_right`](./Arrays.md#array-butch_offscreen_to_right) | Array | Examples: `[ offscreen butch_right ]` | 1 ||
| [`butch_right_to_left`](./Arrays.md#array-butch_right_to_left) | Array | Examples: `[ butch_right butch_left ]` | 1 ||
| [`butch_right_to_offscreen`](./Arrays.md#array-butch_right_to_offscreen) | Array | Examples: `[ butch_right offscreen ]` | 1 ||
| [`frank_offscreen_to_right`](./Arrays.md#array-frank_offscreen_to_right) | Array | Examples: `[ offscreen frank_right ]` | 1 ||
| [`frank_right_to_offscreen`](./Arrays.md#array-frank_right_to_offscreen) | Array | Examples: `[ frank_right offscreen ]` | 1 ||
| [`jack_offscreen_to_right`](./Arrays.md#array-jack_offscreen_to_right) | Array | Examples: `[ offscreen jack_right ]` | 1 ||
| [`jack_right_to_offscreen`](./Arrays.md#array-jack_right_to_offscreen) | Array | Examples: `[ jack_right offscreen ]` | 1 ||
| [`steven_center_to_offscreen`](./Arrays.md#array-steven_center_to_offscreen) | Array | Examples: `[ steven_center offscreen ]` | 1 ||
| [`steven_offscreen_to_center`](./Arrays.md#array-steven_offscreen_to_center) | Array | Examples: `[ offscreen steven_center ]` | 1 ||
| [`tink_left_to_offscreen`](./Arrays.md#array-tink_left_to_offscreen) | Array | Examples: `[ tink_left offscreen ]` | 1 ||
| [`tink_left_to_right`](./Arrays.md#array-tink_left_to_right) | Array | Examples: `[ tink_left tink_right ]` | 1 ||
| [`tink_offscreen_to_left`](./Arrays.md#array-tink_offscreen_to_left) | Array | Examples: `[ offscreen tink_left ]` | 1 ||
| [`tink_offscreen_to_right`](./Arrays.md#array-tink_offscreen_to_right) | Array | Examples: `[ offscreen tink_right ]` | 1 ||
| [`tink_right_to_left`](./Arrays.md#array-tink_right_to_left) | Array | Examples: `[ tink_right tink_left ]` | 1 ||
| [`tink_right_to_offscreen`](./Arrays.md#array-tink_right_to_offscreen) | Array | Examples: `[ tink_right offscreen ]` | 1 ||

</details>

---

### Object: `unprompted`


**Definition:** No definition provided.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ unprompted_a unprompted_b unprompted_c unprompted_d unp..., [ unprompted1 u...` | 5 ||
| `cancelable` | Boolean | Examples: `true` | 3 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_JACK_UNPROMPTED_1, NPC_ORGANGRINDER_UNPROMPTED_1, NPC_TRACY_UNPROMPTED_2` | 3 ||
| `wait_for_cancel` | Number | Examples: `1` | 3 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_UNPROMPTED_1, NPC_TRACY_UNPROMPTED_1` | 2 ||

</details>

---

### Object: `also`


**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_ALSO_1, NPC_BEANIES_ALSO_1, NPC_BUTCH_ALSO_1` | 8 ||

</details>

---

### Object: `unknown`


**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNKNOWN_1, NPC_FRANK_UNKNOWN_1, NPC_BEANIES_UNKNOWN_1` | 8 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 8 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 3 ||
| `lock_controls` | Number | Examples: `1` | 3 ||
| `unlock_controls` | Number | Examples: `1` | 3 ||

</details>

---

### Object: `hide_text`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 4 ||
| [`dialog_and_autopass`](./Strings.md#string-dialog_and_autopass) | String | Examples: `""` | 4 ||

</details>

---

### Object: `purchase_item`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 3 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_PURCHASE_ITEM_1, NPC_ORGANGRINDER_PURCHASE_ITEM_1, NPC_JACK_PURCHAS...` | 3 ||
| `wait_for_cancel` | Number | Examples: `1` | 3 ||
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ purchase_item_a purchase_item_b purchase_item_c purchas...` | 1 ||

</details>

---

### Object: `tooltip`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 4 ||
| [`tooltip_dialog`](./Enums.md#enum-tooltip_dialog) | Enum | Examples: `NPC_TRACY_SHOP_TOOLTIP, NPC_ORGANGRINDER_SHOP_TOOLTIP, NPC_JACK_SHOP_TOOLTIP` | 4 ||
| `wait_for_cancel` | Number | Examples: `1` | 4 ||

</details>

---

### Object: `unprompted_a`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_A_1, NPC_FRANK_UNPROMPTED_A_2, NPC_BUTCH_UNPROMPTED_A_1` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_b`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_B_1, NPC_FRANK_UNPROMPTED_B_1, NPC_FRANK_UNPROMPTED_B_2` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_c`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_C_1, NPC_FRANK_UNPROMPTED_C_2, NPC_BUTCH_UNPROMPTED_C_1` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_d`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_D_1, NPC_BUTCH_UNPROMPTED_D_1, NPC_FRANK_UNPROMPTED_D_2` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_e`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_E_1, NPC_BUTCH_UNPROMPTED_E_1, NPC_FRANK_UNPROMPTED_E_2` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_f`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_F_1, NPC_FRANK_UNPROMPTED_F_2, NPC_FRANK_UNPROMPTED_F_1` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_g`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_G_2, NPC_BUTCH_UNPROMPTED_G_1, NPC_FRANK_UNPROMPTED_G_1` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_h`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_H_1, NPC_FRANK_UNPROMPTED_H_2, NPC_FRANK_UNPROMPTED_H_1` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `unprompted_i`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_I_2, NPC_BUTCH_UNPROMPTED_I_1, NPC_FRANK_UNPROMPTED_I_1` | 4 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 ||

</details>

---

### Object: `cant_afford`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_CANT_AFFORD_1, NPC_JACK_CANT_AFFORD_1` | 2 ||
| `wait_for_cancel` | Number | Examples: `1` | 2 ||
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ cant_afford_a cant_afford_b cant_afford_c cant_afford_d ]` | 1 ||

</details>

---

### Object: `forward_to_tips`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ butch_tips_intelligence butch_tips_charisma butch_tips_..., [ frank_tips_1 ...` | 3 ||

</details>

---

### Object: `out_of_stock`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_OUT_OF_STOCK_1, NPC_JACK_OUT_OF_STOCK_1, NPC_TRACY_OUT_OF_ST...` | 3 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `blocking` | 3 ||

</details>

---

### Object: `beanies_begin_accepting_cats`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_2, NPC_BEANIES_BEANIES_BEGIN_ACCEPTI...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `beanies` | 1 ||

</details>

---

### Object: `beanies_bombquest_2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_2_2, NPC_BEANIES_BEANIES_BOMBQUEST_2_1, NPC_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beanies_bombquest_3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_3_1, NPC_BEANIES_BEANIES_BOMBQUEST_3_2, NPC_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `nuke_quest_get_nuke` | 1 ||

</details>

---

### Object: `beanies_bombquest_amnesia`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_1, NPC_BEANIES_BEANIES_BOMBQUEST_AMNESI...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `nuke_quest_loop` | 1 ||

</details>

---

### Object: `beanies_bombquest_begin`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_2, NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_1,...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 ||

</details>

---

### Object: `beanies_bombquest_fail_jarofblood`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_3, NPC_BEANIES_BEANIES_BOMBQUES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 ||

</details>

---

### Object: `beanies_bombquest_fail_jarofchaos`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_3, NPC_BEANIES_BEANIES_BOMBQUES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 ||

</details>

---

### Object: `beanies_bombquest_fail_jarofradiation`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_1, NPC_BEANIES_BEANIES_BOMB...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 ||

</details>

---

### Object: `beanies_bombquest_fail_nuke`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_3, NPC_BEANIES_BEANIES_BOMBQUEST_FAIL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 ||

</details>

---

### Object: `beanies_future_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_FUTURE_INTRO_2, NPC_BEANIES_BEANIES_FUTURE_INTRO_3, NPC_B...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||

</details>

---

### Object: `beanies_hitler3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_HITLER3_2, NPC_BEANIES_BEANIES_HITLER3_1, NPC_BEANIES_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beanies_hitler3_defeat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_2, NPC_BEANIES_BEANIES_HITLER3_DEFEAT_1, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_amplifier2` | 1 ||

</details>

---

### Object: `beanies_iloveyou`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_ILOVEYOU_2, NPC_BEANIES_BEANIES_ILOVEYOU_3, NPC_BEANIES_B...` | 1 ||

</details>

---

### Object: `beanies_infinite_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_INFINITE_INTRO_3, NPC_POPUP_BEANIES_INFINITE_INTRO_2, NPC_P...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.25` | 1 ||

</details>

---

### Object: `beanies_jurassic_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_JURASSIC_INTRO_1, NPC_BEANIES_BEANIES_JURASSIC_INTRO_2, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beanies_lab_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_LAB_INTRO_1, NPC_BEANIES_BEANIES_LAB_INTRO_3, NPC_BEANIES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`play_cutscene`](./Enums.md#enum-play_cutscene) | Enum | Examples: `credits_1` | 1 ||
| `restart_npc_music` | Number | Examples: `1` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `song_unlock_get_in_the_cage` | 1 ||

</details>

---

### Object: `beanies_quest_complete`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_complete` | 1 ||
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `success` | 1 ||

</details>

---

### Object: `beanies_quest_fail`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_fail` | 1 ||
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `fail` | 1 ||

</details>

---

### Object: `beanies_quests_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_QUESTS_INTRO_3, NPC_BEANIES_BEANIES_QUESTS_INTRO_1, NPC_B...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_intro` | 1 ||
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `newest` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `beanies_quests_repeat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_QUESTS_REPEAT_1, NPC_BEANIES_BEANIES_QUESTS_REPEAT_3, NPC...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_intro` | 1 ||
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `newest` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `beanies_rift_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_RIFT_INTRO_1, NPC_POPUP_BEANIES_RIFT_INTRO_2, NPC_POPUP_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.25` | 1 ||

</details>

---

### Object: `beanies_screenshake_test`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_1, NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_...` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `PickupCoin` | 1 ||
| [`screenshake`](./Arrays.md#array-screenshake) | Array | Examples: `[ .5 10 ]` | 1 ||

</details>

---

### Object: `beanies_seefuture`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SEEFUTURE_3, NPC_BEANIES_BEANIES_SEEFUTURE_2, NPC_BEANIES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beanies_seetheend`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SEETHEEND_1, NPC_BEANIES_BEANIES_SEETHEEND_2, NPC_BEANIES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beanies_terminator1_defeat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_1, NPC_BEANIES_BEANIES_TERMINATOR1_DEF...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_receiver2` | 1 ||

</details>

---

### Object: `beanies_terminator2_defeat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_3, NPC_BEANIES_BEANIES_TERMINATOR2_DEF...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_transmitter2` | 1 ||

</details>

---

### Object: `beanies_theend_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_THEEND_INTRO_3, NPC_BEANIES_BEANIES_THEEND_INTRO_2, NPC_B...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||

</details>

---

### Object: `beanies_timemachine_2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TIMEMACHINE_2_2, NPC_BEANIES_BEANIES_TIMEMACHINE_2_3, NPC...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beanies_timemachine_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_2, NPC_BEANIES_BEANIES_TIMEMACHINE_INTR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `time_machine_quest_begin` | 1 ||

</details>

---

### Object: `beanies_vscreator1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR1_1, NPC_POPUP_BEANIES_VSCREATOR1_3, NPC_POPUP_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 1 ||

</details>

---

### Object: `beanies_vscreator2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR2_1, NPC_POPUP_BEANIES_VSCREATOR2_3, NPC_POPUP_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 1 ||

</details>

---

### Object: `beanies_vscreator3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR3_2, NPC_POPUP_BEANIES_VSCREATOR3_3, NPC_POPUP_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_intensestatic` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 1 ||

</details>

---

### Object: `beanies_vscreator4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR4_2, NPC_POPUP_BEANIES_VSCREATOR4_3, NPC_POPUP_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_intensestatic` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 1 ||
| [`force_current_cat_use_ability`](./Enums.md#enum-force_current_cat_use_ability) | Enum | Examples: `neck_NukeBonus_remote` | 1 ||

</details>

---

### Object: `beanies_vscreatorintro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATORINTRO_1, NPC_POPUP_BEANIES_VSCREATORINTRO_2, NPC_P...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 1 ||

</details>

---

### Object: `beaniesquest_complete_AI`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_3, NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_AirHorn`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_AngryFace`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `beaniesquest_complete_AnimalHands`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_2, NPC_BEANIES_BEANIESQUEST_COM...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_BubbleBoy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_3, NPC_BEANIES_BEANIESQUEST_COMPL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_ChadImplant`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_2, NPC_BEANIES_BEANIESQUEST_COM...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_ChaosDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_1, NPC_BEANIES_BEANIESQUEST_COM...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `beaniesquest_complete_DimensionalDivider`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_2, NPC_BEANIES_BEANIESQU...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_DiseaseJar`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_1, NPC_BEANIES_BEANIESQUEST_COMP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_ExperimentalTreatment`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_3, NPC_BEANIES_BEANIE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_FartFace`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_3, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_FigLeaf`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_3, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_Generic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_2, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_GlassCannon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_1, NPC_BEANIES_BEANIESQUEST_COM...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_HardPill`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_1, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_HiveMind`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_MagicMirror`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_2, NPC_BEANIES_BEANIESQUEST_COM...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_MeStone`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_3, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_MultilinkCable`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_MysteriousDice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_3, NPC_BEANIES_BEANIESQUEST_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_MysteriousGlasses`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_1, NPC_BEANIES_BEANIESQUE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_NDEDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_NuclearKnife`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_2, NPC_BEANIES_BEANIESQUEST_CO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_PartialLobotomy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_1, NPC_BEANIES_BEANIESQUEST...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_PartyDetonator`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_2, NPC_BEANIES_BEANIESQUEST_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_PersonalHeater`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_PersuasionDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_1, NPC_BEANIES_BEANIESQUES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_PrincessHat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_1, NPC_BEANIES_BEANIESQUEST_COM...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_RealityScrambler`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_1, NPC_BEANIES_BEANIESQUES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_Redacted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_SpiderInjector`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_1, NPC_BEANIES_BEANIESQUEST_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_Stopwatch`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_StorageLocker`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_3, NPC_BEANIES_BEANIESQUEST_C...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_TheIOU`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_1, NPC_BEANIES_BEANIESQUEST_COMPLETE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_TheLoner`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_complete_Trapfest99`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_COMP...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `beaniesquest_complete_UltraVision3000`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_1, NPC_BEANIES_BEANIESQUEST...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 ||

</details>

---

### Object: `beaniesquest_fail_AI`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_AI_3, NPC_BEANIES_BEANIESQUEST_FAIL_AI_2, NPC_B...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_AirHorn`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_1, NPC_BEANIES_BEANIESQUEST_FAIL_AIRHOR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_AngryFace`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_2, NPC_BEANIES_BEANIESQUEST_FAIL_ANGR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_AnimalHands`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_1, NPC_BEANIES_BEANIESQUEST_FAIL_AN...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_BubbleBoy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_2, NPC_BEANIES_BEANIESQUEST_FAIL_BUBB...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_ChadImplant`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_3, NPC_BEANIES_BEANIESQUEST_FAIL_CH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_ChaosDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_1, NPC_BEANIES_BEANIESQUEST_FAIL_CH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_DimensionalDivider`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_3, NPC_BEANIES_BEANIESQUEST_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_DiseaseJar`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_3, NPC_BEANIES_BEANIESQUEST_FAIL_DIS...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_ExperimentalTreatment`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_3, NPC_BEANIES_BEANIESQUE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_FartFace`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_2, NPC_BEANIES_BEANIESQUEST_FAIL_FARTF...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_FigLeaf`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_1, NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_Generic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_1, NPC_BEANIES_BEANIESQUEST_FAIL_GENERI...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_GlassCannon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_1, NPC_BEANIES_BEANIESQUEST_FAIL_GL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_HardPill`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_1, NPC_BEANIES_BEANIESQUEST_FAIL_HARDP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_HiveMind`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_2, NPC_BEANIES_BEANIESQUEST_FAIL_HIVEM...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_MagicMirror`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_3, NPC_BEANIES_BEANIESQUEST_FAIL_MA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_MeStone`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_2, NPC_BEANIES_BEANIESQUEST_FAIL_MESTON...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_MultilinkCable`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 ||

</details>

---

### Object: `beaniesquest_fail_MysteriousDice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_MysteriousGlasses`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_3, NPC_BEANIES_BEANIESQUEST_F...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 ||

</details>

---

### Object: `beaniesquest_fail_NDEDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_2, NPC_BEANIES_BEANIESQUEST_FAIL_NDED...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_NuclearKnife`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_3, NPC_BEANIES_BEANIESQUEST_FAIL_N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_PartialLobotomy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_1, NPC_BEANIES_BEANIESQUEST_FAI...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `beaniesquest_fail_PartyDetonator`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_1, NPC_BEANIES_BEANIESQUEST_FAIL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_PersonalHeater`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_FAIL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_PersuasionDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_1, NPC_BEANIES_BEANIESQUEST_FA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_PrincessHat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_1, NPC_BEANIES_BEANIESQUEST_FAIL_PR...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 ||

</details>

---

### Object: `beaniesquest_fail_RealityScrambler`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_1, NPC_BEANIES_BEANIESQUEST_FA...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 ||

</details>

---

### Object: `beaniesquest_fail_Redacted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_1, NPC_BEANIES_BEANIESQUEST_FAIL_REDAC...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `beaniesquest_fail_SpiderInjector`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_Stopwatch`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_2, NPC_BEANIES_BEANIESQUEST_FAIL_STOP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_StorageLocker`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_3, NPC_BEANIES_BEANIESQUEST_FAIL_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_TheIOU`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_1, NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_TheLoner`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_3, NPC_BEANIES_BEANIESQUEST_FAIL_THELO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_Trapfest99`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_FAIL_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `set_state, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_fail_UltraVision3000`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_3, NPC_BEANIES_BEANIESQUEST_FAI...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 ||

</details>

---

### Object: `beaniesquest_intro_AI`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_AI_1, NPC_BEANIES_BEANIESQUEST_INTRO_AI_2, NPC...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_AirHorn`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_2, NPC_BEANIES_BEANIESQUEST_INTRO_AIRH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_AngryFace`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_2, NPC_BEANIES_BEANIESQUEST_INTRO_AN...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_AnimalHands`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_1, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_BubbleBoy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_1, NPC_BEANIES_BEANIESQUEST_INTRO_BU...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_ChadImplant`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_1, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_ChaosDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_3, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_DimensionalDivider`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_1, NPC_BEANIES_BEANIESQUEST...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_DiseaseJar`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_1, NPC_BEANIES_BEANIESQUEST_INTRO_D...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_ExperimentalTreatment`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_2, NPC_BEANIES_BEANIESQU...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||

</details>

---

### Object: `beaniesquest_intro_FartFace`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_1, NPC_BEANIES_BEANIESQUEST_INTRO_FAR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_FigLeaf`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_1, NPC_BEANIES_BEANIESQUEST_INTRO_FIGL...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_Generic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_1, NPC_BEANIES_BEANIESQUEST_INTRO_GENE...` | 1 ||

</details>

---

### Object: `beaniesquest_intro_GlassCannon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_2, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `beaniesquest_intro_HardPill`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_2, NPC_BEANIES_BEANIESQUEST_INTRO_HAR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_HiveMind`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_1, NPC_BEANIES_BEANIESQUEST_INTRO_HIV...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_MagicMirror`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_3, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_MeStone`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_1, NPC_BEANIES_BEANIESQUEST_INTRO_MEST...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||

</details>

---

### Object: `beaniesquest_intro_MultilinkCable`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_INT...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_MysteriousDice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_3, NPC_BEANIES_BEANIESQUEST_INT...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_MysteriousGlasses`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_1, NPC_BEANIES_BEANIESQUEST_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_NDEDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_2, NPC_BEANIES_BEANIESQUEST_INTRO_ND...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_NuclearKnife`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_3, NPC_BEANIES_BEANIESQUEST_INTRO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_PartialLobotomy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_3, NPC_BEANIES_BEANIESQUEST_IN...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_PartyDetonator`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_1, NPC_BEANIES_BEANIESQUEST_INT...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_PersonalHeater`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_INT...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_PersuasionDevice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_3, NPC_BEANIES_BEANIESQUEST_I...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_PrincessHat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_2, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_RealityScrambler`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_3, NPC_BEANIES_BEANIESQUEST_I...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `beaniesquest_intro_Redacted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_2, NPC_BEANIES_BEANIESQUEST_INTRO_RED...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_SpiderInjector`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_2, NPC_BEANIES_BEANIESQUEST_INT...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_Stopwatch`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_2, NPC_BEANIES_BEANIESQUEST_INTRO_ST...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_StorageLocker`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_2, NPC_BEANIES_BEANIESQUEST_INTR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `beaniesquest_intro_TheIOU`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_3, NPC_BEANIES_BEANIESQUEST_INTRO_THEIO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||

</details>

---

### Object: `beaniesquest_intro_TheLoner`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_2, NPC_BEANIES_BEANIESQUEST_INTRO_THE...` | 1 ||

</details>

---

### Object: `beaniesquest_intro_Trapfest99`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_INTRO_T...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||

</details>

---

### Object: `beaniesquest_intro_UltraVision3000`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_1, NPC_BEANIES_BEANIESQUEST_IN...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `boss_fight_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BOSS_FIGHT_INTRO_2, NPC_POPUP_BOSS_FIGHT_INTRO_1, NPC_POPUP_BOSS_FI...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.25, .5` | 1 ||

</details>

---

### Object: `boss_fight_round2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BOSS_FIGHT_ROUND2_1, NPC_POPUP_BOSS_FIGHT_ROUND2_3, NPC_POPUP_BOSS_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_turnorder, offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `butch_begin_accepting_cats`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_3, NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `butch` | 1 ||

</details>

---

### Object: `butch_boneyard_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_BONEYARD_INTRO_3, NPC_BUTCH_BUTCH_BONEYARD_INTRO_1, NPC_BUTCH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `butch_first_house_boss_beat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_2, NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `butch_pyro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_PYRO_2, NPC_BUTCH_BUTCH_PYRO_1, NPC_BUTCH_BUTCH_PYRO_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `butch_tina1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TINA1_3, NPC_BUTCH_BUTCH_TINA1_2, NPC_BUTCH_BUTCH_TINA1_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `butch_tips_backstab`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_BACKSTAB_1, NPC_BUTCH_BUTCH_TIPS_BACKSTAB_3, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_charisma`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_CHARISMA_1, NPC_BUTCH_BUTCH_TIPS_CHARISMA_2, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_combat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_COMBAT_1, NPC_BUTCH_BUTCH_TIPS_COMBAT_2, NPC_BUTCH_BUTCH...` | 1 ||

</details>

---

### Object: `butch_tips_disorders`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_DISORDERS_3, NPC_BUTCH_BUTCH_TIPS_DISORDERS_2, NPC_BUTCH...` | 1 ||

</details>

---

### Object: `butch_tips_drafting`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_DRAFTING_2, NPC_BUTCH_BUTCH_TIPS_DRAFTING_3, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_elements`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_1, NPC_BUTCH_BUTCH_TIPS_ELEMENTS_2, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_hard`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HARD_3, NPC_BUTCH_BUTCH_TIPS_HARD_1, NPC_BUTCH_BUTCH_TIP...` | 1 ||

</details>

---

### Object: `butch_tips_headhome`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HEADHOME_2, NPC_BUTCH_BUTCH_TIPS_HEADHOME_1, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_houseboss`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_3, NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_1, NPC_BUTCH...` | 1 ||

</details>

---

### Object: `butch_tips_info`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INFO_2, NPC_BUTCH_BUTCH_TIPS_INFO_1` | 1 ||

</details>

---

### Object: `butch_tips_intelligence`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_2, NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_3, NPC...` | 1 ||

</details>

---

### Object: `butch_tips_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INTRO_1, NPC_BUTCH_BUTCH_TIPS_INTRO_3, NPC_BUTCH_BUTCH_T...` | 1 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `butch_tips_intelligence` | 1 ||

</details>

---

### Object: `butch_tips_items`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_ITEMS_1, NPC_BUTCH_BUTCH_TIPS_ITEMS_2` | 1 ||

</details>

---

### Object: `butch_tips_lesscats`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_LESSCATS_2, NPC_BUTCH_BUTCH_TIPS_LESSCATS_1, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_magicdamage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_2, NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_1, NPC_B...` | 1 ||

</details>

---

### Object: `butch_tips_passives`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_PASSIVES_1, NPC_BUTCH_BUTCH_TIPS_PASSIVES_3, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_reorient`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_REORIENT_2, NPC_BUTCH_BUTCH_TIPS_REORIENT_1, NPC_BUTCH_B...` | 1 ||

</details>

---

### Object: `butch_tips_rewards`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_REWARDS_3, NPC_BUTCH_BUTCH_TIPS_REWARDS_2, NPC_BUTCH_BUT...` | 1 ||

</details>

---

### Object: `butch_tips_tacticalview`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_1, NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_2, NPC...` | 1 ||

</details>

---

### Object: `butch_tips_turnorder`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_TURNORDER_3, NPC_BUTCH_BUTCH_TIPS_TURNORDER_1, NPC_BUTCH...` | 1 ||

</details>

---

### Object: `butch_tips_wellrounded`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_3, NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_2, NPC_B...` | 1 ||

</details>

---

### Object: `can_still_use_attack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_1, NPC_POPUP_CAN_STILL_USE_ATTACK_2` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_3` | 1 ||
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `can_still_use_attack_didntspell` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `can_still_use_attack_didntspell`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_2` | 1 ||
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `can_still_use_attack` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `cant_afford_a`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_A_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `cant_afford_b`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_B_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `cant_afford_c`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_C_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `cant_afford_d`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_D_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `cant_afford_iceage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_ICEAGE_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `cant_afford_jurassic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_JURASSIC_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `cant_afford_moon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_MOON_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `cant_afford_theend`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_THEEND_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `class_unlock_butcher`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_2, NPC_BUTCH_CLASS_UNLOCK_BUTCHER_3, NPC_BUTCH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Butcher` | 1 ||

</details>

---

### Object: `class_unlock_druid`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_DRUID_1, NPC_BUTCH_CLASS_UNLOCK_DRUID_3, NPC_BUTCH_CLA...` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Druid` | 1 ||

</details>

---

### Object: `class_unlock_jester`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_JESTER_1, NPC_BUTCH_CLASS_UNLOCK_JESTER_3, NPC_BUTCH_C...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Jester` | 1 ||

</details>

---

### Object: `class_unlock_medic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_MEDIC_2, NPC_BUTCH_CLASS_UNLOCK_MEDIC_1, NPC_BUTCH_CLA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Medic` | 1 ||

</details>

---

### Object: `class_unlock_monk`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_MONK_3, NPC_BUTCH_CLASS_UNLOCK_MONK_1, NPC_BUTCH_CLASS...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Monk` | 1 ||

</details>

---

### Object: `class_unlock_necromancer`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_3, NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_2, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Necromancer` | 1 ||

</details>

---

### Object: `class_unlock_psychic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_3, NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_2, NPC_BUTCH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Psychic` | 1 ||

</details>

---

### Object: `class_unlock_thief`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_THIEF_2, NPC_BUTCH_CLASS_UNLOCK_THIEF_1, NPC_BUTCH_CLA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Thief` | 1 ||

</details>

---

### Object: `class_unlock_tinkerer`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_TINKERER_3, NPC_BUTCH_CLASS_UNLOCK_TINKERER_1, NPC_BUT...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Tinkerer` | 1 ||

</details>

---

### Object: `collected_new_items`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_3, NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle2, blocking` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_5` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `collected_nothing`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NOTHING_1, NPC_ORGANGRINDER_COLLECTED_NOTHING_3, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle2, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `do_not_end_turn`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `do_not_end_turn` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_DO_NOT_END_TURN_1` | 1 ||

</details>

---

### Object: `done_spitting_fail_ally`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_ALLY_2, NPC_POPUP_DONE_SPITTING_FAIL_ALLY_3, NPC...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `done_spitting_fail_miss`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_MISS_1, NPC_POPUP_DONE_SPITTING_FAIL_MISS_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `done_spitting_fail_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_RAT_1, NPC_POPUP_DONE_SPITTING_FAIL_RAT_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway` | 1 ||

</details>

---

### Object: `done_spitting_success`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_SUCCESS_2, NPC_POPUP_DONE_SPITTING_SUCCESS_3, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ending`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_ENDING_1, NPC_BEANIES_ENDING_2, NPC_BEANIES_ENDING_3` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `BeaniesEnding_Banging` | 1 ||
| [`screenshake`](./Arrays.md#array-screenshake) | Array | Examples: `[ 1 30 ]` | 1 ||

</details>

---

### Object: `finish_adventure`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FINISH_ADVENTURE_1, NPC_POPUP_FINISH_ADVENTURE_2, NPC_POPUP_FINISH_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, butch_point_food, butch_point_save` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `first_fight_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_FIGHT_INTRO_3, NPC_POPUP_FIRST_FIGHT_INTRO_2, NPC_POPUP_FIRST...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_team, butch_point_enemies` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected, cat_turn` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_FIRST_FIGHT_INTRO_14` | 1 ||
| [`set_mood`](./Enums.md#enum-set_mood) | Enum | Examples: `default` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `first_house_boss_tomorrow`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_3, NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_1,...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `first_house_hint_retired`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_2, NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_3, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `frank_caves_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_CAVES_INTRO_1, NPC_FRANK_FRANK_CAVES_INTRO_2, NPC_FRANK_FRANK...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup` | 1 ||

</details>

---

### Object: `frank_ending`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_ENDING_1, NPC_FRANK_FRANK_ENDING_2, NPC_FRANK_FRANK_ENDING_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||

</details>

---

### Object: `frank_max1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX1_2, NPC_FRANK_FRANK_MAX1_3, NPC_FRANK_FRANK_MAX1_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `frank_max2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX2_1, NPC_FRANK_FRANK_MAX2_3, NPC_FRANK_FRANK_MAX2_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `frank_max3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX3_3, NPC_FRANK_FRANK_MAX3_2, NPC_FRANK_FRANK_MAX3_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `frank_max4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX4_3, NPC_FRANK_FRANK_MAX4_1, NPC_FRANK_FRANK_MAX4_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `frank_max5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX5_1, NPC_FRANK_FRANK_MAX5_2, NPC_FRANK_FRANK_MAX5_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `frank_max_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX_INTRO_2, NPC_FRANK_FRANK_MAX_INTRO_3, NPC_FRANK_FRANK_MAX...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `frank_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ frank_max1 frank_max2 frank_max3 frank_max4 frank_max5 ]` | 1 ||

</details>

---

### Object: `frank_terminator2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TERMINATOR2_2, NPC_FRANK_FRANK_TERMINATOR2_3, NPC_FRANK_FRANK...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||

</details>

---

### Object: `frank_tips_1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_1_1, NPC_FRANK_FRANK_TIPS_1_2, NPC_FRANK_FRANK_TIPS_1_3` | 1 ||

</details>

---

### Object: `frank_tips_10`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_10_2, NPC_FRANK_FRANK_TIPS_10_1, NPC_FRANK_FRANK_TIPS_10_3` | 1 ||

</details>

---

### Object: `frank_tips_2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_2_1, NPC_FRANK_FRANK_TIPS_2_2, NPC_FRANK_FRANK_TIPS_2_3` | 1 ||

</details>

---

### Object: `frank_tips_3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_3_3, NPC_FRANK_FRANK_TIPS_3_2, NPC_FRANK_FRANK_TIPS_3_1` | 1 ||

</details>

---

### Object: `frank_tips_4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_4_3, NPC_FRANK_FRANK_TIPS_4_2, NPC_FRANK_FRANK_TIPS_4_1` | 1 ||

</details>

---

### Object: `frank_tips_5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_5_1, NPC_FRANK_FRANK_TIPS_5_3, NPC_FRANK_FRANK_TIPS_5_2` | 1 ||

</details>

---

### Object: `frank_tips_6`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_6_2, NPC_FRANK_FRANK_TIPS_6_1, NPC_FRANK_FRANK_TIPS_6_3` | 1 ||

</details>

---

### Object: `frank_tips_7`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_7_3, NPC_FRANK_FRANK_TIPS_7_2, NPC_FRANK_FRANK_TIPS_7_1` | 1 ||

</details>

---

### Object: `frank_tips_8`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_8_2, NPC_FRANK_FRANK_TIPS_8_1, NPC_FRANK_FRANK_TIPS_8_3` | 1 ||

</details>

---

### Object: `frank_tips_9`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_9_2, NPC_FRANK_FRANK_TIPS_9_1` | 1 ||

</details>

---

### Object: `gone`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `gone` | 1 ||

</details>

---

### Object: `house_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_INTRO_1, NPC_POPUP_HOUSE_INTRO_2, NPC_POPUP_HOUSE_INTRO_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_cats` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_HOUSE_INTRO_11` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click` | 1 ||

</details>

---

### Object: `house_kitten_box`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_KITTEN_BOX_2, NPC_POPUP_HOUSE_KITTEN_BOX_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `house_pass_day`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PASS_DAY_3, NPC_POPUP_HOUSE_PASS_DAY_1, NPC_POPUP_HOUSE_PASS_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_food` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `house_pass_day2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PASS_DAY2_3, NPC_POPUP_HOUSE_PASS_DAY2_1, NPC_POPUP_HOUSE_PAS...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `house_pipe`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PIPE_1, NPC_POPUP_HOUSE_PIPE_2, NPC_POPUP_HOUSE_PIPE_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `frank_right, offscreen, frank_point_pipe` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `house_retired_cat_box`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_RETIRED_CAT_BOX_1` | 1 ||

</details>

---

### Object: `house_starred_box`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_STARRED_BOX_1, NPC_POPUP_HOUSE_STARRED_BOX_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `house_strays`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_STRAYS_3, NPC_POPUP_HOUSE_STRAYS_2, NPC_POPUP_HOUSE_STRAYS_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_strays` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_HOUSE_STRAYS_5` | 1 ||
| [`request_cat_info`](./Enums.md#enum-request_cat_info) | Enum | Examples: `stray` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click` | 1 ||

</details>

---

### Object: `house_upgrade_4throom`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_4THROOM_3, NPC_FRANK_HOUSE_UPGRADE_4THROOM_2, NPC_FRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_attic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_ATTIC_3, NPC_FRANK_HOUSE_UPGRADE_ATTIC_2, NPC_FRANK_H...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_basement`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_basement2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT2_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_basement3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT3_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_basement4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT4_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_basement5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT5_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_largehouse`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_3, NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_1, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `house_upgrade_mediumhouse`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_2, NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_3,...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_INTRO_3, NPC_BEANIES_INTRO_1, NPC_BEANIES_INTRO_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`set_mood`](./Enums.md#enum-set_mood) | Enum | Examples: `veryhappy, happy, default` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `reject_cat, choose_cat2, choose_cat1` | 1 ||
| [`delay`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | Examples: `.05, 5.4` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_BEANIES_INTRO_15` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `Intro_LabDisposal` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `introduce_hard_path`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_INTRODUCE_HARD_PATH_1, NPC_POPUP_INTRODUCE_HARD_PATH_3, NPC_POPUP_I...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `jack_begin_accepting_cats`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_2, NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_3, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `jack` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_desert_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_DESERT_INTRO_1, NPC_JACK_JACK_DESERT_INTRO_3, NPC_JACK_JACK_DES...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `Jack_Gainaltfurniture`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_GAINALTFURNITURE_3, NPC_JACK_JACK_GAINALTFURNITURE_1, NPC_JACK_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_introduction`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_JACK_INTRODUCTION_2, NPC_POPUP_JACK_INTRODUCTION_3, NPC_POPUP_JACK_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `jack_point_furniture, offscreen, jack_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_JACK_INTRODUCTION_7` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `open_furniture` | 1 ||
| [`get_random_furniture_piece`](./Arrays.md#array-get_random_furniture_piece) | Array | Examples: `[ small_trash_cans small_trash_can2 ]` | 1 ||

</details>

---

### Object: `jack_max1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX1_3, NPC_JACK_JACK_MAX1_2, NPC_JACK_JACK_MAX1_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_max2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX2_2, NPC_JACK_JACK_MAX2_1, NPC_JACK_JACK_MAX2_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_max3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX3_1, NPC_JACK_JACK_MAX3_2, NPC_JACK_JACK_MAX3_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_max4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX4_1, NPC_JACK_JACK_MAX4_3, NPC_JACK_JACK_MAX4_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_max5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX5_2, NPC_JACK_JACK_MAX5_1, NPC_JACK_JACK_MAX5_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_max_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX_INTRO_3, NPC_JACK_JACK_MAX_INTRO_2, NPC_JACK_JACK_MAX_INTRO_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ jack_max1 jack_max2 jack_max3 jack_max4 jack_max5 ]` | 1 ||

</details>

---

### Object: `jack_shopupgrade1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE1_3, NPC_JACK_JACK_SHOPUPGRADE1_2, NPC_JACK_JACK_SHO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_shopupgrade2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE2_2, NPC_JACK_JACK_SHOPUPGRADE2_1, NPC_JACK_JACK_SHO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_shopupgrade3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE3_3, NPC_JACK_JACK_SHOPUPGRADE3_2, NPC_JACK_JACK_SHO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_shopupgrade4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE4_3, NPC_JACK_JACK_SHOPUPGRADE4_2, NPC_JACK_JACK_SHO...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `jack_zara`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_ZARA_3, NPC_JACK_JACK_ZARA_1, NPC_JACK_JACK_ZARA_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `level_up_didnt_select_sunburn`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_1, NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SU...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `level_up_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_INTRO_1, NPC_POPUP_LEVEL_UP_INTRO_2, NPC_POPUP_LEVEL_UP_IN...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_levelup, butch_point_hotblooded, butch_point_sunburn` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click, hovered_passive` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_LEVEL_UP_INTRO_6` | 1 ||
| `lock_mouse` | Number | Examples: `1` | 1 ||
| `unlock_mouse` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `level_up_selected_sunburn`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_2, NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_1,...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `low_on_food`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `tink_point_box, tink_left, tink_point_food` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LOW_ON_FOOD_3, NPC_POPUP_LOW_ON_FOOD_1, NPC_POPUP_LOW_ON_FOOD_2` | 1 ||

</details>

---

### Object: `map_click_node`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_mapnode, offscreen` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_CLICK_NODE_1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `mapnode_selected` | 1 ||

</details>

---

### Object: `map_equip_items`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, butch_point_inventory, offscreen` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS_2` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `inventory_selected` | 1 ||

</details>

---

### Object: `map_equip_items2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_point_inventory` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint` | 1 ||
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `map_equip_items2` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS2_1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `inventory_selected` | 1 ||

</details>

---

### Object: `melee_attack_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMoveHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_ATTACK_RAT_2, NPC_POPUP_MELEE_ATTACK_RAT_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_ATTACK_RAT_3` | 1 ||
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `ranged_cat_attack` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_cat_spit`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_spells` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_2, NPC_POPUP_MELEE_CAT_SPIT_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_3` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_cat_spit_fail_ally`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_2, NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_1, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_4` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_cat_spit_fail_miss`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_2, NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_3, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_4` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_cat_spit_fail_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_1, NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_2, NPC...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_4` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_cat_spit_ignore`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `melee_cat_spit_ignore` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_2` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_cat_spit_success`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_2, NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_3, NPC_P...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_4` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_killed_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_passives, butch_point_team_nocircle` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHintDelay1, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_KILLED_RAT_2, NPC_POPUP_MELEE_KILLED_RAT_1, NPC_POPUP_MELEE_K...` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click, hovered_passive` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_KILLED_RAT_3` | 1 ||
| `unlock_mouse` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `melee_move2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_move` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMoveHint, UISFX_ButchMove` | 1 ||
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `melee_move2` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_MOVE2_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_MOVE2_2` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `melee_out_of_actions`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHintDelay1, UISFX_ButchHint` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_mana, butch_point_cost, butch_point_spells` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_OUT_OF_ACTIONS_2, NPC_POPUP_MELEE_OUT_OF_ACTIONS_1, NPC_POPUP...` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_OUT_OF_ACTIONS_4` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `end_turn` | 1 ||

</details>

---

### Object: `new_adventure`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `tink_point_box, offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_NEW_ADVENTURE_2, NPC_POPUP_NEW_ADVENTURE_1` | 1 ||

</details>

---

### Object: `organ_boneyard_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_3, NPC_ORGANGRINDER_ORGAN_BONEYARD_INTR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_INTRO_1, NPC_ORGANGRINDER_ORGAN_INTRO_2, NPC_ORGANGRIN...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `organgrinder` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_INTRO_20` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| [`set_organ_name`](./Strings.md#string-set_organ_name) | String | Examples: `"Tyler"` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_max1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX1_1, NPC_ORGANGRINDER_ORGAN_MAX1_3, NPC_ORGANGRINDE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_max2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX2_1, NPC_ORGANGRINDER_ORGAN_MAX2_3, NPC_ORGANGRINDE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_max3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX3_3, NPC_ORGANGRINDER_ORGAN_MAX3_1, NPC_ORGANGRINDE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_max4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX4_2, NPC_ORGANGRINDER_ORGAN_MAX4_3, NPC_ORGANGRINDE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_max5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX5_1, NPC_ORGANGRINDER_ORGAN_MAX5_2, NPC_ORGANGRINDE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_max_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_3, NPC_ORGANGRINDER_ORGAN_MAX_INTRO_1, NPC_O...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ organ_max1 organ_max2 organ_max3 organ_max4 organ_max5 ]` | 1 ||

</details>

---

### Object: `organ_rename`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_RENAME_3, NPC_ORGANGRINDER_ORGAN_RENAME_1, NPC_ORGANGR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| [`set_organ_name`](./Strings.md#string-set_organ_name) | String | Examples: `"Tyler"` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_throbbingdomain_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_2, NPC_ORGANGRINDER_ORGAN_THROBB...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_tina3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_TINA3_1, NPC_ORGANGRINDER_ORGAN_TINA3_2, NPC_ORGANGRIN...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_unlock`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UNLOCK_1, NPC_ORGANGRINDER_ORGAN_UNLOCK_3, NPC_ORGANGR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_upgrade1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE1_3, NPC_ORGANGRINDER_ORGAN_UPGRADE1_1, NPC_ORG...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_upgrade2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE2_2, NPC_ORGANGRINDER_ORGAN_UPGRADE2_3, NPC_ORG...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_upgrade3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE3_1, NPC_ORGANGRINDER_ORGAN_UPGRADE3_2, NPC_ORG...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_upgrade4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE4_1, NPC_ORGANGRINDER_ORGAN_UPGRADE4_2, NPC_ORG...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_upgrade5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE5_1, NPC_ORGANGRINDER_ORGAN_UPGRADE5_3, NPC_ORG...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `organ_upgrade6`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE6_1, NPC_ORGANGRINDER_ORGAN_UPGRADE6_2, NPC_ORG...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_a`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_A_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_b`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_B_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_c`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_C_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_d`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_D_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_iceage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_ICEAGE_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_jurassic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_JURASSIC_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_moon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_MOON_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `purchase_item_theend`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_THEEND_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `ranged_attack_tomtom`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_attack_tomtom_fail_ally`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_ALLY_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_FA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_attack_tomtom_fail_miss`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_2, NPC_POPUP_RANGED_ATTACK_TOMTOM_FA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_attack_tomtom_fail_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_RAT_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_FAI...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_attack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ATTACK_1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `ranged_cat_early_attack2_ally`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_early_attack2_miss`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_early_attack2_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_early_attack_ally`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_A...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_early_attack_miss`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_M...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_early_attack_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_2, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_failmove`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_FAILMOVE_1, NPC_POPUP_RANGED_CAT_FAILMOVE_2, NPC_POPUP_R...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `ranged_cat_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_attack, butch_point_move` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_INTRO_3, NPC_POPUP_RANGED_CAT_INTRO_1, NPC_POPUP_RANGED_...` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_INTRO_4` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `ranged_cat_roll`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_cost2, butch_right, butch_point_spells` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchHintDelay2, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLL_1, NPC_POPUP_RANGED_CAT_ROLL_2, NPC_POPUP_RANGED_CA...` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLL_6` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `ranged_cat_rolled_first`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_3, NPC_POPUP_RANGED_CAT_ROLLED_FIRST_1, NPC...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_move` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_4` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `steven_100`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_100_2, NPC_STEVEN_STEVEN_100_1, NPC_STEVEN_STEVEN_100_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_introduction`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_INTRODUCTION_2, NPC_STEVEN_STEVEN_INTRODUCTION_3, NPC_STEVE...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 1 ||
| [`blocking`](./Enums.md#enum-blocking) | Boolean | Examples: `idlenoani` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_milliontrashed`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_MILLIONTRASHED_3, NPC_STEVEN_STEVEN_MILLIONTRASHED_1, NPC_S...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `steven_postendgame`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_POSTENDGAME_1, NPC_STEVEN_STEVEN_POSTENDGAME_2, NPC_STEVEN_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_resummon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_RESUMMON_1` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_savescum_1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_1alt1 steven_savescum_1alt2 steven_save...` | 1 ||

</details>

---

### Object: `steven_savescum_100`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_100_3, NPC_POPUP_STEVEN_SAVESCUM_100_2, NPC_POPUP_S...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_1alt1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_1ALT1_1, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_1alt2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_1, NPC_POPUP_STEVEN_SAVESCUM_1ALT2_2, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_1alt3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_2, NPC_POPUP_STEVEN_SAVESCUM_1ALT3_1, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_2alt1 steven_savescum_2alt2 steven_save...` | 1 ||

</details>

---

### Object: `steven_savescum_2alt1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_2ALT1_1, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_2alt2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_2, NPC_POPUP_STEVEN_SAVESCUM_2ALT2_3, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_2alt3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_3, NPC_POPUP_STEVEN_SAVESCUM_2ALT3_2, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_3alt1 steven_savescum_3alt2 steven_save...` | 1 ||

</details>

---

### Object: `steven_savescum_3alt1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT1_2, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_3alt2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT2_1, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_3alt3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT3_2, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_4alt1 steven_savescum_4alt2 steven_save...` | 1 ||

</details>

---

### Object: `steven_savescum_4alt1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT1_1, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_4alt2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT2_1, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_4alt3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT3_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT3_3, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_houseboss_1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_1, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 ||

</details>

---

### Object: `steven_savescum_houseboss_100`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_2, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOS...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 ||

</details>

---

### Object: `steven_savescum_houseboss_2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_3, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 ||

</details>

---

### Object: `steven_savescum_houseboss_3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_1, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 ||

</details>

---

### Object: `steven_savescum_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_INTRO_1, NPC_POPUP_STEVEN_SAVESCUM_INTRO_3, NPC_POP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 ||

</details>

---

### Object: `steven_savescum_intro_houseboss`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_3, NPC_POPUP_STEVEN_SAVESCUM_INTRO_...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 1 ||
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 ||

</details>

---

### Object: `steven_unlock_act1_crazy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_3, NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_2,...` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_unlock_act1_impossible`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_3, NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `talking, closeup, idle` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_unlock_act2_crazy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_1, NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_2,...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_unlock_act2_hard`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_3, NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_2, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_unlock_act2_impossible`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_2, NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, talking, idle` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_unlock_act3_crazy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_3, NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_2,...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_unlock_act3_hard`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_2, NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_1, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `steven_unlock_act3_impossible`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_3, NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `take_cats_inside`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `take_cats_inside` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TAKE_CATS_INSIDE_1` | 1 ||

</details>

---

### Object: `test_gamepad_prompts`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dialog` | Mixed | Examples: `"Switch to gamepad now if you wanna see gamepad bindings.", NPC_POPUP_FIRST_F...` | 1 ||

</details>

---

### Object: `tink_aggression`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_AGGRESSION_2, NPC_TINK_TINK_AGGRESSION_1, NPC_TINK_TINK_AGGRESS...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, zoomedout, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_basestats`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_BASESTATS_1, NPC_TINK_TINK_BASESTATS_2, NPC_TINK_TINK_BASESTATS_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_begin_accepting_cats`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_3, NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_2, N...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `tink` | 1 ||

</details>

---

### Object: `tink_inbreeding`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_INBREEDING_2, NPC_TINK_TINK_INBREEDING_3, NPC_TINK_TINK_INBREED...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX1_3, NPC_TINK_TINK_MAX1_1, NPC_TINK_TINK_MAX1_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max10`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX10_3, NPC_TINK_TINK_MAX10_1, NPC_TINK_TINK_MAX10_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX2_3, NPC_TINK_TINK_MAX2_2, NPC_TINK_TINK_MAX2_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX3_2, NPC_TINK_TINK_MAX3_3, NPC_TINK_TINK_MAX3_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX4_3, NPC_TINK_TINK_MAX4_2, NPC_TINK_TINK_MAX4_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX5_3, NPC_TINK_TINK_MAX5_1, NPC_TINK_TINK_MAX5_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max6`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX6_2, NPC_TINK_TINK_MAX6_1, NPC_TINK_TINK_MAX6_3` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max7`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX7_2, NPC_TINK_TINK_MAX7_3, NPC_TINK_TINK_MAX7_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `tink_max8`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX8_2, NPC_TINK_TINK_MAX8_1, NPC_TINK_TINK_MAX8_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max9`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX9_2, NPC_TINK_TINK_MAX9_1, NPC_TINK_TINK_MAX9_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX_INTRO_2, NPC_TINK_TINK_MAX_INTRO_3, NPC_TINK_TINK_MAX_INTRO_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ tink_max1 tink_max2 tink_max3 tink_max4 tink_max5 tink_...` | 1 ||

</details>

---

### Object: `tink_prettybow`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_PRETTYBOW_3, NPC_TINK_TINK_PRETTYBOW_2, NPC_TINK_TINK_PRETTYBOW_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_relationships`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_RELATIONSHIPS_3, NPC_TINK_TINK_RELATIONSHIPS_1, NPC_TINK_TINK_R...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_sexuality`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_SEXUALITY_2, NPC_TINK_TINK_SEXUALITY_3, NPC_TINK_TINK_SEXUALITY_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_tags`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TAGS_1, NPC_TINK_TINK_TAGS_2, NPC_TINK_TINK_TAGS_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `tink_terminator`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TERMINATOR_2, NPC_TINK_TINK_TERMINATOR_1, NPC_TINK_TINK_TERMINA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||

</details>

---

### Object: `tink_tina2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TINA2_2, NPC_TINK_TINK_TINA2_1, NPC_TINK_TINK_TINA2_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||

</details>

---

### Object: `tink_tips_appeal`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_APPEAL_3, NPC_TINK_TINK_TIPS_APPEAL_2, NPC_TINK_TINK_TIPS_...` | 1 ||

</details>

---

### Object: `tink_tips_basestats`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_BASESTATS_2, NPC_TINK_TINK_TIPS_BASESTATS_1, NPC_TINK_TINK...` | 1 ||

</details>

---

### Object: `tink_tips_cleaning`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_CLEANING_2, NPC_TINK_TINK_TIPS_CLEANING_1, NPC_TINK_TINK_T...` | 1 ||

</details>

---

### Object: `tink_tips_comfort`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_COMFORT_3, NPC_TINK_TINK_TIPS_COMFORT_2, NPC_TINK_TINK_TIP...` | 1 ||

</details>

---

### Object: `tink_tips_health`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_HEALTH_1, NPC_TINK_TINK_TIPS_HEALTH_3, NPC_TINK_TINK_TIPS_...` | 1 ||

</details>

---

### Object: `tink_tips_inbreeding`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_INBREEDING_1, NPC_TINK_TINK_TIPS_INBREEDING_2, NPC_TINK_TI...` | 1 ||

</details>

---

### Object: `tink_tips_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_INTRO_3, NPC_TINK_TINK_TIPS_INTRO_1, NPC_TINK_TINK_TIPS_IN...` | 1 ||
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `tink_tips_comfort` | 1 ||

</details>

---

### Object: `tink_tips_multiclassing`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_MULTICLASSING_3, NPC_TINK_TINK_TIPS_MULTICLASSING_2, NPC_T...` | 1 ||

</details>

---

### Object: `tink_tips_mutation`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_MUTATION_2, NPC_TINK_TINK_TIPS_MUTATION_1, NPC_TINK_TINK_T...` | 1 ||

</details>

---

### Object: `tink_tips_stimulation`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_STIMULATION_3, NPC_TINK_TINK_TIPS_STIMULATION_2, NPC_TINK_...` | 1 ||

</details>

---

### Object: `tracy_blankcollar1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR1_1, NPC_TRACY_TRACY_BLANKCOLLAR1_3, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_blankcollar2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR2_1, NPC_TRACY_TRACY_BLANKCOLLAR2_3, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_blankcollar3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR3_2, NPC_TRACY_TRACY_BLANKCOLLAR3_3, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodbonus1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODBONUS1_2, NPC_TRACY_TRACY_FOODBONUS1_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE1_3, NPC_TRACY_TRACY_FOODSTORAGE1_1, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage10`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE10_2, NPC_TRACY_TRACY_FOODSTORAGE10_1, NPC_TRACY_T...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE2_3, NPC_TRACY_TRACY_FOODSTORAGE2_2, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE3_1, NPC_TRACY_TRACY_FOODSTORAGE3_2, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE4_3, NPC_TRACY_TRACY_FOODSTORAGE4_1, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE5_1, NPC_TRACY_TRACY_FOODSTORAGE5_3, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage6`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE6_1, NPC_TRACY_TRACY_FOODSTORAGE6_2, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage7`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE7_2, NPC_TRACY_TRACY_FOODSTORAGE7_3, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage8`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE8_2, NPC_TRACY_TRACY_FOODSTORAGE8_1, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_foodstorage9`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE9_3, NPC_TRACY_TRACY_FOODSTORAGE9_2, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_idol1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL1_3, NPC_TRACY_TRACY_IDOL1_2, NPC_TRACY_TRACY_IDOL1_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_idol2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL2_3, NPC_TRACY_TRACY_IDOL2_1, NPC_TRACY_TRACY_IDOL2_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_idol3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL3_2, NPC_TRACY_TRACY_IDOL3_1, NPC_TRACY_TRACY_IDOL3_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_idol4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL4_2, NPC_TRACY_TRACY_IDOL4_3, NPC_TRACY_TRACY_IDOL4_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_idol5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL5_3, NPC_TRACY_TRACY_IDOL5_2, NPC_TRACY_TRACY_IDOL5_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_idol6`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL6_1, NPC_TRACY_TRACY_IDOL6_3, NPC_TRACY_TRACY_IDOL6_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_idol7`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL7_1, NPC_TRACY_TRACY_IDOL7_3, NPC_TRACY_TRACY_IDOL7_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_introduction`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_INTRODUCTION_3, NPC_TRACY_TRACY_INTRODUCTION_2, NPC_TRACY_TRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `tracy` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_kaijufight`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_KAIJUFIGHT_2, NPC_TRACY_TRACY_KAIJUFIGHT_1, NPC_TRACY_TRACY_K...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_max1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX1_2, NPC_TRACY_TRACY_MAX1_1, NPC_TRACY_TRACY_MAX1_3` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_max2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX2_3, NPC_TRACY_TRACY_MAX2_2, NPC_TRACY_TRACY_MAX2_1` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_max3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX3_2, NPC_TRACY_TRACY_MAX3_1, NPC_TRACY_TRACY_MAX3_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_max4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX4_3, NPC_TRACY_TRACY_MAX4_2, NPC_TRACY_TRACY_MAX4_1` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_max5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX5_1, NPC_TRACY_TRACY_MAX5_2, NPC_TRACY_TRACY_MAX5_3` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_max_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX_INTRO_2, NPC_TRACY_TRACY_MAX_INTRO_1, NPC_TRACY_TRACY_MAX...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, zoomedout, blocking` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| `lock_controls` | Number | Examples: `1` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `tracy_max_repeating`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ tracy_max1 tracy_max2 tracy_max3 tracy_max4 tracy_max5 ]` | 1 ||

</details>

---

### Object: `try_again_attack_rat`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_1, NPC_POPUP_TRY_AGAIN_ATTACK_RAT_3, NPC_POPUP...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHintDelay1, UISFX_ButchMove` | 1 ||
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `try_again_attack_rat` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_4` | 1 ||
| [`reset_turn`](./Enums.md#enum-reset_turn) | Enum | Examples: `act` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `try_again_melee_move`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_MELEE_MOVE_1, NPC_POPUP_TRY_AGAIN_MELEE_MOVE_2` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMove` | 1 ||
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `try_again_melee_move` | 1 ||
| [`reset_turn`](./Enums.md#enum-reset_turn) | Enum | Examples: `both` | 1 ||

</details>

---

### Object: `tutorial_cat_dies`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TUTORIAL_CAT_DIES_1, NPC_POPUP_TUTORIAL_CAT_DIES_3, NPC_POPUP_TUTOR...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 1 ||

</details>

---

### Object: `unprompted1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED1_1` | 1 ||

</details>

---

### Object: `unprompted2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED2_1, NPC_BEANIES_UNPROMPTED2_2` | 1 ||

</details>

---

### Object: `unprompted3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED3_2, NPC_BEANIES_UNPROMPTED3_1, NPC_BEANIES_UNPROMPTED3_3` | 1 ||

</details>

---

### Object: `unprompted4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED4_1` | 1 ||

</details>

---

### Object: `unprompted5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED5_1, NPC_BEANIES_UNPROMPTED5_2` | 1 ||

</details>

---

### Object: `unprompted6`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED6_2, NPC_BEANIES_UNPROMPTED6_3, NPC_BEANIES_UNPROMPTED6_1` | 1 ||

</details>

---

### Object: `upgrade_storage_1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_1_3, NPC_BUTCH_UPGRADE_STORAGE_1_2, NPC_BUTCH_UPGRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_2_2, NPC_BUTCH_UPGRADE_STORAGE_2_1, NPC_BUTCH_UPGRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_3_1, NPC_BUTCH_UPGRADE_STORAGE_3_3, NPC_BUTCH_UPGRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_4_1, NPC_BUTCH_UPGRADE_STORAGE_4_3, NPC_BUTCH_UPGRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_5_2, NPC_BUTCH_UPGRADE_STORAGE_5_1, NPC_BUTCH_UPGRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_6`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_6_2, NPC_BUTCH_UPGRADE_STORAGE_6_3, NPC_BUTCH_UPGRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_7`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_7_2, NPC_BUTCH_UPGRADE_STORAGE_7_3, NPC_BUTCH_UPGRA...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_max1`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX1_3, NPC_BUTCH_UPGRADE_STORAGE_MAX1_2, NPC_BUTCH...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 ||

</details>

---

### Object: `upgrade_storage_max2`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX2_2, NPC_BUTCH_UPGRADE_STORAGE_MAX2_3, NPC_BUTCH...` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_max3`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX3_2, NPC_BUTCH_UPGRADE_STORAGE_MAX3_3, NPC_BUTCH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_max4`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX4_3, NPC_BUTCH_UPGRADE_STORAGE_MAX4_2, NPC_BUTCH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_max5`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX5_3, NPC_BUTCH_UPGRADE_STORAGE_MAX5_2, NPC_BUTCH...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_repeating_crazy`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 ||

</details>

---

### Object: `upgrade_storage_repeating_hard`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 ||

</details>

---

### Object: `upgrade_storage_repeating_impossible`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 ||

</details>

---

### Object: `upgrade_storage_repeating_intro`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_3, NPC_BUTCH_UPGRADE_STORAGE_REPEAT...` | 1 ||
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 1 ||
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 ||

</details>

---

### Object: `upgrade_storage_repeating_normal`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 ||

</details>

---

### Object: `use_attack_after_used_weapon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_attack, butch_point_weapon` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_1, NPC_POPUP_USE_ATTACK_AFTER_USED_WEA...` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_3` | 1 ||
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `use_weapon` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `use_weapon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_weapon` | 1 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_USE_WEAPON_2, NPC_POPUP_USE_WEAPON_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_USE_WEAPON_3` | 1 ||
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `use_attack_after_used_weapon` | 1 ||
| `unlock_controls` | Number | Examples: `1` | 1 ||
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 ||

</details>

---

### Object: `welcome`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_boneyard`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BONEYARD_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BONEYARD_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_bunker`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BUNKER_2, NPC_TRACY_SHOP_WELCOME_BUNKER_1` | 1 ||
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BUNKER_3` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_caves`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CAVES_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CAVES_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_core`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CORE_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_crater`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CRATER_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CRATER_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_desert`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_DESERT_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_future`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_FUTURE_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_iceage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_ICEAGE_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_ICEAGE_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_junkyard`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JUNKYARD_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_jurassic`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JURASSIC_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JURASSIC_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_lab`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_LAB_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_LAB_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_moon`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_MOON_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_sewers`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_SEWERS_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_SEWERS_2` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_theend`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_THEEND_1` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_THEEND_2` | 1 ||
| [`set_npc_voice`](./Enums.md#enum-set_npc_voice) | Enum | Examples: `beanies` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_water`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_WATER_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

### Object: `welcome_water_cheap`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 ||
| [`delay`](./Enums.md#enum-delay) | Number | Examples: `.5` | 1 ||
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_WATER_CHEAP_1` | 1 ||
| `wait_for_cancel` | Number | Examples: `1` | 1 ||

</details>

---

