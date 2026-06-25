# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## NPC Scripts


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`states`](./NPC_Scripts.md#context-states) | Object | Examples: `{ ... }` | 24 |
| [`transitions`](./NPC_Scripts.md#context-transitions) | Object | Examples: `{ ... }` | 24 |
| [`unprompted`](./NPC_Scripts.md#context-unprompted) | Object | Examples: `{ ... }` | 18 |
| [`also`](./NPC_Scripts.md#context-also) | Object | Examples: `{ ... }` | 16 |
| [`unknown`](./NPC_Scripts.md#context-unknown) | Object | Examples: `{ ... }` | 16 |
| [`hide_text`](./NPC_Scripts.md#context-hide_text) | Object | Examples: `{ ... }` | 8 |
| [`purchase_item`](./NPC_Scripts.md#context-purchase_item) | Object | Examples: `{ ... }` | 8 |
| [`tooltip`](./NPC_Scripts.md#context-tooltip) | Object | Examples: `{ ... }` | 165 |
| [`unprompted_a`](./NPC_Scripts.md#context-unprompted_a) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_b`](./NPC_Scripts.md#context-unprompted_b) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_c`](./NPC_Scripts.md#context-unprompted_c) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_d`](./NPC_Scripts.md#context-unprompted_d) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_e`](./NPC_Scripts.md#context-unprompted_e) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_f`](./NPC_Scripts.md#context-unprompted_f) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_g`](./NPC_Scripts.md#context-unprompted_g) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_h`](./NPC_Scripts.md#context-unprompted_h) | Object | Examples: `{ ... }` | 8 |
| [`unprompted_i`](./NPC_Scripts.md#context-unprompted_i) | Object | Examples: `{ ... }` | 8 |
| [`cant_afford`](./NPC_Scripts.md#context-cant_afford) | Object | Examples: `{ ... }` | 6 |
| [`forward_to_tips`](./NPC_Scripts.md#context-forward_to_tips) | Object | Examples: `{ ... }` | 6 |
| [`out_of_stock`](./NPC_Scripts.md#context-out_of_stock) | Object | Examples: `{ ... }` | 6 |
| [`beanies_begin_accepting_cats`](./NPC_Scripts.md#context-beanies_begin_accepting_cats) | Object | Examples: `{ ... }` | 2 |
| [`beanies_bombquest_2`](./NPC_Scripts.md#context-beanies_bombquest_2) | Object | Examples: `{ ... }` | 8 |
| [`beanies_bombquest_3`](./NPC_Scripts.md#context-beanies_bombquest_3) | Object | Examples: `{ ... }` | 6 |
| [`beanies_bombquest_amnesia`](./NPC_Scripts.md#context-beanies_bombquest_amnesia) | Object | Examples: `{ ... }` | 4 |
| [`beanies_bombquest_begin`](./NPC_Scripts.md#context-beanies_bombquest_begin) | Object | Examples: `{ ... }` | 4 |
| [`beanies_bombquest_fail_jarofblood`](./NPC_Scripts.md#context-beanies_bombquest_fail_jarofblood) | Object | Examples: `{ ... }` | 6 |
| [`beanies_bombquest_fail_jarofchaos`](./NPC_Scripts.md#context-beanies_bombquest_fail_jarofchaos) | Object | Examples: `{ ... }` | 6 |
| [`beanies_bombquest_fail_jarofradiation`](./NPC_Scripts.md#context-beanies_bombquest_fail_jarofradiation) | Object | Examples: `{ ... }` | 4 |
| [`beanies_bombquest_fail_nuke`](./NPC_Scripts.md#context-beanies_bombquest_fail_nuke) | Object | Examples: `{ ... }` | 4 |
| [`beanies_future_intro`](./NPC_Scripts.md#context-beanies_future_intro) | Object | Examples: `{ ... }` | 4 |
| [`beanies_hitler3`](./NPC_Scripts.md#context-beanies_hitler3) | Object | Examples: `{ ... }` | 2 |
| [`beanies_hitler3_defeat`](./NPC_Scripts.md#context-beanies_hitler3_defeat) | Object | Examples: `{ ... }` | 2 |
| [`beanies_iloveyou`](./NPC_Scripts.md#context-beanies_iloveyou) | Object | Examples: `{ ... }` | 2 |
| [`beanies_infinite_intro`](./NPC_Scripts.md#context-beanies_infinite_intro) | Object | Examples: `{ ... }` | 2 |
| [`beanies_jurassic_intro`](./NPC_Scripts.md#context-beanies_jurassic_intro) | Object | Examples: `{ ... }` | 4 |
| [`beanies_lab_intro`](./NPC_Scripts.md#context-beanies_lab_intro) | Object | Examples: `{ ... }` | 4 |
| [`beanies_quest_complete`](./NPC_Scripts.md#context-beanies_quest_complete) | Object | Examples: `{ ... }` | 2 |
| [`beanies_quest_fail`](./NPC_Scripts.md#context-beanies_quest_fail) | Object | Examples: `{ ... }` | 2 |
| [`beanies_quests_intro`](./NPC_Scripts.md#context-beanies_quests_intro) | Object | Examples: `{ ... }` | 4 |
| [`beanies_quests_repeat`](./NPC_Scripts.md#context-beanies_quests_repeat) | Object | Examples: `{ ... }` | 4 |
| [`beanies_rift_intro`](./NPC_Scripts.md#context-beanies_rift_intro) | Object | Examples: `{ ... }` | 2 |
| [`beanies_screenshake_test`](./NPC_Scripts.md#context-beanies_screenshake_test) | Object | Examples: `{ ... }` | 2 |
| [`beanies_seefuture`](./NPC_Scripts.md#context-beanies_seefuture) | Object | Examples: `{ ... }` | 2 |
| [`beanies_seetheend`](./NPC_Scripts.md#context-beanies_seetheend) | Object | Examples: `{ ... }` | 2 |
| [`beanies_terminator1_defeat`](./NPC_Scripts.md#context-beanies_terminator1_defeat) | Object | Examples: `{ ... }` | 2 |
| [`beanies_terminator2_defeat`](./NPC_Scripts.md#context-beanies_terminator2_defeat) | Object | Examples: `{ ... }` | 2 |
| [`beanies_theend_intro`](./NPC_Scripts.md#context-beanies_theend_intro) | Object | Examples: `{ ... }` | 4 |
| [`beanies_timemachine_2`](./NPC_Scripts.md#context-beanies_timemachine_2) | Object | Examples: `{ ... }` | 2 |
| [`beanies_timemachine_intro`](./NPC_Scripts.md#context-beanies_timemachine_intro) | Object | Examples: `{ ... }` | 2 |
| [`beanies_vscreator1`](./NPC_Scripts.md#context-beanies_vscreator1) | Object | Examples: `{ ... }` | 2 |
| [`beanies_vscreator2`](./NPC_Scripts.md#context-beanies_vscreator2) | Object | Examples: `{ ... }` | 2 |
| [`beanies_vscreator3`](./NPC_Scripts.md#context-beanies_vscreator3) | Object | Examples: `{ ... }` | 2 |
| [`beanies_vscreator4`](./NPC_Scripts.md#context-beanies_vscreator4) | Object | Examples: `{ ... }` | 2 |
| [`beanies_vscreatorintro`](./NPC_Scripts.md#context-beanies_vscreatorintro) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_AI`](./NPC_Scripts.md#context-beaniesquest_complete_ai) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_AirHorn`](./NPC_Scripts.md#context-beaniesquest_complete_airhorn) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_AngryFace`](./NPC_Scripts.md#context-beaniesquest_complete_angryface) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_AnimalHands`](./NPC_Scripts.md#context-beaniesquest_complete_animalhands) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_BubbleBoy`](./NPC_Scripts.md#context-beaniesquest_complete_bubbleboy) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_ChadImplant`](./NPC_Scripts.md#context-beaniesquest_complete_chadimplant) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_ChaosDevice`](./NPC_Scripts.md#context-beaniesquest_complete_chaosdevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_DimensionalDivider`](./NPC_Scripts.md#context-beaniesquest_complete_dimensionaldivider) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_DiseaseJar`](./NPC_Scripts.md#context-beaniesquest_complete_diseasejar) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_ExperimentalTreatment`](./NPC_Scripts.md#context-beaniesquest_complete_experimentaltreatment) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_FartFace`](./NPC_Scripts.md#context-beaniesquest_complete_fartface) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_FigLeaf`](./NPC_Scripts.md#context-beaniesquest_complete_figleaf) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_Generic`](./NPC_Scripts.md#context-beaniesquest_complete_generic) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_GlassCannon`](./NPC_Scripts.md#context-beaniesquest_complete_glasscannon) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_HardPill`](./NPC_Scripts.md#context-beaniesquest_complete_hardpill) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_HiveMind`](./NPC_Scripts.md#context-beaniesquest_complete_hivemind) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_MagicMirror`](./NPC_Scripts.md#context-beaniesquest_complete_magicmirror) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_MeStone`](./NPC_Scripts.md#context-beaniesquest_complete_mestone) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_MultilinkCable`](./NPC_Scripts.md#context-beaniesquest_complete_multilinkcable) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_MysteriousDice`](./NPC_Scripts.md#context-beaniesquest_complete_mysteriousdice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_MysteriousGlasses`](./NPC_Scripts.md#context-beaniesquest_complete_mysteriousglasses) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_NDEDevice`](./NPC_Scripts.md#context-beaniesquest_complete_ndedevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_NuclearKnife`](./NPC_Scripts.md#context-beaniesquest_complete_nuclearknife) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_PartialLobotomy`](./NPC_Scripts.md#context-beaniesquest_complete_partiallobotomy) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_PartyDetonator`](./NPC_Scripts.md#context-beaniesquest_complete_partydetonator) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_PersonalHeater`](./NPC_Scripts.md#context-beaniesquest_complete_personalheater) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_PersuasionDevice`](./NPC_Scripts.md#context-beaniesquest_complete_persuasiondevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_PrincessHat`](./NPC_Scripts.md#context-beaniesquest_complete_princesshat) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_RealityScrambler`](./NPC_Scripts.md#context-beaniesquest_complete_realityscrambler) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_Redacted`](./NPC_Scripts.md#context-beaniesquest_complete_redacted) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_SpiderInjector`](./NPC_Scripts.md#context-beaniesquest_complete_spiderinjector) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_Stopwatch`](./NPC_Scripts.md#context-beaniesquest_complete_stopwatch) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_StorageLocker`](./NPC_Scripts.md#context-beaniesquest_complete_storagelocker) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_TheIOU`](./NPC_Scripts.md#context-beaniesquest_complete_theiou) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_TheLoner`](./NPC_Scripts.md#context-beaniesquest_complete_theloner) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_Trapfest99`](./NPC_Scripts.md#context-beaniesquest_complete_trapfest99) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_complete_UltraVision3000`](./NPC_Scripts.md#context-beaniesquest_complete_ultravision3000) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_AI`](./NPC_Scripts.md#context-beaniesquest_fail_ai) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_AirHorn`](./NPC_Scripts.md#context-beaniesquest_fail_airhorn) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_AngryFace`](./NPC_Scripts.md#context-beaniesquest_fail_angryface) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_AnimalHands`](./NPC_Scripts.md#context-beaniesquest_fail_animalhands) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_BubbleBoy`](./NPC_Scripts.md#context-beaniesquest_fail_bubbleboy) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_ChadImplant`](./NPC_Scripts.md#context-beaniesquest_fail_chadimplant) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_ChaosDevice`](./NPC_Scripts.md#context-beaniesquest_fail_chaosdevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_DimensionalDivider`](./NPC_Scripts.md#context-beaniesquest_fail_dimensionaldivider) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_DiseaseJar`](./NPC_Scripts.md#context-beaniesquest_fail_diseasejar) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_ExperimentalTreatment`](./NPC_Scripts.md#context-beaniesquest_fail_experimentaltreatment) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_FartFace`](./NPC_Scripts.md#context-beaniesquest_fail_fartface) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_FigLeaf`](./NPC_Scripts.md#context-beaniesquest_fail_figleaf) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_Generic`](./NPC_Scripts.md#context-beaniesquest_fail_generic) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_GlassCannon`](./NPC_Scripts.md#context-beaniesquest_fail_glasscannon) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_HardPill`](./NPC_Scripts.md#context-beaniesquest_fail_hardpill) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_HiveMind`](./NPC_Scripts.md#context-beaniesquest_fail_hivemind) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_MagicMirror`](./NPC_Scripts.md#context-beaniesquest_fail_magicmirror) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_MeStone`](./NPC_Scripts.md#context-beaniesquest_fail_mestone) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_MultilinkCable`](./NPC_Scripts.md#context-beaniesquest_fail_multilinkcable) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_MysteriousDice`](./NPC_Scripts.md#context-beaniesquest_fail_mysteriousdice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_MysteriousGlasses`](./NPC_Scripts.md#context-beaniesquest_fail_mysteriousglasses) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_NDEDevice`](./NPC_Scripts.md#context-beaniesquest_fail_ndedevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_NuclearKnife`](./NPC_Scripts.md#context-beaniesquest_fail_nuclearknife) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_PartialLobotomy`](./NPC_Scripts.md#context-beaniesquest_fail_partiallobotomy) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_PartyDetonator`](./NPC_Scripts.md#context-beaniesquest_fail_partydetonator) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_PersonalHeater`](./NPC_Scripts.md#context-beaniesquest_fail_personalheater) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_PersuasionDevice`](./NPC_Scripts.md#context-beaniesquest_fail_persuasiondevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_PrincessHat`](./NPC_Scripts.md#context-beaniesquest_fail_princesshat) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_RealityScrambler`](./NPC_Scripts.md#context-beaniesquest_fail_realityscrambler) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_Redacted`](./NPC_Scripts.md#context-beaniesquest_fail_redacted) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_SpiderInjector`](./NPC_Scripts.md#context-beaniesquest_fail_spiderinjector) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_Stopwatch`](./NPC_Scripts.md#context-beaniesquest_fail_stopwatch) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_StorageLocker`](./NPC_Scripts.md#context-beaniesquest_fail_storagelocker) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_TheIOU`](./NPC_Scripts.md#context-beaniesquest_fail_theiou) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_TheLoner`](./NPC_Scripts.md#context-beaniesquest_fail_theloner) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_Trapfest99`](./NPC_Scripts.md#context-beaniesquest_fail_trapfest99) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_fail_UltraVision3000`](./NPC_Scripts.md#context-beaniesquest_fail_ultravision3000) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_AI`](./NPC_Scripts.md#context-beaniesquest_intro_ai) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_AirHorn`](./NPC_Scripts.md#context-beaniesquest_intro_airhorn) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_AngryFace`](./NPC_Scripts.md#context-beaniesquest_intro_angryface) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_AnimalHands`](./NPC_Scripts.md#context-beaniesquest_intro_animalhands) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_BubbleBoy`](./NPC_Scripts.md#context-beaniesquest_intro_bubbleboy) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_ChadImplant`](./NPC_Scripts.md#context-beaniesquest_intro_chadimplant) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_ChaosDevice`](./NPC_Scripts.md#context-beaniesquest_intro_chaosdevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_DimensionalDivider`](./NPC_Scripts.md#context-beaniesquest_intro_dimensionaldivider) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_DiseaseJar`](./NPC_Scripts.md#context-beaniesquest_intro_diseasejar) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_ExperimentalTreatment`](./NPC_Scripts.md#context-beaniesquest_intro_experimentaltreatment) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_FartFace`](./NPC_Scripts.md#context-beaniesquest_intro_fartface) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_FigLeaf`](./NPC_Scripts.md#context-beaniesquest_intro_figleaf) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_Generic`](./NPC_Scripts.md#context-beaniesquest_intro_generic) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_GlassCannon`](./NPC_Scripts.md#context-beaniesquest_intro_glasscannon) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_HardPill`](./NPC_Scripts.md#context-beaniesquest_intro_hardpill) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_HiveMind`](./NPC_Scripts.md#context-beaniesquest_intro_hivemind) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_MagicMirror`](./NPC_Scripts.md#context-beaniesquest_intro_magicmirror) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_MeStone`](./NPC_Scripts.md#context-beaniesquest_intro_mestone) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_MultilinkCable`](./NPC_Scripts.md#context-beaniesquest_intro_multilinkcable) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_MysteriousDice`](./NPC_Scripts.md#context-beaniesquest_intro_mysteriousdice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_MysteriousGlasses`](./NPC_Scripts.md#context-beaniesquest_intro_mysteriousglasses) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_NDEDevice`](./NPC_Scripts.md#context-beaniesquest_intro_ndedevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_NuclearKnife`](./NPC_Scripts.md#context-beaniesquest_intro_nuclearknife) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_PartialLobotomy`](./NPC_Scripts.md#context-beaniesquest_intro_partiallobotomy) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_PartyDetonator`](./NPC_Scripts.md#context-beaniesquest_intro_partydetonator) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_PersonalHeater`](./NPC_Scripts.md#context-beaniesquest_intro_personalheater) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_PersuasionDevice`](./NPC_Scripts.md#context-beaniesquest_intro_persuasiondevice) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_PrincessHat`](./NPC_Scripts.md#context-beaniesquest_intro_princesshat) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_RealityScrambler`](./NPC_Scripts.md#context-beaniesquest_intro_realityscrambler) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_Redacted`](./NPC_Scripts.md#context-beaniesquest_intro_redacted) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_SpiderInjector`](./NPC_Scripts.md#context-beaniesquest_intro_spiderinjector) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_Stopwatch`](./NPC_Scripts.md#context-beaniesquest_intro_stopwatch) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_StorageLocker`](./NPC_Scripts.md#context-beaniesquest_intro_storagelocker) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_TheIOU`](./NPC_Scripts.md#context-beaniesquest_intro_theiou) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_TheLoner`](./NPC_Scripts.md#context-beaniesquest_intro_theloner) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_Trapfest99`](./NPC_Scripts.md#context-beaniesquest_intro_trapfest99) | Object | Examples: `{ ... }` | 2 |
| [`beaniesquest_intro_UltraVision3000`](./NPC_Scripts.md#context-beaniesquest_intro_ultravision3000) | Object | Examples: `{ ... }` | 2 |
| [`boss_fight_intro`](./NPC_Scripts.md#context-boss_fight_intro) | Object | Examples: `{ ... }` | 2 |
| [`boss_fight_round2`](./NPC_Scripts.md#context-boss_fight_round2) | Object | Examples: `{ ... }` | 2 |
| [`butch_begin_accepting_cats`](./NPC_Scripts.md#context-butch_begin_accepting_cats) | Object | Examples: `{ ... }` | 2 |
| [`butch_boneyard_intro`](./NPC_Scripts.md#context-butch_boneyard_intro) | Object | Examples: `{ ... }` | 4 |
| [`butch_first_house_boss_beat`](./NPC_Scripts.md#context-butch_first_house_boss_beat) | Object | Examples: `{ ... }` | 2 |
| [`butch_pyro`](./NPC_Scripts.md#context-butch_pyro) | Object | Examples: `{ ... }` | 2 |
| [`butch_tina1`](./NPC_Scripts.md#context-butch_tina1) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_backstab`](./NPC_Scripts.md#context-butch_tips_backstab) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_charisma`](./NPC_Scripts.md#context-butch_tips_charisma) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_combat`](./NPC_Scripts.md#context-butch_tips_combat) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_disorders`](./NPC_Scripts.md#context-butch_tips_disorders) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_drafting`](./NPC_Scripts.md#context-butch_tips_drafting) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_elements`](./NPC_Scripts.md#context-butch_tips_elements) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_hard`](./NPC_Scripts.md#context-butch_tips_hard) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_headhome`](./NPC_Scripts.md#context-butch_tips_headhome) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_houseboss`](./NPC_Scripts.md#context-butch_tips_houseboss) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_info`](./NPC_Scripts.md#context-butch_tips_info) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_intelligence`](./NPC_Scripts.md#context-butch_tips_intelligence) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_intro`](./NPC_Scripts.md#context-butch_tips_intro) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_items`](./NPC_Scripts.md#context-butch_tips_items) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_lesscats`](./NPC_Scripts.md#context-butch_tips_lesscats) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_magicdamage`](./NPC_Scripts.md#context-butch_tips_magicdamage) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_passives`](./NPC_Scripts.md#context-butch_tips_passives) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_reorient`](./NPC_Scripts.md#context-butch_tips_reorient) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_rewards`](./NPC_Scripts.md#context-butch_tips_rewards) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_tacticalview`](./NPC_Scripts.md#context-butch_tips_tacticalview) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_turnorder`](./NPC_Scripts.md#context-butch_tips_turnorder) | Object | Examples: `{ ... }` | 2 |
| [`butch_tips_wellrounded`](./NPC_Scripts.md#context-butch_tips_wellrounded) | Object | Examples: `{ ... }` | 2 |
| [`can_still_use_attack`](./NPC_Scripts.md#context-can_still_use_attack) | Object | Examples: `{ ... }` | 2 |
| [`can_still_use_attack_didntspell`](./NPC_Scripts.md#context-can_still_use_attack_didntspell) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_a`](./NPC_Scripts.md#context-cant_afford_a) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_b`](./NPC_Scripts.md#context-cant_afford_b) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_c`](./NPC_Scripts.md#context-cant_afford_c) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_d`](./NPC_Scripts.md#context-cant_afford_d) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_iceage`](./NPC_Scripts.md#context-cant_afford_iceage) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_jurassic`](./NPC_Scripts.md#context-cant_afford_jurassic) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_moon`](./NPC_Scripts.md#context-cant_afford_moon) | Object | Examples: `{ ... }` | 2 |
| [`cant_afford_theend`](./NPC_Scripts.md#context-cant_afford_theend) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_butcher`](./NPC_Scripts.md#context-class_unlock_butcher) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_druid`](./NPC_Scripts.md#context-class_unlock_druid) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_jester`](./NPC_Scripts.md#context-class_unlock_jester) | Object | Examples: `{ ... }` | 4 |
| [`class_unlock_medic`](./NPC_Scripts.md#context-class_unlock_medic) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_monk`](./NPC_Scripts.md#context-class_unlock_monk) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_necromancer`](./NPC_Scripts.md#context-class_unlock_necromancer) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_psychic`](./NPC_Scripts.md#context-class_unlock_psychic) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_thief`](./NPC_Scripts.md#context-class_unlock_thief) | Object | Examples: `{ ... }` | 2 |
| [`class_unlock_tinkerer`](./NPC_Scripts.md#context-class_unlock_tinkerer) | Object | Examples: `{ ... }` | 2 |
| [`collected_new_items`](./NPC_Scripts.md#context-collected_new_items) | Object | Examples: `{ ... }` | 2 |
| [`collected_nothing`](./NPC_Scripts.md#context-collected_nothing) | Object | Examples: `{ ... }` | 2 |
| [`do_not_end_turn`](./NPC_Scripts.md#context-do_not_end_turn) | Object | Examples: `{ ... }` | 2 |
| [`done_spitting_fail_ally`](./NPC_Scripts.md#context-done_spitting_fail_ally) | Object | Examples: `{ ... }` | 2 |
| [`done_spitting_fail_miss`](./NPC_Scripts.md#context-done_spitting_fail_miss) | Object | Examples: `{ ... }` | 2 |
| [`done_spitting_fail_rat`](./NPC_Scripts.md#context-done_spitting_fail_rat) | Object | Examples: `{ ... }` | 2 |
| [`done_spitting_success`](./NPC_Scripts.md#context-done_spitting_success) | Object | Examples: `{ ... }` | 2 |
| [`ending`](./NPC_Scripts.md#context-ending) | Object | Examples: `{ ... }` | 2 |
| [`finish_adventure`](./NPC_Scripts.md#context-finish_adventure) | Object | Examples: `{ ... }` | 2 |
| [`first_fight_intro`](./NPC_Scripts.md#context-first_fight_intro) | Object | Examples: `{ ... }` | 2 |
| [`first_house_boss_tomorrow`](./NPC_Scripts.md#context-first_house_boss_tomorrow) | Object | Examples: `{ ... }` | 2 |
| [`first_house_hint_retired`](./NPC_Scripts.md#context-first_house_hint_retired) | Object | Examples: `{ ... }` | 2 |
| [`frank_caves_intro`](./NPC_Scripts.md#context-frank_caves_intro) | Object | Examples: `{ ... }` | 4 |
| [`frank_ending`](./NPC_Scripts.md#context-frank_ending) | Object | Examples: `{ ... }` | 4 |
| [`frank_max1`](./NPC_Scripts.md#context-frank_max1) | Object | Examples: `{ ... }` | 2 |
| [`frank_max2`](./NPC_Scripts.md#context-frank_max2) | Object | Examples: `{ ... }` | 2 |
| [`frank_max3`](./NPC_Scripts.md#context-frank_max3) | Object | Examples: `{ ... }` | 2 |
| [`frank_max4`](./NPC_Scripts.md#context-frank_max4) | Object | Examples: `{ ... }` | 2 |
| [`frank_max5`](./NPC_Scripts.md#context-frank_max5) | Object | Examples: `{ ... }` | 2 |
| [`frank_max_intro`](./NPC_Scripts.md#context-frank_max_intro) | Object | Examples: `{ ... }` | 4 |
| [`frank_max_repeating`](./NPC_Scripts.md#context-frank_max_repeating) | Object | Examples: `{ ... }` | 4 |
| [`frank_terminator2`](./NPC_Scripts.md#context-frank_terminator2) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_1`](./NPC_Scripts.md#context-frank_tips_1) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_10`](./NPC_Scripts.md#context-frank_tips_10) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_2`](./NPC_Scripts.md#context-frank_tips_2) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_3`](./NPC_Scripts.md#context-frank_tips_3) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_4`](./NPC_Scripts.md#context-frank_tips_4) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_5`](./NPC_Scripts.md#context-frank_tips_5) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_6`](./NPC_Scripts.md#context-frank_tips_6) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_7`](./NPC_Scripts.md#context-frank_tips_7) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_8`](./NPC_Scripts.md#context-frank_tips_8) | Object | Examples: `{ ... }` | 2 |
| [`frank_tips_9`](./NPC_Scripts.md#context-frank_tips_9) | Object | Examples: `{ ... }` | 2 |
| [`gone`](./NPC_Scripts.md#context-gone) | Object | Examples: `{ ... }` | 2 |
| [`house_intro`](./NPC_Scripts.md#context-house_intro) | Object | Examples: `{ ... }` | 2 |
| [`house_kitten_box`](./NPC_Scripts.md#context-house_kitten_box) | Object | Examples: `{ ... }` | 2 |
| [`house_pass_day`](./NPC_Scripts.md#context-house_pass_day) | Object | Examples: `{ ... }` | 2 |
| [`house_pass_day2`](./NPC_Scripts.md#context-house_pass_day2) | Object | Examples: `{ ... }` | 2 |
| [`house_pipe`](./NPC_Scripts.md#context-house_pipe) | Object | Examples: `{ ... }` | 2 |
| [`house_retired_cat_box`](./NPC_Scripts.md#context-house_retired_cat_box) | Object | Examples: `{ ... }` | 2 |
| [`house_starred_box`](./NPC_Scripts.md#context-house_starred_box) | Object | Examples: `{ ... }` | 2 |
| [`house_strays`](./NPC_Scripts.md#context-house_strays) | Object | Examples: `{ ... }` | 2 |
| [`house_upgrade_4throom`](./NPC_Scripts.md#context-house_upgrade_4throom) | Object | Examples: `{ ... }` | 4 |
| [`house_upgrade_attic`](./NPC_Scripts.md#context-house_upgrade_attic) | Object | Examples: `{ ... }` | 4 |
| [`house_upgrade_basement`](./NPC_Scripts.md#context-house_upgrade_basement) | Object | Examples: `{ ... }` | 2 |
| [`house_upgrade_basement2`](./NPC_Scripts.md#context-house_upgrade_basement2) | Object | Examples: `{ ... }` | 2 |
| [`house_upgrade_basement3`](./NPC_Scripts.md#context-house_upgrade_basement3) | Object | Examples: `{ ... }` | 2 |
| [`house_upgrade_basement4`](./NPC_Scripts.md#context-house_upgrade_basement4) | Object | Examples: `{ ... }` | 2 |
| [`house_upgrade_basement5`](./NPC_Scripts.md#context-house_upgrade_basement5) | Object | Examples: `{ ... }` | 2 |
| [`house_upgrade_largehouse`](./NPC_Scripts.md#context-house_upgrade_largehouse) | Object | Examples: `{ ... }` | 4 |
| [`house_upgrade_mediumhouse`](./NPC_Scripts.md#context-house_upgrade_mediumhouse) | Object | Examples: `{ ... }` | 4 |
| [`intro`](./NPC_Scripts.md#context-intro) | Object | Examples: `{ ... }` | 216 |
| [`introduce_hard_path`](./NPC_Scripts.md#context-introduce_hard_path) | Object | Examples: `{ ... }` | 2 |
| [`jack_begin_accepting_cats`](./NPC_Scripts.md#context-jack_begin_accepting_cats) | Object | Examples: `{ ... }` | 2 |
| [`jack_desert_intro`](./NPC_Scripts.md#context-jack_desert_intro) | Object | Examples: `{ ... }` | 4 |
| [`Jack_Gainaltfurniture`](./NPC_Scripts.md#context-jack_gainaltfurniture) | Object | Examples: `{ ... }` | 2 |
| [`jack_introduction`](./NPC_Scripts.md#context-jack_introduction) | Object | Examples: `{ ... }` | 2 |
| [`jack_max1`](./NPC_Scripts.md#context-jack_max1) | Object | Examples: `{ ... }` | 2 |
| [`jack_max2`](./NPC_Scripts.md#context-jack_max2) | Object | Examples: `{ ... }` | 2 |
| [`jack_max3`](./NPC_Scripts.md#context-jack_max3) | Object | Examples: `{ ... }` | 2 |
| [`jack_max4`](./NPC_Scripts.md#context-jack_max4) | Object | Examples: `{ ... }` | 2 |
| [`jack_max5`](./NPC_Scripts.md#context-jack_max5) | Object | Examples: `{ ... }` | 2 |
| [`jack_max_intro`](./NPC_Scripts.md#context-jack_max_intro) | Object | Examples: `{ ... }` | 4 |
| [`jack_max_repeating`](./NPC_Scripts.md#context-jack_max_repeating) | Object | Examples: `{ ... }` | 4 |
| [`jack_shopupgrade1`](./NPC_Scripts.md#context-jack_shopupgrade1) | Object | Examples: `{ ... }` | 4 |
| [`jack_shopupgrade2`](./NPC_Scripts.md#context-jack_shopupgrade2) | Object | Examples: `{ ... }` | 4 |
| [`jack_shopupgrade3`](./NPC_Scripts.md#context-jack_shopupgrade3) | Object | Examples: `{ ... }` | 4 |
| [`jack_shopupgrade4`](./NPC_Scripts.md#context-jack_shopupgrade4) | Object | Examples: `{ ... }` | 4 |
| [`jack_zara`](./NPC_Scripts.md#context-jack_zara) | Object | Examples: `{ ... }` | 2 |
| [`level_up_didnt_select_sunburn`](./NPC_Scripts.md#context-level_up_didnt_select_sunburn) | Object | Examples: `{ ... }` | 2 |
| [`level_up_intro`](./NPC_Scripts.md#context-level_up_intro) | Object | Examples: `{ ... }` | 2 |
| [`level_up_selected_sunburn`](./NPC_Scripts.md#context-level_up_selected_sunburn) | Object | Examples: `{ ... }` | 2 |
| [`low_on_food`](./NPC_Scripts.md#context-low_on_food) | Object | Examples: `{ ... }` | 2 |
| [`map_click_node`](./NPC_Scripts.md#context-map_click_node) | Object | Examples: `{ ... }` | 2 |
| [`map_equip_items`](./NPC_Scripts.md#context-map_equip_items) | Object | Examples: `{ ... }` | 2 |
| [`map_equip_items2`](./NPC_Scripts.md#context-map_equip_items2) | Object | Examples: `{ ... }` | 2 |
| [`melee_attack_rat`](./NPC_Scripts.md#context-melee_attack_rat) | Object | Examples: `{ ... }` | 2 |
| [`melee_cat_spit`](./NPC_Scripts.md#context-melee_cat_spit) | Object | Examples: `{ ... }` | 2 |
| [`melee_cat_spit_fail_ally`](./NPC_Scripts.md#context-melee_cat_spit_fail_ally) | Object | Examples: `{ ... }` | 2 |
| [`melee_cat_spit_fail_miss`](./NPC_Scripts.md#context-melee_cat_spit_fail_miss) | Object | Examples: `{ ... }` | 2 |
| [`melee_cat_spit_fail_rat`](./NPC_Scripts.md#context-melee_cat_spit_fail_rat) | Object | Examples: `{ ... }` | 2 |
| [`melee_cat_spit_ignore`](./NPC_Scripts.md#context-melee_cat_spit_ignore) | Object | Examples: `{ ... }` | 2 |
| [`melee_cat_spit_success`](./NPC_Scripts.md#context-melee_cat_spit_success) | Object | Examples: `{ ... }` | 2 |
| [`melee_killed_rat`](./NPC_Scripts.md#context-melee_killed_rat) | Object | Examples: `{ ... }` | 2 |
| [`melee_move2`](./NPC_Scripts.md#context-melee_move2) | Object | Examples: `{ ... }` | 2 |
| [`melee_out_of_actions`](./NPC_Scripts.md#context-melee_out_of_actions) | Object | Examples: `{ ... }` | 2 |
| [`new_adventure`](./NPC_Scripts.md#context-new_adventure) | Object | Examples: `{ ... }` | 2 |
| [`organ_boneyard_intro`](./NPC_Scripts.md#context-organ_boneyard_intro) | Object | Examples: `{ ... }` | 4 |
| [`organ_intro`](./NPC_Scripts.md#context-organ_intro) | Object | Examples: `{ ... }` | 2 |
| [`organ_max1`](./NPC_Scripts.md#context-organ_max1) | Object | Examples: `{ ... }` | 2 |
| [`organ_max2`](./NPC_Scripts.md#context-organ_max2) | Object | Examples: `{ ... }` | 2 |
| [`organ_max3`](./NPC_Scripts.md#context-organ_max3) | Object | Examples: `{ ... }` | 2 |
| [`organ_max4`](./NPC_Scripts.md#context-organ_max4) | Object | Examples: `{ ... }` | 2 |
| [`organ_max5`](./NPC_Scripts.md#context-organ_max5) | Object | Examples: `{ ... }` | 2 |
| [`organ_max_intro`](./NPC_Scripts.md#context-organ_max_intro) | Object | Examples: `{ ... }` | 4 |
| [`organ_max_repeating`](./NPC_Scripts.md#context-organ_max_repeating) | Object | Examples: `{ ... }` | 4 |
| [`organ_rename`](./NPC_Scripts.md#context-organ_rename) | Object | Examples: `{ ... }` | 2 |
| [`organ_throbbingdomain_intro`](./NPC_Scripts.md#context-organ_throbbingdomain_intro) | Object | Examples: `{ ... }` | 4 |
| [`organ_tina3`](./NPC_Scripts.md#context-organ_tina3) | Object | Examples: `{ ... }` | 2 |
| [`organ_unlock`](./NPC_Scripts.md#context-organ_unlock) | Object | Examples: `{ ... }` | 4 |
| [`organ_upgrade1`](./NPC_Scripts.md#context-organ_upgrade1) | Object | Examples: `{ ... }` | 4 |
| [`organ_upgrade2`](./NPC_Scripts.md#context-organ_upgrade2) | Object | Examples: `{ ... }` | 4 |
| [`organ_upgrade3`](./NPC_Scripts.md#context-organ_upgrade3) | Object | Examples: `{ ... }` | 4 |
| [`organ_upgrade4`](./NPC_Scripts.md#context-organ_upgrade4) | Object | Examples: `{ ... }` | 4 |
| [`organ_upgrade5`](./NPC_Scripts.md#context-organ_upgrade5) | Object | Examples: `{ ... }` | 4 |
| [`organ_upgrade6`](./NPC_Scripts.md#context-organ_upgrade6) | Object | Examples: `{ ... }` | 4 |
| [`purchase_item_a`](./NPC_Scripts.md#context-purchase_item_a) | Object | Examples: `{ ... }` | 2 |
| [`purchase_item_b`](./NPC_Scripts.md#context-purchase_item_b) | Object | Examples: `{ ... }` | 2 |
| [`purchase_item_c`](./NPC_Scripts.md#context-purchase_item_c) | Object | Examples: `{ ... }` | 2 |
| [`purchase_item_d`](./NPC_Scripts.md#context-purchase_item_d) | Object | Examples: `{ ... }` | 2 |
| [`purchase_item_iceage`](./NPC_Scripts.md#context-purchase_item_iceage) | Object | Examples: `{ ... }` | 2 |
| [`purchase_item_jurassic`](./NPC_Scripts.md#context-purchase_item_jurassic) | Object | Examples: `{ ... }` | 2 |
| [`purchase_item_moon`](./NPC_Scripts.md#context-purchase_item_moon) | Object | Examples: `{ ... }` | 2 |
| [`purchase_item_theend`](./NPC_Scripts.md#context-purchase_item_theend) | Object | Examples: `{ ... }` | 2 |
| [`ranged_attack_tomtom`](./NPC_Scripts.md#context-ranged_attack_tomtom) | Object | Examples: `{ ... }` | 2 |
| [`ranged_attack_tomtom_fail_ally`](./NPC_Scripts.md#context-ranged_attack_tomtom_fail_ally) | Object | Examples: `{ ... }` | 2 |
| [`ranged_attack_tomtom_fail_miss`](./NPC_Scripts.md#context-ranged_attack_tomtom_fail_miss) | Object | Examples: `{ ... }` | 2 |
| [`ranged_attack_tomtom_fail_rat`](./NPC_Scripts.md#context-ranged_attack_tomtom_fail_rat) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_attack`](./NPC_Scripts.md#context-ranged_cat_attack) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_early_attack2_ally`](./NPC_Scripts.md#context-ranged_cat_early_attack2_ally) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_early_attack2_miss`](./NPC_Scripts.md#context-ranged_cat_early_attack2_miss) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_early_attack2_rat`](./NPC_Scripts.md#context-ranged_cat_early_attack2_rat) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_early_attack_ally`](./NPC_Scripts.md#context-ranged_cat_early_attack_ally) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_early_attack_miss`](./NPC_Scripts.md#context-ranged_cat_early_attack_miss) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_early_attack_rat`](./NPC_Scripts.md#context-ranged_cat_early_attack_rat) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_failmove`](./NPC_Scripts.md#context-ranged_cat_failmove) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_intro`](./NPC_Scripts.md#context-ranged_cat_intro) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_roll`](./NPC_Scripts.md#context-ranged_cat_roll) | Object | Examples: `{ ... }` | 2 |
| [`ranged_cat_rolled_first`](./NPC_Scripts.md#context-ranged_cat_rolled_first) | Object | Examples: `{ ... }` | 2 |
| [`steven_100`](./NPC_Scripts.md#context-steven_100) | Object | Examples: `{ ... }` | 2 |
| [`steven_introduction`](./NPC_Scripts.md#context-steven_introduction) | Object | Examples: `{ ... }` | 2 |
| [`steven_milliontrashed`](./NPC_Scripts.md#context-steven_milliontrashed) | Object | Examples: `{ ... }` | 4 |
| [`steven_postendgame`](./NPC_Scripts.md#context-steven_postendgame) | Object | Examples: `{ ... }` | 4 |
| [`steven_resummon`](./NPC_Scripts.md#context-steven_resummon) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_1`](./NPC_Scripts.md#context-steven_savescum_1) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_100`](./NPC_Scripts.md#context-steven_savescum_100) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_1alt1`](./NPC_Scripts.md#context-steven_savescum_1alt1) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_1alt2`](./NPC_Scripts.md#context-steven_savescum_1alt2) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_1alt3`](./NPC_Scripts.md#context-steven_savescum_1alt3) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_2`](./NPC_Scripts.md#context-steven_savescum_2) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_2alt1`](./NPC_Scripts.md#context-steven_savescum_2alt1) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_2alt2`](./NPC_Scripts.md#context-steven_savescum_2alt2) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_2alt3`](./NPC_Scripts.md#context-steven_savescum_2alt3) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_3`](./NPC_Scripts.md#context-steven_savescum_3) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_3alt1`](./NPC_Scripts.md#context-steven_savescum_3alt1) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_3alt2`](./NPC_Scripts.md#context-steven_savescum_3alt2) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_3alt3`](./NPC_Scripts.md#context-steven_savescum_3alt3) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_4`](./NPC_Scripts.md#context-steven_savescum_4) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_4alt1`](./NPC_Scripts.md#context-steven_savescum_4alt1) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_4alt2`](./NPC_Scripts.md#context-steven_savescum_4alt2) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_4alt3`](./NPC_Scripts.md#context-steven_savescum_4alt3) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_houseboss_1`](./NPC_Scripts.md#context-steven_savescum_houseboss_1) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_houseboss_100`](./NPC_Scripts.md#context-steven_savescum_houseboss_100) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_houseboss_2`](./NPC_Scripts.md#context-steven_savescum_houseboss_2) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_houseboss_3`](./NPC_Scripts.md#context-steven_savescum_houseboss_3) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_intro`](./NPC_Scripts.md#context-steven_savescum_intro) | Object | Examples: `{ ... }` | 2 |
| [`steven_savescum_intro_houseboss`](./NPC_Scripts.md#context-steven_savescum_intro_houseboss) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act1_crazy`](./NPC_Scripts.md#context-steven_unlock_act1_crazy) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act1_impossible`](./NPC_Scripts.md#context-steven_unlock_act1_impossible) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act2_crazy`](./NPC_Scripts.md#context-steven_unlock_act2_crazy) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act2_hard`](./NPC_Scripts.md#context-steven_unlock_act2_hard) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act2_impossible`](./NPC_Scripts.md#context-steven_unlock_act2_impossible) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act3_crazy`](./NPC_Scripts.md#context-steven_unlock_act3_crazy) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act3_hard`](./NPC_Scripts.md#context-steven_unlock_act3_hard) | Object | Examples: `{ ... }` | 2 |
| [`steven_unlock_act3_impossible`](./NPC_Scripts.md#context-steven_unlock_act3_impossible) | Object | Examples: `{ ... }` | 2 |
| [`take_cats_inside`](./NPC_Scripts.md#context-take_cats_inside) | Object | Examples: `{ ... }` | 2 |
| [`test_gamepad_prompts`](./NPC_Scripts.md#context-test_gamepad_prompts) | Object | Examples: `{ ... }` | 2 |
| [`tink_aggression`](./NPC_Scripts.md#context-tink_aggression) | Object | Examples: `{ ... }` | 4 |
| [`tink_basestats`](./NPC_Scripts.md#context-tink_basestats) | Object | Examples: `{ ... }` | 4 |
| [`tink_begin_accepting_cats`](./NPC_Scripts.md#context-tink_begin_accepting_cats) | Object | Examples: `{ ... }` | 2 |
| [`tink_inbreeding`](./NPC_Scripts.md#context-tink_inbreeding) | Object | Examples: `{ ... }` | 4 |
| [`tink_max1`](./NPC_Scripts.md#context-tink_max1) | Object | Examples: `{ ... }` | 2 |
| [`tink_max10`](./NPC_Scripts.md#context-tink_max10) | Object | Examples: `{ ... }` | 2 |
| [`tink_max2`](./NPC_Scripts.md#context-tink_max2) | Object | Examples: `{ ... }` | 2 |
| [`tink_max3`](./NPC_Scripts.md#context-tink_max3) | Object | Examples: `{ ... }` | 2 |
| [`tink_max4`](./NPC_Scripts.md#context-tink_max4) | Object | Examples: `{ ... }` | 2 |
| [`tink_max5`](./NPC_Scripts.md#context-tink_max5) | Object | Examples: `{ ... }` | 2 |
| [`tink_max6`](./NPC_Scripts.md#context-tink_max6) | Object | Examples: `{ ... }` | 2 |
| [`tink_max7`](./NPC_Scripts.md#context-tink_max7) | Object | Examples: `{ ... }` | 2 |
| [`tink_max8`](./NPC_Scripts.md#context-tink_max8) | Object | Examples: `{ ... }` | 2 |
| [`tink_max9`](./NPC_Scripts.md#context-tink_max9) | Object | Examples: `{ ... }` | 2 |
| [`tink_max_intro`](./NPC_Scripts.md#context-tink_max_intro) | Object | Examples: `{ ... }` | 4 |
| [`tink_max_repeating`](./NPC_Scripts.md#context-tink_max_repeating) | Object | Examples: `{ ... }` | 4 |
| [`tink_prettybow`](./NPC_Scripts.md#context-tink_prettybow) | Object | Examples: `{ ... }` | 4 |
| [`tink_relationships`](./NPC_Scripts.md#context-tink_relationships) | Object | Examples: `{ ... }` | 4 |
| [`tink_sexuality`](./NPC_Scripts.md#context-tink_sexuality) | Object | Examples: `{ ... }` | 4 |
| [`tink_tags`](./NPC_Scripts.md#context-tink_tags) | Object | Examples: `{ ... }` | 4 |
| [`tink_terminator`](./NPC_Scripts.md#context-tink_terminator) | Object | Examples: `{ ... }` | 2 |
| [`tink_tina2`](./NPC_Scripts.md#context-tink_tina2) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_appeal`](./NPC_Scripts.md#context-tink_tips_appeal) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_basestats`](./NPC_Scripts.md#context-tink_tips_basestats) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_cleaning`](./NPC_Scripts.md#context-tink_tips_cleaning) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_comfort`](./NPC_Scripts.md#context-tink_tips_comfort) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_health`](./NPC_Scripts.md#context-tink_tips_health) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_inbreeding`](./NPC_Scripts.md#context-tink_tips_inbreeding) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_intro`](./NPC_Scripts.md#context-tink_tips_intro) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_multiclassing`](./NPC_Scripts.md#context-tink_tips_multiclassing) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_mutation`](./NPC_Scripts.md#context-tink_tips_mutation) | Object | Examples: `{ ... }` | 2 |
| [`tink_tips_stimulation`](./NPC_Scripts.md#context-tink_tips_stimulation) | Object | Examples: `{ ... }` | 2 |
| [`tracy_blankcollar1`](./NPC_Scripts.md#context-tracy_blankcollar1) | Object | Examples: `{ ... }` | 4 |
| [`tracy_blankcollar2`](./NPC_Scripts.md#context-tracy_blankcollar2) | Object | Examples: `{ ... }` | 4 |
| [`tracy_blankcollar3`](./NPC_Scripts.md#context-tracy_blankcollar3) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodbonus1`](./NPC_Scripts.md#context-tracy_foodbonus1) | Object | Examples: `{ ... }` | 2 |
| [`tracy_foodstorage1`](./NPC_Scripts.md#context-tracy_foodstorage1) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage10`](./NPC_Scripts.md#context-tracy_foodstorage10) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage2`](./NPC_Scripts.md#context-tracy_foodstorage2) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage3`](./NPC_Scripts.md#context-tracy_foodstorage3) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage4`](./NPC_Scripts.md#context-tracy_foodstorage4) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage5`](./NPC_Scripts.md#context-tracy_foodstorage5) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage6`](./NPC_Scripts.md#context-tracy_foodstorage6) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage7`](./NPC_Scripts.md#context-tracy_foodstorage7) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage8`](./NPC_Scripts.md#context-tracy_foodstorage8) | Object | Examples: `{ ... }` | 4 |
| [`tracy_foodstorage9`](./NPC_Scripts.md#context-tracy_foodstorage9) | Object | Examples: `{ ... }` | 4 |
| [`tracy_idol1`](./NPC_Scripts.md#context-tracy_idol1) | Object | Examples: `{ ... }` | 4 |
| [`tracy_idol2`](./NPC_Scripts.md#context-tracy_idol2) | Object | Examples: `{ ... }` | 4 |
| [`tracy_idol3`](./NPC_Scripts.md#context-tracy_idol3) | Object | Examples: `{ ... }` | 4 |
| [`tracy_idol4`](./NPC_Scripts.md#context-tracy_idol4) | Object | Examples: `{ ... }` | 4 |
| [`tracy_idol5`](./NPC_Scripts.md#context-tracy_idol5) | Object | Examples: `{ ... }` | 4 |
| [`tracy_idol6`](./NPC_Scripts.md#context-tracy_idol6) | Object | Examples: `{ ... }` | 4 |
| [`tracy_idol7`](./NPC_Scripts.md#context-tracy_idol7) | Object | Examples: `{ ... }` | 4 |
| [`tracy_introduction`](./NPC_Scripts.md#context-tracy_introduction) | Object | Examples: `{ ... }` | 2 |
| [`tracy_kaijufight`](./NPC_Scripts.md#context-tracy_kaijufight) | Object | Examples: `{ ... }` | 2 |
| [`tracy_max1`](./NPC_Scripts.md#context-tracy_max1) | Object | Examples: `{ ... }` | 2 |
| [`tracy_max2`](./NPC_Scripts.md#context-tracy_max2) | Object | Examples: `{ ... }` | 2 |
| [`tracy_max3`](./NPC_Scripts.md#context-tracy_max3) | Object | Examples: `{ ... }` | 2 |
| [`tracy_max4`](./NPC_Scripts.md#context-tracy_max4) | Object | Examples: `{ ... }` | 2 |
| [`tracy_max5`](./NPC_Scripts.md#context-tracy_max5) | Object | Examples: `{ ... }` | 2 |
| [`tracy_max_intro`](./NPC_Scripts.md#context-tracy_max_intro) | Object | Examples: `{ ... }` | 4 |
| [`tracy_max_repeating`](./NPC_Scripts.md#context-tracy_max_repeating) | Object | Examples: `{ ... }` | 4 |
| [`try_again_attack_rat`](./NPC_Scripts.md#context-try_again_attack_rat) | Object | Examples: `{ ... }` | 2 |
| [`try_again_melee_move`](./NPC_Scripts.md#context-try_again_melee_move) | Object | Examples: `{ ... }` | 2 |
| [`tutorial_cat_dies`](./NPC_Scripts.md#context-tutorial_cat_dies) | Object | Examples: `{ ... }` | 2 |
| [`unprompted1`](./NPC_Scripts.md#context-unprompted1) | Object | Examples: `{ ... }` | 2 |
| [`unprompted2`](./NPC_Scripts.md#context-unprompted2) | Object | Examples: `{ ... }` | 2 |
| [`unprompted3`](./NPC_Scripts.md#context-unprompted3) | Object | Examples: `{ ... }` | 2 |
| [`unprompted4`](./NPC_Scripts.md#context-unprompted4) | Object | Examples: `{ ... }` | 2 |
| [`unprompted5`](./NPC_Scripts.md#context-unprompted5) | Object | Examples: `{ ... }` | 2 |
| [`unprompted6`](./NPC_Scripts.md#context-unprompted6) | Object | Examples: `{ ... }` | 2 |
| [`upgrade_storage_1`](./NPC_Scripts.md#context-upgrade_storage_1) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_2`](./NPC_Scripts.md#context-upgrade_storage_2) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_3`](./NPC_Scripts.md#context-upgrade_storage_3) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_4`](./NPC_Scripts.md#context-upgrade_storage_4) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_5`](./NPC_Scripts.md#context-upgrade_storage_5) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_6`](./NPC_Scripts.md#context-upgrade_storage_6) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_7`](./NPC_Scripts.md#context-upgrade_storage_7) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_max1`](./NPC_Scripts.md#context-upgrade_storage_max1) | Object | Examples: `{ ... }` | 2 |
| [`upgrade_storage_max2`](./NPC_Scripts.md#context-upgrade_storage_max2) | Object | Examples: `{ ... }` | 2 |
| [`upgrade_storage_max3`](./NPC_Scripts.md#context-upgrade_storage_max3) | Object | Examples: `{ ... }` | 2 |
| [`upgrade_storage_max4`](./NPC_Scripts.md#context-upgrade_storage_max4) | Object | Examples: `{ ... }` | 2 |
| [`upgrade_storage_max5`](./NPC_Scripts.md#context-upgrade_storage_max5) | Object | Examples: `{ ... }` | 2 |
| [`upgrade_storage_repeating_crazy`](./NPC_Scripts.md#context-upgrade_storage_repeating_crazy) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_repeating_hard`](./NPC_Scripts.md#context-upgrade_storage_repeating_hard) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_repeating_impossible`](./NPC_Scripts.md#context-upgrade_storage_repeating_impossible) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_repeating_intro`](./NPC_Scripts.md#context-upgrade_storage_repeating_intro) | Object | Examples: `{ ... }` | 4 |
| [`upgrade_storage_repeating_normal`](./NPC_Scripts.md#context-upgrade_storage_repeating_normal) | Object | Examples: `{ ... }` | 4 |
| [`use_attack_after_used_weapon`](./NPC_Scripts.md#context-use_attack_after_used_weapon) | Object | Examples: `{ ... }` | 2 |
| [`use_weapon`](./NPC_Scripts.md#context-use_weapon) | Object | Examples: `{ ... }` | 2 |
| [`welcome`](./NPC_Scripts.md#context-welcome) | Object | Examples: `{ ... }` | 2 |
| [`welcome_boneyard`](./NPC_Scripts.md#context-welcome_boneyard) | Object | Examples: `{ ... }` | 2 |
| [`welcome_bunker`](./NPC_Scripts.md#context-welcome_bunker) | Object | Examples: `{ ... }` | 2 |
| [`welcome_caves`](./NPC_Scripts.md#context-welcome_caves) | Object | Examples: `{ ... }` | 2 |
| [`welcome_core`](./NPC_Scripts.md#context-welcome_core) | Object | Examples: `{ ... }` | 2 |
| [`welcome_crater`](./NPC_Scripts.md#context-welcome_crater) | Object | Examples: `{ ... }` | 2 |
| [`welcome_desert`](./NPC_Scripts.md#context-welcome_desert) | Object | Examples: `{ ... }` | 2 |
| [`welcome_future`](./NPC_Scripts.md#context-welcome_future) | Object | Examples: `{ ... }` | 2 |
| [`welcome_iceage`](./NPC_Scripts.md#context-welcome_iceage) | Object | Examples: `{ ... }` | 2 |
| [`welcome_junkyard`](./NPC_Scripts.md#context-welcome_junkyard) | Object | Examples: `{ ... }` | 2 |
| [`welcome_jurassic`](./NPC_Scripts.md#context-welcome_jurassic) | Object | Examples: `{ ... }` | 2 |
| [`welcome_lab`](./NPC_Scripts.md#context-welcome_lab) | Object | Examples: `{ ... }` | 2 |
| [`welcome_moon`](./NPC_Scripts.md#context-welcome_moon) | Object | Examples: `{ ... }` | 2 |
| [`welcome_sewers`](./NPC_Scripts.md#context-welcome_sewers) | Object | Examples: `{ ... }` | 2 |
| [`welcome_theend`](./NPC_Scripts.md#context-welcome_theend) | Object | Examples: `{ ... }` | 2 |
| [`welcome_water`](./NPC_Scripts.md#context-welcome_water) | Object | Examples: `{ ... }` | 2 |
| [`welcome_water_cheap`](./NPC_Scripts.md#context-welcome_water_cheap) | Object | Examples: `{ ... }` | 2 |

</details>

---

### Object: `states`



**Definition:** No definition provided.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`idle`](./Arrays.md#array-idle) | Array | Examples: `[ "idle" "blocking" ], [ "idle" ], [ "idle" "blocking" "gone" ]` | 10 |
| [`closeup`](./Arrays.md#array-closeup) | Array | Examples: `[ "closeup" ]` | 3 |
| [`verycloseup`](./Arrays.md#array-verycloseup) | Array | Examples: `[ "verycloseup" ]` | 3 |
| [`zoomedout`](./Arrays.md#array-zoomedout) | Array | Examples: `[ "zoomedout" ]` | 3 |
| [`beanies_intensestatic`](./Arrays.md#array-beanies_intensestatic) | Array | Examples: `[ "beanies_intensestatic" ]` | 1 |
| [`beanies_right`](./Arrays.md#array-beanies_right) | Array | Examples: `[ "beanies_right" ]` | 1 |
| [`butch_left`](./Arrays.md#array-butch_left) | Array | Examples: `[ "butch_left" "butch_point_move" "butch_point_attack" "b...` | 1 |
| [`butch_right`](./Arrays.md#array-butch_right) | Array | Examples: `[ "butch_right" "butch_point_spells" "butch_point_turnord...` | 1 |
| [`choosecats`](./Arrays.md#array-choosecats) | Array | Examples: `[ "choosecats" ]` | 1 |
| [`closerup`](./Arrays.md#array-closerup) | Array | Examples: `[ "closerup" ]` | 1 |
| [`frank_right`](./Arrays.md#array-frank_right) | Array | Examples: `[ "frank_right" "frank_point_pipe" ]` | 1 |
| [`jack_right`](./Arrays.md#array-jack_right) | Array | Examples: `[ "jack_right" "jack_point_furniture" ]` | 1 |
| [`offscreen`](./Arrays.md#array-offscreen) | Array | Examples: `[ "offscreen" ]` | 1 |
| [`steven_center`](./Arrays.md#array-steven_center) | Array | Examples: `[ "steven_center" "steven_cat" ]` | 1 |
| [`tink_left`](./Arrays.md#array-tink_left) | Array | Examples: `[ "tink_left" "tink_point_cats" "tink_point_food" "tink_p...` | 1 |
| [`tink_right`](./Arrays.md#array-tink_right) | Array | Examples: `[ "tink_right" "tink_point_strays" ]` | 1 |

</details>

---

### Object: `transitions`



**Definition:** No definition provided.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`beanies_intensestatic_to_offscreen`](./Arrays.md#array-beanies_intensestatic_to_offscreen) | Array | Examples: `[ beanies_intensestatic offscreen ]` | 1 |
| [`beanies_offscreen_to_intensestatic`](./Arrays.md#array-beanies_offscreen_to_intensestatic) | Array | Examples: `[ offscreen beanies_intensestatic ]` | 1 |
| [`beanies_offscreen_to_right`](./Arrays.md#array-beanies_offscreen_to_right) | Array | Examples: `[ offscreen beanies_right ]` | 1 |
| [`beanies_right_to_offscreen`](./Arrays.md#array-beanies_right_to_offscreen) | Array | Examples: `[ beanies_right offscreen ]` | 1 |
| [`butch_left_to_offscreen`](./Arrays.md#array-butch_left_to_offscreen) | Array | Examples: `[ butch_left offscreen ]` | 1 |
| [`butch_left_to_right`](./Arrays.md#array-butch_left_to_right) | Array | Examples: `[ butch_left butch_right ]` | 1 |
| [`butch_offscreen_to_left`](./Arrays.md#array-butch_offscreen_to_left) | Array | Examples: `[ offscreen butch_left ]` | 1 |
| [`butch_offscreen_to_right`](./Arrays.md#array-butch_offscreen_to_right) | Array | Examples: `[ offscreen butch_right ]` | 1 |
| [`butch_right_to_left`](./Arrays.md#array-butch_right_to_left) | Array | Examples: `[ butch_right butch_left ]` | 1 |
| [`butch_right_to_offscreen`](./Arrays.md#array-butch_right_to_offscreen) | Array | Examples: `[ butch_right offscreen ]` | 1 |
| [`frank_offscreen_to_right`](./Arrays.md#array-frank_offscreen_to_right) | Array | Examples: `[ offscreen frank_right ]` | 1 |
| [`frank_right_to_offscreen`](./Arrays.md#array-frank_right_to_offscreen) | Array | Examples: `[ frank_right offscreen ]` | 1 |
| [`jack_offscreen_to_right`](./Arrays.md#array-jack_offscreen_to_right) | Array | Examples: `[ offscreen jack_right ]` | 1 |
| [`jack_right_to_offscreen`](./Arrays.md#array-jack_right_to_offscreen) | Array | Examples: `[ jack_right offscreen ]` | 1 |
| [`steven_center_to_offscreen`](./Arrays.md#array-steven_center_to_offscreen) | Array | Examples: `[ steven_center offscreen ]` | 1 |
| [`steven_offscreen_to_center`](./Arrays.md#array-steven_offscreen_to_center) | Array | Examples: `[ offscreen steven_center ]` | 1 |
| [`tink_left_to_offscreen`](./Arrays.md#array-tink_left_to_offscreen) | Array | Examples: `[ tink_left offscreen ]` | 1 |
| [`tink_left_to_right`](./Arrays.md#array-tink_left_to_right) | Array | Examples: `[ tink_left tink_right ]` | 1 |
| [`tink_offscreen_to_left`](./Arrays.md#array-tink_offscreen_to_left) | Array | Examples: `[ offscreen tink_left ]` | 1 |
| [`tink_offscreen_to_right`](./Arrays.md#array-tink_offscreen_to_right) | Array | Examples: `[ offscreen tink_right ]` | 1 |
| [`tink_right_to_left`](./Arrays.md#array-tink_right_to_left) | Array | Examples: `[ tink_right tink_left ]` | 1 |
| [`tink_right_to_offscreen`](./Arrays.md#array-tink_right_to_offscreen) | Array | Examples: `[ tink_right offscreen ]` | 1 |

</details>

---

### Object: `unprompted`



**Definition:** No definition provided.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ unprompted_a unprompted_b unprompted_c unprompted_d unp..., [ unprompted1 u...` | 5 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_JACK_UNPROMPTED_1, NPC_ORGANGRINDER_UNPROMPTED_1, NPC_TRACY_UNPROMPTED_2` | 6 |
| `cancelable` | Boolean | Examples: `true` | 6 |
| `wait_for_cancel` | Number | Examples: `1` | 6 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_UNPROMPTED_1, NPC_TRACY_UNPROMPTED_1` | 4 |

</details>

---

### Object: `also`



**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_ALSO_1, NPC_BEANIES_ALSO_1, NPC_BUTCH_ALSO_1` | 16 |

</details>

---

### Object: `unknown`



**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNKNOWN_1, NPC_FRANK_UNKNOWN_1, NPC_BEANIES_UNKNOWN_1` | 16 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 12 |
| `lock_controls` | Number | Examples: `1` | 6 |
| `unlock_controls` | Number | Examples: `1` | 6 |

</details>

---

### Object: `hide_text`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Strings.md#string-dialog_and_autopass) | String | Examples: `""` | 8 |
| `cancelable` | Boolean | Examples: `true` | 8 |

</details>

---

### Object: `purchase_item`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_PURCHASE_ITEM_1, NPC_ORGANGRINDER_PURCHASE_ITEM_1, NPC_JACK_PURCHAS...` | 6 |
| `cancelable` | Boolean | Examples: `true` | 6 |
| `wait_for_cancel` | Number | Examples: `1` | 6 |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ purchase_item_a purchase_item_b purchase_item_c purchas...` | 1 |

</details>

---

### Object: `tooltip`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tooltip_dialog`](./Enums.md#enum-tooltip_dialog) | Enum | Examples: `NPC_TRACY_SHOP_TOOLTIP, NPC_ORGANGRINDER_SHOP_TOOLTIP, NPC_JACK_SHOP_TOOLTIP` | 8 |
| `cancelable` | Boolean | Examples: `true` | 8 |
| `wait_for_cancel` | Number | Examples: `1` | 8 |

</details>

---

### Object: `unprompted_a`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_A_1, NPC_FRANK_UNPROMPTED_A_2, NPC_BUTCH_UNPROMPTED_A_1` | 16 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_b`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_B_1, NPC_FRANK_UNPROMPTED_B_1, NPC_FRANK_UNPROMPTED_B_2` | 12 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_c`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_C_1, NPC_FRANK_UNPROMPTED_C_2, NPC_BUTCH_UNPROMPTED_C_1` | 10 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_d`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_D_1, NPC_BUTCH_UNPROMPTED_D_1, NPC_FRANK_UNPROMPTED_D_2` | 14 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_e`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_E_1, NPC_BUTCH_UNPROMPTED_E_1, NPC_FRANK_UNPROMPTED_E_2` | 12 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_f`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_F_1, NPC_FRANK_UNPROMPTED_F_2, NPC_FRANK_UNPROMPTED_F_1` | 14 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_g`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_G_2, NPC_BUTCH_UNPROMPTED_G_1, NPC_FRANK_UNPROMPTED_G_1` | 16 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_h`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_H_1, NPC_FRANK_UNPROMPTED_H_2, NPC_FRANK_UNPROMPTED_H_1` | 18 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `unprompted_i`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_I_2, NPC_BUTCH_UNPROMPTED_I_1, NPC_FRANK_UNPROMPTED_I_1` | 16 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 6 |

</details>

---

### Object: `cant_afford`



**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_CANT_AFFORD_1, NPC_JACK_CANT_AFFORD_1` | 4 |
| `cancelable` | Boolean | Examples: `true` | 4 |
| `wait_for_cancel` | Number | Examples: `1` | 4 |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ cant_afford_a cant_afford_b cant_afford_c cant_afford_d ]` | 1 |

</details>

---

### Object: `forward_to_tips`



**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ butch_tips_intelligence butch_tips_charisma butch_tips_..., [ frank_tips_1 ...` | 3 |

</details>

---

### Object: `out_of_stock`



**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_OUT_OF_STOCK_1, NPC_JACK_OUT_OF_STOCK_1, NPC_TRACY_OUT_OF_ST...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `blocking` | 6 |

</details>

---

### Object: `Jack_Gainaltfurniture`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_GAINALTFURNITURE_3, NPC_JACK_JACK_GAINALTFURNITURE_1, NPC_JACK_...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 8 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `beanies_begin_accepting_cats`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_2, NPC_BEANIES_BEANIES_BEGIN_ACCEPTI...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `beanies` | 2 |

</details>

---

### Object: `beanies_bombquest_2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_2_2, NPC_BEANIES_BEANIES_BOMBQUEST_2_1, NPC_BEA...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `beanies_bombquest_3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_3_1, NPC_BEANIES_BEANIES_BOMBQUEST_3_2, NPC_BEA...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `nuke_quest_get_nuke` | 2 |

</details>

---

### Object: `beanies_bombquest_amnesia`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_1, NPC_BEANIES_BEANIES_BOMBQUEST_AMNESI...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `nuke_quest_loop` | 2 |

</details>

---

### Object: `beanies_bombquest_begin`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_2, NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_1,...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 14 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 2 |

</details>

---

### Object: `beanies_bombquest_fail_jarofblood`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_3, NPC_BEANIES_BEANIES_BOMBQUES...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 2 |

</details>

---

### Object: `beanies_bombquest_fail_jarofchaos`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_3, NPC_BEANIES_BEANIES_BOMBQUES...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 2 |

</details>

---

### Object: `beanies_bombquest_fail_jarofradiation`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_1, NPC_BEANIES_BEANIES_BOMB...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 2 |

</details>

---

### Object: `beanies_bombquest_fail_nuke`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_3, NPC_BEANIES_BEANIES_BOMBQUEST_FAIL...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 14 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 2 |

</details>

---

### Object: `beanies_future_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_FUTURE_INTRO_2, NPC_BEANIES_BEANIES_FUTURE_INTRO_3, NPC_B...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 10 |

</details>

---

### Object: `beanies_hitler3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_HITLER3_2, NPC_BEANIES_BEANIES_HITLER3_1, NPC_BEANIES_BEA...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `beanies_hitler3_defeat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_2, NPC_BEANIES_BEANIES_HITLER3_DEFEAT_1, N...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 14 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_amplifier2` | 2 |

</details>

---

### Object: `beanies_iloveyou`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_ILOVEYOU_2, NPC_BEANIES_BEANIES_ILOVEYOU_3, NPC_BEANIES_B...` | 6 |

</details>

---

### Object: `beanies_infinite_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_INFINITE_INTRO_3, NPC_POPUP_BEANIES_INFINITE_INTRO_2, NPC_P...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 4 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.25` | 2 |

</details>

---

### Object: `beanies_jurassic_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_JURASSIC_INTRO_1, NPC_BEANIES_BEANIES_JURASSIC_INTRO_2, N...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |

</details>

---

### Object: `beanies_lab_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_LAB_INTRO_1, NPC_BEANIES_BEANIES_LAB_INTRO_3, NPC_BEANIES...` | 48 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 22 |
| [`play_cutscene`](./Enums.md#enum-play_cutscene) | Enum | Examples: `credits_1` | 2 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `song_unlock_get_in_the_cage` | 2 |
| `restart_npc_music` | Number | Examples: `1` | 2 |

</details>

---

### Object: `beanies_quest_complete`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_complete` | 2 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `success` | 2 |

</details>

---

### Object: `beanies_quest_fail`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_fail` | 2 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `fail` | 2 |

</details>

---

### Object: `beanies_quests_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_QUESTS_INTRO_3, NPC_BEANIES_BEANIES_QUESTS_INTRO_1, NPC_B...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_intro` | 2 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `newest` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `beanies_quests_repeat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_QUESTS_REPEAT_1, NPC_BEANIES_BEANIES_QUESTS_REPEAT_3, NPC...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_intro` | 2 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `newest` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `beanies_rift_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_RIFT_INTRO_1, NPC_POPUP_BEANIES_RIFT_INTRO_2, NPC_POPUP_BEA...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 4 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.25` | 2 |

</details>

---

### Object: `beanies_screenshake_test`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_1, NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_...` | 14 |
| [`screenshake`](./Arrays.md#array-screenshake) | Array | Examples: `[ .5 10 ]` | 1 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `PickupCoin` | 2 |

</details>

---

### Object: `beanies_seefuture`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SEEFUTURE_3, NPC_BEANIES_BEANIES_SEEFUTURE_2, NPC_BEANIES...` | 30 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 18 |

</details>

---

### Object: `beanies_seetheend`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SEETHEEND_1, NPC_BEANIES_BEANIES_SEETHEEND_2, NPC_BEANIES...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |

</details>

---

### Object: `beanies_terminator1_defeat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_1, NPC_BEANIES_BEANIES_TERMINATOR1_DEF...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_receiver2` | 2 |

</details>

---

### Object: `beanies_terminator2_defeat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_3, NPC_BEANIES_BEANIES_TERMINATOR2_DEF...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_transmitter2` | 2 |

</details>

---

### Object: `beanies_theend_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_THEEND_INTRO_3, NPC_BEANIES_BEANIES_THEEND_INTRO_2, NPC_B...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |

</details>

---

### Object: `beanies_timemachine_2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TIMEMACHINE_2_2, NPC_BEANIES_BEANIES_TIMEMACHINE_2_3, NPC...` | 40 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 18 |

</details>

---

### Object: `beanies_timemachine_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_2, NPC_BEANIES_BEANIES_TIMEMACHINE_INTR...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 8 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `time_machine_quest_begin` | 2 |

</details>

---

### Object: `beanies_vscreator1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR1_1, NPC_POPUP_BEANIES_VSCREATOR1_3, NPC_POPUP_BEA...` | 28 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 4 |

</details>

---

### Object: `beanies_vscreator2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR2_1, NPC_POPUP_BEANIES_VSCREATOR2_3, NPC_POPUP_BEA...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 4 |

</details>

---

### Object: `beanies_vscreator3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR3_2, NPC_POPUP_BEANIES_VSCREATOR3_3, NPC_POPUP_BEA...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_intensestatic` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 4 |

</details>

---

### Object: `beanies_vscreator4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR4_2, NPC_POPUP_BEANIES_VSCREATOR4_3, NPC_POPUP_BEA...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_intensestatic` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 4 |
| [`force_current_cat_use_ability`](./Enums.md#enum-force_current_cat_use_ability) | Enum | Examples: `neck_NukeBonus_remote` | 2 |

</details>

---

### Object: `beanies_vscreatorintro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATORINTRO_1, NPC_POPUP_BEANIES_VSCREATORINTRO_2, NPC_P...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 4 |

</details>

---

### Object: `beaniesquest_complete_AI`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_3, NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_AirHorn`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_AngryFace`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `beaniesquest_complete_AnimalHands`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_2, NPC_BEANIES_BEANIESQUEST_COM...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_BubbleBoy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_3, NPC_BEANIES_BEANIESQUEST_COMPL...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_ChadImplant`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_2, NPC_BEANIES_BEANIESQUEST_COM...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_ChaosDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_1, NPC_BEANIES_BEANIESQUEST_COM...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `beaniesquest_complete_DimensionalDivider`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_2, NPC_BEANIES_BEANIESQU...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_DiseaseJar`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_1, NPC_BEANIES_BEANIESQUEST_COMP...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_ExperimentalTreatment`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_3, NPC_BEANIES_BEANIE...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_FartFace`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_3, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_FigLeaf`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_3, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_Generic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_2, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_GlassCannon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_1, NPC_BEANIES_BEANIESQUEST_COM...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_HardPill`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_1, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_HiveMind`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_MagicMirror`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_2, NPC_BEANIES_BEANIESQUEST_COM...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_MeStone`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_3, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_MultilinkCable`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_MysteriousDice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_3, NPC_BEANIES_BEANIESQUEST_...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_MysteriousGlasses`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_1, NPC_BEANIES_BEANIESQUE...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_NDEDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_NuclearKnife`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_2, NPC_BEANIES_BEANIESQUEST_CO...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_PartialLobotomy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_1, NPC_BEANIES_BEANIESQUEST...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_PartyDetonator`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_2, NPC_BEANIES_BEANIESQUEST_...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_PersonalHeater`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_PersuasionDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_1, NPC_BEANIES_BEANIESQUES...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_PrincessHat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_1, NPC_BEANIES_BEANIESQUEST_COM...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_RealityScrambler`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_1, NPC_BEANIES_BEANIESQUES...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_Redacted`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_SpiderInjector`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_1, NPC_BEANIES_BEANIESQUEST_...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_Stopwatch`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_StorageLocker`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_3, NPC_BEANIES_BEANIESQUEST_C...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_TheIOU`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_1, NPC_BEANIES_BEANIESQUEST_COMPLETE...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_TheLoner`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_complete_Trapfest99`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_COMP...` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `beaniesquest_complete_UltraVision3000`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_1, NPC_BEANIES_BEANIESQUEST...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 2 |

</details>

---

### Object: `beaniesquest_fail_AI`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_AI_3, NPC_BEANIES_BEANIESQUEST_FAIL_AI_2, NPC_B...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_AirHorn`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_1, NPC_BEANIES_BEANIESQUEST_FAIL_AIRHOR...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_AngryFace`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_2, NPC_BEANIES_BEANIESQUEST_FAIL_ANGR...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_AnimalHands`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_1, NPC_BEANIES_BEANIESQUEST_FAIL_AN...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_BubbleBoy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_2, NPC_BEANIES_BEANIESQUEST_FAIL_BUBB...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_ChadImplant`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_3, NPC_BEANIES_BEANIESQUEST_FAIL_CH...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_ChaosDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_1, NPC_BEANIES_BEANIESQUEST_FAIL_CH...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_DimensionalDivider`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_3, NPC_BEANIES_BEANIESQUEST_...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_DiseaseJar`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_3, NPC_BEANIES_BEANIESQUEST_FAIL_DIS...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_ExperimentalTreatment`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_3, NPC_BEANIES_BEANIESQUE...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_FartFace`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_2, NPC_BEANIES_BEANIESQUEST_FAIL_FARTF...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_FigLeaf`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_1, NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEA...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_Generic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_1, NPC_BEANIES_BEANIESQUEST_FAIL_GENERI...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_GlassCannon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_1, NPC_BEANIES_BEANIESQUEST_FAIL_GL...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_HardPill`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_1, NPC_BEANIES_BEANIESQUEST_FAIL_HARDP...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_HiveMind`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_2, NPC_BEANIES_BEANIESQUEST_FAIL_HIVEM...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_MagicMirror`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_3, NPC_BEANIES_BEANIESQUEST_FAIL_MA...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_MeStone`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_2, NPC_BEANIES_BEANIESQUEST_FAIL_MESTON...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_MultilinkCable`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 2 |

</details>

---

### Object: `beaniesquest_fail_MysteriousDice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_MysteriousGlasses`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_3, NPC_BEANIES_BEANIESQUEST_F...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 2 |

</details>

---

### Object: `beaniesquest_fail_NDEDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_2, NPC_BEANIES_BEANIESQUEST_FAIL_NDED...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_NuclearKnife`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_3, NPC_BEANIES_BEANIESQUEST_FAIL_N...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_PartialLobotomy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_1, NPC_BEANIES_BEANIESQUEST_FAI...` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `beaniesquest_fail_PartyDetonator`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_1, NPC_BEANIES_BEANIESQUEST_FAIL...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_PersonalHeater`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_FAIL...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_PersuasionDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_1, NPC_BEANIES_BEANIESQUEST_FA...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_PrincessHat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_1, NPC_BEANIES_BEANIESQUEST_FAIL_PR...` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 2 |

</details>

---

### Object: `beaniesquest_fail_RealityScrambler`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_1, NPC_BEANIES_BEANIESQUEST_FA...` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 2 |

</details>

---

### Object: `beaniesquest_fail_Redacted`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_1, NPC_BEANIES_BEANIESQUEST_FAIL_REDAC...` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `beaniesquest_fail_SpiderInjector`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_Stopwatch`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_2, NPC_BEANIES_BEANIESQUEST_FAIL_STOP...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_StorageLocker`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_3, NPC_BEANIES_BEANIESQUEST_FAIL_...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_TheIOU`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_1, NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_TheLoner`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_3, NPC_BEANIES_BEANIESQUEST_FAIL_THELO...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_Trapfest99`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_FAIL_TRA...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `set_state, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_fail_UltraVision3000`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_3, NPC_BEANIES_BEANIESQUEST_FAI...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 2 |

</details>

---

### Object: `beaniesquest_intro_AI`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_AI_1, NPC_BEANIES_BEANIESQUEST_INTRO_AI_2, NPC...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |

</details>

---

### Object: `beaniesquest_intro_AirHorn`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_2, NPC_BEANIES_BEANIESQUEST_INTRO_AIRH...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |

</details>

---

### Object: `beaniesquest_intro_AngryFace`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_2, NPC_BEANIES_BEANIESQUEST_INTRO_AN...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `beaniesquest_intro_AnimalHands`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_1, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |

</details>

---

### Object: `beaniesquest_intro_BubbleBoy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_1, NPC_BEANIES_BEANIESQUEST_INTRO_BU...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |

</details>

---

### Object: `beaniesquest_intro_ChadImplant`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_1, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |

</details>

---

### Object: `beaniesquest_intro_ChaosDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_3, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |

</details>

---

### Object: `beaniesquest_intro_DimensionalDivider`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_1, NPC_BEANIES_BEANIESQUEST...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |

</details>

---

### Object: `beaniesquest_intro_DiseaseJar`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_1, NPC_BEANIES_BEANIESQUEST_INTRO_D...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 2 |

</details>

---

### Object: `beaniesquest_intro_ExperimentalTreatment`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_2, NPC_BEANIES_BEANIESQU...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |

</details>

---

### Object: `beaniesquest_intro_FartFace`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_1, NPC_BEANIES_BEANIESQUEST_INTRO_FAR...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |

</details>

---

### Object: `beaniesquest_intro_FigLeaf`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_1, NPC_BEANIES_BEANIESQUEST_INTRO_FIGL...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |

</details>

---

### Object: `beaniesquest_intro_Generic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_1, NPC_BEANIES_BEANIESQUEST_INTRO_GENE...` | 6 |

</details>

---

### Object: `beaniesquest_intro_GlassCannon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_2, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `beaniesquest_intro_HardPill`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_2, NPC_BEANIES_BEANIESQUEST_INTRO_HAR...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `beaniesquest_intro_HiveMind`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_1, NPC_BEANIES_BEANIESQUEST_INTRO_HIV...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |

</details>

---

### Object: `beaniesquest_intro_MagicMirror`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_3, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |

</details>

---

### Object: `beaniesquest_intro_MeStone`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_1, NPC_BEANIES_BEANIESQUEST_INTRO_MEST...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |

</details>

---

### Object: `beaniesquest_intro_MultilinkCable`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_INT...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 8 |

</details>

---

### Object: `beaniesquest_intro_MysteriousDice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_3, NPC_BEANIES_BEANIESQUEST_INT...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |

</details>

---

### Object: `beaniesquest_intro_MysteriousGlasses`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_1, NPC_BEANIES_BEANIESQUEST_...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `beaniesquest_intro_NDEDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_2, NPC_BEANIES_BEANIESQUEST_INTRO_ND...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |

</details>

---

### Object: `beaniesquest_intro_NuclearKnife`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_3, NPC_BEANIES_BEANIESQUEST_INTRO...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `beaniesquest_intro_PartialLobotomy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_3, NPC_BEANIES_BEANIESQUEST_IN...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |

</details>

---

### Object: `beaniesquest_intro_PartyDetonator`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_1, NPC_BEANIES_BEANIESQUEST_INT...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |

</details>

---

### Object: `beaniesquest_intro_PersonalHeater`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_INT...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |

</details>

---

### Object: `beaniesquest_intro_PersuasionDevice`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_3, NPC_BEANIES_BEANIESQUEST_I...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 10 |

</details>

---

### Object: `beaniesquest_intro_PrincessHat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_2, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |

</details>

---

### Object: `beaniesquest_intro_RealityScrambler`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_3, NPC_BEANIES_BEANIESQUEST_I...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `beaniesquest_intro_Redacted`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_2, NPC_BEANIES_BEANIESQUEST_INTRO_RED...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 16 |

</details>

---

### Object: `beaniesquest_intro_SpiderInjector`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_2, NPC_BEANIES_BEANIESQUEST_INT...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 8 |

</details>

---

### Object: `beaniesquest_intro_Stopwatch`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_2, NPC_BEANIES_BEANIESQUEST_INTRO_ST...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |

</details>

---

### Object: `beaniesquest_intro_StorageLocker`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_2, NPC_BEANIES_BEANIESQUEST_INTR...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `beaniesquest_intro_TheIOU`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_3, NPC_BEANIES_BEANIESQUEST_INTRO_THEIO...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 12 |

</details>

---

### Object: `beaniesquest_intro_TheLoner`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_2, NPC_BEANIES_BEANIESQUEST_INTRO_THE...` | 8 |

</details>

---

### Object: `beaniesquest_intro_Trapfest99`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_INTRO_T...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |

</details>

---

### Object: `beaniesquest_intro_UltraVision3000`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_1, NPC_BEANIES_BEANIESQUEST_IN...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 14 |

</details>

---

### Object: `boss_fight_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BOSS_FIGHT_INTRO_2, NPC_POPUP_BOSS_FIGHT_INTRO_1, NPC_POPUP_BOSS_FI...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 8 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 8 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.25, .5` | 4 |

</details>

---

### Object: `boss_fight_round2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BOSS_FIGHT_ROUND2_1, NPC_POPUP_BOSS_FIGHT_ROUND2_3, NPC_POPUP_BOSS_...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_turnorder, offscreen, butch_right` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |

</details>

---

### Object: `butch_begin_accepting_cats`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_3, NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 8 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `butch` | 2 |

</details>

---

### Object: `butch_boneyard_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_BONEYARD_INTRO_3, NPC_BUTCH_BUTCH_BONEYARD_INTRO_1, NPC_BUTCH...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 14 |

</details>

---

### Object: `butch_first_house_boss_beat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_2, NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEA...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |

</details>

---

### Object: `butch_pyro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_PYRO_2, NPC_BUTCH_BUTCH_PYRO_1, NPC_BUTCH_BUTCH_PYRO_3` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 8 |

</details>

---

### Object: `butch_tina1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TINA1_3, NPC_BUTCH_BUTCH_TINA1_2, NPC_BUTCH_BUTCH_TINA1_1` | 28 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 16 |

</details>

---

### Object: `butch_tips_backstab`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_BACKSTAB_1, NPC_BUTCH_BUTCH_TIPS_BACKSTAB_3, NPC_BUTCH_B...` | 6 |

</details>

---

### Object: `butch_tips_charisma`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_CHARISMA_1, NPC_BUTCH_BUTCH_TIPS_CHARISMA_2, NPC_BUTCH_B...` | 6 |

</details>

---

### Object: `butch_tips_combat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_COMBAT_1, NPC_BUTCH_BUTCH_TIPS_COMBAT_2, NPC_BUTCH_BUTCH...` | 8 |

</details>

---

### Object: `butch_tips_disorders`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_DISORDERS_3, NPC_BUTCH_BUTCH_TIPS_DISORDERS_2, NPC_BUTCH...` | 6 |

</details>

---

### Object: `butch_tips_drafting`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_DRAFTING_2, NPC_BUTCH_BUTCH_TIPS_DRAFTING_3, NPC_BUTCH_B...` | 6 |

</details>

---

### Object: `butch_tips_elements`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_1, NPC_BUTCH_BUTCH_TIPS_ELEMENTS_2, NPC_BUTCH_B...` | 10 |

</details>

---

### Object: `butch_tips_hard`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HARD_3, NPC_BUTCH_BUTCH_TIPS_HARD_1, NPC_BUTCH_BUTCH_TIP...` | 10 |

</details>

---

### Object: `butch_tips_headhome`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HEADHOME_2, NPC_BUTCH_BUTCH_TIPS_HEADHOME_1, NPC_BUTCH_B...` | 8 |

</details>

---

### Object: `butch_tips_houseboss`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_3, NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_1, NPC_BUTCH...` | 6 |

</details>

---

### Object: `butch_tips_info`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INFO_2, NPC_BUTCH_BUTCH_TIPS_INFO_1` | 4 |

</details>

---

### Object: `butch_tips_intelligence`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_2, NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_3, NPC...` | 8 |

</details>

---

### Object: `butch_tips_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INTRO_1, NPC_BUTCH_BUTCH_TIPS_INTRO_3, NPC_BUTCH_BUTCH_T...` | 8 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `butch_tips_intelligence` | 2 |

</details>

---

### Object: `butch_tips_items`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_ITEMS_1, NPC_BUTCH_BUTCH_TIPS_ITEMS_2` | 4 |

</details>

---

### Object: `butch_tips_lesscats`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_LESSCATS_2, NPC_BUTCH_BUTCH_TIPS_LESSCATS_1, NPC_BUTCH_B...` | 6 |

</details>

---

### Object: `butch_tips_magicdamage`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_2, NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_1, NPC_B...` | 8 |

</details>

---

### Object: `butch_tips_passives`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_PASSIVES_1, NPC_BUTCH_BUTCH_TIPS_PASSIVES_3, NPC_BUTCH_B...` | 6 |

</details>

---

### Object: `butch_tips_reorient`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_REORIENT_2, NPC_BUTCH_BUTCH_TIPS_REORIENT_1, NPC_BUTCH_B...` | 10 |

</details>

---

### Object: `butch_tips_rewards`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_REWARDS_3, NPC_BUTCH_BUTCH_TIPS_REWARDS_2, NPC_BUTCH_BUT...` | 8 |

</details>

---

### Object: `butch_tips_tacticalview`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_1, NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_2, NPC...` | 6 |

</details>

---

### Object: `butch_tips_turnorder`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_TURNORDER_3, NPC_BUTCH_BUTCH_TIPS_TURNORDER_1, NPC_BUTCH...` | 6 |

</details>

---

### Object: `butch_tips_wellrounded`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_3, NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_2, NPC_B...` | 10 |

</details>

---

### Object: `can_still_use_attack`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_1, NPC_POPUP_CAN_STILL_USE_ATTACK_2` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_3` | 2 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `can_still_use_attack_didntspell` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `can_still_use_attack_didntspell`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_2` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_1` | 2 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `can_still_use_attack` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_a`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_A_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_b`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_B_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_c`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_C_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_d`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_D_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_iceage`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_ICEAGE_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_jurassic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_JURASSIC_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_moon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_MOON_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `cant_afford_theend`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_THEEND_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `class_unlock_butcher`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_2, NPC_BUTCH_CLASS_UNLOCK_BUTCHER_3, NPC_BUTCH...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Butcher` | 2 |

</details>

---

### Object: `class_unlock_druid`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_DRUID_1, NPC_BUTCH_CLASS_UNLOCK_DRUID_3, NPC_BUTCH_CLA...` | 8 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Druid` | 2 |

</details>

---

### Object: `class_unlock_jester`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_JESTER_1, NPC_BUTCH_CLASS_UNLOCK_JESTER_3, NPC_BUTCH_C...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Jester` | 2 |

</details>

---

### Object: `class_unlock_medic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_MEDIC_2, NPC_BUTCH_CLASS_UNLOCK_MEDIC_1, NPC_BUTCH_CLA...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 6 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Medic` | 2 |

</details>

---

### Object: `class_unlock_monk`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_MONK_3, NPC_BUTCH_CLASS_UNLOCK_MONK_1, NPC_BUTCH_CLASS...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Monk` | 2 |

</details>

---

### Object: `class_unlock_necromancer`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_3, NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_2, N...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Necromancer` | 2 |

</details>

---

### Object: `class_unlock_psychic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_3, NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_2, NPC_BUTCH...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Psychic` | 2 |

</details>

---

### Object: `class_unlock_thief`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_THIEF_2, NPC_BUTCH_CLASS_UNLOCK_THIEF_1, NPC_BUTCH_CLA...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Thief` | 2 |

</details>

---

### Object: `class_unlock_tinkerer`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_TINKERER_3, NPC_BUTCH_CLASS_UNLOCK_TINKERER_1, NPC_BUT...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Tinkerer` | 2 |

</details>

---

### Object: `collected_new_items`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_3, NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle2, blocking` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_5` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `collected_nothing`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NOTHING_1, NPC_ORGANGRINDER_COLLECTED_NOTHING_3, N...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle2, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `do_not_end_turn`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `do_not_end_turn` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_DO_NOT_END_TURN_1` | 2 |

</details>

---

### Object: `done_spitting_fail_ally`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_ALLY_2, NPC_POPUP_DONE_SPITTING_FAIL_ALLY_3, NPC...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `done_spitting_fail_miss`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_MISS_1, NPC_POPUP_DONE_SPITTING_FAIL_MISS_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `done_spitting_fail_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_RAT_1, NPC_POPUP_DONE_SPITTING_FAIL_RAT_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway` | 2 |

</details>

---

### Object: `done_spitting_success`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_SUCCESS_2, NPC_POPUP_DONE_SPITTING_SUCCESS_3, NPC_POP...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ending`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_ENDING_1, NPC_BEANIES_ENDING_2, NPC_BEANIES_ENDING_3` | 38 |
| [`screenshake`](./Arrays.md#array-screenshake) | Array | Examples: `[ 1 30 ]` | 1 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `BeaniesEnding_Banging` | 2 |

</details>

---

### Object: `finish_adventure`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FINISH_ADVENTURE_1, NPC_POPUP_FINISH_ADVENTURE_2, NPC_POPUP_FINISH_...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, butch_point_food, butch_point_save` | 10 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 10 |

</details>

---

### Object: `first_fight_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_FIGHT_INTRO_3, NPC_POPUP_FIRST_FIGHT_INTRO_2, NPC_POPUP_FIRST...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_team, butch_point_enemies` | 16 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHint, UISFX_ButchMove` | 12 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected, cat_turn` | 4 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_FIRST_FIGHT_INTRO_14` | 2 |
| [`set_mood`](./Enums.md#enum-set_mood) | Enum | Examples: `default` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `first_house_boss_tomorrow`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_3, NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_1,...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `first_house_hint_retired`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_2, NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_3, N...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `frank_caves_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_CAVES_INTRO_1, NPC_FRANK_FRANK_CAVES_INTRO_2, NPC_FRANK_FRANK...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup` | 10 |

</details>

---

### Object: `frank_ending`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_ENDING_1, NPC_FRANK_FRANK_ENDING_2, NPC_FRANK_FRANK_ENDING_3` | 32 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 16 |

</details>

---

### Object: `frank_max1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX1_2, NPC_FRANK_FRANK_MAX1_3, NPC_FRANK_FRANK_MAX1_1` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `frank_max2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX2_1, NPC_FRANK_FRANK_MAX2_3, NPC_FRANK_FRANK_MAX2_2` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `frank_max3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX3_3, NPC_FRANK_FRANK_MAX3_2, NPC_FRANK_FRANK_MAX3_1` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `frank_max4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX4_3, NPC_FRANK_FRANK_MAX4_1, NPC_FRANK_FRANK_MAX4_2` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `frank_max5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX5_1, NPC_FRANK_FRANK_MAX5_2, NPC_FRANK_FRANK_MAX5_3` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `frank_max_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX_INTRO_2, NPC_FRANK_FRANK_MAX_INTRO_3, NPC_FRANK_FRANK_MAX...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `frank_max_repeating`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ frank_max1 frank_max2 frank_max3 frank_max4 frank_max5 ]` | 1 |

</details>

---

### Object: `frank_terminator2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TERMINATOR2_2, NPC_FRANK_FRANK_TERMINATOR2_3, NPC_FRANK_FRANK...` | 30 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 16 |

</details>

---

### Object: `frank_tips_1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_1_1, NPC_FRANK_FRANK_TIPS_1_2, NPC_FRANK_FRANK_TIPS_1_3` | 8 |

</details>

---

### Object: `frank_tips_10`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_10_2, NPC_FRANK_FRANK_TIPS_10_1, NPC_FRANK_FRANK_TIPS_10_3` | 8 |

</details>

---

### Object: `frank_tips_2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_2_1, NPC_FRANK_FRANK_TIPS_2_2, NPC_FRANK_FRANK_TIPS_2_3` | 6 |

</details>

---

### Object: `frank_tips_3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_3_3, NPC_FRANK_FRANK_TIPS_3_2, NPC_FRANK_FRANK_TIPS_3_1` | 6 |

</details>

---

### Object: `frank_tips_4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_4_3, NPC_FRANK_FRANK_TIPS_4_2, NPC_FRANK_FRANK_TIPS_4_1` | 6 |

</details>

---

### Object: `frank_tips_5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_5_1, NPC_FRANK_FRANK_TIPS_5_3, NPC_FRANK_FRANK_TIPS_5_2` | 10 |

</details>

---

### Object: `frank_tips_6`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_6_2, NPC_FRANK_FRANK_TIPS_6_1, NPC_FRANK_FRANK_TIPS_6_3` | 6 |

</details>

---

### Object: `frank_tips_7`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_7_3, NPC_FRANK_FRANK_TIPS_7_2, NPC_FRANK_FRANK_TIPS_7_1` | 6 |

</details>

---

### Object: `frank_tips_8`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_8_2, NPC_FRANK_FRANK_TIPS_8_1, NPC_FRANK_FRANK_TIPS_8_3` | 6 |

</details>

---

### Object: `frank_tips_9`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_9_2, NPC_FRANK_FRANK_TIPS_9_1` | 4 |

</details>

---

### Object: `gone`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `gone` | 2 |

</details>

---

### Object: `house_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_INTRO_1, NPC_POPUP_HOUSE_INTRO_2, NPC_POPUP_HOUSE_INTRO_3` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_cats` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_HOUSE_INTRO_11` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click` | 2 |

</details>

---

### Object: `house_kitten_box`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_KITTEN_BOX_2, NPC_POPUP_HOUSE_KITTEN_BOX_1` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `house_pass_day`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PASS_DAY_3, NPC_POPUP_HOUSE_PASS_DAY_1, NPC_POPUP_HOUSE_PASS_...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_food` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |

</details>

---

### Object: `house_pass_day2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PASS_DAY2_3, NPC_POPUP_HOUSE_PASS_DAY2_1, NPC_POPUP_HOUSE_PAS...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `house_pipe`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PIPE_1, NPC_POPUP_HOUSE_PIPE_2, NPC_POPUP_HOUSE_PIPE_3` | 40 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `frank_right, offscreen, frank_point_pipe` | 8 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 8 |

</details>

---

### Object: `house_retired_cat_box`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMove` | 4 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_RETIRED_CAT_BOX_1` | 2 |

</details>

---

### Object: `house_starred_box`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_STARRED_BOX_1, NPC_POPUP_HOUSE_STARRED_BOX_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `house_strays`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_STRAYS_3, NPC_POPUP_HOUSE_STRAYS_2, NPC_POPUP_HOUSE_STRAYS_1` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_strays` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_HOUSE_STRAYS_5` | 2 |
| [`request_cat_info`](./Enums.md#enum-request_cat_info) | Enum | Examples: `stray` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click` | 2 |

</details>

---

### Object: `house_upgrade_4throom`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_4THROOM_3, NPC_FRANK_HOUSE_UPGRADE_4THROOM_2, NPC_FRA...` | 34 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 20 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_attic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_ATTIC_3, NPC_FRANK_HOUSE_UPGRADE_ATTIC_2, NPC_FRANK_H...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_basement`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT_1` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_basement2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT2_1` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_basement3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT3_1` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_basement4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT4_1` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_basement5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT5_1` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_largehouse`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_3, NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_1, N...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `house_upgrade_mediumhouse`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_2, NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_3,...` | 42 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 24 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_INTRO_3, NPC_BEANIES_INTRO_1, NPC_BEANIES_INTRO_2` | 52 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 20 |
| [`set_mood`](./Enums.md#enum-set_mood) | Enum | Examples: `veryhappy, happy, default` | 18 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `reject_cat, choose_cat2, choose_cat1` | 6 |
| [`delay`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | Examples: `.05, 5.4` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_BEANIES_INTRO_15` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `Intro_LabDisposal` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `introduce_hard_path`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_INTRODUCE_HARD_PATH_1, NPC_POPUP_INTRODUCE_HARD_PATH_3, NPC_POPUP_I...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `jack_begin_accepting_cats`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_2, NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_3, N...` | 32 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 10 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `jack` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_desert_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_DESERT_INTRO_1, NPC_JACK_JACK_DESERT_INTRO_3, NPC_JACK_JACK_DES...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 10 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_introduction`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_JACK_INTRODUCTION_2, NPC_POPUP_JACK_INTRODUCTION_3, NPC_POPUP_JACK_...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `jack_point_furniture, offscreen, jack_right` | 8 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 8 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_JACK_INTRODUCTION_7` | 2 |
| [`get_random_furniture_piece`](./Arrays.md#array-get_random_furniture_piece) | Array | Examples: `[ small_trash_cans small_trash_can2 ]` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `open_furniture` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_max1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 8 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX1_3, NPC_JACK_JACK_MAX1_2, NPC_JACK_JACK_MAX1_1` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_max2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX2_2, NPC_JACK_JACK_MAX2_1, NPC_JACK_JACK_MAX2_3` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_max3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX3_1, NPC_JACK_JACK_MAX3_2, NPC_JACK_JACK_MAX3_3` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_max4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX4_1, NPC_JACK_JACK_MAX4_3, NPC_JACK_JACK_MAX4_2` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_max5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX5_2, NPC_JACK_JACK_MAX5_1, NPC_JACK_JACK_MAX5_3` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_max_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX_INTRO_3, NPC_JACK_JACK_MAX_INTRO_2, NPC_JACK_JACK_MAX_INTRO_1` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_max_repeating`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ jack_max1 jack_max2 jack_max3 jack_max4 jack_max5 ]` | 1 |

</details>

---

### Object: `jack_shopupgrade1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE1_3, NPC_JACK_JACK_SHOPUPGRADE1_2, NPC_JACK_JACK_SHO...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_shopupgrade2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE2_2, NPC_JACK_JACK_SHOPUPGRADE2_1, NPC_JACK_JACK_SHO...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_shopupgrade3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE3_3, NPC_JACK_JACK_SHOPUPGRADE3_2, NPC_JACK_JACK_SHO...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_shopupgrade4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE4_3, NPC_JACK_JACK_SHOPUPGRADE4_2, NPC_JACK_JACK_SHO...` | 32 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 16 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `jack_zara`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_ZARA_3, NPC_JACK_JACK_ZARA_1, NPC_JACK_JACK_ZARA_2` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle, blocking` | 8 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `level_up_didnt_select_sunburn`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_1, NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SU...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `level_up_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_INTRO_1, NPC_POPUP_LEVEL_UP_INTRO_2, NPC_POPUP_LEVEL_UP_IN...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_levelup, butch_point_hotblooded, butch_point_sunburn` | 10 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 8 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click, hovered_passive` | 4 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_LEVEL_UP_INTRO_6` | 2 |
| `lock_mouse` | Number | Examples: `1` | 2 |
| `unlock_mouse` | Number | Examples: `1` | 2 |

</details>

---

### Object: `level_up_selected_sunburn`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_2, NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_1,...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `low_on_food`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `tink_point_box, tink_left, tink_point_food` | 8 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 8 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LOW_ON_FOOD_3, NPC_POPUP_LOW_ON_FOOD_1, NPC_POPUP_LOW_ON_FOOD_2` | 6 |

</details>

---

### Object: `map_click_node`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_mapnode, offscreen` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_CLICK_NODE_1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `mapnode_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `map_equip_items`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, butch_point_inventory, offscreen` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 6 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS_2` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS_1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `inventory_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `map_equip_items2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_point_inventory` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint` | 4 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `map_equip_items2` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS2_1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `inventory_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_attack_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMoveHint, UISFX_ButchMove` | 6 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_ATTACK_RAT_2, NPC_POPUP_MELEE_ATTACK_RAT_1` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_ATTACK_RAT_3` | 2 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `ranged_cat_attack` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_cat_spit`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_spells` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_2, NPC_POPUP_MELEE_CAT_SPIT_1` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_3` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_cat_spit_fail_ally`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_2, NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_1, N...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_4` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_cat_spit_fail_miss`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_2, NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_3, N...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_4` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_cat_spit_fail_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_1, NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_2, NPC...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_4` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_cat_spit_ignore`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `melee_cat_spit_ignore` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_2` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_cat_spit_success`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_2, NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_3, NPC_P...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_4` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_killed_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_passives, butch_point_team_nocircle` | 10 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHintDelay1, UISFX_ButchMove` | 8 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_KILLED_RAT_2, NPC_POPUP_MELEE_KILLED_RAT_1, NPC_POPUP_MELEE_K...` | 6 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click, hovered_passive` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_KILLED_RAT_3` | 2 |
| `unlock_mouse` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_move2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_move` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMoveHint, UISFX_ButchMove` | 6 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `melee_move2` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_MOVE2_2` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_MOVE2_1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `melee_out_of_actions`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHintDelay1, UISFX_ButchHint` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_mana, butch_point_cost, butch_point_spells` | 10 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_OUT_OF_ACTIONS_2, NPC_POPUP_MELEE_OUT_OF_ACTIONS_1, NPC_POPUP...` | 6 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_OUT_OF_ACTIONS_4` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `end_turn` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `new_adventure`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `tink_point_box, offscreen, tink_left` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_NEW_ADVENTURE_2, NPC_POPUP_NEW_ADVENTURE_1` | 4 |

</details>

---

### Object: `organ_boneyard_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_3, NPC_ORGANGRINDER_ORGAN_BONEYARD_INTR...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 12 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_INTRO_1, NPC_ORGANGRINDER_ORGAN_INTRO_2, NPC_ORGANGRIN...` | 38 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 18 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `organgrinder` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_INTRO_20` | 2 |
| [`set_organ_name`](./Strings.md#string-set_organ_name) | String | Examples: `"Tyler"` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_max1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX1_1, NPC_ORGANGRINDER_ORGAN_MAX1_3, NPC_ORGANGRINDE...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle, idle2` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_max2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX2_1, NPC_ORGANGRINDER_ORGAN_MAX2_3, NPC_ORGANGRINDE...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_max3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX3_3, NPC_ORGANGRINDER_ORGAN_MAX3_1, NPC_ORGANGRINDE...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_max4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX4_2, NPC_ORGANGRINDER_ORGAN_MAX4_3, NPC_ORGANGRINDE...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_max5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX5_1, NPC_ORGANGRINDER_ORGAN_MAX5_2, NPC_ORGANGRINDE...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_max_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_3, NPC_ORGANGRINDER_ORGAN_MAX_INTRO_1, NPC_O...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_max_repeating`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ organ_max1 organ_max2 organ_max3 organ_max4 organ_max5 ]` | 1 |

</details>

---

### Object: `organ_rename`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_RENAME_3, NPC_ORGANGRINDER_ORGAN_RENAME_1, NPC_ORGANGR...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`set_organ_name`](./Strings.md#string-set_organ_name) | String | Examples: `"Tyler"` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_throbbingdomain_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_2, NPC_ORGANGRINDER_ORGAN_THROBB...` | 32 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 18 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_tina3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_TINA3_1, NPC_ORGANGRINDER_ORGAN_TINA3_2, NPC_ORGANGRIN...` | 32 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 26 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_unlock`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UNLOCK_1, NPC_ORGANGRINDER_ORGAN_UNLOCK_3, NPC_ORGANGR...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_upgrade1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE1_3, NPC_ORGANGRINDER_ORGAN_UPGRADE1_1, NPC_ORG...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_upgrade2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE2_2, NPC_ORGANGRINDER_ORGAN_UPGRADE2_3, NPC_ORG...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_upgrade3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE3_1, NPC_ORGANGRINDER_ORGAN_UPGRADE3_2, NPC_ORG...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_upgrade4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE4_1, NPC_ORGANGRINDER_ORGAN_UPGRADE4_2, NPC_ORG...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_upgrade5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE5_1, NPC_ORGANGRINDER_ORGAN_UPGRADE5_3, NPC_ORG...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `organ_upgrade6`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE6_1, NPC_ORGANGRINDER_ORGAN_UPGRADE6_2, NPC_ORG...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_a`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_A_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_b`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_B_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_c`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_C_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_d`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_D_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_iceage`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_ICEAGE_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_jurassic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_JURASSIC_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_moon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_MOON_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `purchase_item_theend`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_THEEND_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `ranged_attack_tomtom`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_attack_tomtom_fail_ally`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_ALLY_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_FA...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_attack_tomtom_fail_miss`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_2, NPC_POPUP_RANGED_ATTACK_TOMTOM_FA...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_attack_tomtom_fail_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_RAT_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_FAI...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_attack`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ATTACK_1` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `ranged_cat_early_attack2_ally`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_early_attack2_miss`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_early_attack2_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_early_attack_ally`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_A...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_early_attack_miss`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_M...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_early_attack_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_2, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RA...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_failmove`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_FAILMOVE_1, NPC_POPUP_RANGED_CAT_FAILMOVE_2, NPC_POPUP_R...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `ranged_cat_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_attack, butch_point_move` | 8 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHint, UISFX_ButchMove` | 8 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_INTRO_3, NPC_POPUP_RANGED_CAT_INTRO_1, NPC_POPUP_RANGED_...` | 6 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_INTRO_4` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `ranged_cat_roll`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_cost2, butch_right, butch_point_spells` | 12 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchHintDelay2, UISFX_ButchHint, UISFX_ButchMove` | 12 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLL_1, NPC_POPUP_RANGED_CAT_ROLL_2, NPC_POPUP_RANGED_CA...` | 10 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLL_6` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `ranged_cat_rolled_first`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_3, NPC_POPUP_RANGED_CAT_ROLLED_FIRST_1, NPC...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_move` | 6 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_4` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_100`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_100_2, NPC_STEVEN_STEVEN_100_1, NPC_STEVEN_STEVEN_100_3` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 6 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_introduction`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_INTRODUCTION_2, NPC_STEVEN_STEVEN_INTRODUCTION_3, NPC_STEVE...` | 38 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 26 |
| [`blocking`](./Enums.md#enum-blocking) | Enum | Examples: `idlenoani` | 6 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_milliontrashed`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_MILLIONTRASHED_3, NPC_STEVEN_STEVEN_MILLIONTRASHED_1, NPC_S...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `steven_postendgame`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_POSTENDGAME_1, NPC_STEVEN_STEVEN_POSTENDGAME_2, NPC_STEVEN_...` | 30 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 20 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_resummon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_RESUMMON_1` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_savescum_1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_1alt1 steven_savescum_1alt2 steven_save...` | 1 |

</details>

---

### Object: `steven_savescum_100`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_100_3, NPC_POPUP_STEVEN_SAVESCUM_100_2, NPC_POPUP_S...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_1alt1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_1ALT1_1, NPC_POP...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_1alt2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_1, NPC_POPUP_STEVEN_SAVESCUM_1ALT2_2, NPC_POP...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_1alt3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_2, NPC_POPUP_STEVEN_SAVESCUM_1ALT3_1, NPC_POP...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_2alt1 steven_savescum_2alt2 steven_save...` | 1 |

</details>

---

### Object: `steven_savescum_2alt1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_2ALT1_1, NPC_POP...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 6 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_2alt2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_2, NPC_POPUP_STEVEN_SAVESCUM_2ALT2_3, NPC_POP...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 6 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_2alt3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_3, NPC_POPUP_STEVEN_SAVESCUM_2ALT3_2, NPC_POP...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 8 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_3alt1 steven_savescum_3alt2 steven_save...` | 1 |

</details>

---

### Object: `steven_savescum_3alt1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT1_2, NPC_POP...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_3alt2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT2_1, NPC_POP...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_3alt3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT3_2, NPC_POP...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_4alt1 steven_savescum_4alt2 steven_save...` | 1 |

</details>

---

### Object: `steven_savescum_4alt1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT1_1, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_4alt2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT2_1, NPC_POP...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_4alt3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT3_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT3_3, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_houseboss_1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_1, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 2 |

</details>

---

### Object: `steven_savescum_houseboss_100`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_2, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOS...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 2 |

</details>

---

### Object: `steven_savescum_houseboss_2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_3, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 2 |

</details>

---

### Object: `steven_savescum_houseboss_3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_1, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 38 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 2 |

</details>

---

### Object: `steven_savescum_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_INTRO_1, NPC_POPUP_STEVEN_SAVESCUM_INTRO_3, NPC_POP...` | 48 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 2 |

</details>

---

### Object: `steven_savescum_intro_houseboss`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_3, NPC_POPUP_STEVEN_SAVESCUM_INTRO_...` | 40 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 2 |

</details>

---

### Object: `steven_unlock_act1_crazy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 16 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_3, NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_2,...` | 12 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_unlock_act1_impossible`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_3, NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMP...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `talking, closeup, idle` | 8 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_unlock_act2_crazy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_1, NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_2,...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 10 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_unlock_act2_hard`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_3, NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_2, N...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 8 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_unlock_act2_impossible`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_2, NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMP...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, talking, idle` | 8 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_unlock_act3_crazy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_3, NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_2,...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 8 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_unlock_act3_hard`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_2, NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_1, N...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 16 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `steven_unlock_act3_impossible`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_3, NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMP...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 12 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `take_cats_inside`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `take_cats_inside` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TAKE_CATS_INSIDE_1` | 2 |

</details>

---

### Object: `test_gamepad_prompts`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dialog` | Mixed | Examples: `"Switch to gamepad now if you wanna see gamepad bindings.", NPC_POPUP_FIRST_F...` | 16 |

</details>

---

### Object: `tink_aggression`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_AGGRESSION_2, NPC_TINK_TINK_AGGRESSION_1, NPC_TINK_TINK_AGGRESS...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, zoomedout, idle` | 22 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_basestats`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_BASESTATS_1, NPC_TINK_TINK_BASESTATS_2, NPC_TINK_TINK_BASESTATS_3` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_begin_accepting_cats`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_3, NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_2, N...` | 42 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 24 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `tink` | 2 |

</details>

---

### Object: `tink_inbreeding`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_INBREEDING_2, NPC_TINK_TINK_INBREEDING_3, NPC_TINK_TINK_INBREED...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX1_3, NPC_TINK_TINK_MAX1_1, NPC_TINK_TINK_MAX1_2` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max10`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX10_3, NPC_TINK_TINK_MAX10_1, NPC_TINK_TINK_MAX10_2` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX2_3, NPC_TINK_TINK_MAX2_2, NPC_TINK_TINK_MAX2_1` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX3_2, NPC_TINK_TINK_MAX3_3, NPC_TINK_TINK_MAX3_1` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX4_3, NPC_TINK_TINK_MAX4_2, NPC_TINK_TINK_MAX4_1` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX5_3, NPC_TINK_TINK_MAX5_1, NPC_TINK_TINK_MAX5_2` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max6`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX6_2, NPC_TINK_TINK_MAX6_1, NPC_TINK_TINK_MAX6_3` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max7`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX7_2, NPC_TINK_TINK_MAX7_3, NPC_TINK_TINK_MAX7_1` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `tink_max8`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX8_2, NPC_TINK_TINK_MAX8_1, NPC_TINK_TINK_MAX8_3` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max9`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX9_2, NPC_TINK_TINK_MAX9_1, NPC_TINK_TINK_MAX9_3` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX_INTRO_2, NPC_TINK_TINK_MAX_INTRO_3, NPC_TINK_TINK_MAX_INTRO_1` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_max_repeating`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ tink_max1 tink_max2 tink_max3 tink_max4 tink_max5 tink_...` | 1 |

</details>

---

### Object: `tink_prettybow`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_PRETTYBOW_3, NPC_TINK_TINK_PRETTYBOW_2, NPC_TINK_TINK_PRETTYBOW_1` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_relationships`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_RELATIONSHIPS_3, NPC_TINK_TINK_RELATIONSHIPS_1, NPC_TINK_TINK_R...` | 40 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 26 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_sexuality`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_SEXUALITY_2, NPC_TINK_TINK_SEXUALITY_3, NPC_TINK_TINK_SEXUALITY_1` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_tags`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TAGS_1, NPC_TINK_TINK_TAGS_2, NPC_TINK_TINK_TAGS_3` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `tink_terminator`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TERMINATOR_2, NPC_TINK_TINK_TERMINATOR_1, NPC_TINK_TINK_TERMINA...` | 30 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 10 |

</details>

---

### Object: `tink_tina2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TINA2_2, NPC_TINK_TINK_TINA2_1, NPC_TINK_TINK_TINA2_3` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Object: `tink_tips_appeal`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_APPEAL_3, NPC_TINK_TINK_TIPS_APPEAL_2, NPC_TINK_TINK_TIPS_...` | 8 |

</details>

---

### Object: `tink_tips_basestats`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_BASESTATS_2, NPC_TINK_TINK_TIPS_BASESTATS_1, NPC_TINK_TINK...` | 6 |

</details>

---

### Object: `tink_tips_cleaning`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_CLEANING_2, NPC_TINK_TINK_TIPS_CLEANING_1, NPC_TINK_TINK_T...` | 8 |

</details>

---

### Object: `tink_tips_comfort`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_COMFORT_3, NPC_TINK_TINK_TIPS_COMFORT_2, NPC_TINK_TINK_TIP...` | 8 |

</details>

---

### Object: `tink_tips_health`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_HEALTH_1, NPC_TINK_TINK_TIPS_HEALTH_3, NPC_TINK_TINK_TIPS_...` | 10 |

</details>

---

### Object: `tink_tips_inbreeding`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_INBREEDING_1, NPC_TINK_TINK_TIPS_INBREEDING_2, NPC_TINK_TI...` | 10 |

</details>

---

### Object: `tink_tips_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_INTRO_3, NPC_TINK_TINK_TIPS_INTRO_1, NPC_TINK_TINK_TIPS_IN...` | 8 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `tink_tips_comfort` | 2 |

</details>

---

### Object: `tink_tips_multiclassing`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_MULTICLASSING_3, NPC_TINK_TINK_TIPS_MULTICLASSING_2, NPC_T...` | 10 |

</details>

---

### Object: `tink_tips_mutation`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_MUTATION_2, NPC_TINK_TINK_TIPS_MUTATION_1, NPC_TINK_TINK_T...` | 8 |

</details>

---

### Object: `tink_tips_stimulation`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_STIMULATION_3, NPC_TINK_TINK_TIPS_STIMULATION_2, NPC_TINK_...` | 14 |

</details>

---

### Object: `tracy_blankcollar1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR1_1, NPC_TRACY_TRACY_BLANKCOLLAR1_3, NPC_TRACY_TRA...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 16 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_blankcollar2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR2_1, NPC_TRACY_TRACY_BLANKCOLLAR2_3, NPC_TRACY_TRA...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_blankcollar3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR3_2, NPC_TRACY_TRACY_BLANKCOLLAR3_3, NPC_TRACY_TRA...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodbonus1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODBONUS1_2, NPC_TRACY_TRACY_FOODBONUS1_1` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE1_3, NPC_TRACY_TRACY_FOODSTORAGE1_1, NPC_TRACY_TRA...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage10`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE10_2, NPC_TRACY_TRACY_FOODSTORAGE10_1, NPC_TRACY_T...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE2_3, NPC_TRACY_TRACY_FOODSTORAGE2_2, NPC_TRACY_TRA...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE3_1, NPC_TRACY_TRACY_FOODSTORAGE3_2, NPC_TRACY_TRA...` | 32 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 18 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE4_3, NPC_TRACY_TRACY_FOODSTORAGE4_1, NPC_TRACY_TRA...` | 30 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 18 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE5_1, NPC_TRACY_TRACY_FOODSTORAGE5_3, NPC_TRACY_TRA...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage6`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE6_1, NPC_TRACY_TRACY_FOODSTORAGE6_2, NPC_TRACY_TRA...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage7`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE7_2, NPC_TRACY_TRACY_FOODSTORAGE7_3, NPC_TRACY_TRA...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage8`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE8_2, NPC_TRACY_TRACY_FOODSTORAGE8_1, NPC_TRACY_TRA...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_foodstorage9`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE9_3, NPC_TRACY_TRACY_FOODSTORAGE9_2, NPC_TRACY_TRA...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_idol1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL1_3, NPC_TRACY_TRACY_IDOL1_2, NPC_TRACY_TRACY_IDOL1_1` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_idol2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL2_3, NPC_TRACY_TRACY_IDOL2_1, NPC_TRACY_TRACY_IDOL2_2` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_idol3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL3_2, NPC_TRACY_TRACY_IDOL3_1, NPC_TRACY_TRACY_IDOL3_3` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_idol4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL4_2, NPC_TRACY_TRACY_IDOL4_3, NPC_TRACY_TRACY_IDOL4_1` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_idol5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL5_3, NPC_TRACY_TRACY_IDOL5_2, NPC_TRACY_TRACY_IDOL5_1` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_idol6`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL6_1, NPC_TRACY_TRACY_IDOL6_3, NPC_TRACY_TRACY_IDOL6_2` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_idol7`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL7_1, NPC_TRACY_TRACY_IDOL7_3, NPC_TRACY_TRACY_IDOL7_2` | 34 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 22 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_introduction`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_INTRODUCTION_3, NPC_TRACY_TRACY_INTRODUCTION_2, NPC_TRACY_TRA...` | 44 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 26 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `tracy` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_kaijufight`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_KAIJUFIGHT_2, NPC_TRACY_TRACY_KAIJUFIGHT_1, NPC_TRACY_TRACY_K...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 14 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_max1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 10 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX1_2, NPC_TRACY_TRACY_MAX1_1, NPC_TRACY_TRACY_MAX1_3` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_max2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 10 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX2_3, NPC_TRACY_TRACY_MAX2_2, NPC_TRACY_TRACY_MAX2_1` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_max3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX3_2, NPC_TRACY_TRACY_MAX3_1, NPC_TRACY_TRACY_MAX3_3` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_max4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX4_3, NPC_TRACY_TRACY_MAX4_2, NPC_TRACY_TRACY_MAX4_1` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_max5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX5_1, NPC_TRACY_TRACY_MAX5_2, NPC_TRACY_TRACY_MAX5_3` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 14 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_max_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX_INTRO_2, NPC_TRACY_TRACY_MAX_INTRO_1, NPC_TRACY_TRACY_MAX...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, zoomedout, blocking` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| `lock_controls` | Number | Examples: `1` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `tracy_max_repeating`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ tracy_max1 tracy_max2 tracy_max3 tracy_max4 tracy_max5 ]` | 1 |

</details>

---

### Object: `try_again_attack_rat`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_1, NPC_POPUP_TRY_AGAIN_ATTACK_RAT_3, NPC_POPUP...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHintDelay1, UISFX_ButchMove` | 6 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `try_again_attack_rat` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_4` | 2 |
| [`reset_turn`](./Enums.md#enum-reset_turn) | Enum | Examples: `act` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `try_again_melee_move`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_MELEE_MOVE_1, NPC_POPUP_TRY_AGAIN_MELEE_MOVE_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMove` | 4 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `try_again_melee_move` | 2 |
| [`reset_turn`](./Enums.md#enum-reset_turn) | Enum | Examples: `both` | 2 |

</details>

---

### Object: `tutorial_cat_dies`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TUTORIAL_CAT_DIES_1, NPC_POPUP_TUTORIAL_CAT_DIES_3, NPC_POPUP_TUTOR...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |

</details>

---

### Object: `unprompted1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED1_1` | 2 |

</details>

---

### Object: `unprompted2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED2_1, NPC_BEANIES_UNPROMPTED2_2` | 4 |

</details>

---

### Object: `unprompted3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED3_2, NPC_BEANIES_UNPROMPTED3_1, NPC_BEANIES_UNPROMPTED3_3` | 6 |

</details>

---

### Object: `unprompted4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED4_1` | 2 |

</details>

---

### Object: `unprompted5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED5_1, NPC_BEANIES_UNPROMPTED5_2` | 4 |

</details>

---

### Object: `unprompted6`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED6_2, NPC_BEANIES_UNPROMPTED6_3, NPC_BEANIES_UNPROMPTED6_1` | 6 |

</details>

---

### Object: `upgrade_storage_1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_1_3, NPC_BUTCH_UPGRADE_STORAGE_1_2, NPC_BUTCH_UPGRA...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_2_2, NPC_BUTCH_UPGRADE_STORAGE_2_1, NPC_BUTCH_UPGRA...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_3_1, NPC_BUTCH_UPGRADE_STORAGE_3_3, NPC_BUTCH_UPGRA...` | 18 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_4_1, NPC_BUTCH_UPGRADE_STORAGE_4_3, NPC_BUTCH_UPGRA...` | 34 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 18 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_5_2, NPC_BUTCH_UPGRADE_STORAGE_5_1, NPC_BUTCH_UPGRA...` | 32 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_6`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_6_2, NPC_BUTCH_UPGRADE_STORAGE_6_3, NPC_BUTCH_UPGRA...` | 30 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 18 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_7`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_7_2, NPC_BUTCH_UPGRADE_STORAGE_7_3, NPC_BUTCH_UPGRA...` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_max1`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX1_3, NPC_BUTCH_UPGRADE_STORAGE_MAX1_2, NPC_BUTCH...` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 2 |

</details>

---

### Object: `upgrade_storage_max2`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX2_2, NPC_BUTCH_UPGRADE_STORAGE_MAX2_3, NPC_BUTCH...` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_max3`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX3_2, NPC_BUTCH_UPGRADE_STORAGE_MAX3_3, NPC_BUTCH...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_max4`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX4_3, NPC_BUTCH_UPGRADE_STORAGE_MAX4_2, NPC_BUTCH...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_max5`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX5_3, NPC_BUTCH_UPGRADE_STORAGE_MAX5_2, NPC_BUTCH...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_repeating_crazy`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Object: `upgrade_storage_repeating_hard`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Object: `upgrade_storage_repeating_impossible`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Object: `upgrade_storage_repeating_intro`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_3, NPC_BUTCH_UPGRADE_STORAGE_REPEAT...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 2 |

</details>

---

### Object: `upgrade_storage_repeating_normal`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Object: `use_attack_after_used_weapon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_attack, butch_point_weapon` | 8 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 8 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_1, NPC_POPUP_USE_ATTACK_AFTER_USED_WEA...` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_3` | 2 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `use_weapon` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `use_weapon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_weapon` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_USE_WEAPON_2, NPC_POPUP_USE_WEAPON_1` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_USE_WEAPON_3` | 2 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `use_attack_after_used_weapon` | 2 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 2 |
| `unlock_controls` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_boneyard`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BONEYARD_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BONEYARD_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_bunker`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BUNKER_2, NPC_TRACY_SHOP_WELCOME_BUNKER_1` | 4 |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BUNKER_3` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_caves`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CAVES_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CAVES_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_core`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CORE_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_crater`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CRATER_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CRATER_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_desert`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_DESERT_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_future`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_FUTURE_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_iceage`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_ICEAGE_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_ICEAGE_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_junkyard`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JUNKYARD_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_jurassic`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JURASSIC_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JURASSIC_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_lab`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_LAB_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_LAB_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_moon`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_MOON_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_sewers`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_SEWERS_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_SEWERS_2` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_theend`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_THEEND_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_THEEND_2` | 2 |
| [`set_npc_voice`](./Enums.md#enum-set_npc_voice) | Enum | Examples: `beanies` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_water`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_WATER_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

### Object: `welcome_water_cheap`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_WATER_CHEAP_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |

</details>

---

